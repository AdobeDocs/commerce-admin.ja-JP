---
title: 仮想製品
description: メンバーシップ、サービス、保証、サブスクリプションなど、実体以外の項目を表す仮想製品を作成する方法について説明します。
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# 仮想製品

仮想製品（デジタル商品）は、メンバーシップ、サービス、保証、購読、書籍、音楽、ビデオ、その他の製品のデジタルダウンロードなど、非有形の項目を表します。 バーチャル製品は、個別に販売することも、 [グループ化された製品](product-create-grouped.md), [設定可能な製品](product-create-configurable.md)、または [バンドル製品](product-create-bundle.md) 製品タイプ。

～が存在しないことをのぞけば _[!UICONTROL Weight]_フィールド、仮想製品と単純製品の作成プロセスは同じです。 以下の手順は、を使用して仮想製品を作成するプロセスを示しています。 [製品テンプレート](attribute-sets.md)、必須フィールド、基本設定です。 基本を完了したら、必要に応じて他の製品設定を完了できます。

>[!NOTE]
>
>PayPal は、PayPal Express Checkout を通じたデジタル商品の販売に対するサポートを廃止しました。 次のいずれかを使用することをお勧めします [PayPal 支払い標準](../stores-purchase/paypal-payments-standard.md) または、仮想製品を含むあらゆる注文を処理するためのその他の PayPal 支払いゲートウェイ。

![バーチャル製品](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 日 _[!UICONTROL Add Product]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ）メニューを選択し、**[!UICONTROL Virtual Product]**.

   ![バーチャル製品の追加](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択します [属性セット](attribute-sets.md) このテンプレートを使用して、次のいずれかの操作を行います。

- 内をクリック **[!UICONTROL Attribute Set]** フィールドに、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. を入力 **[!UICONTROL Product Name]**.

1. デフォルトを使用 **[!UICONTROL SKU]** これは製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだ整っていないので、を設定します **[!UICONTROL Enable Product]** 対象： `No`.

1. クリック **[!UICONTROL Save]** そして続けて。

   商品を保存すると、 [ストア表示](introduction.md#product-scope) 選択が左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品の入手先。

   ![ストア表示を選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定を完了する

1. を設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

1. を入力 **[!UICONTROL Quantity]** 在庫がある商品の。次の操作を行います。

   - デフォルトを使用 **[!UICONTROL Stock Status]** の設定 `In Stock`.

     仮想製品は出荷されないので、 **[!UICONTROL Weight]** フィールドは使用されません。

   - デフォルトを使用 **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

   >[!NOTE]
   >
   >有効にする場合 [Inventory management](../inventory-management/introduction.md)、単一ソースのマーチャントがこのセクションで数量を設定します。 マルチソースのマーチャントは、「ソース」セクションでソースと数量を追加します。 以下を参照してください _ソースと数量の割り当て（Inventory management）_ セクション。

1. 割り当てる **[!UICONTROL Categories]** 製品に移動するには、 **[!UICONTROL Select…]** 次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致するものが見つかるまで、ボックスに入力を開始します。

   - 割り当てるカテゴリのチェックボックスを選択します。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - を入力 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内の位置を指定します。

   - クリック **[!UICONTROL Create Category]**.

   製品を説明する追加の個人属性が存在する場合があります。 選択は属性セットによって異なり、後で完了できます。

### ソースと数量の割り当て（[!DNL Inventory Management]）

{{$include /help/_includes/inventory-assign-sources.md}}

## 手順 5：製品情報の入力

必要に応じて、以下の節の情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイトの製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

>[!NOTE]
>
>この _[!UICONTROL Is this downloadable product?]_オプションはデフォルトで無効になっています。 仮想製品に対してこの機能を有効にすると、製品が作成されます [ダウンロード可能](product-create-downloadable.md#downloadable-product).

## 手順 6：製品を公開する

1. カタログに製品を公開する準備が整ったら、次のように設定します **[!UICONTROL Enable Product]** 対象： `Yes`.

1. 次のいずれかの操作を行います。

   - **メソッド 1:** 保存とプレビュー

      - 右上隅のをクリックします。 **[!UICONTROL Save]**.

      - ストアで商品を表示するには、次を選択します **[!UICONTROL Customer View]** 日 _Admin_ （ ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ） メニューを使用できます。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **メソッド 2:** 保存して閉じる

     日 _[!UICONTROL Save]_（![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## 注意事項

- 仮想製品は、サービス、サブスクリプション、保証などの非有形製品に使用されます。

- 仮想製品は単純な製品のようなものですが、重量はありません。

- 買い物かごに実物の製品がない限り、チェックアウト時に配送オプションは表示されません。
