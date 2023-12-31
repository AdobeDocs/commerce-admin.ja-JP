---
title: カタログ管理の概要
description: カタログ管理でのカタログおよび製品範囲の機能について説明します。
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# カタログ管理の概要

Adobe CommerceとMagento Open Sourceの用語 _カタログ_ 製品データベース全体を参照する。

ストアを作成および管理する上で最も重要な領域の 1 つは、製品の作成とカテゴリです。 管理者は、ストアの初期設定や、ストアの保守、ビジネスの最適化に使用するツールを提供します。

>[!TIP]
>
>Inventory management for Adobe CommerceとMagento Open Sourceは、製品の在庫を管理するためのツールを提供します。 複数の倉庫、店舗、受け取り場所、受け取り場所、受け取り船などに 1 つの店舗を持つ商人は、これらの機能を使用して、販売数量を維持し、受注を完了するために出荷を処理できます。 これらの機能と、それらを使用して複数の場所で在庫を管理する方法について詳しくは、 [Inventory management User Guide](../inventory-management/introduction.md).

## カタログの範囲

カタログデータへのアクセスは、 [範囲](../getting-started/websites-stores-views.md#scope-settings) 設定、カタログ設定、および [ルートカテゴリ](category-root.md) それがストアに割り当てられている。 カタログには、有効で販売可能な製品と、現在は販売不可の製品が含まれます。

営業では、期間 _カタログ_ 通常は、厳選された一部の商品を指します。 例えば、ある店舗に「春のカタログ」と「秋のカタログ」があるとします。

印刷されたカタログの目次や、ストアのメインメニューと同様に、または _上部ナビゲーション_ ：製品をカテゴリ別に整理し、顧客が必要なものを簡単に見つけられるようにします。 メインメニューは、 _ルートカテゴリ_：ストアに割り当てられるメニューのコンテナです。 特定のメニューオプションはストアビューレベルで定義されるので、各ビューには同じルートカテゴリに基づく異なるメインメニューを割り当てることができます。 各メニュー内では、厳選された厳選されたストアに適した製品を提供できます。

![カタログ階層図](./assets/catalog-hierarchy-scope.svg){width="550"}

## 製品範囲

複数の Web サイト、ストア、表示を含むインストールの場合、 [範囲](../getting-started/websites-stores-views.md#scope-settings) 設定によって、製品を販売できる場所と、各ストア表示で利用できる製品情報が決まります。 最初に、作成したすべての製品がデフォルトの Web サイト、ストア、ストア表示に公開されます。

![マルチサイトストア図](./assets/scope-multisite.svg){width="550"}

デフォルトの表示でストアを 1 つだけ持っている場合は、 [シングルストアモード](../getting-started/websites-stores-views.md#single-store-mode) スコープ設定を非表示にします。 ただし、ストアに複数のビューがある場合は、各フィールドの名前の下に範囲インジケーターが表示されます。

- 特定のビューの製品情報を編集するには、 _ストア表示_ コントロールを使用して、ビューを選択します。 ストア表示レベルで編集できる任意のフィールドに対して、追加のコントロールを使用できるようになります。

- マルチサイトインストールで製品の範囲を定義するには、 [Web サイト内の製品](settings-basic-websites.md) 製品情報のセクション。

ストア表示の商品を編集するプロセスは、その商品情報のレイヤーを追加するのと同じです。製品情報は、そのビューに固有のものです。

権限を持つサイトの製品の編集や割り当てのみが可能です。製品が割り当てられているすべてのサイトに対しては可能ではありません。

ただし、 _スペイン語_ 次の例では、「ストア表示」が選択されています。商品情報は、デフォルトのストア表示の元の言語で表示されます。 製品情報を翻訳するには、 _スペイン語_ テキストフィールド（製品のタイトル、説明、メタデータなど）を保存および翻訳します。 詳しくは、 [製品のローカライズ](../stores-purchase/store-localize.md#localize-products).

## 別の表示での製品の編集

>[!NOTE]
>
>The _すべてのストア表示回数_ 製品が許可された範囲外にも公開されると、特定の範囲に制限された管理者ユーザーに対しては、範囲が無効になります。 制限されたユーザーは実行できないので、編集可能な最初の範囲がデフォルトで選択されています _global_ アクセス権のない範囲に影響を与えるアクションまたはアクション。

1. 左上隅で、 **[!UICONTROL Store View]** を、編集する特定のビューに追加します。

1. 範囲の変更を確認するには、 **[!UICONTROL OK]**.

1. ストア表示の新しい値でフィールドを更新します。

   ストア表示用に編集できるフィールドの下に、チェックボックスが表示されます。 デフォルト値を上書きするには、「 **デフォルト値を使用** チェックボックス。

   ![スペイン語のストア表示の製品名を翻訳しています](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save]**.

1. 左上隅で、 **[!UICONTROL Store View]** 選択をデフォルトに戻します。

1. ストアでの変更を確認するには、次の手順を実行します。

   - 右上隅で、 _管理者_ メニュー矢印をクリックし、「 **[!UICONTROL Customer View]**.

     ![顧客ビュー](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - ストアの右上隅で、 **[!UICONTROL Language Chooser]** をクリックして、編集した商品のストア表示に移動し、その表示用に編集した商品を検索します。

     ![言語の選択](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
