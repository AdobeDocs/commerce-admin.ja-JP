---
title: 価格の表示設定
description: 顧客の購入エクスペリエンスをサポートするカタログ、買い物かご、注文、請求書、クレジットメモでの税金の表示について説明します。
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# 価格の表示設定

価格の表示設定では、製品と配送価格に税が含まれているか除外されているか、または価格の 2 つのバージョン（1 つは税が含まれているか、もう 1 つは税が含まれていないかを決定します。

製品価格に税金が含まれる場合、税金が表示されるのは、税源に一致する税務処理基準があるか、顧客所在地が税務処理基準に一致する場合のみです。 一致をトリガーにできるイベントには、お客様がアカウントを作成したり、ログインしたり、買い物かごから税金と送料の見積もりを生成したりする場合が含まれます。

>[!IMPORTANT]
>
>税金を含む/除外する価格を示すと、お客様にとって混乱を招く可能性があります。 警告メッセージのトリガーを回避するには、 [ガイドライン](international-tax-guidelines.md) お住まいの国や [推奨設定](taxes.md#warning-messages) 警告メッセージを回避する。

![価格の表示設定](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

これらの各設定について詳しくは、を参照してください。 [価格の表示設定](../configuration-reference/sales/tax.md#price-display-settings) が含まれる _設定リファレンスガイド_.

## 価格表示設定の指定

税金、レートおよび区分の計算の構成が終了すると、これらの設定に従って税金が計算されます。 ただし、カタログ、買い物かご、注文、請求書、クレジットメモに含まれる税金の表示は、ストアフロントでの顧客体験をサポートするように設定する必要もあります。

ベストプラクティスは、価格に関連する税金（税を含むもの、または税を含む場合と税を除く場合の両方）を表示して、顧客が注文を行う前にこれらの計算がどのように適用されるかを把握できるようにすることです。

### 手順 1：カタログ価格の表示設定の構成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Price Display Settings]** セクション。

1. の場合 **[!UICONTROL Display Product Prices in Catalog]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >このオプションを `Including Tax`、税金が表示されるのは、税源に一致する税務処理基準がある場合、または税務処理基準に一致する顧客所在地がある場合のみです。 照合をトリガーにできるイベントには、顧客アカウントの作成、ログイン、またはショッピング・カート内の税金および出荷見積ツールの使用が含まれます。

1. の場合 **[!UICONTROL Display Shipping Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

両方の価格（税込および非税込）を表示することを選択した場合、ストアフロントは次のようになります。

![ストアフロントでの税を含む価格表示の例](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### 手順 2：買い物かごの表示設定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Shopping Cart Display Settings]** セクション。

   ![買い物かごの表示設定](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Display Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. の場合 **[!UICONTROL Display Subtotal]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. の場合 **[!UICONTROL Display Shipping Amount]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 残りのオプションごとに、を切り替えます。 `Yes` または `No` 好みに応じて：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### 手順 3：受注、請求書およびクレジット・メモの表示設定の構成

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** セクション。

   ![受注、請求書、クレジット・メモの表示設定](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Display Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. の場合 **[!UICONTROL Display Subtotal]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. の場合 **[!UICONTROL Display Shipping Amount]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]**&#x200B;次のいずれかの操作を行います。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 残りのオプションごとに、を切り替えます。 `Yes` または `No` 好みに応じて：

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、 **[!UICONTROL Save Config]**.
