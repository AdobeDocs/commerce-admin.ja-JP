---
title: 製品ごとの在庫量の割り当て
description: 商品の在庫量を更新し、手元にある利用可能な在庫量を追跡する方法について説明します。
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 210
ht-degree: 0%

---

# 製品ごとの数量の割り当て

[&#x200B; ソース &#x200B;](sources-assign-per-product.md)を追加したら、製品の在庫量を更新します。 これらの値は、手元にある利用可能な在庫量を追跡します。

ソースを削除せずに出荷からソースの在庫を非表示にするには、_[!UICONTROL Source Item Status]_&#x200B;を`Out of Stock`に設定します。 SSAおよび出荷オプションは、利用可能な在庫量を含む`In Stock`としてリストされているソースにのみアクセスします。

更新されたすべての数量とソースが商品グリッドに表示されます。

## 数量の更新

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. 商品を検索して編集モードで開きます。

1. **[!UICONTROL Sources]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Source Item Status]**&#x200B;を`In Stock`に設定します。

1. 手持在庫の数量を更新するには、**[!UICONTROL Qty]**&#x200B;の金額を入力します。

1. 在庫量の通知を設定するには、次のいずれかの操作を行います。

   - カスタム通知数量 – **[!UICONTROL Use Default]** チェックボックスの選択を解除し、**[!UICONTROL Notify Qty]**&#x200B;に金額を入力します。
   - デフォルトの通知数量 – 「**[!UICONTROL Use Default]**」チェックボックスを選択します。 [!DNL Commerce]は、_[!UICONTROL Advanced Inventory]_&#x200B;またはグローバル ストア設定の設定を確認して使用します。

   ![Sourceごとの製品数量の更新](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 保存するには、次のいずれかの操作を行います。

   - **[!UICONTROL Save]**&#x200B;をクリックします。

   - **[!UICONTROL Save]** （![&#x200B; メニュー矢印](../assets/icon-menu-down-arrow-red.png)）メニューで、**[!UICONTROL Save & Close]**&#x200B;を選択します。


製品グリッドは、すべてのソースと関連数量のリストで更新されます。 5つ以上のソースが割り当てられている製品の場合は、_[!UICONTROL Quantity per Source]_&#x200B;列にカーソルを合わせると、完全なリストが表示されます。

![&#x200B; ソースごとの製品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
