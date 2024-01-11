---
title: マーチャンダイジングのカテゴリルール
description: 条件のセットに従って製品の選択を動的に変更するルールを作成する方法を説明します。
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
source-git-commit: 50951e5aae51067cdba2d8b50c1e530c7f79007a
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---

# マーチャンダイジングのカテゴリルール

{{ee-feature}}

カテゴリルールは、条件のセットに従って、製品の選択を動的に変更します。 各カテゴリには 1 つのカテゴリルールのみを含めることができますが、1 つのルールに複数の条件を含めることができます。 例えば、特定のブランドのカテゴリルールを作成できます。 同じブランドの製品が同じカテゴリに割り当てられていない場合でも、自動的にリストに追加されます。 式に条件を必要な数だけ追加して、含める製品を記述できます。

>[!TIP]
>
>カテゴリルールの設定時に、製品は _並べ替え_, _一致_, _割り当てられた_、および _未指定_ その規則に従って **_のみ_** このカテゴリが保存されたとき。 例えば、商品をカタログに追加し、ルールに従って割り当てる場合、 **は、各カテゴリを再度開く必要があります** ルールで製品を照合するために設定される また、いずれかの製品の在庫ステータスが `In Stock` または `Out of Stock` およびカテゴリ内の製品は、 _並べ替え_ 次によると **[!UICONTROL Automatic Sorting]** ルール：次をクリックする必要があります： **[!UICONTROL Save Category]**.

各条件は、属性、値、論理演算子で構成されます。 属性のみ _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_プロパティをに設定 `Yes` はカテゴリルールで使用できます。 製品リストに含まれていない属性を使用する場合は、属性に対してこのプロパティを設定する必要があります。 日付属性はサポートされていませんが、作成日属性または変更日属性を使用して、日付または日付の範囲を定義できます。 例えば、過去 1 週間に作成された製品のみを含めるには、「作成日」を `<7`.

>[!NOTE]
>
>ルールで使用される各属性を、 [_スマート_ 属性](smart-attributes-configure.md).

