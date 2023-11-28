---
title: "有効化 [!DNL Inventory Management]"
description: 有効にする方法を説明します [!DNL Inventory Management] グローバルストアまたは製品レベル。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 有効にする [!DNL Inventory Management]

製品在庫を管理するには、 [!DNL Inventory Management] グローバルストアまたは製品レベル。 次の場合に _在庫の管理_ オプションが有効になっている場合、 [!DNL Inventory Management] は、設定された在庫およびソースを通じて、サイトで使用可能な製品の数量を自動的に追跡します。 すべての機能とオプションは、有効にすると、追加の設定なしでトラッキングとレポートを開始します。

営業のスピードでビジネスが実行され、インベントリの更新が行われます。 顧客が買い物をすると、販売チャネルおよびソースごとに、利用可能な在庫の正確で更新された情報を受け取ります。 顧客が買い物かごに製品を追加し、購入を完了し、注文の管理、出荷の作成、払い戻しの発行を行うと、在庫ごとに使用可能な販売可能数量が更新されます。 新規または移行された在庫更新がソースに到着し、直ちにオンラインでの販売に利用できます。 バックオーダーは、無限の注文や追加の設定なしで、指定したしきい値まで完了します。 また、1 つ以上のソースに対して、一部または全部の出荷をレコメンデーションと共に入力し、受注履行と手持在庫を完全に管理できます。

>[!NOTE]
>
>デフォルトでは、 [!DNL Inventory Management] インストールまたはアップグレード時に有効になります [!DNL Commerce]. ビジネスニーズに応じて、追跡対象の [!DNL Inventory Management] 範囲 [!DNL Commerce].

単一ソースおよび複数ソースのインベントリでのこの設定の仕組みは次のとおりです。

- 次を使用するには： [!DNL Inventory Management]，有効 _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] 製品レベル設定の設定は、ストア設定を上書きします。

- Order Management またはサードパーティのサービス（ERP など）を使用するには、を無効にします [!UICONTROL Manage Stock].

- 製品レベルの設定でシステムのデフォルトが使用されている場合は、ストアの設定が上書きされます。

を使用 [!DNL Inventory Management] 有効にするには、次を参照してすべての設定を行います。

- [グローバルオプションの設定](global-options.md)  — カタログ全体に影響を与える設定は、システムのデフォルト設定と見なされます。

- [製品オプションの設定](product-options.md)  — グローバルオプションを上書きする特定の製品の設定。

## 有効または無効 [!DNL Inventory Management]

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Inventory]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) _製品在庫オプション_ および設定：

   ![製品在庫オプション](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 在庫を管理し、すべてを使用するには [!DNL Commerce] 機能、設定 **[!UICONTROL Manage Stock]** から `Yes` （デフォルト）。

   - 無効にするには [!DNL Inventory Management]、選択を解除 **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Manage Stock]** から `No`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ストアの在庫を管理

詳しくは、 [グローバルオプションの設定](global-options.md).

## 製品の在庫の管理

詳しくは、 [製品オプションの設定](product-options.md).
