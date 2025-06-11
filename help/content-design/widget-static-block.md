---
title: ウィジェットを使用したブロックの配置
description: 静的ブロックウィジェットを使用して、ストア内のほぼ任意の場所に既存のコンテンツを配置する方法を説明します。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# ウィジェットを使用したブロックの配置

_CMS静的ブロック_ [widget](widgets.md) を使用すると、既存の [ コンテンツブロック ](blocks.md) をストア内のほぼどこにでも配置できます。

![ ウィジェット ](./assets/widgets.png){width="700" zoomable="yes"}

## 手順 1：ウィジェットタイプの選択

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Widgets]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. _設定_ セクションで、**[!UICONTROL Type]** を `CMS Static Block` に設定し、「**[!UICONTROL Continue]**」をクリックします。

1. **[!UICONTROL Design Theme]** が現在のテーマに設定されていることを確認し、「**[!UICONTROL Continue]**」をクリックします。

   ![ ウィジェット設定 ](./assets/widget-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Storefront Properties]_&#x200B;セクションで、次の操作を行います。

   - **[!UICONTROL Widget Title]** しくは、ウィジェットのわかりやすいタイトルを入力します。

     このタイトルは、_管理者_ からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**：ウィジェットを表示するストア表示を選択します。

     特定のストア表示を選択することも、`All Store Views` を選択することもできます。 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]** の場合は、数字を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 （`0` = 1 番目、`1` = 2 番目、`3` = 3 番目など）。

     ![ ストアフロントのプロパティ ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 手順 2：ウィジェットレイアウトのアップデートの完了

1. 「_[!UICONTROL Layout Updates]_」セクションで、「**[!UICONTROL Add Layout Update]**」をクリックします。

1. ブロックを表示するカテゴリ、製品またはページに **[!UICONTROL Display On]** を設定します。

1. 特定のページにブロックを配置するには、次の手順を実行します。

   - ブロックを表示する **[!UICONTROL Page]** を選択します。

   - ページ上でブロックが表示される場所を識別する **[!UICONTROL Block Reference]** を選択します。

   - `CMS Static Block Default Template` に設定されている **[!UICONTROL Template]** のデフォルト設定を受け入れます。

     ![ レイアウトの更新 ](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### レイアウト更新オプション

| フィールド | 説明 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | アンカーカテゴリページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション：`All`/`Specific Categories`<br/>**[!UICONTROL Container]** - ページレイアウトのウィジェットを表示する部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| [!UICONTROL Non-Anchor Categories] | アンカーカテゴリ以外のページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション：`All`/`Specific Categories`<br/>**[!UICONTROL Container]** - ページレイアウトのウィジェットを表示する部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Products]_** |  |
| すべての製品タイプ | 特定のタイプの製品ページ、またはすべての製品ページにウィジェットを表示します。 <br/>**[!UICONTROL Products]**- ウィジェットが表示される製品。 オプション：`All` /` Specific Products`<br/>**[!UICONTROL Container]** - ページレイアウトのウィジェットを表示する部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | すべてのページにウィジェットを表示します。 <br/>**[!UICONTROL Container]**- ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]** - レイアウトのテーマを決定します。 |
| [!UICONTROL Specified Page] | 特定のページにウィジェットを表示します。 Options:<br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**テンプレート** - レイアウトのテーマを決定します。 |
| [!UICONTROL Page Layouts] | 特定のレイアウトのページにウィジェットを表示します。 <br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |

{style="table-layout:auto"}

## 手順 3：ブロックを配置する

1. 左側のパネルで「**[!UICONTROL Widget Options]**」を選択します。

1. 「**[!UICONTROL Select Block…]**」をクリックし、配置するブロックをリストから選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   アプリがリストに表示されます。

1. プロンプトが表示されたら、ページ上部の指示に従ってインデックスとページキャッシュを更新します。

1. ストアフロントに戻り、ブロックが正しい場所に表示されていることを確認します。

   ブロックを移動するには、ウィジェットを再度開くか、別のページまたはブロック参照を試します。
