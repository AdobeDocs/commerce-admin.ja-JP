---
title: オーダーのワークフローと処理
description: オーダーのワークフロー、各ステップで適用されるステータス、およびこのプロセスを通じてオーダーを移動する方法について説明します。
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1733'
ht-degree: 0%

---

# オーダーのワークフローと処理

顧客が注文を行うと、販売注文がトランザクションの一時レコードとして作成されます。 「注文」グリッドでは、受注のステータスは最初は「保留中」で、支払いが処理されるまでいつでもキャンセルできます。 支払が確認された後、注文を請求し、発送することができます。

**ステップ 1：発注**  — チェックアウトプロセスは、買い物客がクリックした時点で開始します **[!UICONTROL Go to Checkout]** 買い物かごのページまたは [リオーダー](reorders-allow.md) を直接顧客アカウントから削除します。

**手順 2：注文を保留中**  — 最初の受注ステータスは、 `Pending`. この状態では、支払いは処理されておらず、注文は編集またはキャンセルできます。 この状態は、支払い方法が承認モード用に設定されている場合に発生します。

**ステップ 3：支払いの受け取り**  — 注文ステータスが `Processing` 支払いを受け取ったか、承認された場合。 支払い方法によっては、トランザクションが承認または処理されたときに通知を受け取る場合があります。 この状態は、支払い方法がキャプチャまたはインテント販売モード用に設定されている場合に自動的に発生します。

**手順 4：請求書オーダー**  — 注文は、通常、支払いを受け取った後に請求されます。 支払い方法は、注文に必要な請求オプションを決定します。 請求書が生成され、送信されると、コピーが顧客に送信されます。 支払い方法が `capture` または `intent sale` 支払いアクションを使用すると、支払が承認され、取り込まれると、請求書が自動的に生成されます。

>[!NOTE]
>
>請求書は、 `Gift Card`, `Store Credit`, `Reward Points`、またはその他のオフラインの支払い方法。

**手順 5：単一出荷の予約**  — 注文ステータスが `Complete` 出荷詳細が完了すると、出荷が記帳され、出荷が設定されます。 出荷要件は、印刷された梱包明細と出荷ラベル、または _ピックアップの準備を通知_ が選択されている（ストア内配信方法）。 お客様に通知が届き、パッケージが発送されます。 追跡番号を使用する場合は、顧客のアカウントから出荷を追跡できます。

>[!NOTE]
>
>注文ステータスと支払い方法の設定オプションについて詳しくは、 [注文ステータス](order-status.md) および [支払い](payments.md).

## 注文を表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッド内の順序を検索します。

1. Adobe Analytics の _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL View]**.

1. 注文ステータスの確認：

   - A `Pending` 注文は、変更、保留、キャンセル、または請求と出荷が可能です。

   - A `Processing` 注文を大幅に編集またはキャンセルすることはできませんが、請求および配送先住所は編集できます。

   - A `Completed` 注文は並べ替え可能です。

顧客の E メールは、注文ワークフローの任意の時点で、顧客を編集することで編集できます。 注文がゲストによって行われた場合、E メールは編集できません。

オーダーを開くための左側のパネルを使用して、オーダーに関連する様々なタイプの情報にアクセスできます。

![注文を表示](./assets/order-view.png){width="700" zoomable="yes"}

## オーダーを処理

顧客が注文を行うと、販売注文がトランザクションの一時レコードとして作成されます。 販売注文のステータスは次のとおりです： `Pending` 支払いを受け取るまで。 While in `Pending` ステータス、注文は、支払いが受け取られ、請求書が生成されるまで、編集またはキャンセルできます。 簡単に考えると、オーダーが請求書になり、請求書が出荷になります。 注文グリッドには、ワークフロー内の場所に関係なく、すべての注文がリスト表示されます。 注文に関するお客様のサポート方法については、 [注文の更新](order-update.md).

![購入回数](./assets/orders-grid.png){width="700" zoomable="yes"}

を開くには `Pending` 注文、クリック **[!UICONTROL Edit]** をクリックします。

>[!NOTE]
>
>オーダーは、 `Pending` ステータス。 ステータスが異なる注文や、 [交渉済みの見積もり](../b2b/quotes.md).

![販売注文の編集](./assets/order-pending.png){width="600" zoomable="yes"}

フィールドの説明を参照して、受注の次の項を確認します。

### 注文ビューの説明

