---
title: WYSIWYG エディター
description: エディターを使用し、_What You See Is What You Get_（WYSIWYG）ビューでコンテンツを操作する方法を説明します。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# WYSIWYG エディター

エディターを使用すると、コンテンツの _表示内容は取得内容である_ （WYSIWYG）ビューで作業しながら、入力や書式設定を行うことができます。 基になるHTMLコードを直接操作する場合は、モードを簡単に変更できます。 エディターを使用して、[ ページ ](pages.md)、[ ブロック ](blocks.md) および [ 製品説明 ](../catalog/product-content.md) のコンテンツを作成できます。 製品の詳細を操作する場合は、「」をクリックしてエディターにアクセス **[!UICONTROL Show / Hide Editor]** ます。

>[!NOTE]
>
>TinyMCE 5 はデフォルトの WYSIWYG エディタです。 Adobe CommerceおよびMagento Open Source 2.4.5 の TinyMCE 5.10 ライブラリを更新すると、一部の種類の URL を使用して画像やリンクを更新する際に、任意のJavaScriptを実行できる脆弱性が解決されます。 TinyMCE 3 は 2.4.0 リリースで非推奨（廃止予定）となり、2.4.3 リリースで削除されました。 TinyMCE 4 は 2.4.4 リリースで削除されました。

![ エディターツールバー ](./assets/editor-toolbar.png){width="700" zoomable="yes"}

以下のトピックでは、エディターの使用について詳しく説明します。

- [リンクの挿入](editor-insert-link.md)
- [画像の挿入](editor-insert-image.md)
- [ウィジェットの挿入](editor-widget.md)
- [変数の挿入](editor-insert-variable.md)

## エディターの設定

WYSIWYG エディターはデフォルトで有効になっており、CMS ページやブロック、製品およびカテゴリのコンテンツを編集するために使用できます。 設定からエディターをアクティブ化または非アクティブ化し、製品やカテゴリの説明でメディアコンテンツの URL を [ 動的 ](../catalog/catalog-urls.md#dynamic-url) ではなく静的に使用することを選択できます。

![WYSIWYG オプション ](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

すべての WYSIWYG オプションについて詳しくは、[ 設定リファレンス ](../configuration-reference/general/content-management.md) の _コンテンツ管理_ を参照してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Content Management]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]** を展開します。

1. **[!UICONTROL Enable WYSIWYG Editor]** を好みに合わせて設定します。

   このエディターは、デフォルトで有効になっています。

1. WYSIWYG エディター **[!UICONTROL Static URLs for Media Content in WYSIWYG]** 入力されるすべての [ メディアコンテンツ ](../catalog/catalog-urls.md#static-url) の環境設定に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
