---
title: 価格範囲
description: 製品価格に使用される範囲を説明します。この範囲は、グローバルレベルまたは web サイトレベルのいずれかで適用するように設定できます。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: bc3977f29c8048a1b8578aa21fa55fa1a4d903f2
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 価格範囲

製品価格に使用される [ ベース通貨 ](../stores-purchase/currency-configuration.md) の範囲は、グローバルレベルまたは web サイトレベルのいずれかで適用するように設定できます。 グローバルレベルに適用する場合、ストア階層全体で同じ価格が使用されます。 Web サイトレベルに適用すると、同じ製品を異なる Web サイトに関連付けられた店舗から異なる価格で利用できます。 デフォルトでは、製品価格の範囲はグローバルです。

異なる要因は、ある場所ではなく別の場所で同じ製品の価格に影響を与える可能性があります。 例えば、商品の追加の流通コストや、特定の店舗で販売される商品の価格に影響を与えるその他の考慮事項が発生する可能性があります。 次の図は、基本通貨が web サイトレベルに設定されたマルチサイトのインストールを示しています。 各 web サイトに関連付けられたストアとストアの表示は、web サイトレベルで設定された製品価格を反映します。

![Adobe Commerce B2B](../assets/b2b.svg) 共有カタログを使用している場合は、[Adobe Commerce B2B ガイド ](../b2b/catalog-shared-pricing-structure.md) の _共有カタログの価格と構造の設定_ も参照してください。

![ 価格範囲図 ](./assets/catalog-price-scope.svg){width="550"}

## 価格範囲の設定

1. _管理者_ メニューで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「**[!UICONTROL Price]**」セクションまでスクロールし、**[!UICONTROL Catalog Price Scope]** を次のいずれかに設定します。

   - `Global`
   - `Website`

   選択した範囲設定が、カタログの価格フィールドの下に表示されます。

   ![ カタログの価格範囲 ](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## スコープを使用して製品価格を設定します

Commerceでは、各店舗の商品価格を設定することはできません。 ただし、web サイトごとに価格を変更できます。

1. _管理者_ メニューで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「**[!UICONTROL Price]**」タブで、価格範囲を `Website` ではなく `Global` に設定します。

1. 製品の編集ページを開き、左上の範囲を選択して、web サイトごとに新しい価格を入力して価格を設定します。

まれに、価格範囲が `Global` に設定されている場合、Commerce データベースの web サイトレベルで異なる価格が引き続き設定される可能性があります。 これは、Commerce外部での同期の問題が原因で発生する可能性があります。 この場合、マーチャントはストアレベルで価格のクリーンアップを実行し、Commerce サービスとのカタログ同期を実行する必要があります。