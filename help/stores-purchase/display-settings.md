---
title: 価格表示の設定
description: 顧客購入体験をサポートするカタログ、ショッピングカート、注文、請求書、クレジットメモでの税金の表示について説明します。
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# 価格表示の設定

価格表示設定では、商品と送料に税金が含まれているか含まれていないかを判断するか、価格の2つのバージョンを表示します。1つは税抜きで、もう1つは税抜きで表示されます。

製品価格に税金が含まれている場合、税金は、税出所と一致する税金規則がある場合、または顧客住所が税金規則と一致する場合にのみ表示されます。 顧客がアカウントを作成したり、ログインしたり、ショッピングカートから消費税と送料の見積もりを生成したりする際に、マッチをトリガーできるイベントがあります。

>[!IMPORTANT]
>
>税金を含める価格と除外する価格を表示すると、お客様の混乱を招く可能性があります。 警告メッセージのトリガーを回避するには、お住まいの国の[&#x200B; ガイドライン &#x200B;](international-tax-guidelines.md)および警告メッセージを回避するための[推奨設定](taxes.md#warning-messages)を参照してください。

![価格表示設定](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

これらの各設定設定の詳細については、_設定リファレンスガイド_&#x200B;の[価格表示設定](../configuration-reference/sales/tax.md#price-display-settings)を参照してください。

## 価格表示設定の設定

税金、レートおよびクラスの計算の設定が完了すると、これらの設定に従って税金が計算されます。 ただし、カタログ、ショッピングカート、注文、請求書、クレジットメモへの税金の表示も、ストアフロントでの顧客体験をサポートするように設定する必要があります。

お客様が注文する前に、これらの計算がどのように適用されるかを知ることができるように、関連する税金（税金を含むか、または税金を含む両方）を含む価格を表示することをお勧めします。

### 手順1：カタログ価格の表示設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Tax]**&#x200B;を選択します。

1. **[!UICONTROL Price Display Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Display Product Prices in Catalog]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >このオプションを`Including Tax`に設定すると、税源に一致する税ルールがある場合、または税ルールに一致する顧客住所がある場合にのみ税が表示されます。 マッチをトリガーできるイベントには、お客様アカウントの作成、ログイン、ショッピングカートでの税金と送料の見積もりツールの使用などがあります。

1. **[!UICONTROL Display Shipping Prices]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

両方の価格（税込みおよび税抜き）を表示する場合、ストアフロントは次のようになります。

![&#x200B; ストアフロントでの税金を含む価格表示の例](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### 手順2：ショッピングカートの表示設定の設定

1. **[!UICONTROL Shopping Cart Display Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![買い物かごの表示設定](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display Prices]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Display Subtotal]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Display Shipping Amount]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]**&#x200B;の場合は、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]**&#x200B;の場合は、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 残りの各オプションについて、好みに応じて`Yes`または`No`に切り替えます。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### 手順3：注文、請求書、クレジットメモの表示設定

1. **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![注文、請求書、クレジットメモの表示設定](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display Prices]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Display Subtotal]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Display Shipping Amount]**&#x200B;に対して、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]**&#x200B;の場合は、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]**&#x200B;の場合は、次のいずれかを選択します。

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 残りの各オプションについて、好みに応じて`Yes`または`No`に切り替えます。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
