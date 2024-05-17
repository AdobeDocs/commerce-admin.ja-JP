---
title: PSD2 への準拠
description: ストアに影響を与える可能性のある支払いサービスディレクティブ（PSD2）の要件について説明します。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# PSD2 への準拠

2019 年 9 月 14 日（PT）より、欧州連合（EU）は、EU と英国のすべてのマーチャントに以下に従うことを義務付けています [強力な顧客認証](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) （SCA）支払いサービス指令の要件（PSD2）。 その他すべての国のマーチャントは、ベストプラクティスとしてPSD2 に準拠することをお勧めします。

>[!NOTE]
>
>このトピックは情報提供のみを目的としており、法的な助言と見なされるべきではありません。 ビジネスが法的義務に準拠する必要があるかどうかと、どのように準拠すべきかを判断するには、法務担当者に問い合わせてください。

強力な顧客認証はPSD2 の重要なコンポーネントであり、次の 2 つが必要です。

- 顧客のみが持っているもの（パスワードまたは PIN）
- 顧客のみが知っているもの（電話またはキーフォブによって生成された一意のセキュリティトークン）
- お客様だけが使用するもの（指紋や顔認識などの生体認証）

ヨーロッパの銀行は、要件を満たさない支払いを拒否する可能性があります。 ただし、低リスクおよび低価値の取引は引き続き受け入れられ、その後の定期的なサブスクリプションでの支払いが受け入れられる可能性があります。

この大幅な変更により、お客様の支払いが拒否されないようにするため、Adobeは以下の変更とネイティブ向けの推奨事項を導入しました [!DNL Commerce] 支払いの統合。

| 支払い方法 | コンプライアンス要件 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | ほとんどの PayPal ソリューションでは、要件は PayPal で処理されるので、PSD2 に準拠するための対応は必要ありません。 特定の解決策については、各 PayPal トピックの上部にあるメモを参照してください。 |
| [Braintree](../stores-purchase/braintree.md) | 2.4.0 でインストールされた拡張機能への切り替え以降、要件は含まれるBraintree支払いモジュール内で処理され、PSD2 に準拠するための対応は必要ありません。 <br /><br />**_注意：_**以前のリリースでコア統合を使用してPSD2 に準拠するには、次のいずれかの操作を行います。<br/>- （推奨）から公式のBraintree決済統合拡張機能をインストールします [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}。<br/> – でのBraintree支払い方法の有効化と設定 [!DNL Commerce] 設定。<br/><br/>これらの以前のコア統合は、3D セキュア 2.0 検証をサポートしています。 ただし、JavaScript SDK v2 上で実行されるBraintree実装は、3D Secure 2.0 をサポートしていません。 |
| その他 | その他のすべての支払い統合については、で利用可能な拡張機能を確認してください。 [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}。 PSD2 の要件をサポートするソリューションを支払いプロバイダーに推奨するように依頼してください。 |

{style="table-layout:auto"}