![カテゴリ製品ルール](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

カテゴリ製品ルールを使用すると、カテゴリに表示される製品を決定する条件に基づいて、特定の製品をカテゴリに割り当てるプロセスを迅速に実行できます。 カテゴリ製品ルールで使用できる「スマート」属性は、 [Visual Merchandiser](visual-merchandiser.md) 設定。

>[!NOTE]
>
>条件を満たさない製品はカテゴリから削除されるので、カテゴリ製品ルールを適用する際は注意が必要です。 例えば、紫色のタンクトップのみを含むルールを作成すると、その他のすべてのタンクトップはカテゴリから削除されます。

## 手順 1: _スマート_ 属性

1. ルールで使用する属性ごとに、 [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront プロパティはに設定されます。 `Yes`.

   >[!NOTE]
   >
   >選択した属性が複数選択の属性でないことを確認します。 _[!UICONTROL Input Type]_.

1. 次を完了： [設定](smart-attributes-configure.md) それぞれを特定する _スマート_ Visual Merchandiser で使用する属性。

## 手順 2：カテゴリルールの作成

1. カテゴリツリーで、編集するカテゴリを開きます。

1. Adobe Analytics の **[!UICONTROL Products in Category]** セクション、設定 **[!UICONTROL Match products by rule]** から `Yes`.

   自動並べ替えと条件のオプションが表示されます。

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

1. 次を入力します。 **[!UICONTROL Value]** それはマッチングされる。

   ![カテゴリルールに条件を追加](../catalog/assets/category-rule-create.png){width="500"}

1. 満たす条件を説明するために必要な属性ごとに、この手順を繰り返します。

   例えば、7 ～ 30 日前に作成された製品を照合するには、次の操作を行います。

   - 設定 **[!UICONTROL Date Created]** から `Less than 30`.

   - 設定 **[!UICONTROL Logic]** から `AND`.

     >[!NOTE]
     >
     >次を選択した場合： `AND`の場合、ルールはすべての条件を満たす製品に適用されます。 選ぶ理由 `OR`の場合は、1 つ以上の条件が満たされる製品に適用されます。

   - 設定 **[!UICONTROL Date Modified]** から `Greater than 7`.

1. 動的に生成される製品リストに自動的に並べ替え順を適用するには、 **[!UICONTROL Automatic Sorting]**.

   ![自動並べ替え](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   並べ替え順のオプションはグローバルに定義され、現在の条件に基づいて適用されます。 Web サイト、ストア、ストアの表示レベルに異なる並べ替え順を設定することはできません。

   | 並べ替えオプション | 説明 |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | 在庫に基づいて上か下から並べ替え： `Move low stock to top` または `Move out of stock to bottom` |
   | [!UICONTROL Special price] | 価格に基づいて上か下から並べ替え： `Special price to top` または `Special price to bottom` |
   | [!UICONTROL New Products] | 最新の製品を一覧表示： `Newest products first` |
   | [!UICONTROL Color] | アルファベット順に色で並べ替え： `Sort by color` |
   | [!UICONTROL Product Names] | 名前で昇順または降順に並べ替え： `Name A - Z` または `Name Z -A` |
   | [!UICONTROL SKU] | SKU で昇順または降順に並べ替え： `SKU: Ascending` または `SKU: Descending` |
   | [!UICONTROL Price] | 昇順または降順での価格で並べ替え： `Price: High to low` または `Price: Low to high` |

   {style="table-layout:auto"}

1. 完了したら、「 **[!UICONTROL Save Category]**.

>[!NOTE]
>
>カテゴリルールを設定する際、カテゴリが保存されると、製品が照合され、ルールに割り当てられます。 カタログに商品を追加し、その商品をルールに含める場合は、商品をルール別に照合するように設定された各カテゴリを再度保存する必要があります。 これにより、新しい製品が確実に含まれます。

### メニューオプション

- **[!UICONTROL Match products by rule]**  — カテゴリ内の製品のリストがカテゴリルールによって動的に生成されるかどうかを決定します。 オプション： `Yes` / `No`

- **[!UICONTROL Automatic Sorting]**  — カテゴリ製品のリストに並べ替え順を自動的に適用します。 オプション： `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low`、および `Price: Low to High`

  >[!NOTE]
  >
  >子製品と共に設定可能な製品がある場合、親製品の在庫は子製品の在庫の合計に基づいて計算されます。 設定可能な製品がある場合の例を考えてみましょう。 _Proteus Fitness Shirt_ オレンジ、赤、黄色の子製品の在庫数がそれぞれ異なる 親製品の在庫は、オレンジ、赤、黄の子製品の在庫の合計を基に計算されます。 を使用 `Move low stock to top` オプションを指定すると、販売可能な子製品の在庫をすべて組み合わせて親製品の在庫を計算し、それに応じて並べ替えます。

- **[!UICONTROL Add Condition]**  — ルールに別の条件を追加します。

- **[!UICONTROL Attribute]**  — 条件の基準として使用される属性を決定します。 オプション：

  | オプション | 説明 |
  | ------ | ----------- |
  | `Clone Category ID(s)` | カテゴリ ID に基づく複数のカテゴリから、製品のクローンを、並べ替えや順序なしで動的に作成します。 |
  | `Color` | 色に基づく製品が含まれます。 |
  | `Date Created (days ago)` | 商品がカタログに追加されてからの日数に基づく商品が含まれます。 |
  | `Date Modified (days ago)` | 製品が最後に変更されてからの日数に基づく製品が含まれます。 |
  | `Name` | 製品名に基づく製品が含まれます。 |
  | `Price` | 価格に基づく製品が含まれます。 この属性は、設定可能な製品には独自の価格がないので、適用できません。 |
  | `Quantity` | 在庫数量に基づく製品が含まれます。 |
  | `SKU` | SKU に基づく製品が含まれます。 |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >構成可能な製品の数量と子オプションは、販売可能な子製品の数量をすべて組み合わせて計算されます。 設定可能な製品がある場合の例を考えてみましょう。 _基本フィットネスタンク_ 紫色、赤、黄色の各色のオプションと、それぞれ異なる量が表示されます。 この場合、親製品（基本フィットネスタンク）の数量は、紫、赤、黄色の子製品の合計販売可能数量です。

- **[!UICONTROL Operator]**  — 条件を満たすために属性値に適用される演算子を指定します。 演算子が指定されていない場合、 `Equal` がデフォルトとして使用されます。 オプション： `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to`、および `Contains`

- **[!UICONTROL Value]**  — 属性が条件を満たす必要がある値を指定します。

- **[!UICONTROL Logic]** - 「論理」列は、複数の条件の定義に使用され、別の条件が追加された場合にのみ表示されます。 演算子は MySQL の優先順位に従います [ブール演算子](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). オプション： `AND` / `OR`
