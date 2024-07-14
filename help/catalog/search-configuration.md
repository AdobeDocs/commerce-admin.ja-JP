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

カタログ検索設定には 2 つのバリエーションがあります。 最初の方法では、[Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) のインストール時に使用できる設定を説明します。 2 つ目の方法は、[Elasticsearch][1]{:target=&quot;_blank&quot;} を使用したネイティブ Adobe Commerceの設定を示しています。

## 方法 1:[!DNL Live Search] を使用したAdobe Commerce

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Catalog Search]**」セクションを展開します。

   ![Live Search のカタログ検索 ](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、_Configuration Reference_ の [Live Search のAdobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) を参照してください。

1. 検索クエリテキストの長さと単語数を制限するには、**[!UICONTROL Minimal Query Length]** と **[!UICONTROL Maximum Query Length]** の値を設定します。

1. よく使用される検索結果の量を制限して高速な応答をキャッシュするには、**[!UICONTROL Number of top search results to cache]** の量を設定します。

   デフォルト値は `100` です。 `0` の値を入力すると、2 回目の入力時にすべての検索語句と結果がキャッシュされます。

1. [ ストアフロントポップオーバー ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) で返される結果に使用できる最大行数を変更するには、別の **[!UICONTROL Autocomplete Limit]** 値を入力します。

   行数を制限すると、検索のパフォーマンスが向上し、返されるリストのサイズが小さくなります。 デフォルト値は `8` 行です。

## 方法 2:Elasticsearchを使用したCommerce

>[!IMPORTANT]
>
>2023 年 8 月のサポート終了のお知らせが [!DNL Elasticsearch 7] 件になったため、Adobe Commerceのお客様はすべて OpenSearch 2.x 検索エンジンに移行することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法については、[ アップグレード ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) の _OpenSearch への移行_ を参照してください。

### 手順 1：一般的な検索オプションを設定する

>[!NOTE]
>
>Elasticsearchでは、サフィックスによる検索は標準ではサポートされていません。 例えば、キーワードに SKU の最後の部分のみが含まれている場合、SKU で検索しても期待した結果が返されない場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Catalog Search]**」セクションを展開します。

   ![Elasticsearch設定 ](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   これらのオプションについて詳しくは、_Configuration Reference_ の [ElasticsearchのAdobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) を参照してください。

1. 検索クエリテキストの長さと単語数を制限するには、**[!UICONTROL Minimal Query Length]** と **[!UICONTROL Maximum Query Length]** の値を設定します。

   >[!IMPORTANT]
   >
   >この最小範囲と最大範囲に設定された値は、Elasticsearch検索エンジンの設定で設定された対応する範囲と互換性がある必要があります。 例えば、Commerceでこれらの値を `2` と `300` に設定した場合、検索エンジンの対応する値を更新します。

1. よく使用される検索結果の量を制限して高速な応答をキャッシュするには、**[!UICONTROL Number of top search results to cache]** の量を設定します。

   デフォルト値は `100` です。 `0` の値を入力すると、2 回目の入力時にすべての検索語句と結果がキャッシュされます。

1. 製品 EAV インデクサーを有効または無効にする場合は、**[!UICONTROL Enable EAV Indexer]** を設定します。

   この機能により、インデックス化速度が向上し、サードパーティの拡張機能によるインデクサーの使用が制限されます。

1. 検索オートコンプリートで表示する検索結果の最大数を制限するには、**[!UICONTROL Autocomplete Limit]** の値を設定します。

   この量を制限すると、検索のパフォーマンスが向上し、表示されるリストのサイズが小さくなります。 デフォルト値は `8` です。

### 手順 2:Elasticsearch接続の設定

>[!IMPORTANT]
>
>**[!UICONTROL Search Engine]**、**[!UICONTROL Elasticsearch Server Hostname]**、**[!UICONTROL Elasticsearch Server Port]**、**[!UICONTROL Elasticsearch Index Prefix]**、**[!UICONTROL Enable Elasticsearch HTTP Auth]**、**[!UICONTROL Elasticsearch Server Timeout]** の各フィールドは、Commerceのインストールまたはアップグレード時に設定されました。 これらの値は、Elasticsearchのアップグレードまたは変更時にのみ変更してください。

1. **[!UICONTROL Search Engine]** の場合、デフォルト値 `Elasticsearch 7` をそのまま使用します。

   すべてのCommerce インストールにElasticsearch 7.6.x が必要です。

1. **[!UICONTROL Elasticsearch Server Hostname]**:Commerceのインストール時に設定されたデフォルト値を使用します。

   この例では、デフォルト値は `elasticsearch.internal` です。

1. **[!UICONTROL Elasticsearch Server Port]**:Commerceのインストール時に設定されたデフォルト値を使用します。

   この例では、デフォルト値は `9200` です。

1. **[!UICONTROL Elasticsearch Index Prefix]**:Elasticsearchインデックスを識別するプレフィックスを入力します。

   デフォルト値は `magento2` です。

1. HTTP 認証を使用してElasticsearch・サーバにアクセスするためのユーザー名とパスワードの入力を求めるには、**[!UICONTROL Enable Elasticsearch HTTP Auth]** を `Yes` に設定します。

1. **[!UICONTROL Elasticsearch Server Timeout]**：システムがタイムアウトするまでの秒数を入力します。

   デフォルト値は `15` です。

1. 設定を確認するには、「**[!UICONTROL Test Connection]**」をクリックします。

### 手順 3：提案と推奨事項を設定する

>[!NOTE]
>
>検索の提案や推奨事項は、サーバーのパフォーマンスに影響を与える可能性があります。

1. お勧めを提供するには、**[!UICONTROL Enable Search Recommendations]** を `Yes` に設定して、次の手順を実行します。

   - **[!UICONTROL Search Recommendation Count]** しくは、提供するレコメンデーションの数を入力します。

   - 各レコメンデーションで見つかった結果の数を表示するには、**[!UICONTROL Show Results Count for Each Recommendation]** を `Yes` に設定します。

1. **[!UICONTROL Enable Search Suggestions]** を `Yes` に設定して、以下を実行します。

   - **[!UICONTROL Search Suggestions Count]**：提供する検索候補の数を入力します。

   - 各提案で見つかった結果の数を表示するには、**[!UICONTROL Show Results for Each Suggestion]** を `Yes` に設定します。

### 手順 4：一致する最小用語を設定する

検索結果が返されるために一致する必要があるクエリの用語の最小数を制御するには、**[!UICONTROL Minimum Terms to Match]** の値を指定します。 この値を指定すると、買い物客に最適な結果の関連性が保証されます。 使用可能な値のリストについては、Elasticsearchドキュメントの [minimum_should_match パラメーター ](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) を参照してください。

完了したら、「**[!UICONTROL Save Config]**」をクリックします。

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
