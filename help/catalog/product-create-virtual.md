---
title: 仮想製品
description: メンバーシップ、サービス、保証、サブスクリプションなど、有形でない品目を表す仮想製品の作成方法を説明します。
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 仮想製品

バーチャル製品（デジタル商品）は、会員、サービス、保証、購読、書籍、音楽、ビデオ、その他の製品のデジタルダウンロードなど、非有形の項目を表します。 仮想製品は個別に販売することも、 [グループ化された製品](product-create-grouped.md), [設定可能な製品](product-create-configurable.md)または [バンドル製品](product-create-bundle.md) 製品タイプ。

～がない以外は _[!UICONTROL Weight]_仮想製品と単純な製品の作成プロセスは同じです。 以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

>[!NOTE]
>
>PayPal は、PayPal Express Checkout を通じたデジタル商品販売のサポートを廃止しました。 次のいずれかを使用することをお勧めします。 [PayPal 支払い標準](../stores-purchase/paypal-payments-standard.md) または仮想製品を含む注文を処理するための他の PayPal 支払いゲートウェイ。

![仮想製品](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次の日： _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューを使用して、**[!UICONTROL Virtual Product]**.

   ![仮想製品を追加](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択するには、以下を実行します。 [属性セット](attribute-sets.md) 製品のテンプレートとして使用されるを次のいずれかの操作を行います。

- をクリックします。 **[!UICONTROL Attribute Set]** フィールドに値を入力し、属性セットの名前のすべてまたは一部を入力します。

- 表示されたリストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. 次を入力します。 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れる **[!UICONTROL SKU]** 製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだできていないので、を設定します。 **[!UICONTROL Enable Product]** から `No`.

1. クリック **[!UICONTROL Save]** 続行します。

   製品を保存すると、 [ストア表示](introduction.md#product-scope) セレクタが左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品を使用できる場所。

   ![ストア表示の選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定の完了

1. 設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

1. 次を入力します。 **[!UICONTROL Quantity]** の製品が在庫にあり、次の操作を行います。

   - デフォルトを受け入れる **[!UICONTROL Stock Status]** の設定 `In Stock`.

     仮想製品が出荷されていないので、 **[!UICONTROL Weight]** フィールドが使用されていません。

   - デフォルトを受け入れる **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

   >[!NOTE]
   >
   >有効にした場合 [Inventory management](../inventory-management/introduction.md)では、1 つのソース・マーチャントがこのセクションで数量を設定します。 複数ソースのマーチャントが「ソース」セクションにソースと数量を追加します。 次を参照してください。 _ソースと数量の割り当て (Inventory management)_ 」セクションに入力します。

1. 割り当てるには **[!UICONTROL Categories]** を製品に対して、 **[!UICONTROL Select…]** 」ボックスに移動し、次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致が見つかるまで、ボックスに入力します。

   - 割り当てるカテゴリのチェックボックスをオンにします。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - 次を入力します。 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内での位置を決定します。

   - クリック **[!UICONTROL Create Category]**.

   製品を説明する個々の属性が追加される場合があります。 選択は属性セットによって異なり、後で完了できます。

### ソースと数量を割り当てる ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 手順 5：製品情報の入力

必要に応じて、次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイト内の製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

>[!NOTE]
>
>The _[!UICONTROL Is this downloadable product?]_オプションはデフォルトで無効になっています。 仮想製品に対してこの機能を有効にすると、製品が作成されます [ダウンロード可能](product-create-downloadable.md#downloadable-product).

## 手順 6：製品の公開

1. カタログに商品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** から `Yes`.

1. 次のいずれかの操作を行います。

   - **メソッド 1:** 保存してプレビュー

      - 右上隅で、 **[!UICONTROL Save]**.

      - ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ) メニューを使用します。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法 2:** 保存して閉じる

     次の日： _[!UICONTROL Save]_(![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## 覚えておくべきこと

- 仮想製品は、サービス、購読、保証などの非有形製品に使用されます。

- 仮想製品は、単純な製品に似ていますが、重さはありません。

- 出荷オプションは、買い物かごに有形製品がない限り、チェックアウト時に表示されません。
