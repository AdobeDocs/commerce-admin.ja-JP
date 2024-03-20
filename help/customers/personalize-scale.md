---
title: 規模に応じたパーソナライゼーション
description: 買い物客向けにパーソナライズされたエクスペリエンスを作成できるAdobe Commerceの機能を説明します。
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# 規模に応じたパーソナライゼーション

規模に応じたパーソナライ&#x200B;ズ機能を使用すると、企業は、すぐに使用できるコンテキストと以前に確認された動作に基づいて、すべての顧客タッチポイントのショッピングエクスペリエンスをパーソナライズできます。 目標は、可能な限り関連性の高いパーソナライズされたエクスペリエンスを毎回提示することです。

パーソナライズされたショッピングエクスペリエンスを提供するメリットを理解するには、 [_大規模なパーソナライゼーションの概要_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) レポート。

パーソナライズされたショッピングエクスペリエンスを作成するには、顧客コンテキストを理解するために必要なデータのタイプを学ぶ必要があります。 ここから、そのデータを使用して、パーソナライズされたショッピングエクスペリエンスを作成するために必要な顧客インサイトを解放するAdobe Commerceの機能について学びます。

次の画像は、買い物体験のパーソナライズに関わる概念を示しています。

![パーソナライゼーションパイプラインの構築](assets/personalization-journey.png){width="700" zoomable="yes"}

この記事では、上記の各概念について詳しく説明します。

## 買い物体験をパーソナライズする方法

パーソナライゼーションが成功するには、顧客コンテキストから始まります。 この節では、顧客コンテキストの構築に役立つデータ型について学びます。

### ストアフロントデータ

ストアフロントデータ（行動データやブラウザーデータとも呼ばれます）は、買い物客がサイトとどのようにやり取りするかに関するインサイトを明らかにできます。 例：

- 買い物客が最も関心を持っているのは、どの製品やカテゴリですか？
- 私の買い物客が最も関心を寄せているのは、どのような検索クエリーですか？
- 買い物客が買い物かごに製品を追加して、その後放棄しているか。
- 買い物客がデスクトップまたはモバイルブラウザーを使用しているか。

次のストアフロントイベントでは、これらの質問に回答するのに役立つデータをキャプチャします。

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### バックオフィスデータ

バックオフィスデータ（サーバーサイドデータとも呼ばれます）は、注文のライフサイクルに関するインサイトを明らかにできます。 例：

- シーズンに応じて、より頻繁に購入される製品はありますか。
- 買い物客は製品を返していますか？
- 全期間顧客値を計算するにはどうすればよいですか？

次のバックオフィスイベントでは、これらの質問に回答するのに役立つデータをキャプチャします。

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### 顧客プロファイルとセグメントデータ

顧客プロファイルデータを使用すると、買い物客の人物と、どのセグメントに適合するかに関するインサイトを明らかにできます。 例：

- 名前
- 性別
- アドレス
- ロイヤリティステータス
- 電話番号
- メールアドレス
- ロイヤリティステータス
- 電話番号
- メールアドレス
- アップグレードの実施要件
- クロスチャネルの買い物客
- 新製品の見込み客
- ゴールド、シルバー、ブロンズのロイヤルティメンバー

次のプロファイルイベントは、次の質問への回答に役立つデータをキャプチャします。

