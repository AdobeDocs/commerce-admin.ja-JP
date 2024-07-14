---
title: 税の構成設定
description: 税金クラス、計算、デフォルトの税金宛先など、基本的な税金設定を構成する方法を説明します。
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# 税の構成設定

以下の手順に従うことで、Commerce インスタンスの基本的な税金設定を行うことができます。 税金を設定する前に、[ ロケール ](store-localize.md#step-3-change-the-locale-of-the-store-view) の税金要件を熟知していることを確認してください。 次に、要件に従って税金設定を完了します。

管理者 [ 権限 ](../systems/permissions.md) は、ビジネス ](../systems/permissions-user-roles.md) 必要な情報 _に基づいて、税金リソースに [ アクセス_ を制限するように設定できます。 税金設定へのアクセス権を持つ管理者ロールを作成するには、「売上/税金」および「システム/税金」リソースの両方を選択します。 デフォルトの出荷元と異なる地域に web サイトを設定する場合は、その役割のシステム/出荷資源へのアクセスも許可する必要があります。 配送設定によって、カタログ価格に使用する店舗の税率が決まります。

## 一般税金設定の構成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. マルチサイト設定の場合は、**[!UICONTROL Store View]** を web サイトに設定し、設定のターゲットとなるストアを指定します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Tax]**」を選択します。

1. 次の設定を行います。

   必要に応じて、グレー表示になっている設定の「**[!UICONTROL Use system value]**」チェックボックスをオフにします。

### [!UICONTROL Tax Classes]

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Tax Classes]**」セクションを展開します。

   ![ 税の区分 ](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **出荷用の税金区分**：適切な区分に設定します。 デフォルトのクラスは `None` と `Taxable Goods` です。
   - **ギフトオプションの税クラス** — ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）適切なクラスに設定します。 デフォルトのクラスは `None` と `Taxable Goods` です。
   - **製品のデフォルトの税区分**：適切な区分に設定します。 デフォルトのクラスは `None` と `Taxable Goods` です。
   - **顧客のデフォルト税金区分**：適切な区分に設定します。 デフォルトのクラスは `Retail Customer` と `Wholesale Customer` です。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### [!UICONTROL Calculation Settings]

1. 「**[!UICONTROL Calculation Settings]**」セクションを展開します。

   ![ 算定の設定 ](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Tax Calculation Method Based On]** を次のいずれかに設定します。

   - `Unit Price` – 各製品の価格
   - `Row Total` – 受注の明細品目の合計（値引きを差し引いた値）
   - `Total` – 注文の合計

1. **[!UICONTROL Tax Calculation Based On]** を次のいずれかに設定します。

   - `Shipping Address` – 注文を発送する住所
   - `Billing Address` – 顧客または会社の請求先住所
   - `Shipping Origin` - ストアの [ 接触チャネル ](shipping-settings.md#point-of-origin) として指定されるアドレス

1. **[!UICONTROL Catalog Prices]** を `Excluding Tax` または `Including Tax` に設定します。

1. **[!UICONTROL Shipping Prices]** を `Excluding Tax` または `Including Tax` に設定します。

1. 税金を元の価格に適用するか割引価格に適用するかを決定するには、**[!UICONTROL Apply Customer Tax]** を次のいずれかに設定します：`After Discount` または `Before Discount`

1. 割引に税金が含まれているか税金が含まれていないかを判断するには、**[!UICONTROL Apply Discount on Prices]** を次のいずれかに設定します：`Excluding Tax` または `Including Tax`

1. **[!UICONTROL Apply Tax On]** を `Custom price if available` または `Original price only` に設定します。

1. **[!UICONTROL Enable Cross-Border Trade]** を次のいずれかに設定します。

   - `Yes` – 異なる税率に対して一貫性のある価格設定を使用します。 カタログ価格に税金が含まれる場合、顧客の税率に関係なく価格を固定するには、この設定を選択します。
   - `No` – 税率によって価格を変えます。

   >[!IMPORTANT]
   >
   >[ クロスボーダー取引 ](#cross-border-price-consistency) が有効化されている場合、税率別に利益率が変化します。 利益は式（`Revenue - CustomerVAT - CostOfGoodsSold`）によって決定されます。 国境を越えた貿易を可能にするには、価格を税込みに設定しなければなりません。

### [!UICONTROL Default Tax Destination Calculation]

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Default Tax Destination Calculation]**」セクションを展開します。

   ![ デフォルト税金搬送先計算 ](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 税金計算の **[!UICONTROL Default Country]** を指定します。

1. 必要に応じて、税金計算の **[!UICONTROL Default State]** を指定します。

1. 必要に応じて、税金計算の **[!UICONTROL Default Post Code]** を指定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>税金を含む場合と税金を含まない場合の両方の価格表示に関連する設定の組み合わせが、お客様にとって混乱を招く可能性があります。 警告メッセージがトリガーされないようにするには、[ 推奨設定 ](taxes.md#warning-messages) を参照してください。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Price Display Settings]**」セクションを展開します。

   ![ 価格表示設定 ](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display Product Prices in Catalog]** を次のいずれかに設定します。

   - `Excluding Tax` - ストアフロントに表示されるカタログ価格には、税は含まれていません。
   - `Including Tax` - ストアフロントのカタログ価格には、税務処理基準が税源と一致する場合、または顧客の住所が税務処理基準と一致する場合にのみ税金が含まれます。 この問題は、顧客がアカウントを作成した後、ログインした後、またはカート内の税金と送料の見積もりツールを使用した後に発生する可能性があります。
   - `Including and Excluding Tax` - ストアフロントに表示されるカタログ価格は、税の有無にかかわらず表示されます。

1. **[!UICONTROL Display Shipping Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### [!UICONTROL Shopping Cart Display Settings]

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Shopping Cart Display Settings]**」セクションを展開します。

   ![ 買い物かごの表示設定 ](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 次の各設定について、店舗と地域の要件に応じて、買い物かごに税金と価格を表示する方法を選択します。

   - **[!UICONTROL Display Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - **[!UICONTROL Display Subtotal]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - **[!UICONTROL Display Shipping Amount]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

1. 必要に応じて、次の表示オプションを `Yes` または `No` に設定します。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** のセクションの ![ 展開 ](../assets/icon-display-expand.png) を展開します。

   ![ 注文、請求書、クレジット メモの表示設定 ](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 注文、請求書、およびクレジット メモでの価格と税金の表示方法を指定します。

   - **[!UICONTROL Display Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - **[!UICONTROL Display Subtotal]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - **[!UICONTROL Display Shipping Amount]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Gift Wrapping Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **[!UICONTROL Display Printed Card Prices]** を `Excluding Tax`、`Including Tax` または `Including and Excluding Tax` に設定します。

1. 必要に応じて、次の表示オプションを `Yes` または `No` に設定します。

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### [!UICONTROL Fixed Product Taxes]

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Fixed Product Taxes]**」セクションを展開します。

   ![ 固定製品税 ](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. 必要に応じて、**[!UICONTROL Enable FPT]** を `Yes` または `No` に設定します。

1. FPT が有効な場合は、FPT 表示オプションを指定します。

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` – 表示される価格には固定製品税が含まれます。 FPT 金額は個別には表示されません。
   - `Including FPT and FPT description` – 表示される価格には固定製品税が含まれます。 FPT 金額は個別に表示されます。
   - `Excluding FPT. Including FPT description and final price` – 表示価格には固定製品税は含まれていません。 FPT 金額は個別に表示されます。
   - `Excluding FPT` – 表示価格には固定製品税は含まれていません。 FPT 金額は個別には表示されません。

1. 必要に応じて、**[!UICONTROL Apply Discounts to FPT]** を `Yes` または `No` に設定します。

1. **[!UICONTROL FPT Tax Configuration]** を設定して、FPT の計算方法を決定します。

   - `Not Taxed` – 課税管轄区域が FPT に課税しない場合は、このオプションを選択します。 （例：California）。
   - `Taxed` – 課税管轄区域で FPT が税金である場合は、このオプションを選択します。 （例えば、カナダ）。
   - `Loaded and Displayed with Tax` – 税金を適用する前に FPT を受注合計に追加する場合は、このオプションをクリックします。 （例えば、EU 諸国）。

1. 必要に応じて、**[!UICONTROL Include FPT in Subtotal]** を `Yes` または `No` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 国境を越えた価格の一貫性

国境を越えた貿易（価格の一貫性とも呼ばれます）は、EU （欧州連合）や、店舗の税率と異なる税率を使用する顧客の価格を一貫して維持したい他のマーチャントをサポートします。

地域や地域をまたいで営業しているマーチャントは、商品の価格に税を含めることで 1 つの価格を表示できます。 国ごとに異なる税制構造や税率に関係なく、料金はクリーンで散乱がありません。 これらの設定では、_Vertex Cloud_ などの [Marketplace](../getting-started/commerce-marketplace.md) から税金計算拡張機能をインストールする必要があります。

>[!NOTE]
>
>国境を越えた取引が有効化されると、税率別に利益率が変化します。 利益は次の式によって決定されます。<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_クロスボーダー価格の一貫性を有効にするには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. マルチサイト設定の場合は、**[!UICONTROL Store View]** を web サイトに設定し、設定のターゲットとなるストアを指定します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Tax]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Calculation Settings]**」セクションを展開します。

1. **[!UICONTROL Catalog Prices]** を `Including Tax` に設定します。

1. クロスボーダーの価格の一貫性を有効にするには、**[!UICONTROL Enable Cross Border Trade]** を `Yes` に設定します。

   ![ 国境を越えた貿易設定を有効にする ](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
