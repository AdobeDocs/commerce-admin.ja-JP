---
title: 検索語リダイレクトとストアフロントのルーティング
description: Adobe CommerceとEdge Delivery Servicesのデプロイメント別の検索語リダイレクト、URL書き換え、ライブ検索ルール、ストアフロントルーティングの選択方法について説明します。
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# 検索語のリダイレクトとストアフロントのルーティング

検索語のリダイレクト、URL リダイレクト、検索マーチャンダイジングは、さまざまな問題を解決します。 このガイドでは、[!DNL Edge Delivery Services]を利用した標準の[!DNL Adobe Commerce]検索、[!DNL Live Search]および[!DNL Commerce Storefront]に適した機能を選択します。

## リダイレクトタイプについて

これらの能力は、利用者の行動トリガーや閲覧状況に応じて異なります。

* **検索語リダイレクト**&#x200B;は、指定したページに特定の検索語を入力する買い物客を送信します。

* **URL リダイレクト**&#x200B;は、古いURLのリクエストを新しいURLに送信します。通常、HTTP 301または302の応答が返されます。 ブラウザーのアドレスバーが新しいURLに変更されます。

* **検索マーチャンダイジング**&#x200B;は、要求されたURLを変更することなく、検索結果に表示される商品またはその順序を変更します。

* **URL書き換え**&#x200B;は、サーバー上の1つのURLを別のURLにマッピングします。 [!DNL Adobe Commerce] URL書き換えツールは、古いURLの永続的なリダイレクト （301）を作成します。 詳しくは、[URLの書き換え](url-rewrite.md)を参照してください。

## ルーティング機能の選択

次のガイダンスを使用して、要件に一致する機能を特定します。

