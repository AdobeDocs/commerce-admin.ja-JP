---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: の設定を確認します。 [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] コマース管理者のページ。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

これらの設定は、次の場合に使用できます [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) がインストールされました。

![Sales Channel設定](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | グローバル | オプション：<br/><br/>**`Once Daily`**：このオプションを選択して、1 日に 1 回ストアのアクティビティ履歴を消去します。<br/><br/>**`Once Weekly`**：ストアのアクティビティ履歴を毎週 1 回消去するには、このオプションを選択します。<br/><br/>**`Once Monthly`**:（デフォルト）ストアのアクティビティ履歴を毎月 1 回クリアするには、このオプションを選択します。 |
| [!UICONTROL Background Tasks (CRON) Source] | グローバル | を選択 `Magento CRON` を指定します [!DNL Amazon Sales Channel] は、Commerce cron 設定を使用して、Amazon Seller Central との通信およびデータ同期間隔を決定します。 |
| [!UICONTROL Enable Debug Logging] | グローバル | を選択 `Enabled` トラブルシューティングが必要な場合に追加の同期データを収集します。<br/><br/>このオプションはデフォルトでは無効になっており、トラブルシューティングに必要な場合にのみ有効にしてください。継続したログはパフォーマンスに悪影響を及ぼすからです。 トラブルシューティングが有効な場合は、完了時に無効にする必要があります。<br/><br/>**_注意&#x200B;_**:AmazonのSales Channelログは、に書き込まれます `/var/log/channel_amazon.log` ファイルおよび次で表示できます [開発者モード](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | グローバル | を選択 `Enabled` 送信されるすべての状態変更 API リクエストをブロックします。 読み取り専用モードが無効になるまで、変更は保存されますが、送信されません。 データ転送を再度開始するには、次を選択します `Disabled`.<br/><br/>データベースがインスタンスの新しいコピーに移行されると（設定でストアの URL が変更されたときに検出）、読み取り専用モードが自動的に有効になります。<br/><br/>これは、以下のような実稼動インスタンスのコピーで使用するように設計されています _ステージング_ または _QA_、およびは実稼動インスタンスでは使用しないでください。<br/><br/>**_注意&#x200B;_**：の設定キャッシュをクリアする必要があります [!UICONTROL Read-Only Mode] を有効にします。 |

{style="table-layout:auto"}
