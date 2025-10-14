---
title: Source優先度アルゴリズムの設定
description: レコメンデーションを行うために、在庫の割り当てられたソースの順序に使用されるソース優先度を設定する方法を説明します。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Source優先度アルゴリズムの設定

カスタム在庫には、ストアフロントを通じて利用可能な製品在庫を販売および出荷するためのソースの割り当てられたリストが含まれています。 このアルゴリズムでは、在庫にある割り当てられたソースの順序を使用してレコメンデーションを行います。

実行時のアルゴリズムは次のとおりです。

- 上位から在庫レベルでソースの設定順序を処理します

- リスト内のオーダー、有効数量およびオーダー数量に基づいて、製品ごとに出荷数量およびソースを推奨します。

- 注文出荷が入力されるまでリストの下の方に進みます

- リスト内に無効なソースが見つかった場合はスキップします

設定するには、注文をフルフィルメントするために、それらのソースを上から下に優先して並べ替えます。 Source Selection Algorithm （SSA）は、出荷および在庫控除を決定する際に、この順序を使用してアルゴリズム Priority を提供します。 [&#x200B; 在庫のソースの優先順位付け &#x200B;](stocks-prioritize-sources.md) を参照してください。

## ソースの優先度の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/**[!UICONTROL Inventory]**/**[!UICONTROL Stocks]** に移動します。

1. 在庫を編集モードで開き、_[!UICONTROL Sources]_&#x200B;の領域に移動します。

1. 「**[!UICONTROL Assign Sources]**」をクリックします。

1. _[!UICONTROL Assign Sources]_&#x200B;表示で、必要なソースのチェックボックスを選択し、「**[!UICONTROL Done]**」をクリックして、在庫にソースを割り当てます。

>[!NOTE]
>
>配送に [Distance Priority](distance-priority-algorithm.md) アルゴリズムを使用する際に、配送に対して選択した [Computation mode](distance-priority-algorithm.md) （運転、自転車、歩行）でルートとデータが返されない場合、SSA はデフォルトでSource Priority を使用します。

![&#x200B; 優先順位付け後のSourceの順序 &#x200B;](assets/inventory-stock-priority-after.png)

| アイコン | 説明 |
|----------------------------------------------|----------------------------------------------------------------|
| ![&#x200B; アイコンをドラッグ&amp;ドロップして優先度を設定 &#x200B;](assets/icon-drag-and-drop-action.png) | を使用して、優先度に従ってソースをドラッグ&amp;ドロップします。 |
| ![&#x200B; ソースの割り当てを解除する場合はアイコンをクリック &#x200B;](assets/icon-delete-action.png) | 在庫へのソースの割り当てを解除する。 |
