---
title: '[!DNL New Relic] レポート'
description: 詳しくは、 [!DNL New Relic] New Relic APM サービスのソフトウェアを含む、クラウドインフラストラクチャ上のAdobe Commerceのアカウントのレポートで使用できます。
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] レポート

[New Relic][1] は、アプリケーションの操作を分析および改善するのに役立つソフトウェア分析サービスです。 クラウドインフラストラクチャ上のAdobe Commerceのアカウントには、 [!DNL New Relic APM] サービス。 詳しくは、 [New Relic services][4] （内） _Commerce on Cloud Infrastructure ガイド_.

## 手順 1：に新規登録する [!DNL New Relic] アカウント

1. 次に移動： [[!DNL New Relic]][1] web サイトにアクセスし、アカウントに新規登録します。

   無料体験版アカウントに登録することもできます。

1. サイトの指示に従ってください。 プロンプトが表示されたら、最初にインストールする製品を選択します。

1. アカウントにいる間に、Commerce の構成を完了するために必要な次の資格情報を見つけます。

   | オプション | 説明 |
   | ------ | ----------- |
   | アカウント ID | お使いの [!DNL New Relic] アカウントダッシュボードの「アカウント ID 」は、URL の次の番号になります。 `/accounts` |
   | アプリケーション ID | お使いの [!DNL New Relic] アカウントダッシュボードで、 **[!UICONTROL New Relic APM]**. メニューで、「 」を選択します。 **[!UICONTROL Applications]**. 次に、アプリケーションを選択します。 アプリケーション ID は、URL次の後の番号です。 `/applications/` |
   | 新規 Relic API キー | お使いの [!DNL New Relic] アカウントダッシュボードで、 **[!UICONTROL Account Settings]**. 左側の「統合」の下にあるメニューで、を選択します。 **[!UICONTROL Data Sharing]**. このページから API キーを作成、再生成、または削除できます。 |
   | インサイト API キー | お使いの [!DNL New Relic] アカウントダッシュボードで、 **[!UICONTROL Insights]**. 左側の「管理」の下にあるメニューで、を選択します。 **[!UICONTROL API Keys]**. インサイト API キーがこのページに表示されます。 必要に応じて、プラス記号 (**+**) をクリックし、キーを生成するキーを挿入します。 |

   {style="table-layout:auto"}

## 手順 2: [!DNL New Relic] サーバー上のエージェント

次を使用するには： [!DNL New Relic APM Pro] データを収集して送信するには、PHP エージェントをサーバーにインストールする必要があります。

1. Web エージェントを選択するよう求められたら、 **PHP**.

1. サーバー上に PHP エージェントを設定するには、次の手順に従います。

   ヘルプが必要な場合は、 [New Relic for PHP][3].

1. cron がサーバーで実行されていることを確認します。

   詳しくは、 [cron の設定と実行][5] （開発者向けドキュメント）。

## 手順 3：ストアの設定

>[!NOTE]
>これらの設定オプションは、クラウドインフラストラクチャ上のAdobe Commerceには適用されません。
>
>Pro プランを使用している場合、New Relicは既に [デフォルトで事前設定および有効化](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). スタータープランを使用している場合は、 [New Relicの設定手順](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) 設定プロセスの一部です。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで **[!UICONTROL General]** は展開済みで、「 **[!UICONTROL New Relic Reporting]** 次の操作を実行します。

   ![New Relic Reporting 設定](./assets/new-relic-reporting-general.png){width="600"}

   * 設定 **[!UICONTROL Enable New Relic Integration]** から `Yes`.

   * Adobe Analytics の **[!UICONTROL Insights API URL]**、割合 (`%`) 記号をNew Relicアカウント ID に置き換えます。

   * を入力します。 **[!UICONTROL New Relic Account ID]**.

   * を入力します。 **[!UICONTROL New Relic Application ID]**.

   * を入力します。 **[!UICONTROL New Relic API Key]**.

   * 入力 **[!UICONTROL Insights API Key]**.

1. の場合 **[!UICONTROL New Relic Application Name]**&#x200B;内部参照の設定を識別する名前を入力します。

1. （オプション）の場合 **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**&#x200B;を選択します。 `Yes` ストアフロントと管理者用に収集したデータを別個のアプリとしてNew Relicに送信する場合。

   このオプションには、 **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >この機能を有効にすると、偽陽性の数が減ります [!DNL New Relic] アラートとは、設定された監視とアラートを、フロントエンドのパフォーマンスに厳密に対応するように許可します。 New Relicは、名前にが付いた別のアプリデータファイルを受け取ります。このファイルの `Adminhtml` フロントエンド。 例： `MyStore_Adminhtml`

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 手順 4:Cron を有効にする [!DNL New Relic] レポート

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Cron]** 」セクションに入力します。

   ![New Relic Cron 設定](./assets/new-relic-reporting-cron.png){width="600"}

1. 設定 **[!UICONTROL Enable Cron]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## [!DNL New Relic] クエリ

[!DNL New Relic Insights] データは、 [!DNL New Relic Query Language] (NRQL)、および含める可能性のある任意のカスタムパラメーター。 データは、アドホッククエリから返すことも、ダッシュボードに保存されたクエリから返すこともできます。 詳しくは、 [NRQL 参照][6] （内） [!DNL New Relic] ドキュメント。

