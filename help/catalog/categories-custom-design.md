---
title: カテゴリ – デザイン設定
description: '[!UICONTROL Design] 設定を使用して、カテゴリ、関連するすべての製品ページ、ページレイアウトのルックアンドフィールを定義する方法を説明します。'
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# カテゴリ – デザイン設定

_[!UICONTROL Design]_のセクションでは、カテゴリのルックアンドフィール、関連するすべての製品ページおよびページレイアウトを制御できます。 プロモーションのカテゴリページとそれに関連する製品をカスタマイズしたり、カテゴリを区別したりできます。 例えば、ブランドや特別な製品ライン用に独特のデザインを作成したり、特定の期間に更新を適用したりできます。

![ カテゴリのデザイン設定 ](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>同じ製品が、カテゴリごとに異なるデザイン設定を持つ複数のカテゴリに割り当てられる場合は、**検索エンジン最適化設定オプション [ で** 製品 URL にカテゴリパスを使用 ](../configuration-reference/catalog/catalog.md#search-engine-optimization) = `Yes` を設定することをお勧めします。 この設定にアクセスするには、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動して「**[!UICONTROL Catalog]**」を展開し、左パネルの下にある&#x200B;**カタログ**を選択して、ページの「**検索エンジンの最適化**」セクションを展開します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | 現在のカテゴリが親カテゴリからデザイン設定を継承できるようにします。 これを使用すると、「デザイン」セクションの他のすべてのフィールドが使用できなくなります。 オプション：`Yes` / ` No` |
| [!UICONTROL Theme] | カスタムテーマをカテゴリに適用します。 |
| [!UICONTROL Layout] | カテゴリページに別のレイアウトを適用します。 オプション：<br/>**[!UICONTROL No layout updates]**- デフォルトでは、カテゴリページのレイアウト更新は使用できません。<br/>**[!UICONTROL Empty]** – 独自のページレイアウトを定義する場合に使用します。 （XML を理解している必要があります）。 <br/>**[!UICONTROL 1 column]**- カテゴリページに 1 列のレイアウトを適用します。<br/>**[!UICONTROL 2 columns with left bar]** – 左側のサイドバーを含む 2 列のレイアウトをカテゴリページに適用します。 <br/>**[!UICONTROL 2 columns with right bar]**– 右側のサイドバーを含む 2 列のレイアウトをカテゴリページに適用します。<br/>**[!UICONTROL 3 columns]** - カテゴリページに 3 列のレイアウトを適用します。<br/>**[!UICONTROL Page -- Full Width]**- （[ ページビルダー ](../page-builder/introduction.md) 必要） CMS ページの全幅レイアウトをカテゴリページに適用します。<br/>**[!UICONTROL Category -- Full Width]** - （ページビルダーが必要）カテゴリページの全幅レイアウトをカテゴリページに適用します。 <br/>**[!UICONTROL Product -- Full Width]**- （ページビルダーが必要）製品ページの全幅レイアウトをカテゴリページに適用します。 |
| [!UICONTROL Custom Layout Update] | サーバー上の使用可能なカスタム レイアウト更新ファイルを一覧表示します。 カテゴリに適用するカスタムレイアウトの更新を選択します。 |
| [!UICONTROL Apply Design to Products] | 選択すると、カテゴリ内のすべての製品にカスタム設定が適用されます。 |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

_[!UICONTROL Scheduled Design Update]_セクションでは、カテゴリページにカスタムデザインが適用される日付の範囲を決定します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | カテゴリにカスタムレイアウトが適用される日付の範囲を決定します。 |

![ スケジュールされたデザインの更新 ](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
