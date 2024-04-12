---
title: キャッシュ管理
description: サイトのパフォーマンスを簡単に向上させるキャッシュ管理ツールの使用方法を説明します。
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdf04be69754d0209772d9ceb244e3808f3b61d3
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---

# キャッシュ管理

Adobe CommerceとMagento Open Sourceキャッシュの管理システムを使用すると、サイトのパフォーマンスを簡単に向上させることができます。 キャッシュの更新が必要な場合は常に、通知がにリンクされて表示されます [!UICONTROL Cache Management] ページをクリックして更新を完了します。

![製品属性の保存 – キャッシュメッセージの更新](./assets/product-attribute-save-msg-update-cache.png){width="500"}

この _[!UICONTROL Cache Management]_各プライマリ・キャッシュのステータスと関連するタグが表示されます。 右上隅の大きなボタンを使用して、キャッシュまたは包括的なキャッシュストレージをフラッシュできます。 ページの下部にある追加のボタンを使用すると、カタログ製品画像のキャッシュと JavaScript/CSS キャッシュをフラッシュできます。

>[!IMPORTANT]
>
>カタログエンティティが変更されると、他のページに影響を与え、複数のキャッシュが同時に無効になる可能性があります。 キャッシュ管理ページを確認すると、無効な項目があり、次の場合に更新が必要であることがわかります _**直接編集されない**_. 例えば、この無効化は、任意のカテゴリに割り当てられているカタログ内の製品を編集した場合や、関連する製品ルールを変更した場合に発生します。

キャッシュをクリアした後は、常にブラウザーを更新して、最新のファイルが表示されるようにします。 コマースキャッシュをクリアしても、web ブラウザーのキャッシュはクリアされません。 更新されたコンテンツを表示するには、ブラウザーのキャッシュをクリアする必要がある場合があります。

Adobe Commerceのキャッシュに関するその他の技術情報については、を参照してください [キャッシュの概要](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} _Commerce フロントエンド開発ガイド_.

へのアクセス _[!UICONTROL Cache Management]_次のいずれかの操作を行ってページを作成します。

