---
title: 製品への属性の追加
description: カタログ内の製品に属性を追加する方法を説明します。
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 45d69ccc1a5a6a7b8d072465c19829a76dde826d
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# 製品への属性の追加

属性は主に [&#x200B; ストア &#x200B;](../stores-purchase/stores-menu.md) メニューから管理されますが、製品を操作しながら _その場で_ 新しい属性を追加することもできます。 既存の属性のリストから選択するか、属性を作成できます。 新しい属性が、製品のベースとなる [&#x200B; 属性セット &#x200B;](../catalog/attribute-sets.md) に追加されます。

## 手順 1：属性の追加

1. 製品を編集モードで開きます。

1. 右上隅の「**[!UICONTROL Add Attribute]**」をクリックします。

   ![&#x200B; デフォルトの属性が設定された新しい製品 &#x200B;](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 製品に既存の属性を追加するには、[&#x200B; フィルターコントロール &#x200B;](../getting-started/admin-grid-controls.md) を使用してグリッド内の属性を検索し、次の手順を実行します。

   - 追加する各属性の最初の列のチェックボックスを選択します。

   - 「**[!UICONTROL Add Selected]**」をクリックします。

   ![&#x200B; 属性を選択 &#x200B;](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 新しい属性を定義するには、「**[!UICONTROL Create New Attribute]**」をクリックして手順 2 の項目を完了します。

## 手順 2：基本的な属性プロパティの説明

![&#x200B; 属性プロパティ &#x200B;](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 「_[!UICONTROL Attribute Properties]_」に、属性を識別する&#x200B;**[!UICONTROL Attribute Label]**&#x200B;を入力します。

1. データ入力に使用する **[!UICONTROL Catalog Input Type for Store Owner]** 入力コントロール [&#x200B; のタイプに &#x200B;](attributes-input-types.md) を設定します。

   属性が [&#x200B; 設定可能な製品 &#x200B;](product-create-configurable.md) に使用されている場合は、「`Dropdown`」を選択します。 次に、**[!UICONTROL Required]** を `Yes` に設定します。

1. `Dropdown` および `Multiple Select` の入力タイプの場合、次の操作を行います。

   - [**[!UICONTROL Values]**] で、[**[!UICONTROL Add Value]**] をクリックします。

   - リストに表示する最初の値を入力します。

     管理者に 1 つの値を入力し、各ストア表示にその値を翻訳できます。 ストア表示が 1 つしかない場合は、Admin 値のみを入力できます。この値はストアフロントにも使用されます。

   - **[!UICONTROL Add Value]** をクリックし、リストに含める各オプションに対して前の手順を繰り返します。

   - 「**[!UICONTROL Is Default]**」を選択すると、オプションがデフォルト値として使用されます。

   ![&#x200B; 値 &#x200B;](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 製品を購入する前に顧客にオプションの選択を求める場合は、**[!UICONTROL Required]** を `Yes` に設定します。

## 手順 3：詳細プロパティの説明（オプション）

![&#x200B; 詳細属性プロパティ &#x200B;](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 一意の **[!UICONTROL Attribute Code]** をスペースを含めずに小文字で入力します。

1. **[!UICONTROL Scope]** を設定して、ストア階層内で属性を使用できる場所を示します。

   属性が [&#x200B; 設定可能な製品 &#x200B;](product-create-configurable.md) に使用されている場合は、「`Global`」を選択します。

1. この属性がこの製品にのみ適用される場合は、**[!UICONTROL Unique Value]** を `Yes` に設定します。

1. テキストフィールドに入力されたデータの有効性テストを実行するには、**[!UICONTROL Input Validation for Store Owner]** をフィールドに含めるデータのタイプに設定します。

   このフィールドは、選択した値を持つ入力タイプには使用できません。 入力検証は、次のいずれかの場合に使用できます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![&#x200B; 入力検証 &#x200B;](./assets/product-attribute-input-validation.png){width="500"}

1. 製品グリッドの列として属性を含めたい場合は、**[!UICONTROL Add to Column Options]** を `Yes` に設定します。

1. この列で _[!UICONTROL Products]_&#x200B;グリッドをフィルタリングできるようにする場合は、**[!UICONTROL Use in Filter Options]**&#x200B;を `Yes` に設定します。

## 手順 4：フィールドラベルの入力

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Manage titles]**」セクションを展開します。

1. フィールドのラベルとして使用する **[!UICONTROL Title]** を入力します。

   ストアが異なる言語で使用可能な場合は、各表示に翻訳されたタイトルを入力できます。

   ![&#x200B; タイトルの管理 &#x200B;](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > この属性をライブサーチのファセットとして使用する場合は、ストア固有のラベルを指定する必要があります。 これがないと、属性名がファセット設定ページに正しく表示されない場合があります。 設定を更新するには、[&#x200B; ライブ検索ガイド &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) の _ライブ検索のファセットリストの編集オプション_ を使用して、ラベルを手動で編集します。

## 手順 5：ストアフロントプロパティの説明

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Storefront Properties]**」セクションを展開します。

   ![&#x200B; ストアフロントのプロパティ &#x200B;](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 属性を検索に使用できるようにするには、**[!UICONTROL Use in Search]** を `Yes` に設定します。

1. 製品の比較に属性を含めるには、**[!UICONTROL Comparable on Storefront]** を `Yes` に設定します。

1. 階層型ナビゲーションにドロップダウン、複数の選択または価格の属性を含めるには、**[!UICONTROL Use in Search Results Layered Navigation]** を次のいずれかに設定します。

   - `Filterable (with results)` – 階層ナビゲーションには、一致する製品が見つかるフィルターのみが含まれます。 リストに表示されるすべての製品に既に適用されている属性値は、使用可能なフィルターとしては表示されません。 カウントがゼロ（0）の製品一致を持つ属性値も、使用可能なフィルターのリストから省略されます。<br/><br/> フィルタリングされた製品リストには、フィルターに一致する製品のみが含まれます。 製品リストは、選択したフィルターによって表示内容が変更される場合にのみ更新されます。

   - `Filterable (no results)` – 階層ナビゲーションには、使用可能なすべての属性値とその製品数（製品の一致がゼロ（0）の製品を含む）のフィルターが含まれます。 属性値がスウォッチの場合、その値はフィルタとして表示されますが、交差しています。

   >[!NOTE]
   >
   >_[!UICONTROL Use in Search]_&#x200B;設定が `No` に設定されている場合、_[!UICONTROL Use in Search Results Layered Navigation]_ 設定は表示されず、製品属性は [!UICONTROL Use in Layered Navigation] の設定値を持つ検索で使用されません。

1. 検索結果ページの階層型ナビゲーションで属性を使用するには、「**[!UICONTROL Use in Search Results Layered Navigation]**」を「`Yes`」に設定し、「**[!UICONTROL Position]**」フィールドに数値を入力します。

   位置番号は、階層化ナビゲーションブロック内の属性の相対位置を示します。

   >[!NOTE]
   >
   >_[!UICONTROL Position]_&#x200B;フィールドはデフォルトで淡色表示され、この設定を変更する前に属性を保存する必要があります。

1. 価格ルールで属性を使用するには、**[!UICONTROL Use for Promo Rule Conditions]** を `Yes` に設定します。

1. テキストをHTMLで書式設定するには、**[!UICONTROL Allow HTML Tags on Storefront]** を `Yes` に設定します。

   この設定により、フィールドの編集時にWYSIWYG エディターを使用できるようになります。

1. 製品ページに属性を含めるには、**[!UICONTROL Visible on Catalog Pages on Storefront]** を `Yes` に設定します。

1. テーマでサポートされている以下の設定を行います。

   - 製品リストに属性を含めるには、**[!UICONTROL Used in Product Listing]** を `Yes` に設定します。

   - 属性を製品リストのソートパラメーターとして使用するには、**[!UICONTROL Used for Sorting in Product Listing]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。
