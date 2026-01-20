---
title: Adobeの拡張機能
description: AdobeがリリースしたAdobe CommerceおよびMagento Open Sourceの拡張機能に関する情報を確認します。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 36c91007d21834b49351c8b53c617e442deebaa0
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---

# Adobeの拡張機能

ここでは、AdobeがリリースしたAdobe CommerceおよびMagento Open Sourceの PHP 拡張機能について説明します。

拡張機能は、管理およびストアフロントに機能、機能、サービスおよび統合を追加します。 これらの拡張機能の一部は、Magento Open Source コミュニティのコントリビューションを通じて開発されています。 デフォルトでインストールされる拡張機能もあれば、個別にインストールする必要がある拡張機能もあります。

+++Adobe Commerceの拡張の詳細

Adobeには、Adobe Commerce プロジェクトを拡張またはカスタマイズする 2 つの主な方法が用意されています。

- プロセス内拡張機能：PHP 拡張機能などのAdobe Commerce アプリケーションプロセス内で実行されるカスタムコードおよび拡張機能を使用します。 この従来のアプローチでは、深い統合が可能ですが、アップグレード時には慎重な管理が必要です。

- プロセス外拡張機能：コアソフトウェアとは独立して動作するカスタムコードおよびアプリケーションを使用します。 この最新のアプローチにより、次の方法で TCO （総所有コスト）を削減できます。

   - 拡張機能がコアから切り離されているので、アップグレードが簡素化されます。
   - 実装のタイミングと方法を開発者がより詳細に制御できるようにする
   - 拡張機能コンポーネントの独立したスケーリングおよびメンテナンスの有効化

Adobe Commerceは、両方のタイプの拡張機能をサポートする戦略とツールを提供します。 詳しくは、[Adobe Commerce拡張機能 ](https://developer.adobe.com/commerce/extensibility/) を参照してください。

+++

## Adobe拡張機能はデフォルトでインストールされます

次のAdobe拡張機能はAdobe Commerceに含まれており、Adobe Commerce アプリケーションと共に自動的にインストールされます。 一部の拡張機能では、拡張機能の説明に記載されているように、管理者でさらに設定または有効化する必要があります。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) は、同時チェックアウト保護および出荷照合アルゴリズムにより、1 つまたは複数の場所および販売チャネルにわたる在庫および出荷管理を強化します。 在庫数量を追跡し、正確な販売可能な在庫金額を顧客に提供し、レコメンデーションまたは手動の選択に従って出荷して、在庫全体を管理します。 ソースごと、製品ごとにグローバルに管理設定を構成します。

