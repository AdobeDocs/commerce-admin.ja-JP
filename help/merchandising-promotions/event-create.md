---
title: イベントの作成と更新
description: カタログからカテゴリに関連付けられたイベントを作成する方法を説明します。
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# イベントの作成と更新

{{ee-feature}}

各イベントはカタログのカテゴリに関連付けられ、特定のカテゴリに関連付けることができるイベントは一度に 1 つだけです。 ストアに今後のイベントのリストを表示するには、[&#x200B; カタログイベントカルーセル &#x200B;](../content-design/widget-event-carousel.md) ウィジェットも設定する必要があります。

![&#x200B; イベントリスト &#x200B;](./assets/category-events.png){width="700" zoomable="yes"}

## イベントの作成

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Events]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add Catalog Event]**」をクリックします。

1. カテゴリ ツリーで、イベントに関連付けるカテゴリを選択します。

   各カテゴリは一度に 1 つのイベントしか持つことができないので、既にイベントを持つカテゴリは無効になります。

   ![&#x200B; 新規イベント – カテゴリツリー &#x200B;](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. **[!UICONTROL Catalog Event Information]** を定義します。

   ![&#x200B; カタログイベント情報 &#x200B;](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - イベントの **[!UICONTROL Start Date]** には、カレンダー（![&#x200B; カレンダーアイコン &#x200B;](../assets/icon-calendar.png)）を使用して日付を選択します。 **[!UICONTROL Hour]** と **[!UICONTROL Minute]** のスライダーを使用して、イベントの開始時刻を設定します。

   - イベントの **[!UICONTROL End Date]** には、カレンダー（![&#x200B; カレンダーアイコン &#x200B;](../assets/icon-calendar.png)）を使用して日付を選択します。 **[!UICONTROL Hour]** と **[!UICONTROL Minute]** のスライダーを使用して、イベントの終了時間を設定します。

   - イベントウィジェットの **[!UICONTROL Image]** をアップロードするには、「**[!UICONTROL Choose File]**」をクリックし、ディレクトリから画像ファイルを選択します。

   - 「**[!UICONTROL Sort Order]**」フィールドに、このイベントが他のイベントと共にリストされるときの表示順序を示す数値を入力します。

   - カウントダウンティッカーを表示する各ページタイプのチェックボックスを選択します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## イベントの更新

イベントは、イベント ページまたはイベントに関連付けられているカテゴリから編集できます。 カテゴリにイベントが関連付けられている場合は、右上隅に「イベントを編集」ボタンが表示されます。

### 方法 1：イベントページからイベントを編集する

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Events]**&#x200B;に移動します。

1. リストでイベントを検索し、編集モードで開きます。

1. イベントに対して必要な変更を行います。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

### 方法 2：カテゴリからのイベントの編集

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. 左側のカテゴリ ツリーで、イベントに関連付けられているカテゴリを選択します。

1. 右上隅の「**[!UICONTROL Edit Even]t**」をクリックします。

1. イベントに対して必要な変更を行います。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## イベントの削除

1. _管理者_ サイドバーで、**[!UICONTROL Marketing]**/_[!UICONTROL Private Sales]_/**[!UICONTROL Events]**&#x200B;に移動します。

1. リストでイベントを検索し、編集モードで開きます。

1. 右上隅の「**[!UICONTROL Delete]**」をクリックします。

1. アクションを確定するには、「**[!UICONTROL OK]**」をクリックします。

## フィールドの説明

| フィールド | [&#x200B; 範囲 &#x200B;](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Category] | グローバル | イベントを作成すると、このフィールドはカテゴリツリーにリンクします。 イベントを編集すると、そのイベントに関連するカテゴリページにリンクします。 |
| [!UICONTROL Start Date] | グローバル | `MMDDYYYY HH;MM` 形式のイベントの開始日時。 カレンダーアイコンをクリックして、日付を選択します。 |
| [!DNL End Date] | グローバル | `MMDDYYYY HH;MM` 形式のイベントの終了日時。 カレンダーアイコンをクリックして、日付を選択します。 |
| [!UICONTROL Image] | ストア表示 | [&#x200B; カタログイベントカルーセルウィジェット &#x200B;](../content-design/widget-event-carousel.md) に表示される画像をアップロードします。 |
| [!UICONTROL Sort Order] | グローバル | 他のイベントと共にリストされるときにこのイベントが表示されるシーケンスを決定します。 |
| [!UICONTROL Display Countdown Ticker On] | グローバル | 指定した各ページのヘッダーにカウントダウンティッカーを表示します。 オプション：`Category Page` / `Product Page` |
| [!UICONTROL Status] | グローバル | 開始日と終了日の範囲に基づいて、イベントのステータスを示します。 ステータスは読み取り専用の値です。 値：`Open`/`Closed`/`Upcoming` |

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
