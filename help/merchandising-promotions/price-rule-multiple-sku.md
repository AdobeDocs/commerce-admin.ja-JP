---
title: 複数の SKU を持つカタログ価格ルール
description: 単一のカタログ価格ルールを複数の SKU に適用する方法を説明します。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 複数の SKU を持つカタログ価格ルール

1 つのカタログ価格ルールを複数の SKU に適用して、製品、ブランド、カテゴリに基づいて様々なプロモーションを作成できます。 このルールを作成する際には、選択した SKU に一致する条件を設定します。 ルールを作成する際に、グリッドから SKU を簡単に参照して選択できます。

## 手順 1. 製品属性のストアフロントのプロパティの確認

開始する前に、 [ストアフロント プロパティ](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) の `sku` 属性の設定 `Use in Promo Rules`.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 検索フィルターの上部にある _[!UICONTROL Attribute Code]_列、を入力 `sku` をクリックして、**[!UICONTROL Search]**.

1. クリックすると、 `sku` 編集モードの属性。

1. 左側のパネルで、 **[!UICONTROL Storefront Properties]** そして、次のことを確認します **[!UICONTROL Use for Promo Rule Conditions]** はに設定されています。 `Yes`.

1. プロパティの値を変更した場合は、 **[!UICONTROL Save Attribute]**.

## 手順 2. 複数の SKU への価格ルールの適用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. 次のいずれかの操作を行います。

   - 手順に従ってを作成します [カタログ価格ルール](price-rules-catalog.md).
   - 既存のカタログ価格ルールを開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Conditions]** を選択し、次の手順を実行します。

   - 最初の行で、最初のパラメーターをに設定します。 `ANY`.

     ![カタログ価格ルール条件 – ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - クリック _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)）を次の行の先頭に追加し、の下のリストに追加します **[!UICONTROL Product Attribute]**&#x200B;を選択し、 `SKU`.

     ![カタログ価格ルール条件 – SKU は](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - 比較のために、オプションがあります。 SKU のリストから少なくとも 1 つを見つける場合： `select is one of`. 適用するすべての SKU を特定する場合は、を選択します。 `is`. を選択することをお勧めします。 `is one of`.

     ![カタログ価格ルール条件 – SKU は](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - 条件を完了するには、「その他」（**...**）リンクし、 _選択_ （![リストアイコン](../assets/icon-list-chooser.png)）アイコンで使用可能な製品のリストを表示します。

     ![カタログ価格ルール条件 – 複数の SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 参照、フィルターまたは検索して、追加する SKU を見つけます。 リストで、含める各製品のチェックボックスを選択します。

   - クリック **[!UICONTROL Save and Apply]** SKU を条件に追加します。

     ![カタログ価格ルール条件 – 複数の SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. 次のいずれかを含め、ルールを完了します [アクション](price-rules-catalog.md) 条件が満たされた場合に取得されます。

1. ルールが完了したら、 **[!UICONTROL Save]**.

{{new-price-rule}}
