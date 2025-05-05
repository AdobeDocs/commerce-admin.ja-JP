---
title: 「有効にする  [!DNL Inventory Management]」
description: グローバルストアまたは製品レベルで有効にする方法を説明します  [!DNL Inventory Management]
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Enable [!DNL Inventory Management]

製品インベントリを管理するには、グローバルストアまたは製品レベルで [!DNL Inventory Management] を有効にします。 _在庫を管理_ オプションが有効になっている場合、[!DNL Inventory Management] は設定された在庫とソースを通じて、サイトで使用可能な製品数量を自動的に追跡します。 すべての機能とオプションは、有効になると、追加の設定なしでトラッキングとレポート作成を開始します。

ビジネスの運営と在庫の更新をセールスのスピードに合わせて行います。 顧客が買い物をするとき、販売チャネルおよびソースごとに、利用可能な在庫の正確で更新された情報を受け取ります。 利用可能な販売可能数量は、顧客が買い物かごに商品を追加して購入を完了したとき、および注文を管理し、出荷を作成し、払い戻しを発行したときに、在庫ごとに更新されます。 新規または転送済みの在庫の到着は、ソースに更新され、オンライン販売ですぐに利用できます。 バックオーダーは、無制限オーダーまたは追加構成なしで、指定されたしきい値まで完了します。 また、1 つ以上のソースに対して一部または全出荷を入力し、提示を使用して完了することで、受注の履行および手持在庫を完全に管理できます。

>[!NOTE]
>
>デフォルトでは、[!DNL Commerce] のインストール時またはアップグレード時に [!DNL Inventory Management] が有効になります。 ビジネスニーズに応じて、[!DNL Commerce] 内でトラッキングする [!DNL Inventory Management] を有効または無効にできます。

この設定が単一および複数ソースのインベントリでどのように機能するか：

- [!DNL Inventory Management] を使用するには、_[!UICONTROL Manage Stock]_&#x200B;を有効にします。

- 製品レベル設定の [!UICONTROL Manage Stock] の設定は、ストア設定よりも優先されます。

- Order Managementまたはサードパーティのサービス（ERP など）を使用するには、[!UICONTROL Manage Stock] を無効にします。

- 製品レベルの設定でシステムのデフォルトが使用されている場合は、ストアの設定が上書きされます。

[!DNL Inventory Management] を有効にした場合、すべての設定を指定するには以下の説明を参照してください。

- [ グローバルオプションの設定 ](global-options.md) - カタログ全体に影響する設定は、システムのデフォルト設定と見なされます。

- [ 製品オプションの設定 ](product-options.md) - グローバルオプションを上書きする特定の製品の設定。

## [!DNL Inventory Management] の有効化または無効化

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Inventory]**」を選択します。

1. ![ 展開セレクター ](../assets/icon-display-expand.png)_製品ストックオプション_ を展開し、以下を設定します。

   ![ 商品ストックオプション ](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 在庫を管理し、すべての [!DNL Commerce] 機能を使用するには、**[!UICONTROL Manage Stock]** を `Yes` （デフォルト）に設定します。

   - [!DNL Inventory Management] を無効にするには、「**[!UICONTROL Use system value]**」チェックボックスの選択を解除し、「**[!UICONTROL Manage Stock]**」を「`No`」に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 店舗の在庫の管理

[ グローバルオプションの設定 ](global-options.md) を参照してください。

## 製品の在庫の管理

[ 製品オプションの設定 ](product-options.md) を参照してください。
