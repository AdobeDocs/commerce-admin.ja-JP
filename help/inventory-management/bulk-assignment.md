---
title: 一括在庫ソース割り当てと割り当て解除
description: '[ ソースの割り当て ] ツールを使用して、製品のソース割り当てを管理する方法を説明します。'
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# 一括ソース割り当てと割り当て解除

以下を使用します。 _ソースの割り当て_ ツールを使用して、1 つ以上のソースを製品に追加します。 このツールは、カスタムソースを作成してデフォルトの在庫またはカスタム在庫に割り当て、新しい場所と在庫を準備する際に役立ちます。

新しいカスタムソースを追加した後、 [製品あたりの在庫数量](quantities-assign-per-product.md) または複数の製品の場合は、管理者または [読み込み機能](inventory-import-export.md).

![選択した製品の在庫ソースを追加します](assets/inventory-bulk-assign-sources.gif)

## ソースと数量を割り当てる

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   製品を参照または検索して見つけ、それらのチェックボックスを選択します。

1. 次をクリック： **[!UICONTROL Actions]** 上部のメニューで「 」を選択します。 **[!UICONTROL Assign Inventory Source]**.

1. クリック **[!UICONTROL OK]** をクリックします。

1. 製品に追加するすべてのソースに対して、チェックボックスをオンにします。

1. クリック **[!UICONTROL Assign Sources]**.

   ![ソースを追加する製品を選択](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

在庫数量が 0 の製品にソースが追加されます。 次の項目を追加できます。 [在庫数量](quantities-assign-per-product.md) ソースごと。

## ソースと数量の割り当てを解除する

製品からソースの割り当てを解除すると、その場所に製品が在庫されなくなったことを示します。 このプロセスは、現在製品に割り当てられているソースのすべての在庫データを完全に消去します。 既存の在庫を新しい場所に移動する場合は、 _在庫の転送_ オプション。

{{$include /help/_includes/unassign-source.md}}

ソースを削除する前に、それらの製品のすべての注文と出荷を完了することを強くお勧めします。

![選択した製品のソースの割り当てを解除](assets/inventory-bulk-unassign-sources.gif)

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   製品を参照または検索して見つけ、それらのチェックボックスを選択します。

1. 次をクリック： **[!UICONTROL Actions]** 上部のメニューで「 」を選択します。 **[!UICONTROL Unassign Inventory Source]**.

1. クリック **[!UICONTROL OK]** をクリックします。

1. 製品から削除するソースを選択します。

   割り当てを解除すると、製品から特定のソースと数量のデータがすべて削除されるアラートがページに表示されます。

1. クリック **[!UICONTROL Unassign Sources]**.

   ![選択した製品からソースを削除](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
