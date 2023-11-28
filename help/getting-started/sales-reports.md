---
title: セールスレポート
description: The [!DNL Commerce] 販売レポートを使用すると、注文、税金、請求書、送料、返金、クーポン、PayPal 決済の追跡に役立ちます。
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# セールスレポート

販売レポートの選択には、注文、税金、請求済み、送料、返金、クーポン、PayPal 決済が含まれます。

## レポートフィルター

Web サイト全体または 1 つのストアの販売レポートを生成できます。 販売レポートは、期間、日付、ステータスでフィルタリングできます。

![販売レポートフィルター](./assets/tax-report.png){width="600"}

販売レポートをフィルタするには、次のオプションを設定します。

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Date Used] | レポートに使用するデータを設定します。 |
| [!UICONTROL Period] | データを使用する期間：日、月、年。 |
| [!UICONTROL From/To] | 開始日と終了日で検索データを定義するために使用します。 |
| [!UICONTROL Order Status] | 注文ステータスを示します |
| [!UICONTROL Empty Rows] | レポートに空白の行を追加するかどうかを示します。 |

## [!UICONTROL Orders Report]

The [!UICONTROL Orders Report] には、販売、請求済みの金額、払い戻し済みの金額、収集された税金、送料、割引の合計を含む、発注およびキャンセルされた注文数が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。

1. クリック **[!UICONTROL Show Report]**.

![注文件数レポートレコード](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

The [!UICONTROL Tax Report] 適用される税ルール、税率、注文件数、請求される税額が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。


1. クリック **[!UICONTROL Show Report]**.

![税レポート](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

The [!UICONTROL Invoice Report] 期間中のオーダーと請求書の数が含まれ、請求済み、支払済みおよび未払の金額が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。

1. クリック **[!UICONTROL Show Report]**.

![請求書レポート](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

The [!UICONTROL Shipping Report] 使用した運送業者または発送方法の注文数を含みます。合計販売額と合計送料の金額が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。

1. クリック **[!UICONTROL Show Report]**.

![発送レポート](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

The [!UICONTROL Refunds Report] 返金済みの注文件数と、オンラインおよびオフラインで返金された合計金額が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。

1. クリック **[!UICONTROL Show Report]**.

![払い戻しレポート](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

The [!UICONTROL Coupons Report] には、指定した期間に使用された各クーポンコード、関連する価格ルール、および使用回数が含まれ、合計と販売と割引の小計が含まれます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Adobe Analytics の **[!UICONTROL Filter]** 「 」セクションで、レポートへの入力に使用するレポート期間オプションと注文ステータスを選択します。

1. クリック **[!UICONTROL Show Report]**.

詳しくは、 [!UICONTROL Coupons Report] プロモーションキャンペーンのデータを収集するには、 [クーポンレポート](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) （内） _マーチャンダイジングとプロモーションガイド_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

The [PayPal 決済レポート] ページには、デビットカードトランザクション、開始日と終了日、総額、関連費用など、イベントのタイプが含まれます。 レポートは、PayPal の最新のデータで自動的に更新できます。 日付範囲、マーチャントアカウント、トランザクション ID、請求書 ID または PayPal 参照 ID に対するフィルタリングオプションがあります。

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![PayPal 決済レポート](./assets/reports-sales-paypal-settlement.png){width="600"}

詳しくは、 [!UICONTROL PayPal Settlement Reports] 各 PayPal トランザクションに関する情報を取得して決済に影響を与える場合は、 [PayPal 決済レポート](../stores-purchase/paypal-settlement-reports.md) （内） _店舗および購入エクスペリエンスガイド_.

## [!UICONTROL Braintree Settlement Report]

The [Braintree](../stores-purchase/braintree.md) 決済レポートは、作成日、金額、ステータス、取引タイプ、支払いタイプ、取引 ID、注文 ID、PayPal 支払い ID、タイプ、商人口座 ID または決済バッチ ID に従ってフィルタリングできます。 このレポートには、トランザクション ID、注文 ID、PayPal の支払 ID、種類、作成日、金額、決済コード、ステータス、決済応答テキスト、償還 ID、商人アカウント ID、決済バッチ ID および通貨が含まれます。

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## レポートの書き出し

1. レポートをエクスポートするには、ファイルタイプを選択します。 `Excel XML` または `CSV`

1. クリック **[!UICONTROL Export]**.

## 統計を更新

セールスレポートの生成によるパフォーマンスへの影響を軽減するには、次の手順を実行します。 [!DNL Commerce] 各レポートに必要な統計を計算して保存します。 レポートが生成されるたびに統計を再計算するのではなく、統計を更新しない限り、保存された統計が使用されます。 最新のデータを含めるには、販売レポートを生成する前に、レポート統計を更新する必要があります。

![統計を更新](./assets/refresh-stats.png){width="700"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. リストで、更新する各レポートのチェックボックスを選択します。

1. を設定します。 **[!UICONTROL Actions]** コントロールを次のいずれかに設定します。

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. クリック **[!UICONTROL Submit]**.
