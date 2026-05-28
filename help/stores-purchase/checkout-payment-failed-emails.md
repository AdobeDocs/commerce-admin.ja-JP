---
title: 支払い失敗の通知
description: トランザクションを完了できない支払い方法のメール通信を設定する方法を説明します。
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 支払い失敗の通知

チェックアウト時に選択した支払い方法でトランザクションが完了しなかった場合、ストアの連絡先または指定された管理者ユーザーに通知が送信されます。

## 手順1：電子メールテンプレートの更新

ブランドを反映させるために、必要なメールテンプレートを更新していることを確認してください。 テンプレートの完全なリストについては、[電子メールテンプレートリスト &#x200B;](../systems/email-templates.md#email-template-list)を参照してください。

## 手順2：支払いに失敗した電子メールの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Checkout]**&#x200B;を選択します。

1. **[!UICONTROL Payment Failed Emails]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![支払いに失敗した電子メール &#x200B;](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 支払いに失敗した電子メールのオプションを設定します。

   - メッセージの送信者として表示されるストア連絡先に&#x200B;**[!UICONTROL Payment Failed Email Sender]**&#x200B;を設定します。
   - 失敗したメール送信の通知を受信するストア連絡先に&#x200B;**[!UICONTROL Payment Failed Email Receiver]**&#x200B;を設定します。
   - チェックアウト時に支払い方法が失敗したときに送信される電子メールに使用されるテンプレートに&#x200B;**[!UICONTROL Payment Failed Template]**&#x200B;を設定します。

1. **[!UICONTROL Send Payment Failed Email Copy To]**&#x200B;に、支払い失敗の通知のコピーを受け取るユーザーの電子メールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. **[!UICONTROL Payment Failed Copy Method]**&#x200B;を次のいずれかに設定します：

   - `Bcc` – お客様に送信するのと同じメールのヘッダーに受信者を含めることで、_ブラインドの表敬文_&#x200B;を送信します。 BCC受信者は、お客様には表示されません。
   - `Separate Email` - コピーを別の電子メールとして送信します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。
