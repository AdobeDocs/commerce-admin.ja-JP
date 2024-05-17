---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: の設定を確認します。 [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] コマース管理者のページ。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 1aec5c618d1f3f7f083523956d2aee62b777faca
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>これらの設定オプションは、クラウドインフラストラクチャー上のAdobe Commerceには適用されません。
>
>Pro プランを利用している場合は、New Relicは既にインストールされています [事前設定されており、デフォルトで有効](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). スタータープランを使用している場合は、を完了する必要があります [New Relic設定手順](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) これは、設定プロセスの一部です。

## [!UICONTROL General]

![一般](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | ストア表示 | ストアをで使用できるかどうかを決定します [!DNL New Relic] レポート。 オプション： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | ストア表示 | New Relic API がデプロイされている URL。 例： `https://api.newrelic.com/deployments.xml` |
| インサイト API の URL | ストア表示 | Insights API がデプロイされている URL。 パーセント記号（%）を使用して、アカウント ID を表します。 例： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | ストア表示 | に割り当てられたアカウント ID [!DNL New Relic] アカウント。 |
| [!UICONTROL New Relic Application ID] | ストア表示 | に割り当てられたアプリケーション ID [!DNL New Relic] Commerce統合用アカウント。 |
| [!UICONTROL New Relic API Key] | ストア表示 | へのアクセス権を取得するために割り当てられたキー [!DNL New Relic] API です。 |
| [!UICONTROL Insights API Key] | ストア表示 | インサイトへのアクセス権を取得するために割り当てられたキー。 |
| [!UICONTROL New Relic Application Name] | ストア表示 | に割り当てた名前 [!DNL New Relic] 統合。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | ストア表示 | ストアフロントおよび管理者用に収集されたレポートデータを個別のアプリとしてNew Relicに送信するオプション。 このオプションには、に名前を入力する必要があります [!UICONTROL New Relic Application Name]. この機能により、収集されたアプリデータにアンダースコアが付いたアプリケーション名が追加されます。 例： `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | ストア表示 | 次のかどうかを判断します [!DNL New Relic] レポートは、以下を使用してスケジュールに従って実行できます [Cron](../../systems/cron.md). オプション： `Yes` / `No` |

{style="table-layout:auto"}
