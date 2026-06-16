---
title: 一括在庫ソース割り当てと割り当て解除
description: ソースの割り当てツールを使用して、製品のソース割り当てを管理する方法を説明します。
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/H8UQh7quyOeDq6-hSmf83fzUuJkuSLv0i2dezX-GKRA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 328
ht-degree: 0%

---

# ソースの一括割り当てと割り当て解除

_ソースの割り当て_ ツールを使用して、1つ以上のソースを製品に追加します。 このツールは、デフォルトの在庫またはカスタム在庫にカスタムソースを作成して割り当て、新しい場所と在庫を準備する際に役立ちます。

新しいカスタムソースを追加した後、管理者を通じて、または[&#x200B; インポート機能](inventory-import-export.md)を使用して、製品ごとに[在庫量](quantities-assign-per-product.md)または複数の製品に対して追加できます。

![選択した製品の在庫ソースを追加](assets/inventory-bulk-assign-sources.gif)

## ソースと数量の割り当て

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. ソースを変更する製品を選択します。

   参照または検索して商品を見つけ、それらのチェックボックスを選択します。

1. 上部の&#x200B;**[!UICONTROL Actions]** メニューをクリックし、**[!UICONTROL Assign Inventory Source]**&#x200B;を選択します。

1. 確認ダイアログで「**[!UICONTROL OK]**」をクリックします。

1. 製品に追加するすべてのソースについて、チェックボックスを選択します。

1. **[!UICONTROL Assign Sources]**&#x200B;をクリックします。

   ![&#x200B; ソースを追加する製品を選択](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

在庫量が0の商品にソースが追加されます。 ソースごとに[在庫量](quantities-assign-per-product.md)を追加できます。

## ソースと数量の割り当て解除

製品からソースの割り当てを解除する場合、その製品がその場所に在庫がないことを示します。 このプロセスは、現在製品に割り当てられているソースのすべての在庫データを完全に消去します。 既存の在庫を新しい場所に移動する場合は、「_在庫を転送_」オプションの使用を検討してください。

{{$include /help/_includes/unassign-source.md}}

ソースを削除する前に、これらの製品のすべての注文と出荷を完了することを強くお勧めします。

![選択した製品のソースの割り当てを解除](assets/inventory-bulk-unassign-sources.gif)

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. ソースを変更する製品を選択します。

   参照または検索して商品を見つけ、それらのチェックボックスを選択します。

1. 上部の&#x200B;**[!UICONTROL Actions]** メニューをクリックし、**[!UICONTROL Unassign Inventory Source]**&#x200B;を選択します。

1. 確認ダイアログで「**[!UICONTROL OK]**」をクリックします。

1. 製品から削除するソースを選択します。

   このページには、割り当てを解除すると、製品からすべての特定のソースおよび数量データが削除されるというアラートが表示されます。

1. **[!UICONTROL Unassign Sources]**&#x200B;をクリックします。

   ![選択した製品からソースを削除](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