| 要件 | 推奨される機能 |
| --- | --- |
| 標準の[!DNL Adobe Commerce]検索から特定のクエリをページに送信する | [検索語句を管理](../catalog/search-terms.md)で検索語句を設定します（サポートされている場合）。 |
| 検索結果における商品のランキングや表示の変更 | [!DNL Live Search] [類義語](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms)または[&#x200B; マーチャンダイジングルール &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add)を使用します。 |
| 古い商品、カテゴリ、またはCMS URLをリダイレクト | デプロイメントに適用される場合は、Commerce [URL書き換え](url-rewrite.md) ツールを使用します。 |
| [!DNL Edge Delivery Services] パスをリダイレクト | ストアフロントまたはCDN ルーティングの使用。 |
| ストアフロントの移行後も従来のURLを保持する | レガシーから新しいURL リダイレクトマップを作成してテストします。 |

## Commerceの標準検索

標準カタログ検索を使用すると、コンテンツ ページ、カテゴリページ、製品ページ、またはデプロイメントがこの機能をサポートする外部ページを開くように検索語句を設定できます。 `gift cards`や`returns`などの買い物客が入力したクエリで、キャンペーンまたは情報ページを開く必要がある場合に使用します。

このタイプのリダイレクトを作成または更新するには、[検索語句の管理](../catalog/search-terms.md)を参照してください。 トリガーは既存のURLではなく買い物客のクエリであるため、検索語句の設定はURL書き換えツールとは別になっています。

>[!NOTE]
>
>ストアフロントが標準カタログ検索を使用し、ネイティブ検索語のリダイレクトをサポートしていることを確認します。 動作と使用可能な設定は、[!DNL Live Search]、[!DNL Adobe Commerce as a Cloud Service]、またはヘッドレスストアフロントによって異なる場合があります。

## URL リダイレクトと書き換え

ソースが買い物客が入力した検索語句ではなく既存のURLである場合は、URLの書き換えを使用します。 一般的な例としては、リダイレクトがあります。

* 新しい製品URLへの古い製品URL。

* 廃止されたカテゴリ URLから置換されたカテゴリ URLへ。

* 古いCMS ページ URLから新しいコンテンツページ URL。

URL書き換えツールをサポートするデプロイメントの場合は、**[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]**&#x200B;に移動してリダイレクトを作成します。 ステップバイステップのガイダンスについては、[URLの書き換え](url-rewrite.md)を参照してください。

>[!NOTE]
>
>[URL書き換え](url-rewrite.md) トピックは、PaaSにのみ適用されます。 [!DNL Adobe Commerce as a Cloud Service]または[!DNL Edge Delivery Services] ストアフロントの場合は、代わりにそのストアフロントのルーティングガイダンスを使用します。

## ライブサーチ

[!DNL Live Search]は、デフォルトのストアフロント検索エクスペリエンスに代わって、類義語、ファセット、マーチャンダイジングルールなどの機能を提供します。

検索の関連性、製品ランキング、製品の表示を変更する必要がある場合は、[!DNL Live Search]を使用します。 類義語を使用すると、異なる単語が類似した商品を返すようにできます。 商品をブーストしたり、埋め込んだり、ランクを変更したりする必要がある場合は、マーチャンダイジングルールを適用します。

[!DNL Live Search]検索ビヘイビアーは、すべてのCommerce検索キーワード設定のドロップインの代わりとして扱ってはなりません。 クエリがコンテンツまたはキャンペーンページに移動する必要がある場合は、リクエストを受信するストアフロントまたはエッジルーティング層にリダイレクトを実装します。 詳しくは、[[!DNL Live Search]  ドキュメント &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)を参照してください。

## Edge 配信サービス

[!DNL Edge Delivery Services]を利用したストアフロントの場合、ストアフロントまたはエッジルーティング層でリダイレクトを管理します。 [!DNL Adobe Commerce]管理者URLの書き換えがすべてのリクエストを制御すると仮定しないでください。

ドキュメントのオーサリングを使用する場合は、サイトのリダイレクト設定でリダイレクトマッピングを維持します。 リクエストがオリジンに到達する前に実行する必要があるリダイレクトの場合は、適切なCDNまたはエッジ設定を使用します。 関連するSEO ガイダンスについては、[Commerce StorefrontのSEO ガイドライン &#x200B;](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)を参照してください。

## Lumaからの移行

ストアフロント移行の一部としてリダイレクト移行を扱います。 カスタマージャーニーとSEOの意図を維持してから、ターゲットストアフロントのルーティングを再実装します。

トラフィックを新しいストアフロントに切り替える前に：

1. 既存のLuma URLと検索キーワードのランディングページを書き出してインベントリします。

1. 各項目を検索語リダイレクト、URL リダイレクト、マーチャンダイジングルールに分類します。

1. すべてのレガシーURLを新しいストアフロントパスにマッピングします。

1. リクエストを受け取るレイヤーに各リダイレクトを実装します。

1. ステータスコード、クエリパラメーター、正規URL、ロケールパス、リダイレクトループをテストします。

1. 未解決のレガシーURLについて、起動後のログと分析を監視します。

## リダイレクトのトラブルシューティング

リダイレクトが[!DNL Adobe Commerce]検索、ストアフロントのルーティング、ストアビューで期待どおりに動作しない場合は、次のチェックを使用します。

| イシュー | 確認すべきこと |
| --- | --- |
| 検索語がリダイレクトされない | ストアフロントで標準カタログ検索を使用し、検索クエリが設定された用語と一致し、検索用語が正しいストアビューに割り当てられていることを確認します。 [!DNL Live Search]が有効になっている場合は、リダイレクトがストアフロントまたはエッジ レイヤーに実装されていることを確認します。 |
| リダイレクトはLumaでは機能しますが、Edge Delivery Servicesでは機能しません | リダイレクトが[!DNL Edge Delivery Services] ストアフロントまたはCDN ルーティング層で設定されていることを確認します。[!DNL Adobe Commerce] 管理者URLの書き換えは、リクエストを受け取らない可能性があります。 |
| ライブサーチは、リダイレクトではなく結果を返します | 商品のランキングと表示に[!DNL Live Search] ルールを使用します。 コンテンツページまたはキャンペーンページに移動するには、ストアフロントまたはエッジレイヤーでリダイレクトを設定します。 |
| リダイレクトは、あるストアビューでは機能しますが、別のストアビューでは機能しません | 検索語句またはURL ルールに割り当てられたストアビューを確認します。 影響を受ける各ストアビューで、完全なロケールパスとクエリをテストします。 |

## このトピックの詳細ヘルプ

* [SEOの概要とベストプラクティス](seo-overview.md)

* [ストアフロントとは？](../getting-started/storefront.md)

* [検索語を管理](../catalog/search-terms.md)

* [URLの書き換え](url-rewrite.md)
