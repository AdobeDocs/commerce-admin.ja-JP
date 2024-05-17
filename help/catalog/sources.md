---
title: 製品設定 –  [!UICONTROL Sources]
description: 製品の場合、 [!UICONTROL Sources] 設定は、へのアクセスを可能にします [!DNL Inventory Management] 製品を配布できるソース。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 製品設定 –  [!UICONTROL Sources]

この _[!UICONTROL Sources]_「製品設定」セクションには、製品を配布できるソースが一覧表示されます。 これは、ソースの割り当てと割り当て解除、および製品の数量と可用性の管理に使用します。 このセクションは、ストアに複数のソースが定義されている場合にのみ表示されます。 ソースの詳細については、を参照してください [ソースの管理](../inventory-management/sources-manage.md).

## 製品のソースの割り当て

1. クリック **[!UICONTROL Assign Source]**.

1. 必要なソースのチェックボックスをオンにします。

1. クリック **[!UICONTROL Done]**.

1. を選択 **[!UICONTROL Source Item Status]** を入力し、 **[!UICONTROL Qty]** および **[!UICONTROL Notify Qty]** 必要に応じて、の値を指定します。

1. クリック **[!UICONTROL Save]** 変更を保存します。

![ソースビュー](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## フィールド参照

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | ソースの一意の名前。 |
| [!UICONTROL Source Status] | 製品がカタログで有効になっているか無効になっているかを判断します。 |
| [!UICONTROL Source Item Status] | 商品の現在の可用性を決定します。 オプション：<br />**[!UICONTROL In Stock]**– 製品を購入できるようにします。<br />**[!UICONTROL Out of Stock]** - バックオーダーが有効化されていない限り、は製品を購入できないようにし、カタログからリストを削除します。 |
| [!UICONTROL Qty] | 各ソースの手持在庫金額。 |
| [!UICONTROL Notify Qty] | の金額 _数量を通知_ この特定のソースに対して `Notify Quantity Use Default` が選択されていません。 |
| [!UICONTROL Notify Qty Use Default] | デフォルト設定を使用することを示します _数量を通知_ 商品の詳細在庫またはストア設定のグローバル設定。 製品の高度なインベントリ設定の詳細については、を参照してください。 [製品の詳細オプションの設定](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | 割り当てられたソースに対して、 **[!UICONTROL Unassign]** ：製品でソースを使用できないようにします。 未割り当てのソースに対して、 **[!UICONTROL Assign Sources]** 製品のソースを使用可能にします。 詳しくは、 [!UICONTROL Assign Sources] オプション、を参照 [製品ごとのソースの割り当て](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
