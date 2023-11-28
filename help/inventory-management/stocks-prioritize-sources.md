---
title: 在庫の在庫ソースを優先順位付けする
description: 出荷と在庫控除を決定する際に使用する、優先度の上から下へのソースの配置方法を説明します。
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 在庫のソースを優先順位付けする

追加後 [ソース](sources-manage.md) から [在庫](stocks-manage.md)を使用する場合、オーダーを実行する際に、上から下にソースを並べ替えます。 ソース選択アルゴリズム (SSA) は、出荷と在庫控除を決定する際に、この受注を使用してアルゴリズム優先度を提供します。

在庫に対するソースの優先度は、製品在庫の編集時に割り当てられたソースに影響を与えません。

この例では、英国の在庫には、1 つの店舗と 2 つのロンドンの倉庫、およびベルリンの倉庫に順不同で割り当てられたソースがあります。

![優先順位付け前のソースの順序](assets/inventory-priority-before.png){width="350" zoomable="yes"}

この商人は、大規模なベルリン倉庫、ロンドン倉庫、ロンドンオーバーフロー場所、最後にロンドンの店舗から出荷を優先させることを希望しています。 順序を変更するには、エントリをドラッグして目的の順序にドロップします。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. で在庫を開きます。 _編集_ モード。

1. を展開します。 _[!UICONTROL Sources]_タブに表示されます。

1. 用途 ![並べ替えアイコン](assets/icon-sort.png) をクリックして、ソースを上（最初）から下（最後）の優先順位にドラッグ&amp;ドロップします。

   この注文は、発送注文時に重要です。 SSA は、ソースの注文に基づいて出荷を推奨します

1. クリック **[!UICONTROL Save & Continue]** をクリックして変更を保存します。

![優先順位付け後のソースの順序](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
