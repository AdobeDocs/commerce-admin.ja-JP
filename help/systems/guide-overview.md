---
title: 管理システムガイド
description: Commerce ストアを保護して権限を管理するためのベストセキュリティプラクティスや、データのインポートおよびエクスポート方法、統合と拡張機能の管理方法、日常のメンテナンスを行う方法を学びます。
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
source-git-commit: 0cda54e8d52a866151658573c6d2ace1820dab75
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 7%

---

# Adobe Commerce管理システムガイド

このガイドは、Adobe CommerceおよびMagento Open Source Admin で作業するシステム管理者およびインテグレーターを対象としています。 e コマースビジネスの複数の組織機能にわたるアクティビティをサポートする、管理者セキュリティ、メンテナンス操作、システム全体のリソースに関する詳細情報を提供します。 ここでは、Commerceのコア設定と機能に関する基本的な知識を前提としています。

このガイドでは、次の内容について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [&#x200B; はじめに &#x200B;](introduction.md) | Commerce インスタンス内のシステムと統合機能の概要。 |
| [&#x200B; システムメニュー &#x200B;](system-menu.md) | [!UICONTROL System] メニューを使用して、データのインポートとエクスポート、システム キャッシュとインデックスの管理、ユーザーアカウントと権限の管理、バックアップ、システム通知、およびカスタム変数のツールにアクセスします。 |
| [&#x200B; 管理者アカウントと権限 &#x200B;](permissions.md) | 管理者ユーザーアカウント、およびストア機能へのアクセス権を付与するために使用する役割を管理します。 |
| [&#x200B; 変数 &#x200B;](variables-predefined.md) | 変数を使用すると、メールおよびニュースレターのテンプレートや、サイトおよび顧客体験をサポートするその他のタイプのコンテンツを簡単にパーソナライズできます。 |
| [&#x200B; メールテンプレート &#x200B;](email-templates.md) | メールテンプレートは、ストアから送信される自動メッセージのレイアウト、コンテンツ、書式を定義します。 各トランザクションメールは、特定のタイプのトランザクションまたはイベントに関連付けられているので、トランザクションメールと呼ばれます。 |
| [&#x200B; データ転送 &#x200B;](data-transfer.md) | <ul><li>読み込みツールと書き出しツールを使用すると、1 回の操作で複数のレコードを管理できます。 新しい項目を読み込むだけでなく、既存の製品セットを更新、置換、削除することもできます。</li><li>接続されたCommerce サービスに [[!UICONTROL Data Management Dashboard]](data-dashboard.md) から転送されたエンティティのデータ同期ステータスの表示。</li><li>[[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md) ページからCommerce SaaS サービスにデータフィードを書き出すための同期ステータスをモニタリングします。</li></ul> |
| [&#x200B; アクションログ &#x200B;](action-log.md) | Adobe Commerceの場合、アクションログには、ストアで作業する管理者ユーザーが行ったすべての変更が取り込まれます。 これにより、ストアに加えられたすべての変更を追跡できます。 |
| ツール | [!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"} システム管理者は一連のツールを使用できます。[&#x200B; サポートツール &#x200B;](support.md) は、システムの既知の問題を識別するように設計されています。 システムツールは、日常的な [&#x200B; インデックス &#x200B;](index-management.md) および [&#x200B; キャッシュ &#x200B;](cache-management.md) 管理、[&#x200B; システムのバックアップ &#x200B;](backups.md)、[&#x200B; スケジュールされた操作 &#x200B;](data-scheduled-import-export.md) の管理、および [&#x200B; 開発者ツール &#x200B;](developer-tools.md) の様々な使用を行うための運用サポートを提供します。 |
| [&#x200B; 統合 &#x200B;](integrations.md) | OAuth 認証情報の場所を確立し、サードパーティ統合用のリダイレクト URL を指定します。 |
| [&#x200B; セキュリティ &#x200B;](security.md) | ストアとデータを保護するために使用できるツールと、セキュリティ侵害を検出した場合のセキュリティアクションプランのガイドラインについて説明します。 |

{style="table-layout:auto"}

## 使用可能なドキュメント

{{docs-links}}
