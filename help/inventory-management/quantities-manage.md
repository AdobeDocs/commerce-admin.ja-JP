---
title: 在庫数量の管理
description: 新規製品のソースと数量を割り当てる方法、または既存の製品を変更する方法を説明します。
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 在庫数量の管理

次の情報では、新規製品のソースと数量を割り当てる方法、または既存製品を変更する方法について詳しく説明します。

製品を作成する際は、製品の作成時にソースと数量を割り当てます。 詳しくは、 [製品の作成](../catalog/product-create.md) を参照してください。 これらのページには、ソースの単一ソースおよび複数ソースの情報と、ソースごとの数量が含まれます。

アップグレードされたに初めてアクセスしたとき [!DNL Commerce] 次を使用 [!DNL Inventory Management]に設定されている場合、すべての製品と数量がデフォルトのソースに割り当てられます。 .csv ファイルを使用して新しい製品を読み込むと、それらもデフォルトのソースに割り当てられます。

単一ソースおよび複数ソースのマーチャントは、製品ごとまたは一括でソース、在庫数量、しきい値を更新できます。

- 単一ソース・マーチャントは、デフォルト・ソースの製品数量を更新できます。 この数量は、販売可能な製品の合計数です。

- 複数ソースのマーチャントは、各場所（倉庫、店舗、出荷業者など）に対して、製品ごとに複数のソースと数量を割り当てることができます。 製品の在庫金額を設定する前に、ソースを追加することをお勧めします。

ソースと数量を製品に追加する場合は、製品グリッドを使用して金額を表示できます。 ソースが多い場合は、 _[!UICONTROL Quantity per Source]_現在の数量を含む、スクロール可能なソースの完全なリストを表示します。

![ソースあたりの製品数量](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

在庫を製品に割り当てるには、次のオプションがあります。

- [製品ごとのソースの割り当て](sources-assign-per-product.md)  — カタログ内の製品ごとにソースを手動で割り当てます。

- [製品ごとの数量の割当](quantities-assign-per-product.md)  — ソースごとの製品に手持在庫金額を追加します。 この情報は、複数ソースのマーチャントに固有の情報です。

- [ソースの一括割り当てと割り当て解除](bulk-assignment.md)  — ソースを選択した製品に一括アクションとして割り当てます。 以下を使用します。 [在庫をソースに転送](inventory-transfer.md) オプションを使用します。

- [ソースへの在庫の転送](inventory-transfer.md) - 1 つの出発元ソースから宛先ソースへ、すべての在庫を一括転送します。

- [数量のインポートとエクスポート](inventory-import-export.md)  — インポートおよびエクスポート機能を使用して、複数の製品 SKU をソースおよび在庫数量で更新します。
