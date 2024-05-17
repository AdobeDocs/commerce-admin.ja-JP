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

（を使用） [!DNL Inventory Management]在庫がある出荷を 1 つ以上送信します。 必要に応じて追加の出荷を生成するには、推奨または手動で入力した数量およびソースを使用して、これらの手順を繰り返します。 この手順では、複数ソースのマーチャントが配送を送信する方法について詳しく説明します。 単一ソースのマーチャントは、以下の追加手順を行わずに配送を送信します（を参照）。 [出荷の作成](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} （コアユーザーガイドで説明）を参照してください。

出荷を作成する場合は、ソース選択アルゴリズムを使用して計算されたレコメンデーションを使用します。 これらの推奨事項に従って使用するか、ソースごとの金額を設定して、カスタム出荷を生成します。 注文ごとに出荷する在庫を制御し、差し引く金額を設定し、1 つ以上の出荷を送信し、在庫とバックオーダーを在庫が使用可能な状態で配信します。 受注の各明細品目に対して、ソース数量から控除する金額を入力します。

部分出荷の送信先は、次の場合があります。

- 在庫到着時にバックオーダーを履行

- ソース間の在庫控除残高

出荷を入力すると、手持在庫数量から入力済金額が差し引かれます。 事実上、予約は実際の数量控除に変換されます。

## 出荷の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 注文を見つけて、表示モードで開きます。

1. 注文が支払われ、請求が行われ、出荷準備が整ったら、 **[!UICONTROL Ship]**.

1. ソースごとに商品を送信するには、「ソースの選択」を完了します。

   - 配送に関する推奨事項を表示するには、 **[!UICONTROL Source Selection Algorithm]** アルゴリズムを選択します。

     | アルゴリズム | 説明 |
     |--|--|
     | [ソースの優先度](source-priority-algorithm.md) | 在庫に割り当てられたソースのオーダーに従って、ソースからの出荷が推奨されます。 |
     | [距離の優先度](distance-priority-algorithm.md) | 物理的な距離または最短時間に基づいて、出荷先住所に最も近いソースからの出荷を推奨します。 |

     >[!IMPORTANT]
     >
     >配送およびルートに距離優先アルゴリズムを使用している場合、選択したのデータは返されません [計算モード](distance-priority-algorithm.md) （運転、自転車、またはウォーキング）出荷の場合、SSA はデフォルトで「ソース優先度」に設定されます。 を設定することをお勧めします [在庫あたりのソースの優先度](stocks-prioritize-sources.md).


   - の場合  **[!UICONTROL Select a Source to Ship from]**、出荷を送信するソースを選択します。

   - 行項目ごとに、推奨金額を保持するか、 **[!UICONTROL Qty to Deduct]**. この値は、選択したソースの在庫から差し引かれる金額を指定します。

   - クリック **[!UICONTROL Proceed to Shipment]**.

     ![ソースを選択して数量を入力します](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. をレビュー _[!UICONTROL New Shipment]_必要に応じてページに移動して、さらに変更を加えます。

   この _[!UICONTROL Inventory]_セクションには、ソース、製品出荷、合計受注数量および出荷数量が表示されます。

   ![出荷の在庫詳細（部分出荷など）](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. クリック **[!UICONTROL Submit Shipment]** を完了します。
