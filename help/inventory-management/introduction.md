---
title: ' [!DNL Inventory Management]の概要'
description: ' [!DNL Inventory Management] for [!DNL Commerce] を使用して、ソースと在庫をまたいで在庫を管理し、販売可能な数量を計算し、予約を追跡し、注文処理をサポートする方法を説明します。 管理者を使用して設定を構成し、レポートを生成します。また、設定と背景の変更を行うためのコマンドラインインターフェイスを使用します。'
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# [!DNL Inventory Management]の概要

[!DNL Commerce]の[!DNL Inventory Management]は、1つ以上のweb サイトと物理的またはバーチャルな製品の場所で在庫を管理するのに役立ちます。 管理者とコマンドラインのインターフェイスで、在庫の設定、手元にある販売可能な数量の追跡と集計、チェックアウト時の在庫の保護、注文フルフィルメントのサポートなどを行うツールを提供します。 [!DNL Inventory Management]は、倉庫、店舗、受け取り場所、ドロップシッパー、その他のフルフィルメント場所を含む単一ソースまたはマルチソースネットワークに使用できます。

## [!DNL Inventory Management]の使い方

- **管理者：**&#x200B;在庫オプションを設定し、在庫レポートを生成します。
- **コマンドライン インターフェイス：** セットアップ コマンドを実行し、バックグラウンドでインベントリの変更を適用します。
- **設定範囲：** グローバル、ソース、または製品ごとに在庫設定を構成します。

## 主な機能

[!DNL Inventory Management]の機能は次のとおりです。

- 在庫のソースが単一であるか、複数のソースであるかを問わず、マーチャントのさまざまな構成を確認できます
- 割り当てられたソースをまたいで集計販売可能数量を追跡するための在庫
- 同時チェックアウト防止
- 距離や優先順位にもとづいてフルフィルメントのレコメンデーションを行うことができる、出荷マッチングアルゴリズム

>[!NOTE]
>
>これらの機能は、[Inventory management](https://github.com/magento/inventory) （旧MSI）プロジェクトの一部として、コミュニティエンジニアリングプログラム <br/>を通じて開発されました。
>
>[!DNL Inventory Management] モジュールは、Magento Open SourceおよびAdobe Commerceと共にインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更について詳しくは、[&#x200B; リリースノート &#x200B;](release-notes.md)を参照してください。

## 基本用語

[!DNL Inventory Management]で作業する際は、次の用語を理解することが重要です。

[!UICONTROL Sources]は、使用可能な製品を保存および出荷する物理的な場所を表します。 例と図については、[&#x200B; ストックとソース &#x200B;](sources-stocks.md)を参照してください。 （どの場所でも仮想製品のソースとして指定できます）。

[!UICONTROL Stocks]は、販売チャネル（現在はweb サイトに限定）をソースの場所と手元の在庫にマッピングします。 在庫は複数の販売チャネルにマッピングできますが、販売チャネルは1つの在庫にのみ割り当てることができます。

[!UICONTROL Aggregate Salable Quantity]は、販売チャネルを通じて販売できる仮想インベントリの合計です。 金額は、在庫に割り当てられたすべてのソースにわたって計算されます。

[!UICONTROL Reservations]顧客が商品をカートに追加し、チェックアウトを完了すると、販売可能な数量から引き落としを追跡します。 注文が出荷されると、予約では、特定のソース在庫量から出荷金額がクリアされ、差し引かれます。
