---
title: 最近閲覧した商品または比較した商品
description: 最近閲覧した商品と比較済みの商品のストアフロントのコンテンツブロックを設定する方法を説明します。
exl-id: a4580835-68c2-4eb0-825e-0939eeab921b
feature: Products, Storefront
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/YeayJ1RkE6Muq0wNnd6KAQmmZcyjTQrSZOqEltlj8T8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 254
ht-degree: 0%

---

# 最近閲覧した商品または比較した商品

_最近表示されたブロックと最近比較されたブロック_&#x200B;は、通常、カタログページの右側のサイドバーに表示されます。 各にリストされている製品の数は、web サイト、ストア、またはストアビューごとに設定できます。

**_最近閲覧した商品と比較した商品を設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Recently Viewed/Compared Products]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![&#x200B; カタログ設定 – 最近閲覧/比較された製品](../configuration-reference/catalog/assets/catalog-recently-viewed-and-compared-products.png){width="600" zoomable="yes"}

   これらの各構成設定の詳細については、_構成リファレンスガイド_&#x200B;の[最近表示された製品/比較済み製品](../configuration-reference/catalog/catalog.md#recently-viewedcompared-products)を参照してください。

1. 製品IDなどの製品ウィジェット情報をデータベース内の現在の製品ストレージの可用性と同期させ、この情報を別のデバイスで再利用するように&#x200B;**[!UICONTROL Synchronize widget products with backend storage]**&#x200B;を設定します。

1. 設定が適用されるweb サイト、ストア、またはストア ビューに&#x200B;**[!UICONTROL Show for Current]**&#x200B;を設定します。

1. **[!UICONTROL Default Recently Viewed Products Count]**&#x200B;に、リストに表示する最近閲覧した製品の数を入力します。

1. **[!UICONTROL Default Recently Compared Products Count]**&#x200B;に、リストに表示される最近比較した製品の数を入力します。

1. **[!UICONTROL Lifetime of products in Recently Viewed Widget]**&#x200B;の場合、任意の時間範囲を0より大きい秒数で入力します。

   この設定は、最近閲覧した商品が最近閲覧したリストに表示される時間を決定します。

1. **[!UICONTROL Lifetime of products in Recently Compared Widget]**&#x200B;の場合、任意の時間範囲を0より大きい秒数で入力します。

   この設定は、比較された製品が最近比較されたリストに表示される時間を決定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
