---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Sales] コマース管理のページ。
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

{{beta-updates}}

## [!UICONTROL General]

![一般](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/sales-documents-ref-id.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | ストア表示 | 顧客の IP アドレスが、注文、請求書、出荷、クレジットメモに表示されるかどうかを決定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Checkout Totals Sort Order]

![チェックアウト合計の並べ替え順](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://docs.magento.com/user-guide/sales/checkout-totals-sort-order.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Web サイト | 他のチェックアウト合計に対する小計を計算するタイミングを決定する数値。 デフォルト値： `10` |
| [!UICONTROL Discount] | Web サイト | 他のチェックアウト合計に対する割引をいつ計算するかを決定する数値です。 デフォルト値： `20` |
| [!UICONTROL Shipping] | Web サイト | 配送先を他のチェックアウト合計と比較して計算するタイミングを決定する数値。 デフォルト値： `30` |
| [!UICONTROL Tax] | Web サイト | 他のチェックアウト合計に対する税金の計算日を決定する数値です。 デフォルト値： `40` |
| [!UICONTROL Fixed Product Tax] | Web サイト | 他のチェックアウト合計に対して固定製品税をいつ計算するかを決定する数値です。 デフォルト値： `50` |
| [!UICONTROL Grand Total] | Web サイト | 他のチェックアウト合計に対して総計をいつ計算するかを決定する数値です。 デフォルト値： `100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Reorder]

![並べ替え](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://docs.magento.com/user-guide/sales/reorders-allow.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | ストア表示 | 顧客が自分のアカウントから並べ替えを行えるかどうかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Allow Zero Grand Total]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | ストア表示 | 総計がゼロのクレジット・メモを作成する可能性を決定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Invoice and Packing Slip Design]

![請求書および梱包明細の設計](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://docs.magento.com/user-guide/marketing/sales-document-pdf-logo.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | ストア表示 | PDF請求書および梱包明細のヘッダーに表示されるロゴファイルを識別します。 許可されているファイルタイプ： <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | ストア表示 | 請求書および梱包明細のHTML印刷表示のヘッダーに表示されるロゴファイルを識別します。 許可されているファイルタイプ： <br/>JPG/JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | ストア表示 | 請求書および梱包明細に表示する店舗住所。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Minimum Order Amount]

![最小注文額](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://docs.magento.com/user-guide/sales/cart-minimum-order-amount.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable] | Web サイト | サイトの最小注文額が設定されているかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Web サイト | 割引が適用された後の最小小計の注文を指定します。 |
| [!UICONTROL Include Discount Amount] | Web サイト | 最小注文額に適用された割引が含まれるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Web サイト | 最小注文額に税が含まれているかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Description Message] | ストア表示 | 買い物かごの合計が最小注文額を下回った場合に、買い物かごの上部に表示されるメッセージを決定します。 空白の場合、次のデフォルトのメッセージが表示されます。 `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | ストア表示 | 注文額が必要な最小注文額を下回った場合にミニカートまたはチェックアウトリンクから表示されるメッセージを決定します。 空白の場合、デフォルトのメッセージが表示されます。 |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Web サイト | 複数品目オーダーの場合、別々の住所に行く注文項目が最小注文額を満たしているかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | ストア表示 | 複数アドレスの注文の場合、は、アドレスに送信された品目が最小注文額を下回った場合に、買い物かごに表示されるメッセージを決定します。 |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | ストア表示 | 複数の住所を持つ注文の場合、は、注文額が必要な最小注文額を下回ったときにミニカートまたはチェックアウトリンクから表示されるメッセージを決定します。 空白の場合、デフォルトのメッセージが表示されます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Dashboard]

