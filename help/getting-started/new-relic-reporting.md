---
title: '[!DNL New Relic] 報告書'
description: について説明します [!DNL New Relic] New Relic APM サービスのソフトウェアを含む、クラウドインフラストラクチャー上のAdobe Commerceのアカウントで使用できるレポート。
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] レポート

[New Relic][1] は、アプリケーションのインタラクションを分析および改善するのに役立つソフトウェア分析サービスです。 クラウドインフラストラクチャー上のAdobe Commerceのアカウントには、 [!DNL New Relic APM] サービス。 詳しくは、を参照してください [New Relic サービス][4] が含まれる _クラウドインフラストラクチャー上のCommerce ガイド_.

## 手順 1：にサインアップ [!DNL New Relic] アカウント

1. に移動します [[!DNL New Relic]][1] web サイトでアカウントに新規登録します。

   無料体験版アカウントに新規登録することもできます。

1. サイトの指示に従ってください。 プロンプトが表示されたら、最初にインストールする製品を選択します。

1. アカウントにいる間に、Commerce の構成を完了するために必要な次の資格情報を見つけます。

   | オプション | 説明 |
   | ------ | ----------- |
   | アカウント ID | から [!DNL New Relic] アカウントダッシュボード。アカウント ID は、URL 内の次の後の数字です。 `/accounts` |
   | アプリケーション ID | から [!DNL New Relic] アカウントダッシュボード、クリック **[!UICONTROL New Relic APM]**. メニューで、を選択します **[!UICONTROL Applications]**. 次に、アプリケーションを選択します。 アプリケーション ID は、URL次の後の番号です。 `/applications/` |
   | 新規 Relic API キー | から [!DNL New Relic] アカウントダッシュボード、クリック **[!UICONTROL Account Settings]**. 左側の統合の下のメニューで、 **[!UICONTROL Data Sharing]**. このページから API キーを作成、再生成または削除できます。 |
   | Insights API キー | から [!DNL New Relic] アカウントダッシュボード、クリック **[!UICONTROL Insights]**. 左側の管理の下のメニューで、次を選択します **[!UICONTROL API Keys]**. Insights API キーがこのページに表示されます。 必要に応じて、プラス記号（**+**）を選択し、キーを生成します。 |

   {style="table-layout:auto"}

## 手順 2：をインストールする [!DNL New Relic] サーバー上のエージェント

使用目的 [!DNL New Relic APM Pro] データを収集して送信するには、PHP エージェントがサーバーにインストールされている必要があります。

1. Web エージェントの選択を求められたら、 **PHP**.

1. サーバー上に PHP エージェントを設定するには、次の手順に従います。

   ヘルプが必要な場合は、 [PHP 用New Relic][3].

1. cron がサーバー上で実行されていることを確認します。

   詳しくは、 [Cron の設定と実行][5] 開発者向けドキュメント

## 手順 3：ストアの設定

>[!NOTE]
>これらの設定オプションは、クラウドインフラストラクチャー上のAdobe Commerceには適用されません。
>
>Pro プランを利用している場合は、New Relicは既にインストールされています [事前設定されており、デフォルトで有効](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). スタータープランを使用している場合は、を完了する必要があります [New Relic設定手順](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) これは、設定プロセスの一部です。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のナビゲーションパネルで、 **[!UICONTROL General]** 展開済み、を選択 **[!UICONTROL New Relic Reporting]** 次の手順を実行します。

   ![New Relic レポートの設定](./assets/new-relic-reporting-general.png){width="600"}

   * を設定 **[!UICONTROL Enable New Relic Integration]** 対象： `Yes`.

   * が含まれる **[!UICONTROL Insights API URL]**&#x200B;をパーセントで置き換えます（`%`）記号はNew Relic アカウント ID を使用します。

   * を入力 **[!UICONTROL New Relic Account ID]**.

   * を入力 **[!UICONTROL New Relic Application ID]**.

   * を入力 **[!UICONTROL New Relic API Key]**.

   * 入力 **[!UICONTROL Insights API Key]**.

1. の場合 **[!UICONTROL New Relic Application Name]**&#x200B;を入力し、内部参照用の設定を識別する名前を入力します。

1. （オプション） **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**&#x200B;を選択 `Yes` ストアフロントと管理者の収集したデータを別々のアプリとしてNew Relicに送信する

   このオプションには、に名前を入力する必要があります **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >この機能を有効にすると、偽陽性の数が減ります [!DNL New Relic] アラートと有効化により、フロントエンドのパフォーマンスに厳密に対応した監視とアラートを設定できます。 New Relicは、アプリケーション名がに追加された個別のアプリデータファイルを受け取ります `Adminhtml` フロントエンド 例： `MyStore_Adminhtml`

1. 完了したら、 **[!UICONTROL Save Config]**.

## 手順 4：で Cron を有効にする [!DNL New Relic] レポート

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Cron]** セクション。

   ![New Relic Cron の設定](./assets/new-relic-reporting-cron.png){width="600"}

1. を設定 **[!UICONTROL Enable Cron]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## [!DNL New Relic] クエリ

[!DNL New Relic Insights] データは、で記述されたステートメントに基づいています [!DNL New Relic Query Language] （NRQL）、および含めるカスタムパラメーター。 データは、アドホッククエリから、またはダッシュボードに保存されたクエリから返すことができます。 詳しくは、 [NRQL リファレンス][6] が含まれる [!DNL New Relic] ドキュメント。

