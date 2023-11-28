---
title: 支払い失敗の通知
description: トランザクションの完了に失敗した支払い方法に対して電子メール通信を設定する方法を説明します。
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 支払い失敗の通知

チェックアウト時に選択した支払い方法でトランザクションが完了しなかった場合、ストア連絡先または指定された管理者ユーザーに通知が送信されます。

## 手順 1：電子メールテンプレートの更新

ブランドを反映するように、必要な E メールテンプレートを必ず更新してください。 テンプレートの完全なリストについては、 [メールテンプレートリスト](../systems/email-templates.md#email-template-list).

## 手順 2：支払いに失敗した電子メールを設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Payment Failed Emails]** 」セクションに入力します。

   ![支払いに失敗したメール](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 支払いに失敗した電子メールのオプションを設定します。

   - 設定 **[!UICONTROL Payment Failed Email Sender]** メッセージの送信者として表示されるストア連絡先に追加します。
   - 設定 **[!UICONTROL Payment Failed Email Receiver]** 電子メールの送信失敗の通知を受け取るストア連絡先に送信します。
   - 設定 **[!UICONTROL Payment Failed Template]** を、チェックアウト時に支払い方法が失敗した場合に送信される e メールに使用されるテンプレートに設定します。

1. の場合 **[!UICONTROL Send Payment Failed Email Copy To]**「 」に、支払い失敗通知のコピーを受け取るすべてのユーザーの電子メールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. 設定 **[!UICONTROL Payment Failed Copy Method]** を次のいずれかに変更します。

   - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
   - `Separate Email`  — コピーを別の E メールとして送信します。

1. クリック **[!UICONTROL Save Config]**.
