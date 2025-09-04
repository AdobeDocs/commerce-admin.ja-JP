---
title: 仮想製品
description: メンバーシップ、サービス、保証、サブスクリプションなど、実体以外の項目を表す仮想製品を作成する方法について説明します。
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# 仮想製品

仮想製品（デジタル商品）は、メンバーシップ、サービス、保証、購読、書籍、音楽、ビデオ、その他の製品のデジタルダウンロードなど、非有形の項目を表します。 バーチャル製品は、個別に販売することも、[ グループ化された製品 ](product-create-grouped.md)、[ 設定可能な製品 ](product-create-configurable.md)、または [ バンドル製品 ](product-create-bundle.md) 製品タイプの一部として含めることもできます。

_[!UICONTROL Weight]_の分野がないことはさておき、仮想製品と単純な製品を作成するプロセスは同じです。 以下の手順では、[ 製品テンプレート ](attribute-sets.md)、必須フィールド、基本設定を使用して仮想製品を作成するプロセスを示します。 基本を完了したら、必要に応じて他の製品設定を完了できます。

>[!NOTE]
>
>PayPal は、PayPal Express Checkout を通じたデジタル商品の販売に対するサポートを廃止しました。 仮想製品を含む注文を処理するには、[PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) またはその他の PayPal 支払いゲートウェイを使用することをお勧めします。

![ 仮想製品 ](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 右上隅の _[!UICONTROL Add Product]_（メニュー矢印 ![ メニューで ](../assets/icon-menu-down-arrow-red.png){width="25"} 「**[!UICONTROL Virtual Product]**」を選択します。

   ![ 仮想製品を追加 ](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

製品のテンプレートとして使用される [ 属性セット ](attribute-sets.md) を選択するには、次のいずれかの操作を行います。

- 「**[!UICONTROL Attribute Set]**」フィールドをクリックし、属性セット名の全部または一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![ 属性セットを選択 ](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. **[!UICONTROL Product Name]** を入力します。

1. 製品名に基づくデフォルト **[!UICONTROL SKU]** を受け入れるか、別の名前を入力します。

1. 製品 **[!UICONTROL Price]** を入力します。

1. 製品はまだ公開する準備ができていないので、**[!UICONTROL Enable Product]** を `No` に設定します。

1. 「**[!UICONTROL Save]**」をクリックして続行します。

   商品を保存すると、左上隅に [ ストア表示 ](introduction.md#product-scope) 選択が表示されます。

1. 製品を使用できる **[!UICONTROL Store View]** を選択します。

   ![ ストア表示の選択 ](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定を完了する

1. **[!UICONTROL Tax Class]** を次のいずれかに設定します。

   - `None`
   - `Taxable Goods`

1. 在庫がある商品の **[!UICONTROL Quantity]** を入力し、次の操作を行います。

   - **[!UICONTROL Stock Status]** のデフォルトの `In Stock` 設定を受け入れます。

     仮想製品は出荷されないので、**[!UICONTROL Weight]** フィールドは使用されません。

   - **[!UICONTROL Visibility]** のデフォルトの `Catalog, Search` 設定を受け入れます。

   >[!NOTE]
   >
   >[Inventory management](../inventory-management/introduction.md) を有効にした場合、単一ソース マーチャントがこのセクションで数量を設定します。 マルチソースのマーチャントは、「ソース」セクションでソースと数量を追加します。 次の _ソースと数量の割り当て（Inventory management）_ 節を参照してください。

1. 製品に **[!UICONTROL Categories]** を割り当てるには、**[!UICONTROL Select…]** のボックスをクリックし、次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致するものが見つかるまで、ボックスに入力を開始します。

   - 割り当てるカテゴリのチェックボックスを選択します。

   **カテゴリを作成する**:

   - 「**[!UICONTROL New Category]**」をクリックします。

   - **[!UICONTROL Category Name]** を入力し、メニュー構造内の位置を決定する **[!UICONTROL Parent Category]** を選択します。

   - 「**[!UICONTROL Create Category]**」をクリックします。

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
>「_[!UICONTROL Is this downloadable product?]_」オプションは、デフォルトで無効になっています。 仮想製品に対してこの機能を有効にすると、製品が [ ダウンロード可能 ](product-create-downloadable.md#downloadable-product) になります。

## 手順 6：製品を公開する

1. カタログに製品を公開する準備が整ったら、**[!UICONTROL Enable Product]** を `Yes` に設定します。

1. 次のいずれかの操作を行います。

   - **方法 1:** 保存とプレビュー

      - 右上隅にある「**[!UICONTROL Save]**」をクリックします。

      - ストアで製品を表示するには、**[!UICONTROL Customer View]** 管理者 _（_ メニュー矢印 ![） メニューの ](../assets/icon-menu-down-arrow-black.png) を選択します。

     ストアが新しいブラウザータブで開きます。

     ![ 顧客ビュー ](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **メソッド 2:** 保存して閉じる

     _[!UICONTROL Save]_（メニュー矢印 ![ メニューで ](../assets/icon-menu-down-arrow-red.png){width="25"} 「**[!UICONTROL Save & Close]**」を選択します。

## 注意事項

- 仮想製品は、サービス、サブスクリプション、保証などの非有形製品に使用されます。

- 仮想製品は単純な製品のようなものですが、重量はありません。

- 買い物かごに実物の製品がない限り、チェックアウト時に配送オプションは表示されません。

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