### 管理イベント

#### アクティブな管理者ユーザー

アクティブな管理者ユーザーの数を返します。

    SELECT uniqueCount （AdminId）
    トランザクションから
    appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 現在アクティブな管理者ユーザー

アクティブな管理者ユーザーの名前を返します。

    ユニークを選択（AdminName）
    トランザクションから
    appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 最近の管理者アクティビティ

最近の管理者アクションの数を返します。

    SELECT count （AdminId）
    トランザクションから
    appName =&#39;&lt;your_app_name>&#39; 1 日前からの FACET AdminName

#### 最新の管理者アクティビティ

管理者ユーザー名、期間、アプリケーション名など、最近の管理者アクションに関する詳細情報を返します。

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName !&lt;/your_app_name>= &#39;該当なし&#39; 制限 50

### Cron イベント

#### カテゴリー数

指定した期間におけるカテゴリイベントのアプリケーション数を返します。

    SELECT average （CatalogCategoryCount）
    CRON から
    CatalogCategoryCount が NULL でない場合
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分

#### 現在のカタログ数

指定した期間におけるカテゴリ別のカタログ内のアプリケーション イベントの平均数を返します。

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 分前 LIMIT 1
&lt;/your_app_name>
#### アクティブ製品

指定された期間における製品別のアプリケーション イベントの数を返します。

    SELECT average （CatalogProductActiveCount）
    CRON から
    CatalogProductActiveCount が NULL でない場合
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分

#### アクティブな製品数

指定された期間における製品別のアクティブなアプリケーション・イベントの平均数が戻されます。

    SELECT average （CatalogProductActiveCount）
    CRON から
    CatalogProductActiveCount が NULL でない場合
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### 設定可能な製品

指定された期間内の設定可能な製品のアプリケーション イベントの平均数を返します。

    SELECT average （CatalogProductConfigurableCount）
    CRON から
    CatalogProductConfigurableCount が NULL でない場合
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分

#### 設定可能な製品数

指定された期間内の設定可能な製品別のアプリケーションイベントの平均数を返します。

    SELECT average （CatalogProductConfigurableCount）
    CRON から
    CatalogProductConfigurableCount が NULL でない場合
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### 製品数（すべて）

すべての製品の申請イベントの合計数を返します。

    SELECT average （CatalogProductCount）
    CRON から
    CatalogProductCount が NULL でない場合
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分

#### 現在の製品数（すべて）

指定された期間におけるすべての製品のアプリケーション・イベントの平均数が戻されます。

    SELECT average （CatalogProductCount）
    CRON から
    CatalogProductCount が NULL でない場合
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### 顧客数

アプリケーション イベントの平均数を顧客別に返します。

    SELECT average （CustomerCount）
    CRON から
    CustomerCount が NULL でない場合
    および CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分

#### 現在の顧客数

指定された期間の平均顧客数を返します。

    SELECT average （CustomerCount）
    CRON から
    CustomerCount が NULL でない場合
    CustomerCount > 0 である場合
    AND appName = &#39;&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### モジュールステータス

指定された期間内にアプリケーション モジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average （ModulesDisabled）,average （ModulesEnabled）,average
    （ModulesInstalled）
    CRON から &lt;
    AppName = &#39;の場合&lt;your_app_name>&#39; TIMESERIES 2 分

#### 現在のモジュールステータス

指定された期間内にモジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average （ModulesDisabled）,average （ModulesEnabled）,average
    （ModulesInstalled）
    CRON から
    AppName = &#39;の場合&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### Web サイトとストアの数

指定された期間中の web サイトおよびストア別のアプリケーションイベントの平均数を返します。

    SELECT average （StoreViewCount）, average （WebsiteCount）
    CRON から
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 分

#### 現在の web サイトとストアの数

指定された期間における現在のアプリケーション・イベントの平均数が戻されます。

    SELECT average （StoreViewCount）, average （WebsiteCount）
    CRON から
    AppName = &#39;の場合&lt;your_app_name>&#39; 2 分前の制限 1 からの経過時間

#### Cron - イベントからのすべてのデータ

すべてのアプリケーション イベント データを返します。

    SELECT *
    CRON から
    AppName = &#39;の場合&lt;your_app_name>&#39;

### 顧客

#### アクティブな顧客数

指定された期間のアクティブな顧客の数を返します。

    SELECT uniqueCount （CustomerId）
    トランザクションから
    AppName = &#39;の場合&lt;your_app_name>&#39; 15 分前から

#### アクティブな顧客

指定された期間のアクティブな顧客の名前を返します。

    SELECT uniques （CustomerName）
    トランザクションから
    appName=&#39;&lt;your_app_name>&#39; 15 分前から

#### 上位のお客様

指定された期間内の上位顧客を返します。

    SELECT count （CustomerId）
    トランザクションから
    AppName = &#39;の場合&lt;your_app_name>&#39; 1 日前からの FACET CustomerName

#### 最近の管理者アクティビティ

顧客名や訪問期間など、最近のアクティビティの定義済みレコード数を返します。

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

#### 合計注文金額

指定した期間に受注された明細品目の合計数を戻します。

    SELECT sum(orderValue)
    FROM トランザクション 1 日前以降

#### オーダーされた合計行項目

指定した期間の中で注文された行項目の合計数を返します。

    SELECT sum （lineItemCount）
    1 日前からのトランザクション


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
