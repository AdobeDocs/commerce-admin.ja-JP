---
title: カテゴリのスケジュール済み変更
description: マーケティングキャンペーンやストアプロモーションをサポートするために、カテゴリの変更をスケジュールする方法を説明します。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# カテゴリのスケジュール済み変更

{{ee-feature}}

カテゴリの更新はスケジュールに従って適用でき、他のコンテンツの変更と共にグループ化できます。 カテゴリに対してスケジュールされた変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。 詳しくは、 [コンテンツのステージング](../content-design/content-staging.md).

>[!NOTE]
>
>この [!UICONTROL Schedule Design Update] タブがで削除されました ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceであり、カテゴリで直接変更することはできません。 これらのアクティベーションに対して、スケジュールされた更新を作成する必要があります。

>[!NOTE]
>
>スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも一度に 1 つのスケジュールされた更新しか持つことができません。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、1 つのエンティティに対して、異なるストア表示の複数のスケジュールされた更新を同時に行うことはできません。 現在スケジュールされている更新の影響を受けないすべてのストアビュー内のすべてのエンティティ属性値は、前回スケジュールされた更新ではなく、デフォルト値から取得されます。

## カテゴリの更新をスケジュール

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリ ツリーで、変更するカテゴリを選択します。

1. が含まれる _スケジュールされた変更_ ページの上部にあるボックスで、 **[!UICONTROL Schedule New Update]**.

   ![スケジュールされた変更](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. （を使用） **[!UICONTROL Save as a New Update]** オプションを選択して、更新の基本パラメーターを設定：

   - の場合 **[!UICONTROL Update Name]**、新しいコンテンツのステージングキャンペーンの名前を入力します。

   - 概要を入力 **[!UICONTROL Description]** 更新の概要と使用方法。

   - カレンダーの使用（ ![カレンダーアイコン](../assets/icon-calendar.png) ）を選択します。 **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** キャンペーン用。

   >[!IMPORTANT]
   >
   >キャンペーン **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** を使用して定義する必要があります。 **_default_** 各 web サイトのローカルタイムゾーンから変換される管理タイムゾーン。 例えば、米国のタイムゾーンをベースにキャンペーンを開始する、異なるタイムゾーンの複数の web サイトでは、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 を設定します **[!UICONTROL Start Date]** および **[!UICONTROL End Date]** それぞれに対して、ローカルの web サイトのタイムゾーンからデフォルトの管理者のタイムゾーンに変換されます。

   ![スケジュールされた変更](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. スケジュールされている更新に必要な変更を加えます。

1. 変更をプレビューするには、をクリックします **[!UICONTROL Preview]** 右上のボタンバーに

1. 完了したら、 **[!UICONTROL Save]**.

## 既存の更新に割り当てる

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリ ツリーで、変更するカテゴリを選択します。

1. が含まれる _スケジュールされた変更_ ページの上部にあるボックスで、 **[!UICONTROL Schedule New Update]**.

1. を選択 **[!UICONTROL Assign to Existing Campaign]**.

1. リストで必要なキャンペーンを見つけて、 **[!UICONTROL Select]**.

1. スケジュールされている更新に対して必要な変更を行います。

1. 完了したら、 **[!UICONTROL Save]**.
