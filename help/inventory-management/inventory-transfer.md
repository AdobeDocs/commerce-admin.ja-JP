---
title: 在庫をソースに転送
description: マルチソース対応のマーチャントが、あるソースから別のソースに商品インベントリを転送する方法を説明します。
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/HV6GQjHa88xgcSAi-LXhyqe7k2QW95VzQ8eG2mGlJ8I
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
source-wordcount: 282
ht-degree: 0%

---

# 在庫をソースに転送

マルチソースマーチャントは、ビジネスのニーズや拠点のステータスに応じて、商品インベントリをソースから別の場所に転送することがよくあります。 たとえば、倉庫の場所を閉鎖したり、特定の場所から特定の製品の出荷を停止したりして、それらの製品のすべての操作を新しい場所に移動します。

このオプションを使用すると、1つ以上の製品、在庫を転送する元ソースおよび数量を受け取る宛先ソースを選択できます。

- 在庫量、Sourceの在庫状況（在庫中/在庫切れ）、および選択したソースの通知数量は、商品ごとに移動します。

- 製品にそのソースがない場合は、スキップされます。

- ソースのすべての製品在庫が移動されます。 一部の数量を転送することはできません。

>[!NOTE]
>
>原点ソースと宛先ソースが異なる在庫にある場合は、集計販売可能数量と処理中の注文の予約に影響します。

在庫量を転送する際に、ソースの割り当てを解除することもできます。

{{$include /help/_includes/unassign-source.md}}

![別のソースに在庫を転送](assets/inventory-bulk-transfer-source.gif)

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. ソースを変更する製品を選択します。

   商品を閲覧または検索して見つけ、転送するチェックボックスを選択します。

1. 上部の&#x200B;**[!UICONTROL Actions]** メニューをクリックし、**[!UICONTROL Transfer Inventory to Source]**&#x200B;を選択します。

1. 確認ダイアログで「**[!UICONTROL OK]**」をクリックします。

1. 製品を新しい宛先に転送するには、発信元（_[!UICONTROL from]_）のソースを選択します。

1. 製品を新しい宛先に転送するには、宛先（_[!UICONTROL to]_） ソースを選択します。

1. 製品からソースを削除するには、オプションのチェックボックス **[!UICONTROL Unassign from origin source after transfer]**&#x200B;を選択します。

   ![転送元と転送先を選択](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. **[!UICONTROL Transfer Inventory]**&#x200B;をクリックします。

   すべての製品数量は、原点ソースから差し引かれ、宛先ソースに追加されます。 数量と販売可能数量が自動的に更新されます。

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
