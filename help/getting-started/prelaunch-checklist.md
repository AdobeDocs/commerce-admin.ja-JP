---
title: Prelaunch チェックリスト
description: このリストを使用すると、ストアが実稼動環境に移行する前に、すべてが正しいことを確認するために必要な設定を確認できます。
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Prelaunch チェックリスト

ストアのデザイン、開発、テストを完了したら、ストアの前に次の設定の内容がすべて正しいことを確認します _運用開始_. 設定の詳細については、を参照してください。 [_設定リファレンス_](../configuration-reference/guide-overview.md).

## 一般設定

- [URL を格納](../stores-purchase/store-urls.md) - ストアフロントと管理者のストア URL が実稼動環境に対して正しいことを確認します。
- セキュリティ証明書 – ストアを起動する前に、ベース URL で指定したドメインに 100% 署名および信頼されたセキュリティ証明書をインストールします。
- [メールアドレスの保存](../getting-started/store-details.md#store-email-addresses)  – 新規受注、請求書、出荷、クレジット・メモ、製品価格アラート、ニュースレターなど、電子メール通知の送受信に使用されるすべての電子メール・アドレスを入力します。 各フィールドに有効な業務用メールアドレスが入力されていることを確認します。

## マーケティング設定

- [メールテンプレート](../systems/email-templates.md) - ブランドを反映するようにデフォルトのメールテンプレートを更新します。 テンプレートを作成する場合は、必ず設定を更新してください。
- [営業コミュニケーション](../stores-purchase/introduction.md#order-management-and-operations)  – 請求書と梱包明細に正しいビジネス情報が含まれていることを確認し、ブランドを反映します。
- [Google ツール](../merchandising-promotions/google-tools.md) - [!DNL Commerce] は、Google API との統合を提供して、ビジネスがGoogle AnalyticsおよびGoogle AdWords を使用できるようにします。

## 販売設定

- [買い物かごオプション](../stores-purchase/cart-configuration.md)  – 買い物かごの構成設定を調べて、買い物かごの価格の最小注文額や有効期間の設定など、変更が必要なものがあるかどうかを確認します。
- [チェックアウトオプション](../stores-purchase/checkout-process.md#checkout-options) - チェックアウトオプションを確認して、利用条件の設定やゲストのチェックアウトの設定など、変更が必要なものがあるかどうかを確認します。
- [税金](../stores-purchase/taxes.md)  – 事業税ルールと地域の要件に従って税金が適切に設定されていることを確認します。
- [配信方法](../stores-purchase/delivery.md)  – 会社ですべての通信事業者と配信方法を使用できるようにする。
- [PayPal](../stores-purchase/paypal.md) - PayPal で支払う便利さを顧客に提供する予定がある場合は、PayPal マーチャントアカウントを開き、支払い方法を設定します。 ストアが実稼働する前に、サンドボックスモードでいくつかのテストトランザクションを実行します。
- [支払い方法](../stores-purchase/payments.md)  – 使用する支払い方法を有効にし、適切に設定されていることを確認します。 注文ステータスの設定、許可された通貨、許可されている国などを確認します。

## システム設定

[Cron （スケジュールされたタスク）](../systems/cron.md) - Cron ジョブは、メール、カタログ価格ルール、ニュースレター、顧客アラート、Google サイトマップ、為替レートの更新などの処理に使用されます。 Cron ジョブが適切な時間間隔（分単位）で実行されるように設定されていることを確認します。
