---
title: 製品設定 – [!UICONTROL Sources]
description: 製品の場合、[!UICONTROL Sources]設定は、製品を配布できる [!DNL Inventory Management]  ソースへのアクセスを提供します。
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-wordcount: 259
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Sources]

製品設定の&#x200B;_[!UICONTROL Sources]_&#x200B;セクションには、製品を配布できるソースが一覧表示されます。 ソースの割り当てと割り当て解除、および製品の数量と可用性の管理に使用されます。 このセクションは、ストアに定義されているソースが複数ある場合にのみ表示されます。 ソースについて詳しくは、[&#x200B; ソースの管理](../inventory-management/sources-manage.md)を参照してください。

## 製品のソースの割り当て

1. **[!UICONTROL Assign Source]**&#x200B;をクリックします。

1. 必要なソースのチェックボックスを選択します。

1. **[!UICONTROL Done]**&#x200B;をクリックします。

1. **[!UICONTROL Source Item Status]**&#x200B;を選択し、必要に応じて&#x200B;**[!UICONTROL Qty]**&#x200B;と&#x200B;**[!UICONTROL Notify Qty]**&#x200B;の値を入力します。

1. **[!UICONTROL Save]**&#x200B;をクリックして変更を保存します。

![&#x200B; ソースビュー](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## フィールドリファレンス

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Name] | ソースの一意の名前。 |
| [!UICONTROL Source Status] | 商品がカタログで有効または無効かどうかを指定します。 |
| [!UICONTROL Source Item Status] | 製品の現在の可用性を決定します。 オプション：<br />**[!UICONTROL In Stock]**– 製品を購入可能にします。<br />**[!UICONTROL Out of Stock]** - バックオーダーが有効になっていない限り、製品が購入可能になるのを防ぎ、カタログからリストを削除します。 |
| [!UICONTROL Qty] | 各ソースの手元在庫量。 |
| [!UICONTROL Notify Qty] | `Notify Quantity Use Default`が選択されていない場合は、この特定のソースの&#x200B;_数量の通知_&#x200B;の金額。 |
| [!UICONTROL Notify Qty Use Default] | 製品の詳細在庫またはストア設定のグローバル設定で&#x200B;_数量の通知_&#x200B;のデフォルト設定を使用することを示します。 製品の高度な在庫設定について詳しくは、[高度な製品オプションの設定](../inventory-management/product-options.md)を参照してください。 |
| [!UICONTROL Actions] | 割り当てられたソースの場合は、**[!UICONTROL Unassign]**&#x200B;をクリックして、製品でソースを使用できないようにします。 割り当てられていないソースの場合は、**[!UICONTROL Assign Sources]**&#x200B;をクリックして、製品でソースを利用できるようにします。 [!UICONTROL Assign Sources] オプションについて詳しくは、[製品ごとのソースの割り当て](../inventory-management/sources-assign-per-product.md)を参照してください。 |

{style="table-layout:auto"}
