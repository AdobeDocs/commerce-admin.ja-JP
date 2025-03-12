---
title: Adobeの拡張機能
description: AdobeがリリースしたAdobe CommerceおよびMagento Open Sourceの拡張機能に関する情報を確認します。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Adobeの拡張機能

ここでは、AdobeでリリースされたAdobe CommerceおよびMagento Open Sourceの拡張機能について説明します。 拡張機能は、管理およびストアフロントに機能、機能、サービスおよび統合を追加します。 これらの拡張機能の一部は、Magento Open Source コミュニティのコントリビューションを通じて開発されています。 一部の拡張機能は個別にインストールする必要があり、それ以外はデフォルトでインストールされます。

## インストールされた拡張機能

Adobe CommerceまたはMagento Open Sourceと共に自動的にインストールされる拡張機能もあります。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) は、同時チェックアウト保護および出荷照合アルゴリズムにより、1 つまたは複数の場所および販売チャネルにわたる在庫および出荷管理を強化します。 在庫数量を追跡し、正確な販売可能な在庫金額を顧客に提供し、レコメンデーションまたは手動の選択に従って出荷して、在庫全体を管理します。 ソースごと、製品ごとにグローバルに管理設定を構成します。

>[!NOTE]
>
>この拡張機能は、[[!DNL Inventory Management]](https://github.com/magento/inventory) （旧称 MSI）プロジェクトの一環として、コミュニティエンジニアリングプログラムを通じて開発されました。

[!DNL Inventory Management] は、デフォルトですべての機能が有効な状態でインストールされます。 これらのインベントリ機能を有効にするために必要な追加手順はありません。 [!DNL Inventory Management] の機能について詳しくは、[[!DNL Inventory Management]  ユーザーガイド ](../inventory-management/guide-overview.md) を参照してください。

### Braintree

PayPal と Gene Commerceは共同で、Commerce 2.4.x ストア向けの公式Braintree拡張機能を開発しました。 コンバージョンを促進するように設計された改善されたチェックアウトエクスペリエンスを備えたこのアップデートには、ショッピング中およびチェックアウト中に消費者に関連する PayLater メッセージおよびボタンを自動的に表示する PayLater オプションが含まれています。

この拡張機能はデフォルトでインストールされますが、ストアで [Braintree アカウントと ](https://www.braintreepayments.com/) 管理者の設定が有効になっている必要があります。 Braintreeを使用して取引を処理する際に発生する手数料を確認するには、[Braintreeの価格 ](https://www.braintreepayments.com/braintree-pricing) を確認してください。

管理者のBraintree設定について詳しくは、_セールスおよび購入エクスペリエンスガイド_ の [Braintree](../stores-purchase/braintree.md) に関するトピックを参照してください。

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

## 追加する拡張機能

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/) は、強力な新機能を備えたソリューションを拡張するアプリケーションおよびサービス [!DNL Commerce] グローバル e コマースリソースです。 Adobeでは、Adobe CommerceまたはMagento Open Source ストア内でインストールおよび設定して、統合と機能を強化できる拡張機能を [!DNL Marketplace] を通じてリリースしています。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ

[!DNL Live Search] 拡張機能は、ストアをAdobe Commerceの無料検索プラットフォームである Live Search サービスに接続して、セラーが AI を強化した検索エクスペリエンスをシームレスに提供できるようにします。 Adobeの人工知能とAdobe Senseiで構築されたインテリジェントファセットは、ファセットやフィルタリングに関する手作業を排除することで、マーチャントがより少ない労力でより多くの作業を行うのに役立ちます。

詳しくは、[ ライブ検索ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html) を参照してください。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceのみ

[!DNL Product Recommendations] 拡張機能は、ストアを Product Recommendations サービスに接続します。これは、コンバージョン、売上高、エンゲージメントを向上させるために使用できる強力なマーケティングツールです。 [!DNL Product Recommendations] はAdobe Commerceによって構築され、戦闘でテストされた人工知能であるAdobe Senseiによって推進されているため、自信を持ってエンゲージメントとコンバージョンを推進できます。 この機能により、すべての買い物客に適切な製品レコメンデーションを行うために必要な手動の作業が不要になります。

詳しくは、『 [[!DNL Product Recommendations]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en) を参照してください。

### [!DNL Catalog Service]

[!DNL Catalog Service] を使用すると、パフォーマンスの向上、スケーラビリティの向上、コンバージョンの増加を図りながら、最適化された製品エクスペリエンスを顧客に提供できます。 詳しくは、『 [[!DNL Catalog Service]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html) を参照してください。

### [!DNL Payment Services]

Adobe CommerceおよびMagento Open Source向け [!DNL Payment services] は、支払い管理のプロセスを簡素化し、お客様が自ら進んで支払いを行える、完全に統合された支払いソリューションです。 Adobe Commerce Admin 内のすべての支払いと取引データを安全に紐付けします。これにより、注文と支払いを 1 か所で管理しながら、シームレスなチェックアウトを実現できます。 詳しくは、『 [[!DNL Payment Services]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html) を参照してください。

### [!DNL Store Fulfillment]

Adobe CommerceおよびMagento Open Source向けのストアフルフィルメントでは、モバイルデバイスを通じて可能になる包括的なフルフィルメントワークフローを提供することで、優れたオンライン購入、店舗での集荷（BOPI）カスタマーエクスペリエンスを実現し、従業員の生産性を最大化します。 詳しくは、『 [[!DNL Store Fulfillment]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html) を参照してください。

### [!DNL Amazon Sales Channel]

Adobe Commerceの [!DNL Amazon Sales Channel] を使用すると、Amazon Seller Central のリストデータベースを [!DNL Commerce] の商品カタログと統合し、Commerce Admin でAmazonのリストと売上を管理できます。 詳しくは、『 [[!DNL Amazon Sales]  ガイドユーザーガイド ](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) を参照してください。

### [!DNL Channel Manager]

[!DNL Channel Manager] を使用すると、Adobe CommerceまたはMagento Open Sourceの商品カタログをウォルマートのマーケットプレイスと統合することで、売上高の増加、新規顧客へのリーチ、運営の合理化、時間の節約を実現できます。 拡張機能をインストールして設定した後、スタッフは Walmart Marketplace のリスト、在庫、注文、返品、払い戻しを [!DNL Commerce Admin] からシームレスに管理できます。 詳しくは、『 [[!DNL Channel Manager]  ユーザーガイド ](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) を参照してください。
