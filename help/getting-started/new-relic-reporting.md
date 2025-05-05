---
title: '[!DNL New Relic] レポート'
description: New Relic APM サ  [!DNL New Relic]  ビスのソフトウェアを含む、クラウドインフラストラクチャー上のAdobe Commerceのアカウントで使用できるレポートについて説明します。
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] レポート

[New Relic][1] は、アプリケーションのインタラクションを分析および改善するのに役立つソフトウェア分析サービスです。 クラウドインフラストラクチャー上のAdobe Commerceのアカウントには、[!DNL New Relic APM] サービス用のソフトウェアが含まれます。 詳しくは、_New Relic インフラストラクチャー上のCommerce ガイドの &rbrack;[4]0&rbrace; クラウドサービス &rbrace; を参照してください_&lbrack;

## 手順 1:[!DNL New Relic] アカウントに新規登録する

1. [[!DNL New Relic]][1] の web サイトに移動し、アカウントに新規登録します。

   無料体験版アカウントに新規登録することもできます。

1. サイトの指示に従ってください。 プロンプトが表示されたら、最初にインストールする製品を選択します。

1. アカウントにいる間に、Commerce の構成を完了するために必要な次の資格情報を見つけます。

   | オプション | 説明 |
   | ------ | ----------- |
   | アカウント ID | [!DNL New Relic] アカウントダッシュボードでは、アカウント ID は URL 内の `/accounts` 以降の番号です。 |
   | アプリケーション ID | [!DNL New Relic] アカウントダッシュボードで、「**[!UICONTROL New Relic APM]**」をクリックします。 メニューで、「**[!UICONTROL Applications]**」を選択します。 次に、アプリケーションを選択します。 アプリケーション ID は、URL次の後の番号です。 `/applications/` |
   | 新規 Relic API キー | [!DNL New Relic] アカウントダッシュボードで、「**[!UICONTROL Account Settings]**」をクリックします。 左側の「統合」の下のメニューで、「**[!UICONTROL Data Sharing]**」を選択します。 このページから API キーを作成、再生成または削除できます。 |
   | Insights API キー | [!DNL New Relic] アカウントダッシュボードで、「**[!UICONTROL Insights]**」をクリックします。 左側の管理の下のメニューで、「**[!UICONTROL API Keys]**」を選択します。 Insights API キーがこのページに表示されます。 必要に応じて、[ キーを挿入 ] の横のプラス記号（**+**）をクリックしてキーを生成します。 |

   {style="table-layout:auto"}

## 手順 2：サーバーへの [!DNL New Relic] エージェントのインストール

[!DNL New Relic APM Pro] を使用してデータを収集および送信するには、PHP エージェントがサーバーにインストールされている必要があります。

1. Web エージェントを選択するプロンプトが表示されたら、「**PHP**」をクリックします。

1. サーバー上に PHP エージェントを設定するには、次の手順に従います。

   ヘルプが必要な場合は、[New Relic for PHP][3] を参照してください。

1. cron がサーバー上で実行されていることを確認します。

   詳しくは、開発者向けドキュメントの [cron の設定と実行 ][5] を参照してください。

## 手順 3：ストアの設定

>[!NOTE]
>これらの設定オプションは、クラウドインフラストラクチャー上のAdobe Commerceには適用されません。
>
>Pro プランを使用している場合、New Relicは既に [ デフォルトで事前設定され、有効 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=ja) になっています。 スタータープランを利用している場合は、設定プロセスの一部である [&#128279;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=ja#configure-new-relic-for-starter-environment)0&rbrace;New Relic設定手順を完了する必要があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. **[!UICONTROL General]** が展開されている左側のナビゲーションパネルで「**[!UICONTROL New Relic Reporting]**」を選択し、以下の手順を実行します。

   ![New Relic レポートの設定 ](./assets/new-relic-reporting-general.png){width="600"}

   * **[!UICONTROL Enable New Relic Integration]** を `Yes` に設定します。

   * **[!UICONTROL Insights API URL]** で、パーセント（`%`）記号をNew Relic アカウント ID に置き換えます。

   * **[!UICONTROL New Relic Account ID]** を入力します。

   * **[!UICONTROL New Relic Application ID]** を入力します。

   * **[!UICONTROL New Relic API Key]** を入力します。

   * **[!UICONTROL Insights API Key]** を入力してください。

1. **[!UICONTROL New Relic Application Name]**：内部参照の設定を識別する名前を入力します。

1. （オプション） **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]** の場合は、「`Yes`」を選択して、ストアフロントと管理者の収集したデータを別のアプリとしてNew Relicに送信します。

   このオプションには、**[!UICONTROL New Relic Application Name]** の名前を入力する必要があります。

   >[!NOTE]
   >
   >この機能を有効にすると、偽陽性 [!DNL New Relic] アラートの数が減り、フロントエンドのパフォーマンスに厳密に対応した監視とアラートを設定できるようになります。 New Relicは、アプリケーション名が `Adminhtml` およびフロントエンドに追加された個別のアプリデータファイルを受け取ります。 例：`MyStore_Adminhtml`

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 手順 4:[!DNL New Relic] レポート用に Cron を有効にする

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Cron]**」セクションを展開します。

   ![New Relic Cron 設定 ](./assets/new-relic-reporting-cron.png){width="600"}

