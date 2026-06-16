---
title: '[!UICONTROL Sales] メニュー'
description: Commerce管理者には[!UICONTROL Sales] メニューが含まれており、ワークフロー内の場所に応じて、注文を操作するためのツールにアクセスできます。
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
TQID: https://experienceleague.adobe.com/mliJ1Q1-DEkR5rAoIRLQ9qBxQopBytjicPiqzWTg7ac
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 0%

---

# [!UICONTROL Sales] メニュー

「販売」メニューには、注文ワークフローの位置に応じてトランザクションが一覧表示されます。 各オプションは、注文のライフタイムステージごとに異なると考えることができます。

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

![販売メニュー](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud ServiceおよびAdobe Commerce Optimizer プロジェクト（Adobeが管理するSaaS インフラストラクチャ）にのみ適用されます。"}

![販売メニュー](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## [!UICONTROL Sales] メニューの表示

_管理者_ サイドバーで、**[!UICONTROL Sales]**&#x200B;をクリックします。

## メニューオプション

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bで利用可能）

許可された購入者は、ショッピングカートから[ リクエスト ](../b2b/quote-request.md)を送信することで、販売者と[価格](../b2b/quotes.md)を交渉できます。

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bで利用可能）

再利用可能でカスタマイズ可能な[見積もりテンプレート ](../b2b/quote-templates-overview.md)を作成することで、購入者と販売者が見積もりプロセスを効率化できます。

### [!UICONTROL Orders]

[注文](orders.md)が行われると、販売注文がトランザクションの一時レコードとして作成されます。 支払いは処理されておらず、注文をキャンセルできます。

### [!UICONTROL Invoices]

[請求書](invoices.md)は、注文に対する支払いの受領記録です。 1回の注文で複数の請求書を作成できます。各請求書には、指定した数だけ、または購入した製品の数を指定できます。 支払いアクションに応じて、請求書が生成されたときに支払いを自動的にキャプチャできます。

### [!UICONTROL Shipments]

[配送](shipments.md)は、発送された注文の商品の記録です。 請求書と同様に、注文のすべての商品が出荷されるまで、複数の出荷を1回の注文に関連付けることができます。

### [!UICONTROL Credit Memos]

[ クレジットメモ ](credit-memos.md)は、全額払い戻しまたは一部払い戻しの期限を顧客に示す文書です。 金額は購入に適用されるか、顧客に返金されます。

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

返品された商品認証[ （RMA）は、交換または返金のために商品の返品をリクエストするお客様に付与できます。 ](returns.md)RMAは、Simple、Grouped、Configurable、Bundleの各タイプの製品に対して発行できます。 ただし、RMAは、バーチャルおよびダウンロード可能な商品、ギフトカードでは利用できません。

### [!UICONTROL Billing Agreements]

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

[請求契約書](paypal-billing-agreements.md)は、1回の購入に限定されない点を除き、発注書に似ています。 チェックアウト時に、お客様は支払い方法として請求契約書を選択します。 請求契約書では、顧客は購入するたびに支払い情報を入力する必要がないため、チェックアウトプロセスが合理化されます。

### [!UICONTROL Transactions]

[ トランザクション ](transactions.md) ページには、ストアとすべての支払いシステムの間で行われたすべての支払いアクティビティが一覧表示され、より詳細な情報にアクセスできます。

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

Braintree Virtual Terminal ページで、管理者ユーザーは選択した金額の支払いを受け入れることができます。 ターミナル機能を利用できるようにするには、マーチャントが基本的な[Braintree設定](braintree.md)を設定する必要があります。 Braintreeでは、不正行為の検出とPayPalとの統合により、詳細にカスタマイズ可能なチェックアウト体験を提供します。

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

（アーカイブオプションを有効にする必要があります） [注文](order-archive.md)およびその他のセールスドキュメントをアーカイブすると、パフォーマンスが定期的に向上し、ワークスペースに不要な情報がなくなります。
