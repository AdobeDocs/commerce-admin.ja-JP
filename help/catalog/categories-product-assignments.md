---
title: カテゴリ製品割り当て
description: の使用について説明します [!UICONTROL Products in Category] カテゴリに現在割り当てられている製品を制御する設定です。
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# カテゴリ製品割り当て

カテゴリには、 _[!UICONTROL Products in Category]_現在カテゴリに割り当てられている製品を確認するセクション 各列の上部にある検索フィルターは、商品の追加とカテゴリからの削除に使用されます。 を使用することもできます。 [カテゴリルール](../merchandising-promotions/category-product-rules.md) （ ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ）を使用して、一連の条件が満たされた場合に商品の選択範囲を動的に変更します。 詳しくは、 [ビジュアルマーチャンダイザー](../merchandising-promotions/visual-merchandiser.md)）に設定します。

>[!TIP]
>
>カテゴリルールの設定時に、製品は次のようになります _並べ替え_, _matched_, _割り当て_、および _unassigned_ その規則に従って **_のみ_** このカテゴリの保存時。 新しい製品をカタログに追加すると、その製品がルールに従って確実に割り当てられるようにするには、次の操作を行います **各カテゴリを再保存する必要があります** これは、ルール別に製品を照合するように設定されます。 また、製品の在庫ステータスがに変更された場合 `In Stock` または `Out of Stock` カテゴリのとの製品は次のとおりです _並べ替え_ ～によれば **自動並べ替え** ルールです。をクリックする必要があります **[!UICONTROL Save Category]**.

![カテゴリ製品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>カテゴリページで、 `Out of stock` 製品は常に表示されます **_後_** `In Stock` すべての並べ替えタイプを含む製品リスト上の製品

>[!NOTE]
>
>この _在庫_ 列には、の売り上げ可能な製品数量が表示されます _**選択したカテゴリの範囲**_ のみ。 複数の在庫が製品に対して管理されている場合は、対応するスコープを切り替えて他を表示する必要があります _在庫_ の列値 _カテゴリ製品_ グリッド。

## カテゴリルールの適用

{{ee-feature}}

1. を設定 **[!UICONTROL Match products by rule]** 対象： `Yes`.

   自動並べ替えと条件のオプションが表示されます。

   ![製品をルールで照合するには](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. を **[!UICONTROL Automatic Sorting]** オーダー。

   この自動並べ替えは、現在の条件に基づいて行われます。

   - `Stock level`  – 上または下に移動します。
   - `Special price`  – 上または下に移動します。
   - `New Products`  – 新しい製品から順にリストします。
   - `Color`  – 色順に並べ替えます。
   - `Name`  – 名前で昇順または降順に並べ替えます。
   - `SKU` - SKU で昇順または降順に並べ替え
   - `Price`  – 価格で昇順または降順に並べ替えます。

1. クリック **[!UICONTROL Add Condition]** 次の手順を実行します。

   - を選択します。 **[!UICONTROL Attribute]** それが条件の基礎です。
   - を選択します。 **[!UICONTROL Operator]** 式の形成に必要です。
   - を入力 **[!UICONTROL Value]** それは一致する予定だ。

   ![カテゴリルールへの条件の追加](./assets/category-rule-create.png){width="600" zoomable="yes"}

   満たす条件を記述するために使用する属性ごとに、このプロセスを繰り返します。 例えば、7～30 日前に作成された製品を照合するには、次の手順を実行します。

   - を設定 **[!UICONTROL Date Created]** 対象： `Less than 30`.
   - を設定 **[!UICONTROL Logic]** 対象： `AND`.
   - を設定 **[!UICONTROL Date Modified]** 対象： `Greater than 7`.

1. 完了したら、 **[!UICONTROL Save Category]**.

### ページオプション

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Match products by rule] | カテゴリ内の製品のリストがカテゴリルールによって動的に生成されるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | カテゴリ製品のリストに並べ替え順を自動的に適用します。 オプション： <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | ルールに別の条件を追加します。 |

{style="table-layout:auto"}

### ページ条件

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Attribute] | 条件の基礎として使用する属性を指定します。 オプション： <br/>**[!UICONTROL Clone Category ID(s)]**- カテゴリ ID に基づいて、複数のカテゴリから、並べ替えや順序なしで製品を動的にクローン化します。<br/>**[!UICONTROL Color]**  – 色に基づいて製品を含めます。 <br/>**[!UICONTROL Date Created (days ago)]**– 製品がカタログに追加されてからの経過日数に基づいて、製品が含まれます。<br/>**[!UICONTROL Date Modified (days ago)]**  – 製品が最後に変更されてからの日数に基づいて製品を含みます。 <br/>**[!UICONTROL Name]**– 製品名に基づいて製品を含めます。<br/>**[!UICONTROL Price]**  – 価格に基づいて製品を組み込みます。 <br/>**[!UICONTROL Quantity]**– 在庫数に基づいて製品を含みます。<br/>** SKU **- SKU に基づく製品を含みます。 |
| [!UICONTROL Operator] | 条件を満たすために属性値に適用する演算子を指定します。 演算子を指定しない場合、 `Equal` がデフォルトとして使用されます。 オプション： `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 属性が条件を満たす必要がある値を指定します。 |
| [!UICONTROL Logic] | 複数の条件の定義に使用し、別の条件が追加された場合にのみ表示されます。 オプション： `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>子オプションを持つ設定可能な製品の数量は、すべての販売可能な子製品の数量を組み合わせて計算されます。 設定可能な商品の例について考えてみます _耐久性フィットネスタンクトップ_ 紫、赤、黄のカラーオプションとそれぞれの異なる量を使用します。 このシナリオでは、親商品の数量は、紫色、赤色、黄色の子商品の合計販売可能数量です。

## コントロール


## ページコントロール

{{ee-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![リストとして表示](../assets/icon-view-list.png) | リストとして表示 |
| ![タイルとして表示](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![いいえ切り替え](../assets/toggle-no.png) | ルールによる一致 – いいえ |
| ![「はい」を切り替え](../assets/toggle-yes.png) | ルールによる一致 – はい |
| ![コントローラを移動](../assets/icon-move.png) | ドラッグ&amp;ドロップコントロールを使用すると、製品を選択して、グリッドの現在のページ内の別の位置に移動できます。 詳しくは、 [ビジュアルマーチャンダイザー](../merchandising-promotions/visual-merchandiser.md). |
| ![位置コントローラ](../assets/control-position.png) | リスト内の商品の位置を決定します。 |

{style="table-layout:auto"}

## ページコントロール

{{ce-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![選択済みチェックボックス](../assets/checkbox-selected.png) | 最初の列のヘッダーにあるチェックボックスを使用して、すべての製品を選択するか、すべての選択をクリアします。 最初の行のコントロールは検索の種類を決定し、任意のレコードを含むように設定することも、カテゴリに割り当てられているか割り当てられていないレコードのみを含むように設定することもできます。 各行の最初の列にあるチェックボックスで、カテゴリに追加する製品を指定します。 オプション： `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 各列の上部にあるフィルターコントロールを使用して、「すべてを選択」の設定に応じて、リストに含める値またはリストから除外する値を入力することができます。 |
| [!UICONTROL Reset Filter] | すべての検索フィルターをクリアします。 |
| [!UICONTROL Search] | フィルタ条件に基づいてカタログを検索し、結果を表示します。 |

{style="table-layout:auto"}
