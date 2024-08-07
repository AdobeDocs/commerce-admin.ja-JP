---
title: Inventory managementについて
description: ' [!DNL Inventory Management]  機能を使用して複数の場所で在庫を管理し、店舗が実地在庫を正確に反映する方法  [!DNL Commerce]  説明します。'
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Inventory managementについて

[!DNL Inventory Management] for [!DNL Commerce] には、商品インベントリを管理するツールが用意されています。 複数の倉庫、店舗、集荷場所、直荷主などに 1 つの店舗を持つマーチャントは、これらの機能を使用して販売の数量を管理し、注文を完了するための出荷を処理できます。 在庫数量を追跡し、すべての web サイトの顧客に正確な販売可能な在庫量を提供し、距離または優先度に基づく推奨事項に従って出荷できます。 また、優先する製品設定を（すべてのストアと製品に対して）、ソースごと、製品ごとにグローバルに設定することもできます。 これらの機能はビジネスの成長に合わせて拡張され、単一の倉庫や複雑な配送ネットワークから、いくつかの追加設定で作業できるようになります。

[!DNL Inventory Management] の機能は次のとおりです。

- 単一のソースと複数のソースから在庫を生成するマーチャント向けの様々な設定
- 割り当てられたソースを通じて利用可能な集計数量を追跡するための在庫
- 同時チェックアウトの保護
- 出荷照合アルゴリズム

>[!NOTE]
>
>これらの機能は、コミュニティエンジニアリングプログラムを通じて [Inventory management](https://github.com/magento/inventory) （旧称 MSI）プロジェクトの一部として開発されました。<br/>
>
>[!DNL Inventory Management] モジュールは、Magento Open SourceおよびAdobe Commerceと共にインストールされ、すべての機能がデフォルトで有効になります。 モジュールリリースに含まれる変更点について詳しくは、[ リリースノート ](release-notes.md) を参照してください。

## 基本用語

[!DNL Inventory Management] を使用する際は、次の用語を理解することが重要です。

[!UICONTROL **ソース**] は、使用可能な製品を保存および出荷する物理的な場所を表します。 これらの場所には、倉庫、実店舗、流通センター、ドロップ荷主が含まれます。 （任意の場所を仮想製品のソースとして指定できます。）

[!UICONTROL **在庫**] 販売チャネル（現在は web サイトに限定）をソースの場所と手持在庫にマッピングします。 1 つの在庫を複数の販売チャネルにマッピングできますが、1 つの販売チャネルを割り当てることができる在庫は 1 つだけです。

[!UICONTROL **販売可能数量の集計**] は、販売チャネルを通じて販売できる仮想在庫の合計です。 この金額は、在庫に割り当てられたすべてのソースについて計算されます。

[!UICONTROL **予約**] 顧客が商品を買い物かごに追加してチェックアウトを完了すると、販売可能数量から控除が追跡されます。 受注が出荷されると、予約は特定のソース在庫数量から出荷済金額を消去して控除します。
