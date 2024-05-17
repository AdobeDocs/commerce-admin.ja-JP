---
title: 大規模なパーソナライゼーション
description: Adobe Commerceのどの機能を使用して、買い物客向けにパーソナライズされたエクスペリエンスを作成できるかを説明します。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5f40c98324c3033cdeb8a11e89a71497ced890b8
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# 大規模なパーソナライゼーション

&#x200B;大規模なパーソナライゼーションにより、企業は、直近のコンテキストと以前に観察された行動に基づいて、すべての顧客タッチポイントに対するショッピングエクスペリエンスをパーソナライズできます。 可能な限り関連性が高く、パーソナライズされたエクスペリエンスを毎回提示することが目標です。

パーソナライズされたショッピングエクスペリエンスを提供するメリットを理解するには、 [_大規模なパーソナライゼーションの概要_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) レポート。

パーソナライズされたショッピングエクスペリエンスを作成するには、顧客のコンテキストを理解するために必要なデータのタイプについて知る必要があります。 そこから、そのデータを使用して、パーソナライズされたショッピングエクスペリエンスを構築するために必要な顧客インサイトを解き放つAdobe Commerce機能について説明します。

次の画像は、ショッピングエクスペリエンスのパーソナライズに関する概念を示しています。

![パーソナライゼーションパイプラインの構築](assets/personalization-journey.png){width="700" zoomable="yes"}

この記事では、上記の各概念について詳しく説明します。

## ショッピング体験をパーソナライズする方法

パーソナライゼーションの成功は、顧客コンテキストから始まります。 この節では、顧客コンテキストの構築に役立つデータタイプについて説明します。

### ストアフロントデータ

ストアフロントのデータは、行動データやブラウザーデータとも呼ばれ、買い物客がサイトとどのようにやり取りするかについてのインサイトを明らかにすることができます。 例：

- 買い物客が最も興味を持っているのはどの製品やカテゴリですか？
- 買い物客が最も従事しているのは、どのような検索クエリですか？
- 買い物客は商品を買い物かごに追加した後、放棄していますか？
- 買い物客はデスクトップまたはモバイルブラウザーを使用していますか？

