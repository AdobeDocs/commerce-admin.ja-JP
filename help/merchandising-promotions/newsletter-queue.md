---
title: ニュースレターキュー
description: 複数のニュースレターバッチを送信するためのニュースレターキューを管理する方法を説明します。
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# ニュースレターキュー

サーバーの負荷を管理するために、多数の購読者を持つニュースレターは複数のバッチのキューに送信されます。 ニュースレターキューを定期的に確認して、ステータスを確認したり、処理された数を確認したりできます。 転送中に発生する問題は、以下のデバイスに表示されます。 _ニュースレターの問題_ レポート。

## ニュースレターの送信

1. 日 _Admin_ メニュー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. グリッドで、を見つけます [ニュースレターテンプレート](newsletter-template.md) その通知を送信して、 **[!UICONTROL Action]** 列を `Queue Newsletter`.

1. の場合 **[!UICONTROL Queue Date Start]**&#x200B;で、送信を開始する日付をカレンダーから選択します（![カレンダーアイコン](../assets/icon-calendar.png)）に設定します。

1. の場合 **[!UICONTROL Subscribers From]**&#x200B;を選択し、メール送信に含める各ストア表示を選択します。

1. メールヘッダー情報を入力します。

   - のニュースレターの簡単な説明を入力します **[!UICONTROL Subject]** 電子メールヘッダーの行。

   - を入力 **[!UICONTROL Sender Name]**.

   - の場合 **[!UICONTROL Sender Email]**：送信者のメールアドレスを入力します。

     設定では、送信者のデフォルトの名前とメールアドレスが指定されます。

     ![ニュースレターキュー情報](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 該当する場合は、 **[!UICONTROL Message]** 登録解除する手順の上にあるボックス。

   >[!NOTE]
   >
   >多くの管轄区域で法律で義務付けられている指示を削除しないでください。

1. ニュースレターにカスタムスタイルを適用するには、カスタムスタイルを **[!UICONTROL Newsletter Styles]** フィールド。

1. 完了したら、 **[!UICONTROL Save and Resume]**.

   ニュースレターは、処理待ちのキューに表示されます。

## 問題の確認

日 _Admin_ メニュー、に移動 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずにニュースレターテンプレート ページに戻ります。 |
| **[!UICONTROL Reset]** | キュー情報フォームの未保存の変更をすべて以前の値にリセットします。 |
| **[!UICONTROL Preview Template]** | 別のタブでプレビューページを開きます。 |
| **[!UICONTROL Save and Resume]** | すべての変更を保存します。 ニュースレターをキューに入れます。 |
| **[!UICONTROL Save Newsletter]** | すべての変更を保存します。 ニュースレターをキューに入れます。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各ニュースレターテンプレートに割り当てられる一意の数値識別子。 |
| [!UICONTROL Queue Start] | ニュースレターが送信された日付です。 |
| [!UICONTROL Queue End] | ニュースレターの送信が終了した日付。 |
| [!UICONTROL Subject] | ニュースレターテンプレートの件名です。 |
| [!UICONTROL Status] | ニュースレターのメール送信のステータスを示します。 使用可能な値： `Sent`, `Canceled`, `Not Sent`, `Sending`、または `Paused`. |
| [!UICONTROL Processed] | 送信されたニュースレターの数を示します。 |
| [!UICONTROL Recipients] | 購読者が受信したニュースレターの数を示します。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**：テンプレートのプレビュー用の別のウィンドウが開きます。 |

{style="table-layout:auto"}
