---
title: ウィジェットを使用したブロックの配置
description: 静的ブロックウィジェットを使用して、ストア内のほぼあらゆる場所に既存のコンテンツを配置する方法を説明します。
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/LZt31t9uNhrCglxO5L8E0XfVsFrwEKcv2H-TcKF46Ng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 598
ht-degree: 0%

---

# ウィジェットを使用したブロックの配置

_CMS静的ブロック_ [&#x200B; ウィジェット &#x200B;](widgets.md)を使用すると、既存の[&#x200B; コンテンツブロック &#x200B;](blocks.md)をストア内のほぼどこにでも配置できます。

![&#x200B; ウィジェット &#x200B;](./assets/widgets.png){width="700" zoomable="yes"}

## ステップ 1：ウィジェットの種類を選択する

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Widget]**」をクリックします。

1. _設定_ セクションで、**[!UICONTROL Type]**&#x200B;を`CMS Static Block`に設定し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. **[!UICONTROL Design Theme]**&#x200B;が現在のテーマに設定されていることを確認し、**[!UICONTROL Continue]**&#x200B;をクリックします。

   ![&#x200B; ウィジェット設定](./assets/widget-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Storefront Properties]_&#x200B;セクションで、次の操作を行います。

   - 「**[!UICONTROL Widget Title]**」に、ウィジェットの説明的なタイトルを入力します。

     このタイトルは&#x200B;_管理者_&#x200B;からのみ表示されます。

   - **[!UICONTROL Assign to Store Views]**&#x200B;で、ウィジェットが表示されているストアビューを選択します。

     特定のストアビュー、または`All Store Views`を選択できます。 複数のビューを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

   - （オプション） **[!UICONTROL Sort Order]**&#x200B;の場合、ページの同じ部分で他のユーザーと一緒にこの項目を表示する順序を決定する番号を入力します。 （`0` = first, `1` = second, `3` = thirdなど）

     ![&#x200B; ストアフロントのプロパティ &#x200B;](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 手順2：ウィジェットレイアウトの更新を完了する

1. _[!UICONTROL Layout Updates]_&#x200B;セクションで、**[!UICONTROL Add Layout Update]**&#x200B;をクリックします。

1. ブロックを表示するカテゴリ、製品、またはページに&#x200B;**[!UICONTROL Display On]**&#x200B;を設定します。

1. ブロックを特定のページに配置するには、次の操作を行います。

   - ブロックを表示する&#x200B;**[!UICONTROL Page]**&#x200B;を選択します。

   - ブロックがページ上に表示される場所を特定する&#x200B;**[!UICONTROL Block Reference]**&#x200B;を選択します。

   - **[!UICONTROL Template]**&#x200B;の既定の設定を受け入れます。これは`CMS Static Block Default Template`に設定されています。

     ![&#x200B; レイアウトの更新](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### レイアウト更新オプション

| フィールド | 説明 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | アンカーカテゴリーページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション：`All` /`Specific Categories`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| [!UICONTROL Non-Anchor Categories] | アンカー以外のカテゴリ ページにウィジェットを表示します。<br/>**[!UICONTROL Categories]**- アンカーが表示されるカテゴリ。 オプション：`All` /`Specific Categories`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Products]_** |  |
| すべての製品タイプ | 特定の種類の製品ページまたはすべての製品ページにウィジェットを表示します。<br/>**[!UICONTROL Products]**- ウィジェットが表示される製品。 オプション：`All` /` Specific Products`<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | すべてのページにウィジェットを表示します。<br/>**[!UICONTROL Container]**- ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]** - レイアウトのテーマを決定します。 |
| [!UICONTROL Specified Page] | 特定ページにウィジェットを表示します。 オプション：<br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**テンプレート** - レイアウトのテーマを決定します。 |
| [!UICONTROL Page Layouts] | 特定のレイアウトを持つページにウィジェットを表示します。<br/>**[!UICONTROL Page]**- ウィジェットが表示されるページ。<br/>**[!UICONTROL Container]** - ウィジェットを表示するページレイアウトの部分にコンテナを設定します。<br/>**[!UICONTROL Template]**- レイアウトのテーマを決定します。 |

{style="table-layout:auto"}

## ステップ 3：ブロックを配置する

1. 左側のパネルで、**[!UICONTROL Widget Options]**&#x200B;を選択します。

1. **[!UICONTROL Select Block…]**&#x200B;をクリックし、リストから配置するブロックを選択します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   アプリがリストに表示されます。

1. プロンプトが表示されたら、ページの上部にある手順に従って、インデックスとページキャッシュを更新します。

1. ストアフロントに戻り、ブロックが正しい場所に表示されることを確認します。

   ブロックを移動するには、ウィジェットを再度開くか、別のページまたはブロック参照を試します。
