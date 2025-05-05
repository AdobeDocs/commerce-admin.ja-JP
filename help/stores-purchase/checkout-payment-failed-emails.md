---
title: 支払い失敗通知
description: トランザクションを完了できない支払い方法に対してメール通信を設定する方法を説明します。
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 支払い失敗通知

チェックアウト時に選択した支払い方法でトランザクションを完了できない場合は、店舗担当者または指定した管理者ユーザーに通知が送信されます。

## 手順 1：メールテンプレートの更新

ブランドを反映させるために、必要なメールテンプレートを更新したことを確認します。 テンプレートの完全なリストについては、[ メールテンプレートリスト ](../systems/email-templates.md#email-template-list) を参照してください。

## 手順 2：支払いに失敗したメールの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Checkout]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Payment Failed Emails]**」セクションを展開します。

   ![ 支払いに失敗したメール ](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 支払失敗 E メールのオプションを設定します：

   - メッセージの送信者として表示されるストアの連絡先に **[!UICONTROL Payment Failed Email Sender]** を設定します。
   - **[!UICONTROL Payment Failed Email Receiver]** を、メール送信の失敗の通知を受信するストア連絡先に設定します。
   - チェックアウト中に支払い方法が失敗した場合に送信される E メールに使用されるテンプレートに **[!UICONTROL Payment Failed Template]** を設定します。

1. **[!UICONTROL Send Payment Failed Email Copy To]**：支払失敗通知のコピーを受け取るユーザーの電子メール アドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. **[!UICONTROL Payment Failed Copy Method]** を次のいずれかに設定します。

   - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
   - `Separate Email` - コピーを個別のメールとして送信します。

1. 「**[!UICONTROL Save Config]**」をクリックします。
