---
title: カテゴリ製品の割り当て
description: '[!UICONTROL Products in Category]設定を使用して、現在カテゴリに割り当てられている製品を制御する方法について説明します。'
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
TQID: https://experienceleague.adobe.com/jP75K4-JqaEJUbu733h6crHkX80w8idR9KHbVQF12ag
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 791
ht-degree: 0%

---

# カテゴリ製品の割り当て

カテゴリの場合は、_[!UICONTROL Products in Category]_セクションを使用して、現在そのカテゴリに割り当てられている製品を確認します。 各列の上部にある検索フィルターを使用して、商品をカテゴリに追加したりカテゴリから削除したりします。 また、[ カテゴリルール ](../merchandising-promotions/category-product-rules.md) （![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ）を使用して、一連の条件が満たされたときに商品の選択を動的に変更することもできます。 詳しくは、[Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)）を参照してください。

>[!TIP]
>
>カテゴリルールの設定中、このカテゴリを保存すると、そのルール **_のみ_**&#x200B;に従って、製品は&#x200B;_並べ替え_、_一致_、_割り当て_&#x200B;および&#x200B;_未割り当て_&#x200B;になります。 カタログに追加する際に、ルールに従って新しい製品が割り当てられていることを確認するには、ルールで製品に一致するように設定されている各カテゴリ **を**&#x200B;保存する必要があります。 また、商品の在庫状況が`In Stock`または`Out of Stock`に変更され、カテゴリ内の商品が&#x200B;**自動並べ替え** ルールに従って&#x200B;_並べ替え_&#x200B;される場合は、**[!UICONTROL Save Category]**&#x200B;をクリックする必要があります。

![ カテゴリ製品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>_Stock_&#x200B;列には、_**選択したカテゴリ スコープ**_&#x200B;に対してのみ使用可能な製品数量が表示されます。 商品に対して複数の在庫を管理する場合は、対応する範囲を切り替えて、_カテゴリー商品_ グリッドに他の&#x200B;_在庫_&#x200B;列の値を表示する必要があります。

## カテゴリルールの適用

{{ee-feature}}

1. **[!UICONTROL Match products by rule]**&#x200B;を`Yes`に設定します。

   自動並べ替えと条件オプションが表示されます。

   ![ ルール ](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}で製品を照合する

1. **[!UICONTROL Automatic Sorting]**&#x200B;注文を設定します。

   この自動並べ替えは、現在の状況に基づいています。

   - `Stock level` – 上または下に移動します。
   - `Special price` – 上または下に移動します。
   - `New Products` – 最新の製品を最初にリストします。
   - `Color` - アルファベット順にカラーで並べ替えます。
   - `Name` – 名前で昇順または降順に並べ替えます。
   - `SKU` - SKUで昇順または降順に並べ替え
   - `Price` – 昇順または降順で価格で並べ替えます。

1. **[!UICONTROL Add Condition]**&#x200B;をクリックし、次の操作を行います。

   - 条件の基となる&#x200B;**[!UICONTROL Attribute]**&#x200B;を選択します。
   - 式の形成に必要な&#x200B;**[!UICONTROL Operator]**&#x200B;を選択します。
   - 一致させる&#x200B;**[!UICONTROL Value]**&#x200B;を入力します。

   ![ カテゴリルールに条件を追加](./assets/category-rule-create.png){width="600" zoomable="yes"}

   各属性に対してこのプロセスを繰り返して、満たすべき条件を記述します。 例えば、7 ～ 30日前に作成された製品を照合するには、次の操作を行います。

   - **[!UICONTROL Date Created]**&#x200B;を`Less than 30`に設定します。
   - **[!UICONTROL Logic]**&#x200B;を`AND`に設定します。
   - **[!UICONTROL Date Modified]**&#x200B;を`Greater than 7`に設定します。

1. 完了したら、**[!UICONTROL Save Category]**&#x200B;をクリックします。

### ページオプション

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Match products by rule] | カテゴリ内の製品のリストがカテゴリルールによって動的に生成されるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Automatic Sorting] | カテゴリ製品のリストに自動的に並べ替え順序を適用します。 オプション：<br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | ルールに別の条件を追加します。 |

