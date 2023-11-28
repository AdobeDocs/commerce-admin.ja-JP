---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Tax] コマース管理のページ。
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: 0d1bb3666be18676acd770b6b96e4ee46d3cf1c9
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Adobe CommerceとMagento Open Sourceリリース 2.4.0 ～ 2.4.3 には、との統合に使用する、頂点ベンダーが開発した拡張機能が含まれていました。 [!UICONTROL Vertex Cloud]. 2.4.4 リリース以降、この拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールおよび更新する必要があります。 また、Marketplace では、拡張機能の開発者が提供する最新のドキュメントにアクセスできます。
><br><br>
>バンドルされた拡張機能を有効にして設定済みの場合、2.4.4 アップグレードプロセスの一環として composer.json ファイルを更新し、今後の拡張機能の更新を管理する必要があります。 詳しくは、 [モジュールと拡張機能のアップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) （内） _アップグレードガイド_ を参照してください。

{{config}}

## [!UICONTROL Tax Classes]

![税区分](./assets/tax-tax-classes.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [税区分](../../stores-purchase/tax-class.md) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Web サイト | 出荷に使用する税区分を識別します。 オプションには、使用可能なすべての製品税区分が含まれます。 `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) ギフトオプションに使用されるデフォルトの税区分を識別します。 |
| [!UICONTROL Default Tax Class for Product] | グローバル | 製品に使用されるデフォルトの税区分を識別します。 |
| [!UICONTROL Default Tax Class for Customer] | グローバル | 顧客に使用されるデフォルトの税区分を識別します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Calculation Settings]

![計算設定](./assets/tax-calculation-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Web サイト | 注文の税金の計算に使用する方法を決定します。 オプション：<br/>**`Unit Price`**— 税の計算は各製品の単価に基づきます。<br/>**`Row Total`**  — 税金の計算は、行項目の合計に基づきます。 <br/>**`Total`**— 税金の計算は受注合計に基づきます。<br/><br/>_**&#x200B;注意：**_税額計算の延長が Marketplace からインストールされている場合（例： ）。 _頂点雲_に設定すると、拡張機能サービスはオプションとして表示されます。 |
| [!UICONTROL Tax Calculation Based On] | Web サイト | 税金の計算が、配送先住所、請求先住所、または配送元に基づいて行われるかどうかを決定します。 オプション： `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Web サイト | カタログ価格に税を含めるか、含めないかを指定します。 オプション： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Web サイト | 輸送価格に税を含めるか除外するかを決定します。 オプション： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Web サイト | 税が適用される前か、割引後かを決定します。 オプション： `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Web サイト | 割引価格に税を含めるか除外するかを指定します。 オプション： `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Web サイト | 税金を元の価格に適用するか、カスタム価格に適用するかを指定します（可能な場合）。 オプション： `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Web サイト | 有効にすると、異なる税率を持つ地域の国境をまたいで一貫した価格設定が適用されます。 オプション： `Yes` / `No` <br/><br/>**_注意：_**国境を越えた貿易を利用すると、税率によって利益幅が調整されます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Tax Destination Calculation]

![デフォルトの税金宛先の計算](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Country] | ストア表示 | 税の計算に基づく国を決定します。 |
| [!UICONTROL Default State] | ストア表示 | 税金計算の基準となる州を決定します。 アスタリスク (*) は、選択した国内のすべての州を示すワイルドカードとして機能できます。 |
| [!UICONTROL Default Post Code] | ストア表示 | 税金の計算に基づく郵便番号または郵便番号を識別します。 アスタリスク (*) は、選択した状態のすべての郵便番号を示すワイルドカードとして機能します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Price Display Settings]

![価格の表示設定](./assets/tax-price-display-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [価格の表示設定の指定](../../stores-purchase/display-settings.md#configure-price-display-settings) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | ストア表示 | カタログに公開された製品価格に税を含めるか除外するか、価格の 2 つのバージョン（1 つは付き、もう 1 つは税なし）を表示するかを指定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_注意：_**「製品価格を表示」フィールドを `Including Tax`、税金が表示されるのは、税源と一致する税金ルールがある場合、または税金ルールと一致する顧客住所がある場合のみです。 一致をトリガーできるイベントには、顧客アカウントの作成、ログイン、買い物かごでの税金と送料の見積もりツールの使用などがあります。 |
| [!UICONTROL Display Shipping Prices] | ストア表示 | 送料に税を含めるか除外するかを決定します。また、送料の 2 つのバージョン（1 つは、もう 1 つは税なし）を表示します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Shopping Cart Display Settings]

![買い物かごの表示設定](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [買い物かごの表示設定を構成](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | ストア表示 | 買い物かごの価格に税金を含めるか除外するかを決定します。また、価格の 2 つのバージョン（1 つは付き、もう 1 つは税金なし）を表示するかどうかを決定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | 買い物かごの小計に税金を含めるか除外するかを指定します。小計の 2 つのバージョン（1 つは付き、もう 1 つは税なし）を表示します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | ストア表示 | 買い物かごの送料に税を含めるか除外するかを決定します。または、送料の 2 つのバージョン（1 つは付き、もう 1 つは税なし）を表示します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | ストア表示 | 買い物かごに、税のない総計金額の余分な行を表示するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | ストア表示 | 買い物かごに完全な税金要約が含まれているかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | ストア表示 | 税金がゼロの場合に、買い物かごに税額の小計が含まれるかどうかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![オーダー、請求書、クレジット・メモの表示設定](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [注文、請求書、クレジットメモの表示設定を構成します](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | ストア表示 | 販売ドキュメントの価格に税を含めるか除外するかを指定します。また、各ドキュメントに価格の 2 つのバージョン（1 つは付き、もう 1 つは税なし）が表示されるかどうかを指定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | ストア表示 | 販売ドキュメントの小計に税を含めるか除外するか、各ドキュメントに小計の 2 つのバージョン（1 つは付き、もう 1 つは税なし）が表示されるかを指定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | ストア表示 | 販売ドキュメントの送料に税を含めるか除外するか、各ドキュメントに小計の 2 つのバージョン（1 つは付き、もう 1 つは税なし）が表示されるかを決定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | ストア表示 | 税のない総計金額の余分な行を販売ドキュメントに表示するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | ストア表示 | 販売ドキュメントに完全な税の要約を表示するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | ストア表示 | 税金が請求されない場合に販売ドキュメントの小計セクションを表示するかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | ストア表示 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) ギフト用ラッピングの価格を小計に含めるかどうかを指定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | ストア表示 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 印刷されたカード価格を小計に含めるかどうかを指定します。 オプション： `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixed Product Taxes]

