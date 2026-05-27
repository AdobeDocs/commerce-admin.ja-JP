---
title: 管理者システムの概要
description: ストアの管理者がサイト、データ、統合、および管理者ユーザーを効果的に管理するために使用できるシステムツールと機能について説明します。
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 5517bb16a8f7c8aa2f9f057df773f142302a69c7
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# 管理者システムの概要

ストア管理者は、マーチャントが商品やプロモーションを設定したり、注文を管理したり、その他の管理タスクを実行したりする安全なバックオフィスです。 すべての基本的な設定タスクとストア管理操作は、管理者から実行されます。 また、管理者が組織で管理できる、複数のストア機能をまたいだサポートを提供する機能もあります。

## 変数と顧客コミュニケーション

変数とは、一度作成した情報を複数の場所で利用するための要素です。 ストアには、[電子メール &#x200B;](email-templates.md)および[&#x200B; ニュースレター](../merchandising-promotions/newsletter-template.md) テンプレートや、その他の種類の[&#x200B; コンテンツ &#x200B;](../content-design/introduction.md#content)のパーソナライズに容易に使用できる、多くの定義済み変数が含まれています。 カスタム変数を作成し、ニーズに特化した情報を組み込むこともできます。

- [定義済み変数](variables-predefined.md)
- [カスタム変数](variables-custom.md)

ストアを立ち上げる前に完了すべきタスクの1つは、ストアから送信されるすべてのコミュニケーションに使用されるメールテンプレートを確認して、ブランドを反映していることを確認することです。 これには、電子メールや[&#x200B; ニュースレターテンプレート &#x200B;](../merchandising-promotions/newsletter-template.md)のカスタマイズ、PDFの請求書や梱包明細のカスタマイズが含まれます。 また、変数と[&#x200B; マークアップタグ &#x200B;](markup-tags.md)を使用したコンテンツのパーソナライズも含まれます。

## 業務管理

管理者は、システム管理者が組織内の管理者ユーザーを管理し、ストアを操作するための様々なタスクもサポートしています。 ツールには次のようなものがあります。

- **管理者ユーザーアカウントと権限** – 管理者[&#x200B; ユーザーアカウント &#x200B;](permissions-users-all.md)と、管理者のサイトと機能領域へのアクセスを制御する関連[役割と権限](permissions-user-roles.md)を管理します。
- **管理者セッションとweb サイトの制限** - [&#x200B; セキュリティ &#x200B;](security.md)のベストプラクティスを確認し、管理者セッションと資格情報の管理方法、CAPTCHAの実装およびweb サイトの制限の管理方法について説明します。
- [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} **システムツール** – 日常的な[&#x200B; インデックス &#x200B;](index-management.md)および[&#x200B; キャッシュ &#x200B;](cache-management.md)の管理操作を実行し、[&#x200B; システムをバックアップ &#x200B;](backups.md)し、[&#x200B; スケジュールされた操作](data-scheduled-import-export.md)を管理し、[開発者ツールの選定](developer-tools.md)を使用します。
- **データ転送** - [&#x200B; データ転送](data-transfer.md) ツールを使用して、データのインポートとエクスポートを行うだけでなく、製品、価格、顧客、税率データの管理も行います。
- **統合** - OAuth資格情報の場所を確立し、[&#x200B; サードパーティ統合](integrations.md)のURLをリダイレクトして、使用可能なAPI リソースを特定します。
- **アクションログ** - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）ストアで作業している管理者ユーザーが行った変更のレコード（[&#x200B; アクションログ &#x200B;](action-log.md)）にアクセスします。
- [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"} **サポートツール** - ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） [&#x200B; システムレポート &#x200B;](support.md#access-system-reports)）は、システム内の既知の問題を特定するように設計されています。 開発および最適化プロセスのリソースとして、またサポートチームが問題を特定して解決するための診断ツールとして使用できます。
