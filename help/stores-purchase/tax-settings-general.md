---
title: 税金構成設定
description: 税金区分、計算、デフォルトの税金宛先を含む基本的な税金設定を構成する方法を説明します。
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# 税金構成設定

以下の手順では、コマースインスタンスの基本的な税金設定について説明します。 税金を設定する前に、自分の税金要件に精通していることを確認してください [ロケール](store-localize.md#step-3-change-the-locale-of-the-store-view). 次に、必要に応じて税金設定を完了します。

管理者 [権限](../systems/permissions.md) 制限する [アクセス](../systems/permissions-user-roles.md) 事業に基づいて資源に課税する _知る必要がある_. 税金設定へのアクセス権を持つ管理者ロールを作成するには、「売上/税金」リソースと「システム/税金」リソースの両方を選択します。 デフォルトの発送元と異なる地域用に Web サイトを設定する場合は、その役割のシステム/発送先リソースへのアクセスも許可する必要があります。 配送先設定は、カタログ価格に使用される店舗税率を決定します。

## 一般税の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. マルチサイト設定の場合は、 **[!UICONTROL Store View]** を web サイトに追加し、設定のターゲットとなるを保存します。

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. 次の設定を実行します。

   必要に応じて、 **[!UICONTROL Use system value]** チェックボックスをオンにします。

### [!UICONTROL Tax Classes]

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Tax Classes]** 」セクションに入力します。

   ![税区分](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **輸送用税区分**  — 適切なクラスに設定します。 デフォルトのクラスは次のとおりです。 `None` および `Taxable Goods`
   - **贈与オプションの税区分** — ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 適切なクラスに設定します。 デフォルトのクラスは次のとおりです。 `None` および `Taxable Goods`
   - **製品のデフォルト税区分**  — 適切なクラスに設定します。 デフォルトのクラスは次のとおりです。 `None` および `Taxable Goods`
   - **顧客のデフォルト税区分**  — 適切なクラスに設定します。 デフォルトのクラスは次のとおりです。 `Retail Customer` および `Wholesale Customer`

1. 完了したら、「 **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. を展開します。 **[!UICONTROL Calculation Settings]** 」セクションに入力します。

   ![計算設定](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Tax Calculation Method Based On]** を次のいずれかに変更します。

   - `Unit Price`  — 各製品の価格
   - `Row Total`  — 注文の行項目の合計、割引の少ない
   - `Total`  — 注文の合計

1. 設定 **[!UICONTROL Tax Calculation Based On]** を次のいずれかに変更します。

   - `Shipping Address`  — 発送先の住所
   - `Billing Address`  — 顧客または会社の請求先住所
   - `Shipping Origin` - [原点](shipping-settings.md#point-of-origin) お客様のストアに

1. 設定 **[!UICONTROL Catalog Prices]** から `Excluding Tax` または `Including Tax`.

1. 設定 **[!UICONTROL Shipping Prices]** から `Excluding Tax` または `Including Tax`.

1. 設定 **[!UICONTROL Apply Customer Tax]** 次のいずれかに変更して、税金が当初価格と割引価格のどちらに適用されるかを判断します。 `After Discount` または `Before Discount`

1. 設定 **[!UICONTROL Apply Discount on Prices]** を次のいずれかに変更して、割引に税が含まれるか除外するかを決定します。 `Excluding Tax` または `Including Tax`

1. 設定 **[!UICONTROL Apply Tax On]** から `Custom price if available` または `Original price only`.

1. 設定 **[!UICONTROL Enable Cross-Border Trade]** を次のいずれかに変更します。

   - `Yes`  — 様々な税率で一貫した価格を使用。 カタログ価格に税が含まれる場合は、この設定を選択して、顧客の税率に関係なく価格を修正します。
   - `No` ・税率で価格を変更。

   >[!IMPORTANT]
   >
   >次の場合 [国境を越えた貿易](#cross-border-price-consistency) が有効な場合、利益幅は税率で変更されます。 利益は、数式 (`Revenue - CustomerVAT - CostOfGoodsSold`) をクリックします。 国境を越えた貿易を可能にするには、価格に税を含める必要があります。

### [!UICONTROL Default Tax Destination Calculation]

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default Tax Destination Calculation]** 」セクションに入力します。

   ![デフォルトの税金宛先の計算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 次を指定します。 **[!UICONTROL Default Country]** 税額計算用。

1. 該当する場合は、 **[!UICONTROL Default State]** 税額計算用。

1. 該当する場合は、 **[!UICONTROL Default Post Code]** 税額計算用。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>価格表示に関連する設定の組み合わせの中には、税込みと除外の両方が顧客にとって混乱を招く可能性があるものもあります。 警告メッセージがトリガーされないようにするには、 [推奨設定](taxes.md#warning-messages).

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Price Display Settings]** 」セクションに入力します。

   ![価格の表示設定](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display Product Prices in Catalog]** を次のいずれかに変更します。

   - `Excluding Tax` ・店頭に並ぶカタログ価格には税込みではない。
   - `Including Tax`  — ストアフロントのカタログ価格は、税務処理基準が税務処理基準と一致する場合、または顧客の住所が税務処理基準と一致する場合にのみ、税金が含まれます。 これは、顧客がアカウントを作成した後、ログインした後、または買い物かごで見積もり税と配送ツールを使用した後に発生する場合があります。
   - `Including and Excluding Tax` ・店頭に並ぶカタログ価格は税抜きでも同様に表示される。

1. 設定 **[!UICONTROL Display Shipping Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Shopping Cart Display Settings]** 」セクションに入力します。

   ![買い物かごの表示設定](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 次の各設定で、ストアとロケールの要件に応じて、買い物かごに表示する税金と価格の表示方法を選択します。

   - 設定 **[!UICONTROL Display Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - 設定 **[!UICONTROL Display Subtotal]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - 設定 **[!UICONTROL Display Shipping Amount]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 設定 **[!UICONTROL Display Gift Wrapping Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 設定 **[!UICONTROL Display Printed Card Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

1. 次の表示オプションを次のいずれかに設定します。 `Yes` または `No`必要に応じて、次の手順に従います。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、「 **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. 展開 ![拡張](../assets/icon-display-expand.png) の **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** 」セクションに入力します。

   ![オーダー、請求書、クレジット・メモの表示設定](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 受注、請求書およびクレジット・メモでの価格と税金の表示方法を指定します。

   - 設定 **[!UICONTROL Display Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - 設定 **[!UICONTROL Display Subtotal]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - 設定 **[!UICONTROL Display Shipping Amount]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 設定 **[!UICONTROL Display Gift Wrapping Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 設定 **[!UICONTROL Display Printed Card Prices]** から `Excluding Tax`, `Including Tax`または `Including and Excluding Tax`.

1. 次の表示オプションをに設定します。 `Yes` または `No`、必要に応じて以下をおこないます。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、「 **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Fixed Product Taxes]** 」セクションに入力します。

   ![固定製品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable FPT]** 次のいずれかを実行します。 `Yes` または `No`、必要に応じて。

1. FPT が有効な場合は、FPT 表示オプションを指定します。

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only`  — 表示される価格は、固定製品税を含む。 FPT 金額は別に表示されません。
   - `Including FPT and FPT description`  — 表示される価格は、固定製品税を含む。 FPT 金額は、別々に表示されます。
   - `Excluding FPT. Including FPT description and final price`  — 表示される価格には、固定製品税は含まれません。 FPT 金額は、別々に表示されます。
   - `Excluding FPT`  — 表示される価格には、固定製品税は含まれません。 FPT 金額は別に表示されません。

1. 設定 **[!UICONTROL Apply Discounts to FPT]** から `Yes` または `No`、必要に応じて。

1. 設定 **[!UICONTROL FPT Tax Configuration]** を使用して、FPT の計算方法を決定します。

   - `Not Taxed`  — 課税管轄区域が FPT に課税されない場合は、このオプションを選択します。 （例：カリフォルニア）。
   - `Taxed`  — 課税管轄区域が税金 FPT の場合は、このオプションを選択します。 （例：カナダ）。
   - `Loaded and Displayed with Tax`  — 税金を適用する前に FPT が注文合計に追加される場合は、このオプションをクリックします。 （例：EU 諸国）。

1. 設定 **[!UICONTROL Include FPT in Subtotal]** から `Yes` または `No`、必要に応じて。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 国境を越えた価格の一貫性

国境を越えた貿易（価格一貫性とも呼ばれる）は、EU（欧州連合）や、店舗税率とは異なる税率を持つ顧客に対して一貫した価格を維持したい他の商人をサポートしています。

地域や地域をまたいで運営する商人は、製品の価格に税を含めることで、1 つの価格を表示できます。 国によって異なる税制や税率に関係なく、価格は明確で明確です。 これらの設定では、税計算の拡張機能が [Marketplace](../getting-started/commerce-marketplace.md)、例： _頂点雲_.

>[!NOTE]
>
>国境を越えた取引が有効な場合、利益幅は税率によって変化します。 利益は次の数式で決まります。<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_国境を越えた価格の一貫性を有効にするには、次の手順に従います。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. マルチサイト設定の場合は、 **[!UICONTROL Store View]** を web サイトに追加し、設定のターゲットとなるを保存します。

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Calculation Settings]** 」セクションに入力します。

1. 設定 **[!UICONTROL Catalog Prices]** から `Including Tax`.

1. 国境を越えた価格の一貫性を有効にするには、 **[!UICONTROL Enable Cross Border Trade]** から `Yes`.

   ![国境を越えた取引設定を有効にする](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
