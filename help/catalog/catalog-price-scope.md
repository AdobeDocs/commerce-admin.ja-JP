---
title: 価格の範囲
description: グローバルレベルまたは Web サイトレベルで適用するように設定できる、製品価格に使用される範囲について説明します。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# 価格の範囲

の範囲 [基準通貨](../stores-purchase/currency-configuration.md) 製品価格に使用されるは、グローバルレベルまたは web サイトレベルで適用するように設定できます。 グローバルレベルに適用した場合は、ストア階層全体で同じ価格が使用されます。 Web サイトレベルに適用すると、異なる Web サイトに関連付けられた店舗とは異なる価格で、同じ製品を使用できます。 デフォルトでは、製品価格の範囲はグローバルです。

異なる要因が、ある場所での同じ製品の価格に影響を与え、別の場所では影響を与えない場合があります。 例えば、製品の追加の流通コストや、特定の店舗で販売される製品の価格に影響を与えるその他の考慮事項があります。 次の図は、基本通貨が Web サイトレベルに設定されたマルチサイトインストールを示しています。 各 Web サイトに関連付けられた店舗と店舗の表示は、Web サイトレベルで設定された製品価格を反映しています。

![Adobe Commerce用 B2B](../assets/b2b.svg) 共有カタログを使用している場合は、 [共有カタログの価格と構造を設定](../b2b/catalog-shared-pricing-structure.md) （内） _B2B for Adobe Commerceガイド_.

![価格範囲図](./assets/catalog-price-scope.svg){width="550"}

## 価格範囲の設定

1. 次の日： _管理者_ メニュー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 下にスクロールして、 **[!UICONTROL Price]** セクションとセット **[!UICONTROL Catalog Price Scope]** を次のいずれかに変更します。

   - `Global`
   - `Website`

   選択した範囲設定は、カタログの価格フィールドの下に表示されます。

   ![カタログ価格範囲](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 範囲を使用して製品価格を設定

コマースでは、各店舗の製品価格を設定できません。 ただし、Web サイトごとの価格は次のように変更できます。

1. 次の日： _管理者_ メニュー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. Adobe Analytics の **[!UICONTROL Price]** タブ、価格範囲を次に設定： `Website` グローバルではなく、グローバルです。

1. 商品の編集ページを開き、左上の範囲を選択し、Web サイトごとに新しい価格を入力して、価格を設定します。
