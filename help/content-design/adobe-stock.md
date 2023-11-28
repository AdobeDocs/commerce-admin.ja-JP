---
title: Adobe Stock統合
description: Adobe Stockとの統合 [!DNL Commerce] ストアで使用する無数のメディアアセットにアクセスするためのインスタンス。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock統合

ストアで使用する数え切れないほどのメディアアセットにアクセスするには、を統合します。 [Adobe Stock][adobe-stock] 次を使用 [!UICONTROL Commerce].

![Adobe Stock Search Results](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stockサービスは、数百万もの高品質で厳選されたロイヤリティフリーの写真、ベクター、イラスト、ビデオ、テンプレート、3D アセットに、あらゆるクリエイティブプロジェクトでアクセスできるサービスです。 [!DNL Commerce] Adobe Stock assets の検索、プレビュー、ライセンスの取得をすばやくおこなうことができます。 ユーザーは、これらを [メディアストレージ][media-storage]（すべて、管理ワークスペースから移動しないで）。

## 前提条件

この統合には、以下が必要です。

- An [Adobe Developer][dev-console] アカウント
- Adobe CommerceまたはMagento Open Source, 2.3.4 以降

Adobe Stock画像のライセンスを取得するには、以下が必要です。

- An [Adobeアカウント][adobe-signin]
- 有料 [Adobe Stock][adobe-stock] アカウントに関連付けられたプラン

## 統合 [!DNL Commerce] とAdobe Stock

Adobe Commerce用のAdobe Stock統合の設定は、次の 2 つの手順で構成されます。

1. [adobe.developer 統合の作成](#create-an-adobe-developer-integration) API キーを生成するには、以下を実行します。
1. [コマース管理でのAdobe Stock統合の設定](#configure-the-adobe-stock-integration)

### Adobe Developer統合の作成

1. 次に移動： [Adobe Developer Console][dev-console].

1. の下 _[!UICONTROL Quick Start]_をクリックし、**[!UICONTROL Create new project]**.

1. Adobe Analytics の _[!UICONTROL Project overview]_ブロック、クリック&#x200B;**[!UICONTROL Add API]**.

1. 選択 **[!UICONTROL Adobe Stock]** 「統合」リストで、「 **[!UICONTROL Next]**.

1. OAuth 2.0 を選択します。 **[!UICONTROL Web App]**.

1. 次を指定します。 **[!UICONTROL redirect URI]**.

   デフォルトのリダイレクト URI はフォーム内にあります `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`、例： `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`、ここで、

   - `${HOST}` は、 [!DNL Commerce] 完全修飾ドメイン名（例： ） `https://store.myshop.com`) をクリックします。
   - `${ADMIN_URI}` は、 [!DNL Commerce] 管理 URI ( 例： `admin_hgkq1l`) で始まり、 `magento info:adminuri`.

1. 次を指定します。 **[!UICONTROL Redirect URI pattern]**（2 つの違いがある場合、リダイレクト URI と同じです）。

   - 任意のピリオド (`.`) は 2 つのバックスラッシュ (`\\`) をクリックします。
   - 追加 `.*` をパターンの最後に追加します。

   以前のデフォルトのリダイレクト URI の例を使用すると、次のようになります。 `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. クリック **[!UICONTROL Next]**.

1. 使用可能なスコープを確認し、 **[!UICONTROL Save configured API]**.

1. 次のページで、 **[!UICONTROL Client ID]** （API キー）および **[!UICONTROL Client secret]**.

   この情報は、次の節の手順で使用します。

### Adobe Stock統合の設定

システム設定を [!DNL Commerce] 管理者、 _API キー_ および _クライアント秘密鍵_ 生成された [前のセクション][create-integration].

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** 次の操作を実行します。

   - 設定 **[!UICONTROL Enabled Adobe Stock]** から `Yes`.

   - を入力します。 **[!UICONTROL API Key (Client ID)]**.

   - を入力します。 **[!UICONTROL Client Secret]**.

   - クリック **[!UICONTROL Test Connection]** をクリックして、鍵を検証します。

   ![高度な設定 — Adobe Stock統合](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   検証に数秒を要します。 資格情報が有効な場合は、緑色で表示されます _接続に成功しました。_ メッセージ。

1. 完了したら、「 **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
