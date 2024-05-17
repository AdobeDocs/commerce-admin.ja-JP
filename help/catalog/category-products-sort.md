---
title: カテゴリ製品の並べ替え
description: 手動で、または事前定義済みの並べ替え順を適用してカテゴリ内の製品の位置を定義する方法を説明します。
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# カテゴリ製品の並べ替え

{{ee-feature}}

カテゴリ内の商品の位置は、商品を位置にドラッグ&amp;ドロップするか、事前に定義された並べ替え順を適用することで、手動で指定できます。 デフォルトでは、商品は在庫レベル、年齢、カラー、名前、SKU、価格で並べ替えることができます。 自動ソートは、現在のソート順序を上書きし、手動で設定したドラッグ アンド ドロップ位置をリセットします。 リストに含める製品に必要な色の並べ替え順序と最小在庫レベルは、 [ビジュアルマーチャンダイザー](../configuration-reference/catalog/visual-merchandiser.md) 設定。

>[!NOTE]
>
>カテゴリページで、 `Out of stock` 製品は常に表示されます **_後_** `In Stock` すべての並べ替えタイプを含む製品リスト上の製品

カテゴリオプションは、ごとに個別に設定できます [ストア表示](../stores-purchase/stores.md#add-stores) 商品の選択、リスト内の相対的な位置、カテゴリルールで使用できる属性を決定します。 ただし、1 つだけがあります。 **_global_** カタログ内の並べ替え順と製品位置。すべてのユーザー間で共有されます [ビューを保存](../stores-purchase/store-views.md)、ストア、web サイトなどの情報を管理できます。

## 手順 1：設定の範囲を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 必要に応じて、 **[!UICONTROL Store View]** 設定が適用される場所。

   マルチストアインストールの場合、 _[!UICONTROL Store View]_を設定すると、ストア内の使用可能なすべてのビューに並べ替え順が適用されます。

1. 左側のカテゴリ ツリーで、編集するカテゴリを選択します。

   ![カテゴリツリー](./assets/category-selected.png){width="700" zoomable="yes"}

## 手順 2：製品の並べ替え

>[!NOTE]
>
>カテゴリを製品属性で並べ替える場合、属性値が同じ製品も _[!UICONTROL Product ID]_昇順。

が含まれる _[!UICONTROL Products in Category]_セクションで、タイル（ ![タイルの表示](../assets/icon-view-tiles.png) ）アイコンで製品タイルをグリッドで表示します。 手動または自動のいずれかの方法を使用して、製品を並べ替えます。

![製品タイル](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### 方法 1：手動ソート

1. を設定 **[!UICONTROL Sort Order]** ご希望に合わせてください。

   ![並べ替え順序](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. 新しい並べ替え順を適用するには、をクリックします。 **[!UICONTROL Sort]**.

1. 並べ替え順を保存するには、をクリックします。 **[!UICONTROL Save Category]**.

1. プロンプトが表示されたら、無効なインデクサーを更新します。

### 方法 2：自動ソート

1. を設定 **[!UICONTROL Match products by rule]** （![「はい」を切り替え](../assets/toggle-yes.png)） ～ `Yes`.


1. を設定 **[!UICONTROL Automatic Sorting]** ご希望に合わせてください。

1. カテゴリルールを作成するには、次の手順に従います。

## 手順 3：カテゴリルールの作成

1. を設定 **[!UICONTROL Match products by rule]** （![「はい」を切り替え](../assets/toggle-yes.png)） ～ `Yes`.

1. クリック **[!UICONTROL Add Condition]**.

1. を選択します。 **[!UICONTROL Attribute]** それが条件の基礎です。

1. を設定 **[!UICONTROL Operator]** を次のいずれかに変更します。

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. 適切なを入力 **[!UICONTROL Value]**.

   ![カテゴリ条件](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. 別の条件を追加するには、をクリックします **[!UICONTROL Add Condition]** そしてプロセスを繰り返します。

## 手順 4：保存、更新、検証

1. 完了したら、 **[!UICONTROL Save Category]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** 無効な各キャッシュを更新します。

1. ストアフロントで、製品の選択、並べ替えおよびカテゴリルールが正しく機能していることを確認します。

   調整が必要な場合は、設定を変更して、もう一度試してください。
