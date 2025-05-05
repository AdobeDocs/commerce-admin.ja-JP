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

[ ソース ](sources-assign-per-product.md) を追加した後、商品の在庫数量を更新します。 これらの値は、手持在庫の有効在庫数をトラッキングします。

ソースを削除せずにソースの在庫を出荷から非表示にするには、「_[!UICONTROL Source Item Status]_」を「`Out of Stock`」に設定します。 SSA および出荷オプションは、使用可能な在庫数量を持つ `In Stock` としてリストされたソースにのみアクセスします。

更新されたすべての数量とソースが製品グリッドに表示されます。

## 数量の更新

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品を探して、編集モードで開きます。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Sources]**」セクションを展開します。

1. **[!UICONTROL Source Item Status]** を `In Stock` に設定します。

1. 手持在庫の数量を更新するには、**[!UICONTROL Qty]** の金額を入力します。

1. 在庫数量の通知を設定するには、次のいずれかを実行します。

   - カスタム通知数量：「**[!UICONTROL Use Default]**」チェックボックスの選択を解除して、**[!UICONTROL Notify Qty]** に金額を入力します。
   - デフォルトの通知数量：「**[!UICONTROL Use Default]**」チェックボックスを選択します。 [!DNL Commerce] は、_[!UICONTROL Advanced Inventory]_&#x200B;またはグローバルストア設定の設定を確認し、使用します。

   ![Sourceごとの製品数量の更新 ](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 次のいずれかの操作を行って保存します。

   - 「**[!UICONTROL Save]**」をクリックします。

   - **[!UICONTROL Save]** （メニュー矢印 ![ メニュー ](../assets/icon-menu-down-arrow-red.png) で、「**[!UICONTROL Save & Close]**」を選択します。


製品グリッドが更新され、すべてのソースと関連数量のリストが表示されます。 ソースが 6 つ以上ある製品の場合は、_[!UICONTROL Quantity per Source]_&#x200B;の列にカーソルを合わせると、完全なリストが表示されます。

![ ソースごとの製品数量 ](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
