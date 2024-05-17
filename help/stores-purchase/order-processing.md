---
title: 注文のワークフローと処理
description: 注文ワークフロー、各ステップに適用されるステータス、このプロセスを通じて注文を移動する方法について説明します。
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1728'
ht-degree: 0%

---

# 注文のワークフローと処理

顧客が注文を行うと、そのトランザクションの一時的なレコードとして受注が作成されます。 受注グリッドでは、最初の受注のステータスは「保留」で、支払が処理されるまでいつでも取り消すことができます。 支払いが確認された後、注文を請求して出荷することができます。

**手順 1：注文する** - チェックアウトプロセスは、買い物客がクリックすると開始されます **[!UICONTROL Go to Checkout]** 買い物かごページ、 [並べ替え](reorders-allow.md) 顧客アカウントから直接。

**手順 2：オーダー保留**  – 最初の販売注文ステータスは `Pending`. この状態では、支払いは処理されておらず、注文は引き続き編集またはキャンセルできます。 この状態は、支払方法が承認モードに設定されている場合に発生します。

**手順 3：支払の受信**  – 注文のステータスが「」に変わります `Processing` 支払いが受領または承認されたとき。 支払い方法によっては、トランザクションが承認または処理されたときに通知が届く場合があります。 この状態は、支払方法がキャプチャまたはインテント販売モードに設定されている場合に自動的に発生します。

**手順 4：受注の請求**  – 注文は通常、支払いを受け取った後に請求されます。 支払い方法によって、注文に必要な請求オプションが決まります。 請求書が生成されて送信されると、コピーが顧客に送信されます。 次のように支払方法が設定されている場合 `capture` または `intent sale` 支払処理。支払が承認および取得されると、請求書が自動的に生成されます。

>[!NOTE]
>
>を使用して注文した場合、請求書は自動的には作成されません。 `Gift Card`, `Store Credit`, `Reward Points`、またはその他のオフライン支払い方法。

**手順 5：単一出荷の記帳**  – 注文のステータスが「」に変わります `Complete` 出荷詳細が完了すると、出荷が記帳され、出荷が設定されます。 出荷要件が、印刷された梱包明細および出荷ラベルまたは _集荷準備完了を通知_ が選択されています（店舗での配信方法）。 お客様に通知が届き、パッケージが出荷されます。 追跡番号を使用している場合、出荷は顧客のアカウントから追跡できます。

>[!NOTE]
>
>注文ステータスと支払い方法の設定オプションについて詳しくは、以下を参照してください。 [注文ステータス](order-status.md) および [支払額](payments.md).

## オーダーを表示

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッド内の順序を検索します。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL View]**.

1. 注文ステータスの確認：

   - A `Pending` 注文は変更、保留、キャンセル、請求および出荷が可能です。

   - A `Processing` 注文を大幅に編集またはキャンセルすることはできなくなりましたが、請求および配送先住所は編集できます。

   - A `Completed` 順序は並べ替えることができます。

顧客のメールは、注文ワークフローの任意の時点で、顧客を編集することで編集できます。 ゲストが注文した場合は、メールを編集できません。

オープン注文の左側のパネルから、注文に関連する様々なタイプの情報にアクセスできます。

![注文を表示](./assets/order-view.png){width="700" zoomable="yes"}

## オーダーを処理

顧客が注文を行うと、そのトランザクションの一時的なレコードとして受注が作成されます。 受注のステータスは `Pending` 支払いが受領されるまで。 の実行中 `Pending` ステータス、注文は、支払いを受け取り、請求書を生成するまで、編集またはキャンセルできます。 簡単に考えると、注文は請求書になり、請求書は出荷になります。 注文グリッドには、ワークフロー内の位置に関係なく、すべての注文が一覧表示されます。 顧客の注文を支援する方法については、を参照してください。 [注文を更新](order-update.md).

![注文件数](./assets/orders-grid.png){width="700" zoomable="yes"}

を開くには `Pending` 注文、クリック **[!UICONTROL Edit]** 右上隅

>[!NOTE]
>
>注文は、内でのみ編集できます `Pending` ステータス。 異なるステータスの注文か、に基づく注文については、「編集」ボタンが表示されません。 [交渉による見積](../b2b/quotes.md).

![販売注文の編集](./assets/order-pending.png){width="600" zoomable="yes"}

参照用のフィールドの説明を使用して、受注の次の項を確認します。

