---
title: カタログと商品のURL
description: カタログ製品のURL形式の種類と設定方法について説明します。
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
TQID: https://experienceleague.adobe.com/Lf7Xh4w-rI-o-S1HEqM7nJZWuYGhOsB2ZccDg7Hb-3w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 918
ht-degree: 0%

---

# カタログと商品のURL

製品やカテゴリーに割り当てたURLは、検索エンジンによるサイトのインデックス作成を決定する上で、重要な役割を果たします。 カタログの制作を始める前に、利用可能なオプションを検討します。 現在のURL形式を表示するには、ストアフロントに移動し、カタログ内の任意の商品に移動します。 URLの形式は、ページの検索に使用する現在の設定設定とメソッドによって異なります。

## URL形式

### 動的URL

動的URLは&#x200B;_即座に_&#x200B;作成され、商品ID、並べ替え順序、リクエストが行われたページの変数を含むクエリ文字列を含める場合があります。 顧客が実店舗で商品を検索した場合、結果のURLは次のようになります。

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 静的URL

静的URLは、特定のページの固定アドレスです。 静的URLは、検索エンジンに適した形式、またはIDで商品やカテゴリーを参照する形式で表示できます。 これらのURLには、ユーザーが製品を検索するために使用する可能性のある単語が含まれており、web サーバーの書き換えを有効にする必要があります。 静的URLを持つファイルは、製品ページやカテゴリーページ、コンテンツページ、[&#x200B; テーマアセット &#x200B;](../content-design/theme-assets.md)で一般的に使用されます。

- `http://mystore.com/antonia-racer-tank.html`

## URL コンポーネント

### URL キー

URL キーは、製品またはカテゴリを説明する静的URLの一部です。 製品またはカテゴリを作成すると、名前に基づいて初期URL キーが自動的に生成されます。 URL キーを変更するには、製品情報の「[検索エンジン最適化](product-search-engine-optimization.md)」セクションを参照してください。

>[!NOTE]
>
>デフォルトでは、アクセント付きの特殊文字は、URL キーの通常のアクセントなしバージョンに自動的に置き換えられます。 例えば、`ñ`は自動的に`n`に置き換えられます。 この動作は、_[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;設定オプションを`No`に設定することで無効にできます。 [&#x200B; カタログ URLの設定](#configure-catalog-urls)を参照してください。

URL キーは、小文字で構成する必要があります。小文字のハイフン以外のハイフンは、これらの文字を区切る単語に使用します。 ハイフンは、URL キーの先頭または末尾では使用できません。 適切に設計された「検索エンジンに適した」 URL キーには、検索エンジンによるインデックス作成の方法を改善するために、製品名とキーワードが含まれる場合があります。 URL キーを設定して、URL キーが変更された場合に自動リダイレクトを作成できます。

>[!NOTE]
>
>ローカライズされたURLなど、URLのカスタマイズを拡張するには、[URL書き換え](../merchandising-promotions/url-rewrite.md)を参照してください。

### HTML接尾辞

カタログは、カテゴリと製品のURLの一部としてサフィックスを含めるか除外するように設定できます。 ユーザーが接尾辞を使用または省略することを選択する理由はさまざまです。 サフィックスはもはや有用な目的には役立たず、サフィックスのないページは検索エンジンによってより効果的に索引付けされていると考える人もいます。 ただし、接尾辞を必要とするURLの形式が標準化されている場合があります。

サフィックスはシステム設定によって制御されるので、カテゴリまたは製品のURL キーに直接入力しないでください。 （これにより、URLの末尾に二重接尾辞が付きます）。 接尾辞を使用するかどうかに関係なく、一貫性を持たせて、すべての製品ページとカテゴリーページに同じ設定を使用します。 接尾辞を含むURLと含まないURLの例を次に示します。

#### HTML接尾辞が付いたURL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### HTML サフィックスのないURL

- `http://mystore.com/helena-hooded-fleece`

### カテゴリーパス

製品URLを設定して、環境設定に基づいてカテゴリーパスを含めたり除外したりできます。 デフォルトでは、カテゴリーパスは製品URLに含まれません。 ただし、ネストされたカテゴリは、常にストアフロントのURLに完全なカテゴリーパスを表示し、カテゴリーナビゲーションの明確性と一貫性を確保します。 次の例は、カテゴリーパスを含む製品URLとない製品URLを示しています。

#### カテゴリーパスを含む製品URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### カテゴリーパスのない製品URL

- `http://mystore.com/helena-hooded-fleece.html`

検索エンジンが同じコンテンツにつながる複数のURLをインデックス作成できないようにするには、カテゴリーパスをURLから除外します。 また、標準的なメタタグを使用して、インデックスを作成するURLと無視するURLを検索エンジンに通知する方法もあります。 デフォルトでは、Commerceには商品URLにカテゴリーパスは含まれません。

## カタログ URLの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Search Engine Optimizations]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、オプションを設定します。

   - **[!UICONTROL Product URL Suffix]**&#x200B;を`html`または`htm`に設定します。 自動的に適用されるので、期間なしで接尾辞を入力します。

   - **[!UICONTROL Category URL Suffix]**&#x200B;を`html`または`htm`に設定します。 自動的に適用されるので、期間なしで接尾辞を入力します。

   - **[!UICONTROL Use Categories Path for Product URLs]**&#x200B;を好みに合わせて設定します。

   ![検索エンジン最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、_設定リファレンス_&#x200B;の[検索エンジン最適化](../configuration-reference/catalog/catalog.md#search-engine-optimization)を参照してください。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、システムメッセージの&#x200B;**[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

   ![&#x200B; キャッシュの更新](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   これらのオプションについて詳しくは、[&#x200B; キャッシュの更新](../systems/cache-management.md#refresh-specific-caches)を参照してください。

## カタログメディア URL形式の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL General]**&#x200B;を展開し、**[!UICONTROL Web]**&#x200B;を選択します。

1. **[!UICONTROL Url Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、オプションを設定します。

![Web >一般オプション &#x200B;](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web サーバーの書き換えが有効になっている場合、この設定を有効にすると、現在のビューのストアコードがURLに挿入されます。 オプション：`Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | グローバル | （シングルストア設定の場合）サイトに壊れたリンクがある場合、トラフィックは「404 Page Not Found」メッセージを含むページではなく、ベース URLにリダイレクトされます。 オプション：`No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_重要！_**&#x200B;マルチストア設定のベース URLに自動リダイレクトを使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | 製品とカテゴリに割り当てられたURL形式を定義します。 オプション：<br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**– 変換されたファイル名を一意のハッシュ値として定義します。<br />**[!UICONTROL Image optimization based on query parameters]** - クエリ パラメーターに応じて[画像最適化](../content-design/media-gallery-image-optimization.md) プロセスを定義します。 |

{style="table-layout:auto"}