| タブ | 説明 |
|--- |--- |
| [!UICONTROL Information] | 請求および配送先住所、支払および配送方法、品目の注文、合計、メモなど、注文およびアカウントに関する詳細情報を表示します。 |
| [!UICONTROL Invoices] | 注文に関連付けられている各請求書を一覧表示します。 |
| [!UICONTROL Credit Memos] | オーダーに関連付けられた各クレジット・メモのリストが表示されます。 |
| [!UICONTROL Shipments] | 注文に関連付けられている各出荷レコードをリストします。 |
| [!UICONTROL Comments History] | 注文に関連するすべてのメモのリストを表示します。 |

{style="table-layout:auto"}

>[!NOTE]
>
>管理者ユーザーは、 **[!UICONTROL Sales / Archive]** [権限](../systems/permissions-user-roles.md) 彼らの役割の範囲が _請求書_, _クレジットメモ_、および _出荷_ 「順序」タブ。

### ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに注文ページに戻ります。 |
| **[!UICONTROL Cancel]** | 販売注文をキャンセルします。 |
| **[!UICONTROL Send Email]** | 注文に関する電子メールを顧客に送信します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 販売注文のステータスを次に変更します `On Hold`. 受注の保留を解除するには、次を選択します。 **[!UICONTROL Unhold]**. |
| **[!UICONTROL Invoice]** | 注文を請求書に変換して、販売注文から請求書を作成します。 |
| **[!UICONTROL Ship]** | 注文の出荷レコードを作成します。 |
| **[!UICONTROL Notify Order is Ready for Pickup]** | 注文が店舗配信として配置されている場合にのみ表示されます。 注文の受け取り準備ができたことを顧客に通知します。 |
| **[!UICONTROL Reorder]** | 現在の注文に基づいて販売注文を作成します。 |
| **[!UICONTROL Edit]** | 保留中のオーダーを編集モードで開きます。 ステータスが「 `Processing`、またはネゴシエートされた見積もりに基づく注文。 |

{style="table-layout:auto"}

### 注文のキャンセル

以下が可能です。 [解約](order-update.md) まだ請求されていない注文。 A [クレジットメモ](credit-memos.md) 顧客が請求後（支払いが取り込まれた後）に注文をキャンセルする場合に発行する必要があります。

