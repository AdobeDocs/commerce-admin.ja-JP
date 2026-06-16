---
title: ' [!DNL Inventory Management]を有効にする'
description: グローバルなストアまたは製品レベルで [!DNL Inventory Management] を有効にする方法について説明します。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/evCX34nY-m7WQnZt3xw7ng6-It7Xlf5DTanjKbP1fCk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# [!DNL Inventory Management]を有効にする

商品の在庫を管理するには、グローバル店舗または商品レベルで[!DNL Inventory Management]を有効にします。 _在庫の管理_ オプションが有効になっている場合、[!DNL Inventory Management]は、設定された在庫とソースを通じて、サイトで利用可能な製品数量を自動的に追跡します。 すべての機能とオプションは、追加の設定なしで、有効にすると追跡とレポートが開始されます。

セールスのスピードに合わせてビジネスを展開し、在庫を更新できます。 顧客が商品を購入すると、販売チャネルとソースごとに、利用可能な在庫に関する最新の正確な情報が届きます。 使用可能な販売可能数量は、顧客が商品をカートに追加して購入を完了した場合、および注文を管理し、配送を作成し、返金を発行した場合に、在庫ごとに更新されます。 新しいまたは転送された在庫アップデートのソースへの到着、オンライン販売ですぐに利用できます。 バックオーダーは、無制限の注文や追加の設定なしに、指定されたしきい値まで完了します。 また、レコメンデーションを利用して、1つまたは複数のソースをまたいで部分的または全面的な出荷を入力および完了させることで、注文フルフィルメントと手元の在庫を完全に管理できます。

>[!NOTE]
>
>デフォルトでは、[!DNL Commerce]のインストールまたはアップグレード時に[!DNL Inventory Management]が有効になります。 ビジネスのニーズに応じて、[!DNL Commerce]内でトラッキング対象の[!DNL Inventory Management]を有効または無効にすることができます。

この設定は、シングルソースおよびマルチソースのインベントリで機能します。

- [!DNL Inventory Management]を使用するには、_[!UICONTROL Manage Stock]_を有効にします。

- 製品レベル設定の[!UICONTROL Manage Stock]設定は、ストア設定を上書きします。

- Order Managementまたはサードパーティのサービス （ERPなど）を使用するには、[!UICONTROL Manage Stock]を無効にします。

- 製品レベルの設定でシステムのデフォルトが使用されている場合は、ストア設定が上書きされます。

[!DNL Inventory Management]が有効になっている場合は、すべての設定を構成するために次を参照してください。

- [ グローバル オプションの設定](global-options.md) - カタログ全体に影響する設定は、システムの既定の設定と見なされます。

- [製品オプションの設定](product-options.md) - グローバルオプションを上書きする特定の製品の設定。

## [!DNL Inventory Management]を有効または無効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Catalog]**&#x200B;を展開し、**[!UICONTROL Inventory]**&#x200B;を選択します。

1. ![拡張セレクター](../assets/icon-display-expand.png) _製品ストックオプション_&#x200B;を展開して設定します。

   ![商品ストックオプション ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 在庫を管理し、すべての[!DNL Commerce]機能を使用するには、**[!UICONTROL Manage Stock]**&#x200B;を`Yes`に設定します（デフォルト）。

   - [!DNL Inventory Management]を無効にするには、**[!UICONTROL Use system value]** チェックボックスの選択を解除し、**[!UICONTROL Manage Stock]**&#x200B;を`No`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## 店舗の在庫の管理

[ グローバルオプションの設定](global-options.md)を参照してください。

## 商品の在庫の管理

[製品オプションの設定](product-options.md)を参照してください。
