---
title: "[!DNL Audience Activation]"
description: Adobe CommerceでReal-Time CDP オーディエンスをアクティブ化して、ストアのパーソナライゼーションを促進する方法を説明します。
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: 39d49ac4efd4d00f0f8d22bf469126b748c08173
workflow-type: tm+mt
source-wordcount: '1565'
ht-degree: 1%

---

# [!DNL Audience Activation]

[!DNL Audience Activation] 拡張機能を使用すると、Adobe CommerceでReal-Time CDP オーディエンスをアクティブ化して、買い物かごに一意のオファーを作成できます。 これらのオファーとインセンティブには、_2 つ買うと 1 つ無料_ などの一般的な e コマースマーチャンダイジング手法、その顧客に向けたヒーローバナー、様々なオファーを通じた商品価格の変更が含まれます。 Real-Time CDP内に構築されるオーディエンスは、エンタープライズリソースプランニング（ERP）、顧客関係管理（CRM）、POS、マーケティングシステムなど、様々なエンタープライズシステムのデータに基づいています。 顧客セグメント情報は絶えず更新されるので、顧客はストアでの買い物の際にセグメントとの関連付けや関連付けの解除を行うことができます。

Luma ストアフロントまたは [ ヘッドレス ](#headless-support) ストアフロントでオーディエンスをアクティブ化できます。 Luma ストアフロントでは、オーディエンス情報（セグメントメンバーシップ）がCommerce側の cookie に保存されます。 ヘッドレスストアフロントでは、オーディエンス情報が、`aep-segments-membership` という名前のパラメーターとしてGraphQL API ヘッダーに渡されます。

## リリースノート

この節では、Audience Activation拡張機能のアップデートについて説明します。アップデートには次のものが含まれます。

![ 新機能 ](../assets/new.svg) – 新機能
![ 修正 ](../assets/fix.svg) – 修正点と改善点
![ バグ ](../assets/bug.svg) – 既知の問題

リリーススケジュールとサポートについては、[ 今後のリリース ](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) を参照してください。

詳しくは、開発者向けドキュメントの [ 製品の互換性について ](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) を参照してください。

## サポートされるサービスのアップデート

これらのリリースノートでは、Audience Activationで使用される拡張機能に関連する機能の変更と修正点について説明します。

+++サポートされているサービスのアップデート

_2023 年 8 月 15 日_

![ 修正 ](../assets/fix.svg) - フィルタリングを簡素化するために、[Real-Time CDP オーディエンスダッシュボード ](#real-time-cdp-audiences-dashboard) を更新しました。

_2023 年 6 月 27 日_

![ 修正 ](../assets/fix.svg) - `magento/module-data-services-graphql` パッケージに PHP 8.2 のサポートが追加されました。

_2023 年 5 月 30 日_

![ 新規 ](../assets/new.svg) - [Real-Time CDP オーディエンスダッシュボード ](#real-time-cdp-audiences-dashboard) を更新し、Adobe Commerce インスタンス内のアクティブなオーディエンスの並べ替え、検索、フィルタリング機能を追加しました。

+++

### 2.3.1

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 11 月 12 日_

![ 修正 ](../assets/fix.svg) – 選択可能なReal-Time CDP オーディエンスをフィルタリングする際の問題を修正しました。

### 2.3.0

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 7 月 29 日_

![ 新規 ](../assets/new.svg) - コマンドライン構文が追加され、Adobe Experience Platformからオーディエンスデータを取り込むために更新する必要があるかどうかを判断するために [ 資格情報をテスト ](#validate-the-connection) できるようになりました。

### 2.2.0

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 6 月 12 日_

![ 新規 ](../assets/new.svg) - オーディエンス別に情報を提供する [ 関連製品ルール ](../merchandising-promotions/product-related-rule-create.md) の一般公開（GA）リリース。

### 2.1.1

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 4 月 4 日_

![ 新規 ](../assets/new.svg) - PHP 8.3 のサポートを追加。

### 2.2.0-beta1

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 2 月 16 日_

![ 新規 ](../assets/new.svg) - ベータ版に参加している場合は、`composer.json` ファイルのルートレベルに次のものが含まれていることを確認してください：` "minimum-stability": "beta"`。
![ 新規 ](../assets/new.svg) - （**Beta**）オーディエンスに基づいて [ 関連商品ルール ](../merchandising-promotions/product-related-rule-create.md) を作成する機能が追加されました。

### 2.1.0

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2024 年 1 月 24 日_

![ 新規 ](../assets/new.svg) - [Real-Time CDP Audiences ダッシュボード ](#real-time-cdp-audiences-dashboard) が更新されて、オーディエンスを含む web サイトが含まれ、これらのオーディエンスを使用するように設定された動的ブロックと買い物かご価格ルールが指定されました。

### 2.0.1

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2023 年 11 月 16 日_

![ 修正 ](../assets/fix.svg) – 安定性が向上しました。

### 2.0.0

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2023 年 10 月 10 日_

![ 新規 ](../assets/new.svg) - Audience Activation拡張機能を [ 設定 ](#configure-the-extension) する際に、OAuth 2.0 がサポートされるようになりました。
![ 修正 ](../assets/fix.svg) – 安定性が向上しました。

### 1.2.0

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

_2023 年 8 月 15 日_

![ 修正 ](../assets/fix.svg) - UI コンポーネントのバージョンを更新しました。

### 1.1.0

_2023 年 5 月 30 日_

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

![ 新規 ](../assets/new.svg) - ヘッドレスストアフロントで [ 動的ブロック ](#headless-support) のサポートを追加しました。

### 1.0.1

_2023 年 5 月 11 日_

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

![ 修正 ](../assets/fix.svg) – 動的ブロックまたは買い物かごの価格ルールがストアフロントに適用されなかった問題を修正しました。
![ 修正 ](../assets/fix.svg) - マーチャントが動的ブロックを作成または更新しようとすると、Audience Activation拡張機能の未設定のインストールがエラーを引き起こす問題を修正しました。

### 1.0.0

_2023 年 3 月 31 日_

[!BADGE  互換性 ]{type=Informative tooltip="互換性"}

![ 新規 ](../assets/new.svg) – 一般提供リリース

## 実装

次のタスクは、Luma とヘッドレスストアフロントの両方の実装に適用されます。 Adobe Commerceでオーディエンスをアクティブ化するには、次の操作を行う必要があります。

- Adobe Commerce バージョン 2.4.4 以降をインストールします。
- Real-Time CDPの宛先としてのAdobe Commerce](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html)[ アクティブ化
- 管理者の [!DNL Audience Activation] 拡張機能 ](#install-the-extension) インストール [
- 管理者の [!DNL Audience Activation] 拡張機能 [ 設定 ](#configure-the-extension)

### 拡張機能のインストール

[Marketplace](https://commercemarketplace.adobe.com/magento-audiences.html) から [!DNL Audience Activation] 拡張機能をインストールするか、次のコマンドを実行します。

```bash
composer require magento/audiences
```

### 拡張機能の設定

[!DNL Audience Activation] 拡張機能をインストールした後、Commerce管理者にログインして、次の手順を実行する必要があります。

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Services]_/**[!UICONTROL Commerce Services Connector]**に移動します。

1. Adobeアカウントに [ ログイン ](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) し、組織 ID を選択します。

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Services]_/**[!UICONTROL [!DNL Data Connection]]**に移動します。

1. 「**[!UICONTROL Datastream ID]**」フィールドに、Adobe CommerceをReal-Time CDPの宛先として [ アクティブ化 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) したときに作成したデータストリームの ID を貼り付けます。

   このデータストリームは、買い物客がオーディエンスに属しているかどうかを判断するために、Commerce web サイトからReal-Time CDPにデータを送信します。 まだデータストリームを作成していない場合は、Experience Platformで [create](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) 1 つ、Real-Time CDPのCommerceの宛先および管理者の [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 拡張機能に [add](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) します。

   >[!NOTE]
   >
   >データストリーム ID を指定するときは、[!DNL Data Connection] 拡張機能で [ 特定の web サイトに関連付ける ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) ことができます。 Commerce ストアに複数の web サイトがある場合は、Real-Time CDPの web サイトごとに [ 宛先を作成 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) し、それぞれに異なるデータストリーム ID を使用します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 「**[!UICONTROL Services]**」を展開し、「**[!UICONTROL [!DNL Data Connection]]**」を選択します。

1. [ 追加 ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) サービスアカウントと資格情報の詳細。

## CommerceでReal-Time CDP オーディエンスを使用する場所

[!DNL Audience Activation] 拡張機能を有効にすると、次のことができます。

- オーディエンスに基づく [ 買い物かご価格ルールの作成 ](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)
- オーディエンスに基づく [ 動的ブロックの作成 ](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks)
- オーディエンスに基づく [ 関連製品ルール ](../merchandising-promotions/product-related-rule-create.md) 作成

>[!TIP]
>
>[!DNL Commerce] データをReal-Time CDPに書き出してオーディエンスを作成し、そのオーディエンスを [!DNL Commerce] にアクティブ化する方法に関する詳細なエンドツーエンドのユースケースについては、[ イベントデータを使用したReal-Time CDPでのオーディエンスの作成  [!DNL Commerce] ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) を参照してください。

## Real-Time CDP オーディエンスダッシュボード

[2}Real-Time CDP オーディエンス ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) ダッシュボードを使用すると、Adobe Commerce インスタンス内でパーソナライズするために使用できるすべての **アクティブな } オーディエンスを表示できます。**

**Real-Time CDP オーディエンス** ダッシュボードにアクセスするには、_管理者_ サイドバーで **[!UICONTROL Customers]**/**[!UICONTROL Real-time CDP Audience]** に移動します。

![Real-Time CDP オーディエンスダッシュボード ](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

ダッシュボードには、次のフィールドが含まれています。

| 列 | 説明 |
|--- |--- |
| `Hide filters` | ダッシュボードに適用できるフィルターの表示と非表示を切り替えることができます。 現在、適用できるフィルターは `Last updated` のみです。 このフィルターを使用すると、オーディエンスの最終更新日に基づいてオーディエンスの日付範囲を選択できます。 |
| `Search` | Commerce インスタンス内のアクティブなオーディエンスを検索できます。 |
| `Name` | Real-Time CDPでオーディエンスに付与された名前。 |
| `Origin` | オーディエンスの元の場所を示します（`Experience Platform` など）。 |
| `Websites` | オーディエンスを使用するように設定されている web サイトを示します。 |
| `Dynamic Blocks` | オーディエンスを使用するように設定されている動的ブロックを示します。 |
| `Cart Price Rules` | オーディエンスを使用するように設定されている買い物かご価格ルールを示します。 |
| `Related Product Rules` | オーディエンスを使用するように設定されている関連製品ルールを示します。 |
| `Last updated` | オーディエンスがReal-Time CDPで変更された日時を示します。 |
| `Sync now` | 新規オーディエンスまたは更新されたオーディエンスをReal-Time CDPから取得します。 |
| `Customize table` | `Origin`、`Websites`、`Dynamic Blocks`、`Cart Price Rules`、`Last updated` の列の表示/非表示を切り替えることができます。 |

{style="table-layout:auto"}

## ヘッドレスサポート

AEMやPWAなどのヘッドレス Adobe Commerce インスタンスでオーディエンスをアクティブ化して、買い物かごの価格ルール、関連する製品ルール、またはオーディエンスに基づく動的ブロックを表示できます。

### 買い物かご価格ルールおよび関連する製品ルール

買い物かごの価格ルールおよび関連する商品ルールの場合、ヘッドレスストアフロントは、[Commerce integration framework（CIF） ](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html) を通じてExperience Platformと通信します。 このフレームワークは、GraphQLを使用して実装されるサーバーサイド API を提供します。 買い物客のセグメントなどのオーディエンス情報は、`aep-segments-membership` という名前のGraphQL ヘッダーパラメーターを介してCommerceに渡されます。

全体的なアーキテクチャは次のとおりです。

![ ヘッドレスストアフロントからバックエンドへのデータ送信 ](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

拡張機能を [ インストール ](#install-the-extension) および [ 設定 ](#configure-the-extension) した後、Experience Platform Web SDK には、セグメントメンバーシップの形式でオーディエンス情報が含まれます。

SDK からこれらのセグメントメンバーシップをキャプチャするには、この [ コードスニペット ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes) を参照してください。

取得後、これらのセグメントをGraphQLのヘッダー内でCommerceに渡すことができます。 例：

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### ダイナミック ブロック

ダイナミックブロックの場合、GraphQL `dynamicBlocks` クエリには `audience_id` input 属性を含めることができます。 `dynamicBlocks` クエリで 1 つ以上の `audience_id` 値を指定すると、それらのオーディエンスに割り当てられた動的ブロックのリストが返されます。

#### 使用例

次のクエリは、複数のオーディエンス ID に関連付けられたすべてのダイナミックブロックを返します。

**リクエスト：**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**応答：**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

`dynamicBlocks` GraphQL クエリについて詳しくは、[developer ドキュメント ](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/) を参照してください。

## Adobe Experience Platform Mobile SDK を使用したオーディエンスの取得

Adobe Experience Platform Mobile SDK を使用して、Real-Time CDP オーディエンスを取得できます。

1. [ インストール ](#install-the-extension) Audience Activation拡張機能。
1. [ モバイル Commerce サイトに SDK をインストールして設定します ](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html)。

>[!IMPORTANT]
>
>Adobe Experience Platform Mobile SDK for iOSは、iOS 11 以降をサポートしています。

設定が完了したら、Mobile SDK 操作を使用してオーディエンスデータを取得します。 例：

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

データが取得されたら、それを使用して、オーディエンスに基づいた [ 買い物かご価格ルール ](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)、[ 動的ブロック ](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) および [ 関連の商品ルール ](../merchandising-promotions/product-related-rule-create.md) をCommerce アプリ内に作成できます。

## オーディエンスがCommerceに表示されない

Real-Time CDP オーディエンスがCommerceに表示されない場合は、次の原因が考えられます。

- 無効な接続
- **データ接続** 設定ページで選択された認証タイプが正しくありません
- 生成されたトークンに対する権限が不十分です

次の節では、これらの問題のトラブルシューティング方法について説明します。

### 接続の検証

資格情報とAdobe Experience Platformからの応答を検証するには、次のコマンドを実行します。

```bash
bin/magento audiences:config:status
```

このコマンドは、接続ステータスを返します。 `-v` フラグを追加して、より冗長にします。

```
./bin/magento audiences:config:status -v  
```

例：

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### 設定で選択された認証タイプが正しくありません

1. Commerce インスタンスを開きます。
1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。
1. 「**[!UICONTROL Services]**」を展開し、「**[!UICONTROL [!DNL Data Connection]]**」を選択します。
1. **[!UICONTROL Authentication Type]** フィールドに指定したサーバー間の認証方法が正しいことを確認してください。 Adobeでは **OAuth** を使用することをお勧めします。 JWT は非推奨（廃止予定）になりました。 [ 詳細情報 ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/)。

### 生成されたトークンに対する権限が不十分です

この問題は、生成されたトークンに対する API 権限が不十分なために発生する可能性があります。 トークンに正しい権限があることを確認するには、次の手順に従います。

1. 組織内のAdobe Experience Platformのシステム管理者を特定します。
1. 使用するプロジェクトと資格情報を見つけます。
1. テクニカルアカウントのメールを識別します（例：`fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`）。
1. システム管理者にAdobe Experience Platformを起動してもらい、**[!UICONTROL Permissions]**/**[!UICONTROL Users]**/**[!UICONTROL API credentials]** に移動します。
1. 上記のテクニカルアカウントのメールを使用して、変更する資格情報を検索します。
1. 資格情報を開き、**[!UICONTROL Roles]** / **[!UICONTROL Add roles]** を選択します。
1. 権限を含む役割 **[!UICONTROL Manage destinations]** 追加します。
1. 「**[!UICONTROL Save]**」をクリックします。
1. コンソールのアクセストークンを [ 再生成 ](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) します。
1. [ ターゲット接続 API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections) を使用して、トークンが有効な応答を提供することを確認します。
