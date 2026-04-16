---
title: 最近閲覧した商品または比較した商品
description: 最近閲覧した商品と比較済みの商品のストアフロントのコンテンツブロックを設定する方法を説明します。
exl-id: a4580835-68c2-4eb0-825e-0939eeab921b
feature: Products, Storefront
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 6848b28d05bc3da12d0ecdeb32d6515c7be7cdfb
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# 最近閲覧した商品または比較した商品

_最近表示されたブロックと最近比較されたブロック_&#x200B;は、通常、カタログページの右側のサイドバーに表示されます。 各にリストされている製品の数は、web サイト、ストア、またはストアビューごとに設定できます。

**_最近閲覧した商品と比較した商品を設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. ![ セクションの](../assets/icon-display-expand.png)拡張セレクター&#x200B;**[!UICONTROL Recently Viewed/Compared Products]**&#x200B;を展開します。

   ![ カタログ設定 – 最近閲覧/比較された製品](../configuration-reference/catalog/assets/catalog-recently-viewed-and-compared-products.png){width="600" zoomable="yes"}

   これらの各構成設定の詳細については、[構成リファレンスガイド ](../configuration-reference/catalog/catalog.md#recently-viewedcompared-products)の&#x200B;_最近表示された製品/比較済み製品_&#x200B;を参照してください。

1. 製品IDなどの製品ウィジェット情報をデータベース内の現在の製品ストレージの可用性と同期させ、この情報を別のデバイスで再利用するように&#x200B;**[!UICONTROL Synchronize widget products with backend storage]**&#x200B;を設定します。

1. 設定が適用されるweb サイト、ストア、またはストア ビューに&#x200B;**[!UICONTROL Show for Current]**&#x200B;を設定します。

1. **[!UICONTROL Default Recently Viewed Products Count]**&#x200B;に、リストに表示する最近閲覧した製品の数を入力します。

1. **[!UICONTROL Default Recently Compared Products Count]**&#x200B;に、リストに表示される最近比較した製品の数を入力します。

1. **[!UICONTROL Lifetime of products in Recently Viewed Widget]**&#x200B;の場合、任意の時間範囲を0より大きい秒数で入力します。

   この設定は、最近閲覧した商品が最近閲覧したリストに表示される時間を決定します。

1. **[!UICONTROL Lifetime of products in Recently Compared Widget]**&#x200B;の場合、任意の時間範囲を0より大きい秒数で入力します。

   この設定は、比較された製品が最近比較されたリストに表示される時間を決定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
