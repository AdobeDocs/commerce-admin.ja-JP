---
title: Adobeの拡張機能
description: AdobeがリリースしたAdobe CommerceおよびMagento Open Sourceの拡張機能に関する情報を確認します。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/-QGqm0VMRlCNuKqHGdGVKjs8ZgNcjYZjFaeIFsOLWCA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: da3860b0-d637-47df-bef0-273751180266
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1434
ht-degree: 0%

---

# Adobeの拡張機能

このトピックでは、AdobeがリリースするAdobe CommerceおよびMagento Open SourceのPHP拡張機能について説明します。

拡張機能は、管理者とストアフロントに機能、サービス、統合を追加します。 これらの拡張機能の一部は、Magento Open Source コミュニティのコントリビューションを通じて開発されています。 一部の拡張機能はデフォルトでインストールされ、別の拡張機能は個別にインストールする必要があります。

+++Adobe Commerceの拡張機能について詳しく見る

Adobeでは、Adobe Commerce プロジェクトを拡張またはカスタマイズするための主なアプローチが2つあります。

- インプロセスの拡張性：PHP拡張機能など、Adobe Commerce アプリケーションプロセス内で実行されるカスタムコードと拡張機能を使用します。 この従来のアプローチでは、詳細な統合が可能ですが、アップグレード時には慎重に管理する必要があります。

- プロセス外の拡張性：コアソフトウェアとは独立して動作するカスタムコードとアプリケーションを使用します。 この最新のアプローチは、次のような方法で総所有コストを削減するのに役立ちます。

   - 拡張機能がコアから切り離されているため、アップグレードを簡素化したい
   - 開発者に、実装のタイミングと方法に関する詳細な制御を提供
   - 拡張コンポーネントの独立した拡張とメンテナンスを可能にする

Adobe Commerceでは、両方の拡張機能をサポートする戦略とツールを提供しています。 詳しくは、[Adobe Commerceの拡張性](https://developer.adobe.com/commerce/extensibility/)を参照してください。

+++

## Adobe拡張機能のデフォルトのインストール

次のAdobe拡張機能は、Adobe Commerceに含まれており、Adobe Commerce アプリケーションと共に自動的にインストールされます。 拡張機能の説明に記載されているように、管理者でさらに設定または有効化が必要な拡張機能もあります。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md)は、同時チェックアウト保護と出荷照合アルゴリズムを使用して、1つまたは複数の場所と販売チャネルで強化された在庫と出荷管理を提供します。 在庫量を追跡し、顧客に正確な販売可能な在庫量を提供し、推奨事項に従って出荷したり、手作業で選択したりすることで、在庫全体を制御することができます。 グローバル、ソース、製品ごとに管理設定を構成します。

