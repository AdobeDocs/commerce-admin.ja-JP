---
title: 「有効にする [!DNL Inventory Management]“
description: を有効にする方法を説明します [!DNL Inventory Management] グローバルストアまたは製品レベル。
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Enable （有効） [!DNL Inventory Management]

製品インベントリを管理するには、を有効にします [!DNL Inventory Management] グローバルストアまたは製品レベル。 いつ _在庫の管理_ 」オプションが有効になっています。 [!DNL Inventory Management] 設定済みの在庫とソースを通じて、サイトで使用可能な製品数量を自動的に追跡します。 すべての機能とオプションは、有効になると、追加の設定なしでトラッキングとレポート作成を開始します。

ビジネスの運営と在庫の更新をセールスのスピードに合わせて行います。 顧客が買い物をするとき、販売チャネルおよびソースごとに、利用可能な在庫の正確で更新された情報を受け取ります。 利用可能な販売可能数量は、顧客が買い物かごに商品を追加して購入を完了したとき、および注文を管理し、出荷を作成し、払い戻しを発行したときに、在庫ごとに更新されます。 新規または転送済みの在庫の到着は、ソースに更新され、オンライン販売ですぐに利用できます。 バックオーダーは、無制限オーダーまたは追加構成なしで、指定されたしきい値まで完了します。 また、1 つ以上のソースに対して一部または全出荷を入力し、提示を使用して完了することで、受注の履行および手持在庫を完全に管理できます。

>[!NOTE]
>
>デフォルトでは [!DNL Inventory Management] インストール時またはアップグレード時に有効化 [!DNL Commerce]. ビジネスニーズに応じて、トラッキングされたを有効または無効にすることができます [!DNL Inventory Management] 内 [!DNL Commerce].

この設定が単一および複数ソースのインベントリでどのように機能するか：

- 使用目的 [!DNL Inventory Management]、有効にする _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] 製品レベルの設定は、ストアの設定よりも優先されます。

- Order Management またはサードパーティのサービス（ERP など）を使用するには、無効にします。 [!UICONTROL Manage Stock].

- 製品レベルの設定でシステムのデフォルトが使用されている場合は、ストアの設定が上書きされます。

（を使用） [!DNL Inventory Management] 有効にする。すべての設定を行うには、以下の説明を参照してください。

- [グローバルオプションの設定](global-options.md) - カタログ全体に影響する設定は、システムのデフォルト設定と見なされます。

- [製品オプションの設定](product-options.md) - グローバルオプションを上書きする特定の製品の設定。

## 有効または無効 [!DNL Inventory Management]

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Inventory]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) _製品ストックオプション_ さらに、以下を設定します。

   ![製品ストックオプション](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 在庫を管理し、すべてを使用するには [!DNL Commerce] 機能、設定 **[!UICONTROL Manage Stock]** 対象： `Yes` （デフォルト）。

   - 無効にする [!DNL Inventory Management]、選択を解除 **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Manage Stock]** 対象： `No`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## 店舗の在庫の管理

参照： [グローバルオプションの設定](global-options.md).

## 製品の在庫の管理

参照： [製品オプションの設定](product-options.md).
