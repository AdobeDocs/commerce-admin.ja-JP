---
title: 支払いの概要
description: Adobe CommerceとMagento Open Sourceでネイティブにサポートされている支払い方法とサービスについて説明します。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 支払いの概要

Adobe CommerceとMagento Open Sourceは、様々な支払い方法とサービスをサポートしています。 これには、小切手やマネーオーダーによる支払いや代金引換（COD）など、いくつかのオフライン支払い方法が含まれます。 また、多数のオンライン決済ソリューションやゲートウェイとのネイティブ統合も実現しており、ベンダーが開発したバンドル型の拡張機能であるBraintreeも含まれます。

>[!TIP]
>
>Adobe CommerceおよびMagento Open Source向け支払いサービスは、堅牢で安全な支払い処理を実現するために、サンドボックステストやシンプルなセットアップなどのターンキーセルフサービスソリューションを提供します。 この強力なツールセットの詳細と、購入者にとって最適なエクスペリエンスを実現するために必要なinsightと制御を提供する方法については、[ 支払いサービスユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=ja) を参照してください。 [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/ja/docs/commerce/cloud-service/overview) のデフォルトの支払いソリューションです。

>[!NOTE]
>
>インターネット経由でクレジットカードによる支払いを受け付ける企業の場合、Payment Card Industry （PCI）が設定した要件の概要を説明した [PCI 準拠ガイドライン ](../getting-started/compliance-pci.md) を確認します。

## 2.4 の変更点

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

一部の支払い統合およびバンドルされた拡張機能は、2.4.x リリースで削除され、Commerce Marketplaceに移行されました。 最新の公式の支払い統合拡張機能については、[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"} を参照してください。

- **Amazon Pay** および **Klarna**:Adobe CommerceおよびMagento Open Sourceのリリース 2.4.0 から 2.4.3 には、これらのベンダーが開発した拡張機能が含まれています。 2.4.4 リリース以降、これらの拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールして更新する必要があります。 また、Marketplace では、拡張機能開発者が提供する最新のドキュメントにもアクセスできます。

  これらのバンドルされた拡張機能のいずれかが有効になって設定されている場合、2.4.4 のアップグレードプロセスの一環として composer.json ファイルを更新し、今後、拡張機能の更新を管理する必要があります。 詳しくは、『 [ アップグレードガイド ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=ja) の _アップグレードモジュール_ を参照してください。

- **Worldpay**、**Eway**、**CyberSource**、および **Authorize.Net**：これらの支払い統合から安全に移行する方法については、[DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"} を参照してください。

## オフラインの支払方法

Adobe CommerceとMagento Open Sourceには、サードパーティの支払い処理会社のサービスを必要としない、組み込みのオフライン支払い方法がいくつか用意されています。

- [小計ゼロ チェックアウト](zero-subtotal-checkout.md)
- [代金引換支払](cash-on-delivery.md)
- [銀行振込による支払い](bank-transfer.md)
- [小切手/送金](check-money-order.md)
- [注文書](purchase-order.md)
- [ 分割払い ](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B で利用可能）

## オンライン支払方法

Adobe CommerceとMagento Open Sourceは、世界中のあらゆる場所でマーチャントサービスを提供する多数の支払いソリューションをサポートしています。 他のサイトに制御を転送して取引を完了する支払いソリューションとは異なり、支払いゲートウェイを使用すると、顧客がサイトを離れることなく、店舗から直接クレジットカードの支払いを受け入れることができます。

### 推奨されるソリューション

- [ 資金決済 ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=ja)
- [!BADGE PaaS only]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} [PayPal Express Checkout](paypal-express-checkout.md)
- [!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} [Braintree](braintree.md)

### その他の PayPal 支払いソリューション

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

PayPal 支払い方法のオプションについて詳しくは、[PayPal 支払いソリューション ](paypal.md) を参照してください。

#### オールインワン PayPal ソリューション

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

- [PayPal 支払い詳細](paypal-payments-advanced.md)
- [PayPal ペイメントプロ](paypal-payments-pro.md)
- [PayPal 支払い標準](paypal-payments-standard.md)

#### PayPal 支払いゲートウェイ

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal ペイフローリンク](paypal-payflow-link.md)

## 不正保護

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

不正防止サービスとフィルターは、トランザクションが処理される前に送信済みの注文を調べて、不正な注文を検出し、チャージバックの費用から保護します。 Adobe CommerceとMagento Open Sourceは、次の不正対策ソリューションをサポートしています。

- [PayPal 不正管理フィルター](paypal.md#paypal-fraud-management-filters)

- [Marketplace の不正防止ソリューション ][1]

>[!NOTE]
>
>セキュリティコンプライアンスに関するアップデートをサポートするために、2.4.0 リリース以降、Signifyd の不正対策はCommerceから削除されました。 2.3.x 以前のリリースで Signifyd 統合を使用している場合は、[Signifyd Fraud &amp; Chargeback Protection 拡張機能 ](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"} に移行することをお勧めします。 ベンダーのガイドラインに従って、拡張機能のアップデートを維持してください。

## リソースのトラブルシューティング

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

支払いに関する問題のトラブルシューティングについて詳しくは、[ サポートナレッジベース ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=ja) を参照してください。

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
