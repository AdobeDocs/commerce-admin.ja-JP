---
title: Commerce マーチャンダイジングとプロモーションの概要
description: カスタマーエンゲージメントを目的としたプロモーションやオポチュニティを作成するための Commerce ツールについて説明します。
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 1%

---

# Commerce マーチャンダイジングとプロモーションの概要

プロモーションをターゲットにして、顧客エンゲージメントの機会を作成し、買い物客を購入者に変えます。 購入後のアクティビティをサポートし、再訪問者に特別割引を提供することで、顧客関係を管理します。 SEO イニシアチブをサポートするベストプラクティスとテクニックを学びます。

## マーチャンダイジング

_マーチャンダイジング_ は、フロアプラン開発や商品のプレゼンテーションなどのアートやサイエンスを表す、小売業界で使われる用語です。 次のことを思い浮かべるかもしれません [カテゴリベースのナビゲーション](../catalog/navigation-top.md) 店舗の間取り図として、また店舗内の商品一覧に適用できる条件として商品の動的提示として。 また、製品の売上を増やすプログラムを実装することもできます。

- [ビジュアルマーチャンダイザー](visual-merchandiser.md)  – 製品を配置し、カテゴリリストに表示する製品を決定する条件を適用できる一連の高度なツール。

- [ギフト レジストリ](gift-registries.md)  – 特別な機会にギフト登録を作成したり、友人や家族にギフト登録からギフトを購入してもらったりできるように、顧客に権限を付与します。

- [報酬とロイヤルティ](rewards-loyalty.md) - ポイントシステムを使用して、顧客エンゲージメントを促進し、顧客ロイヤルティを促進する独自のプログラムを実装します。 幅広い取引や顧客活動に対してポイントを付与し、ポイントの割り当て、残高、有効期限を制御できます。

- [個人の販売とイベント](events-private-sales.md)  – 既存の顧客ベースを使用して、バズや新しいリードを生み出したり、民間販売やその他のカタログイベントを通じて余剰在庫をオフロードしたりします。

