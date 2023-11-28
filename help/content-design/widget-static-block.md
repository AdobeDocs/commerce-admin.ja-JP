---
title: ウィジェットを使用してブロックを配置する
description: 静的ブロックウィジェットを使用して、ストア内のほぼ任意の場所に既存のコンテンツを配置する方法を説明します。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# ウィジェットを使用してブロックを配置する

The _CMS 静的ブロック_ [widget](widgets.md) を使用すると、既存の [コンテンツブロック](blocks.md) お店のほとんどどこにでも

![ウィジェット](./assets/widgets.png){width="700" zoomable="yes"}

## 手順 1：ウィジェットのタイプを選択する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅で、 **[!UICONTROL Add Widget]**.

1. Adobe Analytics の _設定_ セクション、設定 **[!UICONTROL Type]** から `CMS Static Block` をクリックします。 **[!UICONTROL Continue]**.

1. 次を確認します。 **[!UICONTROL Design Theme]** を現在のテーマに設定し、 **[!UICONTROL Continue]**.

   ![ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Storefront Properties]_セクションで、以下の操作を実行します。

   - の場合 **[!UICONTROL Widget Title]**」で、ウィジェットの説明的なタイトルを入力します。

     このタイトルは、 _管理者_.

   - の場合 **[!UICONTROL Assign to Store Views]**」で、ウィジェットを表示するストア表示回数を選択します。

     特定のストア表示を選択するか、 `All Store Views`. 複数のビューを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

   - （オプション）の場合 **[!UICONTROL Sort Order]**」、数値を入力して、この項目がページの同じ部分に他の項目と共に表示される順序を決定します。 (`0` =最初 `1` =秒 `3` = 3 番目、など )

     ![ストアフロントのプロパティ](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 手順 2：ウィジェットレイアウトの更新を完了する

1. Adobe Analytics の _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**.

1. 設定 **[!UICONTROL Display On]** を、ブロックを表示するカテゴリ、製品またはページに追加します。

1. ブロックを特定のページに配置するには、次の操作を行います。

   - を選択します。 **[!UICONTROL Page]** ブロックを表示する場所です。

   - を選択します。 **[!UICONTROL Block Reference]** は、ページ上でブロックが表示される場所を識別します。

   - のデフォルト設定を受け入れる **[!UICONTROL Template]**（に設定） `CMS Static Block Default Template`.

     ![レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### レイアウト更新オプション

| フィールド | 説明 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | アンカーカテゴリページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**— アンカーが表示されるカテゴリ。 オプション： `All` /`Specific Categories`<br/>**[!UICONTROL Container]**  — コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**[!UICONTROL Template]**— レイアウトのテーマを決定します。 |
| [!UICONTROL Non-Anchor Categories] | アンカーのないカテゴリページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**— アンカーが表示されるカテゴリ。 オプション： `All` /`Specific Categories`<br/>**[!UICONTROL Container]**  — コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**[!UICONTROL Template]**— レイアウトのテーマを決定します。 |
| **_[!UICONTROL Products]_** |  |
| すべての製品タイプ | ウィジェットを特定のタイプの製品ページまたはすべての製品ページに表示します。 <br/>**[!UICONTROL Products]**— ウィジェットが表示される製品。 オプション： `All` /` Specific Products`<br/>**[!UICONTROL Container]**  — コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**[!UICONTROL Template]**— レイアウトのテーマを決定します。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | すべてのページにウィジェットを表示します。 <br/>**[!UICONTROL Container]**— コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**[!UICONTROL Template]**  — レイアウトのテーマを決定します。 |
| [!UICONTROL Specified Page] | 特定のページにウィジェットを表示します。 オプション：<br/>**[!UICONTROL Page]**— ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]**  — コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**テンプレート**  — レイアウトのテーマを決定します。 |
| [!UICONTROL Page Layouts] | 特定のレイアウトでウィジェットをページに表示します。 <br/>**[!UICONTROL Page]**— ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]**  — コンテナを、ウィジェットを表示するページレイアウトの部分に設定します。<br/>**[!UICONTROL Template]**— レイアウトのテーマを決定します。 |

{style="table-layout:auto"}

## 手順 3：ブロックを配置する

1. 左のパネルで、「 」を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block…]** をクリックし、リストから配置するブロックを選択します。

1. 完了したら、「 **[!UICONTROL Save]**.

   アプリがリストに表示されます。

1. プロンプトが表示されたら、ページ上部の手順に従って、インデックスとページキャッシュを更新します。

1. ストアフロントに戻り、ブロックが正しい場所に表示されていることを確認します。

   ブロックを移動するには、ウィジェットを再度開くか、別のページまたはブロック参照を試すことができます。
