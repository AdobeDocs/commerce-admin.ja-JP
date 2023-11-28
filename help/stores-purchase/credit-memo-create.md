---
title: クレジットメモの発行
description: 請求済み注文のクレジットメモを生成して印刷する方法を説明します。
exl-id: 84ec72ba-7f72-4fa1-a9bf-91c17f43a3a7
feature: Orders, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2157'
ht-degree: 0%

---

# クレジットメモの発行

クレジットメモを印刷する前に、まず [請求済み注文](invoices.md#create-an-invoice). 支払い方法に応じて、オープン・クレジット・メモからオンラインとオフラインの両方の払い戻し（一部または全部）を発行できます。

- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 返金は、店舗クレジットに適用できます。
- ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceで利用可能 ) 返金は、会社のクレジットに適用できます。
- クレジットカードで行われた購入は、オンラインまたはオフラインで返金できます。
- 小切手または送金で行われた購入は、オフラインで返金する必要があります。

クレジットメモ [ステータスを開く](order-status.md) には未払いの払い戻し期限があります。

クレジット・メモを使用すると、次のことが可能になります。

- 請求書の全額を返金します。
- 請求書の一部金額を払い戻します。
- 請求書の複数の部分金額を払い戻します。
- 注文ごとに複数の請求書を払い戻し、合計注文額を超えないようにします。
- 5 枚のシャツのうち 3 枚など、1 行の項目の数量の一部を注文で返金します。

