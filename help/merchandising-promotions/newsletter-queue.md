---
title: ニュースレターのキュー
description: 複数のニュースレターバッチを送信するためのニュースレターキューを管理する方法を説明します。
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# ニュースレターのキュー

サーバーでの負荷を管理するために、多数の購読者を持つニュースレターが、複数のバッチのキューで送信されます。 ニュースレターキューを定期的に調べて、ステータスを確認し、処理されたニュースレターの数を確認できます。 送信中に発生した問題は、 _ニュースレターの問題_ レポート。

## ニュースレターを送信

1. 次の日： _管理者_ メニュー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. グリッドで、 [ニュースレターテンプレート](newsletter-template.md) 送信され、 **[!UICONTROL Action]** 列を `Queue Newsletter`.

1. の場合 **[!UICONTROL Queue Date Start]**、送信を開始する日付をカレンダーから選択します (![カレンダーアイコン](../assets/icon-calendar.png)) をクリックします。

1. の場合 **[!UICONTROL Subscribers From]**」で、e メールの一斉送信に含める各ストアビューを選択します。

1. E メールヘッダー情報を入力します。

   - ニュースレターの簡単な説明を入力 **[!UICONTROL Subject]** e メールヘッダーの行。

   - 次を入力します。 **[!UICONTROL Sender Name]**.

   - の場合 **[!UICONTROL Sender Email]**、送信者の E メールアドレスを入力します。

     送信者のデフォルトの名前と E メールアドレスは、設定で指定します。

     ![ニュースレターキュー情報](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 該当する場合は、 **[!UICONTROL Message]** 」ボックスをオンにします。

   >[!NOTE]
   >
   >多くの管轄地域で法律で規定されている指示を削除しないでください。

1. ニュースレターにカスタムスタイルを適用するには、それらを **[!UICONTROL Newsletter Styles]** フィールドに入力します。

1. 完了したら、「 **[!UICONTROL Save and Resume]**.

   ニュースレターは、処理待ちのキューに表示されます。

## 問題を確認

次の日： _管理者_ メニュー、移動 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに、ニュースレターテンプレートページに戻ります。 |
| **[!UICONTROL Reset]** | キュー情報フォーム内の未保存の変更を、以前の値にリセットします。 |
| **[!UICONTROL Preview Template]** | プレビューページを別のタブで開きます。 |
| **[!UICONTROL Save and Resume]** | 変更をすべて保存します。 ニュースレターをキューに入れます。 |
| **[!UICONTROL Save Newsletter]** | 変更をすべて保存します。 ニュースレターをキューに入れます。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各ニュースレターテンプレートに割り当てられる一意の数値識別子。 |
| [!UICONTROL Queue Start] | ニュースレターが送信された日付。 |
| [!UICONTROL Queue End] | ニュースレターの送信が終了した日付。 |
| [!UICONTROL Subject] | ニュースレターテンプレートの件名です。 |
| [!UICONTROL Status] | ニュースレターの郵送先の状態を示します。 可能な値： `Sent`, `Canceled`, `Not Sent`, `Sending`または `Paused`. |
| [!UICONTROL Processed] | 送信されたニュースレターの数を示します。 |
| [!UICONTROL Recipients] | 購読者が受信したニュースレターの数を示します。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**：別のウィンドウを開き、テンプレートをプレビューします。 |

{style="table-layout:auto"}
