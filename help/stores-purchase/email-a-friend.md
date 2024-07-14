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

![ 例ストアフロント – 友人にメールを送信 ](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## 友だちのメールを設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、「**[!UICONTROL Email to a Friend]**」を選択します。

1. **[!UICONTROL Email Templates]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、オプションを設定します。

   ![ カタログ設定 – メールテンプレート ](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、[ 設定リファレンスガイド ](../configuration-reference/catalog/email-to-a-friend.md) の _メールテンプレート_ を参照してください。

   任意のフィールドのデフォルト設定を変更するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、フィールドを編集可能にします。

   - **[!UICONTROL Enabled]** を `Yes` に設定します。

   - メッセージの基礎として使用するテンプレートに **[!UICONTROL Select Email Template]** を設定します。

   - 登録済みの顧客のみが友人にメールを送信できるようにする必要がある場合は、**[!UICONTROL Allow for Guests]** を `No` に設定します。

   - **[!UICONTROL Max Recipients]**: 1 つのメッセージの配布リストに登録できる友だちの最大数を入力します。

   - **[!UICONTROL Max Products Sent in 1 Hour]** しくは、1 人のユーザーが友人と 1 時間にわたって共有できる製品の最大数を入力します。

   - メールの送信者を識別するには、**[!UICONTROL Limit Sending By]** を次のいずれかの方法に設定します。

     `IP Address` - （推奨）メールの送信に使用されるコンピューターの IP アドレスで送信者を識別します。

     `Cookie (unsafe)` - ブラウザーの cookie によって送信者を識別します。 送信者が cookie を削除して制限を回避できるので、この方法は効果が低くなります。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## ストアフロントの友人にメールを送信

この機能を設定すると、ストア顧客は次の手順に従って商品情報を友達と共有します。

1. 顧客は、カタログページで「**[!UICONTROL Email]**」リンクをクリックします。

1. この機能が登録ユーザーに対してのみ設定されている場合は、次のいずれかを行います。

   - 顧客アカウントにログインします。
   - 新しいアカウントにサインアップします。

1. **[!UICONTROL Message]** を完了し、受信者 **[!UICONTROL Name]** と **[!UICONTROL Email Address]** を入力します。

   必要に応じて、受信者を追加できます。

   - **[!UICONTROL Add Invitee]** をクリックします。

   - 追加したユーザーの **[!UICONTROL Name]** と **[!UICONTROL Email Address]** を入力します。

     設定で許可されている数だけ、追加のユーザーにメッセージを送信できます。 **[!DNL Remove]** のリンクをクリックして、追加された招待者を削除できます。

1. メッセージを送信する準備ができたら、**[!UICONTROL Send Email]** をクリックします。

   ![ ストアフロントの例 – 友人にメール ](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