>[!TIP]
>
>製品Recommendationsと、購入者に最適なエクスペリエンスを提供するために必要なインサイトと制御を製品テンプレートで提供する方法については、を参照してください。 [製品Recommendationsユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

## プロモーション

Adobe Commerceでは、プロモーション機能を使用して商品の関係を設定し、価格ルールを使用して、様々な条件に基づいて割引をトリガーします。 価格ルールを使用して、次のような顧客インセンティブを提供できます。

- 特定の製品を割引するためのクーポンを最高の顧客に送信します
- 一定金額を超える購入に対しては送料無料を提供する
- 特定の期間のプロモーションのスケジュール設定

ルールは、1 つまたはすべてが満たされた場合に製品に価格の変更を適用する条件（1 つ以上）のコレクションです。 各ルールには複数の条件を含めることができ、すべてのステートメントまたは任意のステートメント（すべてではなく 1 つ以上）が true または false の場合に適用されます。

### 条件

条件とは、ルールを適用する製品および状況のリストを絞り込むステートメントです。 条件の属性とオプションは、使用可能なルールのタイプによって異なります。 満たされると、アクションは、割引、BOGO （Buy-One-Get-One）およびその他のオプションなど、完了します。 ルールは、ビジネスニーズ、季節的な割引やプロモーション、年間の機会に合わせて、必要に応じてシンプルにも複雑にも設定できます。 例えば、買い物かごの小計が大きい場合に、年中送料無料で提供しながら、休日のためにいくつかのオプションを追加することができます。

>[!NOTE]
>
>特定の製品属性に基づいて条件を定義する場合は、 **[!UICONTROL Use for Promo Rule Conditions]** に設定する必要があります。 `Yes` のフィールド名に設定します [ストアフロント プロパティ](../catalog/attribute-product-create.md).


### 価格ルール

の場合 [カタログ価格ルール](price-rules-catalog.md)に基づいて条件を作成します [属性セット](../catalog/attribute-sets.md) カタログ内で、比較関数および選択した属性。 いくつかのステートメントを選択することで、文のような条件を作成できます。 例えば、カテゴリに基づいて子供向けの衣類と男女向けの衣類に割引を適用する 2 つの価格ルールを作成できます。

![図 – カタログ価格ルールの例](./assets/diagram-catalog-price-rules.png){width="500"}

[買い物かご価格ルール](price-rules-cart.md) 条件は、ストアの子である任意のカテゴリに基づくことができます [root](../catalog/category-root.md). 価格ルールは事前に設定され、必要な条件が満たされた場合は常に行動に春。 これらのルールでは、属性を使用します。これには、製品属性を使用して買い物かごで SKU を照合するなど、製品属性の組み合わせが含まれます。 また、これらのルールでは、製品選択数量条件、複雑なルールの条件の組み合わせ、小計などの買い物かご属性も使用できます。

![図 – カート価格ルールの例](./assets/diagram-cart-price-rules.png){width="500"}

## 通信と SEO

マスタリング [検索エンジン最適化（SEO）](seo-overview.md) 潜在的な買い手を引き込むのに不可欠である。 検索エンジンによるページのインデックス作成方法を改善するために、検索エンジンの最適化と、サイトのコンテンツおよび表示の微調整について説明します。

ストアを起動する前に完了する必要があるタスクの 1 つは、ストアから送信されるすべてのコミュニケーションに使用されるメールテンプレートを確認して、ブランドが反映されていることを確認することです。 しかし、ブランドや製品を既存の顧客に宣伝するその他のコミュニケーションを開発することで、これを一歩進める必要があります。 変数とマークアップタグを使用してコンテンツをパーソナライズできます。

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Sourceリリース 2.4.0 から 2.4.3 には、dotdigital Engagement Cloud との統合に使用される、dotdigital ベンダーが開発した拡張機能が含まれています。 2.4.4 リリース以降、このCommerce Marketplaceはコアリリースにバンドルされなくなり、拡張機能からインストールおよび更新する必要があります。 また、Marketplace では、拡張機能開発者が提供する最新のドキュメントにもアクセスできます。
><br><br>
>バンドルされた拡張機能を有効にして設定してある場合は、2.4.4 のアップグレードプロセスの一環として composer.json ファイルを更新し、今後、拡張機能の更新を管理する必要があります。 参照： [アップグレードモジュール](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) が含まれる _アップグレードガイド_ を参照してください。

- [ニュースレター](newsletters.md) - ニュースレターの作成、購読者のリストの管理、コンテンツの開発、ストアへのトラフィックの促進などを行います。

- [RSS フィード](social-rss.md#rss-feeds) - RSS フィードを使用して、商品情報をショッピング集計サイトに発行したり、ニュースレターに含めたりできます。 お客様は RSS フィードを購読して、新製品やプロモーションについて知ることができます。

- [ソーシャルネットワーク](social-rss.md#social-networks) - Marketplace 拡張機能をインストールするか、コンテンツページにプラグインを追加して、ストアをソーシャルネットワークと統合します。

## Google マーケティングツール

ストア設定は、コンテンツを最適化し、トラフィックを分析し、カタログをショッピングアグリゲータおよびマーケットプレイスに接続するのに役立つ、次のGoogle ツールと統合されています。

>[!NOTE]
>
>2.4.5 リリース以降、Google サービスの統合が更新されて、GTag API の使用がサポートされるようになりました。 GTag は、Web ページのGoogle機能と統合するための統合メカニズムであり、Google サービスを通じてコンテンツをトラッキングおよび管理するための最新の機能と機会をサポートしています。 詳しくは、 [Google Analytics開発者向けドキュメント](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Google Universal Analytics を使用すると、オフラインおよびモバイルアプリのインタラクションをサポートし、継続的な更新にアクセスできるので、トラッキング用にさらにカスタムのディメンションと指標を定義できます。

- [Google コンテンツ実験](google-content-experiments.md) -Google Analyticsコンテンツを使用して、製品、カテゴリまたはコンテンツページの A/B テストを設定します

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）Google タグマネージャーを使用して、マーケティングキャンペーンイベントに関連する多くのタグを管理します。

- [Google AdWords](google-adwords.md) - Google AdWords キャンペーンを作成し、ストアのコンバージョンを追跡します。
