---
title: カテゴリ – デザイン設定
description: の使用について説明します [!UICONTROL Design] カテゴリ、関連付けられたすべての製品ページおよびページレイアウトのルックアンドフィールを定義するための設定。
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# カテゴリ – デザイン設定

この _[!UICONTROL Design]_セクションでは、カテゴリ、関連するすべての製品ページ、ページレイアウトのルックアンドフィールを制御できます。 プロモーションのカテゴリページとそれに関連する製品をカスタマイズしたり、カテゴリを区別したりできます。 例えば、ブランドや特別な製品ライン用に独特のデザインを作成したり、特定の期間に更新を適用したりできます。

![カテゴリのデザイン設定](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>同じ製品が、カテゴリごとに異なるデザイン設定を持つ複数のカテゴリに割り当てられている場合は、を設定することをお勧めします **製品 URL にカテゴリパスを使用** = `Yes` が含まれる [検索エンジン最適化設定オプション](../configuration-reference/catalog/catalog.md#search-engine-optimization). この設定にアクセスするには、に移動します  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**、を展開&#x200B;**[!UICONTROL Catalog]**を選択します&#x200B;**カタログ**左側のパネルの下にあるを展開します&#x200B;**検索エンジンの最適化**ページの「」セクション。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | 現在のカテゴリが親カテゴリからデザイン設定を継承できるようにします。 これを使用すると、「デザイン」セクションの他のすべてのフィールドが使用できなくなります。 オプション： `Yes` / ` No` |
| [!UICONTROL Theme] | カスタムテーマをカテゴリに適用します。 |
| [!UICONTROL Layout] | カテゴリページに別のレイアウトを適用します。 オプション： <br/>**[!UICONTROL No layout updates]**- デフォルトでは、カテゴリページに対するレイアウトの更新は使用できません。<br/>**[!UICONTROL Empty]**  – 独自のページレイアウトを定義する場合に使用します。 （XML を理解している必要があります）。 <br/>**[!UICONTROL 1 column]**- カテゴリ ページに 1 列のレイアウトを適用します。<br/>**[!UICONTROL 2 columns with left bar]**  – 左側のサイドバーを含む 2 カラムのレイアウトをカテゴリ ページに適用します。 <br/>**[!UICONTROL 2 columns with right bar]**– 右側のサイドバーを含む 2 カラムのレイアウトをカテゴリ ページに適用します。<br/>**[!UICONTROL 3 columns]** - カテゴリページに 3 列のレイアウトを適用します。<br/>**[!UICONTROL Page -- Full Width]**- （必須 [ページビルダー](../page-builder/introduction.md)） CMS ページの全幅レイアウトをカテゴリページに適用します。<br/>**[!UICONTROL Category -- Full Width]** - （ページビルダーが必要）カテゴリページの全幅レイアウトをカテゴリページに適用します。 <br/>**[!UICONTROL Product -- Full Width]**- （ページビルダーが必要）製品ページの全幅レイアウトをカテゴリページに適用します。 |
| [!UICONTROL Custom Layout Update] | サーバー上の使用可能なカスタム レイアウト更新ファイルを一覧表示します。 カテゴリに適用するカスタムレイアウトの更新を選択します。 |
| [!UICONTROL Apply Design to Products] | 選択すると、カテゴリ内のすべての製品にカスタム設定が適用されます。 |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

この _[!UICONTROL Scheduled Design Update]_このセクションでは、カテゴリ ページにカスタム デザインを適用する場合の日付範囲を指定します。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | カテゴリにカスタムレイアウトが適用される日付の範囲を決定します。 |

![スケジュールされたデザインの更新](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
