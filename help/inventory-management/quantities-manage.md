---
title: 在庫量の管理
description: '[!DNL Inventory Management]の新製品と既存製品にソースとソースごとの数量を割り当てる管理手順の概要。'
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%
---
# 在庫量の管理

以下のガイドラインを使用して、新製品または既存製品のソースと数量を割り当てます。

製品作成時には、製品作成時にソースと数量を割り当てます。 詳しい手順については、[製品の作成](../catalog/product-create.md)を参照してください。 これらのページには、ソースごとのソースと数量に関するシングルソースとマルチソースの情報が含まれています。

[!DNL Inventory Management]でアップグレードされた[!DNL Commerce]に最初にアクセスすると、すべての商品と数量がデフォルトのSourceに割り当てられます。 .csv ファイルを使用して新しい商品を読み込む場合、それらはデフォルトのSourceにも割り当てられます。

シングルソースとマルチソースのマーチャントは、商品ごとに、または一括でソース、在庫量、しきい値を更新できます。

- シングルソースのマーチャントは、デフォルトのSourceの商品数量を更新できます。 この数量は、販売可能な製品の合計数です。

- マルチソースのマーチャントは、商品ごとに複数のソースや数量を割り当てることができます（倉庫、実店舗、ドロップシッパーなど）。 製品の在庫量を設定する前に、ソースを追加しておくことをお勧めします。

商品にソースと数量を追加する場合は、商品グリッドで金額を表示できます。 ソースの数が多い場合は、_[!UICONTROL Quantity per Source]_にカーソルを合わせると、現在の量のソースの完全なスクロール可能なリストが表示されます。

![ ソースごとの製品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

商品に在庫を割り当てるには、次のオプションがあります。

- [製品ごとのソースの割り当て](sources-assign-per-product.md) - カタログ内の製品ごとにソースを手動で割り当てます。

- [製品ごとの数量の割り当て](quantities-assign-per-product.md) - ソースごとに手持在庫量を製品に追加します。 この情報は、マルチソースのマーチャントに特化しています。

- [ ソースの一括割り当てと割り当て解除](bulk-assignment.md) – 選択した製品にソースを一括操作として割り当てます。 在庫を転送してソースを削除する場合は、「[在庫をSourceに転送](inventory-transfer.md)」オプションを使用します。

- [在庫をSourceに転送](inventory-transfer.md) – すべての在庫を1つの発信元ソースから発信先ソースに一括転送します。

- [数量のインポートとエクスポート ](inventory-import-export.md) - インポート機能とエクスポート機能を使用して、ソースと在庫数量を含む複数の製品SKUを更新します。
