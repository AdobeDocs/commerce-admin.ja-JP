---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Sales] ページで設定を確認します。
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![&#x200B; 一般 &#x200B;](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | ストア表示 | 顧客 IP アドレスが注文、請求書、出荷、およびクレジット メモに表示されるかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![&#x200B; チェックアウト合計の並べ替え順序 &#x200B;](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Web サイト | 他のチェックアウトの合計との関連で小計を計算するタイミングを決定する数値です。 デフォルト値：`10` |
| [!UICONTROL Discount] | Web サイト | その他のチェックアウト合計に関連して割引を計算するタイミングを決定する数値。 デフォルト値：`20` |
| [!UICONTROL Shipping] | Web サイト | その他のチェックアウト合計に関して配送を計算するタイミングを決定する数値。 デフォルト値：`30` |
| [!UICONTROL Tax] | Web サイト | その他のチェックアウト合計に関連して税金を計算するタイミングを決定する数値。 デフォルト値：`40` |
| [!UICONTROL Fixed Product Tax] | Web サイト | その他のチェックアウト合計に関連して固定製品税を計算するタイミングを決定する数値です。 デフォルト値：`50` |
| [!UICONTROL Grand Total] | Web サイト | 他のチェックアウトの合計に関連して総計を計算するタイミングを決定する数値です。 デフォルト値：`100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![&#x200B; 並べ替え &#x200B;](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | ストア表示 | 顧客がアカウントから並べ替えることができるかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | ストア表示 | 総計が 0 のクレジット メモを作成できるかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![&#x200B; 請求書および梱包明細の設計 &#x200B;](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | ストア表示 | PDFの請求書および納品書のヘッダーに表示されるロゴファイルを特定します。 許可されるファイルタイプ : <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | ストア表示 | 請求書および梱包明細のHTML印刷ビューのヘッダーに表示されるロゴ ファイルを識別します。 許可されるファイルタイプ : <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | ストア表示 | 請求書および梱包明細に表示する店舗の住所。 |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![&#x200B; 最小注文金額 &#x200B;](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | Web サイト | サイトに対して最小注文金額が設定されているかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Minimum Amount] | Web サイト | 割引が適用された後の小計の最小値と注文を指定します。 |
| [!UICONTROL Include Discount Amount] | Web サイト | 最小注文金額に適用済みの割引が含まれるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Web サイト | 最小注文金額に税が含まれるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Description Message] | ストア表示 | 買い物かごの合計が最小注文金額を下回っている場合に、買い物かごの上部に表示されるメッセージを決定します。 空白のままにすると、次のデフォルトのメッセージが表示されます。`Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | ストア表示 | 注文金額が必要な最小注文金額を下回っている場合に、ミニ カートまたはチェックアウト リンクから表示されるメッセージを決定します。 空白の場合は、デフォルトのメッセージが表示されます。 |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Web サイト | 複数品目の注文の場合、別々の住所に移動する注文品目が最小注文額を大幅に満たしているかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | ストア表示 | 複数アドレスからの注文の場合、あるアドレスに送信された商品が最小注文金額に満たない場合に、買い物かごに表示されるメッセージを決定します。 |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | ストア表示 | 複数アドレスの注文の場合、は、注文金額が必要な最小注文金額よりも少ない場合に、ミニ買い物かごまたはチェックアウトリンクから表示されるメッセージを決定します。 空白の場合は、デフォルトのメッセージが表示されます。 |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![&#x200B; ダッシュボード &#x200B;](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | グローバル | リアルタイムで集計された売上データを使用してダッシュボードのスナップショット レポートを作成するかどうかを決定します。 処理するデータが大量にある場合は、リアルタイムデータの表示をオフにすることでパフォーマンスを向上させることができます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![&#x200B; 注文 Cron 設定 &#x200B;](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Web サイト | 保留中の注文の有効期限を分単位で決定します。 デフォルト設定：`480` 分（8 時間） |

{style="table-layout:auto"}

## [!UICONTROL Promotions]

[!BADGE SaaS のみ &#x200B;]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

[!BADGE &#x200B; サンドボックス &#x200B;]{type=Caution tooltip="リストされた項目は、現在、サンドボックス環境でのみ使用できます。 Adobeでは、最初にサンドボックス環境で新しいリリースを使用できるようにして、リリースが実稼動環境で使用できるようになる前に、今後の変更をテストするための時間を提供します。"}

![&#x200B; プロモーションの設定 &#x200B;](./assets/sales-promotions-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Apply Catalog Price Rule on Grouped Price] | グローバル | 階層価格の数量が [&#x200B; に設定されている場合に &#x200B;](../../catalog/product-price-tier.md) カタログ価格ルールの階層価格を `1` 有効にします。  オプション：`Yes` / `No` |

## [!UICONTROL Gift Options]

![&#x200B; ギフト オプション &#x200B;](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Web サイト | 注文全体に対してギフト メッセージを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Messages on Order Items] | Web サイト | 個別の注文品目に対してギフト メッセージを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）注文全体に対してギフト包装を追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）個々の注文項目に対してギフト包装を追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Receipt] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）注文に対してギフト受領書を追加できるかどうかを指定します。 |
| [!UICONTROL Allow Printed Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）印刷されたカードを注文に追加できるかどうかを指定します。 |
| [!UICONTROL Default Price for Printed Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）印刷されるカードのデフォルトの価格を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![&#x200B; 最低広告価格 &#x200B;](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Web サイト | ストアの最小広告価格を有効化します。 オプション：`Yes` / `No` |
| [!UICONTROL Display Actual Price] | Web サイト | 製品の実際の価格が顧客に表示される場所を決定します。 オプション：<br/>**`In Cart`**- ショッピングカートの実際の製品価格を表示します。<br/>**`Before Order Confirmation`** – 注文が確認される直前の、チェックアウトプロセスの最後に実際の製品価格を表示します。 <br/>**`On Gesture`**– 「価格を表示」または「これについて」をクリックすると、実際の製品価格がポップアップに表示されます。 リンク。 |
| [!UICONTROL Default Popup Text Message] | ストア表示 | 顧客がカテゴリリストまたは製品表示ページから「クリックして価格を選択」リンクを選択すると表示されるテキストメッセージ。 |
| [!UICONTROL Default "What's This" Text Message] | ストア表示 | 顧客が「これはなんですか？」をクリックすると表示されるテキストメッセージ 製品表示ページからのリンク。 |
| [!UICONTROL Manufacturer's Suggested Retail Price] | グローバル | 製造元（MSRP）によって提示された小売価格。 |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![&#x200B; 多角形の設定 &#x200B;](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Web サイト | 注文ごとに許可されるクーポンの最大数を決定します。 この機能は、管理者、GraphQLおよび REST API でのみ使用できます。 また、Storefront では **_使用できません_**。 |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![SKU 設定で並べ替え &#x200B;](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![&#x200B; 顧客グループの SKU 設定による注文 &#x200B;](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Web サイト | Order by SKU が顧客アカウントダッシュボードで使用できるかどうかを決定します。 オプション：<br/>**`Yes, for Everyone`**- 「SKU で注文」タブは、すべての顧客のアカウントダッシュボードに表示されます。<br/>**`Yes, for Specified Customer Groups`** – 指定したグループまたは共有カタログのメンバーに対して、アカウントダッシュボードに「SKU で並べ替え」タブが表示されます。 <br/>**`No`**– 「SKU で注文」タブは、お客様のアカウントでは使用できません。 |
| [!UICONTROL Customer Groups] | Web サイト | 顧客グループを決定します。 オプション：`General`/`Retailer`/`Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![&#x200B; 即時購入 &#x200B;](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | Braintreeなどの支払い方法で Vault が有効になっている場合に、店舗ビューの即時購入を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Button Text] | ストア表示 | [ インスタント購入 ] ボタンに表示するテキストを指定します。 デフォルトのテキストは `Instant Purchase` です。 |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![&#x200B; レート制限 &#x200B;](assets/sales-rate-limiting.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | ストア表示 | 店舗表示から注文を行う際にレート制限を使用するかどうかを決定します（デフォルトは `No`）。 オプション：`Yes`/`No`。 |
| [!UICONTROL Requests limit per authenticated customer] | ストア表示 | 認証済みの顧客が期間中に行うことができる購入リクエストの数。 デフォルトの制限は `10` です。 |
| [!UICONTROL Requests limit per guest] | ストア表示 | 認証されていない顧客が指定された期間中に行うことができる購入リクエストの数。 デフォルト値は `50` です。 |
| [!UICONTROL Counter resets in a ...] | ストア表示 | 認証済みまたは未認証の顧客が一定数の購入リクエストを行うことができる期間（デフォルトは `Minute`）。 オプション：`Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![&#x200B; 受注、請求書、出荷、クレジット・メモ・アーカイブ &#x200B;](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

これらの設定の変更について詳しくは、[&#x200B; ストアと購入エクスペリエンスガイド &#x200B;](../../stores-purchase/order-archive.md#configure-the-order-archive) の _注文アーカイブの設定_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | グローバル | アーカイブが有効かどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | グローバル | 完了した注文がアーカイブされるまでの日数を決定します。 デフォルト値：`30` |
| [!UICONTROL Order  Statuses to be Archived] | グローバル | アーカイブする注文の [&#x200B; ステータス &#x200B;](../../stores-purchase/order-status.md) を決定します。 デフォルトでは、ステータスが「完了」または「クローズ」の注文がアーカイブされます。 オプション：`Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA 設定 &#x200B;](./assets/sales-rma-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、[&#x200B; ストアと購入エクスペリエンスガイド &#x200B;](../../stores-purchase/rma-configure.md) の _返品の設定_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Web サイト | 顧客がストアフロントから RMA リクエストを作成および表示できるかどうかを決定します。 RMA は、新規注文と既存注文の両方に適用できます。 デフォルトでは、ストアフロントに対する RMA は有効になっていません。 オプション：`Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Web サイト | 製品情報の [RMA を有効にする ] フィールドの既定値を決定します。 |
| [!UICONTROL Use Store Address] | Web サイト | 返品された商品の出荷に使用される連絡先名および住所を決定します。 オプション：<br/>**`Yes`**– 出荷設定で指定した [&#x200B; 出荷元の場所 &#x200B;](../../stores-purchase/shipping-settings.md#point-of-origin) の住所を使用します。<br/>**`No`** – 住所フォームを開いて、別の住所を入力できます。 |

{style="table-layout:auto"}
