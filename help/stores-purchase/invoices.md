---
title: 請求書
description: オーダー処理およびカスタマーサービス操作をサポートするための請求書を作成および印刷する方法を説明します。
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# 請求書

請求書は、注文の支払い記録です。 1 回の注文に対して複数の請求書を [ 作成 ](#create-an-invoice) でき、それぞれに、指定した購入製品をいくつでも含めることができます。 また、顧客向けのPDF文書として [ 印刷可能な営業請求書 ](#print-invoices) を作成することもできます。

_管理者_ サイドバーで、**[!UICONTROL Sales]**/_運営_/**請求書** に移動して _請求書_ グリッドを開き、作成した請求書にアクセスします。

![ 請求書グリッド ](./assets/invoices.png){width="700" zoomable="yes"}

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象とする引用符のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` |
| [!UICONTROL Invoice] | 管理者から請求書が送信される際に割り当てられる一意の数値 ID。 請求書の詳細を表示する場合、この番号は見積書名ではなく、ページの上部に表示されます。 |
| [!UICONTROL Invoice Date] | 管理者が最初に請求書を送信した日時。 |
| [!UICONTROL Order#] | 購入者によって注文が行われるときに割り当てられる一意の数値識別子。 請求書の詳細を表示すると、この番号は注文および口座情報ブロックにリンクとして表示されます。 |
| [!UICONTROL Order Date] | 顧客が最初に正常に注文した日時。 |
| [!UICONTROL Bill-to Name] | 注文の支払いを担当する人物の名前。 |
| [!UICONTROL Status] | 請求書の現在の状態を示します。 ステータスは、買い手または売り手の一部の行動によってのみ変更できます。 |
| [!UICONTROL Grand Total (Base)] | 購入する製品の合計価格。 合計金額は、web サイトの基本通貨とストアフロントの通貨で表示されます。 |
| [!UICONTROL Grand Total (purchase)] | 注文で購入した製品の合計金額。 合計金額は、web サイトの基本通貨とストアフロントの通貨で表示されます。 |
| [!UICONTROL Purchased From] | 請求書が作成された web サイト /店舗/店舗表示。 |
| [!UICONTROL Billing Address] | 注文を行った顧客の請求先住所。 |
| [!UICONTROL Shipping Address] | 注文を発送する住所。 |
| [!UICONTROL Customer Name] | 請求書を受け取る顧客の氏名。 |
| [!UICONTROL Email] | 請求書を受け取る顧客の E メール アドレス。 |
| [!UICONTROL Customer Group] | 請求書を受け取る顧客に割り当てられた顧客グループ。 |
| [!UICONTROL Payment Method] | 支払に使用される支払方法。 |
| [!UICONTROL Shipping Information] | 注文を発送するために使用される方法。 |
| [!UICONTROL Subtotal] | 出荷および処理を伴わない注文の小計および税金。 |
| [!UICONTROL Shipping and Handling] | 出荷および処理に対して請求される金額。 |
| [!UICONTROL Action] | **[!UICONTROL View]** – 請求書を編集モードで開きます。 |

{style="table-layout:auto"}

## 請求書の作成

オーダーに対して請求書を作成すると、取消や変更ができない状態に移行します。 新しい請求書ページは、いくつかのフィールドが追加された、完了済みの注文に似ています。 注文に関連するすべてのアクティビティは、請求書の「コメント」セクションに記載されています。

通常、注文は出荷処理が開始されると請求され、取得されます。 支払い方法が発注書の場合、または [ 支払いアクション ](../configuration-reference/sales/payment-methods.md#payment-actions) が `Authorize and Capture` に設定されている場合、注文は請求され、支払いはチェックアウト時にキャプチャされます。 梱包明細を含む請求書を生成したり、配送業者アカウントから出荷ラベルを印刷することもできます。 必要に応じて、1 つの注文を部分出荷に分割し、個別に請求することができます。

新しい注文の状態が `Processing` に設定されると、設定で _すべての項目を自動的に請求_ オプションが使用できるようになります。 一部のクレジット カード支払方法では、[ 支払処理 ](../configuration-reference/sales/payment-methods.md#payment-actions) が `Authorize and Capture` に設定されている場合に、プロセスの一部として請求ステップが完了します。 このような場合、「請求書」ボタンは表示されず、注文の出荷準備が整います。

>[!NOTE]
>
>`Gift Card`、`Store Credit`、`Reward Points` またはその他のオフライン支払い方法を使用して注文された場合、請求書は自動的には作成されません。

注文の請求書は、印刷する前に生成する必要があります。 PDFを表示または印刷するには、最初にPDFリーダー（[Adobe Acrobat Reader][1] など）をダウンロードしてインストールします。

**_注文をインボイス化するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/_[!UICONTROL Operations]_/**[!UICONTROL Orders]**に移動します。

1. ステータスが「`Processing`」の受注をグリッドで検索します。 次に、以下の手順を実行します。

1. _アクション_ 列の「**[!UICONTROL View]**」をクリックします。

1. 受注のヘッダーで、「**[!UICONTROL Invoice]**」オプションを選択します。

   >[!NOTE]
   >
   >特定の [ 支払方法 ](../configuration-reference/sales/payment-methods.md#payment-actions) の [ 支払アクション ](../configuration-reference/sales/payment-methods.md) が `Authorize and Capture` に設定され、請求書が自動生成される場合、_[!UICONTROL Invoice]_オプションは表示されません。 これは、注文が行われ、支払い方法の支払いアクションが `Authorize` に設定され、注文が請求された場合にも当てはまります。

   ![ 請求書受注 ](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   新しい請求書ページは完了済み注文ページに似ていますが、編集可能なフィールドが追加されています。

1. 品目の出荷準備が完了している場合は、請求書の作成と同時に出荷の梱包明細を生成します。

   - 「_発送先情報_」セクションで、「**[!UICONTROL Create Shipment]**」チェックボックスをクリックして選択します。

     出荷レコードは、請求書の生成時に作成されます。

   - 追跡番号を含める：

      - 「**[!UICONTROL Add Tracking Number]**」をクリックします。
      - トラッキング情報（_[!UICONTROL Carrier]_、_[!UICONTROL Title]_、_[!UICONTROL Number]_）を入力します

     ![Fedex 出荷の作成 ](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - 必要に応じて、部分請求書を生成します。

      - 「_請求書への品目_」セクションで、「**[!UICONTROL Qty to Invoice]**」列を更新して請求書の特定の品目のみを含めます。
      - 次に、「**[!UICONTROL Update Qty's]**」をクリックします。

        ![ 請求項目 ](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. 注文にオンライン支払い方法を使用した場合は、適切なオプションに **[!UICONTROL Amount]** を設定します。

1. 請求書が生成されたときに E メールで顧客に通知するには、次の手順を実行します。

   - 「**[!UICONTROL Email Copy of Invoice]**」チェックボックスをオンにします。

   - 任意の **[!UICONTROL Invoice Comments]** を入力します。 通知メールにコメントを含めるには、「**[!UICONTROL Append Comments]**」チェックボックスをオンにします。

1. 完了したら、ページ下部の「**[!UICONTROL Submit Invoice]**」をクリックします。

   **_オンライン支払い方法：_**

   ![ 請求書の発行 – オンライン支払方法 ](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_オフライン支払方法：_**

   ![ 請求書の発行 – オフライン支払方法） ](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   注文のステータスが「`Pending`」から「`Complete`」に変わります。

   ![ 完了済みの請求概要 ](./assets/invoice-complete.png){width="600" zoomable="yes"}

## 請求書の印刷

請求書は、個別に印刷することも、バッチとして印刷することもできます。 ただし、請求書を印刷する前に、最初に注文に対して請求書を生成する必要があります。 印刷可能なPDF請求書の高解像度ロゴをアップロードし、ヘッダーに [ 注文 ID](../stores-purchase/sales-documents.md#add-reference-ids) を含めることができます。 ロゴおよび住所を使用して請求書テンプレートをカスタマイズするには、[PDFのロゴ要件 ](../stores-purchase/sales-documents.md#image-formats) を参照してください。

>[!NOTE]
>
>PDFを表示または印刷するには、PDF リーダーが必要です。 ][1]0}Adobe Reader} は無料でダウンロードできます。[

### 単一の請求書を印刷する

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/_[!UICONTROL Operations]_/**[!UICONTROL Invoices]**に移動します。

1. _[!UICONTROL Invoices]_グリッドで請求書を見つけ、_ Action _列の&#x200B;**[!UICONTROL View]**をクリックします。

1. 請求書の上部にある [**[!UICONTROL Print]**] をクリックして、請求書のPDFを作成します。

1. 生成したPDFをファイルに保存するか、印刷します。

### 複数の請求書の印刷

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/_[!UICONTROL Operations]_/**[!UICONTROL Invoices]**に移動します。

1. _[!UICONTROL Invoices]_グリッドで、印刷する各請求書のチェックボックスを選択します。

1. **[!UICONTROL Actions]** コントロールを `PDF Invoices` に設定します。

   ![ 複数請求書の印刷 ](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

請求書は、プリンタに送ったり保存したりできる 1 つのPDFファイルに保存されます。

## リソースのトラブルシューティング

請求書の問題のトラブルシューティングについて詳しくは、_Commerce サポートナレッジベース_ を参照してください。

- [ バンドル製品のバーチャルおよびシンプルな請求書は発行できません ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html)
- [ 店舗クレジット情報のない請求書 ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [100% 割引の税金が請求書に表示される ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [ 注文請求書は自動送信されません ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Readerの取得"
