---
title: 在庫トックの追加
description: 在庫を追加し、販売チャネル（web サイト）にソースをマッピングして、販売可能な数量と製品インベントリへの直接リンクを提供する方法を説明します。
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# 在庫を追加

在庫は、ソースを販売チャネル（または web サイト）にマッピングし、販売可能な数量と製品インベントリへの直接リンクを提供します。

カスタムストックを作成する場合は、web サイトとソースを割り当てます。 ソースには、有効なソースと無効なソースを含めることができます。 例えば、在庫に倉庫を追加し、在庫を管理して出荷を完了するための場所を開く準備を行うことができます。

ソースを追加した後、ソースの順序を上（最初）から下（最後）に優先順位付けする必要があります。 この注文は、注文出荷中の推奨事項に影響を与えます。

![新規在庫](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## 在庫在庫の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. クリック **[!UICONTROL Add New Stock]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General]** セクションを選択して一意のを入力 **[!UICONTROL Name]** 新しい在庫を識別します。

   ![一般的なストックオプション](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Sales Channels]** 「」セクションを選択し、 **[!UICONTROL Websites]** この在庫が利用可能な場所。

   マルチサイトインストールの場合は、Ctrl キー（PC）または Command キー（Mac）を押しながら、各 Web サイトをクリックします。

   >[!NOTE]
   >
   >別の在庫に割り当てられている web サイトまたは販売チャネルを選択した場合、その在庫から割り当てられません。 カスタム在庫に割り当てられていないSales Channelは、デフォルト在庫に割り当てられます。

   ![在庫のSales Channelオプション](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Sources]** デフォルト以外の在庫の場合は、を参照し、次の操作を行います。

   - クリック **[!UICONTROL Assign Sources]**.

   ![割り当てられたソース](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - 在庫に割り当てるすべてのソースのチェックボックスをオンにします。

   >[!IMPORTANT]
   >
   >同じソースを複数の在庫に割り当てると、そのソースに割り当てられた製品が売れ過ぎになる可能性があります。

   - クリック **[!UICONTROL Done]**.

     追加されたソースが「割り当てられたソース」に表示されます。

     ![Stock へのソースの割り当て](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. 使用方法 ![並べ替えアイコン](assets/icon-sort.png) ソースを上（最初）から下（最後）にドラッグ&amp;ドロップします。

   注文を出荷する際には、ソース注文が重要です。

   ![割り当てられたソースの例](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. 日 _[!UICONTROL Save]_（![メニュー矢印](../assets/icon-menu-down-arrow-red.png)） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## フィールドの説明

| フィールド | 説明 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | 在庫名。 例： `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | は、 [範囲](../getting-started/websites-stores-views.md#scope-settings) 在庫を特定の web サイトに割り当てることにより、在庫を _販売チャネル_. 在庫ごとに 1 つ以上の web サイトを選択します。 各 web サイトは、1 つの在庫にのみ割り当てることができます。 |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | この在庫に在庫ソースを割り当てます。 カスタムソースをデフォルトの在庫に割り当てることはできません。 |
| [!UICONTROL Assigned Sources] | 割り当てられたソースのリスト。 を使用してソースをドラッグ&amp;ドロップ ![並べ替えアイコン](assets/icon-sort.png) 注文のフルフィルメントと配送のための優先順位付けされた注文に。<br/><br/>**[!UICONTROL Code]**- ソースの一意のコード ID。<br/>**[!UICONTROL Name]** - ソースの名前の説明。<br/>**[!UICONTROL Unassign]**– を使用して、割り当てられたソースを在庫から削除します ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png). |
