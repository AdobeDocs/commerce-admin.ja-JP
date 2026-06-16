---
title: 支払いの概要
description: Adobe CommerceとMagento Open Sourceでネイティブにサポートされている支払い方法とサービスについて説明します。
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
TQID: https://experienceleague.adobe.com/nu9qbRkc1OWOxkg-eERyZKuGwj0oc8wXDdSCMqGxe1I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: c32adafa-ed01-4b31-997e-2413013911b0
subfeature_v2: id: f2261633-201d-46c5-8a66-999e70527a83
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 900
ht-degree: 0%

---

# 支払いの概要

Adobe CommerceとMagento Open Sourceは、幅広い支払い方法とサービスをサポートしています。 これには、小切手やマネーオーダーによる支払いや代金引換（COD）など、いくつかのオフライン支払い方法が含まれます。 また、Braintreeをバンドルされたベンダー開発の拡張機能として含め、多くのオンライン決済ソリューションやゲートウェイとのネイティブ統合も可能です。

>[!TIP]
>
>Adobe CommerceおよびMagento Open Sourceの決済サービスでは、サンドボックステストやシンプルな設定など、ターンキー型のセルフサービスソリューションを提供し、堅牢で安全な決済処理を実現します。 この強力なツールセットと、購入者に最適なエクスペリエンスを構築するために必要なinsightとコントロールを提供する方法について詳しくは、[決済サービスユーザーガイド ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)を参照してください。 これは、[Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview)のデフォルトの支払いソリューションです。

>[!NOTE]
>
>インターネット経由でクレジットカードによる支払いを受け付けるビジネスのPCI （Payment Card Industry）によって設定された要件の概要を示す[PCI コンプライアンス ガイドライン ](../getting-started/compliance-pci.md)を確認します。

## 2.4の変更点

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

一部の支払い統合機能とバンドルされた拡張機能は、2.4.x リリースで削除され、Commerce Marketplaceに移行されました。 最新の公式な支払い統合拡張機能は、[Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}で確認できます。

- **Amazon Pay**&#x200B;および&#x200B;**Klarna**: Adobe CommerceおよびMagento Open Source リリース 2.4.0 ～ 2.4.3には、これらのベンダーが開発した拡張機能が含まれています。 2.4.4 リリース以降、これらの拡張機能はコアリリースにバンドルされなくなり、Commerce Marketplaceからインストールして更新する必要があります。 Marketplaceでは、拡張機能の開発者が提供する最新のドキュメントにもアクセスできます。

  これらのバンドル拡張機能のいずれかを有効にして設定している場合は、2.4.4 アップグレードプロセスの一環としてcomposer.json ファイルを更新し、拡張機能の更新を今後も管理する必要があります。 詳しくは、_アップグレードガイド_&#x200B;の[ アップグレードモジュール ](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)を参照してください。

- **Worldpay**、**Eway**、**CyberSource**、および&#x200B;**Authorize.Net**：これらの支払い統合からの安全な移行の詳細については、[開発ブログ ](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}を参照してください。

## オフラインのお支払い方法

Adobe CommerceとMagento Open Sourceには、いくつかのオフライン決済方法が組み込まれており、サードパーティの決済処理会社のサービスを必要としません。

- [小計チェックアウトをゼロ](zero-subtotal-checkout.md)
- [代金引換](cash-on-delivery.md)
- [銀行振込お支払い](bank-transfer.md)
- [小切手/マネーオーダー](check-money-order.md)
- [発注](purchase-order.md)
- [ アカウントでのお支払い](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2Bで利用可能）

## オンライン決済の方法

Adobe CommerceとMagento Open Sourceは、世界中のあらゆる地域でマーチャントサービスを提供する多くの決済ソリューションをサポートしています。 決済ゲートウェイは、取引を完了するために別のサイトにコントロールを転送する決済ソリューションとは異なり、顧客がサイトを離れることなく、ストアから直接クレジットカード決済を受け付けることができます。

### 推奨ソリューション

- [決済サービス](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [PayPal Express チェックアウト ](paypal-express-checkout.md)
- [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} [Braintree](braintree.md)

### その他のPayPal決済ソリューション

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

PayPal支払い方法のオプションについて詳しくは、[PayPal支払いソリューション ](paypal.md)を参照してください。

#### オールインワン PayPal ソリューション

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

- [PayPal Payments Advanced](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### PayPal支払いゲートウェイ

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal Payflow Link](paypal-payflow-link.md)

## 不正行為の防止

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

不正利用防止サービスとフィルターは、取引が処理される前に送信された注文を調査し、不正な注文を検出してチャージバックのコストからあなたを保護します。 Adobe CommerceとMagento Open Sourceは、次の不正防止ソリューションをサポートしています。

- [PayPal不正管理フィルター](paypal.md#paypal-fraud-management-filters)

- [Marketplace上の不正利用防止ソリューション](https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection)

>[!NOTE]
>
>セキュリティコンプライアンスのアップデートをサポートするため、Signifyd不正利用防止は2.4.0 リリース以降、Commerceから削除されます。 2.3.x以前のリリースでSignifyd統合を使用している場合は、[Signifyd Fraud &amp; Chargeback Protection拡張機能](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}に移行することをお勧めします。 ベンダーのガイドラインに従って、拡張機能のアップデートを必ず保持してください。

## リソースのトラブルシューティング

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

支払いに関する問題のトラブルシューティングについては、[ サポート ナレッジベース ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html)を参照してください。
