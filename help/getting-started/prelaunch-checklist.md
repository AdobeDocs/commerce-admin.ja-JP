---
title: 事前起動チェックリスト
description: このリストを使用して、ストアが本番環境に移行する前に、必要な設定設定を確認し、すべてが正しいことを確認します。
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 事前起動チェックリスト

ストアの設計、開発、テストを完了したら、次の構成設定を確認して、ストア _が公開される前にすべてが正しいことを確認してください_。 すべての構成設定について詳しくは、[_構成参照_](../configuration-reference/guide-overview.md)&#x200B;を参照してください。

## 一般設定

- [ ストア URL](../stores-purchase/store-urls.md) - ストアフロントと管理者のストア URLがライブ実稼働環境に適していることを確認します。
- セキュリティ証明書 – ストアを起動する前に、ベース URLで指定されたドメインの100%署名済みセキュリティ証明書と信頼済みセキュリティ証明書をインストールします。
- [電子メールアドレスを保存](../getting-started/store-details.md#store-email-addresses) – 新規注文、請求書、出荷、クレジットメモ、製品価格アラート、ニュースレターなど、電子メール通知の送受信に使用されるすべての電子メールアドレスを完了します。 各フィールドに有効なビジネス用メールアドレスが含まれていることを確認します。

## マーケティング設定

- [電子メールテンプレート ](../systems/email-templates.md) - ブランドを反映させるために、デフォルトの電子メールテンプレートを更新します。 テンプレートを作成する場合は、必ず設定を更新してください。
- [ セールスコミュニケーション ](../stores-purchase/introduction.md#order-management-and-operations) – 請求書と梱包明細に正しいビジネス情報が含まれていることを確認し、ブランドを反映してください。
- [Google ツール ](../merchandising-promotions/google-tools.md) - [!DNL Commerce]は、Google APIとの統合を提供して、Google AnalyticsとGoogle AdWordsを利用できるようにします。

## 営業設定

- [買い物かごオプション ](../stores-purchase/cart-configuration.md) - カートの設定設定を確認して、買い物かご内の最低注文金額や価格の有効期間の設定など、変更したい設定があるかどうかを確認します。
- [ チェックアウトオプション ](../stores-purchase/checkout-process.md#checkout-options) - チェックアウトオプションを確認して、利用条件の設定やゲストチェックアウトの設定など、変更する必要があるかどうかを確認します。
- [税金](../stores-purchase/taxes.md) – 法人税のルールと地域の要件に従って、税金が適切に設定されていることを確認します。
- [配送方法](../stores-purchase/delivery.md) – 会社が使用するすべての配送業者と配送方法を有効にします。
- [PayPal](../stores-purchase/paypal.md) – お客様にPayPalでの支払いの利便性を提供する場合は、PayPal加盟店アカウントを開設し、支払い方法を設定します。 ストアが公開される前に、サンドボックスモードでいくつかのテストトランザクションを実行します。
- [支払い方法](../stores-purchase/payments.md) – 使用する支払い方法を有効にし、正しく設定されていることを確認します。 注文ステータスの設定、使用可能な通貨、許可された国などを確認します。

## システム設定

[Cron （スケジュールされたタスク） ](../systems/cron.md) - Cron ジョブは、電子メール、カタログ価格ルール、ニュースレター、お客様からの通知、Google サイトマップ、為替レートの更新などを処理するために使用されます。 Cron ジョブが適切な時間間隔（分単位）で実行されるように設定されていることを確認します。