>[!NOTE]
>
>この拡張機能は、[[!DNL Inventory Management]](https://github.com/magento/inventory) （旧称 MSI）プロジェクトの一環として、コミュニティエンジニアリングプログラムを通じて開発されました。

[!DNL Inventory Management] は、デフォルトですべての機能が有効な状態でインストールされます。 これらのインベントリ機能を有効にするために必要な追加手順はありません。 [!DNL Inventory Management] の機能について詳しくは、[[!DNL Inventory Management]  ユーザーガイド ](../inventory-management/guide-overview.md) を参照してください。

### Braintree

PayPal と Gene Commerceは共同で、Commerce 2.4.x ストア向けの公式Braintree拡張機能を開発しました。 コンバージョンを促進するように設計された改善されたチェックアウトエクスペリエンスを備えたこのアップデートには、ショッピング中およびチェックアウト中に消費者に関連する PayLater メッセージおよびボタンを自動的に表示する PayLater オプションが含まれています。

この拡張機能はデフォルトでインストールされますが、ストアで [Braintree アカウントと ](https://www.braintreepayments.com/) 管理者の設定が有効になっている必要があります。 Braintreeを使用して取引を処理する際に発生する手数料を確認するには、[Braintreeの価格 ](https://www.braintreepayments.com/braintree-pricing) を確認してください。

管理者のBraintree設定について詳しくは、[ セールスおよび購入エクスペリエンスガイド ](../stores-purchase/braintree.md) の _Braintree_ に関するトピックを参照してください。

### Google reCAPTCHA

Google reCAPTCHA は、標準の CAPTCHA よりも高いレベルのセキュリティをストアフロントと管理 UI に提供し、以下の機能を提供します。

- 顧客がいつアカウントを作成するか、パスワードを取得するか、顧客のアカウントにログインするか、または会社に問い合わせるかを確認します。
- 管理者ユーザーがログインしたときのセキュリティを強化します。

これにより、Captcha コードを入力する際に発生する可能性のあるユーザーエラーを減らし、チェックアウト時にハードルを追加することなく、買い物かごへのコンバージョンを促すことができます。 非表示またはインタラクティブなチェックを使用して [reCAPTCHA を有効にして設定 ](../systems/security-google-recaptcha.md) し、[!DNL Commerce] Admin およびストアフロントへの安全なアクセスを強化します。

### 二要素認証

[!DNL Commerce] 管理者は、ストア、注文および顧客データへのすべてのアクセスを提供します。 [2 要素認証 ](../systems/security-two-factor-authentication.md) （2FA または TFA）は、すべてのデバイスから [!DNL Commerce] Admin にアクセスするために、標準のログイン名とパスワード以外の追加認証を必要とすることにより、セキュリティを向上させます。 拡張機能では、Google Authenticator、Authy、[!DNL Duo]、U2F キーなど、複数の認証をサポートしています。 この認証は、管理者ユーザーにのみ適用されます。 ストアフロントの顧客アカウントには使用できません。

これらの機能は、デフォルトで有効になっています。 各管理者ユーザーは、サポートされる認証者の 1 つをインストールして設定する必要があります。

>[!NOTE]
>
>管理者に対してAdobe Identity Management サービス（IMS）認証を有効にしているAdobe Commerce ストアでは、ネイティブのCommerce 2FA が無効になっています。 Adobe資格情報を使用して管理者にログインしているユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [Adobe Identity Management Service （IMS）統合の概要 ](./adobe-ims-integration-overview.md) を参照してください。

## インストールが必要なAdobe拡張機能

Adobeには、Composer を使用して個別にインストールする必要がある追加の拡張機能が用意されています。 これらの拡張機能は、様々なチャネルを通じて使用できます。

- リポジトリアクセス （repo.magento.com）

  次の拡張機能をインストールするには、アカウントのプロビジョニングと資格情報が必要です。 Adobe アカウント担当者にお問い合わせください。

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [CommerceのAEM Assets統合](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  次のAdobe拡張機能は、[marketplace.magento.com](https://marketplace.magento.com) で公開されてアクセスできます。 これらの拡張機能は、追加費用なしで利用できます。

   - [Live Search](#live-search)
   - [製品レコメンデーション](#product-recommendations)
   - [カタログサービス](#catalog-service)
   - [支払いサービス](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ。別のライセンスが必要です。

[!DNL Adobe Commerce B2B] は、標準的なCommerceのストアを、包括的な B2B プラットフォームに変換する統合拡張機能です。 これにより、企業は、統合された会社アカウントの下で、複数の購入者、カスタムの役割および購入権限を持つ複雑な組織構造を管理できます。 主な機能には、会社固有のカタログと価格、交渉可能な見積もり、発注管理、購買依頼リスト、クイックオーダー機能などがあります。 このソリューションは、1 つのインスタンスで B2B モデルと B2C モデルの両方をサポートしており、様々なビジネスニーズに柔軟に対応できます。 この拡張機能は個別のライセンスを必要とし、Adobe Commerceのコア機能とシームレスに統合して完全な B2B e コマースソリューションを提供します。

プロビジョニングについては、Adobe アカウント担当者にお問い合わせください。 実装の詳細と設定手順については、[[!DNL B2B for Adobe Commerce]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) を参照してください。

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ。Adobe Experience Manager（AEM）AssetsおよびAEM Dynamic Media のライセンスも必要です。

[!DNL AEM Assets Integration for Commerce] は、Adobe CommerceをAdobe Experience Managerの Digital Asset Management （DAM）システムと接続して、すべてのデジタルアセットを一元管理できるようにします。 この統合により、コマースストアフロント間でのアセットの自動同期、リアルタイムの更新、効率的なコンテンツの再利用が可能になります。 AEMの堅牢なアセット管理機能とCommerceを組み合わせることで、合理化されたワークフロー、一貫性のあるブランドエクスペリエンス、クラウドベースのインフラストラクチャによる最適化されたメディア配信のメリットが得られます。

プロビジョニングについては、Adobe アカウント担当者にお問い合わせください。 実装の詳細と設定手順については、[[!DNL Assets Integration]  ユーザーガイド ](../content-design/aem-assets-integration.md) を参照してください。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ

ライブ検索は、Adobe Commerce独自の機能で、AI を活用したリアルタイムの「好みに応じて検索」機能を備えた検索ソリューションを提供します。 買い物客が入力すると同時に、製品サムネールで迅速で関連性の高い結果が得られるほか、買い物行動に基づいてフィルターを自動的に調整するインテリジェントなファセット機能も備えています。 このソリューションには、製品のブーストと埋め込み、シノニム管理、検索分析のためのマーチャンダイジング機能が含まれています。 Adobe Commerceに無償で含まれる [!DNL Live Search] は、デフォルトの検索機能に代わって、より高度な SaaS ベースの検索エクスペリエンスが提供されます。 開始するには、最小限の設定が必要です。

実装の詳細と技術的要件については、[Live Search ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html) を参照してください。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ

[!DNL Product Recommendations] は、Adobe AI テクノロジーを活用したAdobe Commerce専用の機能で、カスタマージャーニーを通じてパーソナライズされた商品の提案を提供します。 このソリューションは、買い物客の行動と製品の関係をリアルタイムで分析し、関連するレコメンデーションを自動的に生成します。手動のマーチャンダイジングルールは必要ありません。 この AI 駆動のアプローチは、コンバージョン率と収益の可能性を高めると同時に、買い物客に対してより魅力的な製品発見エクスペリエンスを作成するのに役立ちます。

実装の詳細とベストプラクティスについては、[[!DNL Product Recommendations]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html) を参照してください。

### [!DNL Catalog Service]

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}Adobe CommerceおよびMagento Open Sourceのインストール

[!DNL Catalog Service] は、Adobe CommerceおよびGraphQL用の高性能ソリューションであり、Magento Open Source エンドポイントを介したカタログデータへの最適化されたアクセスを提供します。 製品の詳細および関連情報について、別個の同期済みデータベースを維持し、直接のアプリケーション通信をバイパスして、ページの読み込み時間を短縮します。 このサービスは、製品詳細ページ、カテゴリリスト、検索結果ページで特に価値が高く、従来のコマース実装とヘッドレスコマース実装の両方に最適です。

セットアップ手順と技術的な詳細については、[[!DNL Catalog Service]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html) を参照してください。

>[!NOTE]
>
>カタログサービスは、ライブ検索または製品レコメンデーションが有効な場合に自動的にインストールされます。 手動でのインストールは不要です。

### [!DNL Payment Services]

[!BADGE  サポート対象 ]{type=Informative tooltip="サポート"}Adobe CommerceおよびMagento Open Sourceのインストール

[!DNL Payment Services] は、Adobe CommerceおよびMagento Open Sourceの店舗に対するターンキー支払いソリューションで、包括的な支払い処理機能を提供します。 このサービスは、安全な支払いゲートウェイ機能と組み込みの不正防止を統合し、クレジット/デビットカード、PayPal、Venmo （米国）、PayLater プランなど、複数の支払いオプションを提供します。 Commerce Admin インターフェイスを介した統合トランザクションレポートと注文管理が備わっているので、マーチャントは支払いの追跡、キャッシュフローの管理、財務データの調整を 1 か所で簡単に行えます。

設定手順と支払いオプションについて詳しくは、[[!DNL Payment Services]  ユーザーガイド ](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview) を参照してください。