### 注文ビューの説明

| タブ | 説明 |
|--- |--- |
| [!UICONTROL Information] | 請求先と配送先住所、支払いと配送方法、品目注文、合計、メモなど、注文とアカウントに関する詳細情報を表示します。 |
| [!UICONTROL Invoices] | 注文に関連付けられている各請求書を一覧表示します。 |
| [!UICONTROL Credit Memos] | 受注に関連付けられている各クレジット・メモがリストされます。 |
| [!UICONTROL Shipments] | 注文に関連付けられている各出荷レコードを一覧表示します。 |
| [!UICONTROL Comments History] | 注文に関連するすべてのメモをリストします。 |

{style="table-layout:auto"}

>[!NOTE]
>
>管理者ユーザーには次が必要です **[!UICONTROL Sales / Archive]** [権限](../systems/permissions-user-roles.md) 役割の範囲に表示する内容 _請求書_, _クレジットメモ_、および _出荷_ 順序タブ

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに [ 受注 ] ページに戻ります。 |
| **[!UICONTROL Cancel]** | 販売注文をキャンセルします。 |
| **[!UICONTROL Send Email]** | 注文に関するメールを顧客に送信します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 販売注文の状態を次のように変更します `On Hold`. 受注の保留を解除する手順は、次のとおりです。 **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | 受注を請求書に変換して、受注から請求書を作成します。 |
| **[!UICONTROL Ship]** | 注文の出荷レコードを作成します。 |
| **[!UICONTROL Notify Order is Ready for Pickup]** | 注文が店舗の配信として配置された場合にのみ表示されます。 受注の集荷準備が完了したことを顧客に通知します。 |
| **[!UICONTROL Reorder]** | 現在の注文に基づいて販売注文を作成します。 |
| **[!UICONTROL Edit]** | 保留中の注文を編集モードで開きます。 ステータスがの注文では、「編集」ボタンは表示されません `Processing`または交渉済の見積に基づく注文。 |

{style="table-layout:auto"}

### 注文をキャンセル

次のことができます [キャンセル](order-update.md) まだ請求されていない注文。 A [クレジット メモ](credit-memos.md) 顧客が請求後に注文をキャンセルしたい場合は、発行する必要があります（支払いが取り込まれます）。