![固定製品税](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [固定製品税 (FPT)](../../stores-purchase/fixed-product-tax.md) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Web サイト | FPT が使用可能かどうかを判断します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Web サイト | 製品リストでの FPT の表示を制御します。 オプション：<br/> **`Including FPT Only`**  — 表示される価格は、固定製品税を含む。 FPT 金額は別に表示されません。<br/>**`Including FPT and FPT description`**— 表示される価格は、固定製品税を含む。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT. Including FPT description and final price`**  — 表示される価格には、固定製品税は含まれません。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT`**— 表示される価格には、固定製品税は含まれません。 FPT 金額は別に表示されません。 |
| 製品表示ページに価格を表示 | Web サイト | 製品ページでの FPT の表示を制御します。 オプション：<br/> **`Including FPT Only`**  — 表示される価格は、固定製品税を含む。 FPT 金額は別に表示されません。<br/>**`Including FPT and FPT description`**— 表示される価格は、固定製品税を含む。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT. Including FPT description and final price`**  — 表示される価格には、固定製品税は含まれません。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT`**— 表示される価格には、固定製品税は含まれません。 FPT 金額は別に表示されません。 |
| [!UICONTROL Display Prices in Sales Modules] | Web サイト | 買い物かごとチェックアウト時の FPT の表示を制御します。 オプション：<br/> **`Including FPT Only`**  — 表示される価格は、固定製品税を含む。 FPT 金額は別に表示されません。<br/>**`Including FPT and FPT description`**— 表示される価格は、固定製品税を含む。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT. Including FPT description and final price`**  — 表示される価格には、固定製品税は含まれません。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT`**— 表示される価格には、固定製品税は含まれません。 FPT 金額は別に表示されません。 |
| [!UICONTROL Display Prices in Emails] | Web サイト | E メールでの FPT の表示を制御します。 オプション：<br/> **`Including FPT Only`**  — 表示される価格は、固定製品税を含む。 FPT 金額は別に表示されません。<br/>**`Including FPT and FPT description`**— 表示される価格は、固定製品税を含む。 FPT 金額は、別々に表示されます。<br/>** FPT を除外しています。 FPT の説明と最終価格を含む&#x200B;**— 表示される価格には、固定製品税は含まれません。 FPT 金額は、別々に表示されます。<br/>**`Excluding FPT`**  — 表示される価格には、固定製品税は含まれません。 FPT 金額は別に表示されません。 |
| [!UICONTROL Apply Discounts to FPT] | Web サイト | 割引を FPT 金額に適用できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL FPT Tax Configuration] | Web サイト | FPT 税の計算方法を決定します。 オプション： <br/>**`Not Taxed`**— 課税管轄区域が FPT に課税されない場合は、このオプションを選択します。 （例：カリフォルニア）。<br/>**`Taxed`**  — 課税管轄区域が税金 FPT の場合は、このオプションを選択します。 （例：カナダ）。 <br/>**`Loaded and Displayed with Tax`**— 税金を適用する前に FPT が注文合計に追加される場合は、このオプションをクリックします。 （例：EU 諸国）。 |
| [!UICONTROL Include FPT in Subtotal] | Web サイト | FPT が買い物かごの小計に含まれるかどうかを指定します。 オプション： <br/>**`Yes`**— 買い物かごの小計に FPT を含みます。<br/>**`No`** - FPT は小計に含まれず、買い物かごの小計の後に配置されます。 |

{:style=&quot;table-layout:auto&quot;}
