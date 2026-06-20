---
title: Inventory management ガイド  [!DNL Inventory Management]  ガイド
description: 'Adobe CommerceおよびMagento Open Sourceの管理者に関する包括的な情報（移行および設定を含む）。 [!DNL Inventory Management] '
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# [!DNL Inventory Management] ガイドの概要

このガイドは、Adobe CommerceおよびMagento Open Source Adminで作業する管理者を対象としています。 このモジュールの機能の設定と管理など、このモジュールの有効化に関する詳細な情報を提供します。 コア [!DNL Commerce]の設定と機能に関する基本的な理解を前提としています。

[!DNL Inventory Management]には、管理者が次の2つの領域があります。

- 管理者：この領域を使用して、設定UIとレポートにアクセスします。
- コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

主な内容：

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | 複数の場所の在庫を管理し、Commerce ストアが実際の在庫を正確に反映できるように使用できる[!DNL Inventory Management]機能の概要。 |
| [&#x200B; リリースノート &#x200B;](release-notes.md) | すべての[!DNL Inventory Management] リリースについて詳しくは、リリースノートを参照してください。 |
| 在庫の基本 | 在庫の管理に関する基本について説明します。[在庫とソース &#x200B;](sources-stocks.md)、[&#x200B; ソースの選択と予約](selection-reservations.md)、[注文と予約の状態](order-status.md)、および[製品タイプ &#x200B;](product-types.md) |
| 基本を学ぶ | [!DNL Inventory Management] モジュールと、それがCommerce インスタンスおよびストアオペレーションにどのように適合するかについて説明します。[Commerce アップグレード &#x200B;](migrate.md)、[&#x200B; モジュールのインストールと更新](install-update.md)、[&#x200B; マーチャントのソーシングタイプ &#x200B;](merchant-sourcing.md)、および[&#x200B; ソーシング構造の変更](expand-restructure.md) |
| [設定](configuration.md) | ソースの可用性、ストアフロント製品、および注文出荷を決定する[!DNL Inventory Management] オプションの設定について説明します。 |
| [&#x200B; ソースの管理](sources-manage.md) | 調達先について説明し、商品の在庫を管理および出荷して注文フルフィルメントを行う物理的な場所、またはサービスを提供する物理的な場所を定義する方法について説明します。 |
| [在庫の管理](stocks-manage.md) | 在庫を使用して、セールスチャネルのソースとなる商品のバーチャルな集計在庫を表す方法を説明します。 |
| [数量の管理](quantities-manage.md) | 新製品のソースと数量を割り当てたり、既存の製品を変更したりする方法について説明します。 |
| [注文と出荷の管理](shipments.md) | 出荷プロセスを通じて在庫量を管理するための追加の[!DNL Inventory Management]機能とオプションについて説明します。 |
| [CLI参照](cli.md) | 在庫データと構成設定を管理するために[!DNL Inventory Management] モジュールが提供するコマンドについて説明します。 |

{style="table-layout:auto"}

## 開発者情報

モジュールアーキテクチャ、API、アルゴリズムのカスタマイズについて詳しくは、開発者ドキュメントの[[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)を参照してください。

## Commerce ドキュメント

{{docs-links}}

## トラブルシューティングとサポート

このガイドで説明されていない情報や質問が必要な場合は、次のリソースを使用してください。

- [インベントリのインストール後にStock ステータスが正しくありません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html?lang=ja)
- [&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=ja#submit-ticket)：チケットを送信して追加のヘルプを受け取ります。
