---
title: '[!UICONTROL Sales] メニュー'
description: コマース管理者には、 [!UICONTROL Sales] メニュー：ワークフロー内の場所に従って注文を処理するためのツールにアクセスできます。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# [!UICONTROL Sales] メニュー

[ 販売 ] メニューには、注文ワークフロー内の場所に応じてトランザクションが一覧表示されます。 各オプションは、注文の全期間で異なるステージと考えることができます。

![セールスメニュー](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## 次を表示： [!UICONTROL Sales] メニュー

次の日： _管理者_ サイドバー、クリック **[!UICONTROL Sales]**.

## メニューオプション

### [!UICONTROL Quotes]

![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceに対応 )

許可された購入者は、 [価格を交渉する](../b2b/quotes.md) 売り手と一緒に、 [リクエスト](../b2b/quote-request.md) 買い物かごから。

### [!UICONTROL Orders]

When in an [注文](orders.md) が配置された場合、販売注文はトランザクションの一時レコードとして作成されます。 支払いが処理されておらず、注文はキャンセルできます。

### [!UICONTROL Invoices]

An [請求書](invoices.md) は、注文の支払いの受領を記録したものです。 1 回の注文に対して複数の請求書を作成できます。各請求書には、指定した数の購入製品を含めることも、少数の購入製品に対して複数の請求書を作成することもできます。 支払い処理に応じて、請求書の生成時に支払いが自動的に取り込まれます。

### [!UICONTROL Shipments]

A [出荷](shipments.md) は、出荷された注文の製品の記録です。 請求書と同様に、注文内のすべての製品が出荷されるまで、複数の出荷を 1 つの注文に関連付けることができます。

### [!UICONTROL Credit Memos]

A [クレジットメモ](credit-memos.md) は、全額または一部払い戻しに対して顧客が支払うべき金額を示す文書です。 金額は、購入に対して適用したり、顧客に返金したりできます。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )

A [返品された商品認証](returns.md) (RMA) は、交換用または返金用の品目の返品を要求する顧客に付与できます。 RMA は、Simple、Grouped、Configurable、および Bundle の各製品タイプに対して発行できます。 ただし、仮想製品やダウンロード可能な製品、ギフトカードには RMA を使用できません。

### [!UICONTROL Billing Agreements]

A [請求契約](paypal-billing-agreements.md) は、1 回の購入に限定されない点を除いて、発注と似ています。 チェックアウト時に、顧客は支払い方法として「請求契約」を選択します。 請求契約により、顧客は購入ごとに支払い情報を入力する必要がないので、チェックアウトプロセスが合理化されます。

### [!UICONTROL Transactions]

The [トランザクション](transactions.md) ページには、お客様の店舗とすべての支払いシステムの間で行われたすべての支払いアクティビティが一覧表示され、より詳細な情報へのアクセスが提供されます。

### [!UICONTROL Braintree Virtual Terminal]

管理者ユーザーは、[Braintreeの仮想端末 ] ページで、選択した金額の支払いを受け入れることができます。 ターミナル機能を利用可能にするには、マーチャントは基本を設定する必要があります [Braintree設定](braintree.md). Braintreeは、詐欺検出と PayPal 統合により、完全にカスタマイズ可能なチェックアウトエクスペリエンスを提供します。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ )

（アーカイブオプションを有効にする必要があります） [注文のアーカイブ](order-archive.md) その他のセールス・ドキュメントにより、パフォーマンスが定期的に向上し、ワークスペースに不要な情報がなくなります。
