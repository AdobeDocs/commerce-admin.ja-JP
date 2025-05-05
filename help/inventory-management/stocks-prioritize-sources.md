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

[ ソース ](sources-manage.md) を [stock](stocks-manage.md) に追加した後、注文をフルフィルメントするために、それらのソースを上から下に優先して配置します。 Source Selection Algorithm （SSA）は、出荷および在庫控除を決定する際に、この順序を使用してアルゴリズム Priority を提供します。

在庫のソース優先度は、商品インベントリの編集時に割り当てられたソースには影響しません。

この例では、英国在庫には、ロンドンの 1 つの店舗と 2 つの倉庫およびベルリンの倉庫に対して順不同で割り当てられたソースがあります。

![ 優先順位付けの前のSourceの順序 ](assets/inventory-priority-before.png){width="350" zoomable="yes"}

商人は、より大きなベルリンの倉庫、ロンドンの倉庫、ロンドンのオーバーフロー場所、そして最後にロンドンのストアフロントから出荷を優先することを好みます。 順序を変更するには、エントリを目的の順序にドラッグ&amp;ドロップします。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Inventory]_/**[!UICONTROL Stocks]**&#x200B;に移動します。

1. 在庫を _編集_ モードで開きます。

1. 必要に応じて、「_[!UICONTROL Sources]_」タブを展開します。

1. ![ 並べ替えアイコン ](assets/icon-sort.png) を使用して、ソースを上（最初）から下（最後）の優先度にドラッグ&amp;ドロップします。

   この注文は、注文を出荷する際に重要です。 SSA では、ソースの順序に基づいて出荷を推奨しています

1. 「**[!UICONTROL Save & Continue]**」をクリックして、変更を保存します。

![ 優先順位付け後のSourceの順序 ](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
