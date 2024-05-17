---
title: シンプル製品
description: 個別に、またはグループ化された製品、設定可能な製品、バンドル製品の一部として販売できる、シンプルな製品を作成する方法について説明します。
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# シンプル製品

製品タイプの力を活用するための鍵の 1 つは、シンプルなスタンドアロン製品を使用するタイミングを学ぶことです。 シンプルな製品は、個別に販売することも、グループ化された製品、設定可能な製品、バンドル製品の一部として販売することもできます。 カスタムオプションを含む単純な製品は、と呼ばれることがあります。 _複合製品_.

以下の手順は、を使用して単純な製品を作成するプロセスを示しています。 [製品テンプレート](attribute-sets.md)、必須フィールド、基本設定です。 各必須フィールドには、赤いアスタリスク（`*`）に設定します。 基本を完了したら、必要に応じて他の製品設定を完了できます。

![シンプル製品](./assets/product-simple.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 日 _[!UICONTROL Add Product]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ）メニューを選択します。**[!UICONTROL Simple Product]**.

   ![シンプルな製品を追加](./assets/product-add-simple.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択します [属性セット](attribute-sets.md) これは、製品のテンプレートとして使用されます。

- 内をクリック **[!UICONTROL Attribute Set]** フィールドに、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. を入力 **[!UICONTROL Product Name]**.

1. デフォルトを使用 **[!UICONTROL SKU]** これは製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだ整っていないので、 **[!UICONTROL Enable Product]** 対するオプション `No`.

1. click **[!UICONTROL Save]** そして続けて。

   商品を保存すると、 [ストア表示](introduction.md#product-scope) 選択が左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品の入手先。

   ![ストア表示の選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定を完了する

1. を設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

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

1. を入力 **[!UICONTROL Quantity]** 在庫がある商品の。

   デフォルトでは **[!UICONTROL Stock Status]** はに設定されています。 `In Stock`.

   >[!NOTE]
   >
   >有効にする場合 [Inventory management](../inventory-management/introduction.md)、単一ソースのマーチャントがこのセクションで数量を設定します。 マルチソースマーチャントは、「ソース」セクションでソースと数量を追加します。 以下を参照してください _ソースと数量の割り当て（Inventory management）_ セクション。

1. を入力 **[!UICONTROL Weight]** 商品の。

1. デフォルトを使用 **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 割り当てる _[!UICONTROL Categories]_製品に移動するには、**[!UICONTROL Select…]**次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致するものが見つかるまで、ボックスに入力を開始します。

   - 割り当てる各カテゴリのチェックボックスを選択します。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - を入力 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内の位置を指定します。

   - クリック **[!UICONTROL Create Category]**.

1. 製品をリストに表示するには [新製品](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. を選択します。 **[!UICONTROL Country of Manufacture]**.

製品を説明する追加の個人属性が存在する場合があります。 選択は属性セットによって異なり、後で完了できます。

### ソースと数量の割り当て（[!DNL Inventory Management]）

{{$include /help/_includes/inventory-assign-sources.md}}

## 手順 5：製品情報の入力

下にスクロールして、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイトの製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

## 手順 6：製品を公開する

1. カタログに製品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** 切り替え先 `Yes`.

1. 次のいずれかの操作を行います。

   - **メソッド 1:** 保存とプレビュー

      - 右上隅のをクリックします。 **[!UICONTROL Save]**.

      - ストアで商品を表示するには、次を選択します **[!UICONTROL Customer View]** 日 _Admin_ （![メニュー矢印](../assets/icon-menu-down-arrow-black.png)） メニューを使用できます。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **メソッド 2:** 保存して閉じる

     日 _[!UICONTROL Save]_ （ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- シンプルな製品は、設定可能な製品、バンドル製品、グループ化された製品タイプに含めることができます。

- シンプルな製品設定は、特定の製品の設定可能な製品設定を上書きします。

- シンプルな製品には、様々なタイプの入力を含むカスタムオプションを含めることができ、単一の SKU から多くの製品バリエーションを販売できます。
