---
title: ニュースレター
description: 複数のニュースレターバッチを送信するためのニュースレターキューを管理する方法について説明します。
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
TQID: https://experienceleague.adobe.com/5KMZgOARaHuGktmtPujgirhp0QY-7FI9HtSS5V7YeVM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 0%

---

# ニュースレター

サーバーの負荷を管理するために、多数の購読者を持つニュースレターが複数のバッチのキューで送信されます。 ニュースレターキューを定期的に確認して、ステータスを確認し、処理済みの数を確認できます。 送信中に発生した問題は、_ニュースレターの問題_ レポートに表示されます。

## ニュースレターを送る

1. _管理者_ メニューで、**[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**に移動します。

1. グリッドで、送信する[ ニュースレターテンプレート ](newsletter-template.md)を見つけ、**[!UICONTROL Action]**&#x200B;列を`Queue Newsletter`に設定します。

1. **[!UICONTROL Queue Date Start]**&#x200B;で、送信を開始する日付をカレンダー（![ カレンダーアイコン ](../assets/icon-calendar.png)）から選択します。

1. **[!UICONTROL Subscribers From]**&#x200B;で、メールの一斉配信に含める各ストアビューを選択します。

1. メールヘッダー情報を入力します。

   - メールヘッダーの&#x200B;**[!UICONTROL Subject]**&#x200B;行のニュースレターの簡単な説明を入力します。

   - **[!UICONTROL Sender Name]**&#x200B;を入力します。

   - **[!UICONTROL Sender Email]**&#x200B;に、送信者の電子メールアドレスを入力します。

     送信者のデフォルトの名前とメールアドレスは、設定で指定します。

     ![ ニュースレターキュー情報](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 該当する場合は、購読解除の手順の上にある&#x200B;**[!UICONTROL Message]** ボックスにメモを入力します。

   >[!NOTE]
   >
   >多くの管轄区域で法律で要求されている指示を削除しないでください。

1. ニュースレターにカスタムスタイルを適用するには、**[!UICONTROL Newsletter Styles]** フィールドにカスタムスタイルを追加します。

1. 完了したら、**[!UICONTROL Save and Resume]**&#x200B;をクリックします。

   ニュースレターは、処理待ちのキューに表示されます。

## 問題の確認

_管理者_ メニューで、**[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**に移動します。

## ボタンバー

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずにニュースレターテンプレートページに戻ります。 |
| **[!UICONTROL Reset]** | キュー情報フォームの未保存の変更を以前の値にリセットします。 |
| **[!UICONTROL Preview Template]** | 別のタブでプレビューページを開きます。 |
| **[!UICONTROL Save and Resume]** | すべての変更を保存します。 ニュースレターをキューに追加します。 |
| **[!UICONTROL Save Newsletter]** | すべての変更を保存します。 ニュースレターをキューに追加します。 |

{style="table-layout:auto"}

## 列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各ニュースレターテンプレートに割り当てられる一意の数値識別子。 |
| [!UICONTROL Queue Start] | ニュースレターが送信された日付。 |
| [!UICONTROL Queue End] | ニュースレターの送信が終了した日付。 |
| [!UICONTROL Subject] | ニュースレターテンプレートの件名。 |
| [!UICONTROL Status] | ニュースレターの郵送状況を示します。 使用可能な値：`Sent`、`Canceled`、`Not Sent`、`Sending`または`Paused`。 |
| [!UICONTROL Processed] | ニュースレターの送信数を示します。 |
| [!UICONTROL Recipients] | 購読者が受信したニュースレターの数を示します。 |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: テンプレートをプレビューするために別のウィンドウを開きます。 |

{style="table-layout:auto"}
