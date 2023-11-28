---
title: クレジットメモ
description: クレジットメモと、それらが部分的または完全な返金を発行するためにどのように使用されているかについて説明します。
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# クレジットメモ

A _クレジットメモ_ は、全額または一部払い戻しに対して顧客が支払うべき金額を示す文書です。 金額は、購入に対して適用したり、顧客に返金したりできます。 1 つの注文に対するクレジット・メモを印刷することも、複数の注文に対するクレジット・メモをバッチとして印刷することもできます。 クレジットメモを印刷する前に、注文用に最初に生成する必要があります。 The _クレジットメモ_ ページには、顧客に発行されたクレジットメモの一覧が表示されます。

![クレジットメモ](./assets/credit-memos.png){width="700" zoomable="yes"}

## 払い戻し方法

The [支払方法](payments.md) 注文によって、ある程度、注文を返金する方法が決まる場合。

次の 3 つの方法で注文を返金できます。

- 勘定科目クレジット — 与信勘定科目を使用して支払われた受注は、勘定科目クレジットとして払い戻すことができます。
   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) [店舗クレジット](../customers/store-credit-using.md)
   - ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceに対応 ) [アカウントでの支払い](../b2b/enable-basic-features.md#configure-payment-on-account) （offline メソッド）
   - ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceに対応 ) [会社クレジット](../b2b/credit-company.md)
- [オンライン返金](payments.md#online-payment-methods)- PayPal やBraintreeなどの支払いゲートウェイを通じてクレジットカードで支払われた注文は、支払いプロセッサを通じてオンラインで返金されます。
- [オフライン払い戻し](payments.md#offline-payment-methods) — 現金払いで支払われる注文 ([COD](cash-on-delivery.md)) または ( [小切手または通貨注文](check-money-order.md) オフラインで払い戻されます。

任意の支払い方法に対して、オフラインの返金またはアカウントクレジット（有効な場合）を発行できます。

現金払い ([COD](cash-on-delivery.md)) または ( [小切手または通貨注文](check-money-order.md) はオフラインで払い戻されます。

## 払い戻しワークフロー

1. **支払いアクション** - [支払いアクション](credit-memo-create.md#payment-action-setting) 設定が `Authorize`を使用する場合は、クレジットメモを作成する前に請求書を生成する必要があります。手順 2 に進みます。 に設定した場合、 `Authorize and Capture`、請求書は既に生成されています。手順 3 に進みます。

1. **請求書の生成** - [請求書の作成](invoices.md#create-an-invoice) ご注文の場合は、クレジットメモを使用して顧客に返金を送信できます。

1. **クレジットメモの作成** - [クレジットメモの発行](credit-memo-create.md) ( [信用購入](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)、または [小切手または通貨注文](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となるクレジット・メモ項目のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション： `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | クレジットメモの要求が送信された際に割り当てられる一意の数値識別子。 |
| [!UICONTROL Created] | 購入者が最初にクレジットメモの要求を送信した日時。 |
| [!UICONTROL Order#] | 製品が返される注文の注文 ID。 |
| [!UICONTROL Order Date] | 購入者が注文をした日時。 |
| [!UICONTROL Bill-to Name] | 注文の支払いを担当する人の名前。 |
| [!UICONTROL Status] | クレジットメモ要求の現在の状態を示します。 |
| [!UICONTROL Refunded] | 注文から返金された合計金額。 |
| [!UICONTROL Actions] | **[!UICONTROL View]**  — クレジット・メモの要求をオープンし、バイヤーとセラーの間の交渉記録を維持します。 |
| [!UICONTROL Order Status] | 注文のステータスを示します。 |
| [!UICONTROL Purchased From] | 注文がおこなわれた Web サイト、ストア、ストアの表示を示します。 |
| [!UICONTROL Billing Address] | 注文をした顧客の請求先住所。 |
| [!UICONTROL Shipping Address] | 注文が発送される住所。 |
| [!UICONTROL Customer Name] | 注文をした顧客の氏名。 |
| [!UICONTROL Email] | 注文をした人の電子メールアドレス。 |
| [!UICONTROL Customer Group] | 顧客を割り当てる顧客グループ。 |
| [!UICONTROL Payment Method] | 支払いに使用する支払い方法。 |
| [!UICONTROL Shipping Information] | 注文の出荷に使用するメソッド。 |
| [!UICONTROL Subtotal] | 注文の小計、送料および処理なし、および税。 |
| [!UICONTROL Shipping & Handling] | 送料と処理に請求された金額。 |
| [!UICONTROL Adjustment Refund] | 追加の払い戻しとして返金された合計金額に加算される金額。 |
| [!UICONTROL Adjustment Fee] | 払い戻された合計金額から差し引かれる金額。 |
| [!UICONTROL Grand Total] | 注文の合計。 |

{style="table-layout:auto"}
