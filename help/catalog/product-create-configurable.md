---
title: 設定可能な製品
description: 選択用のバリエーションを買い物客に提供する、設定可能な製品の作成方法を説明します。
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# 設定可能な製品

設定可能な製品は、バリエーション（色やサイズなど）のドロップダウンオプションを持つ単一の製品として表示されます。 各バリエーションは、独自の SKU を持つ個別のシンプルな製品であり、カスタムオプションを持つシンプルな製品とは異なり、個々の在庫トラッキングが可能です。

**最適な対象：** 複数のオプション（色、サイズ、素材など）を持つ製品で、各バリエーションの在庫を追跡する必要があるもの。 初期セットアップには時間がかかりますが、拡張性は向上しています。

![&#x200B; 設定可能な製品 &#x200B;](./assets/product-configurable.png){width="700" zoomable="yes"}

## 始める前に

### 前提条件チェックリスト

設定可能な製品を作成する前に、以下が揃っていることを確認します。

1. **属性セット** - バリエーション属性（色やサイズなど）を含む属性セット
1. **作成されたバリエーション属性** – 以下の設定で設定された属性
1. **製品画像** - （オプションですが推奨）親製品と各バリエーションの画像

### 属性の要件

製品バリエーションに使用する各属性には、次の設定が必要です。

| プロパティ | 必須の設定 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`、`Visual Swatch` または `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

属性の作成手順については、[&#x200B; 製品属性 &#x200B;](product-attributes.md) を参照してください。

## フェーズ 1：製品基盤の作成

### 手順 1：製品タイプの選択

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 右上隅の _[!UICONTROL Add Product]_（メニュー矢印 ![&#x200B; メニューで &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"} 「**[!UICONTROL Configurable Product]**」を選択します。

   ![&#x200B; 設定可能な製品を追加 &#x200B;](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

[&#x200B; 属性セット &#x200B;](attribute-sets.md) は、製品フォームに表示されるフィールドと、バリエーションに使用できる属性を決定します。

1. ページの上部にある属性セットフィールドをクリックして、次のいずれかの操作を行います。

   - **[!UICONTROL Search]**：属性セットの名前を入力します。
   - リストで、使用する属性セットを選択します。

   フォームが更新され、選択した属性セットが反映されます。

1. 属性セットに別の属性を追加する必要がある場合は、「**[!UICONTROL Add Attribute]**」をクリックし、[&#x200B; 属性の追加 &#x200B;](product-attributes-add.md) の手順に従います。

   ![&#x200B; テンプレートを選択 &#x200B;](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 手順 3：基本情報の入力

1. 製品 **[!UICONTROL Product Name]** を入力します。

1. 製品名に基づいてデフォルト **[!UICONTROL SKU]** を受け入れるか、別の値を入力します。

1. 製品 **[!UICONTROL Price]** を入力します。

   >[!NOTE]
   >
   >この価格は、子供製品の価格によって上書きされます。 顧客に表示される実際の価格は、[!UICONTROL In Stock] の子製品から取得されます。

1. 製品はまだ公開する準備ができていないので、**[!UICONTROL Enable Product]** を `No` に設定します。

1. 「**[!UICONTROL Save]**」をクリックして続行します。

   商品を保存すると、左上隅に [&#x200B; ストア表示 &#x200B;](introduction.md#product-scope) 選択が表示されます。

1. 製品を使用できる **[!UICONTROL Store View]** を選択します。

   ![&#x200B; ストア表示の選択 &#x200B;](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 手順 4：基本設定の完了

1. **[!UICONTROL Tax Class]** を次のいずれかに設定します。

   - `None`
   - `Taxable Goods`

1. 空白のままに **[!UICONTROL Quantity]** ます。 数量は、製品のバリエーションによって決定されます。

1. **[!UICONTROL Stock Status]** は設定のままにします。

   設定可能な商品の在庫ステータスは、関連するバリエーションによって決定されます。 商品は数量なしで保存されたため、**[!UICONTROL Stock Status]** は `Out of Stock` に設定されます。

   >[!NOTE]
   >
   >設定可能な商品の **在庫ステータス** は、**_半手動_** で制御される設定であり、一部は子商品の在庫ステータスに基づいています。 これは、**_多基準_** 在庫ステータスの計算の一部です。 詳しくは [&#x200B; 在庫ステータスの設定 &#x200B;](#configure-stock-status) を参照してください。

1. 製品 **[!UICONTROL Weight]** を入力します。

   >[!NOTE]
   >
   >設定可能な製品には、常に重み付けが必要です。 ドロップダウンから「**[!UICONTROL This item has no weight]**」を選択した場合は、製品を保存すると自動的に「**[!UICONTROL This item has weight]**」に変わります。

1. **[!UICONTROL Visibility]** のデフォルトの `Catalog, Search` 設定を受け入れます。

1. [&#x200B; 新製品 &#x200B;](../content-design/widget-new-products-list.md) のリストに製品を特集するには、「**[!UICONTROL Set Product as New]**」チェックボックスを選択します。

1. 製品にカテゴリを割り当てるには、**[!UICONTROL Select…]** のボックスをクリックし、次のいずれかの操作を行います。

   **既存のカテゴリを選択：**

   - 一致するものを見つけるために、ボックスに入力を開始します。

   - 割り当てる各カテゴリのチェックボックスを選択します。

   ![&#x200B; バンドル製品のカテゴリを 1 つ以上選択します &#x200B;](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **新しいカテゴリを作成：**

   - 「**[!UICONTROL New Category]**」をクリックします。

   - **[!UICONTROL Category Name]** を入力し、メニュー構造内の位置を決定する **[!UICONTROL Parent Category]** を選択します。

   - 「**[!UICONTROL Create Category]**」をクリックします。

1. **[!UICONTROL Country of Manufacture]** を選択します。

   属性セットによっては、追加の属性が表示される場合があります。 これらは、後で完了できます。

### 手順 5：保存して続行

この時間に作業内容を保存することをお勧めします。 右上隅の「**[!UICONTROL Save]**」をクリックします。 次のフェーズでは、各バリエーションの設定を設定します。

## フェーズ 2：製品バリエーションの追加

次の手順は、複数のバリエーションの設定を追加する方法を示しています。 ページ上部のプログレスバーには、プロセス内の現在の位置が表示されます。

**例：** 3 色 3 サイズのシャツの場合、一意の SKU を持つシンプルな製品を 9 つ作成します（組み合わせごとに 1 つ）。 デフォルトでは、各バリエーションの製品名と SKU は、属性値と親の製品名または SKU に基づいています。

### 手順 6: バリエーション属性の選択

1. 「_[!UICONTROL Configurations]_」セクションまでスクロールし、「**[!UICONTROL Create Configurations]**」をクリックします。

   ![&#x200B; 設定 &#x200B;](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. バリエーションとして含める各属性のチェックボックスをオンにします。

   この例では、`color` と `size` が選択されています。

   ![&#x200B; 属性を選択 &#x200B;](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   リストには、設定可能な製品で使用できる、属性セットのすべての属性が含まれています。

1. 属性を追加する必要がある場合は、「**[!UICONTROL Create New Attribute]**」をクリックし、次の手順を実行します。

   - 属性プロパティを入力します。

   - 「**[!UICONTROL Save Attribute]**」をクリックします。

   - 属性のチェックボックスを選択します。

1. 右上隅の「**[!UICONTROL Next]**」をクリックします。

### 手順 7：属性値の選択

1. 属性ごとに、製品に適用する値のチェックボックスをオンにします。

   ![&#x200B; 属性値 &#x200B;](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 属性を並べ替えるには、_並べ替え_ （![&#x200B; 並べ替え順序アイコン &#x200B;](../assets/icon-sort-order.png)） アイコンを選択して、セクションを新しい位置に移動します。

   この順序によって、製品ページ上のドロップダウンリストの位置が決まります。

1. プログレスバーで、「**[!UICONTROL Next]**」をクリックします。

### 手順 8：画像、価格および在庫の設定

このステップでは、各設定の画像、価格、数量を決定します。 使用可能なオプションはそれぞれで同じです。 すべての SKU に同じ設定を適用することも、各 SKU に一意の設定を適用することも、今は設定をスキップすることもできます。

#### 画像の設定

適用される設定オプションを選択します。

**オプション 1：すべての SKU に単一の画像セットを適用**

1. 「**[!UICONTROL Apply single set of images to all SKUs]**」を選択します。

1. 商品ギャラリーに含める各画像を参照するか、画像をボックスにドラッグします。

![&#x200B; すべての SKU に同じ画像を使用 &#x200B;](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**オプション 2:SKU ごとに一意の画像を適用**

親製品画像は既にアップロードされているので、このオプションを使用して各バリエーションの画像をアップロードします。 ユーザーが特定のバリエーションを購入したときに買い物かごに表示される様々な画像を追加できます。

1. 「**[!UICONTROL Apply unique images by attribute to each SKU]**」を選択します。

1. 画像で示されている **[!UICONTROL Attribute]** （`color` など）を選択します。

1. 各属性値について、その設定に使用する画像を参照するか、ボックスにドラッグします。

   画像を値ボックスにドラッグすると、他の値のセクションにも表示されます。 画像を削除するには、_ごみ箱_ （![&#x200B; ごみ箱アイコン &#x200B;](../assets/icon-delete-trashcan-solid.png)） アイコンをクリックします。

   ![SKU ごとの一意の画像 &#x200B;](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### 価格の設定

>[!NOTE]
>
>設定可能な製品には、カタログ内に独自の価格はありません。 設定可能な製品価格は、その [!UICONTROL In Stock] の子製品から派生します。

適用される設定オプションを選択します。

**オプション 1：すべての SKU に同じ価格を適用**

1. 価格がすべてのバリエーションで同じ場合は、「**[!UICONTROL Apply single price to all SKUs]**」を選択します。

1. **[!UICONTROL Price]** を入力します。

   ![SKU あたりの同一価格 &#x200B;](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**オプション 2:SKU ごとに異なる価格を適用**

1. または一部のバリエーションで価格が異なる場合は、「**[!UICONTROL Apply unique prices by attribute to each SKU]**」を選択します。

1. 価格差の基礎となる **[!UICONTROL Attribute]** を選択します。

1. 各属性値の **[!UICONTROL Price]** を入力します。

   この例では、XL サイズの方がコストがかかります。

   ![SKU ごとのユニーク価格 &#x200B;](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### 在庫の設定

適用される設定オプションを選択します。

**オプション 1：すべての SKU に同じ数量を適用**

すべての SKU で数量が同じ場合は、「**[!UICONTROL Apply single quantity to each SKU]**」を選択して数量を指定します。

シングル Source マーチャント（_S） :_

**[!UICONTROL Quantity]** を入力します。

[Inventory managementを使用するマルチ Source マーチャント（_M） &#x200B;](../inventory-management/introduction.md):_

生成されたすべての製品バリアントのソースを割り当てて数量を追加します。

1. **[!UICONTROL Apply single quantity to each SKU]** オプションを選択します。

1. ソースを追加するには、「**[!UICONTROL Assign Sources]**」をクリックします。

1. 追加するソースを参照または検索します。 製品のソースの横にあるチェックボックスをオンにします。

1. ソースごとの手持在庫金額を入力します。

   ![&#x200B; すべての SKU に対して単一数量、ソースを割り当て &#x200B;](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**オプション 2：属性別に異なる数量を適用**

シングル Source マーチャント（_S） :_

各属性値の **[!UICONTROL Quantity]** を入力します。

[Inventory managementを使用するマルチ Source マーチャント（_M） &#x200B;](../inventory-management/introduction.md):_

生成されたすべての製品バリアントのソースを割り当てて数量を追加します。

1. 「**[!UICONTROL Apply unique quantity by attribute to each SKU]**」を選択します。

1. バリエーションごとに **[!UICONTROL Quantity]** を入力します。

   ![&#x200B; 属性ごとに異なる数量 &#x200B;](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

画像、価格、数量の設定が完了したら、右上隅の「**[!UICONTROL Next]**」をクリックします。

### 手順 9：製品設定の生成

製品のリストが表示されるまで待ち、次のいずれかの操作を行います。

- 設定に問題がなければ、「**[!UICONTROL Generate Products]**」をクリックします。

- 修正を行うには、「**[!UICONTROL Back]**」をクリックします。

![&#x200B; 製品バリエーションを生成する前に概要を確認 &#x200B;](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

現在の製品バリエーションは、「_設定_ セクションの下部に表示されます。

![&#x200B; 現在の設定 &#x200B;](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 手順 10：製品画像の追加

1. 下にスクロールして、「![」セクションの &#x200B;](../assets/icon-display-expand.png) 展開セレクター _[!UICONTROL Images and Videos]_&#x200B;を展開します。

1. _カメラ_ タイルをクリックし、設定可能な製品に使用するメイン画像を参照します。

詳しくは、[&#x200B; 画像とビデオ &#x200B;](product-images-and-video.md) を参照してください。

### 手順 11：製品情報の完了

下にスクロールして、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)

- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)

- [検索エンジンの最適化](product-search-engine-optimization.md)

- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)

- [Web サイトの製品](settings-basic-websites.md)

- [デザイン](settings-advanced-design.md)

- [ギフトオプション](product-gift-options.md)

## フェーズ 3：製品の公開

### 手順 12：製品を公開する

1. カタログに製品を公開する準備が整ったら、**[!UICONTROL Enable Product]** を `Yes` に設定します。

1. 次のいずれかの操作を行います。

   **方法 1：保存とプレビュー**

   - 右上隅の「**[!UICONTROL Save]**」をクリックします。

   - ストアで製品を表示するには、**[!UICONTROL Customer View]** 管理者 _（_ メニュー矢印 ![） メニューの &#x200B;](../assets/icon-menu-down-arrow-black.png) を選択します。

   ストアが新しいブラウザータブで開きます。

   ![&#x200B; 顧客ビュー &#x200B;](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **方法 2：保存して閉じる**

   _[!UICONTROL Save]_（メニュー矢印 ![&#x200B; メニューで &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"} 「**[!UICONTROL Save & Close]**」を選択します。

## 在庫ステータスの設定

設定可能な製品ストックステータスは、単純な製品ストックステータスとは異なります。 設定可能な製品の場合、在庫ステータスは **_複数条件_** 計算の一部です。

### 在庫ステータスの仕組み

在庫ステータス動作の主な原則：

| 状態をに設定しました | 結果 | 子製品で制御されているか？ |
|---|---|---|
| `Out of Stock` （手動） | 常に管理およびストアフロントに `Out of Stock` を表示 | いいえ – 手動で `In Stock` に変更するまで残ります |
| `In Stock` （手動） | ステータスは子製品に基づいて動的になります | 一部 – 以下の詳細を参照してください |

{style="table-layout:auto"}

### 「在庫」に設定した場合

設定可能な製品在庫ステータスを手動で `In Stock` に設定した場合、動作は在庫設定によって異なります。

**デフォルトのソース/在庫のみ：**

- **管理者およびストアフロント：** 在庫ステータスは、子製品の在庫状況を自動的に反映します

**1 つ以上のカスタムソース/在庫を使用：**

- **ストアフロント：** 在庫ステータスは、子製品の在庫状況を自動的に反映します
- **管理者：** 手動で変更するまで、`In Stock` として残ります（子製品で制御されません）

>[!NOTE]
>
>カスタムの在庫およびソースは、[Inventory management](../inventory-management/sources-stocks.md) 拡張機能の一部です。 このツールは、在庫とソースの管理にのみ使用することを強くお勧めします。 デフォルトの source 関数と stock 関数は、`CatalogInventory` モジュールの一部です。このモジュールは非推奨（廃止予定）になりました。

### 手動在庫ステータスの変更

（管理者ユーザーのアクション、ファイルの読み込み、API 呼び出しを使用して）在庫ステータスを手動で `Out of Stock` に設定した場合、手動で `Out of Stock` に変更し直すまで、管理 `In Stock` ストアフロントの両方に残ります。 子製品の在庫状況の影響を受けません。

## システム設定（オプション）

### バリエーション画像を買い物かごのサムネールで表示

バリエーションごとに異なる画像がある場合、買い物かごのサムネールに適した画像を表示するようにシステムを設定できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Checkout]**」を選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「_[!UICONTROL Shopping Cart]_」セクションを展開します。

1. **[!UICONTROL Configurable Product Image]** を `Product Thumbnail Itself` に設定します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

   ![&#x200B; 買い物かご – 設定可能な製品画像 &#x200B;](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 主な考慮事項

- **バリエーションタイプ：** 買い物客は、ドロップダウン、複数選択、ビジュアルスウォッチ、テキストスウォッチの入力タイプからオプションを選択できます。 各オプションは個別のシンプルな製品です。

- **在庫トラッキング：** カスタムオプションを備えた単純な製品とは異なり、設定可能な製品は、各バリエーションの在庫を個別に追跡します。

- **子製品のタイプ：** 子製品は、シンプル製品または仮想製品 **カスタムオプションなし** にすることができます。 子製品をバーチャルにするには、各子の `Тhis item has no weight` 設定に **[!UICONTROL Weight]** を選択します。

- **グローバルな割り当て：** 子製品は、すべての web サイト、ストア、ストアビューで、設定可能な製品から **グローバル** 同時に割り当ておよび割り当て解除されます。

- **価格：** 設定可能な製品には、カタログに独自の価格はありません。 表示価格は、[!UICONTROL In Stock] の子製品から来ています。

- **属性：** バリエーション属性にはグローバルスコープが必要で、顧客は値を選択する必要があります。 設定可能な製品に使用される属性セットに属性を含める必要があります。

- **買い物かごのサムネール：** 買い物かごのサムネールでは、設定可能な製品レコードまたは製品バリエーションのいずれかからの画像を表示できます。 上記の [&#x200B; システム設定 &#x200B;](#system-configuration-optional) を参照してください。

- **スウォッチの動作：** [&#x200B; スウォッチ属性 &#x200B;](swatches.md#create-swatches-for-products) は、属性編集ページで **[!UICONTROL Update Product Preview Image]** を `No` に設定することで、スウォッチが選択されたときに対応するシンプルな製品画像を表示しないように設定できます。

- **画像ギャラリーの動作：** このテーマは、ユーザーが製品設定を切り替えたときの画像ギャラリーの動作を制御します。 _空白_ テーマのデフォルト動作は、選択したバリエーションで親の設定可能な製品画像を上書きします。 Luma テーマの場合、デフォルトの動作では、選択したバリエーション画像を親の設定可能な商品画像の前に追加します。
