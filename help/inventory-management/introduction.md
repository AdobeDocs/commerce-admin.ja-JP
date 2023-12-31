---
title: Inventory managementの概要
description: 使用方法を学ぶ [!DNL Inventory Management] 複数の場所で在庫を管理する機能を使用し、 [!DNL Commerce] ストアは、実際の在庫を正確に反映します。
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Inventory managementの概要

[!DNL Inventory Management] 対象： [!DNL Commerce] には、製品の在庫を管理するためのツールが用意されています。 複数の倉庫、店舗、受け取り場所、受け取り場所、受け取り船などに 1 つの店舗を持つ商人は、これらの機能を使用して、販売数量を維持し、受注を完了するために出荷を処理できます。 在庫数を追跡し、すべての Web サイトの顧客に対して正確な販売可能な在庫数を提供し、距離や優先度に基づいてレコメンデーションに従って出荷できます。 また、（すべてのストアと製品に対して）グローバルに、ソースごと、および製品ごとに、希望の製品設定を設定することもできます。 これらの機能は、ビジネスと共に拡大し、1 つの倉庫から、または複雑な出荷ネットワークから、いくつかの追加の設定で作業できます。

[!DNL Inventory Management] 次の機能が含まれます。

- 1 つのソースと複数のソースから在庫を取得する商人の異なる構成
- 割り当てられたソースを通じて使用可能な集計数量を追跡する在庫
- 同時チェックアウトの保護
- 出荷照合アルゴリズム

>[!NOTE]
>
>これらの機能は、 [Inventory management](https://github.com/magento/inventory) （旧称 MSI）コミュニティエンジニアリングプログラムを通じてプロジェクトを行います。<br/>
>
>The [!DNL Inventory Management] モジュールは、Magento Open SourceおよびAdobe Commerceと共にインストールされ、すべての機能がデフォルトで有効になっています。 モジュールリリースに含まれる変更点については、 [リリースノート](release-notes.md).

## 基本的な用語

を使用する際は、次の用語を理解することが重要です。 [!DNL Inventory Management]:

[!UICONTROL **ソース**] は、利用可能な製品を保存および出荷する物理的な場所を表します。 これらの場所には、倉庫、実店舗、流通センター、落下荷主などが含まれます。 （任意の場所を仮想製品のソースとして指定できます）。

[!UICONTROL **在庫**] 販売チャネル（現在は web サイトに限定）をソースの場所と手持在庫にマッピングします。 1 つの在庫は複数の販売チャネルにマッピングできますが、販売チャネルは 1 つの在庫にのみ割り当てることができます。

[!UICONTROL **売上可能数量の集計**] は、販売チャネルを通じて販売できる仮想インベントリの合計です。 金額は、1 つの在庫に割り当てられたすべてのソースで計算されます。

[!UICONTROL **予約**] 顧客が商品を買い物かごに追加し、チェックアウトを完了すると、売上高からの控除を追跡します。 注文が出荷されると、予約は特定のソース在庫数量から出荷済金額を消去し、差し引きます。
