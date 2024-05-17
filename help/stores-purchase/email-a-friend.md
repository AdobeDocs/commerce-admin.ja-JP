---
title: 友達にメールを送信
description: 顧客が製品へのリンクを友人と簡単に共有できるようにするメールリンクを提供する方法を説明します。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 友達にメールを送信

メールリンクを使用すると、顧客は製品へのリンクを友人と簡単に共有できます。 デモ Luma ストアでは、メールリンクが封筒アイコンとして表示されます。 メッセージテンプレートは、音声とブランドに合わせてカスタマイズできます。 スパムを防ぐために、各メールの受信者数や、1 時間にわたって共有できる製品数を制限できます。

![ストアフロントの例 – 友人にメールを送信](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 友だちのメールを設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Email to a Friend]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Email Templates]** 「」セクションを選択して、次のオプションを設定します。

   ![カタログ設定 – メールテンプレート](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [メールテンプレート](../configuration-reference/catalog/email-to-a-friend.md) が含まれる _設定リファレンスガイド_.

   任意のフィールドのデフォルト設定を変更するには、 **[!UICONTROL Use system value]** フィールドを編集可能にするチェックボックス。

   - を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

   - を設定 **[!UICONTROL Select Email Template]** をメッセージの基礎として使用するテンプレートに追加します。

   - 登録済みの顧客のみが友人にメールを送信することを要求する場合は、次のように設定します **[!UICONTROL Allow for Guests]** 対象： `No`.

   - の場合 **[!UICONTROL Max Recipients]**&#x200B;に設定する場合は、1 通のメッセージに対して配布リストに登録できる友達の最大数を入力します。

   - の場合 **[!UICONTROL Max Products Sent in 1 Hour]**&#x200B;に設定します。1 人のユーザーが友人と 1 時間にわたって共有できる製品の最大数を入力します。

   - を設定 **[!UICONTROL Limit Sending By]** メールの送信者を識別する次の方法のいずれか

     `IP Address`  - （推奨）メールの送信に使用されるコンピューターの IP アドレスで送信者を識別します。

     `Cookie (unsafe)`  – 送信者をブラウザーの cookie で識別します。 送信者が cookie を削除して制限を回避できるので、この方法は効果が低くなります。

1. 完了したら、 **[!UICONTROL Save Config]**.

## ストアフロントの友人にメールを送信

この機能を設定すると、ストア顧客は次の手順に従って商品情報を友達と共有します。

1. 顧客は、カタログページで **[!UICONTROL Email]** リンク。

1. この機能が登録ユーザーに対してのみ設定されている場合は、次のいずれかを行います。

   - 顧客アカウントにログインします。
   - 新しいアカウントにサインアップします。

1. 完了： **[!UICONTROL Message]** およびが受信者に入力されます **[!UICONTROL Name]** および **[!UICONTROL Email Address]**.

   必要に応じて、受信者を追加できます。

   - クリック数 **[!UICONTROL Add Invitee]**.

   - エントリ数： **[!UICONTROL Name]** および **[!UICONTROL Email Address]** 追加されたユーザー。

     設定で許可されている数だけ、追加のユーザーにメッセージを送信できます。 追加された招待を削除するには、 **[!DNL Remove]** リンク。

1. メッセージを送信する準備ができたら、をクリックします **[!UICONTROL Send Email]**.

   ![ストアフロントの例 – 友人にメールで送信](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
