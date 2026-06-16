---
title: ルートカテゴリと階層
description: カテゴリ階層と、カテゴリ ツリーのメインメニューのコンテナとして機能するルート カテゴリについて説明します。
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# ルートカテゴリと階層

メインメニューの製品は、[ ストア ](../stores-purchase/stores.md#add-stores)に割り当てられているルートカテゴリによって決まります。 ルートカテゴリは、基本的にカテゴリーツリー内のメインメニューのコンテナです。 まったく新しい製品セットを使用してルートカテゴリを作成したり、既存のルートカテゴリから製品をコピーしたりできます。 ルートカテゴリは、現在のストアまたは同じweb サイト内の他のストアに割り当てることができます。

![ カタログ階層図](./assets/catalog-hierarchy-scope.svg){width="550"}

管理画面では、カテゴリ構造は上下の逆さまのツリーのようになり、ルートが上に表示されます。 ルートには名前がありますが、URL キーがなく、ストアの[上部ナビゲーション ](navigation-top.md)には表示されません。 メニュー内の他のすべてのカテゴリは、ルートの下にネストされます。 ルートカテゴリはカタログの最高レベルであるため、ストアは一度に1つのルートカテゴリのみをアクティブにできます。 ただし、別のカタログ構造や別のストア用に追加のルートカテゴリを作成することもできます。

次の例は、ルートカテゴリを作成して別のストアに割り当てる方法を示しています。

## 手順1：ルートカテゴリの作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. 左側で、**[!UICONTROL Add Root Category]**&#x200B;をクリックします。

   ![新しいルートカテゴリ ](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. **[!UICONTROL Category Name]**&#x200B;を入力します。

   選択した名前は、最初にすべてのストアビューに割り当てられます。

1. 現在のカタログから商品をカタログに追加する場合は、次の操作を行います。

   - カテゴリー&#x200B;_セクションの_&#x200B;製品の![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   - [検索フィルター](../getting-started/admin-grid-controls.md)を使用して、目的の商品を検索し、新しいカタログにコピーする各商品のチェックボックスを選択します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## ステップ 2：メインメニューの作成

1. 左側で、前の手順で作成した新しいルートカテゴリを選択します。

1. メインメニューの[ カテゴリ構造](category-create.md)を作成するには、**[!UICONTROL Add Subcategory]**&#x200B;をクリックし、指示に従います。

## 手順3：ルート カテゴリをストアに割り当てる

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**に移動します。

1. グリッドの&#x200B;_ストア_&#x200B;列で、新しいカタログを割り当てるストアをクリックします。

1. **[!UICONTROL Root Category]**&#x200B;を、作成した新しいルート カテゴリに設定します。

1. ストアに&#x200B;**[!UICONTROL Default Store View]**&#x200B;が割り当てられていることを確認してください。

   ストアには、少なくとも1つの[ ストアビュー](../stores-purchase/store-views.md)が必要です。

1. 完了したら、**[!UICONTROL Save Store]**&#x200B;をクリックします。

1. ストアに新しいカタログがあることを確認するには、次の操作を行います。

   - _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

     新しいカタログにコピーされた商品はすべてグリッドに表示されます。

   - 新しいカタログとメインメニューが正しく機能していることを確認するには、ストアフロントにアクセスしてください。
