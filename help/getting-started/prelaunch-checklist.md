---
title: 事前起動チェックリスト
description: このリストを使用して必要な設定を確認し、ストアが実稼動環境に移行する前に、すべてが正しいことを確認します。
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 事前起動チェックリスト

ストアのデザイン、開発、テストを完了したら、次の設定を確認して、ストアの前にすべてが正しいことを確認します _生きる_. すべての設定の詳細については、 [_設定リファレンス_](../configuration-reference/guide-overview.md).

## 一般設定

- [ストアの URL](../stores-purchase/store-urls.md)  — ストアフロントと管理者のストア URL が実稼動環境で正しいことを確認します。
- セキュリティ証明書 — ストアを起動する前に、ベース URL で指定されたドメインの 100%署名済みで信頼済みのセキュリティ証明書をインストールします。
- [電子メールアドレスを保存](../getting-started/store-details.md#store-email-addresses)  — 新しい注文、請求書、出荷、クレジットメモ、製品価格アラート、ニュースレターなど、電子メール通知の送受信に使用するすべての電子メールアドレスを入力します。 各フィールドに、有効なビジネス用電子メールアドレスが含まれていることを確認してください。

## マーケティング設定

- [メールテンプレート](../systems/email-templates.md)  — デフォルトの E メールテンプレートを更新して、ブランドを反映します。 テンプレートを作成する場合は、必ず設定を更新してください。
- [セールスコミュニケーション](../stores-purchase/introduction.md#order-management-and-operations)  — 請求書と梱包明細に正しいビジネス情報が含まれ、お客様のブランドを反映させてください。
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] は、Google API との統合を提供し、ビジネスがGoogle AnalyticsとGoogle AdWords を使用できるようにします。

## 販売設定

- [買い物かごのオプション](../stores-purchase/cart-configuration.md)  — 買い物かごの設定を見て、買い物かご内の価格の最小注文額や有効期間の設定など、変更したいものがあるかどうかを確認します。
- [チェックアウトオプション](../stores-purchase/checkout-process.md#checkout-options)  — チェックアウトオプションを見て、利用条件の設定、ゲストのチェックアウトの設定など、変更したいものがあるかどうかを確認します。
- [税金](../stores-purchase/taxes.md)  — 税金がビジネス税ルールおよび現地の要件に従って適切に設定されていることを確認します。
- [配信方法](../stores-purchase/delivery.md)  — 会社が使用するすべての通信事業者および配信方法を有効にします。
- [PayPal](../stores-purchase/paypal.md) - PayPal での支払いの便利さを顧客に提供する場合は、PayPal Merchant Account を開き、支払い方法を設定します。 ストアが稼働する前に、サンドボックスモードでテストトランザクションを実行します。
- [支払い方法](../stores-purchase/payments.md)  — 使用する予定の支払い方法を有効にし、正しく設定されていることを確認します。 注文ステータスの設定、許可された通貨、許可された国などを確認します。

## システム設定

[Cron（予定タスク）](../systems/cron.md) - Cron ジョブは、電子メール、カタログ価格ルール、ニュースレター、顧客アラート、Googleサイトマップ、通貨レートの更新などの処理に使用されます。 Cron ジョブが適切な時間間隔（分単位）で実行されるように設定されていることを確認します。
