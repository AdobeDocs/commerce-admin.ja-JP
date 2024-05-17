---
title: 在庫の在庫ソースの優先順位付け
description: 出荷および在庫の控除を決定する際に使用する、ソースを上から下に優先して並べ替える方法を説明します。
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 在庫のソースの優先順位付け

追加後 [ソース](sources-manage.md) に [在庫](stocks-manage.md)注文をフルフィルメントするために、それらのソースを上から下に優先して配置します。 Source Selection Algorithm （SSA; ソース選択アルゴリズム）は、出荷および在庫控除を決定する際に、この順序を使用してアルゴリズム Priority を提供します。

在庫のソース優先度は、商品インベントリの編集時に割り当てられたソースには影響しません。

この例では、英国在庫には、ロンドンの 1 つの店舗と 2 つの倉庫およびベルリンの倉庫に対して順不同で割り当てられたソースがあります。

![優先順位付けの前のソース順序](assets/inventory-priority-before.png){width="350" zoomable="yes"}

商人は、より大きなベルリンの倉庫、ロンドンの倉庫、ロンドンのオーバーフロー場所、そして最後にロンドンのストアフロントから出荷を優先することを好みます。 順序を変更するには、エントリを目的の順序にドラッグ&amp;ドロップします。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. で在庫を開きます _編集_ モード。

1. を展開します。 _[!UICONTROL Sources]_必要に応じて、タブをクリックします。

1. 使用方法 ![並べ替えアイコン](assets/icon-sort.png) ソースを上（最初）から下（最後）にドラッグ&amp;ドロップします。

   この注文は、注文を出荷する際に重要です。 SSA では、ソースの順序に基づいて出荷を推奨しています

1. クリック **[!UICONTROL Save & Continue]** 変更を保存します。

![優先順位付け後のソース順序](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
