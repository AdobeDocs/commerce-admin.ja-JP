---
title: Inventory managementの概要
description: ' [!DNL Inventory Management] 機能を使用して複数の場所の在庫を管理し、 [!DNL Commerce] 店舗が実際の在庫を正確に反映できるようにする方法について説明します。'
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
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
ht-degree: 0%

---

# Inventory managementの概要

[!DNL Commerce]の[!DNL Inventory Management]には、商品の在庫を管理するためのツールが用意されています。 単一の店舗を複数の倉庫、店舗、受け取り場所、ドロップシッパーなどに持つマーチャントは、これらの機能を利用して販売の数量を維持し、出荷を処理して注文を完了することができます。 在庫量を追跡し、あらゆるweb サイトで顧客に正確な販売可能な在庫量を提供し、距離や優先順位にもとづいてレコメンデーションに応じて出荷することができます。 また、グローバルに（すべてのストアと製品に対して）、ソースごと、および製品ごとに好みの製品設定を設定することもできます。 これらの機能はビジネスとともに成長するため、単一の倉庫や、いくつかの追加の設定を含む複雑な配送ネットワークから作業することができます。

[!DNL Inventory Management]の機能は次のとおりです。

- 在庫のソースが単一で、複数のソースを起点とするマーチャントのさまざまな構成
- 割り当てられたソースを通じて利用可能な集計量を追跡するための在庫
- 同時チェックアウト防止
- 出荷照合アルゴリズム

>[!NOTE]
>
>これらの機能は、[Inventory management](https://github.com/magento/inventory) （旧MSI）プロジェクトの一部として、コミュニティエンジニアリングプログラム <br/>を通じて開発されました。
>
>[!DNL Inventory Management] モジュールは、Magento Open SourceおよびAdobe Commerceと共にインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更について詳しくは、[&#x200B; リリースノート &#x200B;](release-notes.md)を参照してください。

## 基本用語

[!DNL Inventory Management]で作業する際は、次の用語を理解することが重要です。

[!UICONTROL **ソース**]&#x200B;は、使用可能な製品を保存して出荷する物理的な場所を表します。 これらの場所には、倉庫、実店舗、流通センター、ドロップシッパーなどがあります。 （どの場所でも仮想製品のソースとして指定できます）。

[!UICONTROL **ストック**]&#x200B;は、販売チャネル（現在はweb サイトに限定）をソースの場所と手元の在庫にマッピングします。 在庫は複数の販売チャネルにマッピングできますが、販売チャネルは1つの在庫にのみ割り当てることができます。

[!UICONTROL **集計販売可能数量**]&#x200B;は、販売チャネルを通じて販売できる仮想インベントリの合計数です。 金額は、在庫に割り当てられたすべてのソースにわたって計算されます。

[!UICONTROL **予約**]&#x200B;は、顧客が商品をカートに追加し、チェックアウトを完了すると、販売可能な数量から控除された金額を追跡します。 注文が出荷されると、予約では、特定のソース在庫量から出荷金額がクリアされ、差し引かれます。
