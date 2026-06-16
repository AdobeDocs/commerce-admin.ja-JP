---
title: Source Priority Algorithmの設定
description: 在庫に割り当てられたソースの順序に使用されるソースの優先度を設定してレコメンデーションを行う方法について説明します。
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Source Priority Algorithmの設定

カスタム在庫には、ストアフロントを通じて利用可能な製品在庫を販売および出荷するために、割り当てられたソースのリストが含まれます。 このアルゴリズムは、在庫に割り当てられたソースの順序にもとづいて、商品をレコメンデーションします。

実行すると、アルゴリズムは次のようになります。

- 最上位から始まる在庫レベルで、設定されたソースの順序を使用します

- リスト内の注文、使用可能な数量および注文数量に基づいて、製品ごとに出荷および調達する数量を提案します

- 注文の出荷が完了するまでリストを続行します

- リスト内に無効なソースが見つかった場合はスキップする

注文を処理できるように、ソースを上から下に優先的に配置します。 Source Selection Algorithm （SSA）は、出荷と在庫差し引きを決定する際に、この順序を使用してアルゴリズムの優先度を提供します。 [Stockのソースの優先順位付けを参照](stocks-prioritize-sources.md)。

## ソースの優先度の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**&#x200B;に移動します。

1. ストックを編集モードで開き、_[!UICONTROL Sources]_領域に移動します。

1. **[!UICONTROL Assign Sources]**&#x200B;をクリックします。

1. _[!UICONTROL Assign Sources]_ビューで、必要なソースのチェックボックスを選択し、**[!UICONTROL Done]**をクリックしてソースを在庫に割り当てます。

>[!NOTE]
>
>配送に[Distance Priority](distance-priority-algorithm.md) アルゴリズムを使用する場合、配送に選択した[計算モード ](distance-priority-algorithm.md) （運転、自転車、またはウォーキング）にルートとデータが返されない場合、SSAはデフォルトでSource Priorityを使用します。

![優先順位付け後のSource注文](assets/inventory-stock-priority-after.png)

| アイコン | 説明 |
|----------------------------------------------|----------------------------------------------------------------|
| ![ アイコンをドラッグ&amp;ドロップして優先順位を設定](assets/icon-drag-and-drop-action.png) | を使用すると、優先度に応じてソースをドラッグ&amp;ドロップできます。 |
| ![ クリックアイコンでソースの割り当てを解除する](assets/icon-delete-action.png) | ソースを在庫に割り当て解除します。 |
