---
title: 設定可能な製品
description: 買い物客に選択のバリエーションを提供する設定可能な製品を作成する方法を説明します。
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: f6140fda2769e109d2b38c2f9c458f67097dff0a
workflow-type: tm+mt
source-wordcount: '2483'
ht-degree: 0%

---

# 設定可能な製品

設定可能な製品は、各バリエーションのドロップダウンリストを含む単一の製品のように見えます。 各リスト項目は、実際には一意の SKU を持つ個別のシンプルな製品なので、各製品バリエーションの在庫を追跡できます。 カスタムオプションでシンプルな製品を使用して、同様の効果を得ることができますが、各バリエーションの在庫を追跡する機能はありません。

以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 各必須フィールドには赤いアスタリスク (`*`) をクリックします。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

![設定可能な製品](./assets/product-configurable.png){width="700" zoomable="yes"}

## パート 1：設定可能な製品の作成

設定可能な製品では、より多くの SKU を使用し、最初は設定に少し時間がかかる場合がありますが、最終的に時間を節約できます。 ビジネスを拡大する予定がある場合は、複数のオプションを持つ製品に適した製品タイプを選択できます。

開始する前に、 [属性セット](attribute-sets.md) には、製品のバリエーションごとに許容される入力タイプの 1 つに設定された属性が含まれます。 例えば、属性セットには、色とサイズのドロップダウン属性を含めることができます。

設定可能な製品バリエーションに使用される各属性のプロパティには、次の設定が必要です。

### 製品バリエーション属性の要件

