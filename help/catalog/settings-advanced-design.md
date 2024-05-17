---
title: 製品設定 –  [!UICONTROL Design]
description: 製品の場合、 [!UICONTROL Design] 設定を使用すると、製品ページに別のテーマを適用し、レイアウトを変更できます。
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 製品設定 –  [!UICONTROL Design]

この _[!UICONTROL Design]_設定を使用すると、製品ページに別のテーマを適用したり、列のレイアウトを変更したり、製品オプションの表示場所を決定したり、カスタム XML コードを入力したりできます。

![デザイン](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>同じ製品が、カテゴリごとに異なるデザイン設定を持つ複数のカテゴリに割り当てられている場合は、を設定することをお勧めします **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` が含まれる [検索エンジン最適化設定オプション](../configuration-reference/catalog/catalog.md#search-engine-optimization). この設定にアクセスするには、に移動します  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**、を展開&#x200B;**[!UICONTROL Catalog]**を選択します&#x200B;**[!UICONTROL Catalog]**左側のパネルの下にあるを展開します&#x200B;**[!UICONTROL Search Engine Optimization]**ページの「」セクション。

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|----|
| [!UICONTROL Theme] | ストア表示 | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）別のテーマを商品に適用できます。 オプション：（使用可能なすべてのテーマ） |
| [!UICONTROL Layout] | ストア表示 | 別のを適用できます [layout](../content-design/page-layout.md) 製品ページに移動します。 オプション： <br/>**[!UICONTROL No layout updates]**- デフォルトでは、製品ページのレイアウトのアップデートは利用できません。<br/>**[!UICONTROL Empty]** - 4 列のページなど、独自のレイアウトを定義できます。 （XML を理解している必要があります）。 <br/>**[!UICONTROL 1 column]**– 製品ページに 1 列のレイアウトを適用します。<br/>**[!UICONTROL 2 columns with left bar]**  – 左サイドバーを含む 2 列のレイアウトを製品ページに適用します。 <br/>**[!UICONTROL 2 columns with right bar]**– 右サイドバーを含む 2 列のレイアウトを製品ページに適用します。<br/>**[!UICONTROL 3 columns]** - 3 列のレイアウトを製品ページに適用します。 <br/>**[!UICONTROL Page -- Full Width]**- （必須 [[!DNL Page Builder]](../page-builder/introduction.md)） CMS ページの全幅レイアウトを製品ページに適用します。<br/>**[!UICONTROL Category -- Full Width]** - （必須 [!DNL Page Builder]）カテゴリページの全幅レイアウトを製品ページに適用します。 <br/>**[!UICONTROL Product -- Full Width]**- （必須 [!UICONTROL Page Builder]）製品ページの全幅レイアウトを製品ページに適用します。 |
| [!UICONTROL Display Product Options In] | ストア表示 | 製品ページ上の製品オプションの表示場所を指定します。 オプション： `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | ストア表示 | 製品ページ上のカスタムレイアウトを更新するためのオプションにアクセスするために使用します。 |

{style="table-layout:auto"}
