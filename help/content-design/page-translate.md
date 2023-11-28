---
title: コンテンツページの翻訳
description: 特定のストア表示から利用できる各ページの翻訳バージョンを作成する方法を説明します。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# コンテンツページの翻訳

ストアに異なる [言語](../stores-purchase/store-localize.md)を検索し、各ビューのロケールを異なる言語に設定した場合、結果は部分翻訳されたサイトになります。 次の手順では、特定のストア表示から利用できる各ページの翻訳バージョンを作成します。 The [!UICONTROL Store View] 列 _[!UICONTROL Manage Pages]_リストには、翻訳されたバージョンのページを持つ各ビューが表示されます。

コンテンツページを翻訳するには、元のページと同じ URL キーを持ち、特定のストアビューに割り当てられた別のページを作成する必要があります。 次に、翻訳されたテキストで特定のビューのページを更新します。 次の例は、 _会社概要_ スペイン語のストア表示用のページ。

## 手順 1：翻訳するページの URL キーをコピーする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドで、翻訳するページを見つけ、で開きます。 _編集_ モード。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** セクションを開き、 **[!UICONTROL URL Key]** をクリップボードに追加します。

1. に戻るには、以下を実行します。 _[!UICONTROL Pages]_グリッド、クリック&#x200B;**[!UICONTROL Back]**をクリックします。

## 手順 2：翻訳されたコンテンツのページを追加する

1. クリック **[!UICONTROL Add New Page]**.

1. 翻訳済みを入力 **[!UICONTROL Page Title]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに移動し、ページの翻訳済みテキストを入力します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションで次の操作を実行します。

   - を貼り付けます。 **[!UICONTROL URL Key]** 元のページからコピーした

   - の翻訳済みテキストを入力 **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**、および **[!UICONTROL Meta Description]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Page in Websites]** セクションとセット **[!UICONTROL Store View]** を追加します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Design]** セクションに移動して、列を設定します。 **[!UICONTROL Layout]** 」と入力します。

1. クリック **[!UICONTROL Save]**.

1. プロンプトが表示されたら、無効なものを更新します。 [キャッシュ](../systems/cache-management.md).

## 手順 3：翻訳の検証

翻訳を検証するには、ストアフロントに移動し、言語選択を使用してストア表示を変更します。

会社のフッターリンクを含む、翻訳する必要のあるページ上に一部の要素が残っていることに注意してください。 [ブロック](block-add.md)、 [ようこそメッセージ](../getting-started/storefront-branding.md#change-the-welcome-message)、および [製品情報](../stores-purchase/store-localize.md#localize-products).
