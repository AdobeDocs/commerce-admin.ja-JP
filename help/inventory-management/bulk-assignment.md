---
title: 在庫ソースの一括割り当ておよび割り当て解除
description: ソースを割り当てツールを使用して、製品のソース割り当てを管理する方法について説明します。
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# ソースの一括割り当てと未割り当て

の使用 _ソースの割り当て_ ツールを使用して、1 つ以上のソースを製品に追加します。 このツールは、カスタムソースを作成してデフォルト在庫またはカスタム在庫に割り当て、新しい場所と在庫を準備する際に役立ちます。

新しいカスタムソースを追加した後、次の情報を追加できます [製品ごとの在庫数量](quantities-assign-per-product.md) または、管理者を通じてまたはを使用して複数の製品に対して [インポート機能](inventory-import-export.md).

![選択した製品の在庫ソースを追加](assets/inventory-bulk-assign-sources.gif)

## ソースと数量の割り当て

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   参照または検索して製品を見つけ、それらのチェックボックスを選択します。

1. 「」をクリックします **[!UICONTROL Actions]** 上部のメニューからを選択します。 **[!UICONTROL Assign Inventory Source]**.

1. クリック **[!UICONTROL OK]** 確認ダイアログで、次の手順を実行します。

1. 製品に追加するすべてのソースについて、チェックボックスをオンにします。

1. クリック **[!UICONTROL Assign Sources]**.

   ![ソースを追加する製品を選択](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

ソースは、在庫数量が 0 の製品に追加されます。 次を追加できます [在庫数量](quantities-assign-per-product.md) ソースごとに。

## ソースと数量の割り当て解除

製品からソースの割り当てを解除すると、その製品がその場所でストックされなくなったことを示します。 このプロセスでは、製品に現在割り当てられているソースのすべての在庫データが完全に消去されます。 既存の在庫を新しい場所に移動する場合は、 _在庫の転送_ オプション。

{{$include /help/_includes/unassign-source.md}}

ソースを削除する前に、これらの製品のすべての注文と出荷を完了することを強くお勧めします。

![選択した製品のソースの割り当て解除](assets/inventory-bulk-unassign-sources.gif)

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   参照または検索して製品を見つけ、それらのチェックボックスを選択します。

1. 「」をクリックします **[!UICONTROL Actions]** 上部のメニューからを選択します。 **[!UICONTROL Unassign Inventory Source]**.

1. クリック **[!UICONTROL OK]** 確認ダイアログで、次の手順を実行します。

1. 製品から削除するソースを選択します。

   割り当て解除によってプロダクトから特定のソースおよび数量データがすべて削除されることを示すアラートがページに表示されます。

1. クリック **[!UICONTROL Unassign Sources]**.

   ![選択した製品からソースを削除](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
