---
title: イベントの作成と更新
description: カタログからカテゴリに関連付けられたイベントを作成する方法を説明します。
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# イベントの作成と更新

{{ee-feature}}

各イベントは、カタログのカテゴリに関連付けられ、一度に 1 つのイベントのみ特定のカテゴリに関連付けることができます。 ストアで今後のイベントのリストを表示するには、 [カタログイベントカルーセル](../content-design/widget-event-carousel.md) ウィジェット。

![イベントリスト](./assets/category-events.png){width="700" zoomable="yes"}

## イベントの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. 右上隅で、 **[!UICONTROL Add Catalog Event]**.

1. カテゴリツリーで、イベントに関連付けるカテゴリを選択します。

   各カテゴリには一度に 1 つのイベントしか設定できないので、既にイベントが設定されているカテゴリは無効になります。

   ![新しいイベント — カテゴリツリー](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. 次を定義： **[!UICONTROL Catalog Event Information]**:

   ![カタログイベント情報](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - の **[!UICONTROL Start Date]** イベントのカレンダー (![カレンダーアイコン](../assets/icon-calendar.png)) をクリックして日付を選択します。 以下を使用します。 **[!UICONTROL Hour]** および **[!UICONTROL Minute]** スライダーを使用して、イベントが開始される時間を設定します。

   - の **[!UICONTROL End Date]** イベントのカレンダー (![カレンダーアイコン](../assets/icon-calendar.png)) をクリックして日付を選択します。 以下を使用します。 **[!UICONTROL Hour]** および **[!UICONTROL Minute]** スライダを使用して、イベントの終了時間を設定します。

   - 次をアップロードするには： **[!UICONTROL Image]** イベントウィジェットの場合は、 **[!UICONTROL Choose File]** をクリックし、ディレクトリから画像ファイルを選択します。

   - Adobe Analytics の **[!UICONTROL Sort Order]** 「 」フィールドに、他のイベントと共にこのイベントが表示される順序を示す数値を入力します。

   - カウントダウンティッカーを表示する各ページタイプのチェックボックスをオンにします。

1. 完了したら、「 **[!UICONTROL Save]**.

## イベントを更新

イベントは、イベントページまたはイベントに関連付けられたカテゴリから編集できます。 カテゴリにイベントが関連付けられている場合は、右上隅に「イベントを編集」ボタンが表示されます。

### メソッド 1：イベントページでイベントを編集する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. リストでイベントを探し、編集モードで開きます。

1. イベントに必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save]**.

### メソッド 2：カテゴリからイベントを編集する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 左側のカテゴリツリーで、イベントに関連付けられているカテゴリを選択します。

1. 右上隅で、 **[!UICONTROL Edit Even]t**.

1. イベントに必要な変更を加えます。

1. 完了したら、「 **[!UICONTROL Save]**.

## イベントの削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. リストでイベントを探し、編集モードで開きます。

1. 右上隅で、 **[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## フィールドの説明

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category] | グローバル | イベントを作成すると、このフィールドはカテゴリツリーにリンクします。 イベントを編集すると、イベントに関連するカテゴリページにリンクします。 |
| [!UICONTROL Start Date] | グローバル | イベントの開始日時 ( `MMDDYYYY HH;MM` 形式を使用します。 カレンダーアイコンをクリックして日付を選択します。 |
| [!DNL End Date] | グローバル | イベントの終了日時 ( `MMDDYYYY HH;MM` 形式を使用します。 カレンダーアイコンをクリックして日付を選択します。 |
| [!UICONTROL Image] | ストア表示 | に表示される画像をアップロードします。 [カタログイベントカルーセルウィジェット](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | グローバル | 他のイベントと共にこのイベントが表示される順序を決定します。 |
| [!UICONTROL Display Countdown Ticker On] | グローバル | 指定した各ページのヘッダーにカウントダウンティッカーを表示します。 オプション： `Category Page` / `Product Page` |
| [!UICONTROL Status] | グローバル | 「開始日」と「終了日」の範囲に基づくイベントのステータスを示します。 Status は読み取り専用の値です。 値： `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 新しいイベントや既存のイベントの変更を保存せずに、イベントページに戻ります。 |
| **[!UICONTROL Delete]** | イベントを削除します。 |
| **[!UICONTROL Reset]** | 未保存の変更のフォームをクリアし、元のイベント情報を復元します。 |
| **[!UICONTROL Save and Continue Edit]** | すべての変更を保存し、フォームを編集モードで開いたままにします。 |
| **[!UICONTROL Save]** | 変更を保存し、フォームを閉じて、イベントページに戻ります。 |

{style="table-layout:auto"}
