---
title: 支払の概要
description: Adobe CommerceとMagento Open Sourceでネイティブにサポートされる支払い方法とサービスについて説明します。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# 支払の概要

Adobe CommerceとMagento Open Sourceは、様々な支払い方法とサービスをサポートし、チェックアウトや顧客の利便性を高めます。 このリストには、小切手による支払いや送金による支払い、現金引渡し (COD) など、複数のオフライン支払い方法が含まれます。 また、多数のオンライン支払いソリューションおよびゲートウェイに対するネイティブ統合もあり、バンドルされたベンダー開発の拡張機能としてのBraintreeを含みます。

>[!TIP]
>
>Adobe CommerceおよびMagento Open Source向けの支払いサービスは、堅牢で安全な支払い処理を提供するために、サンドボックステストや簡単な設定を含む自動セルフサービスソリューションを提供します。 この強力なツールセットと、購入者に最適なエクスペリエンスを作成するために必要なインサイトと制御を提供する方法について詳しくは、 [支払サービスユーザーガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>以下を確認します。 [PCI コンプライアンスガイドライン](../getting-started/compliance-pci.md) これは、インターネットを介してクレジットカードによる支払いを受け入れる企業に対して、支払いカード業界 (PCI) が設定する要件の概要を示します。

## 2.4 の変更点

一部の支払い統合とバンドルされた拡張機能は、2.4.x リリースで削除され、Commerce Marketplaceに移行しました。 最新の正式な支払い統合の拡張については、 [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}。

- **Amazon Pay** および **クラルナ**:Adobe CommerceおよびMagento Open Sourceリリース 2.4.0 ～ 2.4.3 には、これらのベンダー開発の拡張機能が含まれていました。 2.4.4 リリース以降、これらの拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールおよび更新する必要があります。 また、Marketplace では、拡張機能の開発者が提供する最新のドキュメントにアクセスできます。

  これらのバンドルされた拡張機能を有効にして設定済みの場合、2.4.4 アップグレードプロセスの一環として composer.json ファイルを更新し、今後の拡張機能のアップデートを管理する必要があります。 詳しくは、 [モジュールのアップグレード](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) （内） _アップグレードガイド_ を参照してください。

- **Worldpay**, **エウェイ**, **CyberSource**、および **Authorize.Net**：これらの支払い統合からの安全な移行について詳しくは、 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}。

## オフラインの支払い方法

Adobe CommerceとMagento Open Sourceには、次のような組み込みのオフライン支払い方法が含まれています。これらは、サードパーティの支払い処理会社のサービスを必要としません。

- [小計ゼロのチェックアウト](zero-subtotal-checkout.md)
- [現金引渡支払](cash-on-delivery.md)
- [銀行振替支払](bank-transfer.md)
- [小切手/通貨注文](check-money-order.md)
- [発注書](purchase-order.md)
- [アカウントでの支払い](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B でAdobe Commerceに対応 )

## オンライン支払い方法

Adobe CommerceとMagento Open Sourceは、世界中のマーチャントサービスを提供する多くの支払いソリューションをサポートしています。 別のサイトに管理を移して取引を完了する支払いソリューションとは異なり、支払いゲートウェイを使用すると、顧客がサイトを離れることなく、お客様の店舗から直接クレジットカードの支払いを受け入れることができます。

### 推奨されるソリューション

- [支払いサービス](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [PayPal Express チェックアウト](paypal-express-checkout.md)
- [Braintree](braintree.md)

### その他の PayPal 支払いソリューション

詳しくは、 [PayPal の支払いソリューション](paypal.md) を参照してください。

#### オールインワン PayPal ソリューション

- [PayPal 支払いの詳細](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

#### PayPal 支払いゲートウェイ

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal ペイフローリンク](paypal-payflow-link.md)

## 不正の保護

不正保護サービスとフィルターは、トランザクションが処理される前に送信された注文を調べて、不正注文を検出し、代金の支払いを防ぐために不正注文を検出します。 Adobe CommerceとMagento Open Sourceは、次の不正保護ソリューションをサポートします。

- [PayPal 不正管理フィルタ](paypal.md#paypal-fraud-management-filters)

- [市場における不正対策ソリューション][1]

>[!NOTE]
>
>セキュリティコンプライアンスの更新をサポートするため、Signifyd 不正保護は、2.4.0 リリース以降、Commerce から削除されます。 2.3.x 以前のリリースで Signifyd 統合を使用している場合は、 [Signifyd Fraud &amp; Chargeback Protection 拡張機能](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;}。 ベンダーのガイドラインに従って、必ず拡張機能の更新を維持してください。

## リソースのトラブルシューティング

支払いに関する問題のトラブルシューティングについては、 [サポートナレッジベース](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
