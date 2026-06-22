---
title: カタログ検索の設定
description: ストアのカタログ検索を設定する方法について説明します。
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
TQID: https://experienceleague.adobe.com/8--7GCHftJl4i1oLVSQqII9Odv-mOXOqrdIyyXmGwrE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 834
ht-degree: 0%

---

# カタログ検索の設定

カタログ検索設定には2つのバリエーションがあります。 最初の方法では、[&#x200B; ライブサーチ &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html)がインストールされたときに使用できる設定について説明します。 2つ目の方法は、[OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html){:target="_blank"}を使用したネイティブ Adobe Commerceの設定について説明します。

>[!NOTE]
>
>クラウドインフラストラクチャプロジェクトについては、「[_Commerce on Cloud Infrastructure Guide_](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/opensearch)」の追加手順を参照してください。

## 方法1: [!DNL Live Search]のAdobe Commerce

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Catalog Search]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![&#x200B; ライブサーチのカタログ検索](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、_設定リファレンス_&#x200B;の「[Adobe Commerce with Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search)」を参照してください。

1. 検索クエリテキストの長さと単語数を制限するには、**[!UICONTROL Minimal Query Length]**&#x200B;と&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;の値を設定します。

1. 高速な応答のためにキャッシュする一般的な検索結果の量を制限するには、**[!UICONTROL Number of top search results to cache]**&#x200B;の量を設定します。

   デフォルト値は`100`です。 `0`の値を入力すると、2回目の入力時にすべての検索語と結果がキャッシュされます。

1. 返される結果に使用できる最大行数を[&#x200B; ストアフロント ポップオーバー](https://experienceleague.adobe.com/docs/commerce/live-search/live-search-storefront/quick-tour.html)で変更するには、別の&#x200B;**[!UICONTROL Autocomplete Limit]**&#x200B;値を入力します。

   行数を制限すると、検索のパフォーマンスが向上し、返されるリストのサイズが小さくなります。 デフォルト値は`8`行です。

## 方法2:OpenSearchを使用したCommerce

>[!IMPORTANT]
>
>- 2023年8月の[!DNL Elasticsearch 7]のサポート終了のお知らせにより、すべてのAdobe Commerceのお客様はOpenSearch 2.x検索エンジンに移行することをお勧めします。 製品のアップグレード中に検索エンジンを移行する方法について詳しくは、_アップグレードガイド_&#x200B;の「[OpenSearchへの移行](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html)」を参照してください。
>- バージョン 2.4.4および2.4.3-p2では、「Elasticsearch」というラベルが付けられたすべてのフィールドがOpenSearchにも適用されます。 Elasticsearch 8.xのサポートがバージョン 2.4.6で導入されたときには、ElasticsearchとOpenSearchの設定を区別するために新しいラベルが作成されました。 ただし、両方の設定オプションは同じです。

### 手順1：一般的な検索オプションの設定

>[!NOTE]
>
>OpenSearchとElasticsearchでは、サフィックスによる検索を標準でサポートしていません。 例えば、キーワードにSKUの最後の部分のみが含まれている場合、SKUによる検索で期待される結果が返されない場合があります。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Catalog Search]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![検索エンジン設定](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   これらのオプションについて詳しくは、_設定リファレンス_&#x200B;の「[Adobe Commerce with native search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search)」を参照してください。

1. 検索クエリテキストの長さと単語数を制限するには、**[!UICONTROL Minimal Query Length]**&#x200B;と&#x200B;**[!UICONTROL Maximum Query Length]**&#x200B;の値を設定します。

   >[!IMPORTANT]
   >
   >この最小範囲と最大範囲に設定された値は、検索エンジン設定で設定された対応する範囲と互換性がある必要があります。 例えば、これらの値をCommerceの`2`と`300`に設定した場合、検索エンジンで対応する値を更新します。

1. 高速な応答のためにキャッシュする一般的な検索結果の量を制限するには、**[!UICONTROL Number of top search results to cache]**&#x200B;の量を設定します。

   デフォルト値は`100`です。 `0`の値を入力すると、2回目の入力時にすべての検索語と結果がキャッシュされます。

1. Product EAV インデクサーを有効または無効にする場合は、**[!UICONTROL Enable EAV Indexer]**&#x200B;を設定します。

   この機能により、インデックス作成の速度が向上し、サードパーティの拡張機能によるインデクサーの使用が制限されます。

1. 検索オートコンプリートで表示する検索結果の最大数を制限するには、**[!UICONTROL Autocomplete Limit]**&#x200B;の値を設定します。

   この量を制限すると、検索のパフォーマンスが向上し、表示されるリストサイズが小さくなります。 デフォルト値は`8`です。

### 手順2:OpenSearch接続の設定

>[!IMPORTANT]
>
>Commerceがインストールまたはアップグレードされたときに、**[!UICONTROL Search Engine]**、**[!UICONTROL OpenSearch Server Hostname]**、**[!UICONTROL OpenSearch Server Port]**、**[!UICONTROL OpenSearch Index Prefix]**、**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;および&#x200B;**[!UICONTROL OpenSearch Server Timeout]**&#x200B;のフィールドが設定されました。 これらの値は、OpenSearchをアップグレードまたは変更する場合にのみ変更する必要があります。

1. **[!UICONTROL Search Engine]**&#x200B;に対して、`OpenSearch`を選択します。

1. **[!UICONTROL OpenSearch Server Hostname]**&#x200B;の場合は、Commerceのインストール時に設定されたデフォルト値をそのまま使用します。

1. **[!UICONTROL OpenSearch Server Port]**&#x200B;の場合は、Commerceのインストール時に設定されたデフォルト値をそのまま使用します。

   この例では、デフォルト値は`9200`です。

1. **[!UICONTROL OpenSearch Index Prefix]**&#x200B;の場合は、Elasticsearch インデックスを識別するためのプレフィックスを入力します。

   デフォルト値は`magento2`です。

1. HTTP認証を使用してユーザー名とパスワードを求め、OpenSearch サーバーにアクセスするには、**[!UICONTROL Enable OpenSearch HTTP Auth]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL OpenSearch Server Timeout]**&#x200B;の場合、システムがタイムアウトするまでの秒数を入力します。

   デフォルト値は`15`です。

1. 設定を確認するには、**[!UICONTROL Test Connection]**&#x200B;をクリックします。

### 手順3：推奨事項と推奨事項の設定

>[!NOTE]
>
>検索候補とレコメンデーションは、サーバーのパフォーマンスに影響を与える可能性があります。

1. 推奨事項を提供するには、**[!UICONTROL Enable Search Recommendations]**&#x200B;を`Yes`に設定し、次の操作を行います。

   - **[!UICONTROL Search Recommendation Count]**&#x200B;に、オファーするレコメンデーションの数を入力します。

   - レコメンデーションごとに見つかった結果の数を表示するには、**[!UICONTROL Show Results Count for Each Recommendation]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Enable Search Suggestions]**&#x200B;を`Yes`に設定し、次の操作を行います。

   - **[!UICONTROL Search Suggestions Count]**&#x200B;に、提供する検索候補の数を入力します。

   - 各提案に対して見つかった結果の数を表示するには、**[!UICONTROL Show Results for Each Suggestion]**&#x200B;を`Yes`に設定します。

### 手順4：一致する最小条件の設定

検索結果が返しに一致する必要があるクエリの最小項目数を制御するには、**[!UICONTROL Minimum Terms to Match]**&#x200B;の値を指定します。 この値を指定することで、買い物客にとって最適な検索結果の関連性が保証されます。 使用可能な値のリストについては、OpenSearch ドキュメントの[minimum_should_match パラメーター](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)を参照してください。

完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