注文が `Pending` または `Processing` そして、支払いは完全にキャプチャされていないか、または完全にキャプチャされていません [注文を取り消す](#void-an-order) キャンセルする代わりに。

キャンセルした注文を復元するには、 **[!UICONTROL Reorder]** ボタンをクリックすると、ステータスを持つ新しい注文が作成されます `Pending`.

>[!NOTE]
>
>注文をキャンセルした場合も無効になりますが、注文を無効にしてもキャンセルはトリガーになりません。

### 注文を無効にする

未請求の販売注文のみ、状態は `Processing`、および [の支払い統合設定 `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions)、にすることができます [無効](order-update.md#void-a-processing-order). 注文を無効にした後は、キャンセルできます。

### [!UICONTROL Order and Account Information]

![注文およびアカウント情報](./assets/order-account-information.png){width="600" zoomable="yes"}

#### オーダー情報

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Order Number] | 注文番号が販売注文の上部に表示され、その後に確認メールが送信されたかどうかを示すメモが表示されます。 |
| [!UICONTROL Order Date] | 注文が行われた日時。 |
| [!UICONTROL Purchased From] | 注文が行われた web サイト、ストア、ストア表示を示します。 |
| [!UICONTROL Placed from IP] | 注文元のコンピューターの IP アドレスを示します。 |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能）は、 [見積もり](../b2b/quotes.md) 注文の生成元（該当する場合）。 見積書名は見積書にリンクされています。 |

{style="table-layout:auto"}

#### アカウント情報

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Customer Name] | 注文を行った顧客または購入者の名前。 顧客名が顧客プロファイルにリンクされています。 |
| [!UICONTROL Email] | 顧客または購入者の電子メールアドレス。 このメールアドレスに、新しいメールメッセージを開くリンクが付いています。 |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前。 |
| [!UICONTROL Company Name] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能）購入者が関連付けられており、その代わりに注文が行われる会社の名前。 会社名はにリンクされています [会社概要](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![住所情報](./assets/order-address-information.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Billing Address] | 注文を行った顧客または購入者の名前、続いて請求先住所、電話番号、および [VAT](vat.md)該当する場合。 電話番号は、モバイルデバイスでのオートダイヤルにリンクされています。 |
| [!UICONTROL Shipping Address] | 注文を出荷する必要がある人物の名前、出荷先住所、電話番号。 電話番号は、モバイルデバイスでのオートダイヤルにリンクされています。 |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![お支払いと配送方法](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Payment Information] | 注文に使用される支払い方法、発注書番号（該当する場合）、注文の際に使用された通貨が続きます。 注文が次を使用して会社クレジットに請求される場合 [分割払い](../b2b/enable-basic-features.md#configure-payment-on-account)、アカウントに請求された金額が示されています。 |
| [!UICONTROL Shipping & Handling Information] | 使用する発送方法と、該当する手数料。 |

{style="table-layout:auto"}

### 並べ替えられた項目を確認

![注文済み品目](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

が含まれる **[!UICONTROL Order Total]** セクションで、次の操作を行います。

1. を入力 **[!UICONTROL Comment]** を注文に含めます。

1. コメントを顧客にメールで送信する場合、 **[!UICONTROL Notify Customer by Email]** チェックボックス。

1. コメントを顧客アカウントに表示する場合、 **[!UICONTROL Visible on Storefront]** チェックボックス。

   ![注文の合計](./assets/order-total.png){width="600" zoomable="yes"}

1. 注文を請求する準備ができたら、 **[!UICONTROL Invoice]** 指示に従って次の操作を行います [請求書の作成](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Product] | 製品名、SKU、オプション（該当する場合）。 |
| [!UICONTROL Item Status] | 項目のステータスを示します。 値： `Ordered` |
| [!UICONTROL Original Price] | 割引前の品目の元のカタログ価格。 |
| [!UICONTROL Price] | 商品の購入価格。 この値は、共有カタログから品目に適用された割引を反映します（該当する場合）。 |
| [!UICONTROL Qty] | 注文された数量。 |
| [!UICONTROL Subtotal] | 小計は、購買価格に数量を乗算したものです。 |
| [!UICONTROL Tax Amount] | 小数値として品目に適用される税の金額。 |
| [!UICONTROL Tax Percent] | この品目に適用される税の割合（パーセント）。 |
| [!UICONTROL Discount Amount] | この品目に適用される割引。 注文が見積りに基づいている場合、割引値はゼロになります。 |
| [!UICONTROL Row Total] | 品目の合計（商品レベルで支払い期限が切れる適用税を含み、割引を差し引いた額）。 |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Status] | 受注のステータスが表示されます。 |
| [!UICONTROL Comment] | 注文に付随する顧客にコメントを入力するために使用されるテキストボックス。 <br/>**[!UICONTROL Notify Customer by Email]**- コメントを別のメールとして顧客に送信する場合は、このチェックボックスをオンにします。<br/>**[!UICONTROL Visible on Storefront]** - コメントを顧客のアカウントから表示する場合は、チェックボックスをオンにします。 <br/>**[!UICONTROL Submit Comment]**- コメントを送信し、メールで送信します（該当する場合）。 |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Shipping & Handling] | 配送料および手数料に対して請求される金額。 |
| [!UICONTROL Tax] | 注文に適用される税額（該当する場合）。 |
| [!UICONTROL Grand Total] | 注文の合計。 |
| [!UICONTROL Total Paid] | 注文に対して支払われた合計金額（該当する場合）。 |
| [!UICONTROL Total Refunded] | 注文から返金された合計金額（該当する場合）。 |
| [!UICONTROL Total Due] | 期限の合計金額。 |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）注文に適用される利用可能なストアクレジットの金額（該当する場合）。 |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能）見積もりの基礎として使用される共通カタログまたは標準カタログの価格に従って、見積もりの品目の合計価格（税抜）。 ストアフロントの表示通貨が基本通貨と異なる場合、値は両方の通貨で表示され、ストアフロントは角括弧で囲まれて表示されます。 |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で利用可能）買い手と売り手の間で交渉された見積もりの結果である割引。 ストアフロントの表示通貨が基本通貨と異なる場合、値は両方の通貨で表示され、ストアフロントは角括弧で囲まれて表示されます。 |
| [!UICONTROL Subtotal] | ![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能） カタログの合計価格から交渉済みの割引を差し引いた値。 |

{style="table-layout:auto"}

## 注文処理デモ

このビデオでは、注文の処理とステータスについて詳しく説明します。

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12)
