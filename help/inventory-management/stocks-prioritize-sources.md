---
title: 在庫の在庫ソースを優先する
description: 出荷と在庫控除を決定する際に使用される、ソースを上から下に優先的に配置する方法について説明します。
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# 在庫のソースを優先する

[ ソース ](sources-manage.md)を[在庫](stocks-manage.md)に追加した後、注文を処理するために、これらのソースを上から下に並べます。 Source Selection Algorithm （SSA）は、出荷と在庫差し引きを決定する際に、この順序を使用してアルゴリズムの優先度を提供します。

在庫のソース優先度は、製品インベントリの編集時に割り当てられたソースには影響しません。

この例では、UK Stockには、ロンドンの店舗と2つの倉庫、ベルリンの倉庫に対して、注文に合わせて割り当てられたソースがあります。

![優先順位付け前のSource注文](assets/inventory-priority-before.png){width="350" zoomable="yes"}

商人は、ベルリンの大きな倉庫、ロンドンの倉庫、ロンドンのオーバーフロー場所、そして最後にロンドンのストアフロントから優先順位を付けた出荷を好みます。 順序を変更するには、エントリを目的の順序にドラッグ&amp;ドロップします。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**に移動します。

1. _編集_ モードで在庫を開きます。

1. 必要に応じて、_[!UICONTROL Sources]_タブを展開します。

1. ![並べ替えアイコン ](assets/icon-sort.png)を使用して、ソースを上（最初）から下（最後）にドラッグ&amp;ドロップします。

   この注文は、注文を配送する際に重要です。 SSAは、ソースの順序に基づいて出荷を推奨します

1. **[!UICONTROL Save & Continue]**&#x200B;をクリックして変更を保存します。

![優先順位付け後のSource注文](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
