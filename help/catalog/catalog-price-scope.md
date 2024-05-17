---
title: 価格範囲
description: 製品価格に使用される範囲を説明します。この範囲は、グローバルレベルまたは web サイトレベルのいずれかで適用するように設定できます。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# 価格範囲

の範囲 [基準通貨](../stores-purchase/currency-configuration.md) 製品価格に使用する配分は、グローバルレベルまたは web サイトレベルで適用するように設定できます。 グローバルレベルに適用する場合、ストア階層全体で同じ価格が使用されます。 Web サイトレベルに適用すると、同じ製品を異なる Web サイトに関連付けられた店舗から異なる価格で利用できます。 デフォルトでは、製品価格の範囲はグローバルです。

異なる要因は、ある場所ではなく別の場所で同じ製品の価格に影響を与える可能性があります。 例えば、商品の追加の流通コストや、特定の店舗で販売される商品の価格に影響を与えるその他の考慮事項が発生する可能性があります。 次の図は、基本通貨が web サイトレベルに設定されたマルチサイトのインストールを示しています。 各 web サイトに関連付けられたストアとストアの表示は、web サイトレベルで設定された製品価格を反映します。

![Adobe Commerceの B2B](../assets/b2b.svg) 共有カタログを使用する場合は、も参照してください [共有カタログの価格と構造の設定](../b2b/catalog-shared-pricing-structure.md) が含まれる _Adobe Commerceの B2B ガイド_.

![価格範囲図](./assets/catalog-price-scope.svg){width="550"}

## 価格範囲の設定

1. 日 _Admin_ メニュー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. にスクロール ダウンします。 **[!UICONTROL Price]** セクションとセット **[!UICONTROL Catalog Price Scope]** を次のいずれかに変更します。

   - `Global`
   - `Website`

   選択した範囲設定が、カタログの価格フィールドの下に表示されます。

   ![カタログの価格スコープ](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## スコープを使用して製品価格を設定します

Commerceでは、各店舗の商品価格を設定することはできません。 ただし、web サイトごとに価格を変更できます。

1. 日 _Admin_ メニュー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. が含まれる **[!UICONTROL Price]** タブ、価格範囲を次に設定 `Website` グローバルの代わりに使用します。

1. 製品の編集ページを開き、左上の範囲を選択して、web サイトごとに新しい価格を入力して価格を設定します。
