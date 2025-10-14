---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Commerce Admin の [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] ページで設定を確認します。
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

これらの設定は、のインストール時 [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=ja) 使用できます。

![Sales Channelの設定 &#x200B;](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | グローバル | オプション：<br/><br/>**`Once Daily`**：ストアのアクティビティ履歴を 1 日に 1 回クリアするには、このオプションを選択します。<br/><br/>**`Once Weekly`**：このオプションを選択すると、ストアのアクティビティ履歴が毎週 1 回消去されます。<br/><br/>**`Once Monthly`**: （デフォルト）このオプションを選択すると、ストアのアクティビティ履歴が毎月 1 回クリアされます。 |
| [!UICONTROL Background Tasks (CRON) Source] | グローバル | 「`Magento CRON`」を選択すると、[!DNL Amazon Sales Channel] がCommerce cron 設定を使用してAmazon Seller Central との通信およびデータ同期間隔を決定します。 |
| [!UICONTROL Enable Debug Logging] | グローバル | トラブルシューティングが必要な場合に、追加の同期データを収集する `Enabled` を選択します。<br/><br/> このオプションはデフォルトでは無効になっており、トラブルシューティングに必要な場合にのみ有効にしてください。継続したログはパフォーマンスに悪影響を及ぼすからです。 トラブルシューティングが有効な場合は、完了時に無効にする必要があります。 |
| [!UICONTROL Read-Only Mode] | グローバル | `Enabled` を選択すると、送信されるすべての状態変更 API リクエストがブロックされます。 読み取り専用モードが無効になるまで、変更は保存されますが、送信されません。 データ転送を再度開始するには、「`Disabled`」を選択します。<br/><br/> データベースがインスタンスの新しいコピーに移行されると（設定でストアの URL が変更されたときに検出されます）、読み取り専用モードが自動的に有効になります。<br/><br/> これは、_ステージング_ や _QA_ など、実稼動インスタンスのコピーで使用するように設計されており、実稼動インスタンスでは使用しないでください。<br/><br/>**_メモ&#x200B;_**:[!UICONTROL Read-Only Mode] を有効にするには、設定キャッシュをクリアする必要があります。 |

{style="table-layout:auto"}
