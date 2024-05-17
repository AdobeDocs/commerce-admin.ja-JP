---
title: '[!UICONTROL Sales] メニュー'
description: Commerce管理者には次が含まれます [!UICONTROL Sales] メニュー。ワークフロー内の位置に応じて、注文を操作するためのツールにアクセスできます。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: a7c6203cf738e3fb9be887d637010ca9c155937a
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# [!UICONTROL Sales] メニュー

「Sales」メニューには、受注ワークフローでの位置に従って取引がリストされます。 各オプションは、注文の有効期間中は異なるステージと考えることができます。

![販売メニュー](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## を表示 [!UICONTROL Sales] メニュー

日 _Admin_ サイドバー、クリック **[!UICONTROL Sales]**.

## メニューオプション

### [!UICONTROL Quotes]

![Adobe Commerceの B2B](../assets/b2b.svg) （Adobe Commerceの B2B で使用可能）

権限のある購入者は、次のことができます [価格を交渉する](../b2b/quotes.md) 売主と共に [リクエスト](../b2b/quote-request.md) 買い物かごから。

### [!UICONTROL Orders]

いつ [順序](orders.md) が配置され、トランザクションの一時レコードとして受注が作成されます。 支払いが処理されておらず、注文は引き続きキャンセルできます。

### [!UICONTROL Invoices]

An [請求書](invoices.md) 注文に対する支払いの受領を記録したものです。 1 回の注文に対して複数の請求書を作成でき、各請求書には指定した購入製品の数を指定できます。 支払い処理に応じて、請求書の生成時に支払いを自動的にキャプチャできます。

### [!UICONTROL Shipments]

A [出荷](shipments.md) は、注文された製品の出荷済みレコードです。 請求書と同様に、1 つの注文に複数の出荷を関連付けることができます。この場合、注文に含まれるすべての製品が出荷されます。

### [!UICONTROL Credit Memos]

A [クレジット メモ](credit-memos.md) は、全額払い戻しまたは一部払い戻しのために顧客に支払われる金額を示すドキュメントです。 金額は、購入に対して適用することも、顧客に払い戻すこともできます。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

A [返品された商品承認](returns.md) （RMA）は、交換または払い戻しのために商品の返品をリクエストするお客様に付与できます。 RMA は、シンプル、グループ化、設定可能、バンドルの各製品タイプに対して発行できます。 ただし、RMA は、仮想およびダウンロード可能な製品やギフトカードでは使用できません。

### [!UICONTROL Billing Agreements]

A [請求契約](paypal-billing-agreements.md) は、1 回の購入に限定されない点を除き、発注書と似ています。 チェックアウト時に、お客様は支払い方法として請求契約を選択します。 請求契約を使用すると、顧客は購入ごとに支払い情報を入力する必要がなくなるので、チェックアウトプロセスが合理化されます。

### [!UICONTROL Transactions]

この [トランザクション](transactions.md) ページには、ストアとすべての支払いシステムの間で発生したすべての支払いアクティビティが一覧表示され、より詳細な情報にアクセスできます。

### [!UICONTROL Braintree Virtual Terminal]

Braintreeバーチャルターミナルページでは、管理者ユーザーは選択した金額の支払いを受け付けることができます。 ターミナル機能を利用可能にするには、マーチャントは基本を設定する必要があります [Braintree設定](braintree.md). Braintreeは、不正検知と PayPal 統合により、完全にカスタマイズ可能なチェックアウトエクスペリエンスを提供します。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

（アーカイブオプションを有効にする必要があります） [注文のアーカイブ](order-archive.md) また、その他の販売文書を使用すると、パフォーマンスが定期的に向上し、ワークスペースに不要な情報が含まれなくなります。
