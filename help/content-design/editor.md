---
title: WYSIWYG エディタ
description: _What You See Is What You Get_(WYSIWYG) ビューでエディターを使用し、コンテンツを操作する方法を説明します。
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG エディタ

エディターを使用すると、 _見えるものは得るものです_ (WYSIWYG) コンテンツの表示。 基になるHTMLコードを直接操作したい場合は、簡単にモードを変更できます。 エディターを使用して、のコンテンツを作成できます。 [ページ](pages.md), [ブロック](blocks.md)、および [製品の説明](../catalog/product-content.md). 製品の詳細を操作する場合は、「 **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>デフォルトの WYSIWYG エディタは TinyMCE 5 です。 Adobe CommerceとMagento Open Source2.4.5 の TinyMCE 5.10 ライブラリが更新され、一部の種類の URL を使用して画像やリンクを更新する際に、任意の JavaScript が実行される脆弱性が解決されました。 TinyMCE 3 は 2.4.0 リリースで廃止され、2.4.3 リリースで削除されました。 TinyMCE 4 は 2.4.4 リリースで削除されました。

![エディターツールバー](./assets/editor-toolbar.png){width="700" zoomable="yes"}

次のトピックでは、エディターの使用に関する詳細を説明します。

- [リンクの挿入](editor-insert-link.md)
- [画像の挿入](editor-insert-image.md)
- [ウィジェットの挿入](editor-widget.md)
- [変数の挿入](editor-insert-variable.md)

## エディターの設定

WYSIWYG エディターはデフォルトで有効になっており、CMS のページやブロック、および製品やカテゴリでのコンテンツの編集に使用できます。 設定から、エディターのアクティベートとアクティベート解除を切り替え、代わりに静的を使用するように選択できます。 [動的](../catalog/catalog-urls.md#dynamic-url)：製品およびカテゴリの説明のメディアコンテンツの URL。

![WYSIWYG オプション](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

すべての WYSIWYG オプションについて詳しくは、 [コンテンツ管理](../configuration-reference/general/content-management.md) （内） _設定リファレンス_.

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Content Management]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. 設定 **[!UICONTROL Enable WYSIWYG Editor]** を選択します。

   エディターはデフォルトで有効になっています。

1. 設定 **[!UICONTROL Static URLs for Media Content in WYSIWYG]** 全ての人の好みに応じて [メディアコンテンツ](../catalog/catalog-urls.md#static-url) WYSIWYG エディタで入力される

1. 完了したら、「 **[!UICONTROL Save Config]**.
