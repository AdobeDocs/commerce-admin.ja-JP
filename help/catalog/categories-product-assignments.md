---
title: カテゴリ製品の割り当て
description: の使用について [!UICONTROL Products in Category] 現在カテゴリに割り当てられている製品を制御するための設定。
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# カテゴリ製品の割り当て

カテゴリの場合は、 _[!UICONTROL Products in Category]_「 」セクションを使用して、現在カテゴリに割り当てられている製品を確認します。 各列の上部にある検索フィルターを使用して、カテゴリの製品を追加および削除します。 また、 [カテゴリルール](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ ) を使用して、一連の条件が満たされた場合に製品の選択を動的に変更できます。 詳しくは、 [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)) をクリックします。

>[!TIP]
>
>カテゴリルールの設定時に、製品は _並べ替え_, _一致_, _割り当てられた_、および _未指定_ その規則に従って **_のみ_** このカテゴリが保存されたとき。 カタログに追加する際に、ルールに従って新しい製品が割り当てられるようにするには、次の手順を実行します。 **は、各カテゴリを再度開く必要があります** ルールで製品を照合するために設定される また、いずれかの製品の在庫ステータスが `In Stock` または `Out of Stock` およびカテゴリ内の製品は、 _並べ替え_ 次によると **自動並べ替え** ルール：次をクリックする必要があります： **[!UICONTROL Save Category]**.

![カテゴリ製品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>カテゴリページで、 `Out of stock` 製品は常に表示されます **_次より後_** `In Stock` すべての並べ替えタイプを含む製品リストの製品。

>[!NOTE]
>
>The _Stock_ 列には、販売可能な製品数量が表示されます _**選択したカテゴリの範囲**_ のみ。 製品に対して複数の在庫を管理する場合は、他のスコープを表示するために、対応するスコープを切り替える必要があります _Stock_ 列の値 _カテゴリ製品_ グリッド。

## カテゴリルールの適用

{{ee-feature}}

1. 設定 **[!UICONTROL Match products by rule]** から `Yes`.

   自動並べ替えと条件のオプションが表示されます。

   ![規則で製品を照合するには](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. を設定します。 **[!UICONTROL Automatic Sorting]** 注文。

   この自動並べ替えは、現在の条件に基づいておこなわれます。

   - `Stock level`  — 上または下に移動します。
   - `Special price`  — 上または下に移動します。
   - `New Products`  — 最新の製品を先にリストします。
   - `Color`  — アルファベット順に色で並べ替えます。
   - `Name`  — 名前で昇順または降順に並べ替えます。
   - `SKU` - SKU で昇順または降順に並べ替え
   - `Price`  — 価格で昇順または降順に並べ替えます。

1. クリック **[!UICONTROL Add Condition]** 次の操作を実行します。

   - を選択します。 **[!UICONTROL Attribute]** それが条件の基礎です。
   - を選択します。 **[!UICONTROL Operator]** 式を形成するために必要です。
   - 次を入力します。 **[!UICONTROL Value]** それはマッチングされる。

   ![カテゴリルールに条件を追加](./assets/category-rule-create.png){width="600" zoomable="yes"}

   満たす条件の説明に使用する属性ごとに、この手順を繰り返します。 例えば、7 ～ 30 日前に作成された製品を照合するには、次の操作を行います。

   - 設定 **[!UICONTROL Date Created]** から `Less than 30`.
   - 設定 **[!UICONTROL Logic]** から `AND`.
   - 設定 **[!UICONTROL Date Modified]** から `Greater than 7`.

1. 完了したら、「 **[!UICONTROL Save Category]**.

### ページオプション

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Match products by rule] | カテゴリ内の製品のリストがカテゴリルールによって動的に生成されるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | カテゴリ商品のリストに並べ替え順を自動的に適用します。 オプション： <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | ルールに別の条件を追加します。 |

{style="table-layout:auto"}

### ページ条件

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Attribute] | 条件の基準として使用される属性を決定します。 オプション： <br/>**[!UICONTROL Clone Category ID(s)]**— カテゴリ ID に基づく複数のカテゴリから、製品のクローンを、並べ替えや順序なしで動的に作成します。<br/>**[!UICONTROL Color]**  — 色に基づく製品が含まれます。 <br/>**[!UICONTROL Date Created (days ago)]**— 商品がカタログに追加されてからの日数に基づく商品が含まれます。<br/>**[!UICONTROL Date Modified (days ago)]**  — 製品が最後に変更されてからの日数に基づく製品が含まれます。 <br/>**[!UICONTROL Name]**— 製品名に基づく製品が含まれます。<br/>**[!UICONTROL Price]**  — 価格に基づく製品が含まれます。 <br/>**[!UICONTROL Quantity]**— 在庫数に基づく製品が含まれます。<br/>** SKU **- SKU に基づく製品が含まれます。 |
| [!UICONTROL Operator] | 条件を満たすために属性値に適用される演算子を指定します。 演算子が指定されていない場合、 `Equal` がデフォルトとして使用されます。 オプション： `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 属性が条件を満たす必要がある値を指定します。 |
| [!UICONTROL Logic] | 複数の条件を定義するために使用され、別の条件が追加された場合にのみ表示されます。 オプション： `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>構成可能な製品の数量と子オプションは、販売可能な子製品の数量をすべて組み合わせて計算されます。 設定可能な製品の例を考えてみましょう。 _持久力フィットネスタンク_ 紫色、赤、黄色の各色のオプションと、それぞれ異なる量が表示されます。 このシナリオでは、親製品数量は、紫、赤、黄色の子製品の合計販売可能数量です。

## コントロール


## ページコントロール

{{ee-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![リストとして表示](../assets/icon-view-list.png) | リスト形式で表示 |
| ![タイルとして表示](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![切り替えなし](../assets/toggle-no.png) | ルールで一致 — いいえ |
| ![はいを切り替え](../assets/toggle-yes.png) | ルールで一致 — はい |
| ![コントローラを移動](../assets/icon-move.png) | ドラッグ&amp;ドロップコントロールを使用すると、商品を取得して、グリッドの現在のページの別の位置に移動できます。 詳しくは、 [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![位置コントローラ](../assets/control-position.png) | リスト内の商品の位置を決定します。 |

{style="table-layout:auto"}

## ページコントロール

{{ce-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![選択したチェックボックス](../assets/checkbox-selected.png) | すべての製品を選択するか、すべての選択を解除するには、最初の列のヘッダーにあるチェックボックスを使用します。 最初の行のコントロールは、検索の種類を決定し、任意のレコードを含めるように設定するか、カテゴリに割り当てられているレコードまたは割り当てられていないレコードのみを含めることができます。 各行の最初の列にあるチェックボックスは、カテゴリに追加する製品を示します。 オプション： `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 各列の最上部にあるフィルタコントロールを使用して、[ すべてを選択 ] の設定に応じて、リストに含めるかリストから除外する特定の値を入力できます。 |
| [!UICONTROL Reset Filter] | すべての検索フィルタをクリアします。 |
| [!UICONTROL Search] | フィルタ条件に基づいてカタログを検索し、結果を表示します。 |

{style="table-layout:auto"}