| プロパティ | 設定 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | 製品バリエーションに使用される属性の入力タイプは、次のいずれかにする必要があります。 `Dropdown`, `Visual Swatch`または `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次の日： _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューを使用して、**[!UICONTROL Configurable Product]**.

   ![設定可能な製品を追加](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

The [属性セット](attribute-sets.md) 製品で使用されるフィールドの選択を決定します。 次の例で使用する属性セットには、色とサイズの属性が含まれています。 属性セットの名前はページの上部に表示され、最初はに設定されます。 `Default`.

1. 製品の属性セットを選択するには、ページ上部の「 」フィールドをクリックし、次のいずれかの操作をおこないます。

   - の場合 **[!UICONTROL Search]**」で、属性セットの名前を入力します。
   - リストで、使用する属性セットを選択します。

   フォームが更新され、変更が反映されます。

1. 属性セットに別の属性を追加する場合は、 **[!UICONTROL Add Attribute]** をクリックし、 [属性の追加](product-attributes-add.md).

   ![テンプレートを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 手順 3：必要な設定を完了する

1. 製品を入力 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れる **[!UICONTROL SKU]** 製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだできていないので、を設定します。 **[!UICONTROL Enable Product]** から `No`.

1. click **[!UICONTROL Save]** 続行します。

   製品を保存すると、 [ストア表示](introduction.md#product-scope) セレクタが左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品を使用できる場所。

   ![ストア表示を選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 手順 4：基本設定の完了

1. 設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

1. The **[!UICONTROL Quantity]** は製品のバリエーションによって決まるので、空白のままにできます。

1. を残します。 **[!UICONTROL Stock Status]** 設定されたとおり。

   設定可能な製品の在庫ステータスは、関連する各設定によって決まります。 製品は数量を入力せずに保存されたので、 **[!UICONTROL Stock Status]** が `Out of Stock`.

   >[!NOTE]
   >
   >The **在庫ステータス** 設定可能な製品の **_半手動で_** 制御設定。 子製品の在庫状況によって部分的に管理されます。 これは、 **_複数条件_** 在庫ステータスの計算 ( [在庫ステータスの設定](#configure-the-stock-status) 」セクションに入力します。

1. 製品を入力 **[!UICONTROL Weight]**.

>[!NOTE]
>
>設定可能な製品には、常に重み付けが必要です。 次を選択した場合、 **[!UICONTROL This item has no weight]** ドロップダウンリストから、自動的に「 」に変更されます。 **[!UICONTROL This item has weight]** 製品を保存した後。

1. デフォルトを受け入れる **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 次のリストで製品を特集するには： [新製品](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. カテゴリを商品に割り当てるには、 **[!UICONTROL Select…]** 」ボックスに移動し、次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致が見つかるまで、ボックスに入力します。

   - 割り当てるカテゴリのチェックボックスをオンにします。

   ![バンドル製品の 1 つ以上のカテゴリを選択します](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - 次を入力します。 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内での位置を決定します。

   s — クリック **[!UICONTROL Create Category]**.

1. を選択します。 **[!UICONTROL Country of Manufacture]**.

   製品の説明に使用される追加の属性が存在する場合があります。 選択は属性セットによって異なり、後で完了できます。

### 手順 5：保存して続行する

今は、作業を保存する良い機会です。 右上隅で、 **[!UICONTROL Save]**. 次の一連の手順では、製品の各バリエーションに対して設定をセットアップします。

## パート 2：設定の追加

次の例は、3 つの色と 3 つのサイズの設定を追加する方法を示しています。 すべてのバリエーションの組み合わせに対応するために、9 つのシンプルな製品が一意の SKU で作成されています。 デフォルトでは、各バリエーションの製品名と SKU は、属性値と親の製品名または SKU に基づいています。

ページ上部のプログレスバーにプロセスの進行状況が表示され、各ステップの指示が示されます。

### 手順 1：属性の選択

1. 上から続けて、下にスクロールして _[!UICONTROL Configurations]_「 」セクションで、「 」をクリックします。**[!UICONTROL Create Configurations]**.

   ![設定](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. 設定として含める各属性のチェックボックスをオンにします。

   この例の場合、 `color` および `size` が選択されている。

   ![属性を選択](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   このリストには、設定可能なプロダクトで使用できる属性セットのすべての属性が含まれます。

1. 属性を追加する場合は、 **[!UICONTROL Create New Attribute]** 次の操作を実行します。

   - 属性プロパティを設定します。

   - クリック **[!UICONTROL Save Attribute]**.

   - 属性のチェックボックスをオンにします。

1. 右上隅で、 **[!UICONTROL Next]**.

### 手順 2：属性値を入力する

1. 各属性で、製品に適用する値のチェックボックスをオンにします。

   ![属性値](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 属性を並べ替えるには、 _並べ替え_ ( ![並べ替え順アイコン](../assets/icon-sort-order.png) ) アイコンをクリックし、セクションを新しい位置に移動します。

   順序によって、製品ページでのドロップダウンリストの位置が決まります。

1. プログレスバーで、 **[!UICONTROL Next]**.

### 手順 3：画像、価格、数量の設定

この手順では、各設定の画像、価格、数量を決定します。 使用可能なオプションはそれぞれ同じで、1 つだけ選択できます。 すべての SKU に同じ設定を適用したり、各 SKU に固有の設定を適用したり、現時点では設定をスキップしたりできます。

適用する設定オプションを選択します。

次のいずれかの方法を使用して、 **[!UICONTROL images]**:

**メソッド 1:** 1 組の画像をすべての SKU に適用

1. 選択 **[!UICONTROL Apply single set of images to all SKUs]**.

1. 製品ギャラリーに含める各画像を参照するか、ボックスにドラッグします。

![すべての SKU に同じ画像を使用](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**方法 2:** 各 SKU に対する個別画像の適用

親製品の画像は既にアップロードされているので、このオプションを使用して各色の画像をアップロードできます。 特定の色で商品を購入したときに買い物かごに表示される別の画像を追加できます。

1. 選択 **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. を選択します。 **[!UICONTROL Attribute]** 例えば、画像が示す `color`.

1. 属性値ごとに、その設定に使用する画像を参照するか、ボックスにドラッグします。

   画像を値ボックスにドラッグすると、他の値のセクションにも表示されます。 画像を削除する場合は、 _ごみ箱_ (![ごみ箱アイコン](../assets/icon-delete-trashcan-solid.png)) アイコンをクリックします。

   ![SKU ごとの個別画像数](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

次のいずれかの方法を使用して、 **[!UICONTROL prices]**:

>[!NOTE]
>
>設定可能な製品は、カタログに独自の価格を持ちません。 設定可能な製品価格は、 [!UICONTROL In Stock] 子製品。

**メソッド 1:** すべての SKU に同じ価格を適用

1. すべてのバリエーションで価格が同じ場合は、「 **[!UICONTROL Apply single price to all SKUs]**.

1. 次を入力します。 **[!UICONTROL Price]**.

   ![SKU ごとに同じ価格](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**方法 2:** 各 SKU に異なる価格を適用

1. 製品のバリエーションごとに価格が異なる場合は、「 」を選択します。 **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. を選択します。 **[!UICONTROL Attribute]** それが価格差の基礎です。

1. 次を入力します。 **[!UICONTROL Price]** を設定します。

   この例では、XL サイズの方がコストが高くなります。

   ![SKU ごとの一意の価格](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

次のいずれかの方法を使用して、 **[!UICONTROL Quantity]**:

**メソッド 1:** すべての SKU に同じ数量を適用

数量がすべての SKU で同じ場合は、 **[!UICONTROL Apply single quantity to each SKU]** 数量を指定します。

_単一ソースのマーチャント_  — を入力します。 **[!UICONTROL Quantity]**.

_複数ソースのマーチャント： [Inventory management](../inventory-management/introduction.md)_  — ソースを割り当て、生成されたすべての製品バリアントに数量を追加します。

1. を選択します。 **[!UICONTROL Apply single quantity to each SKU]** オプション。

1. ソースを追加するには、 **[!UICONTROL Assign Sources]**.

1. 追加するソースを参照または検索します。 製品に追加するソースの横にあるチェックボックスを選択します。

1. ソースごとの手持在庫金額を入力します。

   ![すべての SKU の単一数量、ソースの割り当て](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**方法 2:** 属性別に異なる数量を適用

_単一ソースのマーチャント_  — を入力します。 **[!UICONTROL Quantity]**.

_複数ソースのマーチャント： [Inventory management](../inventory-management/introduction.md)_  — ソースを割り当て、生成されたすべての製品バリアントに数量を追加します。

1. 数量が SKU ごとに異なる場合は、 **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. 次を入力します。 **[!UICONTROL Quantity]** を設定します。

   ![属性ごとに異なる数量](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

画像、価格、数量の設定が完了したら、 **[!UICONTROL Next]** をクリックします。

### 手順 4：製品設定の生成

製品のリストが表示されるまでしばらく待ってから、次のいずれかの操作を行います。

- 設定が完了したら、「 **[!UICONTROL Generate Products]**.

- 修正を行うには、 **[!UICONTROL Back]**.

![製品バリエーションを生成する前に概要を確認する](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

現在の製品バリエーションが _設定_ 」セクションに入力します。

![現在の設定](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 手順 5：製品画像の追加

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Images and Videos]_」セクションに入力します。

1. 次をクリック： _カメラ_ 設定可能な製品に使用するメイン画像を並べて参照します。

詳しくは、 [画像とビデオ](product-images-and-video.md).

### 手順 6：製品情報の入力

下にスクロールし、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)

- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)

- [検索エンジンの最適化](product-search-engine-optimization.md)

- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)

- [Web サイト内の製品](settings-basic-websites.md)

- [デザイン](settings-advanced-design.md)

- [ギフトオプション](product-gift-options.md)

### 手順 7：製品の公開

1. カタログに商品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** から `Yes` 次のいずれかの操作を行います。

   - **メソッド 1:** 保存してプレビュー

      - 右上隅で、 **[!UICONTROL Save]**.

      - ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ) メニューを使用します。

     ストアが新しいブラウザータブで開きます。

     ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **方法 2:** 保存して閉じる

     次の日： _[!UICONTROL Save]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

### 手順 8：買い物かごのサムネールを設定

バリエーションごとに異なる画像がある場合、買い物かごのサムネールに正しい画像を使用するように設定できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Shopping Cart]_」セクションに入力します。

1. 設定 **[!UICONTROL Configurable Product Image]** から `Product Thumbnail Itself`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

   ![買い物かご — 設定可能な製品画像](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 在庫ステータスの設定

設定可能な製品在庫のステータスは、シンプルな製品の在庫ステータスとは異なります。シンプルな製品の在庫ステータスは、製品の可用性を直接表します。 設定可能な製品の場合、在庫ステータスは **_複数条件_** 在庫ステータスの計算です。

### 概要

在庫ステータス関係の主な原則は次のとおりです。

- を変更した場合、 **[!UICONTROL Stock Status]** 設定可能な製品の `Out of Stock` をクリックします。 **[!UICONTROL Save]**、 **_制御されない_** 子製品の在庫ステータス別。 常に次のように表示されます。 `Out of Stock` 管理者とストアフロントで。

- 次の場合、 **[!UICONTROL Stock Status]** 設定可能な製品の `In Stock` をクリックします。 **[!UICONTROL Save]**、 **_部分的に制御される_** 子製品の在庫ステータス別です。これは、管理者およびストアフロントに反映されます。

### 詳細な説明

The _在庫ステータス_ 設定可能な製品の一部は、その子製品の在庫ステータスによって、次の項目に従って制御されます **_複数条件_** 在庫ステータスの計算：

#### デフォルトのソース/在庫のみ：

- 設定可能な製品の在庫ステータスが **_手動_** に設定 `Out of Stock` 管理者ユーザー、ファイルのインポート、API の呼び出しによって、 `Out of Stock` 両方で **_管理者_** および **_ストアフロント_** それまで  **_手動_** 次に変更： `In stock` 管理者ユーザー、ファイルの読み込み、API 呼び出しによって実行されます。 子製品の在庫ステータスでは制御できません。

- 設定可能な製品の在庫ステータスが **_手動_** に設定 `In Stock` 管理者ユーザー、ファイルのインポート、API の呼び出しによって、在庫ステータスは次のようになります。 **_自動的に_** 両方の子製品の在庫状況によって管理される **_管理者_** および **_ストアフロント_**.

>[!NOTE]
>
>カスタム在庫およびソースは、 [Inventory management](../inventory-management/sources-stocks.md) 拡張機能を使用し、このツールは在庫とソースの管理にのみ使用することを強くお勧めします。 デフォルトのソース関数とストック関数は、 `CatalogInventory` モジュールで使用される必要があります。現在は非推奨です。

#### 少なくとも 1 つのカスタムソース/在庫がある場合：

- 設定可能な製品の在庫ステータスの値が **_手動_** に設定 `Out of Stock` 管理者ユーザー、ファイルのインポート、API の呼び出しによって、 `Out of Stock` 両方で **_管理者_** および **_ストアフロント_** それまで **_手動_** 次に変更： `In Stock` 管理者ユーザー、ファイルの読み込み、API 呼び出しによって実行されます。 It **_できません_** 子製品の在庫ステータスによって制御されます。

- 設定可能な製品の在庫ステータスの値が **_手動_** に設定 `In Stock` 管理者ユーザー、ファイルのインポート、API の呼び出しによって、在庫ステータスは次のようになります。 **_自動的に_** ～での子製品の在庫状況によって管理される **_ストアフロント_** のみ。

- 設定可能な製品の在庫ステータスの値が **_手動_** に設定 `In Stock` 管理者ユーザー、ファイルのインポート、API の呼び出しによって、 `In Stock` （内） **_管理者_** それまで **_手動_** 次に変更： `Out of Stock` 管理者ユーザー、ファイルの読み込み、API 呼び出しによって実行されます。 It **_できません_** 子製品の在庫ステータスによって制御されます。

## 覚えておくべきこと

- 設定可能な製品を使用すると、買い物客は、ドロップダウン、複数選択、ビジュアルスウォッチ、テキストスウォッチの入力タイプからオプションを選択できます。 各オプションは、個別のシンプルな製品です。

- [在庫ステータス](../inventory-management/sources-stocks.md) 設定可能な製品の場合は、半手動で制御された設定です。 シンプルな製品の在庫ステータスとは異なります。シンプルな製品の在庫ステータスは、製品の可用性を直接表します。 設定可能な製品の場合、在庫ステータスは複数条件の在庫ステータス計算の一部です。

- 構成可能な子製品は、シンプルな製品または仮想製品にすることができます。 **カスタムオプションなし**. カスタムの子製品を仮想化するには、 `Тhis item has no weight` （の） **[!UICONTROL Weight]** それぞれの設定に含まれています。

- 設定可能な製品は、カタログに独自の価格を持ちません。 設定可能な製品価格は、 [!UICONTROL In Stock] 子製品。

- 製品バリエーションに使用する属性は、グローバルスコープで、顧客は値を選択する必要があります。 設定可能な製品のテンプレートとして使用される属性セットに、製品バリエーション属性を含める必要があります。

- 設定可能な製品のテンプレートとして使用される属性セットには、各製品バリエーションに必要な値を含む属性を含める必要があります。

- 買い物かごのサムネール画像は、設定可能な製品レコードまたは製品バリエーションからの画像を表示するように設定できます。

- [スウォッチの属性](swatches.md#create-swatches-for-products) は、 **[!UICONTROL Update Product Preview Image]** オプション値 `No` （管理の属性編集ページ）をクリックします。

- テーマは、ユーザーが製品設定を切り替えたときのイメージギャラリーの動作を制御します。 のデフォルトの動作 _空白_ 主題は、選択した製品バリエーションで親の設定可能な製品画像を上書きすることです。 Luma テーマの場合、デフォルトの動作では、選択した製品のバリエーション画像が、親の設定可能な製品画像の前に追加されます。
