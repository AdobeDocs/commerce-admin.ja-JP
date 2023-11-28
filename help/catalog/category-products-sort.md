---
title: カテゴリ製品の並べ替え
description: カテゴリ内の製品の位置を手動で定義する方法、または定義済みの並べ替え順を適用する方法について説明します。
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# カテゴリ製品の並べ替え

{{ee-feature}}

カテゴリ内の製品の位置は、製品を位置にドラッグ&amp;ドロップするか、定義済みの並べ替え順を適用することで、手動で指定できます。 デフォルトでは、製品は在庫レベル、年齢、色、名前、SKU、価格で並べ替えることができます。 自動並べ替えは、現在の並べ替え順を上書きし、手動で設定したドラッグ&amp;ドロップの位置をリセットします。 リストに含める製品の色の並べ替え順と最小在庫レベルは、 [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) 設定。

>[!NOTE]
>
>カテゴリページで、 `Out of stock` 製品は常に表示されます **_次より後_** `In Stock` すべての並べ替えタイプを含む製品リストの製品。

各カテゴリのオプションを個別に設定できます [ストア表示](../stores-purchase/stores.md#add-stores) 製品の選択、リスト内での相対位置、カテゴリルールで使用可能な属性を決定します。 しかし、一人が **_global_** カタログ内の並べ替え順と商品の位置。これらはすべての [ストア表示](../stores-purchase/store-views.md)、ストア、Web サイト。

## 手順 1：設定の範囲を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 必要に応じて、 **[!UICONTROL Store View]** ここで、設定が適用されます。

   マルチストアのインストールの場合、 _[!UICONTROL Store View]_を設定すると、ストア内の使用可能なすべてのビューに並べ替え順が適用されます。

1. 左側のカテゴリツリーで、編集するカテゴリを選択します。

   ![カテゴリツリー](./assets/category-selected.png){width="700" zoomable="yes"}

## 手順 2：製品の並べ替え

>[!NOTE]
>
>カテゴリを製品属性で並べ替えると、同じ属性値を持つ製品も、製品属性で並べ替えられます _[!UICONTROL Product ID]_昇順に並べ替えられます。

Adobe Analytics の _[!UICONTROL Products in Category]_「 」セクションで、タイル ( ![タイルを表示](../assets/icon-view-tiles.png) ) アイコンをクリックして、製品タイルをグリッドに表示します。 手動または自動の方法を使用して、製品を並べ替えます。

![製品タイル](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### 方法 1：手動による並べ替え

1. 設定 **[!UICONTROL Sort Order]** を選択します。

   ![並べ替え順](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. 新しい並べ替え順を適用するには、 **[!UICONTROL Sort]**.

1. 並べ替え順を保存するには、 **[!UICONTROL Save Category]**.

1. プロンプトが表示されたら、無効なインデクサーを更新します。

### 方法 2：自動並べ替え

1. 設定 **[!UICONTROL Match products by rule]** (![はいを切り替え](../assets/toggle-yes.png)) から `Yes`.


1. 設定 **[!UICONTROL Automatic Sorting]** を選択します。

1. カテゴリルールを作成するには、次の手順に従います。

## 手順 3：カテゴリルールの作成

1. 設定 **[!UICONTROL Match products by rule]** (![はいを切り替え](../assets/toggle-yes.png)) から `Yes`.

1. クリック **[!UICONTROL Add Condition]**.

1. を選択します。 **[!UICONTROL Attribute]** それが条件の基礎です。

1. 設定 **[!UICONTROL Operator]** を次のいずれかに変更します。

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. 適切な **[!UICONTROL Value]**.

   ![カテゴリ条件](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. 別の条件を追加するには、 **[!UICONTROL Add Condition]** プロセスを繰り返します。

## 手順 4：保存、更新、検証

1. 完了したら、「 **[!UICONTROL Save Category]**.

1. キャッシュを更新するよう求められたら、 **[!UICONTROL Cache Management]** 無効なキャッシュを更新します。

1. ストアフロントで、製品の選択、並べ替え、カテゴリルールが正しく機能することを確認します。

   調整が必要な場合は、設定を変更して、もう一度試してください。
