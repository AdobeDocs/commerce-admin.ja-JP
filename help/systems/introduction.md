---
title: 管理システムの概要
description: ストアの管理者が、サイト、データ、統合、および管理者ユーザーを効果的に管理するために使用できるシステムツールと機能について説明します。
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 46564240e7f76cf2a691c209b36d530763ba4f01
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# 管理システムの概要

店舗管理者は、商人が製品やプロモーションを設定し、注文を管理し、その他の管理タスクを実行する、安全なバックオフィスです。 基本的な設定タスクとストア管理操作は、すべて管理者が実行します。 また、管理者が管理できる複数のストア機能を組織に対してサポートする機能もあります。

## 変数と顧客通信

変数は、1 回作成して複数の場所で使用できる情報の一部です。 ストアには、パーソナライズに簡単に使用できる、多くの事前定義済みの変数が含まれています [電子メール](email-templates.md) および [ニュースレター](../merchandising-promotions/newsletter-template.md) テンプレートおよびその他のタイプ [コンテンツ](../content-design/introduction.md#content). また、カスタム変数を作成して、ニーズに合った情報を組み込むこともできます。

- [定義済み変数](variables-predefined.md)
- [カスタム変数](variables-custom.md)

ストアを起動する前に完了すべきタスクの 1 つは、ストアから送信されるすべてのコミュニケーションで使用される電子メールテンプレートをレビューして、ブランドを反映しているかを確認することです。 これには、電子メールのカスタマイズや [ニュースレターテンプレート](../merchandising-promotions/newsletter-template.md)、およびPDF請求書と梱包明細。 また、変数と [マークアップタグ](markup-tags.md).

## 運用管理

また、システム管理者は、組織内の管理者ユーザーを管理し、ストアを運用するための様々なタスクをサポートしています。 これには、次のツールが含まれます。

- **管理者ユーザーアカウントと権限**  — 管理者の管理 [ユーザーアカウント](permissions-users-all.md)関連付けられた [役割と権限](permissions-user-roles.md) は、Admin のサイトおよび機能領域へのアクセスを制御します。
- **管理セッションと Web サイトの制限**  — レビュー [セキュリティ](security.md) ベストプラクティスを紹介し、管理者セッションと資格情報の管理、CAPTCHA の実装、Web サイト制限の管理方法について説明します。
- **システムツール**  — ルーチンを実行 [index](index-management.md) および [キャッシュ](cache-management.md) 管理操作 [～を取り戻す](backups.md) システム、管理 [予定された操作](data-scheduled-import-export.md)そして、次の項目を使用します。 [開発者ツール](developer-tools.md).
- **データ転送** - [データ転送](data-transfer.md) データのインポートとエクスポートを行い、製品、価格、顧客、税率データを管理するツール。
- **統合**  — の OAuth 資格情報とリダイレクト URL の場所を設定します。 [サードパーティ統合](integrations.md)を参照し、利用可能な API リソースを特定します。
- **アクションログ** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) レコードにアクセスする ([アクションログ](action-log.md)) を参照してください。
- **サポートツール** - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) サポートツール ([データコレクター](support.md#data-collector) および [システムレポート](support.md#access-system-reports)) は、システムの既知の問題を識別するように設計されています。 開発および最適化プロセス中のリソースとして、また、サポートチームが問題を特定して解決するのに役立つ診断ツールとして使用できます。
