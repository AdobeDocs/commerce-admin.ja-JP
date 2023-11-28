---
title: 製品ごとの在庫数量の割り当て
description: 製品の在庫数量を更新し、手持在庫の在庫数量を追跡する方法を説明します。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 製品ごとの数量の割り当て

追加後 [ソース](sources-assign-per-product.md)、製品の在庫数量を更新します。 これらの値は、手持の使用可能な在庫金額を追跡します。

ソースを削除せずに、ソースの在庫を出荷から非表示にするには、 _[!UICONTROL Source Item Status]_から `Out of Stock`. SSA および出荷オプションは、次のようにリストされたソースにのみアクセスします。 `In Stock` 在庫数量と共に使用できます。

更新されたすべての数量とソースが製品グリッドに表示されます。

## 数量を更新

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を検索し、編集モードで開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Sources]** 」セクションに入力します。

1. 設定 **[!UICONTROL Source Item Status]** から `In Stock`.

1. 手持在庫の数量を更新するには、次の数量を入力します： **[!UICONTROL Qty]**.

1. 在庫数量の通知を設定するには、次のいずれかの操作を行います。

   - カスタム通知数量 — 選択を解除 **[!UICONTROL Use Default]** チェックボックスに値を入力します。 **[!UICONTROL Notify Qty]**.
   - デフォルトの通知数量 — **[!UICONTROL Use Default]** チェックボックス。 [!DNL Commerce] の設定をチェックして使用します。 _[!UICONTROL Advanced Inventory]_またはグローバルストア設定。

   ![ソースごとの製品数量の更新](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 次のいずれかの操作を行って保存します。

   - クリック **[!UICONTROL Save]**.

   - 次の日： **[!UICONTROL Save]** (![メニュー矢印](../assets/icon-menu-down-arrow-red.png)) メニューで、「 」を選択します。 **[!UICONTROL Save & Close]**.


製品グリッドは、すべてのソースと関連する数量のリストで更新されます。 ソースが 5 つ以上割り当てられている製品の場合は、 _[!UICONTROL Quantity per Source]_列を使用して完全なリストを確認できます。

![ソースあたりの製品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
