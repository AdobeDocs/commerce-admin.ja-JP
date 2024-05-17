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

エディターを使用すると、での作業中に入力や書式設定をおこなうことができます。 _目に付くものが手に入る_ コンテンツの（WYSIWYG）ビュー。 基になるHTMLコードを直接操作する場合は、モードを簡単に変更できます。 エディターを使用して、のコンテンツを作成できます [ページ](pages.md), [ブロック](blocks.md)、および [製品の説明](../catalog/product-content.md). 製品詳細を操作する場合は、をクリックしてエディターにアクセスします。 **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 はデフォルトの WYSIWYG エディタです。 Adobe CommerceおよびMagento Open Source 2.4.5 の TinyMCE 5.10 ライブラリを更新すると、一部の種類の URL を使用して画像やリンクを更新する際に、任意の JavaScript 実行が許可される脆弱性が解決されます。 TinyMCE 3 は 2.4.0 リリースで非推奨（廃止予定）となり、2.4.3 リリースで削除されました。 TinyMCE 4 は 2.4.4 リリースで削除されました。

![エディターツールバー](./assets/editor-toolbar.png){width="700" zoomable="yes"}

以下のトピックでは、エディターの使用について詳しく説明します。

- [リンクの挿入](editor-insert-link.md)
- [画像の挿入](editor-insert-image.md)
- [ウィジェットの挿入](editor-widget.md)
- [変数の挿入](editor-insert-variable.md)

## エディターの設定

WYSIWYG エディターはデフォルトで有効になっており、CMS ページやブロック、製品およびカテゴリのコンテンツを編集するために使用できます。 設定からエディターをアクティベートまたはアクティベート解除し、 [動的](../catalog/catalog-urls.md#dynamic-url)、製品およびカテゴリの説明内のメディアコンテンツの URL。

![WYSIWYG オプション](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

すべての WYSIWYG オプションについて詳しくは、を参照してください。 [コンテンツ管理](../configuration-reference/general/content-management.md) が含まれる _設定リファレンス_.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL Content Management]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. を設定 **[!UICONTROL Enable WYSIWYG Editor]** ご希望に合わせてください。

   このエディターは、デフォルトで有効になっています。

1. を設定 **[!UICONTROL Static URLs for Media Content in WYSIWYG]** すべてのあなたの好みに [メディアコンテンツ](../catalog/catalog-urls.md#static-url) これは WYSIWYG エディターで入力します。

1. 完了したら、 **[!UICONTROL Save Config]**.
