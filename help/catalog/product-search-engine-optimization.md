---
title: 製品設定 – [!UICONTROL Search Engine Optimization]
description: 製品の場合、[!UICONTROL Search Engine Optimization] 設定では、検索エンジンが製品のインデックス作成に使用する URL キーとメタデータを設定します。
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Search Engine Optimization]

_検索エンジン最適化_ （SEO）は、サイトのコンテンツと表示を微調整して、検索エンジンによるページのインデックス作成方法を改善する手法です。

製品の _[!UICONTROL Search Engine Optimization]_&#x200B;設定では、検索エンジンが製品のインデックスを作成するために使用する [URL キー ](catalog-urls.md) および [ メタデータ ](../merchandising-promotions/meta-data.md) フィールドを指定します。 メタキーワードを無視する検索エンジンもありますが、メタキーワードを使用し続ける検索エンジンもあります。 現在の [SEO のベストプラクティス ](../merchandising-promotions/seo-overview.md) は、価値の高いキーワードをメタタイトルとメタ説明の両方に組み込むことです。

各メタデータフィールドのデフォルト値は、設定で指定された値に基づいて自動生成できます。 各フィールドには、実際の値に置き換えられるプレースホルダーが含まれます。 詳しくは、[ 製品フィールドの自動生成 ](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation) を参照してください。

## SEO フィールドに入力します

1. 製品を編集モードで開きます。

1. 下にスクロールして、「_[!UICONTROL Search Engine Optimization]_」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

![ 検索エンジンの最適化 ](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. **[!UICONTROL URL Key]** を入力します（オプション）。

   デフォルトの URL キーは製品名に基づいています。 デフォルト値を使用することも、必要に応じて変更することもできます。 詳しくは、「[ カタログ URL](catalog-urls.md)」を参照してください。

1. **[!UICONTROL Meta Title]** を入力します（オプション）。

   メタタイトルとは、ブラウザーウィンドウの上部に表示されるテキストのことです。 デフォルトの製品名に基づくを使用することも、必要に応じて変更することもできます。

1. **[!UICONTROL Meta Keywords]** を追加します（オプション）。

   メタキーワードは、一部の検索エンジンで他の検索エンジンよりも多く使用されます。 価値の高いキーワードをいくつか入力すると、製品の可視性を高めることができます。

1. **[!UICONTROL Meta Description]** を入力します。

   メタ説明とは、検索結果のリストに表示されるテキストです。 最良の結果を得るには、説明を 150 ～ 160 文字の範囲で入力してください。

## フィールド参照

| フィールド | [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |------------------|
| [!UICONTROL URL Key] | ストア表示 | 商品のオンラインアドレスを決定します。 URL キーがストアのベース URL に追加され、ブラウザーのアドレスバーに表示されます。 Commerceは最初に、製品名に基づいた _検索エンジンに適した_ URL を作成します。 URL キーは、すべて小文字で、スペースではなく、これらの文字の間にハイフンを含める必要があります。 URL キーには `.html` などのサフィックスを含めないでください。サフィックスは設定内で管理されます。 |
| [!UICONTROL Meta Title] | ストア表示 | タイトルは、ブラウザーのタイトルバーとタブに表示され、検索エンジンの結果ページ（SERP）のタイトルとしても使用されます。 メタタイトルは、ページに固有で、長さが 70 文字未満である必要があります。 自動生成された値：`{{name}}` |
| [!UICONTROL Meta Keywords] | ストア表示 | 商品に関連するキーワード。 製品の検索に顧客が使用する可能性のあるキーワードの使用を検討します。 自動生成された値：`{{name}}` |
| [!UICONTROL Meta Description] | ストア表示 | メタ説明は、検索結果リスト用のページの簡単な概要を提供します。 理想的な長さは 150～160 文字で、最大 255 文字です。 ユーザーには表示されませんが、一部の検索エンジンでは、検索結果ページにメタ説明が含まれます。 自動生成された値：`{{name}} {{description}}` |

{style="table-layout:auto"}
