---
title: 製品属性の作成および削除
description: カタログ内の製品の特定の特性を説明するために使用される製品属性の作成および削除について説明します。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: ab91c19cda6a89219fc8946dad4a0a70d0991b38
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# 製品属性の作成および削除

属性は、製品の操作時または _[!UICONTROL Product Attributes]_&#x200B;ページから作成できます。 次の手順は、_[!UICONTROL Stores]_ メニューから属性を作成する方法を示しています。

## 手順 1：基本的な属性プロパティの説明

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Attribute]**」をクリックします。

   ![&#x200B; 新しい属性プロパティ &#x200B;](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. **[!UICONTROL Default Label]**：属性を識別するラベルを入力します。

1. データ入力に使用される入力コントロールの種類を決定するには、**[!UICONTROL Catalog Input Type for Store Owner]** を次のいずれかに設定します。

   | プロパティ | 説明 |
   |--- |--- |
   | `Text Field` | テキストの 1 行入力フィールド。 |
   | `Text Area` | 製品の説明など、テキストの段落を入力するための複数行の入力フィールド。 WYSIWYG エディターを使用して、テキストをHTML タグで書式設定したり、テキストにタグを直接入力したりできます。 |
   | `Text Editor` | 属性の場所に完全に機能するテキストエディター。 |
   | 日付 | 日付値を [&#x200B; 優先形式 &#x200B;](attributes-input-types.md#date-and-time-options) および [&#x200B; タイムゾーン &#x200B;](../getting-started/store-details.md#locale-options) で表示します。 日付値は、リストまたはカレンダー（![&#x200B; カレンダーアイコン &#x200B;](../assets/icon-calendar.png)）から選択できます。 <br/><br/>**_Note:_** システムの設定に応じて、_Admin_ ユーザーはフィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値を指定する方法については、[&#x200B; 日付と時刻のオプション &#x200B;](attributes-input-types.md#date-and-time-options) を参照してください。 |
   | `Yes/No` | `Yes` と `No` の定義済みオプションを含むドロップダウン リストを表示します。 |
   | `Dropdown` | 1 つの選択のみを受け入れる値のドロップダウン リストを表示します。 ドロップダウン入力タイプは、[&#x200B; 設定可能な製品 &#x200B;](product-create-configurable.md) の主要コンポーネントです。 |
   | `Multiple Select` | 複数の値を選択できるドロップダウン リストを表示します。 |
   | `Price` | この入力タイプは、事前定義済みの属性（価格、特別価格、階層価格およびコスト）に加えて価格フィールドを作成するために使用されます。 使用する通貨は、システム設定によって決まります。 |
   | `Media Image` | 製品ロゴ、ケアの説明、食品ラベルの材料など、製品に追加の画像を関連付けます。 メディア画像属性を製品の属性セットに追加すると、ベース、小、サムネールと共に、追加の画像タイプになります。 メディア画像属性は、[&#x200B; ストアフロントメディアブラウザー &#x200B;](catalog-images-video.md#storefront-media-browser) から除外できます。 |
   | `Fixed Product Tax` | ロケールの要件に基づいて [FPT 率 &#x200B;](../stores-purchase/fixed-product-tax.md) を定義できます。 |
   | `Visual Swatch` | 設定可能な商品のカラー、テクスチャ、パターンを示すスウォッチが表示されます。 [&#x200B; 視覚的なスウォッチ &#x200B;](swatches.md) には、16 進数カラー値を入力するか、オプションのカラー、マテリアル、テクスチャまたはパターンを表すアップロード済み画像を表示できます。 |
   | `Text Swatch` | サイズ調整によく使用される、設定可能な商品オプションのテキストベースの表現です。 [&#x200B; テキストスウォッチ &#x200B;](swatches.md#text-based-swatches) には、16 進数のカラー値を含めることもできます。 |
   | `Page Builder` | 属性の場所にあるの完全に機能する [&#x200B; ページビルダー &#x200B;](../page-builder/introduction.md) ワークスペースで、魅力的なコンテンツを製品ページに簡単に追加できます。 |

   {style="table-layout:auto"}

1. 顧客が商品を購入する前にオプションの選択が必要な場合は、**[!UICONTROL Values Required]** を `Yes` に設定します。

1. [!UICONTROL Dropdown] および [!UICONTROL Multiple Select] の入力タイプの場合、次の操作を行います。

   - [_[!UICONTROL Manage Options]_] で、[**[!UICONTROL Add Option]**] をクリックします。

   - リストに表示する最初の値を入力します。

     管理者に 1 つの値を入力し、各ストア表示にその値を翻訳できます。 ストア表示が 1 つしかない場合は、Admin 値のみを入力できます。この値はストアフロントにも使用されます。

   - **[!UICONTROL Add Option]** をクリックし、リストに含める各オプションに対して前の手順を繰り返します。

   - 「**[!UICONTROL Is Default]**」を選択すると、オプションがデフォルト値として使用されます。

   ![&#x200B; 製品属性 – オプションを管理 &#x200B;](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 手順 2：詳細プロパティを記述する（必要な場合）

1. 一意の **[!UICONTROL Attribute Code]** をスペースを含めずに小文字で入力します。

   >[!NOTE]
   >
   >`type` フィールドに [!UICONTROL Attribute Code] の値を使用することはお勧めしません。 `type` の値はシステムでの使用のために予約されているので、これが原因でエラーが発生する可能性があります。

   ![&#x200B; 製品属性 – 詳細プロパティ &#x200B;](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   使用できるオプションは、_[!UICONTROL Catalog Input Type for Store Owner]_&#x200B;の設定によって異なります。

1. 属性を使用できる **[!UICONTROL Scope]** ストア階層 [&#x200B; の場所を示すために、](../getting-started/websites-stores-views.md) を設定します。

1. 値の重複を防ぐには、**[!UICONTROL Unique Value]** を `Yes` に設定します。

1. 入力値として使用される入力タイプの場合、**[!UICONTROL Input Validation for Store Owner]** をフィールドに格納するデータのタイプに設定することにより、テキストフィールドに入力されたデータの有効性テストを実行します。

   このフィールドは、選択した値を持つ入力タイプには使用できません。 このテストでは、次の項目の検証を行うことができます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![&#x200B; 入力検証 &#x200B;](./assets/product-attribute-input-validation.png){width="400"}

1. この属性を [&#x200B; 製品リスト &#x200B;](products-list.md) に追加するには、次のオプションを `Yes` に設定します。

   - **列オプションに追加** – 属性を列として _[!UICONTROL Products]_&#x200B;リストに含めます。
   - **フィルターオプションで使用** - フィルターリストの列ヘッダーに _[!UICONTROL Products]_&#x200B;ィルターコントロールを追加します。

## 手順 3：フィールドラベルの入力

1. 左側のナビゲーションで「**[!UICONTROL Manage Labels]**」を選択します。

1. フィールドのラベルとして使用する **[!UICONTROL Title]** を入力します。

   ストアが異なる言語で使用可能な場合は、各表示に翻訳されたタイトルを入力できます。

   ![&#x200B; 製品属性 – タイトルの管理 &#x200B;](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > この属性をライブサーチのファセットとして使用する場合は、ストア固有のラベルを指定する必要があります。 これがないと、属性名がファセット設定ページに正しく表示されない場合があります。 設定を更新するには、[&#x200B; ライブ検索ガイド &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) の _ライブ検索のファセットリストの編集オプション_ を使用して、ラベルを手動で編集します。

## 手順 4：ストアフロントプロパティの説明

1. 左側のナビゲーションで「**[!UICONTROL Storefront Properties]**」を選択します。

   ![&#x200B; 製品属性 – ストアフロントのプロパティ &#x200B;](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   使用できるオプションは、_[!UICONTROL Catalog Input Type for Store Owner]_&#x200B;の設定によって異なります。

1. 属性を検索に使用できるようにする場合は、**[!UICONTROL Use in Search]** を `Yes` に設定します。

   - 検索結果での項目の表示位置を制御する **[!UICONTROL Search Weight]** 値を設定します：1 （最小の重み付け） ～ 10 （最大の重み付け）。

   - 必要に応じて **[!UICONTROL Visible in Advanced Search]** を設定します。 詳しくは、[&#x200B; 詳細検索 &#x200B;](search.md#advanced-search) を参照してください。

1. 製品の比較に属性を含めるには、**[!UICONTROL Comparable on Storefront]** を `Yes` に設定します。

1. ドロップダウン、複数の選択および価格フィールドの場合、次の操作を行います。

   - 属性をレイヤーナビゲーションのフィルターとして使用するには、**[!UICONTROL Use in Layered Navigation]** を `Yes` に設定します。

   - 検索結果ページのレイヤーナビゲーションで属性を使用するには、**[!UICONTROL Use in Search Results Layered Navigation]** を `Yes` に設定します。

   - **[!UICONTROL Position]** の場合は、レイヤ ナビゲーション ブロック内の属性の相対位置を示す数字を入力します。

1. 価格ルールで属性を使用するには、**[!UICONTROL Use for Promo Rule Conditions]** を `Yes` に設定します。

1. テキストをHTMLで書式設定するには、**[!UICONTROL Allow HTML Tags on Frontend]** を `Yes` に設定します。

   この設定により、フィールドでWYSIWYG エディターを使用できるようになります。

1. 製品ページに属性を含めるには、**[!UICONTROL Visible on Catalog Pages on Storefront]** を `Yes` に設定します。

1. テーマでサポートされている場合は、次の設定を行います。

   - 製品リストに属性を含めるには、**[!UICONTROL Used in Product Listing]** を `Yes` に設定します。

   - 属性を製品リストのソートパラメーターとして使用するには、**[!UICONTROL Used for Sorting in Product Listing]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

## 手順 5：作成した属性を属性セットに割り当てる

製品作成ページに属性を表示するには、属性を特定の属性セットに追加します。

1. 前の手順が完了したら、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Attribute Set]**&#x200B;に移動します。

1. リストで必要な属性セットを選択し、編集モードで開きます。

1. 作成した属性を **[!UICONTROL Unassigned Attributes]** リストから **グループ** 列の適切なフォルダーにドラッグします。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 設定可能な製品の属性

[&#x200B; 設定可能な製品 &#x200B;](product-create-configurable.md) のオプションのドロップダウンリストとして使用する属性には、次のプロパティが必要です。

| プロパティ | 値 |
|----------|------ |
| 店舗所有者のカタログ入力タイプ | ドロップダウン |
| 範囲 | グローバル |

{style="table-layout:auto"}

## 属性の削除

属性を削除すると、関連する製品および属性セットから削除されます。 システム属性はストアのコア機能の一部であり、削除できません。

属性を削除する前に、その属性がカタログ内のどの製品でも現在使用されていないことを確認してください。 属性が使用中かどうかを簡単に判断するには、[&#x200B; 書き出し &#x200B;](../systems/data-export.md) ツールを使用して、製品エンティティ属性のリストを確認します。 属性がリストに含まれていない場合、カタログ内のどの製品でも使用されません。

属性を削除するには、**_T:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**&#x200B;に移動します。

1. リストで属性を見つけ、編集モードで開きます。

1. 「**[!UICONTROL Delete Attribute]**」をクリックします。

   ![&#x200B; 属性を削除 &#x200B;](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL OK]**」をクリックします。
