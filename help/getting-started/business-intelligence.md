---
title: '[!DNL Commerce Intelligence] ツール'
description: Adobe CommerceとMagento Open SourceマーチャントがCommerce Intelligence ツールを使用して、健全なビジネス上の意思決定に使用されるインサイトを得る方法について説明します。
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: 78bcac16713f9ec87faf7029732972db73216e79
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] ツール

Commerce Intelligence ツールを使用すると、ビジネス上の意思決定を健全にするために使用されるインサイトを得ることができます。

## [!DNL Commerce Intelligence] アカウント

をアクティブ化したとき [!DNL Commerce Intelligence] Adobeを通じてアカウントを設定し、約 70 件のレポートを含む 5 つのダッシュボードにアクセスできます。 これらのレポートは、データに関するインサイトを提供し、「注文が前月比でどのように増加しているか」、「最も常連客は誰か」、「クーポン戦略は機能しているか」などの質問に回答するように設計されています。 このツール セットの詳細については、を参照してください [Commerce Intelligence ユーザーガイド][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] は、Adobe CommerceおよびMagento Open Sourceに含まれています。 この機能を使用すると、製品、注文、顧客データに基づく動的レポートスイートにアクセスでき、ビジネスニーズに合わせてパーソナライズされたダッシュボードが提供されます。 While [!DNL Advanced Reporting] 使用 [!DNL Commerce Intelligence] analytics の場合、使用するためにCommerce Intelligence アカウントは必要ありません [!DNL Advanced Reporting].

技術情報については、を参照してください [[!DNL Advanced Reporting]][2]開発者ドキュメントの {:target=&quot;_blank&quot;} トピック。

>[!NOTE]
>
>との互換性の問題により [!DNL Adobe Commerce Intelligence]、Commerceは、AWS S3 バケットを内のソースデータファイルのメディアとして使用した高度なレポートを一時的にサポートできません [!DNL Commerce Intelligence].

![高度なレポートダッシュボード](./assets/reporting-advanced.png){width="700"}

### 要件

* Web サイトは、公開 web サーバー上で実行する必要があります。

* ドメインには有効なセキュリティ（SSL）証明書が必要です。

* [!DNL Commerce] は、エラーなく正常にインストールまたはアップグレードされた必要があります。

* が含まれる [!DNL Commerce] の設定 [url を格納](../stores-purchase/store-urls.md), **[!UICONTROL Base URL (Secure)]** ストア表示の設定は、セキュア URL を指している必要があります。 例： `https://yourdomain.com`.

* が含まれる [!DNL Commerce] ストア URL の設定、 **[!UICONTROL Use Secure URLs on Storefront]** および **[!UICONTROL Use Secure URLs in Admin]** に設定する必要があります。 `Yes`.

* [[!DNL Commerce] crontab][3] が作成され、インストールされたサーバーで cron ジョブが実行されている。

>[!NOTE]
>
>[!DNL Advanced Reporting] と共にのみ使用できます [!DNL Commerce] 1 つを継続的に使用したインストール [基準通貨](../stores-purchase/currency-configuration.md).


### 手順 1：を有効にする [!DNL Advanced Reporting]

が含まれる [!DNL Commerce] 設定、 [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) はデフォルトで有効になっており、cron が [設定済み](../configuration-reference/advanced/system.md) を実行しています。 サブスクリプションを確立する試みは、成功するまで、次の 24 時間にわたって各時間の初めに開始されます。 購読のステータスは、購読が正常に確立されるまで「保留中」です。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]** 展開済み、を選択 **[!UICONTROL Advanced Reporting]** 次の手順を実行します。

   * を確認します。 **[!UICONTROL Advanced Reporting Service]** はに設定されています。 `Enable` （デフォルト設定）。

   * を **[!UICONTROL Time of day to send data]** サービスでストアから更新されたデータを受信する時刻（24 時間制）。 デフォルトでは、データは午前 2 時に送信されます。

   * 次の下 **[!UICONTROL Industry Data]**、を選択します **[!UICONTROL Industry]** それが君の仕事にもっともよく当てはまる。

   ![高度なレポート設定](./assets/advanced-reporting-config.png){width="400"}

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 **[[!UICONTROL Cache Management]](../systems/cache-management.md)** ページ上部のメッセージで、無効なキャッシュを更新します。

1. 夜間または次にスケジュールされた更新の時間が過ぎるまで待ちます。 次に、サブスクリプションのステータスを確認します。 ステータスが「」の場合 _保留中_&#x200B;をインストールし、すべての要件が満たされていることを確認します。

### 手順 2：アクセス [!DNL Advanced Reporting]

1. 次のいずれかの操作を行います。

   * 日 _Admin_ サイドバー、選択 **[!UICONTROL Dashboard]**. 次に、 **[!UICONTROL Go to Advanced Reporting]**.
   * 日 _Admin_ サイドバー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   この [!DNL Advanced Reporting] ダッシュボードには、注文、顧客、製品の概要が表示されます。 ダッシュボード全体を表示するには、必ず下にスクロールします。