>[!NOTE]
>
>この拡張機能は、コミュニティエンジニアリングプログラムを通じて[[!DNL Inventory Management]](https://github.com/magento/inventory) （旧MSI）プロジェクトの一部として開発されました。

[!DNL Inventory Management]は、すべての機能がデフォルトで有効になっている状態でインストールされます。 これらのインベントリ機能を有効にするために追加の手順は必要ありません。 [!DNL Inventory Management]機能について詳しくは、[[!DNL Inventory Management]  ユーザーガイド &#x200B;](../inventory-management/guide-overview.md)を参照してください。

### Braintree

PayPalとGene Commerceは、Commerce 2.4.x ストア向けにBraintreeの公式拡張機能を共同開発しました。 コンバージョンを促進するために設計された改善されたチェックアウト体験を特徴とし、更新には、ショッピング中やチェックアウト中に消費者に関連するPayLater メッセージとボタンを自動的に表示するPayLater オプションが含まれています。

この拡張機能はデフォルトでインストールされますが、ストアに対して有効にするには、Adminで[Braintree アカウント &#x200B;](https://www.braintreepayments.com/)と設定が必要です。 Braintreeを使用して取引を処理する際に適用される手数料を判断するには、[Braintreeの価格](https://www.braintreepayments.com/braintree-pricing)を確認してください。

AdminでのBraintree設定について詳しくは、_販売および購入エクスペリエンスガイド_&#x200B;の[Braintree](../stores-purchase/braintree.md)のトピックを参照してください。

### Google reCAPTCHA

Google reCAPTCHAは、ストアフロントと管理UIの両方に対して、標準のCAPTCHAで利用できるよりも高いレベルのセキュリティを提供し、次のことを行うことができます。

- 顧客がアカウントを作成する、パスワードを取得する、アカウントにログインする、会社に問い合わせるといったことを確認します。
- 管理者ユーザーがログインするときのセキュリティを強化します。

Captcha コード入力時の潜在的なユーザーエラーを低減し、チェックアウト時のハードルを追加することなく、カートのコンバージョンを促進します。 [非表示またはインタラクティブなチェックを使用してreCAPTCHA](../systems/security-google-recaptcha.md)を有効にして設定し、[!DNL Commerce]管理者とストアフロントへの安全なアクセスを強化します。

### 二段階認証

[!DNL Commerce]管理者は、ストア、注文、顧客データへのすべてのアクセスを提供します。 [2要素認証](../systems/security-two-factor-authentication.md) （2FAまたはTFA）では、すべてのデバイスから[!DNL Commerce]管理者にアクセスするために、標準のログイン名とパスワードを超えた追加の認証が必要になるので、セキュリティが強化されます。 この拡張機能は、Google Authenticator、Authy、[!DNL Duo]、およびU2F キーを含む複数の認証キーをサポートしています。 この認証は、管理者ユーザーにのみ適用されます。 ストアフロントの顧客アカウントでは利用できません。

これらの機能はデフォルトで有効になっています。 各管理者ユーザーは、サポートされている認証者のいずれかをインストールして設定する必要があります。

>[!NOTE]
>
>管理者に対してAdobe Identity Management サービス（IMS）認証を有効にしたAdobe Commerce ストアでは、ネイティブのCommerce 2FAが無効になっています。 Adobeの資格情報を使用して管理者にログインしているユーザーは、多くの管理者タスクに対して再認証を行う必要はありません。 認証は、管理者ユーザーが現在のセッションにログインしたときにAdobe IMSによって処理されます。 [Adobe Identity Management Service （IMS）統合の概要](./adobe-ims-integration-overview.md)を参照してください。

## インストールが必要なAdobe拡張機能

Adobeには、Composerを使用して個別にインストールする必要がある拡張機能が用意されています。 これらの拡張機能は、次のような様々なチャネルで利用できます。

- リポジトリアクセス（repo.magento.com）

  次の拡張機能をインストールするには、アカウントのプロビジョニングと資格情報が必要です。 Adobeの担当者にお問い合わせください。

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [Commerce向けAEM Assets統合](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  次のAdobe拡張機能は、[marketplace.magento.com](https://marketplace.magento.com)で一般にアクセスできます。 これらの拡張機能は追加費用なしで利用できます。

   - [ライブサーチ](#live-search)
   - [商品レコメンデーション](#product-recommendations)
   - [カタログサービス](#catalog-service)
   - [決済サービス](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ。別途ライセンスが必要です。

[!DNL Adobe Commerce B2B]は、標準のCommerce ストアを包括的な企業間基盤に変換する統合拡張機能です。 統合された企業アカウントの下で、複数の購入者、カスタム役割、購買権限を持つ複雑な組織構造を管理できます。 主な機能には、企業固有のカタログと価格設定、交渉可能な見積もり、発注管理、要求リスト、クイックオーダー機能などがあります。 このソリューションは、B2BとB2Cの両方のモデルを単一のインスタンスでサポートし、多様なビジネスニーズに柔軟に対応します。 この拡張機能は、別途ライセンスを必要とし、Adobe Commerceのコア機能とシームレスに統合され、包括的なB2B e コマースソリューションを提供します。

プロビジョニングについては、Adobeの担当者にお問い合わせください。 実装の詳細と設定手順については、[[!DNL B2B for Adobe Commerce]  ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ja)を参照してください。

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ。Adobe Experience Manager （AEM） AssetsおよびAEM Dynamic Mediaのライセンスも必要です。

[!DNL AEM Assets Integration for Commerce]は、Adobe CommerceとAdobe Experience Managerのデジタルアセット管理（DAM）システムを接続して、すべてのデジタルアセットを一元管理します。 この統合により、アセットの自動同期、リアルタイムの更新、コマースのストアフロントをまたいだ効率的なコンテンツ再利用が可能になります。 AEMの堅牢なアセット管理能力とCommerceを組み合わせることで、合理的なワークフロー、一貫性のあるブランドエクスペリエンス、クラウドベースのインフラストラクチャを通じた最適なメディア配信などのメリットを享受できます。

プロビジョニングについては、Adobeの担当者にお問い合わせください。 実装の詳細と設定手順については、[[!DNL Assets Integration]  ユーザーガイド &#x200B;](../content-design/aem-assets-integration.md)を参照してください。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

ライブサーチは、AIを活用した検索ソリューションとリアルタイムの「インスタント検索機能」を提供するAdobe Commerce独自の機能です。 買い物客が文字を入力している間に、商品のサムネールを表示することで、関連性の高い検索結果をすばやく提供できます。また、買い物客の行動にもとづいてフィルターを自動的に調整できる、インテリジェントなファセット機能も搭載されています。 このソリューションには、商品の販売促進と埋め込みのマーチャンダイジング機能、類義語管理、検索分析が含まれています。 Adobe Commerceに追加費用なしで含まれている[!DNL Live Search]は、デフォルトの検索機能を、より洗練されたSaaS ベースの検索エクスペリエンスに置き換えます。 最小限の設定で始められます。

実装の詳細と技術的な要件については、[Live Search ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ja)を参照してください。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

[!DNL Product Recommendations]は、カスタマーショッピング ジャーニー全体を通じてパーソナライズされた商品レコメンデーションを提供する、Adobe AI テクノロジーを搭載したAdobe Commerce限定の機能です。 このソリューションは、買い物客の行動と商品との関係をリアルタイムで分析し、関連性の高いレコメンデーションを自動的に生成します。手作業のマーチャンダイジングルールは必要ありません。 このAIを活用したアプローチは、コンバージョン率と売上の可能性を高めながら、買い物客により魅力的な商品発見体験を提供するのに役立ちます。

実装の詳細とベストプラクティスについては、[[!DNL Product Recommendations]  ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=ja)を参照してください。

### [!DNL Catalog Service]

[!BADGE Adobe CommerceおよびMagento Open Sourceのインストールをサポートしています]{type=Informative tooltip="サポート対象"}

[!DNL Catalog Service]は、Adobe CommerceおよびMagento Open Source向けの高性能ソリューションで、GraphQL エンドポイントを通じてカタログデータへの最適なアクセスを提供します。 製品の詳細や関連情報については、個別の同期データベースを維持し、直接のアプリケーション通信をバイパスして、ページの読み込み時間を短縮します。 このサービスは、商品詳細ページ、カテゴリーリスト、検索結果ページで特に価値があり、従来のコマース実装とヘッドレスコマース実装の両方に最適です。

セットアップ手順と技術的な詳細については、[[!DNL Catalog Service]  ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=ja)を参照してください。

>[!NOTE]
>
>ライブサーチまたは商品レコメンデーションが有効になっている場合、カタログサービスは自動的にインストールされます。 手動インストールは必要ありません。

### [!DNL Payment Services]

[!BADGE Adobe CommerceおよびMagento Open Sourceのインストールをサポートしています]{type=Informative tooltip="サポート対象"}

[!DNL Payment Services]は、包括的な決済処理機能を提供するAdobe CommerceおよびMagento Open Source ストア向けのターンキー決済ソリューションです。 このサービスは、組み込みの不正利用防止機能と安全な支払いゲートウェイ機能を統合しており、クレジットカード/デビットカード、PayPal、Venmo （米国）、PayLater プランなど、複数の支払いオプションを提供しています。 Commerceの管理インターフェイスを通じた取引レポートと注文管理の統合を特徴としており、加盟店が支払いを追跡し、キャッシュフローを管理し、財務データを照合するのに役立ちます。

設定手順と支払いオプションについて詳しくは、[[!DNL Payment Services]  ユーザーガイド &#x200B;](https://experienceleague.adobe.com/ja/docs/commerce/payment-services/overview)を参照してください。
