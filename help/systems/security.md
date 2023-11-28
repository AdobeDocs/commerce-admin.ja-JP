---
title: セキュリティ
description: ストアとデータを保護するために使用できるツール、およびセキュリティアクションプランのガイドライン（セキュリティ侵害を検出した場合）について説明します。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# セキュリティ

ストアを保護し、データセキュリティを維持するには、次の複数の方法があります。

- 設定 [二段階認証](security-two-factor-authentication.md)
- 実装方法 [CAPTCHA](security-captcha.md) または [reCAPTCHA](security-google-recaptcha.md)
- を設定します。 [セキュリティスキャン](security-scan.md) Adobe CommerceまたはMagento Open Sourceインストールの各ドメイン用

次にアクセス： [セキュリティセンター](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} を開き、セキュリティアラートレジストリに参加して、潜在的な脆弱性に関する最新のニュースを確認します。 セキュリティに関するベストプラクティスについて詳しくは、 [コマースサイトとインフラストラクチャの保護](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) （内） _実装プレイブック_.

>[!NOTE]
>
>を有効にしたストア [!DNL Adobe Identity Management Services] (IMS) 認証では、ネイティブのAdobe CommerceとMagento Open Source2FA が無効になっています。 コマースインスタンスにログインしている管理者Adobeは、多くの管理者タスクを再認証する必要はありません。 認証は、管理者Adobe IMSが現在のセッションにログインする際にユーザーによって処理されます。 詳しくは、 [[!DNL Adobe Identity Management Service] (IMS) 統合の概要](../getting-started/adobe-ims-integration-overview.md).

![セキュリティセンター](./assets/product-security-home.png){width="700" zoomable="yes"}

## セキュリティアクションプラン

Adobe CommerceまたはMagento Open Sourceサイトが危険にさらされていると思われる場合は、遅滞なくこのアクションプランに従ってください。

1. **診断**：スキャンを実行して、コマースストアのセキュリティステータスを確立します。 コマース [セキュリティスキャン](security-scan.md) は、Adobeが提供する無料のサービスで、既知のセキュリティリスクやマルウェアをコマースサイトで監視したり、セキュリティ通知を受け取ったりできます。

1. **クリーン**：を雇用します [有資格コンサルタント](https://solutionpartners.adobe.com/s/directory/?partner_type=1) またはすべての悪意のあるコードをサイトから消去するオンラインサービス。 一部のコマースコミュニティメンバーは、 [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). 次を確認します。 `/media` 残りの実行可能コードのフォルダー。 すべての不明な管理者ユーザーを削除し、すべての管理者パスワードをリセットします。

1. **Protect**：コマースのインストールを最新のリリースで最新の状態に保ちます。 古いバージョンを使用している場合は、すべてのセキュリティパッチが利用可能になった時点で適用します。 レビューとフォロー [コマースセキュリティのベストプラクティス](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). 配信登録 [コマースセキュリティアラート](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **レポート**：コマースに特定の脆弱性が見つかったと思われる場合は、 [Adobe](https://hackerone.com/adobe?type=team) 技術的な詳細を含む

1. **アップグレード**: 24/7のサポートによる安心のために、 [クラウドアーキテクチャ上のAdobe Commerce](https://business.adobe.com/products/magento/cloud-delivery.html) 今すぐ。
