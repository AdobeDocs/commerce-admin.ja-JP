---
title: 同期サービスの設定
description: Adobe Commerce プロジェクトとExperience Manager Assets プロジェクトをAssets ルールエンジンサービスに接続して、これら 2 つのシステム間のアセット同期を有効にする方法を説明します。
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# 同期サービスの設定

Asset Rules Engine Service （ARES）は、AEM AssetsとAdobe Commerceを統合するマルチテナントサービスです。 このサービスは、Adobe CommerceとExperience Manager間でアセットを同期します。 ARES サービスは、SKU またはその他の主要な属性に基づいて、AEM内のアセットをAdobe Commerce内の製品に自動的に照合します。 また、最新の製品アセットとバリエーションが、e コマースサイトで常に利用できるようにします。

サービスを設定するには、ARES GraphQL API を使用してテナント ID を登録し、アセットを同期するための一致規則を選択する必要があります。

## 一致する戦略を選択

CommerceのAEM Assets統合では、Adobe CommerceとAEM Assetsの間でアセットを同期するための 2 つの一致戦略をサポートしています。

- **MatchBySku** – これは、製品の最小在庫管理単位（SKU）に基づいてアセットを照合するデフォルトの照合ルールです。 SKU は、各製品の一意の ID です。 このルールは、アセットメタデータの SKU をCommerce製品 SKU と照合し、アセットが正しい製品に関連付けられていることを確認します。

- **ExternalMatcher** – このマッチングルールは、カスタムのマッチングロジックを必要とする、より複雑なシナリオや特定のビジネス要件に対するものです。 このルールを使用するには、アセットと商品のマッチング方法を定義するカスタムコードをAdobe Developer App Builderに実装する必要があります。

最初のオンボーディングでは、`MatchBySku` の戦略を使用します。 必要に応じて、後で一致する戦略を変更できます。

## テナントを登録

>[!BEGINSHADEBOX]

**前提条件**

- [AEM Assets プロジェクトは、アセット ](aem-assets-configure-aem.md) のマッピングに必要なCommerce メタデータで設定されています。

- [Adobe CommerceにExperience Manager Assets統合をインストールして設定します ](aem-assets-configure-commerce.md)。

>[!ENDSHADEBOX]

## 資格情報の収集

Commerce プロジェクト環境とAEM Assets プロジェクト環境をCommerce SaaS サービスで認証して接続するには、次の資格情報が必要です。

| 必須データ | Source | 検索場所 |
| ---------- | ------ | ------------- |
| Magentoアカウントからの API キー | Commerce | ステージングまたは実稼動で使用するCommerce環境の公開 API キーを指定します。 実稼動環境とステージング環境の API キーは、[Commerce サービスコネクタの設定 ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) ページ（管理）または「[!UICONTROL API Portal]」セクションの [!UICONTROL My Account] ページにあります。 |
| Commerce SaaS プロジェクト識別子 <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce管理者 | これらの値は、Commerce環境と、接続先の SaaS データ領域およびプロジェクトを特定します。 値は、[Commerce Services Connector SaaS Identifier configuration] から取得されます。（aem-assets-configure-commerce.md#configure-the-commerce-services-connector）。 |
| AEM `programId`<br>`environmentId` | [AEM Assets オーサリング環境 ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | AEM Sitesページを開き、「**[!UICONTROL Assets]**」を選択します。  次の URL からプロジェクト ID と環境 ID をコピーします。`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | Commerce ストアフロント | Commerce ストアフロントの [ ベース URL](../stores-purchase/store-urls.md)。 |
| API アクセス用の OAuth 認証情報 | Commerce管理者 | これらの資格情報は、Commerce[Assets統合の設定 ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) で確認できます。 |

## テナントを登録

認証資格情報とテナント ID を追加するリクエストをAssets ルールエンジンサービスに送信して、テナント登録を完了します。 リクエストには、サービス、Commerce プロジェクト、Experience Manager Assets プロジェクト間の接続を確立するために必要な、資格情報とプロジェクト識別子が含まれます。

GraphQL クライアントまたは cURL を使用してリクエストを送信します。

>[!BEGINTABS]

>[!TAB GraphQL リクエスト ]

GraphQL クライアントを使用して、API エンドポイント `https://commerce.adobe.io/assets-integration/graphql` にPOSTリクエストを送信します。

**必須ヘッダー**

リクエストに次の HTTP ヘッダーを指定します。

- `x-api-key`:Magentoアカウントの API キー
- `magento-environment-Id`: SaaS 識別子
- `x-gw-signature`:MAGEID に関連付けられた JWT トークン

**リクエスト：**

**構文**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**使用例**

テナントを登録し、`matchBySku` ルールを選択して、Adobe CommerceとAEM Assets プロジェクトの間でアセットをマッピングします。

**リクエスト：**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**応答**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cURL リクエスト ]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### 入力フィールド