### 管理イベント

#### アクティブな管理者ユーザー

アクティブな管理者ユーザーの数を返します。

    SELECT uniqueCount(AdminId)
    FROM トランザクション
    WHERE appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 現在アクティブな管理者ユーザー

アクティブな管理者ユーザーの名前を返します。

    SELECT uniques(AdminName)
    FROM トランザクション
    WHERE appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 最近の管理者アクティビティ

最近の管理者アクションの数を返します。

    SELECT count(AdminId)
    FROM トランザクション
    WHERE appName =&#39;&lt;your_app_name>&#39; 1 日前以降のファセット AdminName

#### 最新の管理アクティビティ

管理者ユーザー名、期間、アプリケーション名など、最近の管理者アクションに関する詳細情報を返します。

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&#39; AND AdminName &lt;your_app_name>IS NOT NULL
    AND AdminName !&lt;/your_app_name>= &#39;該当なし&#39; 制限 50

### Cron イベント

#### カテゴリー数

指定した期間におけるカテゴリイベントのアプリケーション数を返します。

    SELECT average(CatalogCategoryCount)
    Cron から
    CATALOGCategoryCount が NULL ではない場合
    AND appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 現在のカタログ数

指定された期間の、カテゴリ別のカタログ内のアプリケーションイベントの平均数を返します。

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 分前 LIMIT 1
&lt;/your_app_name>
#### アクティブ製品

指定された期間内の製品ごとのアプリケーションイベント数を返します。

    SELECT average(CatalogProductActiveCount)
    Cron から
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 有効な製品数

指定された期間の製品ごとのアクティブなアプリケーションイベントの平均数を返します。

    SELECT average(CatalogProductActiveCount)
    Cron から
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### 設定可能な製品

指定された期間の設定可能な製品のアプリケーションイベントの平均数を返します。

    SELECT average(CatalogProductConfigurableCount)
    Cron から
    CatalogProductConfigurableCount が NULL でない場合
    AND appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 設定可能な製品数

指定された期間の、設定可能な製品別のアプリケーションイベントの平均数を返します。

    SELECT average(CatalogProductConfigurableCount)
    Cron から
    CatalogProductConfigurableCount が NULL でない場合
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### 製品数（すべて）

すべての製品のアプリケーションイベントの合計数を返します。

    SELECT average(CatalogProductCount)
    Cron から
    CATALOGProductCount が NULL ではない場合
    AND appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 現在の製品数（すべて）

指定した期間のすべての製品のアプリケーションイベントの平均数を返します。

    SELECT average(CatalogProductCount)
    Cron から
    CATALOGProductCount が NULL ではない場合
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### 顧客数

顧客別のアプリケーションイベントの平均数を返します。

    SELECT average(CustomerCount)
    Cron から
    CustomerCount が NULL でない場合
    および CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 現在の顧客数

指定された期間の顧客の平均数を返します。

    SELECT average(CustomerCount)
    Cron から
    CustomerCount が NULL でない場合
    および顧客数 > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### モジュールのステータス

指定された期間内にアプリケーションモジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    （インストールされたモジュール）
    Cron から &lt;
    WHERE appName = &#39;&lt;your_app_name>&#39;時系列 2 分

#### 現在のモジュールのステータス

指定された期間にモジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    （インストールされたモジュール）
    Cron から
    WHERE appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### Web サイトおよびストア数

指定された期間の、Web サイトおよびストアごとのアプリケーションイベントの平均数を返します。

    SELECT average(StoreViewCount), average(WebsiteCount)
    Cron から
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 分

#### 現在の Web サイトおよび店舗数

指定した期間の現在のアプリケーションイベントの平均数を返します。

    SELECT average(StoreViewCount), average(WebsiteCount)
    Cron から
    WHERE appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 から

#### Cron — イベントからのすべてのデータ

すべてのアプリケーションイベントデータを返します。

    選択*
    Cron から
    WHERE appName = &#39;&lt;your_app_name>&#39;

### 顧客

#### アクティブな顧客数

指定された期間内のアクティブな顧客の数を返します。

    SELECT uniqueCount(CustomerId)
    FROM トランザクション
    WHERE appName = &#39;&lt;your_app_name>&#39; 15 分前から

#### アクティブな顧客

指定された期間のアクティブな顧客の名前を返します。

    SELECT uniques(CustomerName)
    FROM トランザクション
    WHERE appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 上位の顧客

指定した期間の上位の顧客を返します。

    SELECT count(CustomerId)
    FROM トランザクション
    WHERE appName = &#39;&lt;your_app_name>&#39; 1 日前以降のファセット CustomerName

#### 最近の管理者アクティビティ

顧客名と訪問期間を含む、最近のアクティビティの定義済みのレコード数を返します。

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;該当なし&#39; 制限 50

### 注文

#### 注文数字

指定した期間における注文数を返します。

    SELECT count(Order)
    FROM トランザクション 1 日前以降

#### 合計注文額

指定された期間に注文された行項目の合計数を返します。

    SELECT sum(orderValue)
    FROM トランザクション 1 日前以降

#### オーダーされた合計行項目

指定した期間の中で注文された行項目の合計数を返します。

    SELECT sum(lineItemCount)
    1 日前からのトランザクション


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
