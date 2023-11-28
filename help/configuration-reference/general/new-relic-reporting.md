---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: 次のページで設定を確認します： [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] コマース管理のページ。
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![一般](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | ストア表示 | ストアをと共に使用できるかどうかを指定します [!DNL New Relic] レポート。 オプション： `Yes` / `No` |
| [!UICONTROL New Relic API URL] | ストア表示 | New Relic API がデプロイされる URL。 例： `https://api.newrelic.com/deployments.xml` |
| インサイト API URL | ストア表示 | Insights API がデプロイされる URL。 アカウント ID を表すには、パーセント記号 (%) を使用します。 例： `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | ストア表示 | に割り当てられたアカウント ID [!DNL New Relic] アカウント。 |
| [!UICONTROL New Relic Application ID] | ストア表示 | に割り当てられたアプリケーション ID [!DNL New Relic] コマース統合用のアカウント。 |
| [!UICONTROL New Relic API Key] | ストア表示 | アクセス権を取得するために割り当てられたキー [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | ストア表示 | インサイトにアクセスするために割り当てられたキー。 |
| [!UICONTROL New Relic Application Name] | ストア表示 | 割り当てた名前 [!DNL New Relic] 統合とも呼ばれます。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | ストア表示 | ストアフロントおよび管理者用に収集されたレポートデータを別のアプリとしてNew Relicに送信するオプション。 このオプションには、 [!UICONTROL New Relic Application Name]. この機能では、収集されたアプリデータにアプリケーション名にアンダースコアを追加します。 例： `MyStore_Adminhtml`, `MyStore_frontend` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | ストア表示 | 次の場合に決定 [!DNL New Relic] レポートは、 [Cron](../../systems/cron.md). オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
