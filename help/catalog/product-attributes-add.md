---
title: 製品への属性の追加
description: カタログで製品に属性を追加する方法を説明します。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 製品への属性の追加

属性は主に [ストア](../stores-purchase/stores-menu.md) メニュー新しい属性を追加することもできます。 _即座に_ 製品の操作中。 既存の属性のリストから選択するか、属性を作成できます。 新しい属性が [属性セット](../catalog/attribute-sets.md) 製品のベースとなる

## 手順 1：属性の追加

1. 製品を編集モードで開きます。

1. 右上隅で、 **[!UICONTROL Add Attribute]**.

   ![デフォルトの属性が設定された新しい製品](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 製品に既存の属性を追加するには、 [フィルターコントロール](../getting-started/admin-grid-controls.md) グリッド内の属性を検索し、次の操作を行います。

   - 追加する各属性の最初の列にあるチェックボックスを選択します。

   - クリック **[!UICONTROL Add Selected]**.

   ![属性を選択](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 新しい属性を定義するには、 **[!UICONTROL Create New Attribute]** をクリックし、手順 2 の項目を完了します。

## 手順 2：基本的な属性プロパティの説明

![属性プロパティ](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. の下 _[!UICONTROL Attribute Properties]_、**[!UICONTROL Attribute Label]**属性を識別する。

1. 設定 **[!UICONTROL Catalog Input Type for Store Owner]** 次のタイプに [入力制御](attributes-input-types.md) データ入力に使用します。

   属性が [設定可能な製品](product-create-configurable.md)を選択します。 `Dropdown`. 次に、 **[!UICONTROL Required]** から `Yes`.

1. の場合 `Dropdown` および `Multiple Select` 入力タイプを指定する場合は、次の操作を行います。

   - の下 **[!UICONTROL Values]**&#x200B;をクリックし、 **[!UICONTROL Add Value]**.

   - リストに表示する最初の値を入力します。

     各ストア表示で、管理者に 1 つの値を入力し、その値の翻訳を入力できます。 ストアビューが 1 つだけの場合、Admin 値のみを入力でき、ストアフロントにも使用されます。

   - クリック **[!UICONTROL Add Value]** をクリックし、リストに含める各オプションについて、前の手順を繰り返します。

   - 選択 **[!UICONTROL Is Default]** を指定します。

   ![値](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 製品を購入する前にオプションを選択するよう顧客に求める場合は、 **[!UICONTROL Required]** から `Yes`.

## 手順 3：詳細なプロパティの説明（オプション）

![高度な属性プロパティ](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 一意の **[!UICONTROL Attribute Code]** を小文字にし、スペースを含めない。

1. 設定 **[!UICONTROL Scope]** を使用して、属性を使用できるストア階層内の場所を指定します。

   属性が [設定可能な製品](product-create-configurable.md)を選択します。 `Global`.

1. この属性がこの製品にのみ適用される場合は、 **[!UICONTROL Unique Value]** から `Yes`.

1. テキストフィールドに入力されたデータの有効性テストを実行するには、 **[!UICONTROL Input Validation for Store Owner]** を、フィールドに格納するデータタイプに設定します。

   このフィールドは、値が選択されている入力タイプでは使用できません。 入力検証は、次のいずれかに使用できます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![入力の検証](./assets/product-attribute-input-validation.png){width="500"}

1. 属性を列として製品グリッドに含めるには、 **[!UICONTROL Add to Column Options]** から `Yes`.

1. をフィルタリングする場合、 _[!UICONTROL Products]_この列でグリッドを設定&#x200B;**[!UICONTROL Use in Filter Options]**から `Yes`.

## 手順 4：フィールドラベルを入力する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Manage titles]** 」セクションに入力します。

1. を入力します。 **[!UICONTROL Title]** フィールドのラベルとして使用されます。

   ストアが異なる言語で使用できる場合は、各ビューに翻訳されたタイトルを入力できます。

   ![タイトルを管理](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 手順 5：ストアフロントのプロパティを説明する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Storefront Properties]** 」セクションに入力します。

   ![ストアフロントのプロパティ](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 属性を検索に使用できるようにするには、 **[!UICONTROL Use in Search]** から `Yes`.

1. 製品比較に属性を含めるには、 **[!UICONTROL Comparable on Storefront]** から `Yes`.

1. レイヤーナビゲーションにドロップダウン、複数選択、価格属性を含めるには、 **[!UICONTROL Use in Search Results Layered Navigation]** を次のいずれかに変更します。

   - `Filterable (with results)`  — レイヤーナビゲーションには、一致する製品が見つかるフィルターのみが含まれます。 リストに表示されるすべての製品に既に適用されている属性値は、使用可能なフィルタとして表示されません。 製品の一致数が 0（ゼロ）の属性値も、使用可能なフィルターのリストから除外されます。<br/><br/>フィルターされた製品のリストには、フィルターに一致する製品のみが含まれます。 製品リストは、選択したフィルターで表示内容が変更された場合にのみ更新されます。

   - `Filterable (no results)`  — レイヤーナビゲーションには、0（ゼロ）個の製品が一致する製品を含む、使用可能なすべての属性値とその製品数に対するフィルターが含まれます。 アトリビュート値がスウォッチの場合、値はフィルタとして表示されますが、x 印で消されます。

1. 検索結果ページのレイヤーナビゲーションで使用するには、 **[!UICONTROL Use in Search Results Navigation]** から `Yes` をクリックし、 **[!UICONTROL Position]** フィールドに入力します。

   位置番号は、レイヤー化されたナビゲーションブロック内の属性の相対位置を示します。

1. 価格ルールで属性を使用するには、 **[!UICONTROL Use for Promo Rule Conditions]** から `Yes`.

1. テキストの書式設定をHTMLに許可するには、 **[!UICONTROL Allow HTML Tags on Storefront]** から `Yes`.

   この設定により、フィールドの編集時に WYSIWYG エディターを使用できるようになります。

1. 製品ページに属性を含めるには、 **[!UICONTROL Visible on Catalog Pages on Storefront]** から `Yes`.

1. テーマでサポートされている次の設定を行います。

   - 製品リストに属性を含めるには、 **[!UICONTROL Used in Product Listing]** から `Yes`.

   - 属性を製品リストの並べ替えパラメータとして使用するには、 **[!UICONTROL Used for Sorting in Product Listing]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Attribute]**.