- [プロファイルレコード](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

ストアフロント、バックオフィス、プロファイルのデータは、コマースの顧客と注文のコンテキストの基盤を形成し、顧客が閲覧している製品と最終的に購入している製品を知るのに役立ちます。 その後、顧客の興味をターゲットにし、顧客のエクスペリエンスをパーソナライズできます。 次の節では、買い物客と関わり合える、パーソナライズされたエクスペリエンスのタイプを学びます。

## パーソナライズされたエクスペリエンスのタイプ

コマースの顧客と注文のコンテキストデータは、次のタイプのパーソナライズされたエクスペリエンスを提供します。

| エクスペリエンス | 説明 |
|---|---|
| **製品の検出** | 次のマーチャンダイジングサービスが含まれます： [SaaS としてデプロイ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). これらの機能を使用すると、行動データ、製品属性および在庫レベルを使用して、検索結果、製品のレコメンデーションおよび閲覧ページにわたって製品の検出を自動的にパーソナライズできます。 これらの機能はすべてを使用しています [Adobe Sensei AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **サイトコンテンツ** | サイトを閲覧している現在の顧客に基づいてパーソナライズされた動的コンテンツブロックをデプロイする機能を指します。 |
| **オファーとキャンペーン** | セグメントデータに基づいてパーソナライズされたプロモーションコンテンツをデプロイできます。 |
| **測定** | データインテリジェンスを使用して、売上高、チャネルと商品のパフォーマンス、プロモーションなど、ビジネスをより深く理解できます。 |

次の 2 つの節では、このデータを使用して [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) および [ネイティブコマース機能](#using-commerce-data-in-native-commerce-features).

## Adobe Experience Platformでのコマースデータの使用

すべてのチャネルをまたいで買い物客にパーソナライズされたエクスペリエンスを作成するには、 [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 拡張子。

![データがExperience Platformエッジに送られる仕組み](assets/commerce-edge.png){width="700" zoomable="yes"}

上の画像では、ストアフロント、バックオフィス、顧客プロファイルのデータが、SDK、API、ソースコネクタを使用してExperience Platformエッジに送信されます。 拡張機能でデータ共有の複雑さが処理されるので、これらの要素の動作を完全に理解する必要はありません。 イベントデータが最前線にある場合は、そのデータを他のイベントアプリケーションに取り込むことができますExperience Platform。

次の表は、使用可能なExperience Platformアプリケーションの一部と、それらのアプリケーションがコマースデータをどのように使用するかを示しています。

| エクスペリエンス | アプリ | コマースデータの使用方法 |
|---|---|---|
| **サイトコンテンツ** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerceのデータは、Real-Time CDPが複数のソース (ERP、CRM、CMS、POS) のデータを単一のプロファイルに結合することで、統合された顧客プロファイルを燃料化します。 また、Real-Time CDPは、ルールベースのセグメントと AI ベースのセグメントの両方を作成し、マーケティングソリューションセット全体で使用できます。 また、Real-Time CDPのオーディエンスを使用して、コンテンツブロック、プロモーションおよび関連する製品ルールをパーソナライズすることもできます。 詳しくは、 [[!DNL Audience Activation]](../customers/audience-activation.md) を参照してくださ&#x200B;い。 |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerceデータは、Adobeでアクティブ化できます [!DNL Target] 動的なランディングページのテスト、最適化、作成に使用します。 送信されたコマースデータに基づいて、コンテンツがページに表示される順序（説明、仕様、レビュー、推奨製品など）をパーソナライズできます。 |
| **オファーとキャンペーン** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerceの行動およびバックオフィスデータは、電子メールキャンペーン、SMS、プッシュ通知など、パーソナライズされたオムニチャネルジャーニーのトリガーとして機能しま&#x200B;す。 |
| **測定** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) および [顧客 [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce はストアフロントとバックオフィスの両方のデータを顧客に送信します [!DNL Journey Analytics] ( また、Adobeに対するストアフロントデータのみ [!DNL Analytics]) を使用すると、売上高、商品、プロモーションなど、Adobe Commerceインテリジェンスの基本的な指標を超えた豊富な分析を実現できま&#x200B;す。 |

コマースデータをExperience Platformに送信する方法について詳しくは、 [データ接続](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## ネイティブの Commerce 機能での Commerce データの使用

次の節では、製品Recommendationsやライブ検索などのネイティブのコマース機能を使用して、パーソナライズされたショッピングエクスペリエンスを作成する方法を学びます。 また、 [!DNL Audience Activation]：前述のように、Real-Time CDPと呼ばれるExperience Platformで利用可能な製品のデータを使用します [以前](#using-commerce-data-in-adobe-experience-platform). Real-Time CDPは Commerce のネイティブではありませんが、その情報は [[!DNL Audience Activation]](../customers/audience-activation.md) 拡張子。

次の表は、コマースの顧客と注文のコンテキストデータを実用的なインサイトに変換するために使用できるコマース機能を示しています。

| エクスペリエンス | 機能 | 説明 |
|---|---|---|
| **製品の検出** | [ライブ検索](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | AI ランキングアルゴリズムを使用して、買い物客のオンサイト行動アクションに基づいて検索結果をパーソナライズおよび最適化し、検索の関連性とコンバージョンを高めます。 |
|  | [製品Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | 買い物客の行動、傾向、製品の類似性などに基づいて、AI 燃料の製品レコメンデーションを表示します。 製品レコメンデーションをAdobe Commerceカタログと組み合わせることで、非常に魅力的で関連性が高く、パーソナライズされたエクスペリエンスを提供します。 |
|  | [カテゴリマーチャンダイジング](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | カテゴリマーチャンダイジングはライブ検索管理からアクセスし、AI を使用して各カテゴリページで製品のシーケンスを自動的に再ランク付けし、各買い物客の関連性とコンバージョンを高めます。 AI を利用したルールを作成および管理して、買い物客のアクションと親和性に従って、カテゴリページの製品のシーケンスを自動的に再ランク付けできます。 |
| **サイトコンテンツ** | [ネイティブのコマース機能によって通知される動的ブロック](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | 価格ルールと顧客セグメントで設定されたロジックに基づいて、パーソナライズされたサイトコンテンツを配信できます。 |
|  | [Real-Time CDPオーディエンスから情報を得た動的ブロック](../customers/audience-activation.md) | Real-Time CDPで設定されたオーディエンスに基づいて、マーチャントがパーソナライズされたサイトコンテンツを配信できるようにします。 |
| **オファーとキャンペーン** | [買い物かごの価格ルール](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | 一連の条件に基づいて、買い物かご内の品目に割引を適用できます。 |
|  | [ネイティブのコマース機能によって通知される動的ブロック](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | コマースでネイティブに設定された顧客セグメントに基づいて、パーソナライズされたバナープロモーションを表示できます。 |
|  | [Real-Time CDPオーディエンスから情報を得た動的ブロック](../customers/audience-activation.md) | Real-Time CDPで設定されたオーディエンスに基づいてパーソナライズされたプロモーションを表示できます。 |
| **測定** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | ( 旧称：Magento Business Intelligence) は、データ主導型の意思決定をおこない、十分な情報に基づいた行動を取るのに役立つ、ベストプラクティスのインサイトを提供するクラウドプラットフォームです。 Adobe Commerce Intelligence では、データを分析し、注文の増加、顧客の行動、プロモーション戦略の効果に関する質問に答えるのに役立ちます。 |
