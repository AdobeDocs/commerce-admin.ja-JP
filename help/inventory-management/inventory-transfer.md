---
title: ソースに在庫を転送
description: マルチソースのマーチャントが製品在庫をソースの場所から別の場所に転送する方法を説明します。
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# ソースに在庫を転送

マルチソースマーチャントは、ビジネスニーズや場所のステータスに応じて、多くの場合、製品在庫をソースの場所から別の場所に転送します。 例えば、倉庫の場所を閉鎖したり、特定の製品を場所から出荷しなくなり、それらの製品のすべての操作を新しい場所に移動したりする場合があります。

このオプションを使用すると、1 つ以上の製品、在庫を移動する移動元ソース、および数量を受け入れる移動先ソースを選択できます。

- 在庫数量、ソース品目ステータス（在庫中/在庫切れ）、および選択したソースの通知数量が製品ごとに移動されます。

- 製品にそのソースがない場合は、スキップされます。

- ソースのすべての製品インベントリが移動されます。 一部数量は移動できません。

>[!NOTE]
>
>出荷元と出荷先のソースが異なる在庫にある場合は、集計された販売可能数量と進行中の注文の予約に影響します。

在庫数量の移動時にソースの割当を解除することもできます。

{{$include /help/_includes/unassign-source.md}}

![在庫を別のソースに転送](assets/inventory-bulk-transfer-source.gif)

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   製品を参照または検索して検索し、転送するチェックボックスを選択します。

1. 「」をクリックします **[!UICONTROL Actions]** 上部のメニューからを選択します。 **[!UICONTROL Transfer Inventory to Source]**.

1. クリック **[!UICONTROL OK]** 確認ダイアログで、次の手順を実行します。

1. 新しい宛先に製品を転送するには、転送元（_[!UICONTROL from]_） ソース。

1. 製品を新しい宛先に転送するには、宛先（_[!UICONTROL to]_） ソース。

1. 製品からソースを削除するには、オプションのチェックボックスを選択します **[!UICONTROL Unassign from origin source after transfer]**.

   ![転送元と転送先を選択](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Transfer Inventory]**.

   すべての製品数量が搬送元ソースから差し引かれ、搬送先ソースに追加されます。 「数量」と「販売可能数量」が自動的に更新されます。
