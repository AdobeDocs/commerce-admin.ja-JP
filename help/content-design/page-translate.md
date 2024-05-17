---
title: コンテンツページの翻訳
description: 特定のストア表示から使用可能な各ページの翻訳済みバージョンを作成する方法を説明します。
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# コンテンツページの翻訳

ストアが異なる複数のビューを持っている場合 [languages](../stores-purchase/store-localize.md)各ビューのロケールを異なる言語に設定した場合、部分的に翻訳されたサイトが得られます。 次に、特定のストア表示から使用可能な各ページの翻訳済みバージョンを作成します。 この [!UICONTROL Store View] の列 _[!UICONTROL Manage Pages]_リストには、ページの翻訳済みバージョンを持つ各ビューが表示されます。

コンテンツページを翻訳するには、元のページと同じ URL キーを持ち、特定のストア表示に割り当てられている別のページを作成する必要があります。 次に、翻訳されたテキストで特定のビューのページを更新します。 次の例は、の翻訳済みバージョンを作成する方法を示しています _会社情報_ スペイン語ストア表示のページ。

## 手順 1：翻訳するページの URL キーをコピーする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. グリッドで、翻訳して開くページを見つけます。 _編集_ モード。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** 「」セクションを選択し、 **[!UICONTROL URL Key]** をクリップボードに追加します。

1. に戻る _[!UICONTROL Pages]_グリッド、クリック&#x200B;**[!UICONTROL Back]**上部のボタンバーに移動します。

## 手順 2：翻訳済みコンテンツのページを追加

1. クリック **[!UICONTROL Add New Page]**.

1. 翻訳済みのを入力 **[!UICONTROL Page Title]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** 「」セクションに移動して、ページ用に翻訳されたテキストを入力します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization]** を選択し、次の操作を実行します。

   - を貼り付けます **[!UICONTROL URL Key]** 元のページからコピーしたもの。

   - の翻訳済みテキストを入力 **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**、および **[!UICONTROL Meta Description]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Page in Websites]** セクションとセット **[!UICONTROL Store View]** をクリックします。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Design]** を選択して列を設定 **[!UICONTROL Layout]** を表示します。

1. クリック **[!UICONTROL Save]**.

1. プロンプトが表示されたら、無効なを更新します [キャッシュ](../systems/cache-management.md).

## 手順 3：翻訳を検証

翻訳を確認するには、ストアフロントに移動し、言語選択を使用してストア表示を変更します。

会社のフッターリンクなど、翻訳が必要な要素がページ上にまだ残っていることに注意してください [ブロック](block-add.md), [ようこそメッセージ](../getting-started/storefront-branding.md#change-the-welcome-message)、および [商品情報](../stores-purchase/store-localize.md#localize-products).
