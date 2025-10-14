---
title: 魅力的でパーソナライズされたエクスペリエンスを大規模に作成
description: Adobeの機能を使用して、買い物客  [!DNL Commerce]  パーソナライズされたエクスペリエンスを作成できる方法を説明します。
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# 魅力的でパーソナライズされたエクスペリエンスを大規模に作成

Adobe [!DNL Commerce] は、すべての顧客タッチポイントをパーソナライズし、買い物客のエンゲージメント、コンバージョン、売上高を向上させる強力なツールキットを提供します。

この記事では、次の内容について説明します。

- パーソナライゼーションとは
- パーソナライゼーションを実現するには、どのようなデータが必要ですか？
- Adobeを使用してパーソナライゼーションのロック [!DNL Commerce] 解除するにはどうすればよいですか？
- 利用可能なパーソナライゼーションのユースケース

## パーソナライゼーションとは

Personalizationとは、顧客の固有のニーズ、コンテキスト、好みに合わせて各顧客の購入体験の側面をカスタマイズすることを意味します。 Personalizationは、サイト上のコンテンツや最適な商品の推奨に限定されず、カスタマージャーニー全体にわたるすべてのタッチポイントを包含します。これには以下が含まれます。

- **キャンペーンと通信** - キャンペーンと通信を介して関連性の高い一貫したメッセージを配信します
- **製品の検出** – 適切な製品を適切なタイミングで適切な顧客に表示する
- **プロモーションとオファー** - ターゲティングのプロモーションとオファーで、各顧客のコンバージョンを促進
- **コンテンツエクスペリエンス** – 各顧客とそのジャーニーへの関連性が高いと感じるようにサイトコンテンツをカスタマイズする