![ダッシュボード](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://docs.magento.com/user-guide/stores/admin-dashboard.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | グローバル | リアルタイムの集計販売データを使用してダッシュボードのスナップショットレポートを作成するかどうかを決定します。 処理するデータ量が多い場合は、リアルタイムデータの表示をオフにすることでパフォーマンスを向上できます。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Orders Cron Settings]

![Cron 設定を注文](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://docs.magento.com/user-guide/system/cron.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Web サイト | 保留中の注文の有効期間を分単位で決定します。 デフォルト設定： `480` 分（8 時間） |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Gift Options]

![ギフトオプション](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://docs.magento.com/user-guide/sales/gift-options.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Web サイト | 注文全体に対してギフトメッセージを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Messages on Order Items] | Web サイト | 個々の注文項目に対してギフトメッセージを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) ギフト用ラッピングを注文全体に追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 個々の注文項目にギフト用ラッピングを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Gift Receipt] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 注文にギフトレシートを追加できるかどうかを指定します。 |
| [!UICONTROL Allow Printed Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 印刷されたカードを注文に追加できるかどうかを指定します。 |
| [!UICONTROL Default Price for Printed Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 印刷するカードのデフォルト価格を指定します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Minimum Advertised Price]

![最小広告価格](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://docs.magento.com/user-guide/catalog/product-price-minimum-advertised.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Web サイト | ストアの最小アドバタイズ価格を有効化します。 オプション： `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Web サイト | 製品の実際の価格を顧客に表示する場所を決定します。 オプション： <br/>**`In Cart`**— 買い物かごの実際の製品価格を表示します。<br/>**`Before Order Confirmation`**  — チェックアウトプロセスの最後、注文が確認される直前の実際の製品価格を表示します。 <br/>**`On Gesture`**— 顧客が「価格をクリック」または「価格をクリック」をクリックしたときに、ポップアップに実際の製品価格が表示されます。 リンク。 |
| [!UICONTROL Default Popup Text Message] | ストア表示 | 顧客がカテゴリリストまたは製品表示ページから「価格でクリック」リンクを選択すると表示されるテキストメッセージ。 |
| [!UICONTROL Default "What's This" Text Message] | ストア表示 | 顧客が「What&#39;s this?」（これは何ですか？）をクリックすると表示されるテキストメッセージ リンクを製品表示ページから削除します。 |
| [!UICONTROL Manufacturer's Suggested Retail Price] | グローバル | 製造元 (MSRP) が提示する小売価格。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![SKU 設定別の順序](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://docs.magento.com/user-guide/customers/account-dashboard-order-by-sku.html) -->

![顧客グループの SKU 設定別の注文](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Web サイト | 顧客アカウントダッシュボードで「 SKU ごとの注文」を使用できるかどうかを指定します。 オプション： <br/>**`Yes, for Everyone`**- 「 SKU ごとの並べ替え」タブは、すべての顧客のアカウントダッシュボードに表示されます。<br/>**`Yes, for Specified Customer Groups`** - 「SKU で並べ替え」タブは、指定したグループのメンバーまたは共有カタログのアカウントダッシュボードに表示されます。 <br/>**`No`**— 顧客アカウントでは、「 SKU ごとの並べ替え」タブを使用できません。 |
| [!UICONTROL Customer Groups] | Web サイト | 顧客グループを決定します。 オプション： `General` / `Retailer` / `Wholesale` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Instant Purchase]

![即時購入](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://docs.magento.com/user-guide/sales/checkout-instant-purchase.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | Braintreeなどの支払い方法が Vault を有効にしている場合に、店舗表示の即時購入を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Button Text] | ストア表示 | [ 即時購入 ] ボタンに表示するテキストを指定します。 デフォルトのテキストは、 `Instant Purchase`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![オーダー、請求書、出荷、クレジット・メモ・アーカイブ](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [オーダーアーカイブの設定](../../stores-purchase/order-archive.md#configure-the-order-archive) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | グローバル | アーカイブが有効かどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | グローバル | 完了した注文がアーカイブされるまでの日数を決定します。 デフォルト値： `30` |
| [!UICONTROL Order  Statuses to be Archived] | グローバル | を決定します。 [ステータス](../../stores-purchase/order-status.md) アーカイブする注文の件数です。 デフォルトでは、ステータスが「完了」または「クローズ」のオーダーはアーカイブされます。 オプション： `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA 設定](./assets/sales-rma-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [戻り値の設定](../../stores-purchase/rma-configure.md) （内） _店舗および購入エクスペリエンスガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Web サイト | 顧客がストアフロントから RMA 要求を作成および表示できるかどうかを指定します。 RMA は、新規受注と既存受注の両方に適用できます。 デフォルトでは、ストアフロントの RMA は有効になっていません。 オプション： `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Web サイト | 製品情報の「RMA の有効化」フィールドのデフォルト値を決定します。 |
| [!UICONTROL Use Store Address] | Web サイト | 返品された商品の出荷に使用する連絡先の名前と住所を決定します。 オプション： <br/>**`Yes`**— を使用します。 [原点](../../stores-purchase/shipping-settings.md#point-of-origin) 住所を [ 発送設定 ] から選択します。<br/>**`No`**  — 別の住所を入力できるように、住所フォームを開きます。 |

{:style=&quot;table-layout:auto&quot;}