#### AemInput

Commerce アセットを格納するAEM Assets インスタンスを識別します。 この情報は、Cloud Managerのマイプログラム ビューから、またはコンテンツオーサリング URL から取得できます。

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| `programId` | ストリング！ | AEM Cloud Service内のプロジェクトの一意の ID |
| `environmentId` | ストリング！ | 実稼動、ステージング、開発など、使用しているプロジェクト環境の ID |

#### CommerceInput

この入力フィールドには、Commerce カタログへの API アクセス用の OAuth 認証資格情報が入力されます。 これらの資格情報は、Commerce[Assets統合の設定 ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) で確認できます。

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| `baseUrl` | 文字列 | Commerce ストアフロントの [ ベース URL](../stores-purchase/store-urls.md)。 |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput)! | Commerce インスタンスにアクセスするための資格情報を指定します。 |
| `extensionVersion` | 文字列 | オプション。 Commerce インスタンスにインストールされているCommerce拡張機能のAEM Assets統合のバージョン。 |
| `version` | 文字列 | オプション。 Commerce インスタンスにインストールされているCommerce アプリケーションのバージョン。 |

#### CommerceCredentialsInput

この入力フィールドは、Commerce カタログへの API アクセス用の OAuth 認証情報を提供します。 これらの資格情報は、Commerce[Assets統合の設定 ](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release) で確認できます。

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| `accessToken` | ストリング！ | Assets統合用に生成されたアクセストークン。 |
| `accessTokenSecret` | ストリング！ | Assets統合用に生成されたアクセストークン秘密鍵。 |
| `consumerKey` | ストリング！ | Assets統合用に生成されたコンシューマーキー。 |
| `consumerSecret` | ストリング！ | Assets統合用に生成されたコンシューマーシークレット。 |

