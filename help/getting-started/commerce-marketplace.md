---
title: '[!DNL Adobe Commerce Marketplace]'
description: マーチャントに厳選されたソリューションを提供し、適格な開発者に活発なビジネスを構築するためのツール、プラットフォーム、主要な場所を提供する  [!DNL Commerce Marketplace] について説明します。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace](https://marketplace.magento.com/) は、マーチャント向けに厳選されたソリューションを提供するアプリケーションストアです。資格のあるデベロッパー向けに、活発なビジネスを構築するためのツールやプラットフォームを提供します。 [!DNL Commerce Marketplace] には、無料で利用できる拡張機能と、販売されるその他の拡張機能が用意されています。 購入はクレジットカードまたは [PayPal](https://www.paypal.com/us/home) で支払うことができます。

[!DNL Commerce Marketplace] で利用可能なすべての拡張機能は、包括的なレビューに合格しています。 [Extension Quality Program](https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/) （EQP）は、Commerce Marketplace上のすべての拡張機能がコーディング標準とベストプラクティスを確実に満たすよ [!DNL Commerce] に、専門知識、開発ガイドライン、検証ツールを組み合わせたものです。 レビュープロセスには、自動チェックと手動 QA レビューの両方が含まれます。 このプロセスでは、各拡張機能の構造とコードが検査され、ウイルス/マルウェア感染の証拠や盗用の兆候がないかテストされます。 このレビューには、[!DNL Commerce] エンジニアによる詳細な技術調査と健全性チェックが含まれています。ここでは、ドキュメント、コーディング構造、パフォーマンス、スケーラビリティ、セキュリティ、[!DNL Commerce] コアとの互換性に重点を置いて行われます。

他のソースから拡張機能を購入できますが、[!DNL Commerce Marketplace] で使用可能な拡張機能のみが、拡張機能品質プログラム内の広範な技術およびマーケティングレビューを通じて検証されます。

## アプリリソース

開発者は伝統的に PHP を使用して、Adobe Commerceに機能、機能、サービス、および統合を加えるプロセス内拡張機能を作成してきました。 拡張機能ではなく、プロセス外の拡張機能を備えたアプリを作成することで、互換性の問題を回避できます。

次のリソースは、新規採用者がアプリを習熟するための出発点となります。

### Commerce リソース

- [Adobe Commerceの I/O イベントの設定 &#x200B;](https://developer.adobe.com/commerce/extensibility/events/)
- [Adobe Commerceのイベントの設定 &#x200B;](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [&#x200B; 管理 UI SDKのセットアップ &#x200B;](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [&#x200B; 拡張機能のアプリへの変換 &#x200B;](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder リソース

- [Commerce App Builderの概要 &#x200B;](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Adobe Developer App Builderの API メッシュの設定 &#x200B;](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder アプリのデプロイ &#x200B;](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder アプリの CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/Developer Consoleの概要
   - [App Builderの概要 &#x200B;](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [&#x200B; プロジェクトとワークスペースについて &#x200B;](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 資格情報

[!DNL Commerce Marketplace] から購入した拡張機能をインストールする前に、[!DNL Commerce] アカウントにサインインし、アクティブなアクセスキーがあることを確認します。 [!DNL Commerce][[!DNL Marketplace] または &#x200B;](https://marketplace.magento.com/)Magento.com[&#x200B; のヘッダーから &#x200B;](https://business.adobe.com/products/magento/magento-commerce.html) アカウントにログインできます。

アクセスキーは、[!DNL Commerce] インストールを [!DNL Commerce] アカウントと同期し、資格情報を検証するために使用される、一連の公開鍵と秘密鍵です。 アカウントが同期されると、Commerce Marketplaceから拡張機能やモジュールをインストールしたり、[!DNL Commerce] インストールをアップグレードしたりするたびに、秘密鍵を入力する必要があります。

目的に応じて複数のアクセスキーを作成し、必要に応じて有効または無効にすることができます。 ただし、[!DNL Commerce] ソフトウェアのインストールに使用したのと同じアクセス キーを使用する必要があります。 例えば、Magento Open Source アクセスキーを使用してAdobe Commerceを更新またはアップグレードすることはできません。逆も同様です。 また、別のユーザーに属するアクセスキーや、（共有アカウント [&#x200B; からのアクセスキーは使用でき &#x200B;](commerce-account-share.md) せん。

### アクセスキーの作成

1. [!DNL Commerce] アカウントにログインします。

1. _[!UICONTROL My Account]_&#x200B;ページで、「**[!UICONTROL Marketplace]**」タブを選択します。

1. 名前の横の右上隅にある下向き矢印をクリックし、「**[!UICONTROL My Profile]**」を選択します。

   ![[!DNL Marketplace] プロファイル &#x200B;](./assets/marketplace-profile.png){width="600"}

1. [_[!UICONTROL Marketplace]_] タブの [_[!UICONTROL My Products]_] で [**[!UICONTROL Access Keys]**] をクリックし、次のいずれかの操作を行います。

   - Marketplace での購入に使用できるアクセス キーのセットが既にあるかどうかを確認します。 目的に応じて、複数のアクセスキーのセットを作成できます。

   ![&#x200B; アクセスキー &#x200B;](./assets/access-keys.png){width="600"}

   - 「**[!UICONTROL Create a New Access Key]**」をクリックします。 新しいキーペアの名前を入力し、「**[!UICONTROL OK]**」をクリックします。 有効な文字には、大文字と小文字、スペースではなくハイフンがあります。

1. 完了したら、「**[!UICONTROL OK]**」をクリックします。

   新しいアクセスキーが有効になり、リストに表示されます。

   各公開鍵と秘密鍵の後に _コピー_ リンクがあることに注意してください。 次の手順では、これらの値をコピーして貼り付け、ストアをCommerce Marketplaceと同期します。

## インストールプロセス

>[!IMPORTANT]
>
>Adobe CommerceおよびMagento Open Source 2.4.0 以降では、web セットアップウィザードは削除されるので、コマンドラインを使用してインスタンスを [&#x200B; インストール &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) または [&#x200B; アップグレード &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) する必要があります。 この要件には、[&#x200B; モジュール &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) および [&#x200B; 拡張機能 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) も含まれます。

[!DNL Marketplace] の購入のインストールプロセスは、Adobeの _オンプレミス_ インストールと、Commerce クラウドアーキテクチャ [&#x200B; でホストされるインストールでは異な &#x200B;](https://www.adobe.com/commerce/magento/enterprise.html) ます。

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## サポート

拡張機能のインストールや使用に関するヘルプが必要な場合は、まず拡張機能に付属するドキュメントを参照してください。 質問の回答が見つからない場合は、拡張機能リストの連絡先情報を使用して、開発者に直接問い合わせてください。 Marketplace で購入したものがニーズを満たさない場合は、購入日から 25 日以内に [&#x200B; 払い戻しをリクエスト &#x200B;](#refund-requests) できます。 Adobeは、すべての払い戻しリクエストを確認し、（承認された場合は）適切な払い戻しを発行します。 Commerce Marketplaceに関連する問題の場合：

方法 1: [Adobe Commerce Marketplace からサポートリクエストを送信する – お問い合わせ &#x200B;](https://commercemarketplace.adobe.com/contact-us/) フォーム。

方法 2:[&#x200B; メールサポート &#x200B;](mailto:commercemarketplacesupport@adobe.com)。

### チェックアウトの問題

アカウントプロファイルのアドレスフィールドは、マーケットプレイス購入システムで検証するために入力する必要があります。

1. Marketplace アカウントプロファイルにアドレスフィールドを追加します。
1. 更新したプロファイルを保存します。
1. チェックアウトを続行します。

### ログインに関する問題

ログインの問題は、通常、MAGEID とアカウントデータベースのメールアドレスの不一致に関連しています。 サポートが必要な場合は、Marketplace サポートにお問い合わせください。

>[!INFO]
>
>アプリと拡張機能の購入は、新しいアカウントに [&#x200B; 転送 &#x200B;](#purchase-transfers) できません。

### オープンソースの質問

Marketplace サポートチームは、[commercemarketplace.adobe.com/](https://commercemarketplace.adobe.com/) および [commercedeveloper.adobe.com/](https://commercedeveloper.adobe.com/) サイトに関連する問題のみを解決します。 Magento Open Sourceに関するご質問は、[&#x200B; コミュニティフォーラム &#x200B;](https://community.magento.com/) または [&#x200B; パートナーにお問い合わせください &#x200B;](https://business.adobe.com/products/magento/partners.html) パートナーはMagento Open Sourceを支援できます。

### 払戻要求

Marketplace での購入に対する返金をリクエストするには、アカウントにログインし、次の手順に従います。

1. [!UICONTROL **マイプロファイル**]/[!UICONTROL **購入履歴**] をクリックします。
1. 購入した商品を見つけて、「[!UICONTROL **返金をリクエスト**]」をクリックします。
1. 払い戻し注文フォームに入力します。

Marketplace サポートは、払い戻しリクエストが生成された後、情報をリクエストします。 払い戻しオプションは、購入日から 25 日間ご利用いただけます。 [Marketplace 顧客契約 &#x200B;](https://www.adobe.com/legal/terms/enterprise-licensing/magento-legacy-terms.html) を参照してください。

### 請求書の注文

注文請求書は、Marketplace アカウントの [!UICONTROL **購入履歴**] からダウンロードできます。 この請求書は、現時点では Marketplace の要件ではないため、販売者の VAT または住所を提供しません。

Marketplace での購入に対する注文請求書をダウンロードするには、Marketplace アカウントにログインして、次の手順に従います。

1. [!UICONTROL **マイプロファイル**]/[!UICONTROL **購入履歴**] をクリックします。
1. 購入を見つけます。
1. 注文の右上隅にあるプリンタアイコンをクリックします。

### 購買転送

Marketplace サポート チームには、購入を別のアカウントに転送する機能がありません。 インストールとデプロイメントの問題を回避するには、プライマリ Commerce アカウントですべてのアプリと拡張機能を購入する必要があります。 Adobe Commerceには、1 つの一意の ID が付与されます。 Composer はインストールに使用されるため、プライマリ アカウントに関連付けられた [&#x200B; アクセス キー &#x200B;](#create-an-access-key) のセットを 1 つだけ使用できます。 利用可能な唯一のソリューションは、Marketplace 購入アカウントから [&#x200B; 返金をリクエスト &#x200B;](#refund-requests) することです（Adobe Commerceの返金ポリシーで許可されている場合）。

プライマリアカウントを通じてCommerce インスタンスを [&#x200B; 共有 &#x200B;](commerce-account-share.md) できます。 共有アクセスでは、プライマリ・アカウントから下位アカウントに特別な権限が付与されます。 共有アクセス ポイントはプライマリ アカウントから生成されます。 プライマリ口座は、Commerceの権限付き口座、メインのマーチャントアカウント、組織内で共有される口座のいずれかです。

これらの特別な権限により、Adobe Commerceにプライマリと同じレベルのアクセス権が付与されますが、Adobe Commerce Marketplace や開発者ポータルには引き継がれません。 つまり、Marketplace の下位アカウントから拡張機能を購入しても、プライマリアカウントと共有することはできません。 共有アクセスは一方通行の通りです（従属するプライマリ アカウント）。 下位アカウントがプライマリに共有しようとする場合は機能しません。
