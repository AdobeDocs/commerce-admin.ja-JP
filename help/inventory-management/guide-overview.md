---
title: '''Inventory managementガイド [!DNL Inventory Management] ガイド`'
description: に関する包括的な情報 [!DNL Inventory Management] Adobe CommerceおよびMagento Open Source管理者向け（移行および設定を含む）。
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# [!DNL Inventory Management] ガイドの概要

このガイドは、Adobe CommerceとMagento Open Sourceの管理者を対象としています。 このモジュールの有効化に関する詳細（機能の設定や管理など）を提供します。 コアに関する基本的な理解を前提としています。 [!DNL Commerce] 設定と機能に関する情報です。

[!DNL Inventory Management] には、管理者向けの次の 2 つの領域があります。

- 管理者：この領域を使用して、設定の UI とレポートにアクセスします。
- コマンドラインインターフェイス：このツールを使用して、インストールおよびバックエンドの設定タスクを実行します。

このガイドでは、以下について説明します。

| 件名 | 説明 |
| ------- | ----------- |
| [はじめに](introduction.md) | の概要 [!DNL Inventory Management] 複数の場所で在庫を管理するために使用できる機能を使用して、コマースストアが実際の在庫を正確に反映できます。 |
| [リリースノート](release-notes.md) | すべての [!DNL Inventory Management] リリース。 |
| 在庫の基本 | 在庫管理の基本を学びます。 [在庫およびソース](sources-stocks.md), [ソースの選択と予約](selection-reservations.md), [注文と予約のステータス](order-status.md)、および [製品タイプ](product-types.md) |
| 基本を学ぶ | 詳しくは、 [!DNL Inventory Management] モジュールと、コマースインスタンスおよびストア操作に適した方法を示します。 [コマースのアップグレード](migrate.md), [モジュールのインストールと更新](install-update.md), [マーチャントソーシングタイプ](merchant-sourcing.md)、および [ソース構造の変更](expand-restructure.md) |
| [設定](configuration.md) | の設定について説明します。 [!DNL Inventory Management] ソースの可用性、ストアフロント製品、および注文出荷を決定するオプション。 |
| [ソースの管理](sources-manage.md) | ソースと、製品在庫が管理され、出荷されて注文が達成される物理的な場所、またはサービスが使用可能な場所を定義する方法について説明します。 |
| [在庫の管理](stocks-manage.md) | 在庫を使用して、販売チャネルのソースに対する製品の仮想的で集計された在庫を表す方法を説明します。 |
| [数量の管理](quantities-manage.md) | 新規製品のソースと数量を割り当てる方法、または既存の製品を変更する方法を説明します。 |
| [オーダーと出荷の管理](shipments.md) | その他の [!DNL Inventory Management] 出荷プロセスを通じて在庫数量を管理する機能とオプション。 |
| [CLI リファレンス](cli.md) | が提供するコマンドの詳細 [!DNL Inventory Management] 在庫データと構成設定を管理するモジュールです。 |

{style="table-layout:auto"}

## 開発者情報

詳しくは、 [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) モジュールのアーキテクチャ、API、アルゴリズムのカスタマイズについて詳しくは、開発者向けドキュメントを参照してください。

## Commerce ドキュメント

{{docs-links}}

## トラブルシューティングとサポート

このガイドに記載されていない情報や質問がある場合は、次のリソースを使用してください。

- [多数の予約の不整合](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [在庫の不整合の問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [取り消し線のない在庫が「0」に達するスウォッチ](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [在庫のインストール後に在庫ステータスが正しくありません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [サポートチケット](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) — 追加のヘルプを受け取るには、チケットを送信します。
