---
title: 共有カタログへの製品の追加
description: 製品を共有カタログに個別に、またはカテゴリ別にグループで追加する方法について説明します。
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 共有カタログへの製品の追加

製品は、個別に、またはカテゴリ別に複数の製品のグループとして、共有カタログに追加できます。

複雑な製品（バンドル、グループ化、設定可能など）が共有カタログのストアフロントから表示されるようにするには、次の要件を満たす必要があります。

- すべての [ 関連製品 ](../catalog/product-configurations.md) およびオプションは、同じ共有カタログに割り当てられ、プライマリカタログで有効になっている必要があります。
- [ 設定可能 ](../catalog/product-create-configurable.md) および [ グループ化 ](../catalog/product-create-grouped.md) 製品の場合、有効な関連製品のみが表示されます。
- [ バンドル ](../catalog/product-create-bundle.md) 製品の場合、すべてのオプションを共有カタログに含める必要があります。

  ![ カタログ用の製品を選択 ](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 方法 1：単一の製品を追加する

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. グリッドに追加する製品の _[!UICONTROL Action]_列に移動し、「**[!UICONTROL Edit]**」をクリックします。

1. 下にスクロールして、「展開セレクター ![ 展開セレクター ](../assets/icon-display-expand.png) 「_[!UICONTROL Product in Shared Catalogs]_」セクションを展開し、次の操作を実行します。

   - 製品を表示する各共有カタログのチェックボックスをオンにします。 すべてのカタログを選択するには、「**[!UICONTROL Select all]**」をクリックします。

     ![ 共有カタログ内の製品 ](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     選択した各カタログの名前が「_[!UICONTROL Shared Catalogs]_」フィールドに表示されます。

     ![ 割り当てられている共有カタログ ](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - 「**[!UICONTROL Done]**」をクリックして、設定を保存します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 方法 2：複数の製品を追加する

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Shared Catalogs]** に移動します。

1. グリッド内の共有カタログの場合は、[_[!UICONTROL Action]_] 列に移動して [**[!UICONTROL Set Pricing and Structure]**] を選択します。

1. カテゴリ ツリーで、次のいずれかの操作を行います。

   - すべての製品を含めるには、**[!UICONTROL Select all]** をクリックするか、親カテゴリのチェックボックスをオンにします。
   - 製品の特定のカテゴリを含めるには、含める各カテゴリのチェックボックスをオンにします。
   - 個々の製品を含めるか除外するには、製品のチェックボックスを選択または選択解除します。

   ツリーの各カテゴリの下の表記は、共有カタログに現在含まれているカテゴリの製品数を示しています。 [ ルートカテゴリ ](../catalog/category-root.md) の下の表記には、共有カタログに対して現在選択されているすべてのカテゴリの製品の合計数が表示されます。

1. グリッドにカテゴリ製品を表示するには、ツリーでカテゴリの名前をクリックします。

   カテゴリを選択すると、次の処理が行われます。

   - グリッドの最初の列の切替スイッチは、選択した各製品に対して `On` に設定されます。
   - 製品が複数のカテゴリに割り当てられ、そのうちの 1 つで省略された場合、他のカテゴリおよび [ カタログ検索 ](../catalog/search.md) を通じて使用できます。
   - 選択した製品の [ カテゴリ権限 ](../catalog/category-permissions.md) が自動的に `Allow` に設定されます。
