---
title: 製品アップデートのスケジュール設定
description: キャンペーンやプロモーションプログラムをサポートするために、製品リストの変更をスケジュールする方法を説明します。
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 2cdf3452f1648dc1ed607d6dfb5ade4be5ed5ce9
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# 製品アップデートのスケジュール設定

{{ee-feature}}

製品のアップデートはスケジュールに従って適用でき、他のコンテンツの変更とグループ化できます。 [ コンテンツのステージング ](../content-design/content-staging.md) を使用して、製品に対してスケジュールされた変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。

製品のアップデートのスケジュールを設定し、キャンペーンを編集する場合は、次の点に注意してください。

- スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも一度に 1 つのスケジュールされた更新しか持つことができません。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、1 つのエンティティに対して、異なるストア表示の異なるスケジュールされた更新を同時に行うことはできません。 現在スケジュールされている更新の影響を受けないすべてのストアビュー内のすべてのエンティティ属性値は、前回スケジュールされた更新ではなく、デフォルト値から取得されます。

- スケジュールされた更新のステージングプレビューは、常に **デフォルト** のストア表示から開始されます。この表示は、ステージング更新キャンペーンをナビゲートする顧客のエクスペリエンスをエミュレートします。

- キャンペーンが複数の製品にリンクされている場合、キャンペーンは、[ コンテンツのステージングダッシュボード ](../content-design/content-staging-dashboard.md) からのみ編集できます。

- アクティブなキャンペーンが最初に終了日なしで作成された場合、後でキャンペーンを編集して終了日を含めることはできません。 この場合、重複するキャンペーンを作成し、必要な終了日を入力する必要があります。


>[!NOTE]
>
>[!UICONTROL Set Product as New From] および [!UICONTROL To] フィールドと「[!UICONTROL Schedule Design Update]」タブは、![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceで削除され、商品で直接変更できません。 これらのアクティベーションに対して、スケジュールされた更新を作成する必要があります。

## スケジュールされた更新を作成

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 既存の製品を選択し、「**[!UICONTROL Edit]**」をクリックします。

1. 「**[!UICONTROL Schedule New Update]**」をクリックします。

1. 「**[!UICONTROL Save as a New Update]**」を選択します。

1. **[!UICONTROL Update Name]**：新しいコンテンツのステージングキャンペーンの名前を入力します。

1. 更新の簡単な **[!UICONTROL Description]** と使用方法を入力します。

1. カレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）ツールを使用して、キャンペーンの **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** を選択します。

   >[!NOTE]
   >
   >Campaign **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** は、各 web サイトのローカルタイムゾーンから変換される **_デフォルト_** の管理タイムゾーンを使用して定義する必要があります。 例えば、米国のタイムゾーンをベースにキャンペーンを開始する、異なるタイムゾーンの複数の web サイトでは、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 それぞれに **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** を設定し、ローカル Web サイトのタイムゾーンからデフォルトの管理者のタイムゾーンに変換されます。

   ![ 新しい更新としてスケジュール ](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. _[!UICONTROL Price]_まで下にスクロールし、「**[!UICONTROL Advanced Pricing]**」をクリックします。

1. スケジュール済みキャンペーン中に製品の **[!UICONTROL Special Price]** を入力し、「**[!UICONTROL Done]**」をクリックします。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 既存の更新に割り当て

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 既存の製品を選択し、「**[!UICONTROL Edit]**」をクリックします。

1. 「**[!UICONTROL Schedule New Update]**」をクリックします。

1. 「**[!UICONTROL Assign to Existing Campaign]**」を選択します。

1. リストで、変更するキャンペーンを選択します。

   ![ 既存のキャンペーンへの割り当て ](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. ![ 展開セレクター ](../assets/icon-display-expand.png) **[!UICONTROL Content]** を展開します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## スケジュールされた変更を表示

スケジュールされた変更が、キャンペーンの開始日と終了日と共に、製品ページの上部に表示されます。

![ スケジュールされた変更 ](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## スケジュールされた変更の編集

1. ページ上部の _[!UICONTROL Scheduled Changes]_ボックスで、[**[!UICONTROL View/Edit]**] をクリックします。

1. スケジュールされている更新に必要な変更を加えます。

1. 「**[!UICONTROL Save]**」をクリックします。

## スケジュールされている変更を削除

1. ページ上部の _[!UICONTROL Scheduled Changes]_ボックスで、[**[!UICONTROL View/Edit]**] をクリックします。

1. 上部のバーで「**[!UICONTROL Remove from Update]**」をクリックします。

   ![ スケジュールされた変更を削除 ](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. ダイアログで、「**[!UICONTROL Delete the Update]**」を選択し、「**[!UICONTROL Done]**」をクリックします。

   製品がアップデートから削除され、スケジュールされているすべての変更が失われます。

## 設計の更新をスケジュールする

{{ce-feature}}

_[!UICONTROL Schedule Design Update]_のセクションでは、製品ページの外観を一時的に変更できます。 デザインの変更は、シーズンやプロモーションに合わせてスケジュールを設定することも、新鮮なものにするためだけにスケジュールを設定することもできます。 デザインの変更は事前にスケジュールできるので、定義したスケジュールに従って有効または_ ドリップ _されます。

![ スケジュールされたデザインの更新 ](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 製品にカスタムレイアウトが適用された場合の日付範囲を決定します。 |
| [!UICONTROL New Theme] | カスタムテーマを製品に適用します。 |
| [!UICONTROL New Layout] | 製品ページに別のレイアウトを適用します。 オプション：<br/>**[!UICONTROL No layout updates]**- デフォルトでは、製品ページのレイアウトのアップデートは使用できません。<br/>**[!UICONTROL Empty]** - 4 列のページなど、独自のレイアウトを定義できます。 （XML を理解している必要があります）。 <br/>**[!UICONTROL 1 column]**– 製品ページに 1 列のレイアウトを適用します。<br/>**[!UICONTROL 2 columns with left bar]** – 左サイドバーを含む 2 列のレイアウトを製品ページに適用します。 <br/>**[!UICONTROL 2 columns with right bar]**– 右サイドバーを含む 2 列のレイアウトを製品ページに適用します。<br/>**[!UICONTROL 3 columns]** - 3 列のレイアウトを製品ページに適用します。 |

{style="table-layout:auto"}
