---
title: スニペット
description: 特定のエディションに適用される機能またはページをメモするための再利用されたメモと視覚的要素
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# スニペット

## EE のみの機能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce機能" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerceのみの専用機能（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ja#product-editions"> 詳細情報 </a>）</td></tr>
</table>

## B2B のみの機能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B 機能" src="../assets/b2b.svg" width="20" height="20" /> <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ja">Adobe Commerce B2B</a> でのみ利用可能な排他的機能</td></tr>
</table>

## CE のみの機能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source機能" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Sourceには別の方法が必要です（<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ja#product-editions"> 詳細情報 </a>）</td></tr>
</table>

## IMS 管理者認証に関するメモ {#ims-admin-note}

>[!NOTE]
>
>Adobe IDを持ち、Adobe CommerceおよびAdobe Business 製品への効率的なログインを必要とするAdobe Commerce マーチャントは、Commerce Admin Authentication をAdobe IMS認証ワークフローと統合できます。 この統合がCommerce ストアに対して有効になると、各管理者ユーザーは、Commerce アカウントの資格情報ではなく、Adobeの資格情報を使用してログインする必要があります。 [Adobe CommerceとAdobe IMSの統合：概要 &#x200B;](/help/getting-started/adobe-ims-integration-overview.md) を参照してください。

## GTag API メモ {#gtag-api-note}

>[!NOTE]
>
>2.4.5 リリース以降、Google サービスの統合が更新されて、GTag API の使用がサポートされるようになりました。 GTag は、Web ページのGoogle機能と統合するための統合メカニズムであり、Google サービスを通じてコンテンツをトラッキングおよび管理するための最新の機能と機会をサポートしています。

## URL 書き換え自動スキップメモ {#url-rewrite-skip}

>[!NOTE]
>
>自動リダイレクトを有効にしてカテゴリを保存すると、すべての製品およびカテゴリの書き換えがリアルタイムで生成され、デフォルトで書き換えテーブルに保存されます。 このプロセスにより、製品が多く割り当てられているカテゴリでパフォーマンス上の重大な問題が発生する可能性があります。 解決策は、このデフォルトを変更し、カテゴリの生成/製品 URL の書き換えをスキップしてカテゴリを保存することです。 この場合、製品の書き換えは正規の製品 URL に対してのみ生成されます。 詳しくは、[&#x200B; 製品の自動リダイレクト &#x200B;](/help/merchandising-promotions/url-redirect-product-automatic.md) を参照してください。

## URL 書き換えパラメーターメモ {#url-rewrite-params}

>[!IMPORTANT]
>
>リダイレクトのプロセスでは、セキュリティ上の理由から、URL で指定されたGET パラメーターがすべて削除されます。

## 新規価格ルール {#new-price-rule}

>[!NOTE]
>
>価格ルールは、他のシステムルールと共に自動的に処理されます。 処理頻度は [cron 設定 &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ja) によって異なります。 価格ルールを作成する場合は、システムに入るのに十分な時間を確保します。 システムに取り込まれていることを確認したら、ルールをテストします。

## 設定 {#config}

ストアの設定にアクセスするには、「管理 **[!UICONTROL Stores]** サイドバーから _[!UICONTROL Settings]_/**[!UICONTROL Configuration]**/_ を選択し _す。

## UPS API の廃止 {#ups-api}

>[!IMPORTANT]
>
>2024 年 6 月以降、Adobe Commerceのマーチャントは、現在の UPS 統合で取引できなくなりました。 これは、ネイティブのAdobe Commerce統合で使用される United Parcel Service （UPS） API が、現在、必要な OAuth 2.0 セキュリティモデルをサポートしていないためです。 統合を有効にするには、[UPS 開発者プラットフォーム上でアプリケーションを作成 &#x200B;](https://developer.ups.com/get-started) して、OAuth 2.0 に必要な資格情報を取得します。新しい資格情報を `username` として使用し、Commerce UPS の Shipping 設定で `password` を使用します。 セキュリティモデルの変更について詳しくは、[&#x200B; 開発者ポータルのアクセスキー移行ガイド_](https://developer.ups.com/oauth-developer-guide) を参照してください。<br/>
>
>マーチャントは、SOAP API から OAuth 2.0 認証プロトコルをサポートする RESTful API に移行するために、ストアに [&#x200B; 品質パッチの更新を適用 &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=ja) する必要があります。


## 使用可能なドキュメント {#docs-links}

| ドキュメントリソース | 説明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 管理ユーザーガイド &#x200B;](../landing/home.md) | 管理で操作するマーチャント向けのドキュメントとリソースです。 |
| [Adobe Commerce向けサービスのドキュメント &#x200B;](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=ja) | マーチャンダイジングサービスのコレクションをサポートするドキュメント。マーチャントがビジネスの主要なコンポーネントをストアと統合するのに役立ちます。 |
| [&#x200B; クラウドインフラストラクチャー上のCommerceガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=ja) | 管理された自動ホスティングクラウドプラットフォームにAdobe Commerceをデプロイするためのステップバイステップの手順。 |
| [Adobe Commerce 2.4 運用ガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=ja) | Adobe Commerce on Cloud プロジェクトおよびオンプレミスプロジェクトを開発、デプロイ、管理するためのコンセプト、プロセス、ツールおよびベストプラクティスに関するシステムドキュメント。 |
| [Adobe Commerce 2.4 開発者向けドキュメント &#x200B;](https://developer.adobe.com/commerce/docs) | Adobe Commerceのカスタマイズやサードパーティシステムとの統合に使用する、開発者向けドキュメントです。 |

{style="table-layout:auto"}

## B2B 互換性 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B バージョン 1.4.2 以降は、PHP 8.2 と互換性があります。Commerce インスタンスをバージョン 2.4.7 以降にアップグレードする場合は、インスタンスが PHP バージョン 8.2 を使用して、Adobe Commerce B2B リリースとの互換性を保っていることを確認します。 また、B2B 1.4.2 以降のリリースでは、[GraphQL Application Server](https://experienceleague.adobe.com/ja/docs/commerce-operations/performance-best-practices/concepts/application-server) をサポートしていません。
