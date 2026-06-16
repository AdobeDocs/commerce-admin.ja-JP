---
title: スケジュールされた注文操作
description: この機能をサポートするスケジュールされた注文操作と注文のcron設定について説明します。
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
TQID: https://experienceleague.adobe.com/pViPmBFGErjXeFyvBNBVuJiw8Pn51JIGkeZ2mJAf72M
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 284
ht-degree: 0%

---

# スケジュールされた注文操作

[Cron](../systems/cron.md) ジョブを使用して、次の注文処理タスクをスケジュールします。

![注文グリッド ](./assets/orders-grid.png){width="700" zoomable="yes"}

## 保留中の支払い注文の有効期間の設定

保留中の支払いを伴う注文の有効期間は、_注文Cron設定_&#x200B;設定によって決まります。 デフォルト値は480分（8時間）に設定されています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」セクションを展開し、下の「**[!UICONTROL Sales]**」を選択します。

1. **[!UICONTROL Orders Cron Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![Cron設定を注文](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Pending Payment Order Lifetime (minutes)]**&#x200B;の場合、保留中の支払いが期限切れになるまでの分数を入力します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## スケジュールされたグリッドの更新とインデックス再作成を有効にする

グリッド設定の設定では、次の注文管理グリッドに更新がスケジュールされ、[Cron](../systems/cron.md)のスケジュールに従ってデータのインデックスが再作成されます。

- [注文](orders.md#orders-workspace)
- [請求書](invoices.md)
- [発送数](shipments.md)
- [クレジットメモ](credit-memos.md)

これらのタスクをスケジュールすることで、データの保存時に発生するロックを回避し、処理時間を短縮できます。 有効にすると、更新はスケジュールされたcron ジョブ中にのみ行われます。 最良の結果を得るには、Cronを1分に1回実行するように設定する必要があります。

**_更新とインデックス再作成を有効にするには:_**

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [実稼動モード ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) （クラウドインフラストラクチャ上のAdobe Commerceで使用されるデフォルトモード）が有効になっている場合は、次のコマンドを実行します。

`bin/magento config:set dev/grid/async_indexing 1`

[ デフォルトモード ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode)が有効になっている場合は、次の手順を実行します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]** セクションを展開し、**[!UICONTROL Developer]**&#x200B;を選択します。

1. **[!UICONTROL Grid Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Asynchronous Indexing]**&#x200B;を`Enable`に設定します。

   ![ グリッド設定](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。
