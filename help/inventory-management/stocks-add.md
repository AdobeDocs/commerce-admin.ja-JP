---
title: 在庫トックの追加
description: 在庫を追加し、ソースを販売チャネル（Web サイト）にマッピングし、販売可能数量と製品在庫への直接リンクを提供する方法を説明します。
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# 在庫の追加

在庫は、販売チャネル（または Web サイト）にソースをマッピングし、販売可能な数量と製品在庫への直接リンクを提供します。

カスタム在庫を作成する場合は、Web サイトとソースを割り当てます。 ソースには、有効/無効のソースを含めることができます。 例えば、在庫に倉庫を追加して、在庫を管理し、出荷を完了するための場所を開く準備を行うことができます。

ソースを追加した後、ソースの順序を上（最初）から下（最後）に優先する必要があります。 この注文は、注文出荷時のレコメンデーションに影響します。

![新しい在庫](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## 在庫を追加

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. クリック **[!UICONTROL Add New Stock]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General]** セクションを開き、一意の **[!UICONTROL Name]** をクリックして、新しい在庫を特定します。

   ![一般的な在庫オプション](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Sales Channels]** 」セクションで、 **[!UICONTROL Websites]** この在庫がある場所です。

   マルチサイトインストールの場合は、Ctrl キー (PC) または Command キー (Mac) を押しながら各 Web サイトをクリックします。

   >[!NOTE]
   >
   >別の在庫に割り当てられた Web サイトまたは販売チャネルを選択した場合、その在庫から割り当てられていません。 カスタムSales Channelに割り当てられていない在庫は、デフォルト在庫に割り当てられます。

   ![Sales Channelの在庫オプション](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Sources]** 「 」セクションに移動して、デフォルト以外の在庫に対して次の操作を実行します。

   - クリック **[!UICONTROL Assign Sources]**.

   ![割り当てられたソース](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - 在庫に割り当てるすべてのソースのチェックボックスをオンにします。

   >[!IMPORTANT]
   >
   >同じソースを複数の在庫に割り当てると、そのソースに割り当てられた製品が過剰に販売される可能性があります。

   - クリック **[!UICONTROL Done]**.

     追加されたソースは、「割り当てられたソース」に表示されます。

     ![在庫にソースを割り当て](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. 用途 ![並べ替えアイコン](assets/icon-sort.png) をクリックして、ソースを上（最初）から下（最後）の優先順位にドラッグ&amp;ドロップします。

   発注時にソースの注文が重要です。

   ![割り当てられたソースの例](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. 次の日： _[!UICONTROL Save]_(![メニュー矢印](../assets/icon-menu-down-arrow-red.png)) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## フィールドの説明

| フィールド | 説明 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | 在庫の名前。 例： `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | を定義します。 [範囲](../getting-started/websites-stores-views.md#scope-settings) 在庫を特定のウェブサイトに割り当てることによって、在庫の _営業チャネル_. 1 つの在庫につき 1 つ以上の Web サイトを選択します。 各 Web サイトは 1 つの在庫にのみ割り当てることができます。 |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | 在庫ソースをこの在庫に割り当てます。 カスタムソースは、デフォルトの在庫に割り当てることはできません。 |
| [!UICONTROL Assigned Sources] | 割り当てられたソースのリスト。 次を使用してソースをドラッグ&amp;ドロップ ![並べ替えアイコン](assets/icon-sort.png) を、注文の受け渡しと発送の優先順位付けされた注文に追加します。<br/><br/>**[!UICONTROL Code]**— ソースの一意のコード ID。<br/>**[!UICONTROL Name]**  — ソースの名前の説明。<br/>**[!UICONTROL Unassign]**— 次を使用して、割り当てられたソースを在庫から削除します： ![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png). |
