---
title: '[!DNL Adobe Commerce Marketplace]'
description: について説明します [!DNL Commerce Marketplace]は、マーチャントに厳選されたソリューションを提供し、適格な開発者に活発なビジネスを構築するためのツール、プラットフォーム、主要な場所を提供します。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] は、マーチャントに厳選されたソリューションを提供し、適格な開発者に活発なビジネスを構築するためのツール、プラットフォーム、主要な場所を提供するアプリケーションストアです。 [!DNL Commerce Marketplace] は、無料で利用可能な拡張機能と、販売されているその他の拡張機能を提供します。 購入はクレジットカードまたは [PayPal][2].

で利用できるすべての拡張機能 [!DNL Commerce Marketplace] 大々的な見直しに合格した。 この [拡張機能品質プログラム][3] （EQP）は、 [!DNL Commerce] Commerce Marketplace上のすべての拡張機能がコーディング標準とベストプラクティスを満たしていることを確認するための専門知識、開発ガイドライン、検証ツール。 レビュープロセスには、自動チェックと手動 QA レビューの両方が含まれます。 このプロセスでは、各拡張機能の構造とコードが検査され、ウイルス/マルウェア感染の証拠や盗用の兆候がないかテストされます。 このレビューには、詳細な技術調査と、 [!DNL Commerce] エンジニア：ドキュメント、コーディング構造、パフォーマンス、スケーラビリティ、セキュリティ、との互換性を重視 [!DNL Commerce] コア。

他のソースから拡張機能を購入できますが、で利用できる拡張機能のみです [!DNL Commerce Marketplace] は、拡張機能品質プログラム内の広範な技術的およびマーケティングレビューを通じて検証されます。

## アプリリソース

開発者は伝統的に PHP を使用して、Adobe Commerceに機能、機能、サービス、および統合を加えるプロセス内拡張機能を作成してきました。 拡張機能ではなく、プロセス外の拡張機能を備えたアプリを作成することで、互換性の問題を回避できます。

次のリソースは、新規採用者がアプリを習熟するための出発点となります。

### Commerce リソース：

- [Adobe Commerceの I/O イベントの設定](https://developer.adobe.com/commerce/extensibility/events/)
- [Adobe Commerceのイベントの設定](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [管理 UI SDK のセットアップ](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [拡張機能のアプリへの変換](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder リソース：

- [Commerce App Builder の概要](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Adobe Developer App Builder の API メッシュの設定](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder アプリのデプロイ](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder アプリ用の CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/Developer Console の概要
   - [App Builder の概要](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [プロジェクトとワークスペースについて](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 資格情報

から購入した拡張機能をインストールする前に [!DNL Commerce Marketplace]、にログイン [!DNL Commerce] アカウントを作成し、アクティブなアクセスキーがあることを確認します。 にログインできます [!DNL Commerce] のヘッダーからのアカウント [[!DNL Marketplace]][1] または [Magento.com][6].

アクセスキーは、の同期に使用される公開鍵と秘密鍵のセットです [!DNL Commerce] を使用したインストール [!DNL Commerce] アカウントを設定し、資格情報を検証します。 アカウントが同期されると、Commerce Marketplaceから拡張機能やモジュールをインストールしたり、をアップグレードしたりするたびに、秘密鍵を入力する必要があります [!DNL Commerce] インストール。

目的に応じて複数のアクセスキーを作成し、必要に応じて有効または無効にすることができます。 ただし、のインストールに使用したものと同じアクセスキーを使用する必要があります [!DNL Commerce] ソフトウェア。 例えば、Magento Open Sourceアクセスキーを使用してAdobe Commerceを更新またはアップグレードすることはできません。逆も同様です。 別のユーザーに属するアクセスキーや、 [共有アカウント](commerce-account-share.md).

### アクセスキーの作成

1. にログイン [!DNL Commerce] アカウント。

1. 日 _[!UICONTROL My Account]_ページで、**[!UICONTROL Marketplace]**タブ。

1. 名前の横の右上隅にある下向き矢印をクリックし、 **[!UICONTROL My Profile]**.

   ![あなたの [!DNL Marketplace] profile](./assets/marketplace-profile.png){width="600"}

1. 日 _[!UICONTROL Marketplace]_タブの下_[!UICONTROL My Products]_&#x200B;を選択し、 **[!UICONTROL Access Keys]**&#x200B;次に、次のいずれかの操作を行います。

   - Marketplace での購入に使用できるアクセス キーのセットが既にあるかどうかを確認します。 目的に応じて、複数のアクセスキーのセットを作成できます。

   ![アクセスキー](./assets/access-keys.png){width="600"}

   - クリック **[!UICONTROL Create a New Access Key]**. 新しいキーペアの名前を入力し、 **[!UICONTROL OK]**. 有効な文字には、大文字と小文字、スペースではなくハイフンがあります。

1. 完了したら、 **[!UICONTROL OK]**.

   新しいアクセスキーが有効になり、リストに表示されます。

   に注意してください。 _コピー_ 公開鍵と秘密鍵ごとにリンクします。 次の手順では、これらの値をコピーして貼り付け、ストアをCommerce Marketplaceと同期させます。

## インストールプロセス

>[!IMPORTANT]
>
>Adobe CommerceおよびMagento Open Source 2.4.0 以降では、web セットアップウィザードは削除されるので、コマンドラインを使用して次の操作を行う必要があります [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) または [アップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) お使いのインスタンス。 この要件には、次も含まれます [モジュール](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) および [拡張機能](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

のインストールプロセス [!DNL Marketplace] 購入額は、次の品目で異なります _オンプレミス_ にホストされたインストールの場合とは異なるCommerceのインストール [Adobeクラウドアーキテクチャ][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## サポート

拡張機能のインストールや使用に関するヘルプが必要な場合は、まず拡張機能に付属するドキュメントを参照してください。 質問の回答が見つからない場合は、拡張機能リストの連絡先情報を使用して、開発者に直接問い合わせてください。

Commerce Marketplaceで購入したものがニーズを満たさない場合は、購入日から 25 日以内に払い戻しをリクエストできます。 Adobeはすべての返金リクエストを確認し、承認された場合は適切な返金を行います。

Commerce Marketplaceに関するサポートの問題については、を参照してください。 [[!DNL Marketplace] ヘルプセンター][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
