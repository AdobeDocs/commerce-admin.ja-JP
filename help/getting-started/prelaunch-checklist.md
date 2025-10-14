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

ストアのデザイン、開発、テストを完了したら、ストア _実稼動_ を開始する前に、次の設定の適用が正しいことを確認します。 すべての設定について詳しくは、[_設定リファレンス_](../configuration-reference/guide-overview.md) を参照してください。

## 一般設定

- [&#x200B; ストア URL](../stores-purchase/store-urls.md) - ストアフロントおよび管理者のストア URL がライブ実稼動環境に対して正しいことを確認します。
- セキュリティ証明書 – ストアを起動する前に、ベース URL で指定したドメインに 100% 署名および信頼されたセキュリティ証明書をインストールします。
- [&#x200B; メールアドレスを保存 &#x200B;](../getting-started/store-details.md#store-email-addresses) – 新規注文、請求書、出荷、クレジットメモ、製品価格アラート、ニュースレターなど、メール通知の送受信に使用されるすべてのメールアドレスを入力します。 各フィールドに有効な業務用メールアドレスが入力されていることを確認します。

## マーケティング設定

- [&#x200B; メールテンプレート &#x200B;](../systems/email-templates.md) - ブランドを反映するようにデフォルトのメールテンプレートを更新します。 テンプレートを作成する場合は、必ず設定を更新してください。
- [&#x200B; セールスコミュニケーション &#x200B;](../stores-purchase/introduction.md#order-management-and-operations) – 請求書と梱包明細に正しいビジネス情報が含まれ、ブランドが反映されていることを確認します。
- [Google ツール &#x200B;](../merchandising-promotions/google-tools.md) - [!DNL Commerce] は、Google API との統合を提供し、ビジネスがGoogle AnalyticsおよびGoogle AdWords を使用できるようにします。

## 販売設定

- [&#x200B; 買い物かごオプション &#x200B;](../stores-purchase/cart-configuration.md) – 買い物かご設定の設定を確認して、買い物かごの価格の最小注文額や有効期間の設定など、変更する内容があるかどうかを確認します。
- [&#x200B; チェックアウトオプション &#x200B;](../stores-purchase/checkout-process.md#checkout-options) - チェックアウトオプションを見て、利用条件の設定やゲストのチェックアウトの設定など、変更が必要なものがあるかどうかを確認します。
- [&#x200B; 税金 &#x200B;](../stores-purchase/taxes.md) - ビジネス税規則および地域の要件に従って税金が適切に設定されていることを確認します。
- [&#x200B; 配信方法 &#x200B;](../stores-purchase/delivery.md) – 会社ですべての通信事業者と配信方法を使用できるようにします。
- [PayPal](../stores-purchase/paypal.md) - PayPal で支払う便利さを顧客に提供する予定がある場合は、PayPal マーチャントアカウントを開き、支払い方法を設定します。 ストアが実稼働する前に、サンドボックスモードでいくつかのテストトランザクションを実行します。
- [&#x200B; 支払い方法 &#x200B;](../stores-purchase/payments.md) – 使用する予定の支払い方法を有効にし、適切に設定されていることを確認します。 注文ステータスの設定、許可された通貨、許可されている国などを確認します。

## システム設定

[Cron （スケジュールされたタスク） &#x200B;](../systems/cron.md) - Cron ジョブは、メール、カタログ価格ルール、ニュースレター、顧客アラート、Google サイトマップ、為替レートの更新などの処理に使用されます。 Cron ジョブが適切な時間間隔（分単位）で実行されるように設定されていることを確認します。
