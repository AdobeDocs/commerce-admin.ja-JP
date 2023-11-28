---
title: シンプルな製品
description: 個別に、またはグループ化、設定、またはバンドル製品の一部として販売できる、シンプルな製品を作成する方法を説明します。
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# シンプルな製品

製品タイプの力を活かす鍵の 1 つは、シンプルでスタンドアロンの製品を使用するタイミングを学ぶことです。 単純な製品は、個別に販売することも、グループ化、設定、バンドル製品の一部として販売することもできます。 カスタムオプションを含むシンプルな製品は、 _複合製品_.

以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 各必須フィールドには赤いアスタリスク (`*`) をクリックします。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

![シンプルな製品](./assets/product-simple.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次の日： _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューを右上に表示し、「 」を選択します。**[!UICONTROL Simple Product]**.

   ![シンプルな製品を追加](./assets/product-add-simple.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択するには、以下を実行します。 [属性セット](attribute-sets.md) 製品のテンプレートとして使用される

- をクリックします。 **[!UICONTROL Attribute Set]** フィールドに値を入力し、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. 次を入力します。 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れる **[!UICONTROL SKU]** 製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだできていないので、 **[!UICONTROL Enable Product]** 選択肢 `No`.

1. click **[!UICONTROL Save]** 続行します。

   製品を保存すると、 [ストア表示](introduction.md#product-scope) セレクタが左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品を使用できる場所。

   ![ストア表示を選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定の完了

1. 設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. 次を入力します。 **[!UICONTROL Quantity]** 保管されている製品の。

   デフォルトでは、 **[!UICONTROL Stock Status]** が `In Stock`.

   >[!NOTE]
   >
   >有効にした場合 [Inventory management](../inventory-management/introduction.md)を使用する場合、単一ソースのマーチャントがこのセクションで数量を設定します。 複数ソースのマーチャントは、「ソース」セクションにソースと数量を追加します。 次を参照してください。 _ソースと数量の割り当て (Inventory management)_ 」セクションに入力します。

1. 次を入力します。 **[!UICONTROL Weight]** 製品の。

1. デフォルトを受け入れる **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 割り当てるには _[!UICONTROL Categories]_を製品に対して、**[!UICONTROL Select…]**」ボックスに移動し、次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致が見つかるまで、ボックスに入力します。

   - 割り当てる各カテゴリのチェックボックスをオンにします。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - 次を入力します。 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内での位置を決定します。

   - クリック **[!UICONTROL Create Category]**.

1. 次のリストで製品を特集するには： [新製品](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. を選択します。 **[!UICONTROL Country of Manufacture]**.

製品を説明する個々の属性が追加される場合があります。 選択は属性セットによって異なり、後で完了できます。

### ソースと数量を割り当てる ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 手順 5：製品情報の入力

下にスクロールし、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイト内の製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

## 手順 6：製品の公開

1. カタログに商品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** に切り替える `Yes`.

1. 次のいずれかの操作を行います。

   - **メソッド 1:** 保存してプレビュー

      - 右上隅で、 **[!UICONTROL Save]**.

      - ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ (![メニュー矢印](../assets/icon-menu-down-arrow-black.png)) メニューを使用します。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法 2:** 保存して閉じる

     次の日： _[!UICONTROL Save]_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## 覚えておくべきこと

- シンプルな製品は、構成可能な製品、バンドル製品、グループ化された製品タイプに含めることができます。

- 単純な製品設定は、特定の製品の設定可能な製品設定を上書きします。

- シンプルな製品には、様々な入力タイプのカスタムオプションを含めることができるので、1 つの SKU から多くの製品バリエーションを販売できます。
