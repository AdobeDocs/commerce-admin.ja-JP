---
title: 上部ナビゲーション
description: ストアのメインメニューを定義する方法について説明します。このメニューは、各部門のディレクトリのように機能します。
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/REad4AtBdJeK2eVNRo1XiTrrjJqmTs6oJfum260IfOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# 上部ナビゲーション

ストアのメインメニューは、ストア内のさまざまな部門へのディレクトリのようなものです。 各オプションは、異なるカテゴリの製品を表します。 上部ナビゲーションの位置と表示方法はテーマによって異なりますが、基本的には同じです。

![ トップナビゲーション ](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

カタログのカテゴリ構造は、検索エンジンによるサイトのインデックス作成方法に影響を与える可能性があります。 カテゴリを深くネストすればするほど、完全にインデックス化される可能性は低くなります。 一般的に、表示レベルを1から3つ使用するのが最も効果的です。 [ ルートカテゴリ ](category-root.md)は、最初のレベルとしてカウントされますが、メニューには表示されません。 上部ナビゲーションで使用できるレベルの最大数は、設定によって決まります。 さらに、ストアテーマでサポートされているメニューレベルの数に制限がある場合があります。 例えば、サンプル Luma テーマは、ルートを含む最大5つのレベルをサポートします。

## メニューレベルのカウント

| 項目 | 説明 |
|--- |--- |
| レベル 1 | 最初のレベルはルートカテゴリで、サンプルデータには「デフォルトカテゴリ」という名前が付けられます。 ルートはメニューのコンテナであり、その名前はメニューにオプションとして表示されません。 |
| レベル 2 | デスクトップディスプレイでは、トップナビゲーションはページの上部に表示されるメインメニューです。 モバイルデバイスでは、通常、メインメニューはオプションのフライアウトメニューとして表示されます。 Luma ストアの2番目のレベルのオプションは、_新機能_、_女性_、_男性_、_ギア_、_トレーニング_、および&#x200B;_セール_&#x200B;です。 |
| レベル 3 | 3つ目のレベルは、各メインメニューオプションの下に表示されます。 例えば、_女性_&#x200B;の下では、3番目のレベルのオプションは&#x200B;_トップ_&#x200B;と&#x200B;_ボトム_&#x200B;です。 |
| レベル 4 | 4番目のレベルのオプションは、3番目のレベルのオプションから飛び出すサブカテゴリです。 例えば、_トップス_&#x200B;の下では、4番目のレベルのメニューオプションは&#x200B;_ジャケット_、_パーカーとスウェットシャツ_、_ティー_、および&#x200B;_ブラスとタンク_&#x200B;です。 |

{style="table-layout:auto"}

## 上部ナビゲーションの設定

ストアの上部ナビゲーションにカテゴリを表示するには、次の手順を実行します。

### 手順1：カテゴリの作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. 新しいカテゴリをどこで利用できるかを決定するには、**[!UICONTROL Store View]**&#x200B;を設定します。

1. カテゴリーツリーで、新しいカテゴリの親カテゴリを選択します。

   データを持たずに最初から始める場合、リストに2つのカテゴリ（_デフォルトのカテゴリ_）と&#x200B;_例のカテゴリ_）しか含まれていない可能性があります。

1. **[!UICONTROL Add Subcategory]**&#x200B;をクリックします。

1. 基本的な情報を次の設定で入力します。

   - **[!UICONTROL Enable Category]**&#x200B;が`Yes`に設定されました
   - **[!UICONTROL Include in Menu]**&#x200B;が`Yes`に設定されました

1. 表示設定で、**[!UICONTROL Anchor]**&#x200B;を`Yes`に設定します。

1. その他の必要な[ カテゴリ設定](category-create.md)をすべて完了します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

マルチストアのインストールの場合、各[ ストア ](../stores-purchase/stores.md#add-stores)ごとに、異なるメインメニューを[ ルートカテゴリ ](category-root.md)として割り当てることができます。

### 手順2：上部ナビゲーションの深度を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. **[!UICONTROL Category Top Navigation]** セクションを展開します。

   ![ カテゴリの上位ナビゲーション ](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   上部ナビゲーションの深さはグローバルな[設定スコープ ](../getting-started/websites-stores-views.md#scope-settings)を持つため、この設定はCommerce インストールのすべてのweb サイト、ストア、ストアビューに適用されます。 _[!UICONTROL Category Top Navigation]_設定セクションは、左上隅の_[!UICONTROL Store View]_&#x200B;が`Default Config`に設定されている場合にのみ使用できます。

   これらのオプションの詳細なリストについては、_設定リファレンス_&#x200B;の[ カテゴリトップナビゲーション ](../configuration-reference/catalog/catalog.md#layered-navigation)を参照してください。

1. 上部ナビゲーションに表示されるサブカテゴリの数を制限するには、**[!UICONTROL Maximal Depth]**&#x200B;の数を入力します。

   デフォルト値は`0`で、サブカテゴリーレベルの数に制限はありません。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
