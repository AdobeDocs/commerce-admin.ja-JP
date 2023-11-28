---
title: 製品設定 — [!UICONTROL Sources]
description: 製品の場合、 [!UICONTROL Sources] 設定は、 [!DNL Inventory Management] 製品の配布元。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# 製品設定 — [!UICONTROL Sources]

The _[!UICONTROL Sources]_製品設定の「 」セクションには、製品の配布元のリストが表示されます。 ソースの割り当てと割り当て解除、および製品の数量と使用可能性の管理に使用されます。 このセクションは、ストアに対して複数のソースが定義されている場合にのみ表示されます。 ソースについて詳しくは、 [ソースの管理](../inventory-management/sources-manage.md).

## 製品のソースの割り当て

1. クリック **[!UICONTROL Assign Source]**.

1. 必要なソースのチェックボックスをオンにします。

1. クリック **[!UICONTROL Done]**.

1. 選択 **[!UICONTROL Source Item Status]** をクリックし、 **[!UICONTROL Qty]** および **[!UICONTROL Notify Qty]** の値を指定します。

1. クリック **[!UICONTROL Save]** をクリックして変更を保存します。

![ソース表示](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## フィールド参照

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | ソースの一意の名前。 |
| [!UICONTROL Source Status] | カタログで商品が有効か無効かを指定します。 |
| [!UICONTROL Source Item Status] | 製品の現在の可用性を決定します。 オプション：<br />**[!UICONTROL In Stock]**— 製品を購入できるようにします。<br />**[!UICONTROL Out of Stock]**  — 逆注文が有効化されていない場合、は商品の購入を禁止し、カタログからリストを削除します。 |
| [!UICONTROL Qty] | 各ソースの手持在庫金額。 |
| [!UICONTROL Notify Qty] | の金額 _数量を通知_ 次の場合にこの特定のソースの `Notify Quantity Use Default` が選択されていません。 |
| [!UICONTROL Notify Qty Use Default] | のデフォルト設定を使用することを示します。 _数量を通知_ ストア設定の製品の Advanced Inventory またはグローバル設定。 製品の高度な在庫設定について詳しくは、 [高度な製品オプションの設定](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | 割り当てられたソースの場合は、 **[!UICONTROL Unassign]** をクリックして、ソースを製品で使用できなくします。 未割り当てのソースの場合は、 **[!UICONTROL Assign Sources]** をクリックして、製品で使用できるソースを作成します。 詳しくは、 [!UICONTROL Assign Sources] options, see [製品ごとのソースの割り当て](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
