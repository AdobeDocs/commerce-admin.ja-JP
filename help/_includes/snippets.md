---
title: スニペット
description: 特定のエディションに適用される機能またはページをメモするための再利用されたメモと視覚的要素
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# スニペット

## EE のみの機能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce機能" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerceのみの専用機能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">詳細情報</a>）</td></tr>
</table>

## B2B のみの機能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B 機能" src="../assets/b2b.svg" width="20" height="20" /> 専用機能は次の製品でのみ使用可能： <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce B2B</a></td></tr>
</table>

## CE のみの機能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source機能" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Sourceには別の方式が必要（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">詳細情報</a>）</td></tr>
</table>

## IMS 管理者認証に関するメモ {#ims-admin-note}

>[!NOTE]
>
>Adobe IDを持っていて、Adobe CommerceおよびAdobeビジネス製品への効率的なログインを必要とするAdobe Commerce マーチャントは、Commerce Admin Authentication をAdobe IMS認証ワークフローと統合できます。 この統合がCommerce ストアに対して有効になると、各管理者ユーザーは、Commerce アカウントの資格情報ではなく、Adobeの資格情報を使用してログインする必要があります。 参照： [Adobe CommerceとAdobe IMSの統合：概要](/help/getting-started/adobe-ims-integration-overview.md).

## GTag API メモ {#gtag-api-note}

>[!NOTE]
>
>2.4.5 リリース以降、Google サービスの統合が更新されて、GTag API の使用がサポートされるようになりました。 GTag は、Web ページのGoogle機能と統合するための統合メカニズムであり、Google サービスを通じてコンテンツをトラッキングおよび管理するための最新の機能と機会をサポートしています。 詳しくは、 [Google Analytics開発者向けドキュメント](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL 書き換え自動スキップメモ {#url-rewrite-skip}

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトで書き換えテーブルに保存されます。 このプロセスにより、製品が多く割り当てられているカテゴリでパフォーマンス上の重大な問題が発生する可能性があります。 解決策は、このデフォルトを変更し、カテゴリの生成/製品 URL の書き換えをスキップしてカテゴリを保存することです。 この場合、製品の書き換えは正規の製品 URL に対してのみ生成されます。 参照： [製品の自動リダイレクト](/help/merchandising-promotions/url-redirect-product-automatic.md) を参照してください。

## URL 書き換えパラメーターメモ {#url-rewrite-params}

>[!IMPORTANT]
>
>リダイレクトのプロセスでは、セキュリティ上の理由から、URL で指定されたすべてのGETパラメーターが削除されます。

## 新規価格ルール {#new-price-rule}

>[!NOTE]
>
>価格ルールは、他のシステムルールと共に自動的に処理されます。 処理頻度は、以下によって異なります。 [cron 設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). 価格ルールを作成する場合は、システムに入るのに十分な時間を確保します。 システムに取り込まれていることを確認したら、ルールをテストします。

## 設定 {#config}

ストアの設定にアクセスするには、次を選択します **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**から_ Admin _サイドバー。

## UPS API の廃止 {#ups-api}

>[!IMPORTANT]
>
>2024 年 6 月以降、Adobe Commerceのマーチャントは、現在の UPS 統合で取引できなくなりました。 これは、ネイティブのAdobe Commerce統合で使用される United Parcel Service （UPS） API が、現在、必要な OAuth 2.0 セキュリティモデルをサポートしていないためです。 この変更の詳細については、を参照してください。 [_開発者ポータルアクセスキー移行ガイド_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>商人は [品質パッチの更新を適用](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) をストアに追加して、SOAP API から OAuth 2.0 認証プロトコルをサポートする RESTful API に移行します。


## 使用可能なドキュメント {#docs-links}

| ドキュメントリソース | 説明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 マーチャントドキュメント](../landing/home.md) | Adobe Commerceに関するマーチャント向けドキュメント |
| [Adobe Commerce向けサービス ドキュメント](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | マーチャントがビジネスの主要なコンポーネントをストアと統合するのに役立つ、サービスのコレクションをサポートするドキュメント。 |
| [クラウドインフラストラクチャー上のCommerce ガイド](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 管理された自動ホスティングクラウドプラットフォームにAdobe Commerceをデプロイするためのステップバイステップの手順。 |
| [Adobe Commerce 2.4 運用ガイド](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Adobe Commerce プロジェクトを開発、デプロイ、管理するためのコンセプト、プロセス、ツールおよびベストプラクティスに関するシステムドキュメント。 |
| [Adobe Commerce 2.4 開発者向けドキュメント](https://developer.adobe.com/commerce/docs) | Adobe Commerceのカスタマイズとサードパーティシステムとの統合に使用する、開発者向けドキュメント |

{style="table-layout:auto"}
