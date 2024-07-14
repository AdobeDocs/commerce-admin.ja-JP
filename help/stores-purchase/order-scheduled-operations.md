---
title: スケジュール済み注文操作
description: この機能をサポートするスケジュール済み注文操作および注文 cron 設定について説明します。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# スケジュール済み注文操作

[Cron](../systems/cron.md) ジョブを使用して、次の注文処理タスクをスケジュールします。

![ 注文グリッド ](./assets/orders-grid.png){width="700" zoomable="yes"}

## 保留中の支払注文の有効期間を設定します

支払いが保留されている注文の有効期間は、_注文 Cron 設定_ 設定によって決まります。 デフォルト値は 480 分（8 時間）に設定されています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」セクションを展開し、その下 **[!UICONTROL Sales]** 選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Orders Cron Settings]**」セクションを展開します。

   ![ 注文 Cron 設定 ](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Pending Payment Order Lifetime (minutes)]**：保留中の支払いが期限切れになるまでの分数を入力します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## スケジュールされたグリッドの更新とインデックス再作成を有効にする

グリッド設定の構成スケジュールは、次の Order Management グリッドを更新し、[Cron](../systems/cron.md) がスケジュールどおりにデータのインデックスを再作成します。

- [注文件数](orders.md#orders-workspace)
- [請求書](invoices.md)
- [出荷](shipments.md)
- [クレジットメモ](credit-memos.md)

これらのタスクをスケジュールすることで、データの保存時に発生するロックを回避し、処理時間を短縮できます。 有効にした場合、更新はスケジュールされた cron ジョブ中にのみ行われます。 最良の結果を得るには、Cron が 1 分ごとに 1 回実行されるように設定する必要があります。

**_更新とインデックス再作成を有効にするには：_**

[ 実稼動モード ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) （クラウドインフラストラクチャ上のAdobe Commerceで使用されるデフォルトのモード）が有効な場合は、次のコマンドを実行します。

``bin/magento config:set dev/grid/async_indexing 1``

[ デフォルトモード ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) が有効な場合、次の手順を実行します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」セクションを展開し、「**[!UICONTROL Developer]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Grid Settings]**」セクションを展開します。

1. **[!UICONTROL Asynchronous Indexing]** を `Enable` に設定します。

   ![ グリッド設定 ](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。
