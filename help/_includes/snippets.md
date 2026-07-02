---
title: スニペット
description: 特定のエディションに適用するフィーチャーまたはページに注意するために、再利用されたメモとビジュアル要素
source-git-commit: df2920f654bf932385e78f8cc894bae0daee017a
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 0%

---

# スニペット

## EEのみの機能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerceの機能" src="/help/assets/adobe-logo.svg" width="20" height="20" /> これは、Adobe Commerceでのみ使用できる機能であり、Magento Open Sourceでは使用できません。 （<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ja#product-editions">詳細情報</a>）</td></tr>
</table>

## B2Bのみの機能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2Bの機能" src="/help/assets/b2b.svg" width="20" height="20" /> <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ja">Adobe Commerce B2B</a>でのみ使用できる排他的機能</td></tr>
</table>

## CEのみの機能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Sourceの機能" src="/help/assets/open-source.svg" width="20" height="20" /> Magento Open Sourceには別のメソッドが必要です（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ja#product-editions">詳細情報</a>）</td></tr>
</table>

## IMS管理者認証メモ {#ims-admin-note}

>[!NOTE]
>
>Adobe Commerceを使用しており、Adobe IDおよびAdobe Business製品への効率的なログインを希望するAdobe Commerceの販売者は、Commerce管理者認証をAdobe IMS認証ワークフローに統合できます。 この統合がCommerce ストアに対して有効になった後、各管理者ユーザーはログインするために、Commerce アカウントの資格情報ではなく、Adobeの資格情報を使用する必要があります。 [Adobe CommerceとAdobe IMSの統合の概要](/help/getting-started/adobe-ims-integration-overview.md)を参照してください。

## GTag API メモ {#gtag-api-note}

>[!NOTE]
>
>2.4.5 リリース以降、Google サービス統合が更新され、GTag APIの使用がサポートされるようになりました。 GTagは、web ページのGoogle機能と統合するための統合メカニズムであり、Google サービスを通じてコンテンツをトラッキングおよび管理する最新の機能と機会をサポートします。

## URL書き換え自動スキップノート {#url-rewrite-skip}

>[!NOTE]
>
>自動リダイレクトが有効になっていてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトで書き換えテーブルに保存されます。 このプロセスは、割り当てられた製品が多いカテゴリでパフォーマンスの問題が発生する可能性があります。 解決策は、このデフォルトを変更し、カテゴリの保存のために製品のカテゴリ/製品のURL書き換えの生成をスキップすることです。 この場合、製品の書き換えは、正規の製品URLに対してのみ生成されます。 詳しくは、[製品の自動リダイレクト &#x200B;](/help/merchandising-promotions/url-redirect-product-automatic.md)を参照してください。

## URL書き換えパラメーターメモ {#url-rewrite-params}

>[!IMPORTANT]
>
>リダイレクトのプロセスでは、セキュリティ上の理由から、URLで指定されたすべてのGET パラメーターが削除されます。

## 新しい価格ルール {#new-price-rule}

>[!NOTE]
>
>価格ルールは、他のシステムルールで自動的に処理されます。 処理頻度は、[cron設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ja)によって異なります。 プライスルールを作成するときは、システムに入れるための十分な時間を確保しましょう。 システムに確実に存在する場合は、ルールをテストします。

## 設定 {#config}

ストア設定にアクセスするには、_管理者_ サイドバーから&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;を選択します。

## UPS APIの非推奨化 {#ups-api}

>[!IMPORTANT]
>
>2024年6月以降、Adobe Commerceのマーチャントは現在のUPSとの取引ができなくなります。 これは、ネイティブのAdobe Commerce統合で使用されるUnited Parcel Service （UPS） APIが、現在、必要なOAuth 2.0 セキュリティモデルをサポートしていないためです。 統合を有効にするには、[UPS開発者プラットフォーム &#x200B;](https://developer.ups.com/get-started)でアプリケーションを作成して、OAuth 2.0に必要な資格情報を取得します。 Commerce UPS出荷設定の`username`および`password`として新しい資格情報を使用します。 セキュリティモデルの変更について詳しくは、[開発者ポータル アクセスキー移行ガイド_](https://developer.ups.com/oauth-developer-guide)を参照してください。<br/>
>
>加盟店は、SOAP APIからOAuth 2.0認証プロトコルをサポートするRESTful APIに移行するために、[高品質のパッチアップデート &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=ja)をストアに適用する必要があります。


## 使用可能なドキュメント {#docs-links}

| 関連文書 | 説明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4管理者ユーザーガイド &#x200B;](/help/landing/home.md) | 管理画面で作業するマーチャント向けのドキュメントとリソース。 |
| [Adobe Commerce ドキュメント向けサービス &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=ja) | マーチャンダイジングサービスのコレクションをサポートし、マーチャントがストアとビジネスの主要な要素を統合できるよう支援するドキュメント。 |
| [Commerce on Cloud Infrastructure ガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=ja) | 管理された自動ホスティングクラウドプラットフォームにAdobe Commerceをデプロイするためのステップバイステップの手順。 |
| [Adobe Commerce 2.4運用ガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=ja) | Adobe Commerce オンクラウドおよびオンプレミスプロジェクトの開発、デプロイ、保守の概念、プロセス、ツール、ベストプラクティスに関するシステムドキュメントです。 |
| [Adobe Commerce 2.4開発者向けドキュメント &#x200B;](https://developer.adobe.com/commerce/docs) | Adobe Commerceをカスタマイズし、サードパーティのシステムと統合するために使用される、開発者向けのドキュメント。 |

{style="table-layout:auto"}

## B2B互換性 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2以降は、PHP 8.2と互換性があります。 Commerce インスタンスをバージョン 2.4.7以降にアップグレードする場合は、インスタンスでPHP バージョン 8.2を使用してAdobe Commerce B2B リリースとの互換性を維持してください。 さらに、B2B 1.4.2以降のリリースでは、[GraphQL Application Server](https://experienceleague.adobe.com/ja/docs/commerce-operations/performance-best-practices/concepts/application-server)はサポートされていません。

## reCAPTCHA フォームリスト {#recaptcha-forms-list}

- [!UICONTROL Enable for Customer Login]
- [!UICONTROL Enable for Forgot Password]
- [!UICONTROL Enable for Create New Customer Account]
- [!UICONTROL Enable for Edit Customer Account]
- [!UICONTROL Enable for Create New Company Account] （Adobe Commerce B2Bでのみ使用可能）
- [!UICONTROL Enable for Contact Us]
- [!UICONTROL Enable for Product Review]
- [!UICONTROL Enable for Newsletter Subscription]
- [!UICONTROL Enable for Gift Card] （Adobe Commerceのみ）
- [!UICONTROL Enable for Invitation Create Account]
- [!UICONTROL Enable for Send To Friend] - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}
- [!UICONTROL Enable for Checkout/Placing Order]
- [!UICONTROL Enable for Wishlist Sharing]
- [!UICONTROL Enable for Coupon Codes]
- [!UICONTROL Enable for PayPal PayflowPro payment form] - [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}
