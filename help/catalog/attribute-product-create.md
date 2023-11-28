---
title: 製品属性の作成と削除
description: カタログ内の商品の特定の特性を説明するために使用される商品属性の作成と削除について説明します。
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# 製品属性の作成と削除

属性は、製品の作業中に、または _[!UICONTROL Product Attributes]_ページに貼り付けます。 以下の手順で、_[!UICONTROL Stores]_ メニュー。

## 手順 1：基本的な属性プロパティの説明

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. クリック **[!UICONTROL Add New Attribute]**.

   ![新しい属性プロパティ](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Default Label]**」で、属性を識別するラベルを入力します。

1. データ入力に使用される入力コントロールの種類を判断するには、 **[!UICONTROL Catalog Input Type for Store Owner]** を次のいずれかに変更します。

   | プロパティ | 説明 |
   |--- |--- |
   | `Text Field` | テキストの 1 行の入力フィールドです。 |
   | `Text Area` | 製品の説明など、テキストの段落を入力する複数行の入力フィールド。 WYSIWYG エディターを使用して、テキストをHTMLタグで書式設定したり、テキストに直接タグを入力したりできます。 |
   | `Text Editor` | 属性の場所にある、完全に機能するテキストエディター。 |
   | 日付 | 日付値を [推奨フォーマット](attributes-input-types.md#date-and-time-options) および [タイムゾーン](../getting-started/store-details.md#locale-options). 日付値は、リストまたはカレンダー ( ![カレンダーアイコン](../assets/icon-calendar.png) ) をクリックします。 <br/><br/>**_注意：_**システム構成に応じて、_管理者&#x200B;_ユーザーは、フィールドに日付を直接入力したり、カレンダーやリストから日付を選択したりできます。 日付と時刻の値の指定について詳しくは、 [日付と時間のオプション](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | 次の定義済みオプションを含むドロップダウンリストを表示します。 `Yes` および `No`. |
   | `Dropdown` | 1 つの選択のみを受け入れる値のドロップダウンリストを表示します。 ドロップダウン入力タイプは、 [設定可能な製品](product-create-configurable.md). |
   | `Multiple Select` | 複数の選択を受け入れる値のドロップダウンリストを表示します。 |
   | `Price` | この入力タイプは、Price、Special Price、Tier Price、Cost という事前定義済み属性に加えて、価格フィールドを作成するために使用します。 使用される通貨は、システム設定によって決まります。 |
   | `Media Image` | 特別な画像を製品（製品のロゴ、ケアの指示、食品ラベルの材料など）に関連付けます。 メディアイメージ属性を製品の属性セットに追加すると、追加のイメージタイプになり、ベース、小、サムネールと共に表示されます。 メディア画像属性は、 [storefront メディアブラウザー](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | 以下を定義できます。 [FPT レート](../stores-purchase/fixed-product-tax.md) ロケールの要件に基づきます。 |
   | `Visual Swatch` | 設定可能なプロダクトの色、テクスチャ、またはパターンを示すスウォッチを表示します。 A [ビジュアルスウォッチ](swatches.md) は 16 進数のカラー値で塗りつぶすことも、アップロードした画像を表示してオプションの色、素材、テクスチャまたはパターンを表すこともできます。 |
   | `Text Swatch` | サイズに頻繁に使用される、設定可能な製品オプションのテキストベースの表現です。 [テキストスウォッチ](swatches.md#text-based-swatches) には、16 進数のカラー値を含めることもできます。 |
   | `Page Builder` | 完全に機能している [Page Builder](../page-builder/introduction.md) ワークスペース（製品ページに魅力的なコンテンツを簡単に追加できる属性の場所） |

   {style="table-layout:auto"}

1. 顧客が製品を購入する前にオプションの選択が必要な場合は、 **[!UICONTROL Values Required]** から `Yes`.

1. の場合 [!UICONTROL Dropdown] および [!UICONTROL Multiple Select] 入力タイプを指定する場合は、次の操作を行います。

   - の下 _[!UICONTROL Manage Options]_をクリックし、**[!UICONTROL Add Option]**.

   - リストに表示する最初の値を入力します。

     管理者に 1 つの値を入力し、各ストア表示に 1 つの値の翻訳を入力できます。 ストアビューが 1 つだけの場合、Admin 値のみを入力でき、ストアフロントにも使用されます。

   - クリック **[!UICONTROL Add Option]** をクリックし、リストに含める各オプションについて、前の手順を繰り返します。

   - 選択 **[!UICONTROL Is Default]** を指定します。

   ![製品属性 — オプションの管理](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## 手順 2：詳細なプロパティの説明（必要に応じて）

1. 一意の **[!UICONTROL Attribute Code]** を小文字にし、スペースを含めない。

   ![製品属性 — 詳細プロパティ](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   使用可能なオプションは、 _[!UICONTROL Catalog Input Type for Store Owner]_設定。

1. 設定 **[!UICONTROL Scope]** の場所を示します [ストア階層](../getting-started/websites-stores-views.md) 属性を使用できることを示します。

1. 値の重複を防ぐには、 **[!UICONTROL Unique Value]** から `Yes`.

1. 入力値の入力タイプについては、を設定して、テキストフィールドに入力されたデータの有効性テストを実行します。 **[!UICONTROL Input Validation for Store Owner]** を、フィールドに格納するデータタイプに設定します。

   このフィールドは、値が選択されている入力タイプでは使用できません。 テストでは、次のいずれかを検証できます。

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![入力の検証](./assets/product-attribute-input-validation.png){width="400"}

1. この属性を [製品リスト](products-list.md)、次のオプションをに設定します。 `Yes`.

   - **列オプションに追加**  — 属性を列として _[!UICONTROL Products]_リスト。
   - **フィルターオプションで使用**  — 列見出しにフィルターコントロールを追加します ( _[!UICONTROL Products]_リスト。

## 手順 3：フィールドラベルを入力する

1. 左側のナビゲーションで、「 」を選択します。 **[!UICONTROL Manage Labels]**.

1. を入力します。 **[!UICONTROL Title]** フィールドのラベルとして使用されます。

   ストアが異なる言語で使用できる場合は、各ビューに翻訳されたタイトルを入力できます。

   ![製品属性 — タイトルを管理](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 手順 4：ストアフロントのプロパティを説明する

1. 左側のナビゲーションで、「 」を選択します。 **[!UICONTROL Storefront Properties]**.

   ![製品属性 — ストアフロントプロパティ](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   使用可能なオプションは、 _[!UICONTROL Catalog Input Type for Store Owner]_設定。

1. 属性を検索に使用できるようにする場合は、 **[!UICONTROL Use in Search]** から `Yes`.

   - を設定します。 **[!UICONTROL Search Weight]** 値：検索結果での項目の表示場所を制御します。1（最も小さい重み）～ 10（最も大きい重み）。

   - を設定します。 **[!UICONTROL Visible in Advanced Search]** 必要に応じて。 詳しくは、 [詳細検索](search.md#advanced-search).

1. 製品比較に属性を含めるには、 **[!UICONTROL Comparable on Storefront]** から `Yes`.

1. ドロップダウン、複数の選択、価格の各フィールドで、次の操作を行います。

   - レイヤーナビゲーションで属性をフィルタとして使用するには、 **[!UICONTROL Use in Layered Navigation]** から `Yes`.

   - 検索結果ページのレイヤーナビゲーションで属性を使用するには、 **[!UICONTROL Use in Search Results Layered Navigation]** から `Yes`.

   - の場合 **[!UICONTROL Position]**」で、レイヤー化されたナビゲーションブロック内の属性の相対位置を示す数値を入力します。

1. 価格ルールで属性を使用するには、 **[!UICONTROL Use for Promo Rule Conditions]** から `Yes`.

1. テキストの書式設定をHTMLに許可するには、 **[!UICONTROL Allow HTML Tags on Frontend]** から `Yes`.

   この設定により、WYSIWYG エディターがフィールドで使用できるようになります。

1. 製品ページに属性を含めるには、 **[!UICONTROL Visible on Catalog Pages on Storefront]** から `Yes`.

1. テーマでサポートされている場合は、次の設定を実行します。

   - 製品リストに属性を含めるには、 **[!UICONTROL Used in Product Listing]** から `Yes`.

   - 属性を製品リストの並べ替えパラメータとして使用するには、 **[!UICONTROL Used for Sorting in Product Listing]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Attribute]**.

## 手順 5：作成した属性を属性セットに割り当てる

製品作成ページに表示される属性を特定の属性セットに追加します。

1. 前の手順を完了したら、に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. 必要な属性セットをリストから選択し、編集モードで開きます。

1. 作成した属性を **[!UICONTROL Unassigned Attributes]** リストを **グループ** 列。

1. 完了したら、「 **[!UICONTROL Save]**.

## 設定可能な製品の属性

のオプションのドロップダウンリストとして使用される任意の属性 [設定可能な製品](product-create-configurable.md) は、次のプロパティを持つ必要があります。

| プロパティ | 値 |
|----------|------ |
| ストア所有者のカタログ入力タイプ | ドロップダウン |
| 範囲 | グローバル |

{style="table-layout:auto"}

## 属性の削除

属性が削除されると、関連する製品および属性セットから削除されます。 システム属性はストアのコア機能の一部で、削除できません。

属性を削除する前に、カタログ内のどの製品でも属性が現在使用されていないことを確認します。 属性が使用中かどうかを簡単に判断するには、 [書き出し](../systems/data-export.md) ツールを使用して、製品のエンティティ属性のリストを確認できます。 属性がリストに含まれていない場合、カタログ内のどの製品にも使用されません。

**_属性を削除するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. リストで属性を探し、編集モードで開きます。

1. クリック **[!UICONTROL Delete Attribute]**.

   ![属性を削除](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. 確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.
