---
title: 製品設定 – [!UICONTROL Sources]
description: 製品の場合、[!UICONTROL Sources] の設定を使用すると、製品の配布元となる  [!DNL Inventory Management]  ソースにアクセスできます。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Sources]

製品設定の「_[!UICONTROL Sources]_」セクションには、製品の配布元となるソースが一覧表示されます。 これは、ソースの割り当てと割り当て解除、および製品の数量と可用性の管理に使用します。 このセクションは、ストアに複数のソースが定義されている場合にのみ表示されます。 ソースについて詳しくは、「[&#x200B; ソースの管理 &#x200B;](../inventory-management/sources-manage.md)」を参照してください。

## 製品のソースの割り当て

1. 「**[!UICONTROL Assign Source]**」をクリックします。

1. 必要なソースのチェックボックスをオンにします。

1. 「**[!UICONTROL Done]**」をクリックします。

1. 「**[!UICONTROL Source Item Status]**」を選択し、必要に応じて **[!UICONTROL Qty]** と **[!UICONTROL Notify Qty]** の値を入力します。

1. 「**[!UICONTROL Save]**」をクリックして、変更を保存します。

![&#x200B; ソースビュー &#x200B;](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## フィールド参照

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | ソースの一意の名前。 |
| [!UICONTROL Source Status] | 製品がカタログで有効になっているか無効になっているかを判断します。 |
| [!UICONTROL Source Item Status] | 商品の現在の可用性を決定します。 オプション：<br />**[!UICONTROL In Stock]**– 製品を購入できるようにします。<br />**[!UICONTROL Out of Stock]** - バックオーダーが有効化されていない限り、は商品を購入できないようにし、カタログからリストを削除します。 |
| [!UICONTROL Qty] | 各ソースの手持在庫金額。 |
| [!UICONTROL Notify Qty] | `Notify Quantity Use Default` が選択されていない場合のこの特定のソースに対する _数量の通知_ の金額。 |
| [!UICONTROL Notify Qty Use Default] | 製品の詳細在庫または店舗構成のグローバル設定の _数量の通知_ に対して既定の設定を使用することを示します。 製品の高度なインベントリ設定の詳細については、[&#x200B; 製品の詳細オプションの構成 &#x200B;](../inventory-management/product-options.md) を参照してください。 |
| [!UICONTROL Actions] | 割り当てられたソースに対して「**[!UICONTROL Unassign]**」をクリックすると、そのソースを製品で使用できなくなります。 ソースが割り当てられていない場合は、「**[!UICONTROL Assign Sources]**」をクリックして、ソースを製品で使用できるようにします。 [!UICONTROL Assign Sources] のオプションについて詳しくは、[&#x200B; 製品ごとのソースの割り当て &#x200B;](../inventory-management/sources-assign-per-product.md) を参照してください。 |

{style="table-layout:auto"}
