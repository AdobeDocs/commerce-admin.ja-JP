---
title: Adobeからの拡張機能
description: Adobe Commerceの拡張機能と、AdobeがリリースしたMagento Open Sourceに関する情報を確認します。
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Adobeからの拡張機能

ここでは、Adobe Commerceの拡張機能とAdobeがリリースしたMagento Open Sourceについて説明します。 拡張機能は、管理およびストアフロントに機能、機能、サービスおよび統合を追加します。 これらの拡張機能の一部は、Magento Open Sourceコミュニティのコントリビューションを通じて開発されています。 一部の拡張機能は個別にインストールする必要があり、それ以外はデフォルトでインストールされます。

## インストールされた拡張機能

Adobe CommerceまたはMagento Open Sourceと共に自動的にインストールされる拡張機能もあります。

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) は、同時チェックアウト保護および出荷照合アルゴリズムにより、1 つまたは複数の場所および販売チャネルにわたる在庫および出荷管理を強化します。 在庫数量を追跡し、正確な販売可能な在庫金額を顧客に提供し、レコメンデーションまたは手動の選択に従って出荷して、在庫全体を管理します。 ソースごと、製品ごとにグローバルに管理設定を構成します。

>[!NOTE]
>
>この拡張機能は、 [[!DNL Inventory Management]](https://github.com/magento/inventory) （旧称 MSI）は、コミュニティエンジニアリングプログラムを通じてプロジェクトを行います。

[!DNL Inventory Management] は、デフォルトですべての機能が有効になっている状態でインストールされます。 これらのインベントリ機能を有効にするために必要な追加手順はありません。 について [!DNL Inventory Management] 機能については、を参照してください [[!DNL Inventory Management] ユーザーガイド](../inventory-management/guide-overview.md).

### Braintree

PayPal と Gene Commerceは共同で、Commerce 2.4.x ストア向けの公式Braintree拡張機能を開発しました。 コンバージョンを促進するように設計された改善されたチェックアウトエクスペリエンスを備えたこのアップデートには、ショッピング中およびチェックアウト中に消費者に関連する PayLater メッセージおよびボタンを自動的に表示する PayLater オプションが含まれています。

この拡張機能はデフォルトでインストールされますが、には [Braintreeアカウント](https://www.braintreepayments.com/) および管理者の設定を有効にして、ストアで使用できるようにします。 Braintreeを使用して取引を処理する際に発生する手数料を確認するには、 [Braintree価格](https://www.braintreepayments.com/braintree-pricing).

管理者のBraintree設定については、を参照してください [Braintree](../stores-purchase/braintree.md) のトピック _販売および購入エクスペリエンスガイド_.

### Google reCAPTCHA

Google reCAPTCHA は、標準の CAPTCHA よりも高いレベルのセキュリティをストアフロントと管理 UI に提供し、以下の機能を提供します。

- 顧客がいつアカウントを作成するか、パスワードを取得するか、顧客のアカウントにログインするか、または会社に問い合わせるかを確認します。
- 管理者ユーザーがログインしたときのセキュリティを強化します。

これにより、Captcha コードを入力する際に発生する可能性のあるユーザーエラーを減らし、チェックアウト時にハードルを追加することなく、買い物かごへのコンバージョンを促すことができます。 [reCAPTCHA の有効化と設定](../systems/security-google-recaptcha.md) 目に見えないチェックや対話型チェックを使用して、への安全なアクセスを強化する [!DNL Commerce] 管理およびストアフロント。

### 二要素認証

この [!DNL Commerce] 管理者は、ストア、注文および顧客データへのすべてのアクセスを提供します。 [二要素認証](../systems/security-two-factor-authentication.md) （2FA または TFA）の場合、標準のログイン名とパスワード以外の追加の認証を要求してにアクセスできるため、セキュリティが向上します。 [!DNL Commerce] すべてのデバイスから管理します。 この拡張機能は、Google Authenticator、Authy、 [!DNL Duo]、および U2F キー この認証は、管理者ユーザーにのみ適用されます。 ストアフロントの顧客アカウントには使用できません。

これらの機能は、デフォルトで有効になっています。 各管理者ユーザーは、サポートされる認証者の 1 つをインストールして設定する必要があります。

>[!NOTE]
>
>管理者のAdobe Identity Management サービス（IMS）認証を有効にしているAdobe Commerce ストアでは、ネイティブのCommerce 2FA が無効になっています。 Adobe資格情報を使用して管理者にログインしているユーザーは、多くの管理タスクで再認証の必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 参照： [AdobeIdentity Management サービス（IMS）の統合の概要](./adobe-ims-integration-overview.md).

## 追加する拡張機能

この [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) は、拡大するアプリケーションおよびサービスのグローバル e コマースリソースです [!DNL Commerce] 強力な新機能を備えたソリューション。 Adobeは、 [!DNL Marketplace] Adobe CommerceまたはMagento Open Sourceストア内にインストールおよび設定して、より高度な統合および機能を提供できます。

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

この [!DNL Live Search] この拡張機能により、店舗がAdobe Commerceの無料検索プラットフォームである Live Search サービスに接続され、セラーは AI を強化した検索エクスペリエンスをシームレスに提供できるようになります。 Adobeの人工知能で構築されたAdobe Senseiは、ファセットやフィルタリングに関する手作業をなくすことで、マーチャントがより少ない労力でより多くの作業を行うのに役立ちます。

を参照してください。 [ライブ検索ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) を参照してください。

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceのみ

この [!DNL Product Recommendations] extension は、ストアを Product Recommendations サービスに接続します。これは、コンバージョン、売上高、エンゲージメントを向上させるために使用できる強力なマーケティングツールです。 [!DNL Product Recommendations] はAdobe Commerceによって構築され、その戦いでテストされた人工知能Adobe Senseiによって駆動されているので、自信を持ってエンゲージメントとコンバージョンを推進できます。 この機能により、すべての買い物客に適切な製品レコメンデーションを行うために必要な手動の作業が不要になります。

を参照してください。 [[!DNL Product Recommendations] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) を参照してください。

### [!DNL Catalog Service]

この [!DNL Catalog Service] を使用すると、パフォーマンスを向上させ、スケーラビリティを向上させ、コンバージョンを増やしながら、最適化された製品エクスペリエンスを顧客に提供できます。 を参照してください。 [[!DNL Catalog Service] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) を参照してください。

### [!DNL Payment Services]

[!DNL Payment services] Adobe CommerceとMagento Open Sourceは、支払いを管理するプロセスを簡素化し、お客様が自分で支払いを行える機会を提供する、完全に統合された支払いソリューションです。 Adobe Commerce Admin 内のすべての支払いと取引データを安全に紐付けします。これにより、注文と支払いを 1 か所で管理しながら、シームレスなチェックアウトを実現できます。 を参照してください。 [[!DNL Payment Services] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) を参照してください。

### [!DNL Store Fulfillment]

Adobe CommerceおよびMagento Open Source向けのストアフルフィルメントは、モバイルデバイスを通じて可能になる包括的なフルフィルメントワークフローを提供することで、優れたオンライン購入、店舗での集荷（BOPIS）カスタマーエクスペリエンスを実現し、従業員の生産性を最大限に高めます。 を参照してください。 [[!DNL Store Fulfillment] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) を参照してください。

### [!DNL Amazon Sales Channel]

この [!DNL Amazon Sales Channel] Adobe Commerceの場合、Amazon Seller Central リストデータベースを [!DNL Commerce] 製品カタログを参照し、Commerce Admin でAmazonのリストや売上を管理します。 を参照してください。 [[!DNL Amazon Sales] ガイドユーザーガイド](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) を参照してください。

### [!DNL Channel Manager]

[!DNL Channel Manager] を使用すると、Adobe CommerceまたはMagento Open Sourceの商品カタログをウォルマートのマーケットプレイスと統合することで、売上高の増加、新規顧客へのリーチ、運営の合理化、時間の節約を実現できます。 拡張機能をインストールして設定した後、スタッフは Walmart Marketplace のリスト、在庫、注文、返品、返金をシームレスにから管理できます [!DNL Commerce Admin]. を参照してください。 [[!DNL Channel Manager] ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) を参照してください。