#### ExternalMatcherInput

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| assetToProductUrl | ストリング！ | <!--Add field description--> |
| productToAssetUrl | ストリング！ | <!--Add field description--> |
| 資格情報 | [ExternalMatcherCredentialsInput](#externalmatchercredentials)! | CommerceのAEM Assets統合用のApp Builder プロジェクトにアクセスするための資格情報。 |

#### ExternalMatcherCredentials

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| `oauthServerUrl` | ストリング！ |    |
| `clientId` | ストリング！ |      |
| `clientSecret` | ストリング！ |    |
| `imsOrgId` | ストリング！ | AEM AssetsとAdobe Commerceがプロビジョニングされている IMS 組織。 |

#### MatchBySkuRuleInput

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| metadataField | ストリング！ | 照合に使用するアセットメタデータフィールドを指定します。 `commerce:skus` の使用 |

#### RuleInput

Adobe CommerceとAEM Assets間のアセットの同期に使用する一致規則を指定します。

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | アセットのマッチング用に externalMatcher ルールを選択し、そのルールを使用するために必要なデータを指定します。 |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | アセットの照合に MatchBySkuRule を選択し、使用するために必要なデータを指定します。 |

#### RuleTypeInput

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| RuleType | 列挙 | CommerceのAEM Assets統合で使用できるアセット一致ルールのリストを指定します。 使用可能な値は、`matchBySKU` または `externalMatcher` です。 |

#### TenantInput

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| `aem` | [AemInput!](#aeminput) | は、Commerce アセットを保存するAEM Cloud Service内のAEM Assets インスタンスを識別します。 |
| `commerce` | [CommerceInput!](#commerceinput) | API アクセス用のCommerce プロジェクト情報および資格情報を提供します |
| `enabled` | ブール値！ | Adobe CommerceとAEM Assetsの間のアセット同期を有効または無効にします。 |
| `projectId` | ストリング！ | [Commerce サービスコネクタ SaaS Identifier configuration](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) の SaaS プロジェクト Id。 |
| `rule` | [RuleInput!](#ruleinput) | Adobe CommerceとAEM Assets間のアセットの同期に使用する一致規則を指定します。 `[matchBySkuRule](#matchbyskuruleinput)` または `[externalMatcher](#externalmatcherinput)` を指定します。 |

### 出力フィールド

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| データ | [registerTenant] | テナント登録情報とサーバーからのエラーメッセージを返します。 |

#### RegisterTenantResponse

| フィールド | データタイプ | 説明 |
| ----- | --------- | ----------- |
| tenantId | ストリング！ | 登録されたテナント ID を返します。 この ID は、CommerceのAEM Assets統合のデータが、Commerce環境に関連付けられた SaaS データ空間から保存および取得されるようにします。 |
| userErrors | [[userError!]!](#usererror) | リクエストによって生成されたエラーメッセージを返します。 |

#### UserError

| エラー | 説明 |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | このエラーは、`Magento-Environment-Id` ヘッダーで指定された環境 ID が IMS アカウントに割り当てられていない場合に発生します。 このエラーは、[Commerce サービスコネクタ ](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) がCommerce インスタンス用に設定されている際に、IMS アカウントが接続されなかったために発生する可能性があります。 |
| `Client ID is invalid` | `x-api-key` ヘッダーが正しくありません。 |
| `Client ID is missing` | `x-api-key` ヘッダーが指定されませんでした。 |
| `JWT is required` | `x-gw-signature` ヘッダーが指定されませんでした。 |
| `JWT is invalid` | `x-gw-signature` ヘッダーが指定されませんでした。 |
| `Tenant already exists` | 指定された `mageID` （JWT トークンから取得）および `saasId` （`Magento-Environment-Id` ヘッダーによって提供）を持つテナントが既に登録されています。 |
| `Unexpected error when connecting with AEM Assets` | このエラーは、`programId` 値または `environmentId` 値が無効または存在しないことが原因で発生します。 |
| `Unable to connect with AEM Assets` | このエラーには、次の 2 つの理由が考えられます。<br>1 AEM アセットアカウントは、Adobe Commerceに指定された IMS 組織 ID とは異なる IMS 組織 ID に関連付けられています。<br>2。 `commerce:isCommerce` のメタデータがAEM Assetsに存在しない場合は、AEM AssetsからCommerce インスタンスに送信する承認済みアセットがないことを示します。 |
| `Unexpected error when connecting with Commerce` | このエラーは、無効なコマース `baseURL` が指定された場合に発生します。 |
| `Unable to connect with Commerce, unauthorized` | 無効なコマース資格情報が指定されたため、不正なアクセスが発生しました。 |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | `Rule` フィールドの値が正しくありません。 RegisterTenant リクエストの場合、使用可能なルールタイプは、[RuleTypeInput](#ruletypeinput) 列挙によって定義されます。 |

## Experience Manager Assets統合の有効化

テナントを登録した後、オンボーディングプロセスの最後の手順として、管理者でExperience Manager Assets Integration for Commerce拡張機能を有効にします。

1. 拡張機能を有効にします。

   1. **ストア**/設定/**設定**/**カタログ** に移動します。

   1. **[!UICONTROL Catalog]** を選択して、カタログ設定を開きます。

   1. **[!UICONTROL AEM Assets integration]** を展開します。

   1. **[!UICONTROL Integration enabled]** を `yes` に設定します。

      ![Commerce管理者設定用のAEM Assets統合 ](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
