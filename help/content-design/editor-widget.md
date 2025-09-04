---
title: エディターでのウィジェットの挿入
description: WYSIWYG エディターのウィジェットツールを使用して、ページに様々なコンテンツ要素を追加します。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# エディターでのウィジェットの挿入

[widget](widget-create.md) ツールを使用すると、Commerce コンテンツページやノード、商品、カテゴリへのリンクなど、ページに様々なコンテンツ要素を追加できます。 リンクは、ブロック形式でページ上に配置することも、コンテンツに直接組み込むこともできます。 ウィジェットツールを使用して、次のタイプのコンテンツへのリンクを作成できます。

- [コンテンツページ](pages.md)
- [カタログカテゴリ](../catalog/categories.md)
- [カタログ製品](../catalog/product-create.md)

デフォルトでは、リンクはテーマのスタイルシートからスタイルを継承します。

{{$include /help/_includes/directives-caution.md}}

1. ページ、ブロック、またはダイナミックブロックを編集モードで開きます。

1. 「_[!UICONTROL Content]_」セクションに移動して、エディターをサポートする要素をクリックします。

1. ウィジェットを表示する位置にカーソルを置き、「_ウィジェットを挿入_」アイコンをクリックします。

   ![ エディターツールバー – ウィジェットを挿入 ](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   ページビルダーを有効にしていない場合にコードを操作するには、「**[!UICONTROL Show / Hide Editor]**」をクリックします。 ウィジェットを表示するテキスト内の位置に挿入ポイントを置きます。 次に、「**[!UICONTROL Insert Widget]**」をクリックします。

1. **[!UICONTROL Widget Type]** を選択します。

   これらのオプションについて詳しくは、[ ウィジェットの種類 ](widgets.md#widget-types) を参照してください。 次の手順では、製品へのリンクを挿入する例を使用します。

1. 製品名を使用するには、「**[!UICONTROL Anchor Custom Text]**」フィールドを空のままにします。

1. SEO ベストプラクティスの **[!UICONTROL Anchor Custom Title]** を入力します。

   このタイトルはページに表示されません。

1. **[!UICONTROL Template]** を次のいずれかに設定します。

   - リンクをテキストに組み込むには、「`Product Link Inline Template`」を選択します。

   - リンクを別の行に配置するには、[`Product Link Block Template`] を選択します。

1. 「**[!UICONTROL Select Product]**」をクリックして、次の操作を実行します。

   - ツリーで、目的のカテゴリに移動します。

   - リストで、リンクされた製品を選択します。

1. 「**[!UICONTROL Insert Widget]**」をクリックして、ページにリンクを配置します。

   HTML コードを操作している場合は、ページ上部にリンクの [ マークアップタグ ](../systems/markup-tags.md) が表示され、二重中括弧で囲まれます。 必要に応じて、_切り取りと貼り付け_ を使用して、コード内でリンクを表示する位置にマークアップタグを配置します。

1. コンテンツの編集が完了したら、「**[!UICONTROL Save]**」をクリックします。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
