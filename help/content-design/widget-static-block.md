---
title: ウィジェットを使用したブロックの配置
description: 静的ブロックウィジェットを使用して、ストア内のほぼ任意の場所に既存のコンテンツを配置する方法を説明します。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# ウィジェットを使用したブロックの配置

この _CMS 静的ブロック_ [ウィジェット](widgets.md) を使用すると、既存のを配置できます [コンテンツブロック](blocks.md) お店のほぼどこにでも。

![ウィジェット](./assets/widgets.png){width="700" zoomable="yes"}

## 手順 1：ウィジェットタイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]**.

1. が含まれる _設定_ セクション、設定 **[!UICONTROL Type]** 対象： `CMS Static Block` をクリックして、 **[!UICONTROL Continue]**.

1. を確認します **[!UICONTROL Design Theme]** が現在のテーマに設定されている場合は、 **[!UICONTROL Continue]**.

   ![ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. が含まれる _[!UICONTROL Storefront Properties]_セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Widget Title]**、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、次の場所からのみ表示されます： _Admin_.

   - の場合 **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、 `All Store Views`. 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;を入力し、この項目がページの同じ部分に他のユーザーと表示される順序を決定します。 （`0` =最初、 `1` =秒、 `3` = 3 番目、など）。

     ![ストアフロントのプロパティ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 手順 2：ウィジェットレイアウトのアップデートの完了

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**.

1. を設定 **[!UICONTROL Display On]** ブロックを表示するカテゴリ、製品またはページに移動します。

1. 特定のページにブロックを配置するには、次の手順を実行します。

   - を選択します。 **[!UICONTROL Page]** ブロックを表示する場所。

   - を選択します。 **[!UICONTROL Block Reference]** は、ブロックがページ上で表示される場所を識別します。

   - のデフォルト設定を使用 **[!UICONTROL Template]**。に設定されています。 `CMS Static Block Default Template`.

     ![レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### レイアウト更新オプション

| フィールド | 説明 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | アンカーカテゴリページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション： `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| [!UICONTROL Non-Anchor Categories] | アンカーカテゴリ以外のページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション： `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Products]_** |  |
| すべての製品タイプ | 特定のタイプの製品ページ、またはすべての製品ページにウィジェットを表示します。 <br/>**[!UICONTROL Products]**- ウィジェットが表示される製品。 オプション： `All` /` Specific Products`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | すべてのページにウィジェットを表示します。 <br/>**[!UICONTROL Container]**- ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]** - レイアウトのテーマを決定します。 |
| [!UICONTROL Specified Page] | 特定のページにウィジェットを表示します。 オプション：<br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**Template** - レイアウトのテーマを決定します。 |
| [!UICONTROL Page Layouts] | 特定のレイアウトのページにウィジェットを表示します。 <br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |

{style="table-layout:auto"}

## 手順 3：ブロックを配置する

1. 左パネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block…]** そして、リストから配置するブロックを選択します。

1. 完了したら、 **[!UICONTROL Save]**.

   アプリがリストに表示されます。

1. プロンプトが表示されたら、ページ上部の指示に従ってインデックスとページキャッシュを更新します。

1. ストアフロントに戻り、ブロックが正しい場所に表示されていることを確認します。

   ブロックを移動するには、ウィジェットを再度開くか、別のページまたはブロック参照を試します。
