---
title: イベントの作成と更新
description: カタログからカテゴリに関連付けられたイベントを作成する方法を説明します。
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# イベントの作成と更新

{{ee-feature}}

各イベントはカタログのカテゴリに関連付けられ、特定のカテゴリに関連付けることができるイベントは一度に 1 つだけです。 ストアで今後のイベントのリストを表示するには、以下を設定する必要があります。 [カタログイベントカルーセル](../content-design/widget-event-carousel.md) ウィジェット。

![イベントリスト](./assets/category-events.png){width="700" zoomable="yes"}

## イベントの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Catalog Event]**.

1. カテゴリ ツリーで、イベントに関連付けるカテゴリを選択します。

   各カテゴリは一度に 1 つのイベントしか持つことができないので、既にイベントを持つカテゴリは無効になります。

   ![新しいイベント – カテゴリツリー](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. の定義 **[!UICONTROL Catalog Event Information]**:

   ![カタログイベント情報](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - の場合 **[!UICONTROL Start Date]** イベントの場合は、カレンダー（![カレンダーアイコン](../assets/icon-calendar.png)）を選択して、日付を選択します。 の使用 **[!UICONTROL Hour]** および **[!UICONTROL Minute]** スライダを使用して、イベントが開始される時間を設定します。

   - の場合 **[!UICONTROL End Date]** イベントの場合は、カレンダー（![カレンダーアイコン](../assets/icon-calendar.png)）を選択して、日付を選択します。 の使用 **[!UICONTROL Hour]** および **[!UICONTROL Minute]** スライダーを使用して、イベントが終了する時間を設定します。

   - をアップロードするには **[!UICONTROL Image]** イベント ウィジェットで、をクリックします。 **[!UICONTROL Choose File]** ディレクトリから画像ファイルを選択します。

   - が含まれる **[!UICONTROL Sort Order]** フィールドに、このイベントが他のイベントと共にリストされた際に表示される順序を示す数字を入力します。

   - カウントダウンティッカーを表示する各ページタイプのチェックボックスを選択します。

1. 完了したら、 **[!UICONTROL Save]**.

## イベントの更新

イベントは、イベント ページまたはイベントに関連付けられているカテゴリから編集できます。 カテゴリにイベントが関連付けられている場合は、右上隅に「イベントを編集」ボタンが表示されます。

### 方法 1：イベントページからイベントを編集する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. リストでイベントを検索し、編集モードで開きます。

1. イベントに対して必要な変更を行います。

1. 完了したら、 **[!UICONTROL Save]**.

### 方法 2：カテゴリからのイベントの編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリ ツリーで、イベントに関連付けられているカテゴリを選択します。

1. 右上隅のをクリックします。 **[!UICONTROL Edit Even]t**.

1. イベントに対して必要な変更を行います。

1. 完了したら、 **[!UICONTROL Save]**.

## イベントの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. リストでイベントを検索し、編集モードで開きます。

1. 右上隅のをクリックします。 **[!UICONTROL Delete]**.

1. アクションを確定するには、をクリックします **[!UICONTROL OK]**.

## フィールドの説明

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category] | グローバル | イベントを作成すると、このフィールドはカテゴリツリーにリンクします。 イベントを編集すると、そのイベントに関連するカテゴリページにリンクします。 |
| [!UICONTROL Start Date] | グローバル | でのイベントの開始日時 `MMDDYYYY HH;MM` 形式。 カレンダーアイコンをクリックして、日付を選択します。 |
| [!DNL End Date] | グローバル | イベントの終了日時 `MMDDYYYY HH;MM` 形式。 カレンダーアイコンをクリックして、日付を選択します。 |
| [!UICONTROL Image] | ストア表示 | に表示される画像をアップロードします。 [カタログイベントカルーセルウィジェット](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | グローバル | 他のイベントと共にリストされるときにこのイベントが表示されるシーケンスを決定します。 |
| [!UICONTROL Display Countdown Ticker On] | グローバル | 指定した各ページのヘッダーにカウントダウンティッカーを表示します。 オプション： `Category Page` / `Product Page` |
| [!UICONTROL Status] | グローバル | 開始日と終了日の範囲に基づいて、イベントのステータスを示します。 ステータスは読み取り専用の値です。 値： `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 新しいイベントや既存のイベントの変更を保存せずにイベントページに戻ります。 |
| **[!UICONTROL Delete]** | イベントを削除します。 |
| **[!UICONTROL Reset]** | 保存されていない変更のフォームをクリアし、元のイベント情報に戻します。 |
| **[!UICONTROL Save and Continue Edit]** | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| **[!UICONTROL Save]** | 変更を保存し、フォームを閉じて、イベント ページに戻ります。 |

{style="table-layout:auto"}
