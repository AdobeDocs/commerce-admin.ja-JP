---
title: WYSIWYG Editor
description: エディターを使用し、_What You See Is What You Get_（WYSIWYG）ビューでコンテンツを操作する方法について説明します。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# WYSIWYG Editor

エディターを使用すると、コンテンツの _What You See Is What You Get_ （WYSIWYG）ビューでの作業中に、入力や書式設定をおこなうことができます。 基になるHTML コードを直接操作する場合は、モードを簡単に変更できます。 エディターを使用して、[&#x200B; ページ &#x200B;](pages.md)、[&#x200B; ブロック &#x200B;](blocks.md) および [&#x200B; 製品説明 &#x200B;](../catalog/product-content.md) のコンテンツを作成できます。 製品の詳細を操作する場合は、「」をクリックしてエディターにアクセス **[!UICONTROL Show / Hide Editor]** ます。

![&#x200B; エディターツールバー &#x200B;](./assets/editor-toolbar.png){width="700" zoomable="yes"}

以下のトピックでは、エディターの使用について詳しく説明します。

- [リンクの挿入](editor-insert-link.md)
- [画像の挿入](editor-insert-image.md)
- [ウィジェットの挿入](editor-widget.md)
- [変数の挿入](editor-insert-variable.md)

## エディターの設定

WYSIWYG エディターはデフォルトで有効になっており、CMSのページやブロックおよび商品やカテゴリのコンテンツを編集するために使用できます。 設定からエディターをアクティブ化または非アクティブ化し、製品やカテゴリの説明でメディアコンテンツの URL を [&#x200B; 動的 &#x200B;](../catalog/catalog-urls.md#dynamic-url) ではなく静的に使用することを選択できます。

![WYSIWYG オプション &#x200B;](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

すべてのWYSIWYG オプションについて詳しくは、[&#x200B; 設定リファレンス &#x200B;](../configuration-reference/general/content-management.md) の _コンテンツ管理_ を参照してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]** を展開します。

1. **[!UICONTROL Enable WYSIWYG Editor]** を好みに合わせて設定します。

   このエディターは、デフォルトで有効になっています。

1. WYSIWYG エディターで入力するすべての [&#x200B; メディアコンテンツ &#x200B;](../catalog/catalog-urls.md#static-url) に対して、環境設定に **[!UICONTROL Static URLs for Media Content in WYSIWYG]** を設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
