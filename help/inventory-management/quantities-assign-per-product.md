---
title: 製品ごとの在庫数量の割り当て
description: 製品の在庫数量を更新し、手持在庫と有効在庫数をトラッキングする方法について説明します。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# 製品ごとの数量の割り当て

追加後 [ソース](sources-assign-per-product.md)製品の在庫数量を更新します。 これらの値は、手持在庫の有効在庫数をトラッキングします。

ソースを削除せずにソースの在庫を出荷から非表示にするには、次のように設定します _[!UICONTROL Source Item Status]_対象： `Out of Stock`. SSA および出荷オプションは、次のようにリストされたソースにのみアクセスします `In Stock` 使用可能な在庫数量を使用。

更新されたすべての数量とソースが製品グリッドに表示されます。

## 数量の更新

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を探して、編集モードで開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Sources]** セクション。

1. を設定 **[!UICONTROL Source Item Status]** 対象： `In Stock`.

1. 手持在庫の数量を更新するには、 **[!UICONTROL Qty]**.

1. 在庫数量の通知を設定するには、次のいずれかを実行します。

   - カスタム通知数量 – 選択を解除 **[!UICONTROL Use Default]** チェックボックスに金額を入力 **[!UICONTROL Notify Qty]**.
   - デフォルトの通知数量 – を選択します **[!UICONTROL Use Default]** チェックボックス。 [!DNL Commerce] の設定を確認して使用します _[!UICONTROL Advanced Inventory]_またはグローバルストア設定です。

   ![ソースごとの製品数量の更新](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 次のいずれかの操作を行って保存します。

   - クリック **[!UICONTROL Save]**.

   - 日 **[!UICONTROL Save]** （![メニュー矢印](../assets/icon-menu-down-arrow-red.png)） メニュー、を選択 **[!UICONTROL Save & Close]**.


製品グリッドが更新され、すべてのソースと関連数量のリストが表示されます。 ソースが 6 つ以上の製品の場合は、にポインタを合わせます。 _[!UICONTROL Quantity per Source]_列に移動して完全なリストを表示します。

![ソースごとの製品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