- 「」をクリックします **[!UICONTROL Cache Management]** ワークスペースの上にあるメッセージ内のリンク。
- 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![キャッシュ管理](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## キャッシュのベストプラクティス

Commerce では、インデックス再作成とキャッシュに異なる目的があります。 [インデックス](index-management.md) データベース情報を追跡して、検索パフォーマンスの向上、ストアフロントのデータ取得の迅速化などを実現します。 キャッシュは、読み込んだデータ、画像、形式などを保存して、ストアフロントへの読み込みとアクセスのパフォーマンスを向上させます。

- 拡張機能やモジュールをインストールした後は、必ずキャッシュをフラッシュしてください。 1 つ以上の拡張機能をインストールしてから、キャッシュをフラッシュできます。
- Commerce をインストールした後、キャッシュをフラッシュします。 新規インストールの場合は、のインデックスも再作成する必要があります。
- あるバージョンの Open Source または Commerce から別のバージョンにアップグレードした後で、キャッシュをフラッシュします。
- キャッシュをフラッシュする場合は、キャッシュのタイプと、ピーク時以外の時間にフラッシュをスケジュールすることを考慮してください。 例えば、深夜や早朝など、サイトを使用する顧客が少ない時間を選択します。 ピーク時の要求時にキャッシュ タイプをクリアすると、管理者の負荷が増え、操作が完了するまでサイトが停止する場合があります。
- 条件 [再インデックス](index-management.md)キャッシュをフラッシュする必要はありません。

## キャッシュ管理ロール リソース

キャッシュの表示、切り替え、フラッシュのオプションなど、特定のキャッシュメンテナンスアクションへのアクセスを役割ごとにユーザーに割り当てることができます。 Adobeでは、管理者レベルのユーザーに対してのみフラッシュアクションを有効にすることをお勧めします。 すべてのキャッシュ管理機能にアクセスできるようにすると、ストアフロントのパフォーマンスに影響を与える可能性があります。

![役割リソース – キャッシュ管理](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

管理者ユーザーアカウントに対するアクセスを許可するためのリソースの割り当てについては、を参照してください。 [役割リソース](permissions-user-roles.md#role-resources). 次のリソースは、キャッシュ管理ツールへのアクセスを制御します。

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## 特定のキャッシュの更新

1. 更新するキャッシュごとに、行の先頭にあるチェックボックスを選択します。

1. を設定 **[!UICONTROL Actions]** 対象： `Refresh` をクリックして、 **[!UICONTROL Submit]**.

## 一括アクション更新の実行

1. キャッシュのグループを選択するには、を設定します **[!UICONTROL Mass Actions]** を次のいずれかに変更します。

   - `Select All`
   - `Select Visible`

1. 更新する各キャッシュのチェックボックスを選択します。

1. を設定 **[!UICONTROL Actions]** 対象： `Refresh` をクリックして、 **[!UICONTROL Submit]**.

## 製品画像キャッシュをフラッシュします。

1. 次の下 _[!UICONTROL Additional Cache Management]_を選択し、**[!UICONTROL Flush Catalog Images Cache]**事前に生成された製品画像ファイルをクリアします。

   この `Image cache was cleaned` メッセージがワークスペースの上部に表示されます。

1. ブラウザーのキャッシュをクリアします。

## Javascript/CSS キャッシュをフラッシュします

1. 次の下 _[!UICONTROL Additional Cache Management]_をクリックし、1 つのファイルに結合された Javascript ファイルおよび CSS ファイルを消去します。**[!UICONTROL Flush JavaScript/CSS Cache]**.

   この `The JavaScript/CSS cache has been cleaned` メッセージがワークスペースの上部に表示されます。

1. ブラウザーのキャッシュをクリアします。

## コマンドラインを使用したフラッシュ

Commerce アプリケーション サーバへのアクセス権を持つシステム管理者および開発者は、Commerce CLI を使用してコマンド ラインからキャッシュとキャッシュの設定を管理することもできます。 参照： [キャッシュの管理](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target=&quot;_blank&quot;} _設定ガイド_.

## コントロール

| 制御 | 説明 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | 複数のキャッシュのチェックボックスを選択します。 オプション： <br/>**[!UICONTROL Select All]**– すべてのキャッシュのチェックボックスを選択します。<br/>**&#x200B;すべて選択解除&#x200B;**– すべてのキャッシュのチェックボックスをクリアします。<br/>**[!UICONTROL Select Visible]**  – すべての表示可能なキャッシュのチェックボックスを選択します。 <br/>**[!UICONTROL Unselect Visible]**– すべての表示可能なキャッシュのチェックボックスをクリアします。 |
| [!UICONTROL Actions] | 選択したすべてのキャッシュに適用されるアクションを決定します。 オプション： <br/>**[!UICONTROL Enable]**– 選択したすべてのキャッシュを有効にします。<br/>**[!UICONTROL Disable]**  – 選択したすべてのキャッシュを無効にします。 <br/>**[!UICONTROL Refresh]**– 選択したすべてのキャッシュを更新します。 |
| [!UICONTROL Submit] | 選択したすべてのキャッシュにアクションを適用します。 |

{style="table-layout:auto"}

### ボタン

| ボタン | 説明 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | デフォルトのコマースキャッシュのすべての項目を削除します（`var/cache`）に設定します（関連付けられたコマース タグに従います）。 |
| [!UICONTROL Flush Cache Storage] | Commerce タグに関係なく、キャッシュからすべての項目を削除します。 システムで別のキャッシュの場所を使用している場合、他のアプリケーションで使用されているキャッシュされたファイルは、そのプロセスで削除されます。 |
| [!UICONTROL Flush Catalog Images Cache] | に保存されている、サイズが自動的に変更された、透かし付きのカタログ画像をすべて削除します `media/catalog/product/cache`. 最近アップロードした画像がカタログに反映されない場合は、カタログをフラッシュし、ブラウザーを更新してみてください。 |
| [!UICONTROL Flush JavaScript/CSS Cache] | JavaScript ファイルと CSS ファイルの結合コピーをキャッシュから削除します。 スタイルシートまたは JavaScript に対する最近の変更がストアに反映されない場合は、JavaScript/CSS キャッシュをフラッシュし、ブラウザーを更新してみてください。 |
| [!UICONTROL Flush Static Files Cache] | 前処理されたビューファイルと静的ファイルを削除します。 |

{style="table-layout:auto"}

### キャッシュ

この [!UICONTROL Cache Management] ページには、管理者から管理できるキャッシュタイプと、現在のステータスが一覧表示されます。 ここでは、Adobe Commerceでサポートされるデフォルトのキャッシュタイプについて説明します。 この _キャッシュタグ_ および _キャッシュ ID_ 列は、Commerce アプリケーションコードで使用される値を記述します。

- `cache_type_id` キャッシュタイプの一意の ID を定義します。

- `%CACHE_TYPE_TAG%` キャッシュタイプスコーピングで使用される一意のタグを定義します。

開発者およびシステムインテグレーターは、これらの値を使用して、Adobe Commerceのカスタマイズや統合を行う際のキャッシュの設定や管理を行います。例えば、GraphQL API を使用して統合を開発する場合などです。 この `cache type id` は、Commerce CLI を使用してアプリケーションサーバーのコマンドラインからキャッシュを管理する場合にも使用されます。 例： ` bin/magento cache:status config` 構成キャッシュの現在のステータスが表示されます。

>[!NOTE]
>
>開発者およびシステムインテグレーターは、Commerce キャッシュ管理システムをカスタマイズおよび拡張して、カスタムモジュールと統合をサポートできます。 詳しくは、を参照してください [キャッシュの設定](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) が含まれる _Adobe Commerce設定ガイド_.

<!-- prettier-ignore -->

#### キャッシュリストの詳細

| キャッシュ | 説明 | キャッシュタグ | キャッシュ ID |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce は、すべてのモジュールから XML 設定を収集し、結合して、結合結果をキャッシュに保存します。<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>このキャッシュには、ファイルシステムとデータベースに保存されたストア固有の設定も含まれます。 構成ファイルを変更した後、このキャッシュの種類を消去またはフラッシュしてください。 | `CONFIG` | `config` |
| [!UICONTROL Layouts] | コンパイル済みのページレイアウト、つまり、すべてのコンポーネントのレイアウトコンポーネント。 レイアウト ファイルを変更した後で、このキャッシュの種類を消去またはフラッシュしてください。 | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | ブロックごとのHTMLページフラグメント。 ビューレイヤを変更した後で、このキャッシュ タイプをクリーンアップまたはフラッシュします。 | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | データベースクエリの結果を保存するコレクションデータファイル。 必要に応じて、Commerce はこのキャッシュを自動的にクリーンアップしますが、サードパーティの開発者は任意のデータをキャッシュの任意のセグメントに配置できます。 カスタム モジュールでロジックが使用され、その結果 Commerce でクリーンアップできないキャッシュ エントリが生成される場合は、このキャッシュ タイプをクリーンアップまたはフラッシュしてください。 | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | 通常は実行時に生成される API インターフェイスのリフレクションデータをクリアします。 | `REFLECTION` | `reflection` |
| `Database DDL operations` | データベーススキーマ。 必要に応じて、Commerce はこのキャッシュを自動的にクリーンアップしますが、サードパーティの開発者は任意のデータをキャッシュの任意のセグメントに配置できます。 データベーススキーマにカスタムの変更を加えた後、このキャッシュタイプをクリーンアップまたはフラッシュします。 （つまり、これらは Commerce 自体が行わない更新です。） データベーススキーマを自動的に更新する 1 つの方法は、magento 設定を使用することです:db-schema:アップグレード コマンド。 | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | コードのコンパイルの結果。 | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Webhook リクエストに対する応答をキャッシュします。 詳しくは、 [Webhook ガイド](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) （Commerce 開発者向けドキュメント）を参照してください。 | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | エンティティ属性値（EAV）属性に関連するメタデータのエンティティ・タイプ宣言をキャッシュします。 属性には、ストアラベル、関連する PHP コードへのリンク、属性レンダリング、検索設定などが含まれます。 通常、このキャッシュタイプをクリーンアップまたはフラッシュする必要はありません。 | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | ユーザーインターフェイスに表示される一時通知。 | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | 顧客、CMS ページ、CMS ブロック、製品メディアギャラリーエンティティのGraphQL クエリリゾルバーの結果をキャッシュします。 GraphQLのパフォーマンスを向上させるために、このキャッシュを有効のままにします。 | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | 統合設定ファイル。 統合を変更または追加した後で、このキャッシュをクリーンアップまたはフラッシュしてください。 | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | ストア統合用にコンパイル済みの統合 API 設定。 | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | カスタマイズを管理者にキャッシュします。 参照： [管理者による設定とテスト](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) が含まれる _管理 UI SDK ガイド_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | 完全なページキャッシュ。 | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | ターゲットルールインデックス | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Web API 構造をキャッシュしています。 | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | 翻訳ファイル。 | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## フルページキャッシュ

Adobe CommerceとMagento Open Sourceでは、カテゴリ、製品および CMS ページをすばやく表示するために、サーバー上でフルページキャッシュを使用します。 フルページキャッシュにより、応答時間が改善され、サーバーの負荷が軽減されます。 キャッシュを使用しない場合、各ページでコードブロックを実行し、データベースから情報を取得する必要が生じる可能性があります。 ただし、フルページキャッシュを有効にすると、完全に生成されたページをキャッシュから直接読み取ることができます。

>[!NOTE]
>
>次の操作をお勧めします [Varnish キャッシュ](https://varnish-cache.org/){:target=&quot;_blank&quot;} は、実稼動環境でのみ使用してください。

キャッシュされたコンテンツを使用して、類似したタイプの訪問からのリクエストを処理できます。 その結果、不用意な訪問者に表示されるページは、顧客に表示されるページとは異なる場合があります。 キャッシュの目的上、各訪問は次の 3 つのタイプのいずれかになります。

- `Non-sessioned` - セッションなしの訪問中、買い物客はページを表示しますが、ストアとのやり取りは行いません。 システムは、表示された各ページのコンテンツをキャッシュし、セッションに参加していない他の買い物客に提供します。
- `Sessioned` - セッション訪問中、ストアとやり取りする買い物客には、セッション ID が割り当てられます。 インタラクションには、製品の比較や買い物かごへの製品の追加などのアクティビティが含まれます。 セッション中に生成されたキャッシュ済みページは、セッション中にその買い物客のみが使用します。
- `Customer`  – 登録済みのアカウントを使用してログインして買い物をした顧客に対して、顧客セッションが作成されます。 セッションの間、お客様には、割り当てられた顧客グループに基づいて、特別なオファー、プロモーション、価格が提示されます。

技術情報については、を参照してください [ワニスの設定と使用](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} と [コマースページとデフォルトキャッシュに Redis を使用します](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} _設定ガイド_.

**_フルページキャッシュを設定するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Full Page Cache]** セクション。

   ![詳細設定 – フルページキャッシュ](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Caching Application]** を次のいずれかに変更します。

   - `Built-in Application`
   - `Varnish Caching`

1. ページキャッシュのタイムアウトを設定するには、 **[!UICONTROL TTL for public content]**. （デフォルト値は `86400`）

1. の最大数を指定するには [レイアウトハンドル](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) でを処理します [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) HTTP エンドポイントの場合、を入力します **[!UICONTROL Handles param size]**. サイズを制限すると、セキュリティとパフォーマンスが向上する可能性があります。 （デフォルト値は `100`）

1. ワニスを使用している場合は、次の手順を実行します **[!UICONTROL Varnish Configuration]** セクションを次のように設定します。

   - **[!UICONTROL Access list]**  – 設定ファイルを生成するために、Varnish 設定をパージできる IP アドレスを入力します。 複数のエントリはコンマで区切ります。 デフォルト値はです `localhost`.

   - **[!UICONTROL Backend host]**  – 設定ファイルを生成するバックエンドホストの IP アドレスを入力します。 デフォルト値はです `localhost`.

   - **[!UICONTROL Backend port]**  – 設定ファイルの生成に使用するバックエンドポートを特定します。 デフォルト値はです。 `8080`.

   - **[!UICONTROL Grace period]**  – 設定ファイルを生成するための猶予期間として使用する秒数を指定します。 参照： [高度なワニス設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) が含まれる _設定ガイド_.

   - 設定をとしてエクスポートするには `varnish.vcl` ファイルで、使用するワニスのバージョンのボタンをクリックします。

   ![事前設定 – 全ページのキャッシュワニス](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
