---
title: Inventory management ガイド  [!DNL Inventory Management]  ガイド
description: 移行や設定を含む、Adobe CommerceおよびMagento Open Sourceの管理者向けの  [!DNL Inventory Management]  に関する包括的な情報です。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: dbc0057f02bddf681d769bdaebfaf6b526c8dbd2
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# [!DNL Inventory Management] ガイドの概要

このガイドは、Adobe CommerceおよびMagento Open Source Admin で作業する管理者を対象としています。 機能の設定および管理を含む、このモジュールの有効化に関する詳細情報を提供します。 ここでは、コア [!DNL Commerce] の設定と機能に関する基本的な知識を前提としています。

[!DNL Inventory Management] には、管理者向けの領域が 2 つあります。

- 管理者：この領域を使用して、設定 UI およびレポートにアクセスします。
- コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

このガイドでは、次の内容について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [ はじめに ](introduction.md) | Commerce ストアが実地棚卸を正確に反映するように、複数の場所で在庫を管理するために使用できる [!DNL Inventory Management] の機能の概要です。 |
| [ リリースノート ](release-notes.md) | すべてのリリースについて詳しくは、リリースノート [!DNL Inventory Management] 参照してください。 |
| 在庫の基本 | 在庫の管理に関する基本を説明します：[ 在庫とソース ](sources-stocks.md)、[ ソースの選択と予約 ](selection-reservations.md)、[ 注文と予約のステータス ](order-status.md)、および [ 製品タイプ ](product-types.md) |
| 基本を学ぶ | [!DNL Inventory Management] モジュールの概要、およびそれがCommerce インスタンスとストアオペレーションにどのように適合するかについて説明します：[Commerceのアップグレード ](migrate.md)、[ モジュールのインストールと更新 ](install-update.md)、[ マーチャントソーシングタイプ ](merchant-sourcing.md)、[ ソーシング構造の変更 ](expand-restructure.md) |
| [ 設定 ](configuration.md) | ソースの可用性、ストアフロント製品および注文出荷を決定する [!DNL Inventory Management] オプションの設定について説明します。 |
| [ ソースの管理 ](sources-manage.md) | ソースと、製品在庫が受注履行のために管理および出荷される物理的な場所、またはサービスが使用可能な場所を定義する方法について説明します。 |
| [ 在庫の管理 ](stocks-manage.md) | Stock を使用して、販売チャネルのソースとなる製品の仮想的な集計在庫を表す方法について説明します。 |
| [ 数量の管理 ](quantities-manage.md) | 新しい製品のソースと数量を割り当てる方法や、既存の製品を変更する方法について説明します。 |
| [ 注文と出荷の管理 ](shipments.md) | 出荷プロセスを通じて在庫数量を管理するためのその他の [!DNL Inventory Management] 機能およびオプションについて説明します。 |
| [CLI リファレンス ](cli.md) | インベントリデータと設定を管理するために [!DNL Inventory Management] モジュールが提供するコマンドについて説明します。 |

{style="table-layout:auto"}

## 開発者情報

モジュールのアーキテクチャ、API、アルゴリズムのカスタマイズについて詳しくは、開発者向けドキュメントの [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) を参照してください。

## Commerce ドキュメント

{{docs-links}}

## トラブルシューティングとサポート

情報が必要な場合や、このガイドで扱われていない質問がある場合は、次のリソースを使用してください。

- [ 在庫インストール後の在庫ステータスが正しくない ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [ サポートチケット ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) - チケットを送信すると、追加のヘルプを受けることができます。
