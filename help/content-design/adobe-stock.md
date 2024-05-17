---
title: Adobe Stockの統合
description: Adobe Stockとの統合 [!DNL Commerce] ストア内で使用する無数のメディアアセットにアクセスするためのインスタンス。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Adobe Stockの統合

ストアで使用する無数のメディアアセットにアクセスするには、次を統合します。 [Adobe Stock][adobe-stock] （を使用） [!UICONTROL Commerce].

![Adobe Stockの検索結果](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock サービスは、あらゆるクリエイティブプロジェクトに使用できる、何百万点もの質の高い選ばれたロイヤリティーフリーの写真、ベクター、イラスト、ビデオ、テンプレートおよび 3D アセットを提供します。 [!DNL Commerce] Adobe Stock アセットをすばやく検索、プレビュー、ライセンス付与することができます。 ユーザーは、以下に保存することもできます [メディアストレージ][media-storage]管理ワークスペースから移動せずに実行できます。

## 前提条件

この統合には次が必要です。

- An [Adobe Developer][dev-console] アカウント
- Adobe CommerceまたはMagento Open Source、2.3.4 以降

Adobe Stock イメージのライセンスを取得するには、次の操作が必要です。

- An [Adobeアカウント][adobe-signin]
- 有給 [Adobe Stock][adobe-stock] アカウントに関連付けられたプラン

## の統合 [!DNL Commerce] とAdobe Stock

Adobe Stock統合をAdobe Commerce用に設定するには、次の 2 つの手順があります。

1. [adobe.developer 統合の作成](#create-an-adobe-developer-integration) api キーを生成するには
1. [Commerce Admin でのAdobe Stock統合の設定](#configure-the-adobe-stock-integration)

### Adobe Developer統合の作成

1. に移動します。 [Adobe Developer コンソール][dev-console].

1. 次の下 _[!UICONTROL Quick Start]_を選択し、**[!UICONTROL Create new project]**.

1. が含まれる _[!UICONTROL Project overview]_ブロック、クリック&#x200B;**[!UICONTROL Add API]**.

1. を選択 **[!UICONTROL Adobe Stock]** 統合リストから、次の順にクリックします **[!UICONTROL Next]**.

1. Oauth 2.0 を選択します。 **[!UICONTROL Web App]**.

1. を指定 **[!UICONTROL redirect URI]**.

   デフォルトのリダイレクト URI の形式は次のとおりです `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`（例：） `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`。ここで、

   - `${HOST}` が自分 [!DNL Commerce] 完全修飾ドメイン名（例：） `https://store.myshop.com`）に設定します。
   - `${ADMIN_URI}` が自分 [!DNL Commerce] 管理 URI （など） `admin_hgkq1l`）、次を実行して取得できます。 `magento info:adminuri`.

1. を指定 **[!UICONTROL Redirect URI pattern]**（リダイレクト URI と同じですが、次の 2 つの違いがあります。）

   - 任意の期間（`.`）は、2 つのバックスラッシュ（`\\`）に設定します。
   - 追加 `.*` をパターンの最後まで追加します。

   前のデフォルトのリダイレクト URI の例を使用すると、次のようになります `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. クリック **[!UICONTROL Next]**.

1. 使用可能な範囲を確認し、 **[!UICONTROL Save configured API]**.

1. 次のページで、 **[!UICONTROL Client ID]** （API キー）と **[!UICONTROL Client secret]**.

   この情報は、次の節の手順で使用します。

### Adobe Stock統合の設定

でシステム設定を指定するには [!DNL Commerce] 管理者、を使用する _API キー_ および _クライアント秘密鍵_ 生成日時： [前のセクション][create-integration].

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** 次の手順を実行します。

   - を設定 **[!UICONTROL Enabled Adobe Stock]** 対象： `Yes`.

   - を入力 **[!UICONTROL API Key (Client ID)]**.

   - を入力 **[!UICONTROL Client Secret]**.

   - クリック **[!UICONTROL Test Connection]** キーを検証します。

   ![詳細設定 – Adobe Stockの統合](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   検証を数秒間行います。 資格情報が有効な場合は、緑のマークが表示されます _接続に成功しました。_ メッセージ。

1. 完了したら、 **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
