---
title: カテゴリの予定された変更
description: マーケティング施策やストアプロモーションをサポートするために、カテゴリの変更をスケジュールする方法を説明します。
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/OEeNwdPokv1ZM4JFV-fnphk6wWDAQuYI-hu1CCzVibg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 464
ht-degree: 0%

---

# カテゴリの予定された変更

{{ee-feature}}

カテゴリーの更新はスケジュールどおりに適用でき、他のコンテンツの変更とグループ化することも可能です。 カテゴリに予定された変更に基づいてキャンペーンを作成したり、既存のキャンペーンに変更を適用したりできます。 詳しくは、[ コンテンツのステージング ](../content-design/content-staging.md)を参照してください。

カテゴリの変更をスケジュールする場合は、次の点に注意してください。

- スケジュールされた更新はすべて連続して適用されます。つまり、どのエンティティも一度に1つのスケジュールされた更新のみを持つことができます。 スケジュールされた更新は、その時間枠内のすべてのストアビューに適用されます。 その結果、エンティティは、異なるストアビューに対して同時に複数のスケジュールされた更新を行うことはできません。 現在のスケジュールされた更新の影響を受けない、すべてのストアビュー内のすべてのエンティティ属性値は、以前のスケジュールされた更新の値ではなく、デフォルト値から取得されます。

- キャンペーンが複数のカテゴリにリンクされている場合、キャンペーンは[ コンテンツステージングダッシュボード ](../content-design/content-staging-dashboard.md)からのみ編集できます。

- キャンペーンが複数のカテゴリにリンクされている場合、キャンペーンは[ コンテンツステージングダッシュボード ](../content-design/content-staging-dashboard.md)からのみ編集できます。

>[!NOTE]
>
>[!UICONTROL Schedule Design Update] タブは![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerceで削除されました。カテゴリで直接変更することはできません。 これらのアクティベーションのスケジュールされた更新を作成する必要があります。

## カテゴリの更新をスケジュール

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. 左側のカテゴリーツリーで、変更するカテゴリを選択します。

1. ページ上部の「_変更予定_」ボックスで、「**[!UICONTROL Schedule New Update]**」をクリックします。

   ![変更予定](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save as a New Update]** オプションを選択した状態で、更新の基本パラメーターを設定します。

   - **[!UICONTROL Update Name]**&#x200B;に、新しいコンテンツステージングキャンペーンの名前を入力します。

   - 更新プログラムの概要&#x200B;**[!UICONTROL Description]**&#x200B;とその使用方法を入力します。

   - カレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）ツールを使用して、キャンペーンの&#x200B;**[!UICONTROL Start Date]**&#x200B;と&#x200B;**[!UICONTROL End Date]**&#x200B;を選択します。

   >[!IMPORTANT]
   >
   >キャンペーン **[!UICONTROL Start Date]**&#x200B;と&#x200B;**[!UICONTROL End Date]**&#x200B;は、各web サイトのローカルタイムゾーンから変換される&#x200B;**_default_**&#x200B;管理者タイムゾーンを使用して定義する必要があります。 たとえば、米国のタイムゾーンにもとづいて施策を開始する複数のタイムゾーンのweb サイトがある場合、ローカルタイムゾーンごとに個別の更新をスケジュールする必要があります。 **[!UICONTROL Start Date]**&#x200B;と&#x200B;**[!UICONTROL End Date]**&#x200B;をそれぞれ設定し、ローカル web サイトのタイムゾーンからデフォルトの管理者タイムゾーンに変換します。

   ![変更予定](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. スケジュールされた更新に必要な変更を加えます。

1. 変更をプレビューするには、右上のボタンバーで「**[!UICONTROL Preview]**」をクリックします。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

## 既存の更新プログラムに割り当てる

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**&#x200B;に移動します。

1. 左側のカテゴリーツリーで、変更するカテゴリを選択します。

1. ページ上部の「_変更予定_」ボックスで、「**[!UICONTROL Schedule New Update]**」をクリックします。

1. **[!UICONTROL Assign to Existing Campaign]**&#x200B;を選択します。

1. リストで、必要なキャンペーンを見つけて「**[!UICONTROL Select]**」をクリックします。

1. スケジュールされた更新に必要な変更を加えます。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。
