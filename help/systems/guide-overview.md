---
title: 管理者システムガイド
description: Commerce ストアを保護して権限を管理するためのベストセキュリティプラクティスや、データのインポートおよびエクスポート方法、統合と拡張機能の管理方法、日常のメンテナンスを行う方法を学びます。
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
TQID: https://experienceleague.adobe.com/TMdBCvfpmoU6cWCqaC8W4JJpIiyt4tXY7Lun7-p-rHA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: cc250cf1-34eb-4863-80d0-d170d45ea067
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 6%

---

# Adobe Commerce管理システムガイド

このガイドは、Adobe CommerceおよびMagento Open Source Adminで作業するシステム管理者およびインテグレーターを対象としています。 コマースビジネスの複数の部門をまたいでアクティビティをサポートする、管理者のセキュリティ、メンテナンス運用、システム全体のリソースに関する詳細な情報を提供します。 このモデルでは、Commerceのコア設定と機能に関する基本的な理解が必要です。

主な内容：

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | Commerce インスタンス内のシステムと統合機能の概要。 |
| [&#x200B; システムメニュー](system-menu.md) | [!UICONTROL System] メニューを使用して、データのインポートとエクスポート、システムキャッシュとインデックス管理、ユーザーアカウントと権限管理、バックアップ、システム通知、カスタム変数のツールにアクセスします。 |
| [管理者アカウントと権限](permissions.md) | ストア機能へのアクセス権を付与するために使用される管理者ユーザーアカウントと役割を管理します。 |
| [変数](variables-predefined.md) | 変数を使用すると、電子メールやニュースレターテンプレートなど、サイトや顧客体験をサポートするコンテンツを容易にパーソナライズできます。 |
| [&#x200B; メールテンプレート &#x200B;](email-templates.md) | メールテンプレートは、ストアから送信される自動メッセージのレイアウト、コンテンツ、形式を定義します。 トランザクションメールとは、それぞれが特定の種類のトランザクション、つまりイベントに関連付けられているため、トランザクションメールと呼ばれます。 |
| [&#x200B; データ転送](data-transfer.md) | <ul><li>読み込みツールと書き出しツールを使用すると、1回の操作で複数のレコードを管理できます。 新しいアイテムを読み込むだけでなく、既存の製品セットを更新、置換、削除することもできます。</li><li>[[!UICONTROL Data Management Dashboard]](data-dashboard.md)から接続されたCommerce サービスに転送されたエンティティのデータ同期ステータスを表示します。</li><li>[[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md) ページからCommerce SaaS サービスへのデータフィード書き出しの同期ステータスをモニタリングします。</li></ul> |
| [&#x200B; アクションログ &#x200B;](action-log.md) | Adobe Commerceの場合、アクションログには、ストアで作業する管理者ユーザーが行ったすべての変更が記録されます。 これにより、ストアに加えられたすべての変更を追跡できます。 |
| ツール | [!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}のシステム管理者は、利用可能なツールのコレクションを持っています。[&#x200B; サポートツール &#x200B;](support.md)は、システム内の既知の問題を識別するように設計されています。 日常的な[&#x200B; インデックス &#x200B;](index-management.md)および[&#x200B; キャッシュ &#x200B;](cache-management.md)管理、[&#x200B; システム &#x200B;](backups.md)のバックアップ、[&#x200B; スケジュールされた操作](data-scheduled-import-export.md)の管理、一連の[開発者ツール &#x200B;](developer-tools.md)の使用を実行するための運用サポートを提供します。 |
| [統合](integrations.md) | OAuth資格情報の場所を確立し、サードパーティ統合にリダイレクト URLを提供します。 |
| [&#x200B; セキュリティ &#x200B;](security.md) | ストアとデータのセキュリティを確保するために利用できるツールと、セキュリティ対策プランのガイドラインについて説明します。 |

{style="table-layout:auto"}

## 使用可能なドキュメント

{{docs-links}}
