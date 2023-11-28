---
title: エディターでのウィジェットの挿入
description: WYSIWYG エディターのウィジェットツールを使用して、様々なコンテンツ要素をページに追加します。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# エディターでのウィジェットの挿入

The [widget](widget-create.md) ツールを使用して、任意の Commerce コンテンツページ、ノード、製品、カテゴリへのリンクを含む、様々なコンテンツ要素をページに追加できます。 リンクをページ上にブロック形式で配置したり、コンテンツに直接組み込んだりできます。 ウィジェットツールを使用して、次のタイプのコンテンツへのリンクを作成できます。

- [コンテンツページ](pages.md)
- [カタログカテゴリ](../catalog/categories.md)
- [カタログ製品](../catalog/product-create.md)

デフォルトでは、リンクはテーマのスタイルシートからスタイルを継承します。

{{$include /help/_includes/directives-caution.md}}

1. 編集モードでページ、ブロック、ダイナミックブロックを開きます。

1. 次に移動： _[!UICONTROL Content]_」セクションを開き、エディターをサポートする要素をクリックします。

1. ウィジェットを表示する場所にカーソルを置き、 _ウィジェットの挿入_ アイコン。

   ![エディタツールバー — ウィジェットの挿入](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Page Builder が有効になっていないので、コードを操作する場合は、 **[!UICONTROL Show / Hide Editor]**. テキスト内で、ウィジェットを表示する位置に挿入ポイントを置きます。 次に、「 **[!UICONTROL Insert Widget]**.

1. を選択します。 **[!UICONTROL Widget Type]**.

   これらのオプションについて詳しくは、 [ウィジェットのタイプ](widgets.md#widget-types). 次の手順では、製品へのリンクを挿入する例を使用します。

1. 製品名を使用するには、 **[!UICONTROL Anchor Custom Text]** フィールドが空です。

1. を入力します。 **[!UICONTROL Anchor Custom Title]** SEO のベストプラクティスについて

   このタイトルは、ページには表示されません。

1. 設定 **[!UICONTROL Template]** を次のいずれかに変更します。

   - リンクをテキストに組み込むには、 `Product Link Inline Template`.

   - リンクを別の行に配置するには、 `Product Link Block Template`.

1. クリック **[!UICONTROL Select Product]** 次の操作を実行します。

   - ツリーで、目的のカテゴリに移動します。

   - リストで、リンクされた商品を選択します。

1. クリック **[!UICONTROL Insert Widget]** をクリックして、ページにリンクを配置します。

   HTMLコードを操作する場合、 [マークアップタグ](../systems/markup-tags.md) リンクはページの上部に二重中括弧で囲まれて表示されます。 必要に応じて、 _切り取って貼り付け_ をクリックして、リンクを表示するコード内にマークアップタグを配置します。

1. コンテンツの編集が完了したら、「 **[!UICONTROL Save]**.