{style="table-layout:auto"}

### ページ条件

| オプション | 説明 |
|--- |--- |
| [!UICONTROL Attribute] | 条件の基礎として使用される属性を指定します。 オプション：<br/>**[!UICONTROL Clone Category ID(s)]**- カテゴリ IDに基づいて複数のカテゴリから、並べ替えや順序を指定せずに製品を動的に複製します。<br/>**[!UICONTROL Color]** – 色に基づいて製品を含めます。<br/>**[!UICONTROL Date Created (days ago)]**– 商品がカタログに追加されてからの日数に基づいて商品が含まれます。<br/>**[!UICONTROL Date Modified (days ago)]** – 製品が最後に変更されてからの日数に基づいて製品が含まれます。<br/>**[!UICONTROL Name]**– 製品名に基づく製品が含まれます。<br/>**[!UICONTROL Price]** – 価格に基づく商品が含まれます。<br/>**[!UICONTROL Quantity]**– 在庫量に基づく商品が含まれます。<br/>** SKU **- SKUに基づく商品が含まれます。 |
| [!UICONTROL Operator] | 条件を満たすために属性値に適用される演算子を指定します。 演算子を指定しない限り、`Equal`がデフォルトとして使用されます。 オプション：`Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 属性が条件を満たす必要がある値を指定します。 |
| [!UICONTROL Logic] | 複数の条件を定義するために使用され、別の条件が追加されたときにのみ表示されます。 オプション：`OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>子オプションを含む設定可能な製品の数量は、すべての子製品数量を組み合わせて計算されます。 紫色、赤色、黄色の色のオプションと、それぞれ異なる数量を持つ設定可能な製品&#x200B;_耐久フィットネスタンク_&#x200B;の例を考えてみましょう。 このシナリオでは、親製品数量は、紫色、赤色、黄色の子製品を組み合わせた数量です。

## コントロール


## ページコントロール

{{ee-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![ リストとして表示](../assets/icon-view-list.png) | リストとして表示 |
| ![ タイルとして表示](../assets/icon-view-tiles.png) | タイルとして表示 |
| ![No](../assets/toggle-no.png)を切り替え | ルールによる一致 – いいえ |
| ![はい](../assets/toggle-yes.png)に切り替え | ルールによる一致 – はい |
| ![ コントローラーを移動](../assets/icon-move.png) | ドラッグ&amp;ドロップコントロールを使用すると、商品を取得し、グリッドの現在のページ内の別の位置に移動できます。 詳しくは、[Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)を参照してください。 |
| ![位置コントローラー](../assets/control-position.png) | リスト内の製品の位置を決定します。 |

{style="table-layout:auto"}

## ページコントロール

{{ce-feature}}

| 制御 | 説明 |
|----------|--------------|
| ![選択したチェックボックス ](../assets/checkbox-selected.png) | 最初の列のヘッダーのチェックボックスを使用して、すべての製品を選択するか、すべての選択をクリアします。 最初の行のコントロールは検索のタイプを決定し、任意のレコードを含めるか、カテゴリに割り当てられているか割り当てられていないレコードのみを含めるように設定できます。 各行の最初の列のチェックボックスは、カテゴリに追加する製品を示します。 オプション：`Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 各列の上部にあるフィルターコントロールを使用して、「すべてを選択」設定に応じて、リストに含める特定の値を入力したり、リストから除外したりできます。 |
| [!UICONTROL Reset Filter] | すべての検索フィルターを消去します。 |
| [!UICONTROL Search] | フィルター条件に基づいてカタログを検索し、結果を表示します。 |

{style="table-layout:auto"}