注文が `Pending` または `Processing` そして、支払いがキャプチャされていないか、完全にキャプチャされていない場合は、 [命令を無効にする](#void-an-order) キャンセルする代わりに

キャンセルしたオーダーを復元するには、 **[!UICONTROL Reorder]** ボタンをクリックし、新しい順序を「 」ステータスで作成します。 `Pending`.

>[!NOTE]
>
>オーダーをキャンセルしても、ボイドが生成されますが、オーダーを無効にしても、キャンセルはトリガーされません。

### 注文を無効にする

請求されていない、ステータスが「 」の販売注文のみ `Processing`、および [支払統合設定 `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions)、 [無効](order-update.md#void-a-processing-order). 注文を無効にした後、キャンセルできます。

### [!UICONTROL Order and Account Information]

![注文およびアカウント情報](./assets/order-account-information.png){width="600" zoomable="yes"}

#### 注文情報

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Order Number] | 注文番号が販売注文の上部に表示され、確認 E メールが送信されたかどうかを示すメモが続きます。 |
| [!UICONTROL Order Date] | 注文が行われた日時。 |
| [!UICONTROL Purchased From] | 注文がおこなわれた Web サイト、ストア、ストアの表示を示します。 |
| [!UICONTROL Placed from IP] | 注文元のコンピューターの IP アドレスを示します。 |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で使用可能 ) [引用](../b2b/quotes.md) 該当する場合は、注文が生成されたソース。 見積もりの名前は見積もりにリンクされます。 |

{style="table-layout:auto"}

#### アカウント情報

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Customer Name] | 注文を行った顧客または購入者の名前。 顧客名は、顧客プロファイルにリンクされます。 |
| [!UICONTROL Email] | 顧客または購入者の電子メールアドレス。 新しい電子メールメッセージを開くための電子メールアドレスがリンクされています。 |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前。 |
| [!UICONTROL Company Name] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 購入者が関連付けられ、その代理で注文がおこなわれる会社の名前。 会社名は [会社プロファイル](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![住所情報](./assets/order-address-information.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Billing Address] | 注文をした顧客または購入者の名前。その後に請求先住所、電話番号、 [VAT](vat.md)（該当する場合） 電話番号は、モバイルデバイス上のオートダイヤルにリンクされます。 |
| [!UICONTROL Shipping Address] | 注文を発送する人物の名前。その後に発送先住所と電話番号が続きます。 電話番号は、モバイルデバイス上のオートダイヤルにリンクされます。 |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![お支払い方法と発送方法](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Payment Information] | 注文に使用する支払い方法と、該当する場合は発注番号、その後に注文の発行に使用された通貨が続きます。 注文が次を使用して会社のクレジットに請求される場合 [アカウントでの支払い](../b2b/enable-basic-features.md#configure-payment-on-account)の場合、アカウントに請求された金額が表示されます。 |
| [!UICONTROL Shipping & Handling Information] | 使用する発送方法、および適用される手数料。 |

{style="table-layout:auto"}

### 注文された項目のレビュー

![並べ替え済み項目](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Adobe Analytics の **[!UICONTROL Order Total]** セクションで、以下の操作を実行します。

1. を入力します。 **[!UICONTROL Comment]** を並べ替えます。

1. 顧客にコメントを電子メールで送信する場合は、 **[!UICONTROL Notify Customer by Email]** チェックボックス。

1. 顧客アカウントでコメントを表示する場合は、 **[!UICONTROL Visible on Storefront]** チェックボックス。

   ![注文合計](./assets/order-total.png){width="600" zoomable="yes"}

1. 注文を請求する準備が整ったら、「 **[!UICONTROL Invoice]** そして次の手順に従います。 [請求書の作成](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Product] | 製品名、SKU、および該当する場合はオプション。 |
| [!UICONTROL Item Status] | 項目のステータスを示します。 値： `Ordered` |
| [!UICONTROL Original Price] | 割引前の品目の元のカタログ価格。 |
| [!UICONTROL Price] | 品目の購入価格。 この値は、該当する場合は、共有カタログの品目に適用された割引を反映します。 |
| [!UICONTROL Qty] | 注文された数量。 |
| [!UICONTROL Subtotal] | 小計は、購入価格に数量を掛けた値です。 |
| [!UICONTROL Tax Amount] | 項目に小数値として適用される税額。 |
| [!UICONTROL Tax Percent] | この品目に割合として適用される税の割合。 |
| [!UICONTROL Discount Amount] | この項目に適用される割引。 注文が見積もりに基づく場合、割引値は 0 です。 |
| [!UICONTROL Row Total] | 製品レベルで支払われる適用税を含む、行項目の合計、割引の少ない。 |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Status] | 販売注文のステータスを表示します。 |
| [!UICONTROL Comment] | 注文に付随する顧客へのコメントを入力するために使用されるテキストボックス。 <br/>**[!UICONTROL Notify Customer by Email]**— コメントを別の E メールとして顧客に送信する場合は、このチェックボックスを選択します。<br/>**[!UICONTROL Visible on Storefront]**  — 顧客のアカウントからコメントを表示する場合は、このチェックボックスを選択します。 <br/>**[!UICONTROL Submit Comment]**— コメントを送信し、必要に応じて電子メールで送信します。 |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Shipping & Handling] | 送料と手数料に対して請求された金額。 |
| [!UICONTROL Tax] | オーダーに適用される税額（該当する場合）。 |
| [!UICONTROL Grand Total] | 注文の合計。 |
| [!UICONTROL Total Paid] | 注文に対して支払われた合計金額（該当する場合）。 |
| [!UICONTROL Total Refunded] | 必要に応じて、注文から返金された合計金額。 |
| [!UICONTROL Total Due] | 支払期限の合計金額。 |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 注文に適用される利用可能な店舗クレジットの額（該当する場合）。 |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 見積書の品目の合計価格 ( 見積書の基礎として使用される共有カタログまたは標準カタログの価格に従って、税なしで見積書に含まれる品目の合計価格。 ストアフロントの表示通貨が基本通貨と異なる場合は、値が両方の通貨で表示され、ストアフロントは角括弧で囲まれて表示されます。 |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 購入者と販売者の間で交渉された見積もりの結果である割引。 ストアフロントの表示通貨が基本通貨と異なる場合は、値が両方の通貨で表示され、ストアフロントは角括弧で囲まれて表示されます。 |
| [!UICONTROL Subtotal] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) カタログ合計価格は、交渉された割引を下回ります。 |

{style="table-layout:auto"}

## 注文処理のデモ

このビデオでは、注文の処理とステータスについて詳しくご覧いただけます。

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12)
