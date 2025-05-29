---
title: 管理システムの概要
description: サイト、データ、統合および管理者ユーザーを効果的に管理するためにストアの管理者が使用できるシステムツールおよび機能について説明します。
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 5517bb16a8f7c8aa2f9f057df773f142302a69c7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 管理システムの概要

ストア管理は、マーチャントが製品やプロモーションの設定、注文の管理、その他の管理タスクを実行する安全なバックオフィスです。 基本的な設定タスクとストアの管理操作はすべて、管理者から実行します。 また、複数のストア機能をサポートする機能もあり、管理者が組織を管理できます。

## 変数と顧客コミュニケーション

変数は、一度作成すると複数の場所で使用できる情報です。 ストアには、[ メール ](email-templates.md) および [ ニュースレター ](../merchandising-promotions/newsletter-template.md) テンプレート、その他のタイプの [ コンテンツ ](../content-design/introduction.md#content) のパーソナライズに簡単に使用できる、事前定義済みの変数が多数含まれています。 また、カスタム変数を作成して、ニーズに固有の情報を組み込むこともできます。

- [事前定義済みの変数](variables-predefined.md)
- [カスタム変数](variables-custom.md)

ストアを起動する前に完了する必要があるタスクの 1 つは、ストアから送信されるすべてのコミュニケーションに使用されるメールテンプレートを確認して、ブランドが反映されていることを確認することです。 これには、メールおよび [ ニュースレターテンプレート ](../merchandising-promotions/newsletter-template.md)、PDFの請求書および納品書のカスタマイズが含まれます。 また、変数と [ マークアップタグ ](markup-tags.md) を使用したコンテンツのパーソナライズも含まれます。

## 運用管理

また、管理者は、システム管理者が組織内の管理者ユーザーを管理し、ストアを操作するための様々なタスクもサポートしています。 これには、次のツールが含まれます。

- **管理者ユーザーアカウントと権限** – 管理者 [ ユーザーアカウント ](permissions-users-all.md) と、管理者のサイトや機能領域へのアクセスを制御する関連 [ 役割と権限 ](permissions-user-roles.md) を管理します。
- **管理セッションと web サイト制限** - [ セキュリティ ](security.md) ベストプラクティスを確認し、管理セッションと資格情報の管理方法、CAPTCHA の実装方法、web サイト制限の管理方法を説明します。
- [!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} **システムツール** - ルーチンの [ インデックス ](index-management.md) および [ キャッシュ ](cache-management.md) 管理操作の実行、[ バックアップ ](backups.md) システムの管理、[ スケジュールされた操作 ](data-scheduled-import-export.md) の管理、および [ 開発者ツール ](developer-tools.md) の品揃えの使用を行います。
- **データ転送** - [ データ転送 ](data-transfer.md) ツールを使用して、データの読み込みと書き出しを行い、製品、価格、顧客、税率のデータを管理します。
- **統合** - [ サードパーティ統合 ](integrations.md) 用の OAuth 認証情報とリダイレクト URL の場所を確立し、使用可能な API リソースを特定します。
- **アクションログ** - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ストアで作業している管理者ユーザーによる変更について、レコード（[ アクションログ ](action-log.md)）にアクセスします。
- [!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} **サポートツール** - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [ システムレポート ](support.md#access-system-reports)）は、システムの既知の問題を特定するように設計されています。 開発および最適化プロセス中のリソースとして、また、サポートチームが問題を特定して解決するのに役立つ診断ツールとして使用できます。
