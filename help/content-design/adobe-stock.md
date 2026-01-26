---
title: Adobe Stockの統合
description: Adobe Stockをお使いのインスタンスと統合して  [!DNL Commerce]  ストアで使用するための無数のメディアアセットにアクセスできるようにします。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 9aec049cfaa12f342d66f45a75af0ce50a23c2c8
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Adobe Stockの統合

ストアで使用する無数のメディアアセットにアクセスするには、[Adobe Stock](https://stock.adobe.com) を [!UICONTROL Commerce] と統合します。

![Adobe Stock検索結果 &#x200B;](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock サービスは、あらゆるクリエイティブプロジェクトに使用できる、何百万点もの質の高い選ばれたロイヤリティーフリーの写真、ベクター、イラスト、ビデオ、テンプレートおよび 3D アセットを提供します。 [!DNL Commerce] ユーザーは、Adobe Stock アセットをすばやく検索、プレビューおよびライセンス付与することができます。 また、ユーザーは、管理ワークスペースを離れることなく、すべてを [&#x200B; メディアストレージ &#x200B;](./media-storage.md) に保存できます。

## 前提条件

この統合には次が必要です。

- [Adobe Developer](https://developer.adobe.com/console/home) アカウント
- Adobe CommerceまたはMagento Open Source, 2.3.4 以降

Adobe Stock イメージのライセンスを取得するには、次の操作が必要です。

- [Adobe アカウント &#x200B;](https://helpx.adobe.com/jp/manage-account/using/access-adobe-id-account.html)
- アカウントに関連付けられた有料の [Adobe Stock](https://stock.adobe.com) プラン

## [!DNL Commerce] とAdobe Stockの統合

Adobe Stock統合をAdobe Commerce用に設定するには、次の 2 つの手順があります。

1. [adobe.developer 統合を作成 &#x200B;](#create-an-adobe-developer-integration) して API キーを生成
1. [Commerce Admin でのAdobe Stock統合の設定](#configure-the-adobe-stock-integration)

### Adobe Developer統合の作成

1. [Adobe Developer Console](https://developer.adobe.com/console/home) に移動します。

1. [_[!UICONTROL Quick Start]_] で、[**[!UICONTROL Create new project]**] をクリックします。

1. _[!UICONTROL Project overview]_&#x200B;ブロックで、「**[!UICONTROL Add API]**」をクリックします。

1. 統合リストから「**[!UICONTROL Adobe Stock]**」を選択し、「**[!UICONTROL Next]**」をクリックします。

1. 「OAuth 2.0 **[!UICONTROL Web App]**」を選択します。

1. **[!UICONTROL redirect URI]** を指定してください

   デフォルトのリダイレクト URI の形式は `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/` です。例えば `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/` です。

   - `${HOST}` は、[!DNL Commerce] の完全修飾ドメイン名（例：`https://store.myshop.com`）です。
   - `${ADMIN_URI}` は [!DNL Commerce] の管理者 URI （`admin_hgkq1l` など）で、`magento info:adminuri` を実行して取得できます。

1. **[!UICONTROL Redirect URI pattern]** を指定します。これは、リダイレクト URI と同じですが、次の 2 つの違いがあります。

   - ピリオド（`.`）は、2 つのバックスラッシュ（`\\`）でエスケープする必要があります。
   - パターンの最後に `.*` を追加します。

   前のデフォルトのリダイレクト URI の例を使用すると、パターンは `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*` のようになります

1. 「**[!UICONTROL Next]**」をクリックします。

1. 使用可能な範囲を確認し、「**[!UICONTROL Save configured API]**」をクリックします。

1. 次のページで、**[!UICONTROL Client ID]** （API キー）と **[!UICONTROL Client secret]** をコピーします。

   この情報は、次の節の手順で使用します。

### Adobe Stock統合の設定

[!DNL Commerce] Admin でシステム設定を設定するには、_前の節_ で生成した _API キー_ と [&#x200B; クライアントシークレット &#x200B;](#create-an-adobeio-integration) を使用します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. ![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) を展開し **[!UICONTROL Adobe Stock Integration]** 以下を実行します。

   - **[!UICONTROL Enabled Adobe Stock]** を `Yes` に設定します。

   - **[!UICONTROL API Key (Client ID)]** を入力します。

   - **[!UICONTROL Client Secret]** を入力します。

   - 「**[!UICONTROL Test Connection]**」をクリックしてキーを検証します。

   ![&#x200B; 詳細設定 – Adobe Stockの統合 &#x200B;](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   検証を数秒間行います。 資格情報が有効な場合は、緑色の _接続に成功しました！_ メッセージ。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
