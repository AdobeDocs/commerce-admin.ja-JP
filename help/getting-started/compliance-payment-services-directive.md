---
title: PSD2 コンプライアンス
description: 店舗に影響を与える可能性のある支払いサービス指令 (PSD2) の要件について説明します。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# PSD2 コンプライアンス

2019 年 9 月 14 日以降、欧州連合 (EU) では、EU および UK のすべての商人が [強力な顧客認証](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) 支払サービス指令 (PSD2) の要件。 他のすべての国の商人は、ベストプラクティスとしてPSD2 に従うことをお勧めします。

>[!NOTE]
>
>このトピックは情報提供のみを目的としており、法的な助言と解釈してはなりません。 ビジネスが法的義務を遵守する必要があるかどうか、またどのように遵守する必要があるかを判断するには、弁護士に相談してください。

強力な顧客認証は、PSD2 の重要なコンポーネントで、次の 2 つが必要です。

- お客様のみが持っているもの（パスワードまたは PIN）
- 顧客のみが把握できるもの（電話またはキーフォブで生成された一意のセキュリティトークン）
- お客様のみに適用されるもの（指紋や顔認識などの生体認証）

欧州の銀行は、この条件を満たさない支払いを拒否する可能性があります。 ただし、低リスクおよび低価値のトランザクションは引き続き受け入れられ、その後の定期購読での支払い。

この大きな変化と顧客の支払いが確実に低下しないように、Adobeはネイティブ向けに次の変更と推奨事項を導入しました [!DNL Commerce] 支払統合。

| 支払い方法 | コンプライアンス要件 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | ほとんどの PayPal ソリューションでは、要件は PayPal で処理されるので、PSD2 に準拠するためのアクションは必要ありません。 特定のソリューションに関する情報は、各 PayPal トピックの上部にあるメモを参照してください。 |
| [Braintree](../stores-purchase/braintree.md) | 2.4.0 のインストール済み拡張機能への切り替え以降、要件は付属のBraintree支払いモジュール内で処理され、PSD2 に準拠するためのアクションは不要です。 <br /><br />**_注意：_**以前のリリースのコア統合を使用してPSD2 に準拠するには、次のいずれかの操作を行います。<br/>- （推奨）次の公式のBraintree支払統合拡張機能をインストールします： [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}。<br/> — でBraintree支払い方法を有効にして設定 [!DNL Commerce] 設定。<br/><br/>これらの以前のコア統合は、3D セキュア 2.0 の検証をサポートしていました。 ただし、JavaScript SDK v2 で実行するBraintree実装は、3D Secure 2.0 をサポートしていません。 |
| その他 | その他すべての支払い統合については、 [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}。 支払いプロバイダーに問い合わせて、支払い 2 の要件をサポートするソリューションを推奨するPSDを依頼します。 |

{style="table-layout:auto"}
