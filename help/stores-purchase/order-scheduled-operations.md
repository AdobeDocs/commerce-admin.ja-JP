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

使用方法 [Cron](../systems/cron.md) ジョブ：次のオーダー処理タスクをスケジュールします。

![注文グリッド](./assets/orders-grid.png){width="700" zoomable="yes"}

## 保留中の支払注文の有効期間を設定します

支払いが保留されている注文の有効期間は、 _注文 Cron 設定_ 設定。 デフォルト値は 480 分（8 時間）に設定されています。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** セクションで選択 **[!UICONTROL Sales]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Orders Cron Settings]** セクション。

   ![注文 Cron 設定](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Pending Payment Order Lifetime (minutes)]**：保留中の支払いが期限切れになるまでの分数を入力します。

1. クリック **[!UICONTROL Save Config]**.

## スケジュールされたグリッドの更新とインデックス再作成を有効にする

「グリッド設定」構成では、次の受注管理グリッドが更新され、スケジュールに従ってデータの索引が再作成されます。 [Cron](../systems/cron.md):

- [注文件数](orders.md#orders-workspace)
- [請求書](invoices.md)
- [出荷](shipments.md)
- [クレジットメモ](credit-memos.md)

これらのタスクをスケジュールすることで、データの保存時に発生するロックを回避し、処理時間を短縮できます。 有効にした場合、更新はスケジュールされた cron ジョブ中にのみ行われます。 最良の結果を得るには、Cron が 1 分ごとに 1 回実行されるように設定する必要があります。

**_更新とインデックス再作成を有効にするには：_**

条件 [実稼動モード](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) （クラウドインフラストラクチャー上のAdobe Commerceで使用されるデフォルトモード）が有効になっている場合は、次のコマンドを実行します。

``bin/magento config:set dev/grid/async_indexing 1``

条件 [デフォルトモード](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) が有効になっている場合は、以下の手順を実行します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** セクションで選択 **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Grid Settings]** セクション。

1. を設定 **[!UICONTROL Asynchronous Indexing]** 対象： `Enable`.

   ![グリッド設定](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.
