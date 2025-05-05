---
title: Adobe Commerce管理ユーザーガイド
description: Adobe Commerce 製品ドキュメントの参照
seo-title: Services for Adobe Commerce
seo-description: Documentation and resources for Adobe Commerce and Magento Open Source users working in the Admin.
breadcrumb-title: 管理ユーザーガイド
exl-id: e30f769f-9140-4370-943e-75007b39ebc0
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# &#x200B;<!-- use banner as heading -->![ 管理ドキュメント ](./assets/banner-user-home.png) {#documentation}

次世代の世界最先端のデジタルコマースプラットフォームへようこそ。 Adobe Commerceは、オンラインストアの外観、コンテンツ、機能をこれまでになく柔軟に制御できるようにします。 管理者は、強力なマーケティング、検索エンジンの最適化、製品管理ツールを備えており、独自のビジネスニーズに合わせてカスタマイズされたサイトを作成できます。

管理者ユーザーガイドの情報は、Adobe Commerce管理者またはMagento Open Source コードベースで作業するビジネスユーザーに合わせて設計されています。 Adobe Commerce専用の機能や関数、または拡張された機能セット専用の機能や関数の表記法があります。

## Adobe Commerce {#product-editions}

Adobe Commerceは、アジャイルな B2B および B2C コマースプラットフォームであり、オンラインおよび物理スペースをまたいで顧客中心のデジタルコマースエクスペリエンスを通じて、マーチャントおよびブランドの収益を促進できます。 オンプレミスからマネージドクラウドまで、SLA が保証された最も柔軟性の高いデプロイメントモデルを提供するため、中規模およびエンタープライズ組織にとって業界をリードする選択肢です。 Adobe Commerceを使用すると、API ファースト統合と完全にカスタマイズ可能な拡張機能を利用できるほか、マーケティングからマーチャンダイジング、フルフィルメントに至るまで、エンタープライズクラスの豊富なコマースエクスペリエンス機能を利用できます。 Adobe Commerceは、他のコマースプラットフォームとは異なり、柔軟性と拡張性を提供するために、オープンソースコードベースに基づいて構築されています。

