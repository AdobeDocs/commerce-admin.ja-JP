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

- [ 二要素認証 ](security-two-factor-authentication.md) の設定
- [CAPTCHA](security-captcha.md) または [reCAPTCHA](security-google-recaptcha.md) の実装
- Adobe CommerceまたはMagento Open Sourceのインストール環境に含まれるドメインごとに [ セキュリティスキャン ](security-scan.md) を設定します。

>[!NOTE]
>
>[!DNL Adobe Identity Management Services] （IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceとMagento Open Source 2FA が無効になっています。 Adobe資格情報を使用してCommerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [[!DNL Adobe Identity Management Service]  （IMS）統合の概要を参照してください ](../getting-started/adobe-ims-integration-overview.md)。

潜在的な脆弱性に関する最新の情報を入手するには、[ セキュリティ センター ](https://helpx.adobe.com/jp/security.html){:target=&quot;_blank&quot;} にアクセスしてください。また、Adobe セキュリティ通知の登録や、Adobeのセキュリティ センターへのアクセスも可能です。

![ セキュリティセンター ](./assets/product-security-home.png){width="700" zoomable="yes"}

セキュリティのベストプラクティスについては、_実装プレイブック_ の [Commerce サイトとインフラストラクチャのセキュリティ保護 ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html?lang=ja) を参照してください。

## セキュリティ アクション プラン

Adobe CommerceまたはMagento Open Sourceサイトが侵害されていると思われる場合は、遅滞なく、この行動計画に従ってください。

1. **診断**：スキャンを実行して、Commerce ストアのセキュリティステータスを確認します。 Commerce[ セキュリティスキャン ](security-scan.md) は、Adobeが提供する無料サービスで、Commerce サイトを監視して既知のセキュリティリスクやマルウェアを発見し、セキュリティ通知を受け取ることができます。

1. **クリーン**:[ 資格のあるコンサルタント ](https://solutionpartners.adobe.com/s/directory/?partner_type=1) またはオンラインサービスを雇って、すべての悪意のあるコードのサイトをクリーンアップします。 一部のCommerce コミュニティメンバーは、[[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal) を推奨しています。 `/media` フォルダーに、実行可能コードの残りがないか確認します。 すべての不明な管理者ユーザーを削除し、すべての管理者パスワードをリセットします。

1. **Protect**: Commerceのインストールを最新リリースの最新の状態に保ちます。 古いバージョンを使用している場合は、使用可能になったらすべてのセキュリティパッチを適用します。 [Commerce セキュリティのベストプラクティス ](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf) を確認し、従います。 [Commerce セキュリティアラート ](https://www.adobe.com/subscription/adbeSecurityNotifications.html) を購読する。

1. **レポート**:Commerceに特定の脆弱性が見つかったと思われる場合は、[Adobeに関する問題を開く ](https://hackerone.com/adobe?type=team) と、技術的な詳細を含めます。

1. **アップグレード**: 24 時間 365 日のサポートによるさらなる安心のために、今すぐクラウドアーキテクチャで [Adobe Commerce](https://business.adobe.com/products/magento/cloud-delivery.html) へのアップグレードを計画してください。