1. データをよりよく表示するには、 **[!UICONTROL Filters]** をクリックします。 次に、以下の手順を実行します。

   * 詳しくは、任意のデータポイントにポインタを合わせます。
   * すべてのダッシュボードレポートを表示するには、各タブをクリックします。

   ![データポイント](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## アクセス [!DNL Advanced Reporting] データリソース

詳細レポート ダッシュボードの右上隅のをクリックします。 **[!UICONTROL Additional Resources]**.

![高度なレポートデータリソース](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## トラブルシューティング

404 「Page Not Found」というメッセージが表示された場合は、ストアが次の要件を満たしていることを確認します。 [!DNL Advanced Reporting]. 次に、指示に従って統合がインストールされていることを確認します。

### 統合がアクティブであることを確認

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. を確認します **[!UICONTROL Magento Analytics user]** 統合がリストに表示され、 **[!UICONTROL Status]** 等しい `Active`.

1. ユーザーを再確立するには、 **[!UICONTROL Reauthorize]** 次の手順を実行します。

   ![再認証](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * プロンプトが表示されたら、 **[!UICONTROL Reauthorize]** API リソースへのアクセスを承認します。

     ![API リソースへのアクセスを再認証](./assets/advanced-reporting-integration-api.png){width="600"}

   * 拡張機能の統合トークンのリストが完了していることを確認します。 次に、 **完了**.

     ![統合トークン](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. 統合を示すメッセージを探します `Magento Analytics user` 再認証されました。

1. 夜間または次にスケジュールされた更新の時間が過ぎるまで待ちます。

### 単一の基本通貨を検証

[!DNL Advanced Reporting] と共にのみ使用できます [!DNL Commerce] 1 つしか使用していないインストール [基準通貨](../stores-purchase/currency-configuration.md) インストール時から。 その結果、履歴では、すべての注文が同じ基本通貨を使用します。 [!DNL Advanced Reporting] の基本通貨を変更し、履歴に別の基本通貨で処理された注文がある場合、は機能しません。

ストアに複数の基本通貨があるかどうかを判断するには、 [!DNL Commerce] 次の MySQL の例を使用して、コマンドラインからデータベースを取得します。 場合によっては、データ構造に合わせてテーブル名を変更する必要があります。

```sql
select distinct base_currency_code from sales_order;
```

### データの不一致

次のことに気付いた場合： `Data last updated...` キャプションには、今日ではなく昨日の日付が表示されます。詳細レポートの更新には、最大 1 日の遅延が生じる可能性があります。 この遅延は、予想されるキューサイズよりも大きいことが原因です。

## ダッシュボードレポート

**[!UICONTROL Orders]**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Revenue] | 定義された期間にストア表示で受け取ったすべての収益を表示します。 |
| [!UICONTROL Orders] | 定義された期間にストア ビューを通じて行われたすべての注文を表示します。 |
| [!UICONTROL AOV] | 定義された期間にストア ビューを通じて注文された平均注文額を表示します。 |
| [!UICONTROL Refunds] | 定義された期間にストア表示を通じて処理されたすべての払戻を表示します。 |
| [!UICONTROL Tax Collected] | 定義された期間にストア表示で徴収されたすべての税金を表示します。 |
| [!UICONTROL Shipping Collected] | 定義された期間にストア表示を通じて収集されたすべての配送料を表示します。 |
| [!UICONTROL Orders by Status] | 定義された期間における店舗表示の注文数をステータス別に表示します。 |
| [!UICONTROL Orders by Status] | 注文数の概要をステータス別にリストします。 |
| [!UICONTROL Coupon Usage] | 定義された期間にストア表示を通じて引き換えられるすべてのクーポンコードと各ユーザー数を一覧表示します。 |
| [!UICONTROL Orders and Revenue by Billing Region] | 定義された期間における店舗表示の注文数と売上高を地域別にリストします。 |
| [!UICONTROL Tax Collected by Billing Region] | 定義された期間にストア表示でリージョン別に徴収された税額をリストします。 |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | 定義された期間にストア ビューでリージョンごとに収集された配送料の一覧が表示されます。 |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Unique Customers] | 定義された期間にストア表示に関連付けられた一意の顧客アカウントの数を表示します。 |
| [!UICONTROL New Registered Accounts] | 定義された期間にストア表示に登録された新しい顧客アカウントの数を表示します。 |
| [!UICONTROL Top Coupon Users] | 顧客 ID 別の上位のクーポンユーザーおよび定義された期間内にストア表示のクーポンで発注された注文数をリストします。 |
| [!UICONTROL Customer KPI Table] | 定義された期間における店舗表示の注文数、売上高、および平均注文額を顧客 ID 別にリストします。 |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | 定義された期間にストア ビューを通じて販売された商品の数を表示します。 |
| [!UICONTROL Products Added to Wishlists] | 定義された期間にストア表示を通じてウィッシュリストに追加されたすべての製品をリストします。 |
| [!UICONTROL Best Selling Products by Quantity] | 定義された期間にストア表示を通じて販売された最も売れた商品および数量をリストします。 |
| [!UICONTROL Best Selling Products by Revenue] | 定義された期間内にストア表示を介した商品の販売によって生成された、最も売れた商品と収益を一覧表示します。 |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
