---
title: 複数ソース出荷の作成
description: 複数ソースのマーチャントが出荷を作成および送信する方法を説明します。
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 複数ソース出荷の作成

を使用 [!DNL Inventory Management]、在庫がある場合は 1 つ以上の出荷を送信します。 必要に応じて追加の出荷を生成するには、推奨数量または手動で入力した数量とソースを使用して、これらの手順を繰り返します。 複数ソースのマーチャントが出荷を送る方法を詳しく説明します。 シングルソースのマーチャントは、追加の手順を行わずに出荷を送信します ( [出荷の作成](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} （コアユーザーガイド）。

出荷を作成する場合は、計算された推奨に対して「ソース選択アルゴリズム」を使用します。 これらの推奨事項に従って使用するか、ソースごとに金額を設定して、カスタム出荷を生成します。 各注文に対して出力在庫を管理し、金額を差し引くように設定し、1 つ以上の出荷を送信し、在庫が使用可能な場合は在庫と逆注文で納入します。 オーダー内の各品目に対して、ソース数量から差し引く金額を入力します。

一部出荷の送付先は次のとおりです。

- 在庫の到着時にバックオーダーを処理

- ソース間の在庫控除の残高

出荷を入力すると、手持在庫数量によって入力した金額が差し引かれます。 予約は実際の数量控除に変換されます。

## 出荷の作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 順序を探し、表示モードで開きます。

1. 注文が支払済みで請求済みで、出荷準備が整っている場合は、「 **[!UICONTROL Ship]**.

1. ソースごとに製品を送信するための「ソースの選択」を完了します。

   - 発送レコメンデーションを表示するには、 **[!UICONTROL Source Selection Algorithm]** をクリックし、アルゴリズムを選択します。

     | アルゴリズム | 説明 |
     |--|--|
     | [ソースの優先度](source-priority-algorithm.md) | 在庫に割り当てられたソースのオーダーに従って、ソースからの出荷を推奨します。 |
     | [距離の優先度](distance-priority-algorithm.md) | 配送先住所に最も近いソースからの出荷を、物理的な距離または最短時間に基づいて推奨します。 |

     >[!IMPORTANT]
     >
     >輸送とルートおよびデータに距離優先アルゴリズムを使用する場合、選択したに対しては戻りません [計算モード](distance-priority-algorithm.md) 出荷の場合、SSA はデフォルトで「ソース優先度」に設定されます。 また、 [在庫ごとのソースの優先順位](stocks-prioritize-sources.md).


   - の場合  **[!UICONTROL Select a Source to Ship from]**、出荷を送信するソースを選択します。

   - 行項目ごとに、推奨金額を保持するか、 **[!UICONTROL Qty to Deduct]**. この値は、選択したソースの在庫から控除される金額を指定します。

   - クリック **[!UICONTROL Proceed to Shipment]**.

     ![ソースを選択し、数量を入力します。](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. 以下を確認します。 _[!UICONTROL New Shipment]_ページに移動し、必要に応じて追加の変更を入力します。

   The _[!UICONTROL Inventory]_「 」セクションには、ソース、製品出荷、合計発注数量、出荷する数量が表示されます。

   ![出荷の在庫詳細（一部出荷の例）](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. クリック **[!UICONTROL Submit Shipment]** をクリックして完了します。
