---
title: エディターでのウィジェットの挿入
description: WYSIWYGエディターのウィジェットツールを使用して、ページに様々なコンテンツ要素を追加します。
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/NdvL4SUXxRGF451r8SpP6JJ5iBa0gJoU4QIqTMefvc8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 356
ht-degree: 0%

---

# エディターでのウィジェットの挿入

[widget](widget-create.md) ツールを使用すると、任意のCommerce コンテンツページまたはノード、製品、またはカテゴリへのリンクを含む、様々なコンテンツ要素をページに追加できます。 リンクは、ブロック形式でページに配置するか、コンテンツに直接組み込むことができます。 ウィジェットツールを使用して、次の種類のコンテンツへのリンクを作成できます。

- [コンテンツページ](pages.md)
- [カタログのカテゴリ](../catalog/categories.md)
- [カタログ製品](../catalog/product-create.md)

デフォルトでは、リンクはテーマのスタイルシートからスタイルを継承します。

{{$include /help/_includes/directives-caution.md}}

1. 編集モードでページ、ブロック、またはダイナミックブロックを開きます。

1. _[!UICONTROL Content]_セクションに移動し、エディターをサポートする任意の要素をクリックします。

1. ウィジェットを表示する場所にカーソルを置き、_ウィジェットを挿入_ アイコンをクリックします。

   ![ エディターツールバー – ウィジェットの挿入](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   ページビルダーを有効にしておらず、コードを操作したい場合は、**[!UICONTROL Show / Hide Editor]**&#x200B;をクリックします。 ウィジェットを表示するテキスト内に挿入ポイントを置きます。 次に、**[!UICONTROL Insert Widget]**&#x200B;をクリックします。

1. **[!UICONTROL Widget Type]**&#x200B;を選択します。

   これらのオプションについて詳しくは、[ ウィジェットの種類](widgets.md#widget-types)を参照してください。 次の手順では、製品へのリンクを挿入する例を使用します。

1. 製品名を使用するには、**[!UICONTROL Anchor Custom Text]** フィールドを空のままにします。

1. SEOのベストプラクティスとして&#x200B;**[!UICONTROL Anchor Custom Title]**&#x200B;を入力してください。

   このタイトルはページに表示されません。

1. **[!UICONTROL Template]**&#x200B;を次のいずれかに設定します：

   - リンクをテキストに組み込むには、`Product Link Inline Template`を選択します。

   - リンクを別の行に配置するには、`Product Link Block Template`を選択します。

1. **[!UICONTROL Select Product]**&#x200B;をクリックし、次の操作を行います。

   - ツリーで、必要なカテゴリに移動します。

   - リストで、リンクされた製品を選択します。

1. **[!UICONTROL Insert Widget]**&#x200B;をクリックして、ページにリンクを配置します。

   HTML コードを使用している場合、リンクの[ マークアップタグ ](../systems/markup-tags.md)がページの上部に表示され、二重中括弧で囲まれます。 必要に応じて、_カット&amp;ペースト_&#x200B;を使用して、リンクを表示するコード内にマークアップタグを配置します。

1. コンテンツの編集が完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