1. **[!UICONTROL Enable Cron]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## [!DNL New Relic] クエリ

[!DNL New Relic Insights] データは、[!DNL New Relic Query Language] （NRQL）で記述されたステートメントと、含める可能性のあるカスタムパラメーターに基づいています。 データは、アドホッククエリから、またはダッシュボードに保存されたクエリから返すことができます。 詳しくは、[!DNL New Relic] ドキュメントの [NRQL リファレンス ][6] を参照してください。

### 管理イベント

#### アクティブな管理者ユーザー

アクティブな管理者ユーザーの数を返します。

    SELECT uniqueCount （AdminId） 
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 分 

#### 現在アクティブな管理者ユーザー

アクティブな管理者ユーザーの名前を返します。

    SELECT uniques （AdminName） 
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 分 

#### 最近の管理者アクティビティ

最近の管理者アクションの数を返します。

    SELECT count （AdminId） 
    FROM Transaction
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName SINCE 1 day ago

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
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
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
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分 

#### アクティブな製品数

指定された期間における製品別のアクティブなアプリケーション・イベントの平均数が戻されます。

    SELECT average （CatalogProductActiveCount） 
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
     および CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### 設定可能な製品

指定された期間内の設定可能な製品のアプリケーション イベントの平均数を返します。

    SELECT average （CatalogProductConfigurableCount） 
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分 

#### 設定可能な製品数

指定された期間内の設定可能な製品別のアプリケーションイベントの平均数を返します。

    SELECT average （CatalogProductConfigurableCount） 
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
     および CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### 製品数（すべて）

すべての製品の申請イベントの合計数を返します。

    SELECT average （CatalogProductCount） 
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分 

#### 現在の製品数（すべて）

指定された期間におけるすべての製品のアプリケーション・イベントの平均数が戻されます。

    SELECT average （CatalogProductCount） 
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
     および CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### 顧客数

アプリケーション イベントの平均数を顧客別に返します。

    SELECT average （CustomerCount） 
    FROM Cron
    WHERE CustomerCount NOT NULL
     および CustomerCount > 0&lt;
     および appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分 

#### 現在の顧客数

指定された期間の平均顧客数を返します。

    SELECT average （CustomerCount） 
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; LIMIT 1

#### モジュールステータス

指定された期間内にアプリケーション モジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average （ModulesDisabled）, average （ModulesEnabled）, average
     （ModulesInstalled） 
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 分 

#### 現在のモジュールステータス

指定された期間内にモジュールが有効、無効、またはインストールされた平均回数を返します。

    SELECT average （ModulesDisabled）, average （ModulesEnabled）, average
     （ModulesInstalled） 
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Web サイトとストアの数

指定された期間中の web サイトおよびストア別のアプリケーションイベントの平均数を返します。

    SELECT average （StoreViewCount）, average （WebsiteCount） 
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name&gt;&#39; TIMESERIES 2 分 

#### 現在の web サイトとストアの数

指定された期間における現在のアプリケーション・イベントの平均数が戻されます。

    SELECT average （StoreViewCount）, average （WebsiteCount） 
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Cron - イベントからのすべてのデータ

すべてのアプリケーション イベント データを返します。

    SELECT *
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39;

### 顧客

#### アクティブな顧客数

指定された期間のアクティブな顧客の数を返します。

    SELECT uniqueCount （CustomerId） 
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 15 分 

#### アクティブな顧客

指定された期間のアクティブな顧客の名前を返します。

    SELECT uniques （CustomerName） 
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 分 

#### 上位のお客様

指定された期間内の上位顧客を返します。

    SELECT count （CustomerId） 
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName SINCE 1 day ago

#### 最近の管理者アクティビティ

顧客名や訪問期間など、最近のアクティビティの定義済みレコード数を返します。

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName!&lt;/your_app_name>= &#39;該当なし&#39; 制限 50

### 詻

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
    FROM Transaction SINCE 1 day ago


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=ja
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ja
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
