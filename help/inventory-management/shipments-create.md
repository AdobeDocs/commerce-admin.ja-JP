---
title: 複数ソース出荷の作成
description: 複数ソースのマーチャントが配送を作成および送信する方法を説明します。
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 複数ソース出荷の作成

[!DNL Inventory Management] を使用する場合は、在庫があるように 1 つ以上の出荷を送信します。 必要に応じて追加の出荷を生成するには、推奨または手動で入力した数量およびソースを使用して、これらの手順を繰り返します。 この手順では、複数ソースのマーチャントが配送を送信する方法について詳しく説明します。 単一ソースのマーチャントは、これらの追加手順を行わずに出荷を送信します（コアユーザーガイドの [ 出荷の作成 ](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} を参照）。

出荷品を作成する際は、計算されたレコメンデーションにSource選択アルゴリズムを使用します。 これらの推奨事項に従って使用するか、ソースごとの金額を設定して、カスタム出荷を生成します。 注文ごとに出荷する在庫を制御し、差し引く金額を設定し、1 つ以上の出荷を送信し、在庫とバックオーダーを在庫が使用可能な状態で配信します。 受注の各明細品目に対して、ソース数量から控除する金額を入力します。

部分出荷の送信先は、次の場合があります。

- 在庫到着時にバックオーダーを履行

- ソース間の在庫控除残高

出荷を入力すると、手持在庫数量から入力済金額が差し引かれます。 事実上、予約は実際の数量控除に変換されます。

## 出荷の作成

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** に移動します。

1. 注文を見つけて、表示モードで開きます。

1. 注文が支払われ、請求が行われ、出荷準備が整ったら、「**[!UICONTROL Ship]**」をクリックします。

1. ソースごとに商品を送信するSourceの選択を行います。

   - 出荷レコメンデーションを表示するには、「**[!UICONTROL Source Selection Algorithm]**」をクリックし、アルゴリズムを選択します。

     | アルゴリズム | 説明 |
     |--|--|
     | [Sourceの優先度 ](source-priority-algorithm.md) | 在庫に割り当てられたソースのオーダーに従って、ソースからの出荷が推奨されます。 |
     | [ 距離の優先度 ](distance-priority-algorithm.md) | 物理的な距離または最短時間に基づいて、出荷先住所に最も近いソースからの出荷を推奨します。 |

     >[!IMPORTANT]
     >
     >出荷およびルートに「Distance Priority」アルゴリズムを使用し、出荷に対して選択した [Computation mode](distance-priority-algorithm.md) （運転、自転車、または歩行）のデータが返されない場合、SSA はデフォルトで「Source Priority」を設定します。 [ 在庫あたりのソースの優先度 ](stocks-prioritize-sources.md) も設定することをお勧めします。


   - **[!UICONTROL Select a Source to Ship from]**：出荷を送信するソースを選択します。

   - 各品目に対して、推奨金額を保持するか、**[!UICONTROL Qty to Deduct]** に特定の金額を入力します。 この値は、選択したソースの在庫から差し引かれる金額を指定します。

   - 「**[!UICONTROL Proceed to Shipment]**」をクリックします。

     ![Sourceを選択して数量を入力 ](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. _[!UICONTROL New Shipment]_ページをレビューし、必要に応じて追加の変更を入力します。

   「_[!UICONTROL Inventory]_」セクションには、ソース、製品出荷、合計受注数量および出荷数量が表示されます。

   ![ 部分出荷など、出荷の在庫詳細 ](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. 「**[!UICONTROL Submit Shipment]**」をクリックして完了します。
