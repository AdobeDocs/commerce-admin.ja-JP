---
title: カタログと製品の URL
description: カタログ製品の URL 形式タイプと、それらの設定方法について説明します。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# カタログと製品の URL

製品やカテゴリに割り当てた URL は、検索エンジンによるサイトのインデックス付けの程度を決定する際に大きな役割を果たします。 カタログの作成を開始する前に、使用可能なオプションを考慮します。 現在の URL 形式を表示するには、ストアフロントに移動し、カタログ内の任意の製品に移動します。 URL の形式は、ページの検索に使用する現在の設定と方法によって異なります。

## URL 形式

### 動的 URL

動的 URL が作成されます _即座に_ には、製品 ID、並べ替え順、リクエストがおこなわれたページの変数を含むクエリ文字列を含めることができます。 顧客がストア内の製品を検索すると、結果の URL は次のようになります。

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 静的 URL

静的 URL は、特定のページの固定アドレスです。 静的 URL は、検索エンジンに適した形式で表示することも、ID で製品やカテゴリを参照する形式で表示することもできます。 これらの URL には、ユーザーが商品を探す際に使用する単語が含まれ、Web サーバーの書き換えを有効にする必要があります。 静的 URL を含むファイルは、製品ページ、カテゴリページ、コンテンツページ、 [テーマアセット](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL コンポーネント

### URL キー

URL キーは、製品またはカテゴリを説明する静的 URL の一部です。 製品またはカテゴリを作成すると、名前に基づいて最初の URL キーが自動的に生成されます。 URL キーを変更するには、 [検索エンジンの最適化](product-search-engine-optimization.md) 」セクションに表示されます。

>[!NOTE]
>
>デフォルトでは、アクセント記号付きの特殊文字は、URL キー内の通常のアクセント記号付きでないバージョンに自動的に置き換えられます。 例： `ñ` は自動的にに置き換えられます。 `n`. この動作は、 _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_設定オプション `No`. 詳しくは、 [カタログ URL の設定](#configure-catalog-urls).

URL キーは、単語を区切るために、末尾にハイフンを含まない小文字の文字で構成する必要があります。 ハイフンは、URL キーの先頭または末尾では使用できません。 適切に設計された「検索エンジン対応」URL キーには、検索エンジンによるインデックス付けを改善するために、製品名とキーワードが含まれる場合があります。 URL キーは、URL キーが変更された場合に自動リダイレクトを作成するように設定できます。

>[!NOTE]
>
>ローカライズされた URL など、URL のカスタマイズを拡張するには、 [URL の書き換え](../merchandising-promotions/url-rewrite.md) を参照してください。

### HTMLサフィックス

カタログは、カテゴリ URL と製品 URL の一部としてサフィックスを含めるか除外するように設定できます。 サフィックスの使用や省略を選択する理由は様々です。 一部のユーザーは、サフィックスが役に立つ目的を果たさなくなり、サフィックスのないページは検索エンジンによってより効果的にインデックス付けされると考えています。 ただし、サフィックスが必要な標準形式の URL を使用している場合があります。

サフィックスはシステム設定によって制御されるので、カテゴリまたは製品の URL キーに直接入力しないでください。 （この場合、URL の末尾に二重サフィックスが付きます）。 サフィックスを使用するかどうかは、一貫性を保ち、すべての製品ページとカテゴリページで同じ設定を使用します。 サフィックスの付いた（および付いていない）URL の例を以下に示します。

#### HTMLサフィックス付き URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL (HTMLサフィックスなし )

- `http://mystore.com/helena-hooded-fleece`

### カテゴリパス

カテゴリパスを含めるか除外するかを URL で設定できます。 デフォルトでは、カテゴリパスはすべてのカテゴリページと製品ページに含まれます。 次の例は、カテゴリパスのある（およびない）同じ製品 URL を示しています。

#### カテゴリパスを含む URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### カテゴリパスのない URL

- `http://mystore.com/helena-hooded-fleece.html`

検索エンジンが同じコンテンツにつながる複数の URL のインデックスを作成するのを防ぐには、その URL からカテゴリパスを除外します。 もう 1 つの方法は、正規メタタグを使用して、インデックスを作成する URL と無視する URL を検索エンジンに知らせることです。 デフォルトでは、Commerce は製品 URL にカテゴリパスを含めません。

## カタログ URL の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimizations]** 」セクションに移動して、次のオプションを設定します。

   - 設定 **[!UICONTROL Product URL Suffix]** から `html` または `htm`. サフィックスは自動的に適用されるので、ピリオドを含まないで入力します。

   - 設定 **[!UICONTROL Category URL Suffix]** から `html` または `htm`. サフィックスは自動的に適用されるので、ピリオドを含まないで入力します。

   - 設定 **[!UICONTROL Use Categories Path for Product URLs]** を選択します。

   ![検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、 [検索エンジンの最適化](../configuration-reference/catalog/catalog.md#search-engine-optimization) （内） _設定リファレンス_.

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   ![キャッシュを更新](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   これらのオプションについて詳しくは、 [キャッシュを更新](../systems/cache-management.md#refresh-specific-caches).

## カタログメディアの URL 形式を設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Url Options]** 」セクションに移動して、次のオプションを設定します。

![Web /一般オプション](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web サーバーの書き換えが有効な場合、この設定を有効にすると、現在のビューのストアコードが URL に挿入されます。 オプション： `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | グローバル | （シングルストアの設定の場合）サイトに壊れたリンクがある場合、これにより、「404 Page Not Found」というメッセージが表示されたページではなく、ベース URL にトラフィックがリダイレクトされます。 オプション： `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_重要！_**マルチストアの設定では、ベース URL への自動リダイレクトを使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | 製品とカテゴリに割り当てる URL 形式を定義します。 オプション： <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**— 変換されたファイル名を一意のハッシュ値として定義します。<br />**[!UICONTROL Image optimization based on query parameters]**  — 定義 [画像最適化](../content-design/media-gallery-image-optimization.md) プロセスを実行できます。 |

{style="table-layout:auto"}
