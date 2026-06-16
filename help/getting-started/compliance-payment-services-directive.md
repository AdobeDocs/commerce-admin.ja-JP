---
title: PSD2 コンプライアンス
description: ストアに影響を与える可能性のある支払いサービス指令（PSD2）の要件について説明します。
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# PSD2 コンプライアンス

2019年9月14日以降、EUおよび英国のすべての加盟店は、決済サービス指令（PSD2）の[Strong Customer Authentication](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) （SCA）要件に準拠する必要があります。 その他のすべての国の販売者は、ベストプラクティスとしてPSD2に準拠することが推奨されます。

>[!NOTE]
>
>このトピックは、情報提供のみを目的としたもので、法的なアドバイスとして解釈されるべきものではありません。 自社が法的義務を遵守する必要があるかどうか、どのように遵守すべきかを判断するには、弁護士に相談してください。

強力な顧客認証はPSD2の重要な要素であり、次のふたつが必要です。

- お客様のみが持っているもの（パスワードまたはPIN）
- お客様のみが知っているもの（電話またはキーフォブによって生成された一意のセキュリティトークン）
- 顧客のみが使用する場合（指紋や顔認証などの生体認証）

ヨーロッパの銀行は、要件を満たさない支払いを辞退する可能性があります。 ただし、低リスクおよび低価値の取引は引き続き受け入れられ、その後の定期的なサブスクリプションでの支払いが受け入れられる可能性があります。

この大幅な変更により、お客様の支払いが拒否されないようにするために、Adobeでは、ネイティブの[!DNL Commerce]支払い統合に関する次の変更と推奨事項が導入されました。

| お支払い方法 | コンプライアンス要件 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | ほとんどのPayPal ソリューションでは、要件はPayPalによって処理されるため、PSD2に準拠するためのアクションは必要ありません。 特定のソリューションについて詳しくは、各PayPal トピックの上部にあるメモを参照してください。 |
| [Braintree](../stores-purchase/braintree.md) | 2.4.0のインストール済み拡張機能への切り替えから、要件は付属のBraintree支払いモジュール内で処理され、PSD2に準拠するためのアクションは必要ありません。 <br /><br />**_Note:_**&#x200B;以前のリリースでコアインテグレーションを使用してPSD2に準拠するには、次のいずれかの操作を行います。<br/>- （推奨）Braintreeの公式な支払いインテグレーション拡張機能を[[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}からインストールします。<br/>- [!DNL Commerce]設定でBraintree支払い方法を有効にして設定します。<br/><br/>これらの以前のコア統合は、3D Secure 2.0検証をサポートしています。 ただし、JavaScript SDK v2で実行されるBraintreeの実装では、3D Secure 2.0はサポートされていません。 |
| その他 | その他のすべての支払い統合については、[[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}で利用可能な拡張機能を確認してください。 決済サービスプロバイダーに、PSD2の要件に対応するソリューションの推奨を依頼してください。 |

{style="table-layout:auto"}
