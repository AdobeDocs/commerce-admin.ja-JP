---
title: '[!DNL Inventory Management] ガイド'
description: 'Adobe CommerceとMagento Open Sourceの在庫、ソース、数量、設定、注文、および出荷に関する管理者とCLI ガイド。 [!DNL Inventory Management] '
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 94e419120b8e16848cc1d449650f023f361a2af7
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# [!DNL Inventory Management] の概要

このガイドは、Adobe CommerceとMagento Open Sourceの複数の場所で在庫を管理する管理者向けです。 [!DNL Inventory Management] モジュールの設定と管理手順を提供し、コア [!DNL Commerce]機能に関する基本的な理解を前提としています。

設定、レポート、および日々の在庫管理タスクには、**管理者**&#x200B;を使用します。 インストール、アップグレード、バックエンド設定には、**コマンドラインインターフェイス**&#x200B;を使用します。

主な内容：

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | 機能、用語、および[!DNL Inventory Management]がお客様のストアにどのように適合するか。 |
| [ リリースノート ](release-notes.md) | モジュールのリリース履歴と既知の問題。 |
| [ インベントリの基本](sources-stocks.md) | [在庫とソース ](sources-stocks.md)、[ ソースの選択と予約](selection-reservations.md)、[注文と予約の状態](order-status.md)、および[製品タイプ ](product-types.md)の概念。 |
| 基本を学ぶ | [Commerceのアップグレード ](migrate.md)、[ インストールとアップデート ](install-update.md)、[ マーチャントのソーシングタイプ ](merchant-sourcing.md)、[ インベントリの再構築](expand-restructure.md)。 |
| [設定](configuration.md) | ストアフロントの表示と出荷のグローバル、製品、アルゴリズム設定。 |
| [ ソースの管理](sources-manage.md) | フルフィルメントの場所を作成および管理する。 |
| [在庫の管理](stocks-manage.md) | ソースをセールスチャネルにマッピング： |
| [数量の管理](quantities-manage.md) | ソースごとに製品数量を割り当てて更新します。 |
| [注文と出荷の管理](shipments.md) | 注文を処理し、在庫からの出荷を管理します。 |
| [CLI参照](cli.md) | コマンドラインのインベントリと設定タスク。 |

{style="table-layout:auto"}

## 開発者情報

API、カスタマイズ、モジュールアーキテクチャの高度なリソースにアクセスできます。 APIとアルゴリズムのカスタマイズに関する技術的な詳細については、REST API開発者ドキュメントの[[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)を参照してください。

## Commerce ドキュメント

Adobe Commerceのあらゆる機能に関する、マーチャント、クラウド、開発者ガイドをご覧ください。 セットアップや管理のニーズに応じて、これらのリソースを使用できます。

{{docs-links}}

## トラブルシューティングとサポート

サポート記事やチケットシステムを使用して、在庫の問題を迅速に解決できます。 在庫状況や商品管理に関する追加ヘルプを表示します。

このガイドで説明されていない情報や質問が必要な場合は、次のリソースを使用してください。

- [インベントリのインストール後にStock ステータスが正しくありません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [ サポートチケット ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)：チケットを送信して追加のヘルプを受け取ります。