次のストアフロントイベントでは、これらの質問に答えるのに役立つデータを取得しています。

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [ログイン](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### バックオフィスデータ

バックオフィスデータ（サーバーサイドデータとも呼ばれます）を使用すると、注文のライフサイクルに関するインサイトを得ることができます。 例：

- 季節に応じてより頻繁に購入される製品はありますか？
- 買い物客は商品を返していますか？
- 顧客の生涯価値を計算するにはどうすればよいですか？

次のバックオフィスイベントでは、これらの質問に答えるのに役立つデータを取得しています。

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### 顧客プロファイルとセグメントデータ

顧客プロファイルデータを使用すると、買い物客の概要と対象となるセグメントに関するインサイトを得ることができます。 例：

- 名前
- 性別
- アドレス
- ロイヤルティステータス
- 電話番号
- メールアドレス
- ロイヤルティステータス
- 電話番号
- メールアドレス
- アップグレードの実施要件
- クロスチャネルショッパー
- 新製品の見通し
- ゴールド、シルバーまたはブロンズのロイヤルティメンバー

次のプロファイルイベントでは、これらの質問に答えるのに役立つデータを取得します。

- [プロファイルレコード](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

ストアフロント、バックオフィス、プロファイルデータは、Commerceのお客様および注文コンテキストの基盤となるので、お客様が表示している商品や最終的に購入する商品を把握するのに役立ちます。 その後、顧客の関心をターゲットにし、エクスペリエンスをパーソナライズできます。 次の節では、買い物客と関わることができる、パーソナライズされたエクスペリエンスのタイプについて説明します。

## パーソナライズされたエクスペリエンスのタイプ

Commerceの顧客および注文のコンテキストデータにより、次のタイプのパーソナライズされたエクスペリエンスが実現します。

| 経験 | 説明 |
|---|---|
| **製品の検出** | 次のマーチャンダイジングサービスが含まれます [saaS として導入](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). これらの機能を使用すると、行動データ、製品属性、在庫レベルを使用して、検索結果、製品レコメンデーションおよび閲覧ページ全体で製品検出を自動的にパーソナライズできます。 これらの機能はすべて [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **サイトコンテンツ** | サイトを閲覧している現在の顧客に基づいて、パーソナライズされた動的コンテンツブロックをデプロイする機能を指します。 |
| **オファーとキャンペーン** | セグメントデータに基づいてパーソナライズされたプロモーションコンテンツをデプロイできます。 |
| **測定** | は、データインテリジェンスを使用して、売上高、チャネルおよび商品のパフォーマンス、プロモーションなどを含むビジネスをよりよく理解します。 |

次の 2 つの節では、このデータを使用して、パーソナライズされたエクスペリエンスをで作成する方法について説明します [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) および [Commerceのネイティブ機能](#using-commerce-data-in-native-commerce-features).

## Adobe Experience PlatformでのCommerce データの使用

Commerce Experience Platform Edge Networkすべてのチャネルをまたいで買い物客にパーソナライズされたエクスペリエンスを提供するには、 [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 拡張機能。

![Experience Platformエッジへのデータのフロー](assets/commerce-edge.png){width="700" zoomable="yes"}

上記の画像では、SDK、API およびソースコネクタを使用して、ストアフロント、バックオフィスおよびExperience Platformプロファイルデータがカスタマーエッジに送信されています。 拡張機能がデータ共有の複雑さを処理するので、これらの要素の仕組みを完全に理解する必要はありません。 イベントデータがエッジにある場合は、そのデータを他のExperience Platformアプリケーションに取り込むことができます。

次の表に、使用可能なExperience Platformアプリケーションの一部と、それらのアプリケーションでのCommerce データの使用方法を示します。

| 経験 | 用途 | Commerce データの使用方法 |
|---|---|---|
| **サイトコンテンツ** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce データは、Real-Time CDPが複数のソース（ERP、CRM、CMS、POS）のデータを単一のプロファイルにステッチすることで、統合された顧客プロファイルを強化します。 Real-Time CDPでは、ルールベースのセグメントと AI ベースのセグメントの両方を作成して、マーケティングソリューションセット全体で使用することもできます。 また、Real-Time CDP オーディエンスを使用して、コンテンツブロック、プロモーションおよび関連する商品ルールをパーソナライズすることもできます。 参照： [[!DNL Audience Activation]](../customers/audience-activation.md) を参照してください。&#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce データは、Adobeでアクティブ化できます [!DNL Target] （動的ランディングページのテスト、最適化および作成の場合）。 送信されるCommerce データに基づいて、説明、仕様、レビュー、お勧め商品など、ページ上でのコンテンツの表示順序をパーソナライズできます。 |
| **オファーとキャンペーン** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerceの行動データやバックオフィスデータは、メールキャンペーン、SMS、プッシュ通知などのパーソナライズされたオムニチャネルジャーニーのトリガーとして機能できます&#x200B; |
| **測定** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) および [顧客 [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerceは、ストアフロントとバックオフィスの両方のデータをお客様に送信します [!DNL Journey Analytics] （ストアフロントデータのみAdobeに送信） [!DNL Analytics]）を使用して、Adobe Commerce Intelligence の基本指標（売上高、商品、プロモーションなど）を超えた豊富な分析を可能に&#x200B;ます。 |

Commerce データをExperience Platformに送信する方法について詳しくは、以下を参照してください。 [データ接続](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Commerceのネイティブ機能でのCommerce データの使用

次の節では、製品Recommendationsや Live Search などのCommerceのネイティブ機能を使用して、パーソナライズされたショッピングエクスペリエンスを作成する方法について説明します。 また、という機能についても説明します [!DNL Audience Activation]：前述のように、Real-Time CDPというExperience Platformで利用可能な製品のデータを使用します [以前](#using-commerce-data-in-adobe-experience-platform). Real-Time CDPはCommerce固有ではありませんが、その情報は次を通じてCommerceに取り込むことができます [[!DNL Audience Activation]](../customers/audience-activation.md) 拡張機能。

次の表に、Commerceの顧客データと注文コンテキストデータを実用的なインサイトに変えるために使用できるCommerce機能を示します。

| 経験 | 機能 | 説明 |
|---|---|---|
| **製品の検出** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | AI ランキングアルゴリズムを使用して、買い物客のオンサイト行動アクションに基づいて検索結果をパーソナライズおよび最適化し、検索の関連性とコンバージョンを高めます。 |
|  | [製品のRecommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | 買い物客の行動、トレンド、製品の類似性などに基づく、AI を活用した製品レコメンデーションを表示します。 商品レコメンデーションをAdobe Commerce カタログと組み合わせると、非常に魅力的で関連性が高く、パーソナライズされたエクスペリエンスが提供されます。 |
|  | [カテゴリマーチャンダイジング](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | ライブサーチ管理者からアクセスするカテゴリマーチャンダイジングは、AI を使用して、各カテゴリページの製品のシーケンスを自動的にランク変更し、すべての買い物客の関連性とコンバージョンを高めます。 AI を活用したルールを作成および管理し、買い物客のアクションとアフィニティに従って、カテゴリページでの製品シーケンスを自動的にランク付け直すことができます。 |
| **サイトコンテンツ** | [Commerceのネイティブ機能に基づく動的ブロック](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | を使用すると、価格ルールや顧客セグメントで設定されたロジックに基づいてパーソナライズされたサイトコンテンツを配信できます。 |
|  | [Real-Time CDP オーディエンスによって通知された動的ブロック](../customers/audience-activation.md) | マーチャントは、Real-Time CDPで設定されたオーディエンスに基づいてパーソナライズされたサイトコンテンツを提供できます。 |
| **オファーとキャンペーン** | [買い物かご価格ルール](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | 一連の条件に基づいて、買い物かご内の商品に割引を適用できます。 |
|  | [Commerceのネイティブ機能に基づく動的ブロック](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Commerceでネイティブに設定された顧客セグメントに基づいて、パーソナライズされたバナープロモーションを表示できます。 |
|  | [Real-Time CDP オーディエンスによって通知された動的ブロック](../customers/audience-activation.md) | Real-Time CDPで設定されたオーディエンスに基づいて、パーソナライズされたプロモーションを表示できます。 |
| **測定** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | （旧称：Magento Business Intelligence）は、データに基づいた意思決定や、明確で十分な情報に基づいたアクションの実行に役立つベストプラクティスのインサイトを提供するクラウドプラットフォームです。 Adobe Commerce Intelligence は、お客様のデータを分析して、注文の増加、お客様の行動、プロモーション戦略の効果に関する質問に回答するのに役立ちます。 |
