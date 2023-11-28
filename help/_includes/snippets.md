---
title: スニペット
description: 特定のエディションに適用される機能やページをメモするために、メモやビジュアル要素を再利用しました。
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# スニペット

## EE のみの機能 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce機能" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">詳細情報</a>)</td></tr>
</table>

## B2B のみの機能 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce向け B2B 機能" src="../assets/b2b.svg" width="20" height="20" /> 専用の機能はでのみ使用できます <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce用 B2B</a></td></tr>
</table>

## CE のみの機能 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source機能" src="../assets/open-source.svg" width="20" height="20" /> MAGENTO OPEN SOURCE(<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">詳細情報</a>)</td></tr>
</table>

## ベータ 1 アップデート {#beta-updates}

>[!NOTE]
>
>[!BADGE 2.4.7-beta1]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="2.4.7-beta1 でのみ使用可能"}[リリースノート](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) 」を参照してください。

## ベータ 2 アップデート {#beta2-updates}

>[!NOTE]
>
[!BADGE 2.4.7-beta2]{type=Informative url="https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html" tooltip="2.4.7-beta2 でのみ使用可能"}[リリースノート](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) 」を参照してください。

## ベータ 2 とパッチのアップデート {#beta2-patches-updates}

>[!NOTE]
>
[!BADGE 2.4.6-p3]{type=Informative tooltip="2.4.6-p3 の更新点"}[!BADGE 2.4.7-beta2]{type=Informative tooltip="2.4.7-beta2 の更新点"}[2.4.7-beta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) および [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p3.html) のリリースでは、説明の機能が強化されています。 またはこれらのリリースバージョンを使用している場合は、リリースノートを確認してください。

## IMS 管理者の認証メモ {#ims-admin-note}

>[!NOTE]
>
Adobe IDをお持ちで、Adobe CommerceおよびAdobeビジネス製品への効率的なログインを必要とするAdobe Commerceのマーチャントは、コマース管理者認証をAdobe IMS認証ワークフローと統合できます。 この統合をコマースストアで有効にした後、各管理者ユーザーは、（コマースアカウントの資格情報ではなく）Adobeの資格情報を使用してログインする必要があります。 詳しくは、 [Adobe CommerceとのAdobe IMSの概要](/help/getting-started/adobe-ims-integration-overview.md).

## GTag API に関する注意 {#gtag-api-note}

>[!NOTE]
>
2.4.5 リリースより、GTag API の使用をサポートするよう、Googleのサービス統合が更新されます。 GTag は、Web ページのGoogle機能と統合するための統合メカニズムで、Google Services を通じてコンテンツを追跡し、管理するための最新の機能と機会をサポートします。 詳しくは、 [Google Analytics開発者向けドキュメント](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL 書き換えの自動スキップメモ {#url-rewrite-skip}

>[!NOTE]
>
自動リダイレクトを有効にしてカテゴリを保存すると、製品とカテゴリのすべての書き換えがリアルタイムで生成され、デフォルトで書き換えテーブルに保存されます。 このプロセスにより、多くの製品が割り当てられたカテゴリのパフォーマンスに大きな問題が生じる可能性があります。 解決策は、このデフォルトを変更し、カテゴリの保存用に製品のカテゴリ/製品 URL 書き換えの生成をスキップすることです。 この場合、製品の書き換えは、正規の製品 URL に対してのみ生成されます。 詳しくは、 [製品の自動リダイレクト](/help/merchandising-promotions/url-redirect-product-automatic.md) を参照してください。

## URL 書き換えパラメーター注意 {#url-rewrite-params}

>[!IMPORTANT]
>
リダイレクトのプロセスでは、セキュリティ上の理由から、URL で指定されたすべてのGETパラメーターが削除されます。

## 新しい価格ルール {#new-price-rule}

>[!NOTE]
>
価格ルールは、他のシステムルールと共に自動的に処理されます。 処理頻度は [cron 設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). 価格ルールを作成する場合は、システムに取り込むのに十分な時間を割いてください。 システムに正しく存在することを確認したら、ルールをテストします。

## 設定 {#config}

ストアの設定にアクセスするには、 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**から_&#x200B;管理者&#x200B;_サイドバー。

## UPS API の廃止 {#ups-api}

>[!IMPORTANT]
>
2024 年 6 月以降、Adobe Commerceの商人は現在の UPS 統合と取引できなくなりました。 これは、ネイティブのAdobe Commerce統合で使用される United Parcel Service(UPS)API が、現在、必要な OAuth 2.0 セキュリティモデルをサポートしていないためです。 この変更について詳しくは、 [_開発者ポータルアクセスキー移行ガイド_](https://developer.ups.com/oauth-developer-guide). <br/>
>
商人は [品質パッチ更新の適用](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) をストアに移行して、SOAP API から OAuth 2.0 認証プロトコルをサポートする RESTful API に移行します。


## 利用可能なドキュメント {#docs-links}

| ドキュメントリソース | 説明 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Merchant ドキュメント](../landing/home.md) | Adobe CommerceとMagento Open Sourceの両方に関するマーチャント中心のドキュメント |
| [Adobe Commerce Documentation のサービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | マーチャントがビジネスの主要なコンポーネントを店舗に統合するのに役立つサービスのコレクションをサポートするドキュメントです。 |
| [クラウドインフラストラクチャー上の Commerce に関するガイド](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 管理対象の自動ホスティングされた Cloud プラットフォームにAdobe Commerceをデプロイする手順を説明します。 |
| [Adobe Commerce 2.4 運用ガイド](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Adobe CommerceおよびMagento Open Sourceプラットフォームにデプロイされたプロジェクトを開発、デプロイ、メンテナンスするための概念、プロセス、ツール、ベストプラクティスに関するシステムドキュメントです。 |
| [Adobe Commerce 2.4 開発者向けドキュメント](https://developer.adobe.com/commerce/docs) | Adobe CommerceまたはMagento Open Sourceの構築とカスタマイズに使用する開発者向けドキュメント |

{style="table-layout:auto"}
