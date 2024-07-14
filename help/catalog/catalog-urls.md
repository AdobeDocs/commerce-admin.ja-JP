---
title: カタログおよび製品 URL
description: カタログ製品の URL 形式タイプと設定方法について説明します。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# カタログおよび製品 URL

製品およびカテゴリに割り当てる URL は、検索エンジンでサイトのインデックスがどの程度適切に作成されるかを決定する際に大きな役割を果たします。 カタログの作成を開始する前に、使用可能なオプションを検討してください。 現在の URL 形式を表示するには、ストアフロントに移動し、カタログ内の製品に移動します。 URL の形式は、現在の設定と、ページの検索に使用する方法によって異なります。

## URL 形式

### 動的 URL

動的 URL は _その場で_ 作成され、製品 ID、並べ替え順、リクエストが行われたページの変数を含むクエリ文字列を含む場合があります。 顧客がストア内の製品を検索すると、結果の URL は次のようになります。

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 静的 URL

静的 URL は、特定のページの固定アドレスです。 静的 URL は、検索エンジンに適した形式、または製品やカテゴリを ID で参照する形式で表示できます。 これらの URL には、製品の検索に使用される単語が含まれており、web サーバーの書き換えを有効にする必要があります。 静的 URL を持つファイルは、製品ページとカテゴリページ、コンテンツページおよび [ テーマアセット ](../content-design/theme-assets.md) で一般的に使用されます。

- `http://mystore.com/antonia-racer-tank.html`

## URL コンポーネント

### URL キー

URL キーは、製品またはカテゴリを説明する静的 URL の一部です。 製品またはカテゴリを作成すると、名前に基づいて初期 URL キーが自動的に生成されます。 URL キーを変更するには、製品情報の [ 検索エンジンの最適化 ](product-search-engine-optimization.md) の節を参照してください。

>[!NOTE]
>
>デフォルトでは、アクセント付きの特殊文字は、URL キー内の通常のアクセント付きでないバージョンに自動的に置き換えられます。 例えば、`ñ` は自動的に `n` に置き換えられます。 この動作は、_[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_設定オプションを `No` に設定することで無効にできます。 [ カタログ URL の設定 ](#configure-catalog-urls) を参照してください。

URL キーは、単語を区切るために、これらの文字の間に末尾でないハイフンを含む小文字で構成する必要があります。 URL キーの先頭または末尾にはハイフンを使用できません。 適切にデザインされた「検索エンジンに適した」 URL キーには、検索エンジンによるインデックス作成方法を向上させるために、製品名とキーワードが含まれている場合があります。 URL キーは、URL キーが変更された場合に自動リダイレクトを作成するように設定できます。

>[!NOTE]
>
>ローカライズされた URL など、URL のカスタマイズを拡張する方法については、[URL の書き換え ](../merchandising-promotions/url-rewrite.md) を参照してください。

### HTML接尾辞

カタログは、カテゴリおよび製品 URL の一部としてサフィックスを含めるか除外するように設定できます。 サフィックスを使用または省略する理由は様々です。 サフィックスは有用な目的に役立たなくなり、サフィックスのないページは検索エンジンによって効果的にインデックス化されると考える人もいます。 ただし、会社が、サフィックスを必要とする URL の標準化された形式を持っている場合があります。

サフィックスはシステム設定によって制御されるので、カテゴリや製品の URL キーに直接入力しないでください。 （これにより、URL の末尾に 2 つのサフィックスが付きます）。 サフィックスを使用するかどうかに関係なく、一貫性を保ち、すべての製品ページとカテゴリページに同じ設定を使用します。 サフィックスを含む（または含まない） URL の例を次に示します。

#### HTMLサフィックスを含む URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### HTMLサフィックスのない URL

- `http://mystore.com/helena-hooded-fleece`

### カテゴリパス

URL を設定して、カテゴリパスを含めたり除外したりできます。 デフォルトでは、カテゴリパスは、すべてのカテゴリページと製品ページに含まれています。 次の例は、カテゴリパスを含む場合と含まない場合で同じ製品 URL を示しています。

#### カテゴリパスを含む URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### カテゴリパスのない URL

- `http://mystore.com/helena-hooded-fleece.html`

検索エンジンで同じコンテンツにつながる複数の URL のインデックスが作成されないようにするには、URL からカテゴリパスを除外します。 もう 1 つの方法は、正規のメタタグを使用して、インデックスを作成する URL と無視する URL を検索エンジンに通知することです。 デフォルトでは、Commerceは商品 URL にカテゴリパスを含めません。

## カタログ URL の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Search Engine Optimizations]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

   - **[!UICONTROL Product URL Suffix]** を `html` または `htm` に設定します。 サフィックスは自動的に適用されるので、ピリオドを付けずに入力します。

   - **[!UICONTROL Category URL Suffix]** を `html` または `htm` に設定します。 サフィックスは自動的に適用されるので、ピリオドを付けずに入力します。

   - **[!UICONTROL Use Categories Path for Product URLs]** を好みに合わせて設定します。

   ![ 検索エンジンの最適化 ](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、[ 設定リファレンス ](../configuration-reference/catalog/catalog.md#search-engine-optimization) の _検索エンジンの最適化_ を参照してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、システムメッセージの **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   ![ キャッシュの更新 ](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   これらのオプションについて詳しくは、[ キャッシュの更新 ](../systems/cache-management.md#refresh-specific-caches) を参照してください。

## カタログメディアの URL 形式の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、「**[!UICONTROL Web]**」を選択します。

1. **[!UICONTROL Url Options]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

![Web > 一般オプション ](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| フィールド | [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web サーバーの書き換えが有効な場合、この設定を有効にすると、現在のビューのストア コードが URL に挿入されます。 オプション：`Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | グローバル | （シングルストア設定の場合）サイトに壊れたリンクがある場合、「404 Page Not Found」というメッセージが表示されたページではなく、ベース URL にトラフィックがリダイレクトされます。 オプション：`No`/`Yes (302 Found)`/`Yes (301 Moved Permanently)`<br /><br />**_重要！_**マルチストア設定の場合は、ベース URL への自動リダイレクトを使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | 製品およびカテゴリに割り当てる URL フォーマットを定義します。 オプション：<br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**– 変換されたファイル名を一意のハッシュ値として定義します。<br />**[!UICONTROL Image optimization based on query parameters]** - クエリパラメーターに応じて ](../content-design/media-gallery-image-optimization.md) 画像の最適化 [ プロセスを定義します。 |

{style="table-layout:auto"}
