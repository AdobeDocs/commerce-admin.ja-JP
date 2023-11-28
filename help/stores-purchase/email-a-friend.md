---
title: 友達にメールを送信
description: 顧客が友達と商品へのリンクを簡単に共有できる電子メールリンクを提供する方法を説明します。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 友達にメールを送信

「電子メール」リンクを使用すると、顧客が製品へのリンクを友達と簡単に共有できます。 デモ Luma ストアでは、電子メールリンクがエンベロープアイコンとして表示されます。 メッセージテンプレートは、ボイスおよびブランドに合わせてカスタマイズできます。 スパムを防ぐには、各 E メールの受信者数と 1 時間に共有できる製品の数を制限します。

![ストアフロントの例 — 友達に E メールを送信する](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 友達へのメールの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Email to a Friend]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Email Templates]** 」セクションに移動して、次のオプションを設定します。

   ![カタログ設定 — 電子メールテンプレート](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [メールテンプレート](../configuration-reference/catalog/email-to-a-friend.md) （内） _設定リファレンスガイド_.

   任意のフィールドのデフォルト設定を変更するには、 **[!UICONTROL Use system value]** チェックボックスをオンにして、フィールドを編集可能にします。

   - 設定 **[!UICONTROL Enabled]** から `Yes`.

   - 設定 **[!UICONTROL Select Email Template]** を、メッセージの基礎として使用するテンプレートに追加します。

   - 友達にメールを送信できるのは、登録した顧客だけです。必要に応じて、 **[!UICONTROL Allow for Guests]** から `No`.

   - の場合 **[!UICONTROL Max Recipients]**」には、1 つのメッセージの配信リストに登録できる友達の最大数を入力します。

   - の場合 **[!UICONTROL Max Products Sent in 1 Hour]**」には、1 時間の間に 1 人のユーザーが友達と共有できる製品の最大数を入力します。

   - 設定 **[!UICONTROL Limit Sending By]** を次のいずれかの方法で追加して、e メールの送信者を識別します。

     `IP Address`  - （推奨）送信者を E メールの送信に使用されるコンピューターの IP アドレスで識別します。

     `Cookie (unsafe)`  — 送信者をブラウザーの Cookie で識別します。 送信者は制限を回避するために Cookie を削除できるので、この方法はあまり有効ではありません。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ストアフロントで友達にメールを送信

この機能を設定すると、ストアの顧客は次の手順に従って製品情報を友達と共有できます。

1. カタログページで、顧客が **[!UICONTROL Email]** リンク。

1. この機能が登録ユーザーに対してのみ設定されている場合、は次のいずれかを実行します。

   - 顧客アカウントにログインします。
   - 新しいアカウントにサインアップします。

1. 次を完了します。 **[!UICONTROL Message]** 受信者を入力 **[!UICONTROL Name]** および **[!UICONTROL Email Address]**.

   必要に応じて、顧客はさらに受信者を追加できます。

   - クリック数 **[!UICONTROL Add Invitee]**.

   - 次に入る **[!UICONTROL Name]** および **[!UICONTROL Email Address]** 追加された人物の

     ユーザーは、設定できるだけ多くの追加のユーザーにメッセージを送信できます。 追加された招待者を削除するには、 **[!DNL Remove]** リンク。

1. メッセージを送信する準備が整ったら、クリックします **[!UICONTROL Send Email]**.

   ![ストアフロントの例 — 友人への E メール](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
