---
title: '[!UICONTROL Sales] メニュー'
description: Commerce管理者には [!UICONTROL Sales] メニューが含まれており、ワークフロー内の場所に応じて、注文を操作するためのツールにアクセスできます。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 621b4729e23952ddd720b4dcc49b5341baae64cc
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# [!UICONTROL Sales] メニュー

「Sales」メニューには、受注ワークフローでの位置に従って取引がリストされます。 各オプションは、注文の有効期間中は異なるステージと考えることができます。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS のみ ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

![ 販売メニュー ](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerceas a Cloud Service]

[!BADGE SaaS のみ ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

![ 販売メニュー ](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## [!UICONTROL Sales] メニューの表示

_管理者_ サイドバーで、「**[!UICONTROL Sales]**」をクリックします。

## メニューオプション

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B で使用可能）

権限のある購入者は、買い物かごから [ リクエスト ](../b2b/quotes.md) を送信することで、販売者と [ 価格の交渉 ](../b2b/quote-request.md) を行うことができます。

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B で使用可能）

再利用可能でカスタマイズ可能な [ 見積もりテンプレート ](../b2b/quote-templates-overview.md) を作成することにより、購入者と販売者が見積もりプロセスを合理化できます。

### [!UICONTROL Orders]

[ 注文 ](orders.md) が行われると、トランザクションの一時的なレコードとして受注が作成されます。 支払いが処理されておらず、注文は引き続きキャンセルできます。

### [!UICONTROL Invoices]

[ 請求書 ](invoices.md) は、注文の支払いを受け取った記録です。 1 回の注文に対して複数の請求書を作成でき、各請求書には指定した購入製品の数を指定できます。 支払い処理に応じて、請求書の生成時に支払いを自動的にキャプチャできます。

### [!UICONTROL Shipments]

[ 出荷 ](shipments.md) は、注文に含まれている、出荷済みの製品の記録です。 請求書と同様に、1 つの注文に複数の出荷を関連付けることができます。この場合、注文に含まれるすべての製品が出荷されます。

### [!UICONTROL Credit Memos]

[ クレジット・メモ ](credit-memos.md) は、全額払い戻しまたは一部払い戻しのために顧客に支払われる金額を示す文書です。 金額は、購入に対して適用することも、顧客に払い戻すこともできます。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

交換または払い戻しのために商品を返品することをリクエストするお客様には、[ 返品商品承認 ](returns.md) （RMA）を付与できます。 RMA は、シンプル、グループ化、設定可能、バンドルの各製品タイプに対して発行できます。 ただし、RMA は、仮想およびダウンロード可能な製品やギフトカードでは使用できません。

### [!UICONTROL Billing Agreements]

[!BADGE PaaS のみ ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

[ 請求契約 ](paypal-billing-agreements.md) は、1 回の購入に限定されない点を除き、発注書に似ています。 チェックアウト時に、お客様は支払い方法として請求契約を選択します。 請求契約を使用すると、顧客は購入ごとに支払い情報を入力する必要がなくなるので、チェックアウトプロセスが合理化されます。

### [!UICONTROL Transactions]

[ トランザクション ](transactions.md) ページには、店舗とすべての支払いシステムの間で発生したすべての支払いアクティビティが一覧表示され、より詳細な情報にアクセスできます。

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE PaaS のみ ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

Braintreeバーチャルターミナルページでは、管理者ユーザーは選択した金額の支払いを受け入れることができます。 ターミナル機能を利用できるようにするには、マーチャントが基本的な [Braintree設定 ](braintree.md) を設定する必要があります。 Braintreeは、不正検知と PayPal 統合により、完全にカスタマイズ可能なチェックアウトエクスペリエンスを提供します。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

（アーカイブ・オプションを有効にする必要があります） [ オーダーやその他のセールス・ドキュメントをアーカイブする ](order-archive.md) と、パフォーマンスが定期的に向上し、ワークスペースに不要な情報が含まれなくなります。
