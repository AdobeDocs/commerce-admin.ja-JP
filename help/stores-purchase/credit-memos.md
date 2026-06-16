---
title: クレジットメモ
description: クレジットメモと、部分的または全額払い戻しを発行するために使用される方法について説明します。
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
TQID: https://experienceleague.adobe.com/-G3nrlvCcdrsFJFxGWKZB7j3LsmhBTzNdncuNzsFuE4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 583
ht-degree: 0%

---

# クレジットメモ

_クレジットメモ_&#x200B;は、全額払い戻しまたは一部払い戻しの期限を顧客に示す文書です。 金額は購入に適用されるか、顧客に返金されます。 1回の注文または複数の注文のクレジットメモをバッチとして印刷できます。 クレジットメモを印刷する前に、最初に注文のために生成する必要があります。 _クレジットメモ_ ページには、顧客に発行されたクレジットメモが一覧表示されます。

![ クレジットメモ ](./assets/credit-memos.png){width="700" zoomable="yes"}

## 返金方法

注文の[支払い方法](payments.md)は、注文を返金する方法を一定の範囲で決定します。

注文を返金するには、次の3つの方法があります。

- アカウント・クレジット：クレジット・アカウントを使用して支払われた注文は、アカウント・クレジットとして返金できます。
   - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [ ストアクレジット ](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bで利用可能） [ アカウントでのお支払い](../b2b/enable-basic-features.md#configure-payment-on-account) （オフライン方式）
   - ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bで利用可能） [会社クレジット ](../b2b/credit-company.md)
- [ オンライン払い戻し](payments.md#online-payment-methods) - PayPalやBraintreeなどの支払いゲートウェイを介してクレジットカードで支払われた注文は、決済代行会社を介してオンラインで返金されます。
- [ オフライン払い戻し](payments.md#offline-payment-methods) – 代金引換（[COD](cash-on-delivery.md)）または[小切手またはマネーオーダー](check-money-order.md)によって支払われた注文は、オフラインで返金されます。

任意の支払い方法に対して、オフラインの払い戻しまたはアカウントクレジット（有効な場合）を発行できます。

代金引換（[COD](cash-on-delivery.md)）または[小切手またはマネーオーダー](check-money-order.md)によって支払われた注文は、オフラインで返金されます。

## 返金ワークフロー

1. **支払いアクション** - [支払いアクション ](credit-memo-create.md#payment-action-setting)の設定が`Authorize`に設定されている場合は、クレジットメモを作成する前に請求書を生成する必要があります。手順2に進みます。 `Authorize and Capture`に設定されている場合は、請求書が既に生成されています。手順3に進みます。

1. **請求書を生成** - [注文の請求書](invoices.md#create-an-invoice)を作成して、クレジットメモを介してお客様に返金を送信できるようにします。

1. **クレジットメモを作成** - [管理画面で[ クレジット購入](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)または[小切手またはマネーオーダー](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order)のクレジットメモ ](credit-memo-create.md)を発行します。

## 列の説明

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Select] | アクションの対象となるクレジットメモ項目のチェックボックスを選択するか、列ヘッダーの選択コントロールを使用します。 オプション：`Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | クレジットメモのリクエストが送信されたときに割り当てられる一意の数値識別子。 |
| [!UICONTROL Created] | 購入者が最初にクレジットメモのリクエストを送信した日時。 |
| [!UICONTROL Order#] | 商品が返品される注文の注文ID。 |
| [!UICONTROL Order Date] | 購入者が注文した日時。 |
| [!UICONTROL Bill-to Name] | 注文の支払いの責任を負う人の名前。 |
| [!UICONTROL Status] | クレジットメモ要求の現在の状態を示します。 |
| [!UICONTROL Refunded] | 注文から返金された合計金額。 |
| [!UICONTROL Actions] | **[!UICONTROL View]** - クレジットメモのリクエストを開き、購入者と販売者の間の交渉の記録を保持します。 |
| [!UICONTROL Order Status] | 注文ステータスを示します。 |
| [!UICONTROL Purchased From] | 注文が行われたweb サイト、ストア、ストアビューを示します。 |
| [!UICONTROL Billing Address] | 注文した顧客の請求先住所。 |
| [!UICONTROL Shipping Address] | 注文が発送される住所。 |
| [!UICONTROL Customer Name] | 注文した顧客の姓と名。 |
| [!UICONTROL Email] | 注文したユーザーの電子メールアドレス。 |
| [!UICONTROL Customer Group] | 顧客が割り当てられている顧客グループ。 |
| [!UICONTROL Payment Method] | 支払いに使用する支払い方法。 |
| [!UICONTROL Shipping Information] | 注文の出荷に使用する方法。 |
| [!UICONTROL Subtotal] | 注文の小計（送料および処理料なし）、および税金。 |
| [!UICONTROL Shipping & Handling] | 送料と処理費。 |
| [!UICONTROL Adjustment Refund] | 追加払い戻しとして払い戻される合計金額に追加される金額。 |
| [!UICONTROL Adjustment Fee] | 返金された合計金額から差し引かれる金額。 |
| [!UICONTROL Grand Total] | 注文の合計。 |

{style="table-layout:auto"}