![Personalizationの種類 &#x200B;](assets/types-personalization.png){width="700" zoomable="yes"}

このようなパーソナライズされたエクスペリエンスは、少数の顧客に対しては実現可能と思われますが、すべてのタッチポイントとチャネルで数千または数百万の顧客に対して大規模にパーソナライズすると、すべてリアルタイムで実現が不可能と感じることがあります。 以降の節では、Adobe [!DNL Commerce] とAdobe Experience Cloudの機能について説明します。

## パーソナライゼーションを実現するには、どのようなデータが必要ですか？

効果的なパーソナライゼーションには、顧客に関する情報を提供するコンテキストまたはシグナルが必要で、それを使用してエクスペリエンスを変更できます。 次の表に、様々なデータタイプと、そのデータの収集とアクティブ化をサポートする際にAdobe [!DNL Commerce] が果たす役割を示します。

| データタイプ | ストアフロントデータ（行動イベント） | バックオフィスデータ（サーバーサイドイベント） | 顧客プロファイルとセグメントデータ |
|---|---|---|---|
| **定義** | サイトに対する顧客のクリックまたはアクション。 | 各注文のライフサイクルと詳細（過去および現在）に関する情報。 | 買い物客は誰で、どのようなセグメントに該当するか。 |
| **Adobe Commerceのイベント** | [pageView](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **注文ステータス**:<br>[orderPlaced](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**注文履歴**](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU、名前、価格数量、割引 <br> – 製品カテゴリ <br> – 支払い金額、タイプ、通貨 <br> – 発送方法と金額 <br> – 払い戻し ID、金額、通貨 <br> – 返品理由、条件、解決策 <br> – 住所 <br>- メール | [**プロファイルレコード**](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-profilerecord):（名前、性別、住所、ロイヤルティステータス、電話番号、メールアドレス） <br>**アカウントステータス**:<br>[accountCreated](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

これらの豊富なファーストパーティ [!DNL Commerce] データを使用すると、買い物客のエクスペリエンスをターゲットにしてパーソナライズする準備が整います。 次の節では、[!DNL Commerce] とAdobe Experience Cloudを使用して、パーソナライズされたエクスペリエンスと、アクティブ化できるユースケースを作成する方法を説明します。

## Adobe [!DNL Commerce] はパーソナライゼーションをどのように強化しますか？

Adobe [!DNL Commerce] Data Sharing を使用すると、前のテーブルのデータタイプを収集して他のAdobe Experience Cloud製品と共有し、統合された顧客プロファイルとオーディエンス、パーソナライズされたキャンペーン、豊富な分析とインサイトを強化できます。

![Experience Platform エッジへのデータのフロー &#x200B;](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Data Sharing には、次の 2 つの主要なコンポーネントが含まれます。

1. [&#x200B; データ接続 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/overview)：次のようなAdobe Experience Cloud アプリケーションをまたいで使用するために、Adobe [!DNL Commerce] からAdobe Experience Platform Edge Network にストアフロント、バックオフィス、顧客プロファイルデータを共有します。

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/ja/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview)：様々なソース（ERP、CRM、POS）からの顧客データを統合されたプロファイルに結び付け、ルールベースまたは AI ベースのセグメントを作成します。
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/ja/docs/journey-optimizer/using/get-started/get-started): メールキャンペーン、SMS、プッシュ通知など、パーソナライズされたオムニチャネルジャーニーを開始します。
   - [Customer Journey Analytics](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-overview/cja-overview) および [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/ja/docs/analytics/analyze/admin-overview/analytics-overview)：お客様とビジネスに関するインサイトを得ます。
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/ja/docs/target/using/introduction/intro): コンテンツ、おすすめの商品、オファー、ナビゲーションなどをテストして最適化します。

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/ja/docs/commerce-admin/customers/audience-activation): [!DNL Real-Time CDP] オーディエンスを使用して、Adobe [!DNL Commerce] サイト上の動的コンテンツブロック、プロモーションおよび関連する製品ルールをパーソナライズします。

### あらゆるチャネルにわたって規模に応じてパーソナライズされたストアフロントエクスペリエンス

Adobe [!DNL Commerce] は、[Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/?lang=ja) と呼ばれる高性能なストアフロントを活用して、AI 機能をコアに、速度を基盤として、すべてのチャネルにわたってパーソナライズされたエクスペリエンスを提供できます。

Edge Delivery Servicesを使用すると、次のことができます。

- **パーソナライズされたコンテンツを作成**：ドキュメントベースのオーサリング、生成 AI テキストと画像バリエーションのネイティブ実験を使用して、エクスペリエンスを大規模にパーソナライズします。 Assetsとジェネレーティブ AI のコンテンツ作成を使用して、商品およびマーケティング画像を大規模に生成します。

- **バリエーションを生成**：コンテンツ作成者が生成 AI を使用して、パーソナライズされた AI 駆動型の大量の [&#x200B; テキストコンテンツと画像のバリエーション &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-manager-learn/sites/generative-ai/generate-variations) をAdobe Fireflyで作成できます。

- **Edge Delivery Services ストアフロントを介したデプロイ**：ドロップインコンポーネントを活用したEdgeおよびCommerce機能のコンテンツをデプロイして、オーディエンスにカスタムのショッパブルエクスペリエンスを作成します。

- **CommerceとAdobe Experience Manager Assets**：大規模なジェネレーティブ AI 製品のアセット作成とバリエーション。 任意のチャネルをまたいだコンテンツ配信を作成、配信、監視します。

![&#x200B; ドロップダウン：製品の詳細ページ &#x200B;](assets/drop-in.png){width="700" zoomable="yes"}

### 標準のPersonalization: Adobe [!DNL Commerce] のネイティブ機能の概要

Adobe [!DNL Commerce] は、すぐに使用できるネイティブの機能により、強力なパーソナライゼーションを提供します。 次の表に [!DNL Commerce] パーソナライゼーションジャーニーを開始するために直ちにアクティブ化できる機能を示します。

| カテゴリ | 機能 |
|---|---|
| パーソナライズされた製品検出 | [[!DNL Live Search]](https://experienceleague.adobe.com/ja/docs/commerce/live-search/overview):AI を活用した検索で、買い物客のオンサイト行動アクションと親和性に基づいて検索結果をパーソナライズし最適化します。<br>[&#x200B; インテリジェントカテゴリマーチャンダイジング &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/live-search/live-search-admin/category-merch)：買い物客のオンサイトでの行動とアフィニティに基づく、カテゴリページに関する AI 主導の製品ランキング。<br>[&#x200B; 製品レコメンデーション &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/product-recommendations/guide-overview)：買い物客の行動、トレンド、アフィニティに基づく、AI を活用した製品レコメンデーション。<br>[&#x200B; 関連製品ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)：カスタムルールを定義して、カタログの製品を表示し、クロスセルとアップセルを促進します。 |
| パーソナライズされたサイトコンテンツ | [&#x200B; 動的コンテンツブロック &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks):Adobe Commerceの顧客セグメントに基づいて、パーソナライズされたコンテンツブロック（バナーなど）を表示します。 |
| パーソナライズされたオファーとプロモーション | [&#x200B; 買い物かご価格ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart):Adobe [!DNL Commerce] の顧客セグメントなど、一連の条件に基づいて、買い物かご内の商品に割引を適用します。 |
| インサイトと測定 | [Adobe [!DNL Commerce]  インテリジェンス &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-business-intelligence/mbi/getting-started)：パーソナライズ機能戦略の仕組みを把握し、時間の経過と共に効果を向上させます。 |

## 上位のパーソナライゼーションユースケース

Adobe [!DNL Commerce] のお客様は、標準搭載の機能を使用し、様々なユースケースでAdobe Experience Cloudにデータを共有しています。 以下の節では、上位のユースケースを重点的に取り上げ、Adobe [!DNL Commerce] Only または [!DNL Commerce] とExperience Cloud アプリを使用してどのように実装されるかを説明します。

### パーソナライズされたキャンペーンとコミュニケーション

| ユースケース | 解決策 |
|---|---|
| **放棄された買い物かごと参照** – 高いエンゲージメントを示した後に顧客が買い物かごや閲覧セッションを放棄した場合に、パーソナライズされた再エンゲージメントメールまたは通知を配信します | **Adobe [!DNL Commerce] のみ**:<br>[&#x200B; メールのリマインダー &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe Journey OptimizerとのAdobe [!DNL Commerce]**:<br>[!DNL Commerce] データは、オムニチャネル離脱ジャーニーのトリガーとして機能します。 顧客属性、破棄した内容、その他の買い物行動、過去の購入に基づいて、ジャーニーをパーソナライズします。<br>Adobe Journey OptimizerとReal-Time CDPのCommerce：放棄キャンペーンは、共通の顧客プロファイルと一元管理されたオーディエンスに基づいてカスタマイズできます。例えば、高い離脱率のオーディエンスを作成することができます。 |
| **一元的なオーディエンスの作成** - オンサイト行動、過去の購入、プロファイル属性、カテゴリアフィニティ、ロイヤルティステータス、顧客価値などに基づいて、ルールベースまたは AI を利用したオーディエンスを作成します | **Adobe [!DNL Commerce] Only**:<br> 顧客がアカウントを作成する際に、顧客プロファイル情報 [!DNL Commerce] 収集します。 ルールベース [&#x200B; 顧客セグメント &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/customers/segments/customer-segments) と顧客グループを作成して、コンテンツとプロモーションをパーソナライズします。<br>**Adobe [!DNL Commerce] とAdobe Real-Time CDP**:<br> データソースやチャネルをまたいだ [&#x200B; 統合プロファイル &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/segmentation/home)。ルールベースまたは AI を活用したオーディエンス。 |
| **買い物客の行動に基づくパーソナライズされたメール/SMS オファー** – 過去の購入および買い物客の行動に基づいて、ターゲットメールを使用して顧客にパーソナライズされたオファーを送信します。例えば、顧客が表示またはエンゲージメントした製品やカテゴリのオファーを送信します。 | **Adobe [!DNL Commerce] Only**:<br> マーケティング自動化ソリューションで使用するデータをエクスポートします。<br>**Adobe Journey OptimizerとReal-Time CDPのAdobe [!DNL Commerce]**:<br>[!DNL Commerce] データは、メールまたは SMS オファーのトリガーとして機能し、に基づいてパーソナライズするためのシグナル（買い物客の行動）を提供します。 Real-Time CDPは必須ではありませんが、通常、これらのオファーとキャンペーンは、Real-Time CDP内で作成および管理されるオーディエンスを中心に作成されます。 |
| **クロスまたはアップセル互換の製品/ブランド** – 顧客が互換性のある製品やブランドを購入した場合、または別の製品やブランドに対する親和性が高いことを示した場合は、キャンペーン（メール/SMS）を送信してクロスセルコンバージョンを促進します。 | **Adobe [!DNL Commerce] のみ**:<br>Adobe [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/ja/docs/commerce/product-recommendations/guide-overview) を使用して、サイト上の特定の商品をお勧めします。 [&#x200B; 関連製品ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) を使用して、他の製品を提案することもできます。<br>**[!DNL Commerce] と [!DNL Target]**:<br>Adobe [!DNL Target] には、カテゴリ親和性などの強力な機能を備えたビルトインの商品レコメンデーションエンジンもあります。 これは、クロスまたはアップセルに使用できます。Adobe Journey Optimizerとの <br>**[!DNL Commerce] 携**:<br>[!DNL Target] または [!DNL Commerce] を使用してレコメンデーションする商品を決定し、Adobe Journey Optimizerを通じて配信します。 |

### パーソナライズされたサイトエクスペリエンス

| ユースケース | 解決策 |
|---|---|
| **サイトコンテンツのパーソナライズ** – 製品の参照やカテゴリへの親和性など、買い物客のアクションに基づいて、サイトバナーやその他のページコンテンツをパーソナライズします。 A/B テストの結果やビジネス目標に基づいて、最適なコンテンツをデプロイします。 | **Adobe [!DNL Commerce] Only**:<br> セグメント固有の [&#x200B; 動的コンテンツブロック &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) をデプロイします。Real-Time CDPとの <br>**[!DNL Commerce] 携 &#x200B;**:<br>[Audience Activation](https://experienceleague.adobe.com/ja/docs/commerce-admin/customers/audience-activation) を使用して、Real-Time CDPでプロファイルとオーディエンスを一元的に管理しながら、リアルタイムのアクションと統合された顧客プロファイルデータに対応する、オーディエンス固有の動的コンテンツブロックをデプロイします。[!DNL Target]**:<br>Adobe [!DNL Target] のAdobe [!DNL Commerce] データを使用して、コンテンツ、ナビゲーション項目、フルページレイアウトなど、サイトエクスペリエンスのあらゆる部分をパーソナライ <br>**[!DNL Commerce] します。 コンテンツの A/B テストを行い、顧客ごとに勝者コンテンツを自動的に選択してデプロイします。AEM Assetsを <br>**[!DNL Commerce] 用する場合 &#x200B;**:<br> すべてのコンテンツをAdobe Experience Manager Assetsに保存します。 Adobe Commerce内からそのコンテンツにネイティブにアクセスします。 ジェネレーティブ AI を使用して、コンテンツのバリエーションを作成し、様々なセグメントやオーディエンスに合わせてパーソナライズします。 |
| **行動に基づくパーソナライズされたオンサイトオファー** – 製品の閲覧やカテゴリへの親和性など、買い物客のアクションに基づいてプロモーションをパーソナライズします。 A/B テストの結果やビジネス目標に基づいて、次善のオファーをデプロイします。 | **Adobe [!DNL Commerce] Only**:<br> セグメント固有のカタログおよび [&#x200B; 買い物かご価格ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) をデプロイします。<br>**Adobe [!DNL Commerce] とReal-Time CDP**:<br>[Audience Activation](https://experienceleague.adobe.com/ja/docs/commerce-admin/customers/audience-activation) を使用すると、Real-Time CDPでプロファイルやオーディエンスを一元的に管理しながら、オーディエンス固有のオファーをデプロイできます。<br>**[!DNL Target]** のCommerce: Offer Decisioning を使用して、Adobe Commerceにデプロイされたオファーをガイドするために、デプロイするオファー、A/B テストまたはビジネス目標を決定します。 |

### 分析とインサイト

| ユースケース | 解決策 |
|---|---|
| **チャネル別の顧客行動** – 顧客が各チャネル（web、対面、アプリなど）にどのように関与して各チャネルのマーケティング戦略に影響を与えるかのニュアンスを理解します。買い物客ファネルとカスタマーエクスペリエンスの弱点を理解します。 | **Adobe [!DNL Commerce] Only**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/ja/docs/commerce-business-intelligence/mbi/getting-started) は、デジタル [!DNL Commerce] チャネルに関する豊富な分析機能を提供しますが、チャネルやカスタマージャーニーのより広範な部分に関する分析は提供しません。<br>**Customer Journey AnalyticsのAdobe [!DNL Commerce]**:<br>[!DNL Commerce] データフィードのデータダッシュボードには、カスタマーエクスペリエンスのすべてのステージ（チャネルをまたぐ）における豊富な詳細情報が表示されます。 すべてのタッチポイントとより広範なファネルを理解して、顧客がフォールオフする可能性のあるカスタマージャーニーの弱点を特定します。 |
| **購入の傾向** – 特定の時間枠における購入行動（買い物客バスケット分析、製品分析など）を把握して、過去の購入パターンに基づいてトレンド、季節性を特定し、マーケティングを最適化します。 | **Adobe [!DNL Commerce] Only**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/ja/docs/commerce-business-intelligence/mbi/getting-started) は、デジタル [!DNL Commerce] チャネルに関する豊富な分析機能を提供しますが、チャネルやカスタマージャーニーのより広範な部分に関する分析は提供しません。<br>**Customer Journey AnalyticsのAdobe [!DNL Commerce]**:<br>[!DNL Commerce] データフィードのデータダッシュボードには、カスタマーエクスペリエンスのすべてのステージ（チャネルをまたぐ）における豊富な詳細情報が表示されます。 すべてのタッチポイントとより広範なファネルを理解して、顧客がフォールオフする可能性のあるカスタマージャーニーの弱点を特定します。 |

## 使用例

- Adobe Journey Optimizerを使用して [&#x200B; 放棄された買い物かごのメールを送信 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/use-cases/using-ajo) する方法を説明します。
- Adobe [!DNL Commerce] で買い物かごの価格ルールを通知する [Real-Time CDPでオーディエンスを作成 &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/data-connection/use-cases/create-audience) する方法を説明します。
