---
title: セキュリティ
description: ストアとデータを保護するために使用できるツールと、セキュリティ侵害を検出した場合のセキュリティアクションプランのガイドラインについて説明します。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: fede05a413428520eec89d46f41a1cdd9c9c3a2e
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# セキュリティ

ストアを保護し、データのセキュリティを維持する方法は複数あります。

- の設定 [二要素認証](security-two-factor-authentication.md)
- 実装方法 [CAPTCHA](security-captcha.md) または [reCAPTCHA](security-google-recaptcha.md)
- を設定 [セキュリティスキャン](security-scan.md) （Adobe CommerceまたはMagento Open Sourceのインストールの各ドメインに対して）。

>[!NOTE]
>
>が有効になっているストア [!DNL Adobe Identity Management Services] （IMS）認証では、ネイティブのAdobe CommerceとMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 参照： [[!DNL Adobe Identity Management Service] （IMS）統合の概要](../getting-started/adobe-ims-integration-overview.md).

にアクセスします [セキュリティセンター](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} すると、潜在的な脆弱性に関する最新の情報を取得したり、Adobeのセキュリティ通知を登録したり、Adobeのセキュリティ センターにアクセスしたりできます。

![セキュリティセンター](./assets/product-security-home.png){width="700" zoomable="yes"}

セキュリティのベストプラクティスについては、を参照してください。 [Commerceのサイトとインフラストラクチャを保護](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) が含まれる _実装プレイブック_.

## セキュリティ アクション プラン

Adobe CommerceまたはMagento Open Sourceサイトが侵害されていると思われる場合は、遅滞なく、この行動計画に従ってください。

1. **診断**：スキャンを実行して、Commerce ストアのセキュリティステータスを確立します。 コマース [セキュリティスキャン](security-scan.md) は、Adobeが提供する無料のサービスで、Commerce サイトをモニタリングして既知のセキュリティリスクやマルウェアを発見し、セキュリティ通知を受け取ることができます。

1. **クリーン**：を雇う [資格のあるコンサルタント](https://solutionpartners.adobe.com/s/directory/?partner_type=1) または、すべての悪意のあるコードのサイトをクリーンアップするためのオンラインサービス。 一部のCommerce コミュニティメンバーがお勧めします [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). を確認します `/media` 残りの実行可能コードのフォルダー。 すべての不明な管理者ユーザーを削除し、すべての管理者パスワードをリセットします。

1. **Protect**:Commerce インストールを最新リリースの最新の状態に保ちます。 古いバージョンを使用している場合は、使用可能になったらすべてのセキュリティパッチを適用します。 レビューしてフォロー [Commerceのセキュリティのベストプラクティス](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). の購読 [Commerceのセキュリティアラート](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **報告書**:Commerceに特定の脆弱性があると思われる場合、 [Adobeの問題を開く](https://hackerone.com/adobe?type=team) 技術的な詳細を含めます。

1. **アップグレード**:24 時間 365 日のサポートによるさらなる安心を得るには、へのアップグレードを計画してください。 [クラウドアーキテクチャ上のAdobe Commerce](https://business.adobe.com/products/magento/cloud-delivery.html) 今すぐ。
