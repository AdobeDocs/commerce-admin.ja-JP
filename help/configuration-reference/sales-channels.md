---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: 次のページで設定を確認します： [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] コマース管理のページ。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

これらの設定は、 [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) がインストールされている。

![Sales Channel設定](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | グローバル | オプション：<br/><br/>**`Once Daily`**：ストアのアクティビティ履歴を 1 日に 1 回クリアするには、このオプションを選択します。<br/><br/>**`Once Weekly`**：ストアのアクティビティ履歴を毎週 1 回クリアするには、このオプションを選択します。<br/><br/>**`Once Monthly`**: （デフォルト）このオプションを選択すると、ストアのアクティビティ履歴が毎月 1 回クリアされます。 |
| [!UICONTROL Background Tasks (CRON) Source] | グローバル | 選択 `Magento CRON` を指定する [!DNL Amazon Sales Channel] は、Commerce の cron 設定を使用して、Amazon Seller Central との通信間隔とデータ同期間隔を決定します。 |
| [!UICONTROL Enable Debug Logging] | グローバル | 選択 `Enabled` トラブルシューティングが必要な場合に、追加の同期データを収集する。<br/><br/>このオプションはデフォルトで無効になっており、ログの記録がパフォーマンスに悪影響を与えるので、トラブルシューティングに必要な場合にのみ有効にする必要があります。 トラブルシューティング用に有効にした場合、完了時に無効にする必要があります。<br/><br/>**_注意&#x200B;_**:AmazonSales Channelのログは、 `/var/log/channel_amazon.log` ファイルに保存し、 [開発者モード](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | グローバル | 選択 `Enabled` をクリックして、送信状態が変化するすべての API リクエストをブロックします。 潜在的な変更は、読み取り専用モードが無効になるまで保存されますが、送信されません。 データ転送を再度開始するには、「 」を選択します。 `Disabled`.<br/><br/>データベースがインスタンスの新しいコピーに移行された場合（設定でストアの URL が変更された場合に検出）、読み取り専用モードが自動的に有効になります。<br/><br/>これは、実稼動インスタンスのコピーで使用するために設計されています。例： _ステージング_ または _QA_、およびは、実稼動インスタンスでは使用しないでください。<br/><br/>**_注意&#x200B;_**：の設定キャッシュをクリアする必要があります。 [!UICONTROL Read-Only Mode] を有効にします。 |

{:style=&quot;table-layout:auto&quot;}
