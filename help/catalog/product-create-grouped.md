---
title: グループ化された製品
description: グループとして提示されるシンプルなスタンドアロン製品で構成されるグループ化された製品を作成する方法を説明します。
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# グループ化された製品

グループ化された製品は、単純なスタンドアロン製品で構成され、グループとして表示されます。 1 つの製品のバリエーションを提供したり、シーズン別またはテーマ別にグループ化したりできます。 グループ化された製品を提示すると、顧客が追加の品目を購入するインセンティブを作成できます。 グループ化された製品では、製品のバリエーションを簡単に提供し、すべてを同じページに一覧表示できます。

例えば、オープンストックのフラットウェアを販売し、正式な場所の設定で使用されるすべての種類の器具をリストすることができます。 複数のサラダフォーク、魚のフォーク、ディナーフォーク、ディナーナイフ、魚のナイフ、バターナイフ、スープスプーン、デザートスプーンを注文する人もいます。 他のお客様は、簡単なフォーク、ナイフ、スプーンを注文するかもしれません。 お客様は、各品目の数に応じて任意の数の注文を行うことができます。

グループとして提示されますが、グループ内の各製品は別々の品目として購入されます。 買い物かごでは、各品目と購入した数量が別々の行項目として表示されます。

以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 各必須フィールドには赤いアスタリスク (`*`) をクリックします。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

![グループ化された製品](./assets/product-grouped.png){width="700" zoomable="yes"}

## 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次の日： _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューを使用して、**[!UICONTROL Grouped Product]**.

   ![グループ化された製品を追加](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択するには、以下を実行します。 [属性セット](attribute-sets.md) 製品のテンプレートとして使用されるを次のいずれかの操作を行います。

- 検索するには、 **[!UICONTROL Attribute Set]**.
- リストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![テンプレートを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

必要な属性が存在しない場合は、製品の作成時に新しい属性を追加できます。

- 右上隅で、 **[!UICONTROL Add Attribute]**.
- 新しい属性を定義します ( [製品への属性の追加](product-attributes-add.md)) をクリックします。

  ![新しい属性](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

製品に既存の属性を追加するには、 [フィルターコントロール](../getting-started/admin-grid-controls.md) グリッド内の属性を検索し、次の操作を行います。

- 追加する各属性の最初の列にあるチェックボックスを選択します。
- クリック **[!UICONTROL Add Selected]**.

## 手順 3：必要な設定を完了する

1. 次を入力します。 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れる **[!UICONTROL SKU]** 製品名に基づくか、別の名前を入力します。

   なお、 **[!UICONTROL Quantity]** 値はグループを構成する個々の製品から派生しているので、フィールドは使用できません。

   グループ化された製品は、カタログに独自の価格を持ちません。 グループ化された製品価格は、グループに含まれる個々の製品の価格から導き出されます。

1. 製品の公開準備がまだできていないので、を設定します。 **[!UICONTROL Enable Product]** から `No` ( ![切り替えなし](../assets/toggle-no.png) ) をクリックします。

1. クリック **[!UICONTROL Save]** 続行します。

   製品を保存すると、製品名がページの上部に表示され、 [ストア表示](introduction.md#product-scope) セレクタが左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品を使用できる場所。

   ![ストア表示の選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定の完了

1. を受け入れる **[!UICONTROL Stock Status]** の設定 `In Stock`.

1. 割り当てるには **[!UICONTROL Categories]** を製品に対して、 **[!UICONTROL Select…]** 」ボックスに移動し、次のいずれかの操作を行います。

   **既存のカテゴリを選択：**

   - 一致が見つかるまで、ボックスに入力します。

   - 割り当てるカテゴリのチェックボックスをオンにします。

   **カテゴリの作成：**

   - クリック **[!UICONTROL New Category]**.

   - 次を入力します。 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内での位置を決定します。

   - クリック **[!UICONTROL Create Category]**.

1. を受け入れる **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 製品を [新製品のリスト](../content-design/widget-new-products-list.md)、選択 **[!UICONTROL Set Product as New]** **[!UICONTROL from]** および **[!UICONTROL to]** 日付をカレンダーに追加します。

1. を選択します。 **[!UICONTROL Country of Manufacture]**.

   製品を説明する個々の属性が追加される場合があります。 選択は属性セットを変え、後で完了できます。

## 手順 5：グループに製品を追加する

1. 下にスクロールして、 **[!UICONTROL Grouped Products]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Add Products to Group]**.

   ![グループ化された製品](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. 必要に応じて、 [フィルター](../getting-started/admin-grid-controls.md) をクリックして、グループに含める製品を検索します。

1. リストで、グループに含める各項目のチェックボックスをオンにします。

   >[!NOTE]
   >
   >子製品のグループ化は、設定可能なオプションを持たない、シンプル、ダウンロード可能、および仮想製品のみ可能です。 その他の製品タイプは、選択リストに表示されません。

   ![選択した製品を追加](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. 製品グループに追加するには、 **[!UICONTROL Add Selected Products]**.

   選択した製品が _[!UICONTROL Grouped Products]_」セクションに入力します。

   複数ソースのマーチャントの場合： [Inventory management](../inventory-management/sources-stocks.md)の場合、グリッドには **[!UICONTROL Quantity per Source]** 列に、各割り当て済みのソースと在庫の在庫金額が表示されます。

   ![グループ内の製品](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. を入力します。 **[!UICONTROL Default Quantity]** のいずれかの項目に対して。

1. 製品の順序を変更するには、 _変更管理_ アイコン ( ![位置コントローラ](../assets/icon-sort-order.png) ) をクリックし、製品をリストの新しい位置にドラッグします。

1. グループから製品を削除するには、 **[!UICONTROL Remove]**.

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

## 手順 6：製品の公開

1. カタログに商品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** から `Yes`.

1. 次のいずれかの操作を行います。

   **メソッド 1:** 保存してプレビュー

   - 右上隅で、 **[!UICONTROL Save]**.

   - ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ) メニューを使用します。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **方法 2:** 保存して閉じる

   - 次の日： _[!UICONTROL Save]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## 手順 7：買い物かごのサムネールの設定（オプション）

グループ内の製品ごとに異なる画像がある場合、買い物かごのサムネールに正しい画像を使用するように設定できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Shopping Cart]**.

   これらの設定オプションの詳細なリストについては、 [買い物かご](../configuration-reference/sales/checkout.md#shopping-cart) （内） _設定リファレンス_.

1. 設定 **[!UICONTROL Grouped Product Image]** から `Product Thumbnail Itself`.

   ![買い物かご](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   必要に応じて、「 **[!UICONTROL Use system value]** 」チェックボックスをオンにしてこのオプションを設定します。

1. クリック **[!UICONTROL Save Config]**.

## 覚えておくべきこと

- グループ化された製品は、基本的には単純な関連製品のコレクションです。

- グループ化された子製品は、シンプルな、ダウンロード可能な、または仮想製品にすることができます **[!UICONTROL without custom options]**.

- 購入した各品目は、グループの一部ではなく、買い物かごに個別に表示されます。

- グループ化された製品は、カタログに独自の価格を持ちません。 グループ化された製品価格は、グループに含まれる個々の製品の価格から導き出されます。

- 買い物かごのサムネール画像を設定して、グループ化された親製品または関連する製品の画像を表示できます。
