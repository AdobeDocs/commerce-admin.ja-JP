---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Commerce Admin の [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] ページで設定を確認します。
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
>Pro プランを使用している場合、New Relicは既に [ デフォルトで事前設定され、有効 ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html) になっています。 スタータープランを利用している場合は、設定プロセスの一部である ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment)0}New Relic設定手順を完了する必要があります。[

## [!UICONTROL General]

![ 一般 ](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | ストア表示 | ストアを [!DNL New Relic] Reporting で使用できるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL New Relic API URL] | ストア表示 | New Relic API がデプロイされている URL。 例：`https://api.newrelic.com/deployments.xml` |
| インサイト API の URL | ストア表示 | Insights API がデプロイされている URL。 パーセント記号（%）を使用して、アカウント ID を表します。 例：`https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | ストア表示 | [!DNL New Relic] アカウントに割り当てられたアカウント ID。 |
| [!UICONTROL New Relic Application ID] | ストア表示 | Commerce統合用に [!DNL New Relic] アカウントに割り当てられたアプリケーション ID。 |
| [!UICONTROL New Relic API Key] | ストア表示 | [!DNL New Relic] API へのアクセスを取得するために割り当てられたキー。 |
| [!UICONTROL Insights API Key] | ストア表示 | インサイトへのアクセス権を取得するために割り当てられたキー。 |
| [!UICONTROL New Relic Application Name] | ストア表示 | [!DNL New Relic] 統合に割り当てた名前。 |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | ストア表示 | ストアフロントおよび管理者用に収集されたレポートデータを個別のアプリとしてNew Relicに送信するオプション。 このオプションには、[!UICONTROL New Relic Application Name] の名前を入力する必要があります。 この機能により、収集されたアプリデータにアンダースコアが付いたアプリケーション名が追加されます。 例：`MyStore_Adminhtml`、`MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | ストア表示 | [Cron](../../systems/cron.md) を使用 [!DNL New Relic] てスケジュールに従ってレポートを実行できるかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}
