---
title: 製品設定 — [!UICONTROL Design]
description: 製品の場合、 [!UICONTROL Design] 設定を使用すると、製品ページに別のテーマを適用し、レイアウトを変更できます。
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 製品設定 — [!UICONTROL Design]

The _[!UICONTROL Design]_設定を使用すると、製品ページに別のテーマを適用したり、列のレイアウトを変更したり、製品オプションを表示する場所を決定したり、カスタム XML コードを入力したりできます。

![デザイン](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>同じ製品が複数のカテゴリに割り当てられ、各カテゴリに異なるデザイン設定が設定されている場合は、 **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` （内） [検索エンジン最適化設定オプション](../configuration-reference/catalog/catalog.md#search-engine-optimization). この設定にアクセスするには、に移動します。  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**、展開&#x200B;**[!UICONTROL Catalog]**を選択します。**[!UICONTROL Catalog]**左側のパネルの下で、を展開します。**[!UICONTROL Search Engine Optimization]**」セクションに表示されます。

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---|---|----|
| [!UICONTROL Theme] | ストア表示 | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 製品に別のテーマを適用できます。 オプション： （使用可能なすべてのテーマ） |
| [!UICONTROL Layout] | ストア表示 | 異なる [レイアウト](../content-design/page-layout.md) を製品ページに追加します。 オプション： <br/>**[!UICONTROL No layout updates]**— デフォルトでは、製品ページのレイアウトの更新は使用できません。<br/>**[!UICONTROL Empty]** - 4 列のページなど、独自のレイアウトを定義できます。 （XML に関する理解が必要です）。 <br/>**[!UICONTROL 1 column]**- 1 列のレイアウトを製品ページに適用します。<br/>**[!UICONTROL 2 columns with left bar]**  — 製品ページに左にサイドバーがある 2 列のレイアウトを適用します。 <br/>**[!UICONTROL 2 columns with right bar]**— 製品ページに右側のサイドバーを持つ 2 列のレイアウトを適用します。<br/>**[!UICONTROL 3 columns]** - 3 列のレイアウトを製品ページに適用します。 <br/>**[!UICONTROL Page -- Full Width]**- （必須） [[!DNL Page Builder]](../page-builder/introduction.md)) 製品ページに CMS ページの全幅レイアウトを適用します。<br/>**[!UICONTROL Category -- Full Width]** - （必須） [!DNL Page Builder]製品ページにカテゴリページの全幅レイアウトを適用します。 <br/>**[!UICONTROL Product -- Full Width]**- （必須） [!UICONTROL Page Builder]) 製品ページに全幅レイアウトを適用します。 |
| [!UICONTROL Display Product Options In] | ストア表示 | 製品オプションが製品ページのどこに表示されるかを決定します。 オプション： `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | ストア表示 | 製品ページのカスタムレイアウトを更新するためのオプションにアクセスするために使用します。 |

{style="table-layout:auto"}
