---
title: カテゴリの作成
description: 設定で設定されたメニューの最大深度に応じて、必要な数のサブカテゴリを追加できます。
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---

# カテゴリの作成

カタログのカテゴリ構造は、ルートが上に来た、逆さまになったツリーのようなものです。 ツリーの各セクションは、展開したり折りたたんだりできます。 無効なカテゴリや非表示のカテゴリはグレー表示されます。 第 1 レベルのカテゴリ（の下） [root](category-root.md)）は、通常、でオプションとして表示されます。 [メインメニュー](navigation-top.md). 設定で設定されたメニューの最大深度に応じて、必要な数のサブカテゴリを追加できます。 カテゴリは、ツリー内の他の場所にドラッグ アンド ドロップできます。 カテゴリ ID 番号は、ページ上部のカテゴリ名の後の括弧内に表示されます。

複数のプロパティを持つ web サイトの場合 [ストア](../stores-purchase/stores.md#add-stores)を使用すると、に使用されるカテゴリのセットを定義するルートカテゴリをストアごとに作成できます [上部ナビゲーション](navigation-top.md).

![カテゴリツリー](./assets/category-selected.png){width="700" zoomable="yes"}

## ベストプラクティス

カテゴリを計画および作成する際は、次のベストプラクティスを使用します。

### カテゴリ構造

メインメニューのカテゴリの構造は、顧客体験とパフォーマンスに影響を与える可能性があります。 ベストプラクティスとして、1 つの包括的な最上位カテゴリを識別し、同じ名前の他のカテゴリを含めないようにする必要があります。 例えば、「子供」に対して複数のカテゴリを、次のような異なる部門の下で整理するのではなく、 `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. 最上位の親カテゴリを作成する方が効率的な場合があります `Kids`次に、必要に応じて以下にサブカテゴリを作成します。 カテゴリ構造に一貫性を持ち、カタログ内のすべての製品タイプに同じアプローチを使用します。

### ビジネスルールと自動処理

ビジネスロジックを使用してカタログページに類似の項目を表示したり、パーソナライズされたプロモーション、自動プロセスまたは検索条件を設定する場合は、カテゴリ構造と使用可能な属性値を考慮します。 例えば、親カテゴリとして「polo」を指定した場合、性別が混在した商品や年齢に適していない商品が結果に含まれる可能性があります。 ただし、ポロシャツの特定のサブカテゴリに一致する場合、結果はより狭く、特定の顧客にアピールする可能性が高くなります。 特定の顧客をターゲットとする他の属性値と組み合わせると、結果をさらに具体的にすることができます。 特定のカテゴリパスを参照する際に、フィルタリングして取得する必要がある製品の数を考慮します。 結果の違いは劇的になる場合があります。 次のカテゴリパスから返される様々な結果を考えてみましょう。

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

次のようなカテゴリ関係を明確に定義することが重要です。

- 親カテゴリ
- サブカテゴリ
- カテゴリパス

また、次のような関連するキーワードおよび属性も定義します。

- 使用可否
- 販売価格
- ブランド
- サイズ
- 色

## 手順 1：カテゴリの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. を設定 **[!UICONTROL Store View]** 新しいカテゴリを使用できる場所を決定します。

1. カテゴリ ツリーで、新しいカテゴリの親カテゴリを選択します。

   親は、新しいカテゴリの 1 レベル上にあります。

   データを使用せずに最初から開始する場合、リストには次の 2 つのカテゴリしかない可能性があります。 _既定のカテゴリ_、はルートで、 _カテゴリの例_

1. クリック **[!UICONTROL Add Subcategory]**.

## 手順 2：基本情報を入力する

1. カテゴリをストアですぐに使用できるようにする場合は、を設定します **[!UICONTROL Enable Category]** 対象： `Yes`.

1. カテゴリをに含めるには [上部ナビゲーション](navigation-top.md)、設定 **[!UICONTROL Include in Menu]** 対象： `Yes`.

1. を入力 **[!UICONTROL Category Name]**.

   ![基本的なカテゴリ情報](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. click **[!UICONTROL Save]** そして続けて。

## 手順 3：カテゴリコンテンツの完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

   ![カテゴリコンテンツ](./assets/category-content.png){width="600" zoomable="yes"}

1. を表示するには **[!UICONTROL Category Image]** ページの上部で、独自の画像をアップロードするか、に存在する画像を使用することができます。 [メディアストレージ](../content-design/media-storage.md).

   - 独自の画像をアップロードするには、をクリックします **[!UICONTROL Upload]** カテゴリを表す画像を選択します。

   - メディア ストレージのイメージを使用するには、次のボタンをクリックします。 **[!UICONTROL Select from Gallery]** カテゴリを表す画像を選択します。

   >[!NOTE]
   >
   >Media Gallery 内では、 [Adobe Stockの統合](../content-design/adobe-stock.md) をクリックして適切なイメージを検索するには **[!UICONTROL Search Adobe Stock]**.

1. の場合 **[!UICONTROL Description]**&#x200B;を選択し、カテゴリランディングページに表示するテキストまたはその他のコンテンツを入力します。

   詳しくは、を参照してください [カテゴリコンテンツ](categories-content-settings.md).

1. カテゴリランディングページにコンテンツブロックを含めるには、 **[!UICONTROL CMS Block]** 表示する。

1. click **[!UICONTROL Save]** そして続けて。

## 手順 4：表示設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Display Setting]** セクション。

   ![ディスプレイ設定](./assets/category-display-settings.png){width="600" zoomable="yes"}

   これらのオプションの詳細については、を参照してください。これらのオプションの詳細については、  [ディスプレイ設定](categories-display-settings.md).

1. を設定 **[!UICONTROL Display Mode]** を次のいずれかに変更します。

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. カテゴリページに次を含める場合 _`Filter by Attribute`_セクション，階層的ナビゲーション，設定&#x200B;**[!UICONTROL Anchor]**対象： `Yes`.

1. の場合 **[!UICONTROL Available Product Listing Sort By]** オプションで、顧客がリストを並べ替えるために使用できる値を 1 つ以上選択します。 この設定は、 [!DNL Live Search] [製品一覧ページウィジェット](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   デフォルトでは、使用可能なすべての値が含まれます。 の選択を解除 **[!UICONTROL Use All]** チェックボックスをオンにして、選択項目を変更します。 例えば、次のような値が含まれます。

   - `Position`
   - `Product Name`
   - `Price`

1. カテゴリの既定の並べ替え順を設定するには、 **[!UICONTROL Default Product Listing Sort By]** の値。 この設定は、 [!DNL Live Search] [製品一覧ページウィジェット](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. 既定のレイヤ ナビゲーションを変更するには [価格ステップ](navigation-layered.md#configure-price-navigation) 設定を行い、次の手順を実行します。

   - の選択を解除 **[!UICONTROL Use Config Settings]** チェックボックス。

   - レイヤーナビゲーションの増分価格ステップとして使用する値を入力します。

1. クリック **[!UICONTROL Save]** そして続けて。

## 手順 5：検索エンジンの最適化設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Optimization Settings]** セクション。

   ![検索エンジンの最適化](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細については、を参照してください [検索エンジンの最適化](categories-search-engine-optimization.md).

1. 次の手順を実行します [メタデータ](../merchandising-promotions/meta-data.md) カテゴリの場合：

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. クリック **[!UICONTROL Save]** そして続けて。

## 手順 6：カテゴリ内の製品の選択

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Products in Category]** セクション。

   ![カテゴリ内の製品](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   これらのオプションの詳細については、を参照してください [カテゴリ内の製品](categories-product-assignments.md).

1. 必要に応じて、を使用します [フィルター](../getting-started/admin-grid-controls.md) 商品を検索します。

   カテゴリにまだ含まれていないすべてのレコードを表示するには、最初の列でレコード選択を次のように設定します `No` をクリックして、 **[!UICONTROL Search]**.

1. 最初の列で、カテゴリに含める各製品のチェックボックスを選択します。

1. クリック **[!UICONTROL Save]** そして続けて。

## 手順 7：カテゴリ権限の設定

{{ee-feature}}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Category Permissions]** セクション。

1. マルチサイトインストールの場合は、 **[!UICONTROL Website]** カテゴリ権限が適用される場所。

1. を選択します。 **[!UICONTROL Customer Group]** カテゴリ権限が適用される場所。

   ![Adobe Commerce B2B](../assets/b2b.svg) （[Adobe Commerce B2B](../b2b/introduction.md) のみ）必要に応じて、 **[!UICONTROL Shared Catalog]** その代わり。

1. 必要に応じて、次の権限を設定します。

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. 別の権限ルールを追加するには、次のボタンをクリックします： **[!UICONTROL New Permission]** そしてプロセスを繰り返します。

   ![カテゴリ権限](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## 手順 8：デザイン設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Design]** セクション。

1. 必要に応じてデザイン設定を指定します。

   - （[Adobe Commerce B2B](../b2b/introduction.md) のみ）このカテゴリに親カテゴリのデザイン設定を適用するには、 **[!UICONTROL Use Parent Category Settings]** 対象： `Yes`.

   - カテゴリページのデザインを変更するには、 **[!UICONTROL Theme]** お申し込みください。

   - カテゴリページの列のレイアウトを変更するには、 **[!UICONTROL Layout]** お申し込みください。

   - カスタムコードを入力するには、有効な XML コードを **[!UICONTROL Layout Update XML]** ボックス。

   - 製品ページに同じデザインを使用するには、次を設定します **[!UICONTROL Apply Design to Products]** 対象： `Yes`.

   ![デザイン設定](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) （Magento Open Sourceのみ）特定の期間に対して設計の更新をスケジュールするには、次の手順を実行します。

   - を展開します。 _[!UICONTROL Schedule Design Update]_セクション。

   - カレンダーの使用（![カレンダーアイコン](../assets/icon-calendar.png)）、スケジュールの更新を選択します **[!UICONTROL from]** および **[!UICONTROL to]** 日付。

   ![スケジュールされたデザインの更新](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.
