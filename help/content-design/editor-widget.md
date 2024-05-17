---
title: エディターでのウィジェットの挿入
description: WYSIWYG エディターのウィジェットツールを使用して、ページに様々なコンテンツ要素を追加します。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# エディターでのウィジェットの挿入

この [ウィジェット](widget-create.md) このツールを使用して、Commerceのコンテンツページやノード、商品、カテゴリへのリンクなど、様々なコンテンツ要素をページに追加できます。 リンクは、ブロック形式でページ上に配置することも、コンテンツに直接組み込むこともできます。 ウィジェットツールを使用して、次のタイプのコンテンツへのリンクを作成できます。

- [コンテンツページ](pages.md)
- [カタログカテゴリ](../catalog/categories.md)
- [カタログ製品](../catalog/product-create.md)

デフォルトでは、リンクはテーマのスタイルシートからスタイルを継承します。

{{$include /help/_includes/directives-caution.md}}

1. ページ、ブロック、またはダイナミックブロックを編集モードで開きます。

1. に移動します _[!UICONTROL Content]_「」セクションで、エディターをサポートする要素をクリックします。

1. ウィジェットを表示する位置にカーソルを置き、 _ウィジェットを挿入_ アイコン。

   ![エディターツールバー – ウィジェットを挿入](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   ページビルダーを有効にしていない場合にコードを操作するには、 **[!UICONTROL Show / Hide Editor]**. ウィジェットを表示するテキスト内の位置に挿入ポイントを置きます。 次に、 **[!UICONTROL Insert Widget]**.

1. を選択します。 **[!UICONTROL Widget Type]**.

   これらのオプションの詳細については、を参照してください [ウィジェットのタイプ](widgets.md#widget-types). 次の手順では、製品へのリンクを挿入する例を使用します。

1. 製品名を使用するには、 **[!UICONTROL Anchor Custom Text]** フィールドが空です。

1. を入力 **[!UICONTROL Anchor Custom Title]** （SEO のベストプラクティス用）

   このタイトルはページに表示されません。

1. を設定 **[!UICONTROL Template]** を次のいずれかに変更します。

   - リンクをテキストに組み込むには、 `Product Link Inline Template`.

   - 別の行にリンクを配置するには、次のオプションを選択します `Product Link Block Template`.

1. クリック **[!UICONTROL Select Product]** 次の手順を実行します。

   - ツリーで、目的のカテゴリに移動します。

   - リストで、リンクされた製品を選択します。

1. クリック **[!UICONTROL Insert Widget]** をクリックして、ページにリンクを配置します。

   HTMLコードを使用する場合、 [マークアップ タグ](../systems/markup-tags.md) リンクは、二重中括弧で囲まれたページの上部に表示されます。 必要に応じて、を使用します _切り取りと貼り付け_ をクリックして、コード内でリンクを表示する位置にマークアップ タグを配置します。

1. コンテンツの編集が完了したら、 **[!UICONTROL Save]**.
