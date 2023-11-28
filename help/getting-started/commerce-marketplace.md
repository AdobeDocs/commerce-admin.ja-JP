---
title: '[!DNL Adobe Commerce Marketplace]'
description: 詳しくは、 [!DNL Commerce Marketplace]：マーチャントは厳選されたソリューションを提供し、適格な開発者に対して、成功するビジネスを構築するためのツール、プラットフォーム、主要な場所を提供します。
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce Marketplace

[Adobe Commerce Marketplace][1] は、厳選されたソリューションをマーチャントに提供し、適格な開発者に対して、ビジネスを成長させるためのツール、プラットフォーム、主要な場所を提供するアプリケーションストアです。 [!DNL Commerce Marketplace] は、無料で利用できる拡張機能や、販売する拡張機能の選択を提供します。 購入は、クレジットカードまたは [PayPal][2].

で使用できるすべての拡張機能 [!DNL Commerce Marketplace] 広範な調査に合格した The [拡張品質プログラム][3] (EQP) 結合 [!DNL Commerce] Commerce Marketplace上のすべての拡張機能がコーディング標準とベストプラクティスを確実に満たすようにするための専門知識、開発ガイドライン、検証ツール。 レビュープロセスには、自動チェックと手動 QA レビューの両方が含まれます。 プロセス中に、各拡張機能の構造とコードを調べ、ウイルス/マルウェア感染の証拠と、盗作の兆候を調べてテストします。 レビューには、 [!DNL Commerce] エンジニア、ドキュメント、コーディング構造、パフォーマンス、拡張性、セキュリティ、および [!DNL Commerce] コア。

他のソースから拡張機能を購入することはできますが、で使用できる拡張機能のみです [!DNL Commerce Marketplace] は、拡張機能品質プログラム内の広範な技術およびマーケティングのレビューを通じて検証されます。

## アプリのリソース

開発者は従来、PHP を使用してプロセス内拡張機能を作成し、Adobe Commerceに機能、機能、サービス、統合を追加してきました。 拡張機能とは異なり、プロセス外の拡張機能を使用してアプリを作成することで、互換性の問題を回避できます。

以下のリソースは、新しいアダプターがアプリに慣れるための出発点となります。

### コマースリソース：

- [Adobe Commerceの I/O イベントの設定](https://developer.adobe.com/commerce/extensibility/events/)
- [Adobe Commerce用のイベントの設定](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [Admin UI SDK の設定](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [拡張機能からアプリへの変換](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder のリソース：

- [Commerce App Builder の概要](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Adobe Developer App Builder の API メッシュの設定](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder アプリのデプロイ](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder アプリ用 CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/Developer Console 使用の手引き
   - [App Builder の概要](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [プロジェクトとワークスペースについて](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 資格情報

購入した拡張機能をインストールする前に [!DNL Commerce Marketplace]を使用し、 [!DNL Commerce] アカウントを作成し、アクティブなアクセスキーがあることを確認します。 以下のページにログインして、 [!DNL Commerce] ヘッダーからのアカウント [[!DNL Marketplace]][1] または [Magento.com][6].

アクセスキーは、 [!DNL Commerce] のインストール [!DNL Commerce] アカウントを設定し、資格情報を確認します。 アカウントを同期した後、Commerce Marketplaceから拡張機能やモジュールをインストールするか、 [!DNL Commerce] インストール。

様々な目的で複数のアクセスキーを作成し、必要に応じて有効または無効にすることができます。 ただし、 [!DNL Commerce] ソフトウェア。 例えば、Adobe Commerceの更新やアップグレードにMagento Open Sourceアクセスキーを使用することはできません。また、逆も使用することもできません。 また、別のユーザーに属するアクセスキーや、 [共有アカウント](commerce-account-share.md).

### アクセスキーの作成

1. ログイン先： [!DNL Commerce] アカウント。

1. 次の日： _[!UICONTROL My Account]_ページで、**[!UICONTROL Marketplace]**タブをクリックします。

1. 名前の横の右上隅で、下向き矢印をクリックし、「 」を選択します。 **[!UICONTROL My Profile]**.

   ![お使いの [!DNL Marketplace] profile](./assets/marketplace-profile.png){width="600"}

1. 次の日： _[!UICONTROL Marketplace]_下のタブ_[!UICONTROL My Products]_&#x200B;をクリックし、 **[!UICONTROL Access Keys]**&#x200B;をクリックし、次のいずれかの操作を行います。

   - Marketplace での購入に関する一連のアクセスキーを既に持っているかどうかを確認します。 様々な目的で複数のアクセスキーのセットを作成できます。

   ![アクセスキー](./assets/access-keys.png){width="600"}

   - クリック **[!UICONTROL Create a New Access Key]**. 新しいキーペアの名前を入力し、 **[!UICONTROL OK]**. 有効な文字には、スペースの代わりに、大文字と小文字およびハイフンが含まれます。

1. 完了したら、「 **[!UICONTROL OK]**.

   新しいアクセスキーが有効になり、リストに表示されます。

   次の点に注意してください。 _コピー_ 各公開鍵と秘密鍵の後のリンク。 次の手順では、これらの値をコピーして貼り付け、ストアとCommerce Marketplaceを同期します。

## インストールプロセス

>[!IMPORTANT]
>
>Adobe CommerceおよびMagento Open Source2.4.0 以降、Web セットアップウィザードは削除されました。次の操作を行うには、コマンドラインを使用する必要があります。 [install](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) または [アップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) インスタンスを作成します。 この要件には、も含まれます。 [モジュール](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) および [拡張機能](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

のインストールプロセス [!DNL Marketplace] 購入は _オンプレミス_ でホストされるインストールの場合と比較したコマースのインストール [Adobeクラウドアーキテクチャ][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## サポート

のインストールや拡張機能の使用に関するヘルプが必要な場合は、拡張機能に付属しているドキュメントでまず目を通してください。 質問に対する回答が見つからない場合は、拡張機能のリストにある連絡先情報を使用して、開発者に直接問い合わせてください。

Commerce Marketplaceで購入したものがニーズに合わない場合は、購入日から 25 日以内に返金をリクエストできます。 Adobeはすべての払い戻し要求をレビューし、承認された場合は、適切な払い戻しを発行します。

Commerce Marketplaceに関するサポートの問題については、 [[!DNL Marketplace] ヘルプセンター][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
