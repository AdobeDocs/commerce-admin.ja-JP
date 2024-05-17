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

ブランドを反映させるために、必要なメールテンプレートを更新したことを確認します。 テンプレートの完全なリストについては、を参照してください [E メール テンプレート リスト](../systems/email-templates.md#email-template-list).

## 手順 2：支払いに失敗したメールの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Checkout]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Payment Failed Emails]** セクション。

   ![支払いに失敗したメール](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 支払失敗 E メールのオプションを設定します：

   - を設定 **[!UICONTROL Payment Failed Email Sender]** メッセージの送信者として表示されるストアの連絡先に送信されます。
   - を設定 **[!UICONTROL Payment Failed Email Receiver]** に送信されます。ストアの連絡先は、メール送信の失敗の通知を受け取ることになります。
   - を設定 **[!UICONTROL Payment Failed Template]** チェックアウト中に支払い方法が失敗した場合に送信されるメールに使用されるテンプレート。

1. の場合 **[!UICONTROL Send Payment Failed Email Copy To]**：支払い失敗通知のコピーを受け取るユーザーのメールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. を設定 **[!UICONTROL Payment Failed Copy Method]** を次のいずれかに変更します。

   - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
   - `Separate Email` - コピーを別のメールとして送信します。

1. クリック **[!UICONTROL Save Config]**.
