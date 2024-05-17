---
title: カタログ検索の設定
description: ストアのカタログ検索を設定する方法について説明します。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# カタログ検索の設定

カタログ検索設定には 2 つのバリエーションがあります。 最初のメソッドでは、次の場合に使用可能な設定について説明します [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) がインストールされました。 2 番目の方法は、を使用したネイティブ Adobe Commerceの設定を示しています [Elasticsearch][1]{:target=&quot;_blank&quot;}。

## 方法 1：を使用したAdobe Commerce [!DNL Live Search]

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Catalog Search]** セクション。

   ![Live Search のカタログ検索](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、を参照してください [Adobe Commerceと Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) が含まれる _設定リファレンス_.

1. 検索クエリテキストの長さと単語数を制限するには、の値を設定します **[!UICONTROL Minimal Query Length]** および **[!UICONTROL Maximum Query Length]**.

1. キャッシュする一般的な検索結果の量を制限して応答を高速化するには、次の量を設定します： **[!UICONTROL Number of top search results to cache]**.

   デフォルト値はです `100`. 値の入力 `0` 2 回目の入力時にすべての検索語句と検索結果をキャッシュします。

1. で、返される結果に使用できるラインの最大数を変更するには [店頭のポップオーバー](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html)、別のを入力 **[!UICONTROL Autocomplete Limit]** の値。

   行数を制限すると、検索のパフォーマンスが向上し、返されるリストのサイズが小さくなります。 デフォルト値はです `8` ライン。

## 方法 2:Elasticsearchを使用したCommerce

>[!IMPORTANT]
>
>により、 [!DNL Elasticsearch 7] 2023 年 8 月のサポート終了のお知らせです。Adobe Commerceをご利用のすべてのお客様に、OpenSearch 2.x 検索エンジンを利用することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法については、を参照してください。 [OpenSearch への移行](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) が含まれる _アップグレードガイド_.

### 手順 1：一般的な検索オプションを設定する

>[!NOTE]
>
>Elasticsearchでは、サフィックスによる検索は標準ではサポートされていません。 例えば、キーワードに SKU の最後の部分のみが含まれている場合、SKU で検索しても期待した結果が返されない場合があります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Catalog Search]** セクション。

   ![Elasticsearch設定](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   これらのオプションの詳細については、を参照してください [ElasticsearchのAdobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) が含まれる _設定リファレンス_.

1. 検索クエリテキストの長さと単語数を制限するには、の値を設定します **[!UICONTROL Minimal Query Length]** および **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >この最小範囲と最大範囲に設定された値は、Elasticsearch検索エンジンの設定で設定された対応する範囲と互換性がある必要があります。 例えば、これらの値をに設定した場合 `2` および `300` Commerceで、検索エンジンの対応する値を更新します。

1. キャッシュする一般的な検索結果の量を制限して応答を高速化するには、次の量を設定します： **[!UICONTROL Number of top search results to cache]**.

   デフォルト値はです `100`. 値の入力 `0` 2 回目の入力時にすべての検索語句と検索結果をキャッシュします。

1. 製品 EAV インデクサーを有効または無効にする場合は、 **[!UICONTROL Enable EAV Indexer]**.

   この機能により、インデックス化速度が向上し、サードパーティの拡張機能によるインデクサーの使用が制限されます。

1. 検索オートコンプリートで表示する検索結果の最大数を制限するには、次の数を設定します **[!UICONTROL Autocomplete Limit]**.

   この量を制限すると、検索のパフォーマンスが向上し、表示されるリストのサイズが小さくなります。 デフォルト値はです `8`.

### 手順 2:Elasticsearch接続の設定

>[!IMPORTANT]
>
>この **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**、および **[!UICONTROL Elasticsearch Server Timeout]** フィールドは、Commerceのインストールまたはアップグレード時に設定されました。 これらの値は、Elasticsearchのアップグレードまたは変更時にのみ変更してください。

1. の場合 **[!UICONTROL Search Engine]**、デフォルト値を使用します `Elasticsearch 7`.

   すべてのCommerce インストールにElasticsearch 7.6.x が必要です。

1. の場合 **[!UICONTROL Elasticsearch Server Hostname]**&#x200B;を使用する場合は、Commerceのインストール時に設定されたデフォルト値を使用します。

   この例では、デフォルト値はです。 `elasticsearch.internal`.

1. の場合 **[!UICONTROL Elasticsearch Server Port]**&#x200B;を使用する場合は、Commerceのインストール時に設定されたデフォルト値を使用します。

   この例では、デフォルト値はです。 `9200`.

1. の場合 **[!UICONTROL Elasticsearch Index Prefix]**&#x200B;を入力し、Elasticsearchインデックスを識別するプレフィックスを入力します。

   デフォルト値はです `magento2`.

1. HTTP 認証を使用してElasticsearch・サーバにアクセスするためのユーザー名とパスワードの入力を求めるには、 **[!UICONTROL Enable Elasticsearch HTTP Auth]** 対象： `Yes`.

1. の場合 **[!UICONTROL Elasticsearch Server Timeout]**：システムがタイムアウトするまでの秒数を入力します。

   デフォルト値はです `15`.

1. 設定を確認するには、 **[!UICONTROL Test Connection]**.

### 手順 3：提案と推奨事項を設定する

>[!NOTE]
>
>検索の提案や推奨事項は、サーバーのパフォーマンスに影響を与える可能性があります。

1. お勧めを提供するには、次を設定します **[!UICONTROL Enable Search Recommendations]** 対象： `Yes` 次の手順を実行します。

   - の場合 **[!UICONTROL Search Recommendation Count]**&#x200B;に、提供するお勧めの数を入力します。

   - レコメンデーションごとに見つかった結果の数を表示するには、次のように設定します **[!UICONTROL Show Results Count for Each Recommendation]** 対象： `Yes`.

1. を設定 **[!UICONTROL Enable Search Suggestions]** 対象： `Yes` 次の手順を実行します。

   - の場合 **[!UICONTROL Search Suggestions Count]**&#x200B;を入力し、提供する検索候補の数を入力します。

   - 各提案で見つかった結果の数を表示するには、次のように設定します **[!UICONTROL Show Results for Each Suggestion]** 対象： `Yes`.

### 手順 4：一致する最小用語を設定する

検索結果が返されるために一致する必要があるクエリの用語の最小数を制御するには、の値を指定します **[!UICONTROL Minimum Terms to Match]**. この値を指定すると、買い物客に最適な結果の関連性が保証されます。 使用可能な値のリストについては、を参照してください [minimum_should_match パラメーター](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) Elasticsearchドキュメント

完了したら、 **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
