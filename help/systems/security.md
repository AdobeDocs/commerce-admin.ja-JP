---
title: セキュリティ
description: ストアとデータを保護するために使用できるツールと、セキュリティ対策プランのガイドラインについて説明します。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2: id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# セキュリティ

ストアを保護し、データセキュリティを維持するには、複数の方法があります。

- [二段階認証](security-two-factor-authentication.md)を設定
- [CAPTCHA](security-captcha.md)または[reCAPTCHA](security-google-recaptcha.md)を実装
- Adobe CommerceまたはMagento Open Sourceの各ドメインに対して[ セキュリティスキャン ](security-scan.md)を設定します。

>[!NOTE]
>
>[!DNL Adobe Identity Management Services] （IMS）認証を有効にしているストアでは、ネイティブ Adobe CommerceとMagento Open Source 2FAが無効になっています。 Adobeの資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理者タスクで再認証を行う必要はありません。 認証は、管理者ユーザーが現在のセッションにログインしたときにAdobe IMSによって処理されます。 [[!DNL Adobe Identity Management Service]  （IMS）統合の概要](../getting-started/adobe-ims-integration-overview.md)を参照してください。

[ セキュリティセンター](https://helpx.adobe.com/security.html){:target="_blank"}にアクセスして、潜在的な脆弱性に関する最新ニュースを入手し、Adobe セキュリティ通知に登録し、Adobe Trust Centerにアクセスします。

![ セキュリティセンター](./assets/product-security-home.png){width="700" zoomable="yes"}

セキュリティのベストプラクティスについて詳しくは、_実装プレイブック_&#x200B;の[Commerce サイトとインフラストラクチャの保護](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)を参照してください。

## セキュリティアクションプラン

Adobe CommerceまたはMagento Open Sourceのサイトが侵害されたと疑われる場合は、遅滞なく、このアクションプランに従ってください。

1. **診断**: スキャンを実行して、Commerce ストアのセキュリティ ステータスを確認します。 Commerce [ セキュリティスキャン ](security-scan.md)は、Adobeが提供する無料サービスです。Commerce サイトで既知のセキュリティリスクやマルウェアを監視し、セキュリティ通知を受け取ることができます。

1. **クリーン**: [適格コンサルタント ](https://solutionpartners.adobe.com/s/directory/?partner_type=1)またはオンラインサービスを雇用して、サイトに存在するすべての悪意のあるコードをクリーニングします。 一部のCommerce コミュニティ メンバーは[[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal)を推奨しています。 残りの実行可能なコードについては、`/media` フォルダーを確認してください。 不明な管理者ユーザーをすべて削除し、すべての管理者パスワードをリセットします。

1. **Protect**：最新のリリースで、Commerceのインストールを最新の状態に保ちます。 古いバージョンを使用している場合は、利用可能になったすべてのセキュリティパッチを適用します。 [Commerceのセキュリティに関するベストプラクティス ](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf)を確認してフォローします。 [Commerce セキュリティ アラート ](https://www.adobe.com/subscription/adbeSecurityNotifications.html)を購読します。

1. **レポート**: Commerceで特定の脆弱性が見つかったと思われる場合は、[Adobe](https://hackerone.com/adobe?type=team)で問題を開き、技術的な詳細を含めてください。

1. **アップグレード**:24時間年中無休のサポートによる安心を得るために、今すぐ[Adobe Commerce Cloud Architecture](https://business.adobe.com/products/magento/cloud-delivery.html)へのアップグレードを計画してください。
