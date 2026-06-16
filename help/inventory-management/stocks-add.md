---
title: 在庫タスクの追加
description: 販売可能な数量と製品在庫への直接リンクを提供して、在庫とマッピングソースを販売チャネル（web サイト）に追加する方法について説明します。
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
TQID: https://experienceleague.adobe.com/oP-H4hvUmNunTl-hThx4ytzC6qOXa1PhK4P1omwFBUg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 409
ht-degree: 0%

---

# ストックを追加

ストックマップでは、販売可能な数量や製品在庫への直接リンクを提供し、ソースを販売チャネル（またはweb サイト）にマッピングします。

カスタム在庫を作成する際には、web サイトとソースを割り当てます。 ソースには、有効なソースと無効なソースを含めることができます。 たとえば、在庫に倉庫を追加し、在庫を管理し、出荷を完了するために場所を開く準備をすることができます。

ソースを追加したら、ソースの順序を上（最初）から下（最後）に優先順位付けする必要があります。 この注文は、注文出荷時のレコメンデーションに影響します。

![新しいストック ](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## 在庫在庫の追加

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**に移動します。

1. **[!UICONTROL Add New Stock]**&#x200B;をクリックします。

1. **[!UICONTROL General]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、一意の&#x200B;**[!UICONTROL Name]**&#x200B;を入力して新しい在庫を識別します。

   ![一般的なストックオプション ](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. **[!UICONTROL Sales Channels]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、この在庫が利用可能な&#x200B;**[!UICONTROL Websites]**&#x200B;を選択します。

   マルチサイトインストールの場合は、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各Web サイトをクリックします。

   >[!NOTE]
   >
   >別の在庫に割り当てられたweb サイトまたは販売チャネルを選択した場合、その在庫から割り当てられていません。 カスタム在庫に割り当てられていない販売チャネルは、デフォルト在庫に割り当てられます。

   ![株式の販売チャネルオプション ](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. **[!UICONTROL Sources]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、デフォルト以外の在庫について次の操作を行います。

   - **[!UICONTROL Assign Sources]**&#x200B;をクリックします。

   ![割り当てられたソース ](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - 在庫に割り当てるすべてのソースのチェックボックスを選択します。

   >[!IMPORTANT]
   >
   >同じソースを複数の在庫に割り当てると、そのソースに割り当てられた商品が売り越される可能性があります。

   - **[!UICONTROL Done]**&#x200B;をクリックします。

     追加されたソースは、割り当てられたソースに表示されます。

     ![Stockへのソースの割り当て](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. ![並べ替えアイコン ](assets/icon-sort.png)を使用して、ソースを上（最初）から下（最後）にドラッグ&amp;ドロップします。

   注文を配送する際には、ソース注文が重要になります。

   ![割り当てられたソースの例](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. _[!UICONTROL Save]_（![ メニュー矢印](../assets/icon-menu-down-arrow-red.png)）メニューで、**[!UICONTROL Save & Close]**を選択します。

## フィールドの説明

| フィールド | 説明 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | 在庫の名前。 例：`UK Stock`、`US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | 特定のweb サイトに&#x200B;_販売チャネル_&#x200B;として在庫を割り当てることで、在庫の[範囲](../getting-started/websites-stores-views.md#scope-settings)を定義します。 在庫ごとに1つ以上のweb サイトを選択します。 各web サイトは1つの在庫にのみ割り当てることができます。 |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | 在庫ソースをこの在庫に割り当てます。 カスタムソースをデフォルトストックに割り当てることはできません。 |
| [!UICONTROL Assigned Sources] | 割り当てられたソースのリスト。 ![並べ替えアイコン ](assets/icon-sort.png)を使用してソースをドラッグ&amp;ドロップし、注文フルフィルメントと発送の優先順位付け注文に追加します。<br/><br/>**[!UICONTROL Code]**- ソースの一意のコード ID。<br/>**[!UICONTROL Name]** - ソースの名前の説明。<br/>**[!UICONTROL Unassign]**- ![ ゴミ箱アイコン ](../assets/icon-delete-trashcan-solid.png)を使用して、割り当てられたソースを在庫から削除します。 |
