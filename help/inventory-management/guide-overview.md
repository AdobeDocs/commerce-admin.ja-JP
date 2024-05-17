---
title: '''Inventory management ガイド [!DNL Inventory Management] ガイド`'
description: ～に関する包括的な情報 [!DNL Inventory Management] Adobe Commerce管理者およびMagento Open Source管理者（移行や設定を含む）
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# [!DNL Inventory Management] ガイドの概要

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 機能の設定および管理を含む、このモジュールの有効化に関する詳細情報を提供します。 ここでは、コア部分の基本的な理解を前提としています [!DNL Commerce] 設定と機能。

[!DNL Inventory Management] には、管理者向けの次の 2 つの領域があります。

- 管理者：この領域を使用して、設定 UI およびレポートにアクセスします。
- コマンドラインインターフェイス：このツールを使用して、インストールタスクとバックエンド設定タスクを実行します。

このガイドでは、次の内容について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | の概要 [!DNL Inventory Management] Commerce ストアが物理的な在庫を正確に反映するように、複数の場所で在庫を管理するために使用できる機能。 |
| [リリースノート](release-notes.md) | すべてについて詳しくは、リリースノートを確認してください [!DNL Inventory Management] リリース。 |
| 在庫の基本 | 在庫管理の基本について説明します。 [在庫とソース](sources-stocks.md), [ソースの選択と予約](selection-reservations.md), [注文と予約のステータス](order-status.md)、および [製品タイプ](product-types.md) |
| 基本を学ぶ | について説明します [!DNL Inventory Management] モジュールと、Commerce インスタンスおよびストアオペレーションへの適合： [Commerce アップグレード](migrate.md), [モジュールのインストールとアップデート](install-update.md), [マーチャントソーシングタイプ](merchant-sourcing.md)、および [ソーシング構造の変更](expand-restructure.md) |
| [設定](configuration.md) | 設定について説明します [!DNL Inventory Management] ソースの可用性、ストアフロント製品および注文出荷を決定するオプション。 |
| [ソースの管理](sources-manage.md) | ソースと、製品在庫が受注履行のために管理および出荷される物理的な場所、またはサービスが使用可能な場所を定義する方法について説明します。 |
| [在庫の管理](stocks-manage.md) | Stock を使用して、販売チャネルのソースとなる製品の仮想的な集計在庫を表す方法について説明します。 |
| [数量の管理](quantities-manage.md) | 新しい製品のソースと数量を割り当てる方法や、既存の製品を変更する方法について説明します。 |
| [注文と出荷の管理](shipments.md) | その他について説明します [!DNL Inventory Management] 出荷プロセスを通じて在庫数量を管理するための機能とオプション。 |
| [CLI リファレンス](cli.md) | が提供するコマンドについて説明します [!DNL Inventory Management] インベントリ データと構成設定を管理するモジュール。 |

{style="table-layout:auto"}

## 開発者情報

参照： [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) モジュールのアーキテクチャ、API およびアルゴリズムのカスタマイズについて詳しくは、開発者ドキュメントを参照してください。

## Commerce ドキュメント

{{docs-links}}

## トラブルシューティングとサポート

情報が必要な場合や、このガイドで扱われていない質問がある場合は、次のリソースを使用してください。

- [大量の予約の不整合](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [在庫の不整合の問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [スウォッチがストライクスルー在庫に達していない状態が「0」に達する](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [在庫インストール後の在庫状態が正しくない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [サポートチケット](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)- チケットを送信して、追加のヘルプを受けます。
