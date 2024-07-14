---
title: ギフト レジストリ検索の追加
description: 来店者が顧客レジストリから商品を購入するのに役立つ、ギフトレジストリ検索ボックスを配置する方法を説明します。
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# ギフト レジストリ検索の追加

{{ee-feature}}

[ ウィジェット ](../content-design/widgets.md) ツールを使用すると、ストア内の最も多くの場所にギフトレジストリ検索ボックスを配置できます。 名前、メールアドレス、ギフトレジストリ ID など、顧客が使用できる検索オプションを指定できます。 顧客が「検索」ボタンをクリックすると、結果が「ギフトレジストリの検索」ページに表示されます。 検索で結果が返されない場合は、他のパラメーターを使用して再試行できます。

![ ストアフロントの例 – ギフトレジストリ検索 ](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## ギフト レジストリ検索の構成

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. 「**[!UICONTROL Settings]**」タブを選択し、次の操作を実行します。

   - **[!UICONTROL Type]** を `Gift Registry Search` に設定します。

   - ストアで使用されるテーマに **[!UICONTROL Design Theme]** を設定します。

   - 「**[!UICONTROL Continue]**」をクリックします。

   ![ ギフトレジストリ – 検索設定 ](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. _[!UICONTROL Storefront Properties]_セクションで、次の操作を行います。

   - 内部参照の **[!UICONTROL Widget Title]** を入力します。

   - **[!UICONTROL Assign to Store Views]** を、ギフトレジストリ検索を使用できるストア表示に設定します。

   - ページ上の同じ場所に割り当てられている他のブロックがある場合に、ギフトレジストリ検索ブロックが表示される順序を決定するには、**[!UICONTROL Sort Order]** を設定します。

   ![ ギフトレジストリ – ストアフロントのプロパティ ](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. 「**[!UICONTROL Layout Updates]**」セクションで、「**[!UICONTROL Add Layout Update]**」をクリックします。

1. ギフト レジストリの検索がストア内のどこに表示されるかを確認するには、次の操作を行います。

   - ストア内のギフトレジストリ検索ブロックを表示するページに **[!UICONTROL Display On]** を設定します。

   - 必要に応じて、表示する **[!UICONTROL Categories]** を選択します。

   - ページ上の場所に **[!UICONTROL Container]** を設定して、ギフトレジストリ検索ブロックを配置します。

   ![ ギフトレジストリ – レイアウトの更新 ](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. 左側のパネルで「**[!UICONTROL Widget Options]**」を選択します。

1. サイトの訪問者がギフトレジストリを検索する方法を決定するには、次の中から該当するものを選択します。

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![ ギフトレジストリ – ウィジェットオプション ](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. ページキャッシュを更新するように求めるプロンプトが表示されたら、ワークスペース上部のメッセージに記載されているリンクをクリックし、指示に従います。

## フィールドの説明

### [!UICONTROL Settings]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | `Gift Registry Search` をウィジェットのタイプとして識別します。 |
| [!UICONTROL Design Theme] | ギフトレジストリ検索が表示されるストアで使用されるテーマ。 |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Widget Title] | 内部参照の名前。 |
| [!UICONTROL Assign to Store Views] | ギフトレジストリ検索を使用できるストア表示を識別します。 |
| [!UICONTROL Sort Order] | 割り当てられている他のブロックが同じ場所にある場合に、ギフト レジストリ検索ブロックが表示される順序を示します。 |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Display On] | ギフトレジストリ検索ブロックが表示される特定のページまたはページの種類を指定します。 |
| [!UICONTROL Categories] | 該当する場合、はギフトレジストリ検索が表示されるカテゴリページを識別します。 |
| [!UICONTROL Container] | ギフト レジストリ検索が配置されるページ レイアウト ブロックを示します。 オプションは、テンプレートとテーマによって異なります。 |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | ギフト レジストリ検索で実行できる検索の種類を決定します。 オプション：`All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