詳しくは、 [請求書の作成](invoices.md#create-an-invoice) を参照してください。

## 支払アクション設定

クレジットカードで支払われる注文の払い戻しワークフローは、 [支払いアクション設定](../configuration-reference/sales/payment-methods.md#payment-actions) を設定します。 払い戻しは、トランザクションが決済されるまで発行できません。

![支払いアクション設定](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- 設定した支払方法の支払処理が次のように設定されている場合 `Authorize`の場合、クレジットメモを作成する前に、まず管理者から請求書を生成する必要があります。
- 設定した支払方法の支払処理が次のように設定されている場合 `Authorize and Capture`の場合、請求書は支払処理者によって既に生成されていますが、資金は取引が決済されるまで使用できません。 この短い待ち時間は、多くの支払いプロセッサーがセキュリティ対策として推奨し、通常は自動的に処理できます。 トランザクションは、お客様のマーチャントアカウントから支払処理者と手動で決済することもできます。
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) ギフトオプションを含む注文のクレジットメモを作成すると、ギフト用ラッピングや印刷されたカードの払い戻しがクレジットメモの「返金合計」セクションに表示されます。 返金する金額からこれらの原価を除外するには、金額を「調整手数料」に入力します。 同じ注文に対して複数のクレジット・メモが発行された場合、ギフト・オプションの払い戻しは最初のクレジット・メモにのみ表示されます。

## クレジットメモの作成

払い戻しのタイプを決定します。 [信用購入](#issue-a-refund-for-a-credit-purchase) または [小切手または通貨注文](#issue-an-offline-refund-for-check-or-money-order) — クレジットメモを生成し、払い戻しを発行します。

### クレジット購入の返金を行う

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![注文グリッド](./assets/orders-grid.png){width="700" zoomable="yes"}

1. グリッド内の順序を探し、 **[!UICONTROL View]**.

1. 次の場合、 _[!UICONTROL Credit Memo]_ボタンがボタンバーに表示されるので、次のいずれかの操作を行います。

   - を発行するには、 `offline` 払い戻し、ステップ#6に移動します。
   - を発行するには、 `online` 払い戻し、ステップ#4で続行します。

   詳しくは、 [クレジットメモ](credit-memos.md) オフラインおよびオンラインでの返金の詳細については、を参照してください。

1. クリック **[!UICONTROL Invoices]** をクリックします。

1. グリッドで請求書を検索し、 **[!UICONTROL View]**.

   ![請求書グリッド](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. 下にスクロールして、 **[!UICONTROL Invoice Totals]** 請求書のセクションで、請求書が `Capture Online`をクリックし、 **[!UICONTROL Submit Invoice]**.

   ![オンラインキャプチャ](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   このオプションが使用できない場合は、請求書が既に作成されています。 次の手順に進みます。

1. 請求書上部のボタンバーで、 **[!UICONTROL Credit Memo]**.

1. 次のページで情報を確認します。 **[!UICONTROL Items to Refund]** 」セクションに移動し、必要に応じて次の操作を行います。

   - 製品を在庫に戻すには、 **[!UICONTROL Return to Stock]** チェックボックス。

     次の場合、製品は自動的に在庫に戻ります。 _製品在庫オプション_ が `Automatically Return Credit Memo Item to Stock`. を使用 [Inventory management有効](../inventory-management/enable.md)の場合、品目は出荷を送信したソースに戻ります。

   - を更新します。 **[!UICONTROL Qty to Refund]**&#x200B;をクリックし、 **[!UICONTROL Update Qty's]**.

     ![払い戻す項目](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. を更新します。 **[!UICONTROL Refunds Totals]** 節の内容は次のとおりです。

   - の場合 **[!UICONTROL Refund Shipping]**、送料から返金される金額を入力します。

     このフィールドには、最初に、返金に使用できる注文からの合計送料が表示されます。 これは、注文からの完全な送料と同じで、既に払い戻された送料の額を減らします。 量と同様に、量は減らすことができますが、増加することはできません。

   - の場合 **[!UICONTROL Adjustment Refund]**」に値を入力すると、払い戻された合計金額に追加され、注文の特定の部分（発送、品目または税金）に適用されない追加の払い戻しとして追加されます。 また、管理者が最初に非仮想支払い方法を返金したい場合、ギフトカードなどの仮想マネーによる部分的な返金にも使用できます。

     入力した金額は、合計払い戻し額を支払額より高くすることはできません。

   - の場合 **[!UICONTROL Adjustment Fee]**」に、払い戻された合計金額から減算する値を入力します。

     この金額は、出荷、品目、税金など、注文の特定のセクションから差し引かれません。

1. コメントを追加するには、 **[!UICONTROL Credit Memo Comments]** ボックス。

   - 顧客に電子メール通知を送信するには、 **[!UICONTROL Email Copy of Credit Memo]** チェックボックス。

1. クリック **[!UICONTROL Update Totals]**.

1. 必要に応じて、次の操作を実行します。

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 顧客の店舗クレジットに金額を返金するには、 **[!UICONTROL Refund to Store Credit]** チェックボックス。

   - ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 顧客の会社クレジットに金額を払い戻すには、 **[!UICONTROL Refund to Company Credit]** チェックボックス。

   - オフラインで払い戻しを発行するには、 **[!UICONTROL Refund Offline]**.

   - オンラインで払い戻しを行うには、 **[!UICONTROL Refund]**.

   - ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 購入が会社クレジットで支払われた場合、 **[!UICONTROL Refund to Company Credit]**.

   詳しくは、 [クレジットメモ](credit-memos.md) オフラインおよびオンラインでの返金の詳細については、を参照してください。

   ![注文の合計払い戻し](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### 小切手または送金のオフライン払い戻しを発行

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッドで完了したオーダーを見つけ、 **[!UICONTROL View]** リンク。

1. ページ上部のボタンバーで、 **[!UICONTROL Invoice]**.

1. ページの下部まで下にスクロールし、をクリックします。 **[!UICONTROL Submit Invoice]**.

1. 請求書上部のボタンバーで、 **[!UICONTROL Credit Memo]**.

   ![クレジットメモの作成](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. 次のページで情報を確認します。 **[!UICONTROL Items to Refund]** 」セクションに移動し、必要に応じて次の操作を行います。

   ![払い戻す項目](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Return to Stock]** チェックボックスをオンにします。

     Inventory managementが有効な場合、在庫数量は出荷を送信したソースに戻ります。 次の場合、製品は自動的に在庫に戻ります。 [製品在庫オプション](../inventory-management/enable.md) が `Automatically Return Credit Memo Item to Stock`.

   - を更新します。 **[!UICONTROL Qty to Refund]** をクリックします。 **[!UICONTROL Update Qty's]**.

     繰り入れる金額は、払い戻しに使用できる最大金額を超えてはなりません。

1. を更新します。 **[!UICONTROL Refunds Totals]** 該当するセクション：

   - の場合 **[!UICONTROL Refund Shipping]**、送料から返金される金額を入力します。

     このフィールドには、返金に使用できる注文の合計送料が最初に表示されます。 これは、注文からの完全な送料と同じで、既に払い戻された送料の額を減らします。 量と同様に、量は減らすことができますが、増加することはできません。

   - の場合 **[!UICONTROL Adjustment Refund]**」に値を入力すると、払い戻された合計金額に追加され、注文の特定の部分（発送、品目または税金）に適用されない追加の払い戻しとして追加されます。 また、管理者が最初に非仮想支払い方法を返金したい場合、ギフトカードなどの仮想マネーによる部分的な返金にも使用できます。

     入力した金額は、合計払い戻し額を支払額より高くすることはできません。

   - の場合 **[!UICONTROL Adjustment Fee]**」に、払い戻された合計金額から減算する値を入力します。

     この金額は、出荷、品目、税金など、注文の特定のセクションから差し引かれません。

   - 購入が店舗クレジットで支払われた場合、 **[!UICONTROL Refund to Store Credit]** 「 」チェックボックスをオンにして、金額を顧客勘定残高に計上します。

1. コメントを追加するには、 **[!UICONTROL Credit Memo Comments]** 」ボックスに移動して、以下の操作を実行します。

   - 顧客に電子メール通知を送信するには、 **[!UICONTROL Email Copy of Credit Memo]** チェックボックス。

   - 電子メールに入力したコメントを含めるには、 **[!UICONTROL Append Comments]** チェックボックス。

     クレジット・メモ通知のステータスは、クレジット・メモ番号の横にある完了済のクレジット・メモに表示されます。

     ![払い戻し合計](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. 処理を完了して払い戻しを発行するには、 **[!UICONTROL Refund Offline]**.

## フィールドの説明

### [!UICONTROL Order & Account Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Order Number] | 注文番号が _注文およびアカウント情報_&#x200B;に続いて、確認 E メールが送信されたかどうかを示すメモが表示されます。 |
| [!UICONTROL Order Date] | 注文が行われた日時。 |
| [!UICONTROL Order Status] | 注文ステータスを次のように示します `Complete`. |
| [!UICONTROL Purchased From] | 注文がおこなわれた Web サイト、ストア、ストアの表示を示します。 |
| [!UICONTROL Placed from IP] | 注文元のコンピューターの IP アドレスを示します。 |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Customer Name] | 注文を行った顧客または購入者の名前。 顧客名は、顧客プロファイルにリンクされます。 |
| [!UICONTROL Email] | 顧客または購入者の電子メールアドレス。 新しい電子メールメッセージを開くための電子メールアドレスがリンクされています。 |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループまたは共有カタログの名前。 |
| [!UICONTROL Company Name] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 購入者に関連付けられた会社の名前で、その会社に代わって注文がおこなわれます。 会社名は会社プロファイルにリンクされます。 |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Billing Address] | 注文をした顧客または購入者の名前。その後に請求先住所、電話番号、 [VAT](vat.md)（該当する場合） 電話番号は、モバイルデバイス上のオートダイヤルにリンクされます。 |
| [!UICONTROL Shipping Address] | 注文を発送する人物の名前。その後に発送先住所と電話番号が続きます。 電話番号は、モバイルデバイス上のオートダイヤルにリンクされます。 |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Payment Information] | 注文に使用する支払い方法と、該当する場合は発注番号、その後に注文の発行に使用された通貨が続きます。 注文が次を使用して会社のクレジットに請求される場合 [アカウントでの支払い](../b2b/enable-basic-features.md#configure-payment-on-account)の場合、アカウントに請求された金額が表示されます。 |
| [!UICONTROL Shipping & Handling Information] | 使用する発送方法、および適用される手数料。 |

{style="table-layout:auto"}

### [!UICONTROL Items to Refund]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Product] | 製品名、SKU、およびオプション（該当する場合）。 |
| [!UICONTROL Price] | 品目の購入価格。 Adobe Commerceの B2B の場合、この値は、該当する場合は、共有カタログの品目に適用された割引を反映します。 |
| [!UICONTROL Qty] | 注文された数量。 |
| [!UICONTROL Return to Stock] | 返品された品目を在庫に返品するかどうかを示すチェックボックス。 |
| [!UICONTROL Qty to Refund] | 製品から返される数量を示します。 |
| [!UICONTROL Subtotal] | 小計は、返された製品の数量を掛けた購入価格です。 |
| [!UICONTROL Tax Amount] | 小数値で返される品目に適用される税額。 |
| [!UICONTROL Tax Percent] | 返品品目に適用される税の割合（パーセンテージ）。 |
| [!UICONTROL Discount Amount] | 返された項目に適用される割引。 |
| [!UICONTROL Row Total] | 返品された製品レベルに対して支払われる適用税を含む、行項目の合計。割引が少なくなります。 |
| _注文合計_ |  |

{style="table-layout:auto"}

### [!UICONTROL Credit Memo Comments]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Comment Text] | クレジットメモに関するコメントを顧客に入力するために使用するテキストボックスです。 |

{style="table-layout:auto"}

### [!UICONTROL Refund Totals]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Refund Shipping] | 払い戻す送料。 |
| [!UICONTROL Adjustment Refund] | 送料、品目、税など、注文の特定の部分に適用されない追加の払い戻しとして返済された合計金額に加算された金額。 入力した金額は、合計払い戻し額を支払った金額より高くすることはできません。 |
| [!UICONTROL Adjustment Fee] | 返品済みの合計金額から差し引かれる金額（返品手数料、ギフト用ラッピングやギフトオプションに関連する金額など）。 |
| [!UICONTROL Grand Total] | 払い戻しの総額 |
| [!UICONTROL Append Comments] | コメントをクレジットメモに含めるかどうかを指定するチェックボックスです。 |
| [!UICONTROL Email Copy of Credit Memo] | クレジットメモのコピーを電子メールで送信するかどうかを指定するチェックボックス。 |
| [!UICONTROL Refund to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 合計をに返金するかどうかを指定するチェックボックス [店舗クレジット](../customers/store-credit-using.md). |
| [!UICONTROL Subtotal] | ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceに利用可能 ) 返金されるすべての行項目の合計。 |

{style="table-layout:auto"}

### 払い戻しボタン

注文に使用される支払い方法は、クレジットメモに使用できる払い戻しボタンを決定します。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Refund]** | 元の購入が支払ゲートウェイを介してクレジットカードで支払われた場合、払い戻し額は支払い処理者によって管理される。 払い戻しを管理するには、支払いプロバイダーから提供されるドキュメントを参照してください。 |
| **[!UICONTROL Refund Offline]** | 元の購入が小切手または送金で支払われた場合、返金は、お客様に直接支払われ、小切手、ギフトカード、またはレンガとモルタルの店舗がある場合は現金を発行します。 クレジットメモは、オフライントランザクションの記録として機能します。 |
| **[!UICONTROL Refund to Company Credit]** | ![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの B2B で利用可能 ) 購入が会社のクレジットに請求された場合、返金は [会社アカウント](../b2b/credit-company.md). |

{style="table-layout:auto"}

## クレジットメモの印刷

完了したクレジットメモを印刷または表示するには、PDFリーダーがインストールされている必要があります。 ダウンロード可能 [Adobe Reader][1] 無料で

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. クレジット・メモを印刷するには、次のいずれかの方法を使用します。

### 方法 1：現在のクレジット・メモの印刷

1. グリッドで、クレジットメモを開きます。

1. クリック **[!UICONTROL Print]**.

   ![クレジットメモの印刷](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### 方法 2：複数のクレジット・メモの印刷

1. リストで、印刷する各クレジット・メモのチェック・ボックスを選択します。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `PDF Credit Memos` をクリックします。 **[!UICONTROL Submit]**.

   ![選択したクレジットメモの印刷](./assets/credit-memos-print.png){width="600" zoomable="yes"}

1. プロンプトが表示されたら、次のいずれかの操作を行います。

   - ドキュメントを保存するには、 **[!UICONTROL Save]** 画面の指示に従って、ファイルをコンピュータに保存します。 ダウンロードが完了したら、Adobe ReaderでPDFを開き、ドキュメントを印刷します。

   - ドキュメントを表示するには、 **[!UICONTROL Open]**. 印刷済みのPDFクレジットメモがAdobe Readerで開きます。 ここから、クレジットメモを印刷するか、コンピュータに保存できます。


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Get Adobe Reader"
