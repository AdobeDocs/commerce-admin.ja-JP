---
title: "[!DNL Audience Activation]"
description: Adobe CommerceでReal-Time CDP オーディエンスをアクティブ化して、ストアのパーソナライゼーションを促進する方法を説明します。
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: 9884d0991cceda7c2917f723467230d3702b2d0f
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---

# [!DNL Audience Activation]

この [!DNL Audience Activation] 拡張機能を使用すると、Adobe CommerceでReal-Time CDP オーディエンスをアクティブ化して、買い物かごに一意のオファーを作成できます。 これらのオファーとインセンティブには、一般的な e コマースマーチャンダイジング手法が含まれ、例えば次のようなものがあります _2 つ購入すると 1 つ無料_、その顧客に向けたヒーローバナーで、様々なオファーを通じて製品の価格を変更しました。 Real-Time CDP内に構築されるオーディエンスは、エンタープライズリソースプランニング（ERP）、顧客関係管理（CRM）、POS、マーケティングシステムなど、様々なエンタープライズシステムのデータに基づいています。 顧客セグメント情報は絶えず更新されるので、顧客はストアでの買い物の際にセグメントとの関連付けや関連付けの解除を行うことができます。

Luma ストアフロントまたは [ヘッドレス](#headless-support) ストアフロント。 Luma ストアフロントでは、オーディエンス情報（セグメントメンバーシップ）がCommerce側の cookie に保存されます。 ヘッドレスストアフロントでは、オーディエンス情報が、次の名前のパラメーターとしてGraphQL API ヘッダーに渡されます。 `aep-segments-membership`.

## リリースノート

この節では、Audience Activation拡張機能のアップデートについて説明します。アップデートには次のものが含まれます。

![新規](../assets/new.svg)  – 新機能
![修正](../assets/fix.svg)  – 修正点および改善点
![バグ](../assets/bug.svg)  – 既知の問題

参照： [今後のリリース](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) リリーススケジュールとサポートについて説明します。

詳しくは、開発者向けドキュメントを参照してください [製品の互換性について説明します](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## サポートされるサービスのアップデート

これらのリリースノートでは、Audience Activationで使用される拡張機能に関連する機能の変更と修正点について説明します。

+++サポートされているサービスのアップデート

_2023 年 8 月 15 日（Pt）_

![修正](../assets/fix.svg)  – が更新されました [Real-Time CDP Audiences ダッシュボード](#real-time-cdp-audiences-dashboard) フィルタリングを簡素化する。

_2023 年 6 月 27 日（Pt）_

![修正](../assets/fix.svg)  – に PHP 8.2 のサポートを追加しました `magento/module-data-services-graphql` パッケージ。

_2023 年 5 月 30 日（Pt）_

![新規](../assets/new.svg)  – が更新されました [Real-Time CDP Audiences ダッシュボード](#real-time-cdp-audiences-dashboard) Adobe Commerce インスタンス内のアクティブなオーディエンスを並べ替え、検索およびフィルタリングする機能を含めることができます。

+++

### 2.1.1

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2024 年 4 月 4 日（Pt）_

![新規](../assets/new.svg) - PHP 8.3 のサポートを追加。

### 2.2.0-beta1

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2024 年 2 月 16 日（Pt）_

![新規](../assets/new.svg) - ベータ版に参加している場合は、必ずを入手してください `composer.json` ファイルのルートレベルは次のとおりです。 ` "minimum-stability": "beta"`.
![新規](../assets/new.svg) - （**ベータ版**）作成する機能を追加しました [関連する製品ルール](../merchandising-promotions/product-related-rule-create.md) オーディエンス別に表示

### 2.1.0

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2024 年 1 月 24 日（Pt）_

![新規](../assets/new.svg)  – が更新されました [Real-Time CDP Audiences ダッシュボード](#real-time-cdp-audiences-dashboard) オーディエンスを含む web サイトを含め、これらのオーディエンスを使用するように設定されている動的ブロックと買い物かごの価格ルールを指定します。

### 2.0.1

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2023 年 11 月 16 日（Pt）_

![修正](../assets/fix.svg)  – 安定性の向上。

### 2.0.0

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2023 年 10 月 10 日（Pt）_

![新規](../assets/new.svg)  – 次の場合に OAuth 2.0 がサポートされるようになりました [設定](#configure-the-extension) Audience Activation拡張機能。
![修正](../assets/fix.svg)  – 安定性の向上。

### 1.2.0

[!BADGE 互換性]{type=Informative tooltip="互換性"}

_2023 年 8 月 15 日（Pt）_

![修正](../assets/fix.svg) - UI コンポーネントバージョンを更新しました。

### 1.1.0

_2023 年 5 月 30 日（Pt）_

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![新規](../assets/new.svg)  – のサポートを追加 [ダイナミック ブロック](#headless-support) ヘッドレスストアフロントで。

### 1.0.1

_2023 年 5 月 11 日（Pt）_

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![修正](../assets/fix.svg)  – 動的ブロックまたは買い物かごの価格ルールがストアフロントに適用されなかった問題を修正しました。
![修正](../assets/fix.svg) - マーチャントが動的ブロックを作成または更新しようとすると、Audience Activation拡張機能の未設定のインストールによってエラーが発生する問題を修正しました。

### 1.0.0

_2023 年 3 月 31 日（Pt）_

[!BADGE 互換性]{type=Informative tooltip="互換性"}

![新規](../assets/new.svg)  – 一般提供リリース

## 実装

次のタスクは、Luma とヘッドレスストアフロントの両方の実装に適用されます。 Adobe Commerceでオーディエンスをアクティブ化するには、次の操作を行う必要があります。

- Adobe Commerce バージョン 2.4.4 以降をインストールします。
- [Activate](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Real-Time CDPの宛先としてのAdobe Commerce
- [インストール](#install-the-extension) この [!DNL Audience Activation] 管理者の拡張機能
- [設定](#configure-the-extension) この [!DNL Audience Activation] 管理者の拡張機能

### 拡張機能のインストール

のインストール [!DNL Audience Activation] からの拡張機能 [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)または、次のコマンドを実行します。

```bash
composer require magento/audiences
```

### 拡張機能の設定

をインストールしたら、 [!DNL Audience Activation] 拡張機能を使用するには、Commerce管理者にログインし、次の手順を実行する必要があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [ログイン](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) をAdobeアカウントに追加し、組織 ID を選択します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. が含まれる **[!UICONTROL Datastream ID]** フィールドに、作成したデータストリームの ID を貼り付けます。 [有効化済み](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Real-Time CDPの宛先としてのAdobe Commerce。

   このデータストリームは、買い物客がオーディエンスに属しているかどうかを判断するために、Commerce web サイトからReal-Time CDPにデータを送信します。 まだデータストリームを作成していない場合、 [作成](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) 一人はExperience Platformに [add](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Real-Time CDPのCommerceの宛先に送信され、 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 管理者の拡張機能。

   >[!NOTE]
   >
   >データストリーム ID を指定すると、次のようになります [特定の web サイトへの関連付け](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) が含まれる [!DNL Data Connection] 拡張機能。 Commerce ストアに複数の web サイトがある場合、 [宛先の作成](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) Real-Time CDPの web サイトごとに異なるデータストリーム ID を使用します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. を展開 **[!UICONTROL Services]** を選択して、 **[!UICONTROL [!DNL Data Connection]]**.

1. [追加](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) サービスアカウントと資格情報の詳細。

## CommerceでReal-Time CDP オーディエンスを使用する場所

（を使用） [!DNL Audience Activation] 拡張機能を有効にすると、次のことが可能になります。

- [買い物かご価格ルールの作成](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) オーディエンス別に表示
- [ダイナミック ブロックを作成する](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) オーディエンス別に表示
- [（**ベータ版**）関連製品ルールを作成します](../merchandising-promotions/product-related-rule-create.md) オーディエンス別に表示

書き出し方法に関する完全なエンドツーエンドのユースケースについては、こちらを参照してください [!DNL Commerce] Real-Time CDPにデータを送信してオーディエンスを作成したあと、そのオーディエンスを次に対してアクティブ化します [!DNL Commerce]を参照してください [を使用した、Real-Time CDPでのオーディエンスの作成 [!DNL Commerce] イベントデータ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience).

## Real-Time CDP オーディエンスダッシュボード

すべて表示できます [アクティブ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) を使用して、Adobe Commerce インスタンス内でパーソナライズするために使用可能なオーディエンス **Real-Time CDP オーディエンス** ダッシュボード。

にアクセスするには **Real-Time CDP オーディエンス** ダッシュボードで、 _Admin_ サイドバーの後、に移動します。 **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Real-Time CDP Audiences ダッシュボード](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

ダッシュボードには、次のフィールドが含まれています。

| 列 | 説明 |
|--- |--- |
| `Hide filters` | ダッシュボードに適用できるフィルターの表示と非表示を切り替えることができます。 現在、適用できるフィルターはのみです。 `Last updated`. このフィルターを使用すると、オーディエンスの最終更新日に基づいてオーディエンスの日付範囲を選択できます。 |
| `Search` | Commerce インスタンス内のアクティブなオーディエンスを検索できます。 |
| `Name` | Real-Time CDPでオーディエンスに付与された名前。 |
| `Origin` | オーディエンスの元の場所を示します（例：） `Experience Platform`. |
| `Websites` | オーディエンスを使用するように設定されている web サイトを示します。 |
| `Dynamic Blocks` | オーディエンスを使用するように設定されている動的ブロックを示します。 |
| `Cart Price Rules` | オーディエンスを使用するように設定されている買い物かご価格ルールを示します。 |
| `Last updated` | オーディエンスがReal-Time CDPで変更された日時を示します。 |
| `Sync now` | 新規オーディエンスまたは更新されたオーディエンスをReal-Time CDPから取得します。 |
| `Customize table` | を表示または非表示にできます `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`、および `Last updated` 列。 |

{style="table-layout:auto"}

## ヘッドレスサポート

AEMやPWAなどのヘッドレス Adobe Commerce インスタンスでオーディエンスをアクティブ化して、買い物かごの価格ルール、関連する製品ルール、またはオーディエンスに基づく動的ブロックを表示できます。

### 買い物かご価格ルールおよび関連する製品ルール

Experience Platform買い物かごの価格ルールおよび関連する商品ルールの場合、ヘッドレスストアフロントは、 [Commerce integration framework（CIF）](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). このフレームワークは、GraphQLを使用して実装されるサーバーサイド API を提供します。 買い物客のセグメントなどのオーディエンス情報は、次の名前のGraphQL ヘッダーパラメーターを介してCommerceに渡されます。 `aep-segments-membership`.

全体的なアーキテクチャは次のとおりです。

![ヘッドレスストアフロントからバックエンドへのデータ送信](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

お先に [install](#install-the-extension) および [設定](#configure-the-extension) 拡張機能のExperience PlatformWeb SDK には、オーディエンス情報がセグメントメンバーシップの形式で含まれています。

これらのセグメントメンバーシップを SDK からキャプチャするには、こちらを参照してください [コードスニペット](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

取得後、これらのセグメントをGraphQLのヘッダー内でCommerceに渡すことができます。 例：

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### ダイナミック ブロック

ダイナミックブロックの場合、GraphQL `dynamicBlocks` クエリには、次を含めることができます `audience_id` 入力属性。 1 つ以上を指定する場合 `audience_id` a の値 `dynamicBlocks` クエリを実行すると、これらのオーディエンスに割り当てられた動的ブロックのリストが返されます。

#### 使用例

次のクエリは、複数のオーディエンス ID に関連付けられたすべてのダイナミックブロックを返します。

**リクエスト :**

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

の詳細情報 `dynamicBlocks` でのGraphQL クエリ [開発者向けドキュメント](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Adobe Experience Platform Mobile SDK を使用したオーディエンスの取得

Adobe Experience Platform Mobile SDK を使用して、Real-Time CDP オーディエンスを取得できます。

1. [インストール](#install-the-extension) Audience Activation拡張機能。
1. [モバイル Commerce サイトに SDK をインストールして設定します](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

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

データの取得後、それを使用して、オーディエンスに基づいたデータを作成できます [買い物かご価格ルール](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [ダイナミック ブロック](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) および  [関連する製品ルール](../merchandising-promotions/product-related-rule-create.md) Commerce アプリで上書きできます。

## オーディエンスがCommerceに表示されない

Real-Time CDP オーディエンスがCommerceに表示されない場合は、次の原因が考えられます。

- で選択された認証タイプが正しくありません **データ接続** 設定ページ
- 生成されたトークンに対する権限が不十分です

次の 2 つの節では、どちらの場合もトラブルシューティングを行う方法について説明します。

### 設定で選択された認証タイプが正しくありません

1. Commerce インスタンスを開きます。
1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. を展開 **[!UICONTROL Services]** を選択して、 **[!UICONTROL [!DNL Data Connection]]**.
1. で指定したサーバー間認証方法を確認します。 **[!UICONTROL Authentication Type]** フィールドが正しいこと。 Adobeでは、を使用することをお勧めします。 **OAuth**. JWT は非推奨（廃止予定）になりました。 [詳細情報](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### 生成されたトークンに対する権限が不十分です

この問題は、生成されたトークンに対する API 権限が不十分なために発生する可能性があります。 トークンに正しい権限があることを確認するには、次の手順に従います。

1. 組織内のAdobe Experience Platformのシステム管理者を特定します。
1. 使用するプロジェクトと資格情報を見つけます。
1. テクニカルアカウントのメールを特定します。例： `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. システム管理者にAdobe Experience Platformを起動してもらい、次の URL に移動します。 **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. 上記のテクニカルアカウントのメールを使用して、変更する資格情報を検索します。
1. 資格情報を開いてから、 **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. 追加 **実稼動のすべてのアクセス**.
1. クリック **[!UICONTROL Save]**.
1. [再生成](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) コンソールのアクセストークン。
1. トークンが、 [ターゲット接続 API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
