---
title: 上部ナビゲーション
description: 様々な部門に対してディレクトリのように機能するストアのメインメニューを定義する方法について説明します。
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# 上部ナビゲーション

ストアのメインメニューは、ストア内の様々な部門へのディレクトリのようなものです。 各オプションは、異なるカテゴリの製品を表します。 上部ナビゲーションの位置と表示は、テーマによって異なる場合がありますが、動作は基本的に同じです。

![上部ナビゲーション](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

カタログのカテゴリ構造は、検索エンジンでサイトのインデックスがどの程度作成されるかに影響を与える可能性があります。 カテゴリが深くネストされるほど、完全にインデックス化される可能性が低くなります。 一般に、1 ～ 3 段階の可視レベルを使用するのが最も効果的です。 この [ルートカテゴリ](category-root.md) 最初のレベルとしてカウントされますが、メニューには表示されません。 上部のナビゲーションで使用できるレベルの最大数は、設定によって決まります。 また、ストアテーマでサポートされるメニューレベルの数に制限が生じる場合があります。 例えば、サンプルの Luma テーマは、ルートを含む最大 5 つのレベルをサポートしています。

## メニューレベルのカウント

| 項目 | 説明 |
|--- |--- |
| 第一級 | 最初のレベルはルートカテゴリで、サンプルデータでは「デフォルトのカテゴリ」という名前が付けられています。 ルートはメニューのコンテナであり、その名前はメニューのオプションとして表示されません。 |
| 第二級 | デスクトップディスプレイの場合、上部のナビゲーションは、ページ上部に表示されるメインメニューです。 モバイルデバイスでは、通常、メインメニューはオプションのフライアウトメニューとして表示されます。 Luma ストアの第 2 レベルオプションは次のとおりです _新機能_, _女性_, _男性_, _歯車_, _Training_、および _販売_. |
| 第三級 | 3 番目のレベルは、各メインメニューオプションの下に表示されます。 例えば、の下です _女性_&#x200B;第 3 レベルのオプションは次のとおりです _Tops_ および _底_. |
| 第四級 | 第 4 レベルのオプションは、第 3 レベルのオプションから飛び出すサブカテゴリです。 例えば、の下です _Tops_&#x200B;第 4 レベルのメニューオプションは次のとおりです _ジャケット_, _パーカー&amp;スウェットシャツ_, _ティー_、および _ブラス&amp;タンク_. |

{style="table-layout:auto"}

## 上部ナビゲーションの設定

カテゴリをストアの上部ナビゲーションに表示するには、次の手順を実行します。

### 手順 1：カテゴリの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. を設定 **[!UICONTROL Store View]** 新しいカテゴリを使用できる場所を決定します。

1. カテゴリ ツリーで、新しいカテゴリの親カテゴリを選択します。

   データを使用せずに最初から開始する場合、リストには次の 2 つのカテゴリしかない可能性があります。 _既定のカテゴリ_、はルートで、 _カテゴリの例_.

1. クリック **[!UICONTROL Add Subcategory]**.

1. 基本情報を次の設定で入力します。

   - **[!UICONTROL Enable Category]** をに設定 `Yes`
   - **[!UICONTROL Include in Menu]** をに設定 `Yes`

1. 表示設定で設定 **[!UICONTROL Anchor]** 対象： `Yes`.

1. その他の必要な作業を完了する [カテゴリ設定](category-create.md).

1. 完了したら、 **[!UICONTROL Save]**.

マルチストアインストールでは、別のメインメニューを [ルートカテゴリ](category-root.md) for each [store](../stores-purchase/stores.md#add-stores).

### 手順 2：上部ナビゲーションの深度の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開します。 **[!UICONTROL Category Top Navigation]** セクション。

   ![カテゴリのトップ ナビゲーション](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   上部ナビゲーションの深さにはグローバルな特徴があるからです [設定スコープ](../getting-started/websites-stores-views.md#scope-settings)この設定は、Commerceのインストール環境におけるすべての web サイト、ストア、ストアビューに適用されます。 この _[!UICONTROL Category Top Navigation]_「設定」セクションは、_[!UICONTROL Store View]_ 左上隅のをに設定します。 `Default Config`.

   これらのオプションの詳細なリストについては、を参照してください [カテゴリのトップ ナビゲーション](../configuration-reference/catalog/catalog.md#layered-navigation) が含まれる _設定リファレンス_.

1. 上部ナビゲーションに表示されるサブカテゴリの数を制限するには、次の数を入力します **[!UICONTROL Maximal Depth]**.

   デフォルト値はです `0`サブカテゴリレベルの数に制限はありません。

1. 完了したら、 **[!UICONTROL Save Config]**.
