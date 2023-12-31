---
title: ソースの優先度アルゴリズムの設定
description: 在庫内で割り当てられたソースの順序に使用するソースの優先順位を設定して、レコメンデーションをおこなう方法について説明します。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# ソースの優先度アルゴリズムの設定

カスタム在庫には、販売するソースの割り当て済みリストが含まれ、ストアフロントを通じて使用可能な製品在庫を出荷します。 このアルゴリズムは、在庫内で割り当てられたソースの順序を使用して、レコメンデーションをおこないます。

実行時に、アルゴリズムは次の操作をおこないます。

- 上部から始まる在庫レベルで、設定された順序でソースを処理します。

- リスト内のオーダー、使用可能数量、オーダー数量に基づいて、製品ごとの出荷およびソースに数量を推奨します。

- 注文の出荷が入力されるまで、リストの下方に進みます

- リストに無効なソースが見つかった場合、そのソースをスキップします

設定するには、オーダーを実行する際に、上から下にソースを並べ替えます。 ソース選択アルゴリズム (SSA) は、出荷と在庫控除を決定する際に、この受注を使用してアルゴリズム優先度を提供します。 詳しくは、 [在庫のソースの優先順位付け](stocks-prioritize-sources.md).

## ソースの優先度の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. 在庫を編集モードで開き、 _[!UICONTROL Sources]_領域。

1. クリック **[!UICONTROL Assign Sources]**.

1. Adobe Analytics の _[!UICONTROL Assign Sources]_表示し、必要なソースのチェックボックスを選択して、**[!UICONTROL Done]**ソースを在庫に割り当てます。

>[!NOTE]
>
>を使用する場合、 [距離の優先度](distance-priority-algorithm.md) ルートとデータが選択したに対して返されない場合の、発送のアルゴリズム [計算モード](distance-priority-algorithm.md) 出荷の場合、SSA は「ソース優先度」を使用してデフォルト設定されます。

![優先順位付け後のソースの順序](assets/inventory-stock-priority-after.png)

| アイコン | 説明 |
|----------------------------------------------|----------------------------------------------------------------|
| ![アイコンをドラッグ&amp;ドロップして優先度を設定](assets/icon-drag-and-drop-action.png) | 優先度に従ってソースをドラッグ&amp;ドロップするには、を使用します。 |
| ![ソースの割り当てを解除するには、アイコンをクリックします](assets/icon-delete-action.png) | 在庫へのソースの割り当て解除 |
