---
title: 価格範囲
description: グローバルレベルまたはweb サイトレベルで適用するように設定できる製品価格に使用される範囲について説明します。
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# 価格範囲

製品価格に使用される[基本通貨](../stores-purchase/currency-configuration.md)の範囲は、グローバル レベルまたはweb サイト レベルで適用するように設定できます。 グローバルレベルに適用した場合、ストア階層全体で同じ価格が使用されます。 同じ商品をweb サイトレベルに適用すると、同じ商品を異なるweb サイトに関連付けられているストアから異なる価格で利用できます。 デフォルトでは、製品の価格設定の範囲はグローバルです。

異なる要因は、ある場所の同じ製品の価格に影響を与える可能性があり、別の場所には影響しません。 たとえば、商品の流通コストが追加されたり、特定の店舗で販売される商品の価格に影響を与えるその他の考慮事項が生じたりする可能性があります。 次の図は、基本通貨がweb サイトレベルに設定されたマルチサイトインストールを示しています。 各web サイトに関連付けられたストアビューとストアビューには、web サイトレベルで設定された製品価格が反映されます。

![Adobe Commerce B2B](../assets/b2b.svg)共有カタログを使用している場合は、_Adobe Commerce B2B ガイド_&#x200B;の[共有カタログの価格と構造の設定](../b2b/catalog-shared-pricing-structure.md)も参照してください。

![価格範囲図](./assets/catalog-price-scope.svg){width="550"}

## 価格範囲の設定

1. _管理者_ メニューで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Price]** セクションまでスクロールし、**[!UICONTROL Catalog Price Scope]**&#x200B;を次のいずれかに設定します。

   - `Global`
   - `Website`

   選択したスコープ設定は、カタログの価格フィールドの下に表示されます。

   ![&#x200B; カタログ価格範囲](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 範囲を使用した製品価格の設定

Commerceでは、各店舗の商品価格を設定することはできません。 しかし、あなたはウェブサイトあたりの価格を変更することができます：

1. _管理者_ メニューで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. 「**[!UICONTROL Price]**」タブで、価格の範囲を`Global`ではなく`Website`に設定します。

1. 商品編集ページを開き、左上の範囲を選択して、web サイトごとに新しい価格を入力することで、価格を設定します。

価格範囲が`Global`に設定されている場合、Commerce データベースでは、web サイト レベルで異なる価格を引き続き使用できます。 これは、Commerce以外の同期の問題の結果として発生する可能性があります。 この場合、加盟店はストアレベルで価格のクリーンアップを行い、Commerce サービスでカタログシンクを実行する必要があります。