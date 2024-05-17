---
title: ソースの優先度アルゴリズムの設定
description: レコメンデーションを行うために、在庫の割り当てられたソースの順序に使用されるソース優先度を設定する方法を説明します。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# ソースの優先度アルゴリズムの設定

カスタム在庫には、ストアフロントを通じて利用可能な製品在庫を販売および出荷するためのソースの割り当てられたリストが含まれています。 このアルゴリズムでは、在庫にある割り当てられたソースの順序を使用してレコメンデーションを行います。

実行時のアルゴリズムは次のとおりです。

- 上位から在庫レベルでソースの設定順序を処理します

- リスト内のオーダー、有効数量およびオーダー数量に基づいて、製品ごとに出荷数量およびソースを推奨します。

- 注文出荷が入力されるまでリストの下の方に進みます

- リスト内に無効なソースが見つかった場合はスキップします

設定するには、注文をフルフィルメントするために、それらのソースを上から下に優先して並べ替えます。 Source Selection Algorithm （SSA; ソース選択アルゴリズム）は、出荷および在庫控除を決定する際に、この順序を使用してアルゴリズム Priority を提供します。 参照： [在庫のソースの優先順位](stocks-prioritize-sources.md).

## ソースの優先度の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. 在庫を編集モードで開き、に移動します _[!UICONTROL Sources]_領域。

1. クリック **[!UICONTROL Assign Sources]**.

1. が含まれる _[!UICONTROL Assign Sources]_表示して、必要なソースのチェックボックスを選択し、**[!UICONTROL Done]**：在庫にソースを割り当てます。

>[!NOTE]
>
>使用する場合 [距離の優先度](distance-priority-algorithm.md) 選択したのルートとデータが返されない場合の配送用のアルゴリズム [計算モード](distance-priority-algorithm.md) （運転、自転車、または徒歩）出荷の場合、SSA はデフォルトでソース優先度を使用します。

![優先順位付け後のソース順序](assets/inventory-stock-priority-after.png)

| アイコン | 説明 |
|----------------------------------------------|----------------------------------------------------------------|
| ![アイコンをドラッグ&amp;ドロップして優先度を設定](assets/icon-drag-and-drop-action.png) | を使用して、優先度に従ってソースをドラッグ&amp;ドロップします。 |
| ![ソースの割り当てを解除するには、アイコンをクリック](assets/icon-delete-action.png) | 在庫へのソースの割り当てを解除する。 |
