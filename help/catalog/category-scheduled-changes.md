---
title: カテゴリに対する予定変更
description: マーケティングキャンペーンをサポートし、プロモーションを保存するために、カテゴリの変更をスケジュールする方法を説明します。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# カテゴリに対する予定変更

{{ee-feature}}

カテゴリの更新は、スケジュールに従って適用し、他のコンテンツの変更と共にグループ化できます。 カテゴリに対する予定された変更に基づいてキャンペーンを作成したり、変更を既存のキャンペーンに適用したりできます。 詳しくは、 [コンテンツのステージング](../content-design/content-staging.md).

>[!NOTE]
>
>スケジュールされたすべての更新は連続して適用されます。つまり、どのエンティティも一度に 1 つのスケジュールされた更新のみを持つことができます。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、異なるストア表示に対して、エンティティが複数のスケジュール済み更新を同時に持つことはできません。 現在のスケジュール済み更新の影響を受けない、すべてのストア表示内のすべてのエンティティ属性値は、以前のスケジュール済み更新の値ではなく、デフォルト値から取得されます。

## カテゴリの更新をスケジュールする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリツリーで、変更するカテゴリを選択します。

1. Adobe Analytics の _予定されている変更_ 」ボックスをクリックします。 **[!UICONTROL Schedule New Update]**.

   ![予定されている変更](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. を使用 **[!UICONTROL Save as a New Update]** オプションを選択した場合、更新の基本パラメーターを設定します。

   - の場合 **[!UICONTROL Update Name]**」に、新しいコンテンツステージングキャンペーンの名前を入力します。

   - 概要を入力 **[!UICONTROL Description]** を更新し、その使用方法を示します。

   - カレンダー ( ![カレンダーアイコン](../assets/icon-calendar.png) ) ツールを使用して **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** キャンペーンの。

   >[!IMPORTANT]
   >
   >Campaign **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** は、 **_デフォルト_** 管理者タイムゾーン。各 Web サイトのローカルタイムゾーンから変換されます。 例えば、異なるタイムゾーンの複数の Web サイトで、米国のタイムゾーンに基づいてキャンペーンを開始する場合、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 次の項目を設定します。 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** それぞれに対して（ローカル web サイトのタイムゾーンからデフォルトの管理者タイムゾーンに変換されます）。

   ![予定されている変更](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. スケジュールされた更新に必要な変更を加えます。

1. 変更をプレビューするには、 **[!UICONTROL Preview]** をクリックします。

1. 完了したら、「 **[!UICONTROL Save]**.

## 既存の更新に割り当て

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリツリーで、変更するカテゴリを選択します。

1. Adobe Analytics の _予定されている変更_ 」ボックスをクリックします。 **[!UICONTROL Schedule New Update]**.

1. 選択 **[!UICONTROL Assign to Existing Campaign]**.

1. リストで、必要なキャンペーンを見つけて、 **[!UICONTROL Select]**.

1. スケジュールされた更新に必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save]**.
