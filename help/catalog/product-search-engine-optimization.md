---
title: 製品設定 – [!UICONTROL Search Engine Optimization]
description: 製品の場合、[!UICONTROL Search Engine Optimization]設定は、検索エンジンが製品のインデックス作成に使用するURL キーとメタデータを設定します。
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
TQID: https://experienceleague.adobe.com/ya6B95jMPXfOYW785xN7WrmbFOwtKXdcr7yXTDvOAcw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-git-commit: 5e73225b71682f6d2527dab772abe0301ce5f0c8
workflow-type: tm+mt
source-wordcount: 531
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Search Engine Optimization]

_検索エンジン最適化_ （SEO）は、検索エンジンによるページのインデックス作成方法を改善するために、サイトのコンテンツとプレゼンテーションを微調整する方法です。

製品の&#x200B;_[!UICONTROL Search Engine Optimization]_&#x200B;設定では、検索エンジンが製品のインデックス作成に使用する[URL キー](catalog-urls.md)および[&#x200B; メタデータ &#x200B;](../merchandising-promotions/meta-data.md) フィールドを指定します。 meta キーワードを無視する検索エンジンもありますが、他の検索エンジンでは引き続きmeta キーワードを使用しています。 現在の[SEOのベストプラクティス &#x200B;](../merchandising-promotions/seo-overview.md)は、メタタイトルとメタディスクリプションの両方に価値の高いキーワードを組み込むことです。

各メタデータフィールドのデフォルト値は、設定で指定された値に基づいて自動生成できます。 各フィールドには、実際の値に置き換えられるプレースホルダーが含まれています。 詳しくは、[製品フィールドの自動生成](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation)を参照してください。

>[!NOTE]
>
>カタログのエンリッチメントは、LLMとAIを活用した検索のために、製品名と説明を改善するのに役立ちます。 SEOのメタフィールドに置き換わるものではありません。 詳しくは、[&#x200B; カタログの強化](catalog-enrichment.md)を参照してください。

## SEO フィールドに入力します

1. 製品を編集モードで開きます。

1. 下にスクロールして、_[!UICONTROL Search Engine Optimization]_&#x200B;セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

![検索エンジン最適化](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. **[!UICONTROL URL Key]**&#x200B;を入力します（オプション）。

   デフォルトのURL キーは、製品名に基づいています。 デフォルトを使用することも、必要に応じて変更することもできます。 詳しくは、[&#x200B; カタログ URL](catalog-urls.md)を参照してください。

1. **[!UICONTROL Meta Title]**&#x200B;を入力します（オプション）。

   メタタイトルは、ブラウザーウィンドウの上部に表示されるテキストです。 製品名に基づくデフォルトを使用するか、必要に応じて変更できます。

1. **[!UICONTROL Meta Keywords]**&#x200B;を追加します（オプション）。

   meta キーワードは、一部の検索エンジンで他の検索エンジンよりも使用されています。 製品がより可視化しやすくなるように、いくつかの価値の高いキーワードを入力することをお勧めします。

1. **[!UICONTROL Meta Description]**&#x200B;を入力します。

   メタディスクリプションは、検索結果リストに表示されるテキストです。 最適な結果を得るには、150 ～ 160文字の説明を入力します。

## フィールドリファレンス

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |------------------|
| [!UICONTROL URL Key] | ストアビュー | 製品のオンラインアドレスを決定します。 URL キーは、ストアのベース URLに追加され、ブラウザーのアドレスバーに表示されます。 Commerceでは、最初に、製品名に基づく&#x200B;_検索エンジンに適した_ URLを作成します。 URL キーは、すべて小文字にする必要があります。スペースではなく、これらの文字間にハイフン以外のハイフンを使用します。 URL キーに`.html`などのサフィックスを含めないでください。これは、設定で管理されているためです。 |
| [!UICONTROL Meta Title] | ストアビュー | タイトルは、ブラウザーのタイトルバーとタブに表示され、検索エンジンの結果ページ（SERP）のタイトルとしても使用されます。 メタタイトルは、ページに固有で、70文字未満である必要があります。 自動生成された値：`{{name}}` |
| [!UICONTROL Meta Keywords] | ストアビュー | 製品に関連するキーワード。 顧客が商品を見つけるために使用する可能性のあるキーワードの使用を検討します。 自動生成された値：`{{name}}` |
| [!UICONTROL Meta Description] | ストアビュー | メタディスクリプションは、検索結果リストのページの概要を提供します。 理想的な長さは150～160文字で、最大255文字です。 顧客からは見えませんが、一部の検索エンジンでは、検索結果ページにメタディスクリプションが表示されています。 自動生成された値：`{{name}} {{description}}` |

{style="table-layout:auto"}
