---
title: カテゴリ製品の並べ替え
description: 手動で、または事前定義済みの並べ替え順を適用してカテゴリ内の製品の位置を定義する方法を説明します。
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# カテゴリ製品の並べ替え

{{ee-feature}}

カテゴリ内の商品の位置は、商品を位置にドラッグ&amp;ドロップするか、事前に定義された並べ替え順を適用することで、手動で指定できます。 デフォルトでは、商品は在庫レベル、年齢、カラー、名前、SKU、価格で並べ替えることができます。 自動ソートは、現在のソート順序を上書きし、手動で設定したドラッグ アンド ドロップ位置をリセットします。 色の並べ替え順序と、リストに含める製品に必要な最小在庫レベルは、[&#x200B; ビジュアルマーチャンダイザー &#x200B;](../configuration-reference/catalog/visual-merchandiser.md) 設定で設定します。

カテゴリオプションを [&#x200B; ストア表示 &#x200B;](../stores-purchase/stores.md#add-stores) ごとに個別に設定して、商品の選択、リスト内の相対的な位置、カテゴリルールに使用できる属性を決定することができます。 ただし、カタログ内には単一の **_グローバル_** 並べ替え順と製品位置があり、これらは [&#x200B; ストア表示 &#x200B;](../stores-purchase/store-views.md)、ストア、web サイトすべてで共有されます。

## 手順 1：設定の範囲を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. 必要に応じて、設定が適用される **[!UICONTROL Store View]** を選択します。

   マルチストアインストールの場合、_[!UICONTROL Store View]_&#x200B;設定は、ストア内の使用可能なすべてのビューに並べ替え順を適用します。

1. 左側のカテゴリ ツリーで、編集するカテゴリを選択します。

   ![&#x200B; カテゴリツリー &#x200B;](./assets/category-selected.png){width="700" zoomable="yes"}

## 手順 2：製品の並べ替え

>[!NOTE]
>
>カテゴリを製品属性で並べ替える場合、同じ属性値を持つ製品も _[!UICONTROL Product ID]_&#x200B;の昇順で並べ替えられます。

「_[!UICONTROL Products in Category]_」セクションでタイル（![&#x200B; タイルを表示 &#x200B;](../assets/icon-view-tiles.png)）アイコンをクリックして、製品タイルをグリッドで表示します。 手動または自動のいずれかの方法を使用して、製品を並べ替えます。

![&#x200B; 製品タイル &#x200B;](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### 方法 1：手動ソート

1. **[!UICONTROL Sort Order]** を好みに合わせて設定します。

   ![&#x200B; 並べ替え順 &#x200B;](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. 新しい並べ替え順を適用するには、[**[!UICONTROL Sort]**] をクリックします。

1. 並べ替え順を保存するには、「**[!UICONTROL Save Category]**」をクリックします。

1. プロンプトが表示されたら、無効なインデクサーを更新します。

### 方法 2：自動ソート

1. 「**[!UICONTROL Match products by rule]**」（![&#x200B; 切り替え yes](../assets/toggle-yes.png)）を「`Yes`」に設定します。


1. **[!UICONTROL Automatic Sorting]** を好みに合わせて設定します。

1. カテゴリルールを作成するには、次の手順に従います。

## 手順 3：カテゴリルールの作成

1. 「**[!UICONTROL Match products by rule]**」（![&#x200B; 切り替え yes](../assets/toggle-yes.png)）を「`Yes`」に設定します。

1. 「**[!UICONTROL Add Condition]**」をクリックします。

1. 条件の基礎となる **[!UICONTROL Attribute]** を選択します。

1. **[!UICONTROL Operator]** を次のいずれかに設定します。

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. 適切な **[!UICONTROL Value]** を入力します。

   ![&#x200B; カテゴリ条件 &#x200B;](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. 別の条件を追加するには、「**[!UICONTROL Add Condition]**」をクリックして手順を繰り返します。

## 手順 4：保存、更新、検証

1. 完了したら、「**[!UICONTROL Save Category]**」をクリックします。

1. キャッシュを更新するように求めるメッセージが表示されたら、[ **[!UICONTROL Cache Management]** ] をクリックして無効な各キャッシュを更新します。

1. ストアフロントで、製品の選択、並べ替えおよびカテゴリルールが正しく機能していることを確認します。

   調整が必要な場合は、設定を変更して、もう一度試してください。
