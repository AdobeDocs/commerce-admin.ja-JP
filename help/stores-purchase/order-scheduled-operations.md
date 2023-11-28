---
title: 予定オーダー操作
description: この機能をサポートする、スケジュールされた注文操作と注文 Cron 設定について説明します。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 予定オーダー操作

用途 [Cron](../systems/cron.md) ジョブを使用して、次の順序処理タスクをスケジュールします。

![注文グリッド](./assets/orders-grid.png){width="700" zoomable="yes"}

## 保留中の支払注文の有効期間を設定

保留中の支払いを含む注文の有効期間は、 _Cron 設定を注文_ 設定。 デフォルト値は 480 分（8 時間）に設定されています。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** 「 」セクションで「 」を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Orders Cron Settings]** 」セクションに入力します。

   ![Cron 設定を注文](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Pending Payment Order Lifetime (minutes)]**」には、保留中の支払いが期限切れになるまでの時間（分）を入力します。

1. クリック **[!UICONTROL Save Config]**.

## スケジュールされたグリッドの更新とインデックス再作成を有効にする

「グリッド設定」構成では、次の Order Management グリッドに対して更新がスケジュールされ、次の日付でスケジュールされたデータに対して再インデックスが実行されます。 [Cron](../systems/cron.md):

- [購入回数](orders.md#orders-workspace)
- [請求書](invoices.md)
- [出荷](shipments.md)
- [クレジットメモ](credit-memos.md)

これらのタスクをスケジュールすると、データの保存時に発生するロックを回避し、処理時間を短縮できます。 有効にすると、すべての更新は、スケジュールされた Cron ジョブ中にのみおこなわれます。 最適な結果を得るには、Cron を毎分 1 回実行するように設定する必要があります。

**_更新とインデックス再作成を有効にするには：_**

条件 [実稼動モード](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) ( クラウドインフラストラクチャ上のAdobe Commerceで使用されるデフォルトのモード ) が有効になっている場合は、次のコマンドを実行します。

``bin/magento config:set dev/grid/async_indexing 1``

条件 [デフォルトモード](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) を有効にするには、次の手順を実行します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** 「 」セクションで「 」を選択します。 **[!UICONTROL Developer]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Grid Settings]** 」セクションに入力します。

1. 設定 **[!UICONTROL Asynchronous Indexing]** から `Enable`.

   ![グリッド設定](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.
