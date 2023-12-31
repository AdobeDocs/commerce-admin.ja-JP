---
title: メタデータ
description: 検索エンジンによるコマースサイトのインデックス作成を改善するために、キーワードリッチメタデータを入力する方法について説明します。
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# メタデータ

ストアには、検索エンジンによるサイトのインデックス作成を改善するために、キーワードリッチメタデータを入力できる場所が読み込まれます。 ストアのセットアップ中に、後で完了する目的で、事前メタデータを入力する場合があります。 時間の経過と共に、メタデータを微調整して、顧客の購入パターンや好みをターゲットに設定できます。

![製品設定 — 検索エンジン最適化](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## メタタイトル

メタタイトルは、ブラウザーおよび検索結果リストのタイトルバーとタブに表示されます。 メタタイトルは、ページに固有で、長さが 70 文字未満である必要があります。

![ストアフロントの例 — メタタイトル](./assets/storefront-home-page-meta-title.png){width="600"}

## メタキーワード

メタキーワードを無視する検索エンジンもありますが、引き続き使用する検索エンジンもあります。 現在のベストプラクティスは、高価値のキーワードをメタタイトルとメタ説明に組み込むことです。

![Web ブラウザー検索 — メタキーワード](./assets/storefront-meta-description.png){width="500"}

## メタの説明

メタの説明は、検索結果リストのページの概要を示します。 メタ記述の長さは 150 ～ 160 文字にするのが理想的ですが、フィールドには最大 255 文字まで入力できます。

## リッチスニペット

リッチスニペットでは、検索結果リストやその他のアプリケーションに関する詳細情報を提供します。 デフォルトでは、 [schema.org][1] 標準がストアの製品テンプレートに追加されます。 その結果、検索エンジンに関する詳細が、 _リッチスニペット_ 製品リスト内。

## 標準メタタグ

一部の検索エンジンでは、同じコンテンツを指す複数の URL を持つ Web サイトに対して、罰則が課せられます。 正規メタタグは、複数の URL に同一または類似のコンテンツがある場合に、インデックスを作成するページを検索エンジンに指示します。 canonical meta タグを使用すると、サイトのランキングを改善し、ページビュー数を集計できます。 標準メタタグは、 `<head>` 商品またはカテゴリページのブロック。 優先 URL へのリンクが提供されるので、検索エンジンではより大きな重み付けが得られます。

### 例 1：カテゴリパスによって重複する URL が作成される

例えば、カタログが製品 URL にカテゴリパスを含むように設定されている場合、ストアは同じ製品ページを指す複数の URL を生成します。

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### 例 2：カテゴリページの完全な URL

カテゴリの正規メタタグが有効な場合、ストアのカテゴリページには、完全なカテゴリ URL の正規 URL が含まれます。

    http://mystore.com/gear/bags/

### 例 3：製品ページの完全な URL

製品の正規メタタグが有効な場合、製品ページには、製品 URL キーがグローバルに一意なので、domain-name/product-url-key への正規 URL が含まれます。

    http://mystore.com/driven-backpack.html

製品 URL にカテゴリパスも含めると、正規 URL は domain-name/product-url-key のままになります。 ただし、製品は、カテゴリを含む完全修飾 URL を使用してアクセスすることもできます。 例えば、製品 URL キーが `driven-backpack` およびは、歯車/バッグカテゴリに割り当てられ、製品は、どちらかの URL を使用してアクセスできます。

URL からカテゴリを省略するか、標準メタタグを使用して製品やカテゴリでインデックスを作成するよう検索エンジンに指示することで、検索エンジンによって罰金が課されるのを防ぐことができます。 ベストプラクティスとして、カテゴリと製品の両方で標準メタタグを有効にすることをお勧めします。

### 正規メタタグの有効化

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **検索エンジンの最適化** 」セクションに入力します。

   フィールド値を変更するには、まず **システム値を使用** チェックボックスをオンにします。

   ![カタログ設定 — 検索エンジンの最適化](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. 完全なカテゴリパスを使用して、検索エンジンでカテゴリページのみのインデックスを作成する場合は、次の操作を行います。

   - 設定 **カテゴリに正規リンクメタタグを使用する** から `Yes`.

   - 設定 **製品に正規リンクメタタグを使用する** から `No`.

1. 検索エンジンで、domain-name/product-url-key 形式のみを使用して製品ページのインデックスを作成する場合は、次の手順を実行します。

   - 設定 **製品に正規リンクメタタグを使用する** から `Yes`.

   - 設定 **カテゴリに正規リンクメタタグを使用する** から `No`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## メタデータデモ

SEO メタデータの管理については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12)

[1]: https://schema.org/
