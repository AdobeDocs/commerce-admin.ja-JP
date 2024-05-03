---
title: 製品アップデートのスケジュール設定
description: キャンペーンやプロモーションプログラムをサポートするために、製品リストの変更をスケジュールする方法を説明します。
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 製品アップデートのスケジュール設定

{{ee-feature}}

製品のアップデートはスケジュールに従って適用でき、他のコンテンツの変更とグループ化できます。 次を使用できます [コンテンツのステージング](../content-design/content-staging.md) 製品に対してスケジュールされた変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。

>[!NOTE]
>
>この [!UICONTROL Set Product as New From] および [!UICONTROL To] フィールドと [!UICONTROL Schedule Design Update] タブが削除されました ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceおよびを商品で直接変更することはできません。 これらのアクティベーションに対して、スケジュールされた更新を作成する必要があります。

>[!NOTE]
>
>スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも一度に 1 つのスケジュールされた更新しか持つことができません。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、1 つのエンティティに対して、異なるストア表示の異なるスケジュールされた更新を同時に行うことはできません。 現在スケジュールされている更新の影響を受けないすべてのストアビュー内のすべてのエンティティ属性値は、前回スケジュールされた更新ではなく、デフォルト値から取得されます。

>[!NOTE]
>
>スケジュールされた更新のステージングプレビューは、常に以下から開始します。 **default** ストア表示。ステージング更新キャンペーンを通じて移動する顧客のエクスペリエンスをエミュレートします。

## スケジュールされた更新を作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 既存の製品を選択し、 **[!UICONTROL Edit]**.

1. クリック **[!UICONTROL Schedule New Update]**.

1. を選択 **[!UICONTROL Save as a New Update]**.

1. の場合 **[!UICONTROL Update Name]**、新しいコンテンツのステージングキャンペーンの名前を入力します。

1. 概要を入力 **[!UICONTROL Description]** 更新の概要と使用方法。

1. カレンダーの使用（![カレンダーアイコン](../assets/icon-calendar.png)）を選択します。 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** キャンペーン用。

   >[!NOTE]
   >
   >キャンペーン **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** を使用して定義する必要があります。 **_default_** 管理タイムゾーン （各 web サイトのローカルタイムゾーンから変換されます）。 例えば、米国のタイムゾーンをベースにキャンペーンを開始する、異なるタイムゾーンの複数の web サイトでは、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 を設定 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** それぞれに対して、ローカル web サイトのタイムゾーンからデフォルトの管理者タイムゾーンに変換されます。

   ![新しい更新としてスケジュール](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Scroll down to _[!UICONTROL Price]_をクリックして、**[!UICONTROL Advanced Pricing]**.

1. を入力 **[!UICONTROL Special Price]** スケジュールされたキャンペーン中の製品のを選択し、 **[!UICONTROL Done]**.

1. 完了したら、 **[!UICONTROL Save]**.

## 既存の更新に割り当て

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 既存の製品を選択し、 **[!UICONTROL Edit]**.

1. クリック **[!UICONTROL Schedule New Update]**.

1. を選択 **[!UICONTROL Assign to Existing Campaign]**.

1. リストで、変更するキャンペーンを選択します。

   ![既存のキャンペーンへの割り当て](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. 完了したら、 **[!UICONTROL Save]**.

## スケジュールされた変更を表示

スケジュールされた変更が、キャンペーンの開始日と終了日と共に、製品ページの上部に表示されます。

![スケジュールされた変更](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## スケジュールされた変更の編集

1. が含まれる _[!UICONTROL Scheduled Changes]_ページの上部にあるボックスで、**[!UICONTROL View/Edit]**.

1. スケジュールされている更新に必要な変更を加えます。

1. クリック **[!UICONTROL Save]**.

## スケジュールされている変更を削除

1. が含まれる _[!UICONTROL Scheduled Changes]_ページの上部にあるボックスで、**[!UICONTROL View/Edit]**.

1. 上部バーで、 **[!UICONTROL Remove from Update]**.

   ![スケジュールされた変更を削除](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. ダイアログで、を選択します。 **[!UICONTROL Delete the Update]** をクリックして、 **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >製品がアップデートから削除され、スケジュールされているすべての変更が失われます。

## 設計の更新をスケジュールする

{{ce-feature}}

この _[!UICONTROL Schedule Design Update]_「」セクションでは、製品ページの外観を一時的に変更できます。 デザインの変更は、シーズンやプロモーションに合わせてスケジュールを設定することも、新鮮なものにするためだけにスケジュールを設定することもできます。 デザインの変更は事前にスケジュールできるので、次の場合に有効になります。_&#x200B;点滴&#x200B;_、定義したスケジュールに従います。

![スケジュールされたデザインの更新](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 製品にカスタムレイアウトが適用された場合の日付範囲を決定します。 |
| [!UICONTROL New Theme] | カスタムテーマを製品に適用します。 |
| [!UICONTROL New Layout] | 製品ページに別のレイアウトを適用します。 オプション： <br/>**[!UICONTROL No layout updates]**- デフォルトでは、製品ページのレイアウトのアップデートは利用できません。<br/>**[!UICONTROL Empty]** - 4 列のページなど、独自のレイアウトを定義できます。 （XML を理解している必要があります）。 <br/>**[!UICONTROL 1 column]**– 製品ページに 1 列のレイアウトを適用します。<br/>**[!UICONTROL 2 columns with left bar]**  – 左サイドバーを含む 2 列のレイアウトを製品ページに適用します。 <br/>**[!UICONTROL 2 columns with right bar]**– 右サイドバーを含む 2 列のレイアウトを製品ページに適用します。<br/>**[!UICONTROL 3 columns]** - 3 列のレイアウトを製品ページに適用します。 |

{style="table-layout:auto"}
