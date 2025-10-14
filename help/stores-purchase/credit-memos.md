---
title: クレジットメモ
description: クレジットメモと、それらを使用して部分的または完全な払い戻しを発行する方法について説明します。
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# クレジットメモ

_クレジット・メモ_ は、全額払い戻しまたは一部払い戻しのために顧客に支払われる金額を示す文書です。 金額は、購入に対して適用することも、顧客に払い戻すこともできます。 1 つの受注または複数の受注のクレジット・メモをバッチとして印刷できます。 クレジット メモを印刷する前に、まず注文に対して生成する必要があります。 「_クレジット・メモ_」ページには、顧客に発行されたクレジット・メモがリストされます。

![&#x200B; クレジットメモ &#x200B;](./assets/credit-memos.png){width="700" zoomable="yes"}

## 払い戻し方法

注文の [&#x200B; 支払い方法 &#x200B;](payments.md) は、ある程度、注文の払い戻し方法を決定します。

注文の払い戻しは、次の 3 つの方法で行うことができます。

- アカウント・クレジット – クレジット・アカウントを使用して支払われた注文は、アカウント・クレジットとして払い戻すことができます。
   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [&#x200B; ストアクレジット &#x200B;](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B で使用可能） [&#x200B; 分割払い &#x200B;](../b2b/enable-basic-features.md#configure-payment-on-account) （オフライン方式）
   - ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B で利用可能） [&#x200B; 会社クレジット &#x200B;](../b2b/credit-company.md)
- [&#x200B; オンライン払い戻し &#x200B;](payments.md#online-payment-methods) - PayPal やBraintreeなどの支払い方法を通じてクレジットカードで支払われた注文は、支払い処理業者を通じてオンラインで払い戻されます。
- [&#x200B; オフライン払い戻し &#x200B;](payments.md#offline-payment-methods) - キャッシュオンデリバリー（[COD](cash-on-delivery.md)）または [&#x200B; 小切手またはマネーオーダー &#x200B;](check-money-order.md) で支払われた注文は、オフラインで払い戻されます。

任意の支払い方法について、オフラインでの払い戻しまたはアカウントのクレジット（有効な場合）を発行できます。

代金引換払い（[COD](cash-on-delivery.md)）または [&#x200B; 小切手またはマネーオーダー &#x200B;](check-money-order.md) で支払われた注文は、オフラインで返金されます。

## 返金ワークフロー

1. **支払処理** - [&#x200B; 支払処理 &#x200B;](credit-memo-create.md#payment-action-setting) 構成が「`Authorize`」に設定されている場合、クレジット・メモを作成する前に請求書を生成する必要があります。手順 2 に進みます。 `Authorize and Capture` に設定した場合、請求書は既に生成されています。手順 3 に進みます。

1. **請求書の生成** - [&#x200B; 請求書の作成 &#x200B;](invoices.md#create-an-invoice) 注文について、クレジット・メモを使用して顧客に払戻を送信できるようにします。

1. **クレジットメモの作成** - [&#x200B; クレジット購入 &#x200B;](credit-memo-create.md) または [&#x200B; 小切手またはマネーオーダー &#x200B;](credit-memo-create.md#issue-a-refund-for-a-credit-purchase) の場合は、管理者で [&#x200B; クレジットメモを発行 &#x200B;](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order) します。

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となるクレジット・メモ項目のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | クレジット メモの要求が送信されるときに割り当てられる一意の数値識別子。 |
| [!UICONTROL Created] | 購買担当がクレジット・メモの要求を最初に発行した日時。 |
| [!UICONTROL Order#] | 商品が返される注文の注文 ID。 |
| [!UICONTROL Order Date] | 購入者が注文した日時。 |
| [!UICONTROL Bill-to Name] | 注文の支払いを担当する人物の名前。 |
| [!UICONTROL Status] | クレジット メモ要求の現在の状態を示します。 |
| [!UICONTROL Refunded] | 注文から払い戻された合計金額。 |
| [!UICONTROL Actions] | **[!UICONTROL View]** - クレジット・メモの要求をオープンし、バイヤーとセラー間のネゴシエーションの記録を保持します。 |
| [!UICONTROL Order Status] | 注文ステータスを示します。 |
| [!UICONTROL Purchased From] | 注文が行われた web サイト、ストア、ストア表示を示します。 |
| [!UICONTROL Billing Address] | 注文を行った顧客の請求先住所。 |
| [!UICONTROL Shipping Address] | 注文を発送する住所。 |
| [!UICONTROL Customer Name] | 注文を行った顧客の姓と名。 |
| [!UICONTROL Email] | 注文を行った人物のメールアドレス。 |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループ。 |
| [!UICONTROL Payment Method] | 支払に使用される支払方法。 |
| [!UICONTROL Shipping Information] | 注文を発送するために使用される方法。 |
| [!UICONTROL Subtotal] | 出荷および処理を伴わない注文の小計および税金。 |
| [!UICONTROL Shipping & Handling] | 出荷および処理に対して請求される金額。 |
| [!UICONTROL Adjustment Refund] | 追加払い戻しとして払い戻された金額の合計に加算される金額。 |
| [!UICONTROL Adjustment Fee] | 払い戻された合計金額から差し引かれる金額。 |
| [!UICONTROL Grand Total] | 注文の合計。 |

{style="table-layout:auto"}
