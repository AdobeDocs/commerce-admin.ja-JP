---
title: 在庫をソースに転送
description: 複数ソースのマーチャントが、あるソースの場所から別のソースの場所に製品在庫を転送する方法を説明します。
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 在庫をソースに転送

複数のソースを持つ商人は、ビジネスのニーズや場所の状況に応じて、あるソースの場所から別の場所に製品の在庫を移します。 たとえば、倉庫の場所を閉じたり、特定の製品を場所から出荷しなくなったりする場合、それらの製品のすべての工程を新しい場所に移動できます。

このオプションでは、1 つ以上の製品、在庫を転送する原産地ソース、数量を受け取る搬送先ソースを選択できます。

- 在庫数量、ソース品目ステータス（在庫/在庫切れ）および選択したソースの通知数量は、製品ごとに移動されます。

- そのソースが製品にない場合はスキップされます。

- ソースのすべての製品在庫が移動されます。 一部の数量は転送できません。

>[!NOTE]
>
>出発元と出発先のソースが異なる在庫にある場合は、集計済の出荷可能数量と進行中のオーダーの予約に影響します。

在庫数量の移動時に、ソースの割り当てを解除することもできます。

{{$include /help/_includes/unassign-source.md}}

![在庫を別のソースに転送](assets/inventory-bulk-transfer-source.gif)

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. ソースを変更する製品を選択します。

   製品を検索し、転送するチェックボックスを選択するには、参照または検索します。

1. 次をクリック： **[!UICONTROL Actions]** 上部のメニューで「 」を選択します。 **[!UICONTROL Transfer Inventory to Source]**.

1. クリック **[!UICONTROL OK]** をクリックします。

1. 製品を新しい宛先に転送するには、接触チャネル (_[!UICONTROL from]_) ソース。

1. 製品を新しい宛先に転送するには、宛先 (_[!UICONTROL to]_) ソース。

1. 製品からソースを削除するには、オプションのチェックボックスをオンにします。 **[!UICONTROL Unassign from origin source after transfer]**.

   ![転送元と転送先を選択](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Transfer Inventory]**.

   すべての製品数量が元のソースから差し引かれ、宛先のソースに追加されます。 「数量」と「販売可能数量」が自動的に更新されます。
