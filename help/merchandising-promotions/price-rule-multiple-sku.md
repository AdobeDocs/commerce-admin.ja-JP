---
title: 複数の SKU を使用するカタログ価格ルール
description: 単一のカタログ価格ルールを複数の SKU に適用する方法を説明します。
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 複数の SKU を使用するカタログ価格ルール

単一のカタログ価格ルールを複数の SKU に適用できるので、製品、ブランド、カテゴリに基づいて様々なプロモーションを作成できます。 このルールを作成する際に、選択した SKU に一致する条件を設定する必要があります。 ルールを作成する際に、グリッドから SKU を簡単に参照して選択できます。

## 手順 1. 製品属性のストアフロントプロパティの検証

開始する前に、 [ストアフロントのプロパティ](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) の `sku` 属性が `Use in Promo Rules`.

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 」をクリックします。 _[!UICONTROL Attribute Code]_列、入力 `sku` をクリックします。**[!UICONTROL Search]**.

1. クリックして、 `sku` 属性を編集モードで使用します。

1. 左側のパネルで、 **[!UICONTROL Storefront Properties]** そして確かに **[!UICONTROL Use for Promo Rule Conditions]** が `Yes`.

1. プロパティの値を変更した場合、 **[!UICONTROL Save Attribute]**.

## 手順 2. 複数の SKU への価格ルールの適用

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. 次のいずれかの操作を行います。

   - 手順に従って、 [カタログ価格ルール](price-rules-catalog.md).
   - 既存のカタログ価格ルールを開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Conditions]** 」セクションに移動し、次の操作を行います。

   - 最初の行で、最初のパラメーターをに設定します。 `ANY`.

     ![カタログ価格ルール条件 — 任意](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - クリック _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) を次の行の先頭に配置し、リスト内の **[!UICONTROL Product Attribute]**&#x200B;をクリックし、 `SKU`.

     ![カタログ価格ルールの条件 — SKU は次のいずれかです。](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - 比較には、オプションがあります。 SKU のリストから少なくとも 1 つを見つけたい場合、 `select is one of`. 適用する必要のある SKU のグループを特定する場合は、 `is`. を選択することをお勧めします。 `is one of`.

     ![カタログ価格ルールの条件 — SKU は次のいずれかです。](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - 条件を完了するには、その他 (**...**) リンクをクリックし、 _選択_ (![リストアイコン](../assets/icon-list-chooser.png)) アイコンをクリックします。

     ![カタログ価格ルールの条件 — 複数の SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 参照、フィルタリングまたは検索を行って、追加する SKU を見つけます。 リストで、含める各製品のチェックボックスを選択します。

   - クリック **[!UICONTROL Save and Apply]** をクリックして SKU を条件に追加します。

     ![カタログ価格ルールの条件 — 複数の SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. ルールを完了します。このルールには、 [アクション](price-rules-catalog.md) 条件が満たされたときに取られる。

1. ルールが完了したら、「 **[!UICONTROL Save]**.

{{new-price-rule}}
