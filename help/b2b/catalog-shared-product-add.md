---
title: 共有カタログに商品を追加する
description: 個別の製品、またはカテゴリ別のグループに製品を共有カタログに追加する方法について説明します。
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# 共有カタログに商品を追加する

製品は、個別に、またはカテゴリ別に複数の製品のグループに共有カタログに追加できます。

複雑な製品（バンドル、グループ化、設定など）を共有カタログのストアフロントから表示するには、次の要件を満たす必要があります。

- すべて [関連製品](../catalog/product-configurations.md) およびオプションは、同じ共有カタログに割り当てられ、プライマリカタログで有効にする必要があります。
- の場合 [設定可能](../catalog/product-create-configurable.md) および [グループ化](../catalog/product-create-grouped.md) 製品を選択すると、有効になっている関連製品のみが表示されます。
- の [バンドル](../catalog/product-create-bundle.md) 製品の場合は、すべてのオプションを共有カタログに含める必要があります。

  ![カタログの製品を選択](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 方法 1：単一の製品を追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 追加するグリッド内の製品について、 _[!UICONTROL Action]_列とクリック&#x200B;**[!UICONTROL Edit]**.

1. 下にスクロールし、展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Product in Shared Catalogs]_」セクションに移動し、次の操作を行います。

   - 商品を表示する各共有カタログのチェックボックスをオンにします。 すべてのカタログを選択するには、 **[!UICONTROL Select all]**.

     ![共有カタログ内の商品](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     選択した各カタログの名前が _[!UICONTROL Shared Catalogs]_フィールドに入力します。

     ![割り当てられた共有カタログ](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - クリック **[!UICONTROL Done]** をクリックして設定を保存します。

1. 完了したら、「 **[!UICONTROL Save]**.

## 方法 2：複数の製品を追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. グリッド内の共有カタログについて、 _[!UICONTROL Action]_列と選択&#x200B;**[!UICONTROL Set Pricing and Structure]**.

1. カテゴリツリーで、次のいずれかの操作を行います。

   - すべての製品を含めるには、 **[!UICONTROL Select all]** または親カテゴリのチェックボックスをオンにします。
   - 特定の商品カテゴリを含めるには、含める各カテゴリのチェックボックスをオンにします。
   - 個々の製品を含めるか除外するには、製品のチェックボックスをオンまたはオフにします。

   ツリー内の各カテゴリの下の表記は、共有カタログに現在含まれているカテゴリの製品数を示します。 以下の表記 [ルートカテゴリ](../catalog/category-root.md) 共有カタログに対して現在選択されているすべてのカテゴリの製品の合計数を表示します。

1. グリッドにカテゴリ商品を表示するには、ツリーのカテゴリ名をクリックします。

   カテゴリを選択すると、次のことが発生します。

   - グリッドの最初の列の切り替えは、に設定されます。 `On` 選択した製品ごとに
   - 製品が複数のカテゴリに割り当てられ、その中の 1 つに省略された場合、他のカテゴリや [カタログ検索](../catalog/search.md).
   - システムが自動的にを設定 [カテゴリ権限](../catalog/category-permissions.md) から `Allow` 選択した製品の
