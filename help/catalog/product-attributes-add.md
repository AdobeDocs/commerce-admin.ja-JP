---
title: 製品への属性の追加
description: カタログ内の製品に属性を追加する方法を説明します。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# 製品への属性の追加

属性は主にから管理されます [ストア](../stores-purchase/stores-menu.md) メニューから、新しい属性を追加することもできます _その場で_ 製品に取り組んでいる間。 既存の属性のリストから選択するか、属性を作成できます。 新しい属性がに追加されます。 [属性セット](../catalog/attribute-sets.md) 製品のベースとなる。

## 手順 1：属性の追加

1. 製品を編集モードで開きます。

1. 右上隅のをクリックします。 **[!UICONTROL Add Attribute]**.

   ![デフォルトの属性が設定された新しい製品](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 既存の属性を製品に追加するには、 [フィルターコントロール](../getting-started/admin-grid-controls.md) グリッド内で属性を検索するには、次の手順を実行します。

   - 追加する各属性の最初の列のチェックボックスを選択します。

   - クリック **[!UICONTROL Add Selected]**.

   ![属性を選択](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 新しい属性を定義するには、をクリックします **[!UICONTROL Create New Attribute]** 手順 2 の項目を完了します。

## 手順 2：基本的な属性プロパティの説明

![属性プロパティ](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 次の下 _[!UICONTROL Attribute Properties]_、を入力&#x200B;**[!UICONTROL Attribute Label]**をクリックして属性を識別します。

1. を設定 **[!UICONTROL Catalog Input Type for Store Owner]** ～の種類に [入力制御](attributes-input-types.md) データ入力に使用されます。

   属性がに使用されている場合 [設定可能な製品](product-create-configurable.md)、を選択 `Dropdown`. 次に、を設定します **[!UICONTROL Required]** 対象： `Yes`.

1. の場合 `Dropdown` および `Multiple Select` 入力タイプ、次の手順を実行します。

   - 次の下 **[!UICONTROL Values]**&#x200B;を選択し、 **[!UICONTROL Add Value]**.

   - リストに表示する最初の値を入力します。

     管理者に 1 つの値を入力し、各ストア表示にその値を翻訳できます。 ストア表示が 1 つしかない場合は、Admin 値のみを入力できます。この値はストアフロントにも使用されます。

   - クリック **[!UICONTROL Add Value]** リストに含める各オプションに対して、前の手順を繰り返します。

   - を選択 **[!UICONTROL Is Default]** をクリックして、オプションをデフォルト値として使用します。

   ![値](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 製品を購入する前に顧客にオプションの選択を求める場合は、次のように設定します **[!UICONTROL Required]** 対象： `Yes`.

## 手順 3：詳細プロパティの説明（オプション）

![詳細属性プロパティ](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 一意のを入力 **[!UICONTROL Attribute Code]** 小文字（スペースなし）。

1. を設定 **[!UICONTROL Scope]** を使用して、ストア階層内で属性を使用できる場所を示します。

   属性がに使用されている場合 [設定可能な製品](product-create-configurable.md)、を選択 `Global`.

1. この属性がこの製品にのみ適用される場合は、 **[!UICONTROL Unique Value]** 対象： `Yes`.

1. テキストフィールドに入力されたデータの有効性テストを実行するには、次のように設定します。 **[!UICONTROL Input Validation for Store Owner]** をフィールドに含める必要があるデータのタイプに変更します。

   このフィールドは、選択した値を持つ入力タイプには使用できません。 入力検証は、次のいずれかの場合に使用できます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![入力検証](./assets/product-attribute-input-validation.png){width="500"}

1. 製品グリッドの列として属性を含めるには、次のように設定します **[!UICONTROL Add to Column Options]** 対象： `Yes`.

1. をフィルタリングできるようにする場合 _[!UICONTROL Products]_この列でグリッド、設定&#x200B;**[!UICONTROL Use in Filter Options]**対象： `Yes`.

## 手順 4：フィールドラベルの入力

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Manage titles]** セクション。

1. を入力 **[!UICONTROL Title]** フィールドのラベルとして使用されます。

   ストアが異なる言語で使用可能な場合は、各表示に翻訳されたタイトルを入力できます。

   ![タイトルの管理](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 手順 5：ストアフロントプロパティの説明

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Storefront Properties]** セクション。

   ![ストアフロント プロパティ](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 属性を検索に使用できるようにするには、次のように設定します **[!UICONTROL Use in Search]** 対象： `Yes`.

1. 製品比較に属性を含めるには、次を設定します **[!UICONTROL Comparable on Storefront]** 対象： `Yes`.

1. 階層型ナビゲーションにドロップダウン、複数の選択または価格属性を含めるには、次のように設定します **[!UICONTROL Use in Search Results Layered Navigation]** を次のいずれかに変更します。

   - `Filterable (with results)`  – 階層ナビゲーションには、一致する製品が見つかるフィルターのみが含まれます。 リストに表示されるすべての製品に既に適用されている属性値は、使用可能なフィルターとしては表示されません。 カウントがゼロ（0）の製品一致を持つ属性値も、使用可能なフィルターのリストから省略されます。<br/><br/>フィルタリングされた製品リストには、フィルターに一致する製品のみが含まれます。 製品リストは、選択したフィルターによって表示内容が変更される場合にのみ更新されます。

   - `Filterable (no results)`  – 階層ナビゲーションには、使用可能なすべての属性値とその製品数（製品の一致がゼロ（0）の製品を含む）のフィルターが含まれます。 属性値がスウォッチの場合、その値はフィルタとして表示されますが、交差しています。

   >[!NOTE]
   >
   >いつ _[!UICONTROL Use in Search]_はに設定されています。 `No`,_[!UICONTROL Use in Search Results Layered Navigation]_ 設定は表示されず、製品属性は使用されません [!UICONTROL Use in Layered Navigation] 値を設定します。

1. 検索結果ページの階層型ナビゲーションで属性を使用するには、次のように設定します **[!UICONTROL Use in Search Results Layered Navigation]** 対象： `Yes` さらに、に数値を入力します **[!UICONTROL Position]** フィールド。

   位置番号は、階層化ナビゲーションブロック内の属性の相対位置を示します。

   >[!NOTE]
   >
   >この _[!UICONTROL Position]_フィールドはデフォルトで淡色表示され、この設定を変更するには属性を保存する必要があります。

1. 価格ルールで属性を使用するには、次のように設定します **[!UICONTROL Use for Promo Rule Conditions]** 対象： `Yes`.

1. テキストをHTMLで書式設定するには、次のように設定します **[!UICONTROL Allow HTML Tags on Storefront]** 対象： `Yes`.

   この設定により、フィールドの編集時に WYSIWYG エディターを使用できるようになります。

1. 製品ページに属性を含めるには、次を設定します **[!UICONTROL Visible on Catalog Pages on Storefront]** 対象： `Yes`.

1. テーマでサポートされている以下の設定を行います。

   - 製品リストに属性を含めるには、次を設定します **[!UICONTROL Used in Product Listing]** 対象： `Yes`.

   - 属性を製品リストのソートパラメーターとして使用するには、次を設定します **[!UICONTROL Used for Sorting in Product Listing]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Attribute]**.