Adobe Commerceに含まれている高度な機能のリストについては、_リリース情報_ の [Commerce機能 ](https://experienceleague.adobe.com/docs/commerce-operations/release/features.html?lang=ja) を参照してください。

## Magento Open Source コードベース

Magento Open Sourceは、Adobeが公式に提供し、Adobe Commerceへの移行の互換性を確保するコードベースです。 このコードベースは、個人のデベロッパーを支援し、急速な成長を目指す中小企業を育成するAdobeの取り組みの一部です。

## 管理ユーザーガイド

<table>
<tr>
   <td valign="top" width="60px">
       <img alt="はじめに" src="./assets/icon-lightbulb.svg" width="40" height="40" /></td>
   <td valign="top">
   <a href="https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html?lang=ja"><strong> はじめに </strong></a>
    <div>
    <em> ほとんどのマーチャントが、管理者に最初に問い合わせる際に持つ「理由、場所、方法」の質問に加え、リソースと参照情報です。 このガイドは、より高度なトピックを紹介します。</em>
    <br> </div>
  </td>
  </tr>
<tr>
  <td valign="top">
      <img alt="Adobe Commerce B2B" src="./assets/icon-building.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/guide-overview.html?lang=ja"><strong>Adobe Commerce B2B</strong></a>
    <div><em> この機能セットは、顧客が主に企業である販売者（マーチャント）のニーズを満たすように設計されています。複雑な組織構造を持っている場合や、様々な役割や購入の許可レベルに対応した複数のスタッフを持っている場合があります。</em>
    <br></div>
  </td>
</tr>
<tr>
  <td valign="top">
    <img alt="カタログ管理" src="./assets/icon-shop.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/catalog/guide-overview.html?lang=ja"><strong> カタログの管理 </strong></a>
    <div><em> ストアを作成および管理する際に最も重要な領域の 1 つは、製品カタログとカテゴリです。 管理者には、ストアと製品カタログの初期設定に使用できる多くのツールが用意されています。</em>
    <br></div>
  </td>
    </tr>
<tr>
    <td valign="top">
       <img alt="Inventory management" src="./assets/icon-transfer.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/inventory/guide-overview.html?lang=ja"> <strong>[!DNL Inventory Management]</strong></a>
    <div><em>[!DNL Inventory Management] の機能により、1 つの店舗を持つマーチャントは、複数の倉庫、店舗、受け取り場所、ドロップシッパーなどにアクセスできます。 これらの機能を使用して、受注の数量を管理し、受注を完了するための出荷を処理します。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="マーチャンダイジングとプロモーション" src="./assets/icon-labels.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/marketing/guide-overview.html?lang=ja"><strong> マーチャンダイジングおよびプロモーション </strong></a>
    <div><em> 買い物客を購入者に変える、顧客エンゲージメントのターゲットを絞ったプロモーションと機会を作成します。 購入後のアクティビティをサポートし、再訪問者に特別割引を提供することで、顧客関係を管理します。 SEO イニシアチブをサポートするベストプラクティスとテクニックについて説明します。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="コンテンツとデザイン" src="./assets/icon-color-wheel.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/content-design/guide-overview.html?lang=ja"> <strong> コンテンツとデザイン </strong></a>
    <div><em> コンテンツは、顧客がストアにアクセスした際に表示されるページと要素を定義します。 ページの基本的な要素（テキストや画像など）を定義し、インタラクティブで動的なコンテンツを提供する高度な要素を定義してショッピングエクスペリエンスを向上させます。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="ページビルダー" src="./assets/icon-web-pages.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/page-builder/guide-overview.html?lang=ja"> <strong>[!DNL Page Builder]</strong></a>
    <div><em>[!DNL Page Builder] を使用すると、カスタムレイアウトでコンテンツに富んだページを簡単に作成できます。 これらの機能は、品質を向上し、カスタムページの作成に要する時間とコストを削減するように設計されています。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="顧客管理" src="./assets/icon-demographic.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/customers/guide-overview.html?lang=ja"> <strong> 顧客管理 </strong></a>
    <div><em> ストアの保守と拡張を続行する場合は、管理者で顧客アカウントと顧客グループを管理します。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="店舗と購入エクスペリエンス" src="./assets/icon-shopping-cart.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/guide-overview.html?lang=ja"> <strong> 店舗および購入エクスペリエンス </strong></a>
    <div><em> 買い物かごは、購入するパスの最後、購入と放棄の交差点に配置されます。 買い物かごの品目を完了済みの注文に変換する購入時点とサポート機能を設定します。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="管理システム" src="./assets/icon-globe-grid.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/systems/guide-overview.html?lang=ja"> <strong> 管理システム </strong></a>
    <div><em> 管理者には、システムを管理し、パフォーマンスを最適化するための複数のツールが用意されています。 このガイドには、管理者ユーザーアカウントの管理に関する情報と、関連する役割および権限が記載されています。</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="設定リファレンス" src="./assets/icon-settings.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/config/guide-overview.html?lang=ja"> <strong> 設定リファレンス </strong></a>
    <div><em> 管理画面のすべての設定に関するフィールドの説明を提供する、簡単で便利なリファレンスです。</em></div>
  </td>
</tr>
</table>

## 管理ユーザーガイドの新機能

>[!TIP]
>
>また、[Commerce サービスのドキュメントの新機能 ](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=ja#what%E2%80%99s-new) および [ 運用ガイドの新機能 ](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=ja#what%E2%80%99s-new) も確認できます。

| 説明 | タイプ | 日付 |
| ----------- | ---- | ---- |
| **1.4.0 B2B リリース** - Adobe Commerce B2B リリースノートでは、[1.4.0 リリース ](../b2b/release-notes.md#b2b-v140) の変更点と追加点について説明しています。 | 更新 | 2023/6/13 |
| **1.4.0 B2B リリース** - [ 購入者への見積書の開始 ](../b2b/sales-rep-initiates-quote.md) トピックが _Adobe Commerce B2B ガイド_ に含まれるようになりました。 販売者が特定の購入者に対して見積もりを作成して交渉プロセスを開始する方法を説明します。 | 新規 | 2023/6/13 |
| **1.4.0 B2B リリース** - [ 見積りの交渉 ](../b2b/quote-price-negotiation.md)、[ 交渉可能な見積り ](../b2b/quotes.md) および [B2B 機能の有効化 ](../b2b/enable-basic-features.md) の各トピックが更新され、セラーが開始した見積りとデフォルト機能の変更が反映されます。 | 更新 | 2023/6/13 |
| **2.2.0 Adobe IMS統合リリース** - [Adobe IDとのCommerce管理者の統合を無効にする ](../getting-started/adobe-ims-disable.md) トピックが _はじめる前に_ ガイドに含まれるようになりました。 ここでは、Adobe Commerce Admin とAdobe IMSの統合を無効にするオプションの手順について説明します。 | 新規 | 2023/6/13 |
| **2.2.0 Adobe IMS統合リリース** [&#128279;](../getting-started/adobe-ims-integration-overview.md) - Adobe Identity Management Service （IMS）統合の概要および [CommerceとAdobe IDの管理者の統合の設定 ](../getting-started/adobe-ims-config.md) のトピックの変更点が、更新された機能に反映されました。 | 更新 | 2023/6/13 |
| **[!DNL Audience Activation]** - [[!DNL Audience Activation]](../customers/audience-activation.md) トピックには、[!DNL Experience Platform Connector] 設定 UI と、買い物かご価格ルールおよび動的ブロックでヘッドレス Commerce インスタンスを使用する方法に関する、新しい情報、更新された情報、改善された情報が含まれています。 | 更新 | 2023/6/13 |
| **UPS API の廃止** - [United Parcel Service （UPS） ](../stores-purchase/ups.md) トピックおよび [ 配信方法 ](../configuration-reference/sales/delivery-methods.md#ups) 設定リファレンスページを更新して、新しい API キーを生成するための UPS API の一時的な廃止を反映しました。 | 更新 | 2023/6/08 |
| **2.4.6 リリース** - [ 製品リスト ](../catalog/products-list.md) および [ 管理者設定リファレンス ](../configuration-reference/advanced/admin.md) トピックを更新して、大きなカタログのパフォーマンスを向上させるために使用できる製品の表示制限に関する情報を追加しました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** - [ 顧客セグメントの作成と削除 ](../customers/customer-segment-create.md) および [ 顧客設定リファレンス ](../configuration-reference/customers/customer-configuration.md) のトピックを更新して、セグメントのリアルタイム検証に関する情報を含めました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** - バンドルされたBraintree統合でサポートされている更新済みの支払いオプションと新しい支払いオプションを反映するために、[Braintree](../stores-purchase/braintree.md) および [Braintree設定リファレンス ](../configuration-reference/sales/braintree.md) のトピックを更新しました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** - [ 通貨設定 ](../stores-purchase/currency-configuration.md) および [ 通貨セットアップ設定 ](../configuration-reference/general/currency-setup.md) トピックを更新して、新しい [!DNL Fixer API] （APILayer）オプションを含めました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** - [ メール通信の設定 ](../systems/email-communications.md) および [ システム設定リファレンス ](../configuration-reference/advanced/system.md#uicontrol-mail-sending-settings) トピックを更新して、メール通信用の新しい SMTP オプションを含めました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** – 最新のバンドルされた拡張機能バージョン（v1.2.6）に含まれる修正の説明的なリストを使用して [&#128279;](../inventory-management/release-notes.md)2&rbrace;Inventory management リリースノート &rbrace; を更新しました。 | 更新 | 2023/3/14 |
| **2.4.6 リリース** – 最新の拡張機能バージョン（v1.3.5）に含まれる修正の説明的なリストを使用して [B2B リリースノート ](../b2b/release-notes.md) を更新しました。 | 更新 | 2023/3/14 |
| **新しいトピック** - [Customer Management Guide](../getting-started/commerce-account-transfer.md) に Audience Activation _のトピックが追加されました。このガイドでは、Adobe CommerceでのReal-Time CDP オーディエンスのアクティブ化に関する詳細情報を提供_ ます。 | 新規 | 2023/3/13 |
| **新しいトピック** - [Commerce アカウントの転送 ](../getting-started/commerce-account-transfer.md) のトピックを _はじめる前に_ に追加しました。 | 新規 | 2023/27 |

{style="table-layout:auto"}
