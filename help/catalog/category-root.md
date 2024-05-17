---
title: ルートのカテゴリと階層
description: カテゴリツリーのメインメニューのコンテナとして機能するカテゴリ階層とルートカテゴリについて説明します。
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# ルートのカテゴリと階層

メインメニューの商品は、に割り当てられたルートカテゴリによって決定されます。 [store](../stores-purchase/stores.md#add-stores). ルートカテゴリは、基本的にカテゴリツリーのメインメニューのコンテナです。 まったく新しい商品セットを使用してルートカテゴリを作成したり、既存のルートカテゴリから商品をコピーしたりできます。 ルートカテゴリは、現在のストアまたは同じ web サイト内の他のストアに割り当てることができます。

![カタログ階層図](./assets/catalog-hierarchy-scope.svg){width="550"}

管理者から見ると、カテゴリ構造は逆さまのツリーのようなもので、ルートが上にあります。 ルートに名前があるが URL キーがなく、に表示されない [上部ナビゲーション](navigation-top.md) 店舗の。 メニュー内のその他すべてのカテゴリは、ルートの下にネストされます。 ルート カテゴリはカタログの最上位レベルなので、ストアが一度にアクティブにできるルート カテゴリは 1 つだけです。 ただし、別のカタログ構造や別のストア用に追加のルート カテゴリを作成することができます。

次の例は、ルートカテゴリを作成して別のストアに割り当てる方法を示しています。

## 手順 1：ルートカテゴリの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側で、 **[!UICONTROL Add Root Category]**.

   ![新しいルートカテゴリ](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Category Name]**.

   選択した名前は、最初にすべてのストアビューに割り当てられます。

1. 現在のカタログからカタログに製品を追加する場合は、次の操作を行います。

   - を展開 ![展開セレクター](../assets/icon-display-expand.png) この _カテゴリ内の製品_ セクション。

   - の使用 [フィルターを検索](../getting-started/admin-grid-controls.md) 必要な製品を検索し、新しいカタログにコピーする各製品のチェックボックスをオンにします。

1. 完了したら、 **[!UICONTROL Save]**.

## 手順 2：メインメニューの作成

1. 左側で、前の手順で作成した新しいルートカテゴリを選択します。

1. を作成するには [カテゴリ構造](category-create.md) メインメニューで、 **[!UICONTROL Add Subcategory]** 指示に従ってください。

## 手順 3：ルートカテゴリをストアに割り当てる

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. が含まれる _ストア_ グリッドの列で、新しいカタログを割り当てるストアをクリックします。

1. を設定 **[!UICONTROL Root Category]** 作成した新しいルートカテゴリに移動します。

1. その店にが入っていることを確認する **[!UICONTROL Default Store View]** 割り当て。

   ストアには少なくとも 1 つのが必要です [ストア表示](../stores-purchase/store-views.md).

1. 完了したら、 **[!UICONTROL Save Store]**.

1. ストアに新しいカタログがあることを確認するには、次の手順を実行します。

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     新しいカタログにコピーされた製品がグリッドに表示されます。

   - 新しいカタログとメインメニューが正しく機能していることを確認するには、ストアフロントにアクセスしてください。
