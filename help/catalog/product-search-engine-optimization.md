---
title: 製品設定 — [!UICONTROL Search Engine Optimization]
description: 製品の場合、 [!UICONTROL Search Engine Optimization] 設定検索エンジンで製品のインデックスを作成する際に使用する URL キーおよびメタデータを設定します。
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# 製品設定 — [!UICONTROL Search Engine Optimization]

_検索エンジンの最適化_ (SEO) は、検索エンジンによるページのインデックス作成方法を改善するために、サイトのコンテンツと表示を微調整する方法です。

The _[!UICONTROL Search Engine Optimization]_製品の設定で、 [URL キー](catalog-urls.md) および [メタデータ](../merchandising-promotions/meta-data.md) 検索エンジンで製品のインデックスを作成する際に使用されるフィールド。 一部の検索エンジンではメタキーワードが無視されますが、他の検索エンジンでは引き続きメタキーワードが使用されます。 現在の [SEO ベストプラクティス](../merchandising-promotions/seo-overview.md) は、メタタイトルとメタ説明の両方に高価値のキーワードを組み込むことを目的としています。

各メタデータフィールドのデフォルト値は、設定で指定された値に基づいて自動生成できます。 各フィールドには、実際の値に置き換えられるプレースホルダーが含まれます。 詳しくは、 [製品フィールドの自動生成](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## SEO フィールドに入力します。

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Search Engine Optimization]_」セクションに入力します。

![検索エンジンの最適化](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. 次を入力します。 **[!UICONTROL URL Key]** （オプション）。

   デフォルトの URL キーは製品名に基づいています。 デフォルトのを使用するか、必要に応じて変更できます。 詳しくは、 [カタログ URL](catalog-urls.md).

1. 次を入力します。 **[!UICONTROL Meta Title]** （オプション）。

   メタタイトルとは、ブラウザーウィンドウの上部に表示されるテキストです。 製品名に基づくデフォルトを使用するか、必要に応じて変更できます。

1. 次を追加： **[!UICONTROL Meta Keywords]** （オプション）。

   メタキーワードは、一部の検索エンジンでは他の検索エンジンよりも使用されます。 製品の可視性を高めるのに役立つ、価値の高いキーワードをいくつか入力することをお勧めします。

1. 次を入力します。 **[!UICONTROL Meta Description]**.

   メタ説明とは、検索結果の一覧に表示されるテキストです。 最も良い結果を得るには、150 ～ 160 文字の説明を入力してください。

## フィールド参照

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |------------------|
| [!UICONTROL URL Key] | ストア表示 | 製品のオンラインアドレスを指定します。 URL キーは、ストアのベース URL に追加され、ブラウザーのアドレスバーに表示されます。 Commerce は最初に _検索エンジンに優しい_ 製品名に基づく URL。 URL キーは、すべて小文字にする必要があります。スペースの代わりに、これらの文字の間には末尾にハイフンを付けないでください。 次のようなサフィックスを含めない `.html` を設定で管理するので、URL キーに入力します。 |
| [!UICONTROL Meta Title] | ストア表示 | タイトルは、ブラウザーのタイトルバーとタブに表示され、検索エンジン結果ページ (SERP) のタイトルとしても使用されます。 メタタイトルは、ページに固有で、長さが 70 文字未満である必要があります。 自動生成値： `{{name}}` |
| [!UICONTROL Meta Keywords] | ストア表示 | 商品の関連キーワード。 顧客が商品を見つける際に使用する可能性のあるキーワードの使用を検討します。 自動生成値： `{{name}}` |
| [!UICONTROL Meta Description] | ストア表示 | メタ説明は、検索結果リスト用のページの概要を提供します。 理想的な長さは、150～160 文字で、最大 255 文字です。 お客様には表示されませんが、一部の検索エンジンでは、検索結果ページにメタ説明が含まれています。 自動生成値： `{{name}} {{description}}` |

{style="table-layout:auto"}
