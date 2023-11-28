---
title: カタログ検索の設定
description: ストアのカタログ検索を設定する方法を説明します。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# カタログ検索の設定

カタログ検索設定には、2 つのバリエーションがあります。 1 つ目の方法では、 [ライブ検索](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) がインストールされている。 2 つ目の方法では、 [Elasticsearch][1]{:target=&quot;_blank&quot;}。

## 方法 1:Adobe Commerceと [!DNL Live Search]

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Catalog Search]** 」セクションに入力します。

   ![ライブ検索のカタログ検索](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、 [Adobe Commerceとライブ検索](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) （内） _設定リファレンス_.

1. 検索クエリテキストの長さと単語数を制限するには、 **[!UICONTROL Minimal Query Length]** および **[!UICONTROL Maximum Query Length]**.

1. 最頻使用の検索結果の量を制限して応答を高速化するには、 **[!UICONTROL Number of top search results to cache]**.

   デフォルト値は `100`. 値の入力 `0` は、2 回目に入力したときにすべての検索用語と結果をキャッシュします。

1. 返される結果の最大行数を [～に対する店頭のポップアップ](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html)、別の **[!UICONTROL Autocomplete Limit]** の値です。

   行数を制限すると、検索のパフォーマンスが向上し、返されるリストのサイズが小さくなります。 デフォルト値は `8` 行。

## 方法 2:Elasticsearchを使用したコマース

>[!IMPORTANT]
>
>期限： [!DNL Elasticsearch 7] 2023 年 8 月のサポート終了のお知らせ。すべてのAdobe Commerceのお客様は、OpenSearch 2.x 検索エンジンに移行することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法については、 [OpenSearch への移行](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) （内） _アップグレードガイド_.

{{beta2-updates}}

### 手順 1：一般検索オプションの設定

>[!NOTE]
>
>Elasticsearchでは、サフィックスによる検索は標準でサポートされていません。 例えば、キーワードに SKU の最後の部分のみが含まれている場合、SKU で検索しても期待した結果が返されないことがあります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Catalog Search]** 」セクションに入力します。

   ![Elasticsearch設定](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   これらのオプションについて詳しくは、 [Adobe Commerce withElasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) （内） _設定リファレンス_.

1. 検索クエリテキストの長さと単語数を制限するには、 **[!UICONTROL Minimal Query Length]** および **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >この最小範囲と最大範囲に設定された値は、Elasticsearch検索エンジン構成で設定された対応する範囲と互換性がある必要があります。 例えば、次の値を `2` および `300` コマースで、検索エンジンの対応する値を更新します。

1. 最頻使用の検索結果の量を制限して応答を高速化するには、 **[!UICONTROL Number of top search results to cache]**.

   デフォルト値は `100`. 値の入力 `0` は、2 回目に入力したときにすべての検索用語と結果をキャッシュします。

1. 製品 EAV インデクサーを有効または無効にする場合は、 **[!UICONTROL Enable EAV Indexer]**.

   この機能により、インデクス作成速度が向上し、サードパーティの拡張機能によるインデクサーの使用が制限されます。

1. 検索のオートコンプリートで表示する検索結果の最大数を制限するには、以下の値を設定します。 **[!UICONTROL Autocomplete Limit]**.

   この数を制限すると、検索のパフォーマンスが向上し、表示されるリストのサイズが小さくなります。 デフォルト値は `8`.

### 手順 2:Elasticsearch接続の設定

>[!IMPORTANT]
>
>The **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**、および **[!UICONTROL Elasticsearch Server Timeout]** Commerce のインストール時またはアップグレード時にフィールドが設定されました。 これらの値は、Elasticsearchのアップグレードまたは変更時にのみ変更する必要があります。

1. の場合 **[!UICONTROL Search Engine]**、デフォルト値を受け入れる `Elasticsearch 7`.

   Elasticsearch7.6.x は、すべての Commerce インストールで必要です。

1. の場合 **[!UICONTROL Elasticsearch Server Hostname]** Commerce がインストールされた際に設定されたデフォルト値を受け入れます。

   この例では、デフォルト値は `elasticsearch.internal`.

1. の場合 **[!UICONTROL Elasticsearch Server Port]** Commerce がインストールされた際に設定されたデフォルト値を受け入れます。

   この例では、デフォルト値は `9200`.

1. の場合 **[!UICONTROL Elasticsearch Index Prefix]**&#x200B;を入力し、Elasticsearchインデックスを識別するプレフィックスを入力します。

   デフォルト値は `magento2`.

1. HTTP 認証を使用して、Elasticsearch・サーバにアクセスするためのユーザ名とパスワードを求めるには、 **[!UICONTROL Enable Elasticsearch HTTP Auth]** から `Yes`.

1. の場合 **[!UICONTROL Elasticsearch Server Timeout]**、システムがタイムアウトするまでの秒数を入力します。

   デフォルト値は `15`.

1. 設定を確認するには、 **[!UICONTROL Test Connection]**.

### 手順 3：提案とレコメンデーションの設定

>[!NOTE]
>
>検索候補や推奨事項は、サーバーのパフォーマンスに影響を与える可能性があります。

1. レコメンデーションを提供するには、 **[!UICONTROL Enable Search Recommendations]** から `Yes` 次の操作を実行します。

   - の場合 **[!UICONTROL Search Recommendation Count]**、オファーするレコメンデーションの数を入力します。

   - 各レコメンデーションで見つかった結果の数を表示するには、 **[!UICONTROL Show Results Count for Each Recommendation]** から `Yes`.

1. 設定 **[!UICONTROL Enable Search Suggestions]** から `Yes` 次の操作を実行します。

   - の場合 **[!UICONTROL Search Suggestions Count]**」に、オファーする検索候補の数を入力します。

   - 各提案で見つかった結果数を表示するには、 **[!UICONTROL Show Results for Each Suggestion]** から `Yes`.

### 手順 4：一致するキーワードの最小数を設定する

クエリから、検索結果で一致するキーワードの最小数を制御するには、 **[!UICONTROL Minimum Terms to Match]**. この値を指定すると、買い物客に最適な結果の関連性が確保されます。 使用可能な値のリストについては、 [minimum_should_match パラメーター](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) (Elasticsearchドキュメント )

完了したら、「 **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
