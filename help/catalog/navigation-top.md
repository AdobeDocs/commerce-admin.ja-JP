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

![ 上部ナビゲーション ](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

カタログのカテゴリ構造は、検索エンジンでサイトのインデックスがどの程度作成されるかに影響を与える可能性があります。 カテゴリが深くネストされるほど、完全にインデックス化される可能性が低くなります。 一般に、1 ～ 3 段階の可視レベルを使用するのが最も効果的です。 [ ルートカテゴリ ](category-root.md) は、メニューには表示されませんが、最初のレベルとしてカウントされます。 上部のナビゲーションで使用できるレベルの最大数は、設定によって決まります。 また、ストアテーマでサポートされるメニューレベルの数に制限が生じる場合があります。 例えば、サンプルの Luma テーマは、ルートを含む最大 5 つのレベルをサポートしています。

## メニューレベルのカウント

| 項目 | 説明 |
|--- |--- |
| 第一級 | 最初のレベルはルートカテゴリで、サンプルデータでは「デフォルトのカテゴリ」という名前が付けられています。 ルートはメニューのコンテナであり、その名前はメニューのオプションとして表示されません。 |
| 第二級 | デスクトップディスプレイの場合、上部のナビゲーションは、ページ上部に表示されるメインメニューです。 モバイルデバイスでは、通常、メインメニューはオプションのフライアウトメニューとして表示されます。 Luma ストアの第 2 レベルのオプションは、_新機能_、_女性_、_男性_、_歯車_、_トレーニング_、_販売_ です。 |
| 第三級 | 3 番目のレベルは、各メインメニューオプションの下に表示されます。 例えば、_Women_ の下では、3 番目のレベルのオプションは _Tops_ と _Bottoms_ です。 |
| 第四級 | 第 4 レベルのオプションは、第 3 レベルのオプションから飛び出すサブカテゴリです。 例えば、_トップ_ の下の 4 番目のレベルのメニューオプションは、_ジャケット_、_パーカーとスウェットシャツ_、_ティー_、_ブラとタンク_ です。 |

{style="table-layout:auto"}

## 上部ナビゲーションの設定

カテゴリをストアの上部ナビゲーションに表示するには、次の手順を実行します。

### 手順 1：カテゴリの作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. **[!UICONTROL Store View]** を設定して、新しいカテゴリを使用できる場所を決定します。

1. カテゴリ ツリーで、新しいカテゴリの親カテゴリを選択します。

   データを使用せずに最初から開始する場合は、リストには、ルートである _デフォルトのカテゴリ_ と _例カテゴリ_ の 2 つのカテゴリしかない可能性があります。

1. 「**[!UICONTROL Add Subcategory]**」をクリックします。

1. 基本情報を次の設定で入力します。

   - **[!UICONTROL Enable Category]** を `Yes` に設定
   - **[!UICONTROL Include in Menu]** を `Yes` に設定

1. ディスプレイ設定で、**[!UICONTROL Anchor]** を `Yes` に設定します。

1. その他の必要な [ カテゴリ設定 ](category-create.md) を入力します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

マルチストアインストールの場合、[ ストア ](../stores-purchase/stores.md#add-stores) ごとに異なるメインメニューを [ ルートカテゴリ ](category-root.md) として割り当てることができます。

### 手順 2：上部ナビゲーションの深度の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、その下の「**[!UICONTROL Catalog]**」を選択します。

1. 「**[!UICONTROL Category Top Navigation]**」セクションを展開します。

   ![ カテゴリのトップ ナビゲーション ](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   上部のナビゲーションの深度にはグローバルな [Configuration Scope](../getting-started/websites-stores-views.md#scope-settings) があるので、この設定は、Commerce インストール内のすべての web サイト、ストア、ストアビューに適用されます。 「_[!UICONTROL Category Top Navigation]_&#x200B;設定」セクションは、左上隅の「_[!UICONTROL Store View]_」が「`Default Config`」に設定されている場合にのみ使用できます。

   これらのオプションの詳細なリストについては、[ 設定リファレンス ](../configuration-reference/catalog/catalog.md#layered-navigation) の _カテゴリの上部ナビゲーション_ を参照してください。

1. 上部ナビゲーションに表示されるサブカテゴリの数を制限するには、**[!UICONTROL Maximal Depth]** の数を入力します。

   デフォルト値は `0` で、サブカテゴリレベルの数に制限はありません。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
