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

メインメニューの商品は、[store](../stores-purchase/stores.md#add-stores) に割り当てられたルートカテゴリによって決定されます。 ルートカテゴリは、基本的にカテゴリツリーのメインメニューのコンテナです。 まったく新しい商品セットを使用してルートカテゴリを作成したり、既存のルートカテゴリから商品をコピーしたりできます。 ルートカテゴリは、現在のストアまたは同じ web サイト内の他のストアに割り当てることができます。

![ カタログ階層図 ](./assets/catalog-hierarchy-scope.svg){width="550"}

管理者から見ると、カテゴリ構造は逆さまのツリーのようなもので、ルートが上にあります。 ルートには名前がありますが、URL キーがなく、ストアの [ 上部のナビゲーション ](navigation-top.md) に表示されません。 メニュー内のその他すべてのカテゴリは、ルートの下にネストされます。 ルート カテゴリはカタログの最上位レベルなので、ストアが一度にアクティブにできるルート カテゴリは 1 つだけです。 ただし、別のカタログ構造や別のストア用に追加のルート カテゴリを作成することができます。

次の例は、ルートカテゴリを作成して別のストアに割り当てる方法を示しています。

## 手順 1：ルートカテゴリの作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. 左側で、「**[!UICONTROL Add Root Category]**」をクリックします。

   ![ 新しいルートカテゴリ ](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. **[!UICONTROL Category Name]** を入力します。

   選択した名前は、最初にすべてのストアビューに割り当てられます。

1. 現在のカタログからカタログに製品を追加する場合は、次の操作を行います。

   - ![ 展開セレクター ](../assets/icon-display-expand.png) 「カテゴリ内の商品 _セクション_ を展開します。

   - [ 検索フィルター ](../getting-started/admin-grid-controls.md) を使用して必要な製品を検索し、新しいカタログにコピーする各製品のチェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 手順 2：メインメニューの作成

1. 左側で、前の手順で作成した新しいルートカテゴリを選択します。

1. メインメニューの [ カテゴリ構造 ](category-create.md) を作成するには、「**[!UICONTROL Add Subcategory]**」をクリックし、指示に従います。

## 手順 3：ルートカテゴリをストアに割り当てる

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL All Stores]**&#x200B;に移動します。

1. グリッドの _ストア_ 列で、新しいカタログを割り当てるストアをクリックします。

1. 作成した新しいルートカテゴリに **[!UICONTROL Root Category]** を設定します。

1. ストアに **[!UICONTROL Default Store View]** が割り当てられていることを確認します。

   ストアには少なくとも 1 つの [ ストア表示 ](../stores-purchase/store-views.md) が必要です。

1. 完了したら、「**[!UICONTROL Save Store]**」をクリックします。

1. ストアに新しいカタログがあることを確認するには、次の手順を実行します。

   - _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

     新しいカタログにコピーされた製品がグリッドに表示されます。

   - 新しいカタログとメインメニューが正しく機能していることを確認するには、ストアフロントにアクセスしてください。
