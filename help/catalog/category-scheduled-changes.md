---
title: カテゴリのスケジュール済み変更
description: マーケティングキャンペーンやストアプロモーションをサポートするために、カテゴリの変更をスケジュールする方法を説明します。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# カテゴリのスケジュール済み変更

{{ee-feature}}

カテゴリの更新はスケジュールに従って適用でき、他のコンテンツの変更と共にグループ化できます。 カテゴリに対してスケジュールされた変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。 詳しくは、[ コンテンツのステージング ](../content-design/content-staging.md) を参照してください。

>[!NOTE]
>
>[!UICONTROL Schedule Design Update] タブは、![Adobe Commerce](../assets/adobe-logo.svg)Adobe Commerceで削除されており、カテゴリで直接変更することはできません。 これらのアクティベーションに対して、スケジュールされた更新を作成する必要があります。

>[!NOTE]
>
>スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも一度に 1 つのスケジュールされた更新しか持つことができません。 スケジュールされた更新は、その期間内のすべてのストアビューに適用されます。 その結果、1 つのエンティティに対して、異なるストア表示の複数のスケジュールされた更新を同時に行うことはできません。 現在スケジュールされている更新の影響を受けないすべてのストアビュー内のすべてのエンティティ属性値は、前回スケジュールされた更新ではなく、デフォルト値から取得されます。

## カテゴリの更新をスケジュール

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. 左側のカテゴリ ツリーで、変更するカテゴリを選択します。

1. ページ上部の _スケジュールされた変更_ ボックスで、「**[!UICONTROL Schedule New Update]** 更」をクリックします。

   ![ スケジュールされた変更 ](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save as a New Update]** オプションを選択した状態で、更新の基本パラメーターを設定します。

   - **[!UICONTROL Update Name]**：新しいコンテンツのステージングキャンペーンの名前を入力します。

   - 更新の簡単な **[!UICONTROL Description]** と使用方法を入力します。

   - カレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）ツールを使用して、キャンペーンの **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** を選択します。

   >[!IMPORTANT]
   >
   >Campaign **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** は、各 web サイトのローカルタイムゾーンから変換される **_デフォルト_** の管理タイムゾーンを使用して定義する必要があります。 例えば、米国のタイムゾーンをベースにキャンペーンを開始する、異なるタイムゾーンの複数の web サイトでは、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 それぞれの **[!UICONTROL Start Date]** と **[!UICONTROL End Date]** を設定します。これらは、ローカル Web サイトのタイムゾーンからデフォルトの管理者のタイムゾーンに変換されます。

   ![ スケジュールされた変更 ](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. スケジュールされている更新に必要な変更を加えます。

1. 変更をプレビューするには、右上のボタンバーの「**[!UICONTROL Preview]**」をクリックします。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 既存の更新に割り当てる

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. 左側のカテゴリ ツリーで、変更するカテゴリを選択します。

1. ページ上部の _スケジュールされた変更_ ボックスで、「**[!UICONTROL Schedule New Update]** 更」をクリックします。

1. 「**[!UICONTROL Assign to Existing Campaign]**」を選択します。

1. リストで必要なキャンペーンを見つけて、「**[!UICONTROL Select]**」をクリックします。

1. スケジュールされている更新に対して必要な変更を行います。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   >[!NOTE]
   >
   >キャンペーンが複数のカテゴリにリンクされている場合、キャンペーンは、[ コンテンツのステージングダッシュボード ](../content-design/content-staging-dashboard.md) からのみ編集できます。