---
title: 製品属性の作成および削除
description: カタログ内の製品の特定の特性を説明するために使用される製品属性の作成および削除について説明します。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# 製品属性の作成および削除

属性は、製品での作業中にまたは以下から作成できます _[!UICONTROL Product Attributes]_ページ。 次の手順は、から属性を作成する方法を示しています_[!UICONTROL Stores]_ メニュー。

## 手順 1：基本的な属性プロパティの説明

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. クリック **[!UICONTROL Add New Attribute]**.

   ![新しい属性プロパティ](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Default Label]**：属性を識別するラベルを入力します。

1. データ入力に使用される入力コントロールの種類を決定するには、次のように設定します **[!UICONTROL Catalog Input Type for Store Owner]** を次のいずれかに変更します。

   | プロパティ | 説明 |
   |--- |--- |
   | `Text Field` | テキストの 1 行入力フィールド。 |
   | `Text Area` | 製品の説明など、テキストの段落を入力するための複数行の入力フィールド。 WYSIWYG エディターを使用して、HTMLタグでテキストの書式を設定したり、テキストにタグを直接入力したりできます。 |
   | `Text Editor` | 属性の場所に完全に機能するテキストエディター。 |
   | 日付 | に日付値を表示します [優先フォーマット](attributes-input-types.md#date-and-time-options) および [タイムゾーン](../getting-started/store-details.md#locale-options). 日付値は、リストまたはカレンダー（ ![カレンダーアイコン](../assets/icon-calendar.png) ）に設定します。 <br/><br/>**_注意：_**システム設定に応じて、_Admin _ユーザーは、フィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値の指定については、を参照してください。 [日付と時刻のオプション](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | 次のオプションがあらかじめ定義されたドロップダウン リストを表示 `Yes` および `No`. |
   | `Dropdown` | 1 つの選択のみを受け入れる値のドロップダウン リストを表示します。 ドロップダウン入力タイプは、の主要コンポーネントです [設定可能な製品](product-create-configurable.md). |
   | `Multiple Select` | 複数の値を選択できるドロップダウン リストを表示します。 |
   | `Price` | この入力タイプは、事前定義済みの属性（価格、特別価格、階層価格およびコスト）に加えて価格フィールドを作成するために使用されます。 使用する通貨は、システム設定によって決まります。 |
   | `Media Image` | 製品ロゴ、ケアの説明、食品ラベルの材料など、製品に追加の画像を関連付けます。 メディア画像属性を製品の属性セットに追加すると、ベース、小、サムネールと共に、追加の画像タイプになります。 メディア画像属性は、次から除外できます [ストアフロントメディアブラウザー](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | を定義できます [FPT 率](../stores-purchase/fixed-product-tax.md) ロケールの要件に基づいています。 |
   | `Visual Swatch` | 設定可能な商品のカラー、テクスチャ、パターンを示すスウォッチが表示されます。 A [ビジュアルスウォッチ](swatches.md) 16 進数のカラー値で塗りつぶしたり、オプションのカラー、マテリアル、テクスチャ、またはパターンを表すアップロード済み画像を表示したりできます。 |
   | `Text Swatch` | サイズ調整によく使用される、設定可能な商品オプションのテキストベースの表現です。 [テキストスウォッチ](swatches.md#text-based-swatches) また、16 進数のカラー値を含めることもできます。 |
   | `Page Builder` | 完全に機能する [ページビルダー](../page-builder/introduction.md) 製品ページに魅力的なコンテンツを簡単に追加できる、属性の場所のワークスペース。 |

   {style="table-layout:auto"}

1. 顧客が商品を購入する前にオプションの選択が必要な場合は、次のように設定します **[!UICONTROL Values Required]** 対象： `Yes`.

1. の場合 [!UICONTROL Dropdown] および [!UICONTROL Multiple Select] 入力タイプ、次の手順を実行します。

   - 次の下 _[!UICONTROL Manage Options]_を選択し、**[!UICONTROL Add Option]**.

   - リストに表示する最初の値を入力します。

     管理者に 1 つの値を入力し、各ストア表示にその値を翻訳できます。 ストア表示が 1 つしかない場合は、Admin 値のみを入力できます。この値はストアフロントにも使用されます。

   - クリック **[!UICONTROL Add Option]** リストに含める各オプションに対して、前の手順を繰り返します。

   - を選択 **[!UICONTROL Is Default]** をクリックして、オプションをデフォルト値として使用します。

   ![製品属性 – オプションの管理](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 手順 2：詳細プロパティを記述する（必要な場合）

1. 一意のを入力 **[!UICONTROL Attribute Code]** 小文字（スペースなし）。

   ![製品属性 – 詳細プロパティ](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   使用できるオプションは、 _[!UICONTROL Catalog Input Type for Store Owner]_の設定値。

1. を設定 **[!UICONTROL Scope]** 内の場所を示すには [ストア階層](../getting-started/websites-stores-views.md) 属性が使用できる。

1. 値の重複を防ぐには、次のように設定します **[!UICONTROL Unique Value]** 対象： `Yes`.

1. 入力値として使用される入力タイプの場合は、を設定して、テキストフィールドに入力されたデータの有効性テストを実行します。 **[!UICONTROL Input Validation for Store Owner]** をフィールドに含める必要があるデータのタイプに変更します。

   このフィールドは、選択した値を持つ入力タイプには使用できません。 このテストでは、次の項目の検証を行うことができます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![入力検証](./assets/product-attribute-input-validation.png){width="400"}

1. この属性をに追加します [商品リスト](products-list.md)以下のオプションをに設定します。 `Yes`.

   - **列に追加オプション**  – 属性を列として _[!UICONTROL Products]_リスト。
   - **フィルターオプションで使用**  – の列ヘッダーにフィルターコントロールを追加します _[!UICONTROL Products]_リスト。

## 手順 3：フィールドラベルの入力

1. 左側のナビゲーションで、を選択します **[!UICONTROL Manage Labels]**.

1. を入力 **[!UICONTROL Title]** フィールドのラベルとして使用されます。

   ストアが異なる言語で使用可能な場合は、各表示に翻訳されたタイトルを入力できます。

   ![製品属性 – タイトルの管理](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 手順 4：ストアフロントプロパティの説明

1. 左側のナビゲーションで、を選択します **[!UICONTROL Storefront Properties]**.

   ![製品属性 – ストアフロントのプロパティ](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   使用できるオプションは、 _[!UICONTROL Catalog Input Type for Store Owner]_の設定値。

1. 属性を検索に使用できるようにする場合は、を設定します **[!UICONTROL Use in Search]** 対象： `Yes`.

   - を **[!UICONTROL Search Weight]** 検索結果での項目の表示場所を制御する値：1 （最小の重み付け）から 10 （最大の重み付け）。

   - を **[!UICONTROL Visible in Advanced Search]** 必要に応じて。 詳しくは、を参照してください。 [詳細検索](search.md#advanced-search).

1. 製品比較に属性を含めるには、次を設定します **[!UICONTROL Comparable on Storefront]** 対象： `Yes`.

1. ドロップダウン、複数の選択および価格フィールドの場合、次の操作を行います。

   - 属性をレイヤーナビゲーションのフィルターとして使用するには、を設定します **[!UICONTROL Use in Layered Navigation]** 対象： `Yes`.

   - 検索結果ページの階層型ナビゲーションで属性を使用するには、次のように設定します **[!UICONTROL Use in Search Results Layered Navigation]** 対象： `Yes`.

   - の場合 **[!UICONTROL Position]**&#x200B;を入力し、レイヤーナビゲーションブロック内の属性の相対位置を示す数値を入力します。

1. 価格ルールで属性を使用するには、次のように設定します **[!UICONTROL Use for Promo Rule Conditions]** 対象： `Yes`.

1. テキストをHTMLで書式設定するには、次のように設定します **[!UICONTROL Allow HTML Tags on Frontend]** 対象： `Yes`.

   この設定により、フィールドで WYSIWYG エディターを使用できるようになります。

1. 製品ページに属性を含めるには、次を設定します **[!UICONTROL Visible on Catalog Pages on Storefront]** 対象： `Yes`.

1. テーマでサポートされている場合は、次の設定を行います。

   - 製品リストに属性を含めるには、次を設定します **[!UICONTROL Used in Product Listing]** 対象： `Yes`.

   - 属性を製品リストのソートパラメーターとして使用するには、次を設定します **[!UICONTROL Used for Sorting in Product Listing]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Attribute]**.

## 手順 5：作成した属性を属性セットに割り当てる

製品作成ページに属性を表示するには、属性を特定の属性セットに追加します。

1. 前の手順が完了したら、に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. リストで必要な属性セットを選択し、編集モードで開きます。

1. 作成した属性を「」からドラッグします。 **[!UICONTROL Unassigned Attributes]** で適切なフォルダーにリストします **グループ** 列。

1. 完了したら、 **[!UICONTROL Save]**.

## 設定可能な製品の属性

のオプションのドロップダウンリストとして使用される属性 [設定可能な製品](product-create-configurable.md) 次のプロパティが必要です。

| プロパティ | 値 |
|----------|------ |
| 店舗所有者のカタログ入力タイプ | ドロップダウン |
| 範囲 | グローバル |

{style="table-layout:auto"}

## 属性の削除

属性を削除すると、関連する製品および属性セットから削除されます。 システム属性はストアのコア機能の一部であり、削除できません。

属性を削除する前に、その属性がカタログ内のどの製品でも現在使用されていないことを確認してください。 属性が使用中かどうかを簡単に判断するには、 [Export](../systems/data-export.md) 製品エンティティ属性のリストを確認するツール。 属性がリストに含まれていない場合、カタログ内のどの製品でも使用されません。

**_属性を削除するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. リストで属性を見つけ、編集モードで開きます。

1. クリック **[!UICONTROL Delete Attribute]**.

   ![属性を削除](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 確認を求められたら、 **[!UICONTROL OK]**.
