---
title: Adobeからの拡張
description: Adobe Commerceの拡張機能と、AdobeがリリースしたMagento Open Sourceに関する情報を確認します。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: c22ad5c3220f14588131d6b29a88dab3c5347681
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Adobeからの拡張

このトピックでは、Adobe Commerceの拡張機能と、AdobeがリリースしたMagento Open Sourceに関する情報を提供します。 拡張機能は、機能、機能、サービス、統合を管理者やストアフロントに追加します。 これらの拡張機能の一部は、Magento Open Sourceコミュニティの投稿を通じて開発されます。 一部の拡張機能は別個のインストールが必要です。それ以外の拡張機能はデフォルトでインストールされます。

## インストール済みの拡張機能

一部の拡張機能は、Adobe CommerceまたはMagento Open Sourceと共に自動的にインストールされます。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) は、1 つまたは複数の場所と販売チャネルにわたる在庫と出荷の管理を強化し、同時チェックアウト保護および出荷照合アルゴリズムを使用して提供します。 在庫数量を追跡し、顧客に正確な販売可能な在庫量を提供し、在庫全体を管理するための推奨または手動選択に従って出荷します。 管理設定をグローバルに、ソースごと、および製品ごとに設定します。

>[!NOTE]
>
>この拡張機能は、 [[!DNL Inventory Management]](https://github.com/magento/inventory) （旧称 MSI）コミュニティエンジニアリングプログラムを通じてプロジェクトを行います。

[!DNL Inventory Management] は、すべての機能を既定で有効にしてインストールします。 これらのインベントリ機能を有効にするために追加の手順は必要ありません。 詳しくは、 [!DNL Inventory Management] 機能 (「 [[!DNL Inventory Management] ユーザーガイド](../inventory-management/guide-overview.md).

### Braintree

PayPal と Gene Commerce は共に、コマース 2.4.x 店舗の公式Braintree拡張を開発しました。 コンバージョンを促進するために設計されたチェックアウトエクスペリエンスを強化した機能を備えたアップデートには、買い物中やチェックアウト中に、関連する PayLater メッセージとボタンを消費者に自動的に表示する PayLater オプションが含まれます。

この拡張機能はデフォルトでインストールされますが、にはが必要です。 [Braintreeアカウント](https://www.braintreepayments.com/) および設定を管理者に送信して、ストアに対して有効にします。 トランザクションの処理にBraintreeを使用する場合に適用される手数料を決定するには、 [Braintree価格](https://www.braintreepayments.com/braintree-pricing).

管理でのBraintree設定について詳しくは、 [Braintree](../stores-purchase/braintree.md) トピック _セールスおよび購入エクスペリエンスガイド_.

### Google reCAPTCHA

Google reCAPTCHA は、ストアフロントと管理 UI の両方に対して、標準の CAPTCHA よりも高いセキュリティレベルを提供し、次の機能を提供します。

- 顧客がアカウントを作成したり、パスワードを取得したり、アカウントにログインしたり、会社に問い合わせたりするタイミングを確認します。
- 管理者ユーザーがログインした際のセキュリティを強化します。

Captcha コードを入力する際のユーザーエラーの可能性を減らし、チェックアウト時にハードルを追加することなく、買い物かごのコンバージョンを促します。 [reCAPTCHA の有効化と設定](../systems/security-google-recaptcha.md) 目に見えない、またはインタラクティブなチェックを使用して、 [!DNL Commerce] 管理者とストアフロント。

### 二段階認証

The [!DNL Commerce] 管理者は、ストア、注文、顧客データへのすべてのアクセスを提供します。 [二段階認証](../systems/security-two-factor-authentication.md) （2FA または TFA）は、標準のログイン名やパスワードを超えて、 [!DNL Commerce] すべてのデバイスから管理者。 この拡張機能は、Google Authenticator、Authy、 [!DNL Duo]、および U2F キー。 この認証は、管理者ユーザーにのみ適用されます。 ストアフロントの顧客アカウントには使用できません。

これらの機能は、デフォルトで有効になっています。 各管理者ユーザーは、サポートされている認証子の 1 つをインストールして構成する必要があります。

>[!NOTE]
>
>管理者に対してAdobeIdentity Management Services(IMS) 認証を有効にしたAdobe Commerceストアでは、ネイティブの Commerce 2FA が無効になっています。 ユーザーの資格情報を使用して管理者にログインしているAdobeは、多くの管理者タスクを再認証する必要はありません。 認証は、管理者Adobe IMSが現在のセッションにログインする際にユーザーによって処理されます。 詳しくは、 [AdobeIdentity Managementサービス (IMS) 統合の概要](./adobe-ims-integration-overview.md).

## 追加する拡張機能

The [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) は、拡大するアプリケーションやサービス向けのグローバルな e コマースリソースです。 [!DNL Commerce] 強力な新機能と機能を備えたソリューション Adobeは、 [!DNL Marketplace] Adobe CommerceまたはMagento Open Sourceストア内にインストールおよび設定して、統合と機能を強化できます。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

The [!DNL Live Search] 拡張機能は、ストアをAdobe Commerceの無料検索プラットフォーム（AI で強化された検索機能を販売者にシームレスに提供する、の無料検索サービス）に接続します。 Adobeの人工知能を使用して構築されたAdobe Sensei、インテリジェントファセッティングは、ファセットやフィルタリングに関する手動作業を削除することで、より少ない手間でより多くの作業を行うのに役立ちます。

詳しくは、 [ライブ検索ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) を参照してください。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

The [!DNL Product Recommendations] 拡張機能は、ストアを Product Recommendationsサービスに接続します。これは、コンバージョン、売上高、エンゲージメントを増やすために使用できる強力なマーケティングツールです。 [!DNL Product Recommendations] Adobe Commerceが構築し、戦いのテストを受けた人工知能Adobe Senseiが原因で、エンゲージメントとコンバージョンを自信を持って推進できます。 この機能により、すべての買い物客に対して関連製品のレコメンデーションをおこなうのに必要な手動作業を削除できます。

詳しくは、 [[!DNL Product Recommendations] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) を参照してください。

### [!DNL Catalog Service]

The [!DNL Catalog Service] を使用すると、最適化された製品エクスペリエンスを提供しながら、パフォーマンスを向上させ、拡張性を向上させ、コンバージョンを増やすことができます。 詳しくは、 [[!DNL Catalog Service] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) を参照してください。

### [!DNL Payment Services]

[!DNL Payment services] Adobe CommerceとMagento Open Sourceは、支払い管理プロセスを簡素化し、顧客が支払いを行う機会を提供する完全統合支払いソリューションです。 Adobe Commerce Admin 内ですべての支払いとトランザクションデータを安全に紐付けし、シームレスなチェックアウトを提供しながら、注文と支払いを 1 か所で管理できます。 詳しくは、 [[!DNL Payment Services] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) を参照してください。

### [!DNL Quick Checkout]

[!DNL Quick Checkout] Adobe Commerceは、1 回限りのゲスト買い物客を常連のアカウント所有者に変換するための、シームレスなチェックアウトエクスペリエンスを強化します。
詳しくは、 [[!DNL Quick Checkout] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/quick-checkout/overview.html) を参照してください。

### [!DNL Store Fulfillment]

Adobe CommerceとMagento Open Source向けのストアフルフィルメントは、優れたオンライン購入を可能にし、ストア (BOPIS) での顧客体験を提供し、モバイルデバイスを通じて可能な包括的なフルフィルメントワークフローを提供し、従業員の生産性を最大化します。 詳しくは、 [[!DNL Store Fulfillment] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) を参照してください。

### [!DNL Amazon Sales Channel]

The [!DNL Amazon Sales Channel] Adobe Commerceの場合は、Amazonセラーセントラルリストデータベースを [!DNL Commerce] 商品カタログを開き、コマース管理でAmazonの一覧と販売を管理します。 詳しくは、 [[!DNL Amazon Sales] ガイドユーザガイド](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) を参照してください。

### [!DNL Channel Manager]

[!DNL Channel Manager] Adobe CommerceまたはMagento Open Sourceの製品カタログを Walmart Marketplace に統合することで、売上高の増加、新規顧客へのリーチ、運用の合理化、時間の節約を実現します。 拡張機能をインストールして設定すると、スタッフは Walmart Marketplace のリスト、在庫、注文、返品、返金を [!DNL Commerce Admin]. 詳しくは、 [[!DNL Channel Manager] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) を参照してください。
