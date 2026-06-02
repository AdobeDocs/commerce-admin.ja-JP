---
title: 友達にメール
description: お客様が商品へのリンクを簡単に友人と共有できるようにするメールリンクを提供する方法について説明します。
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 友達にメール

メールリンクを使用すると、顧客は商品へのリンクを友人と簡単に共有できます。 デモ Luma ストアでは、メールのリンクがエンベロープのアイコンとして表示されます。 メッセージテンプレートは、声やブランドに合わせてカスタマイズできます。 迷惑メールを防ぐには、1通のメールの受信者数と、1時間の間に共有できる商品の数を制限することができます。

![&#x200B; ストアフロントの例 – 友達にメールを送信](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## email-a-friendの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Catalog]**&#x200B;を展開し、**[!UICONTROL Email to a Friend]**&#x200B;を選択します。

1. **[!UICONTROL Email Templates]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、オプションを設定します。

   ![&#x200B; カタログ設定 – メールテンプレート &#x200B;](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   これらの各設定設定の詳細については、_設定リファレンスガイド_&#x200B;の[電子メールテンプレート &#x200B;](../configuration-reference/catalog/email-to-a-friend.md)を参照してください。

   任意のフィールドのデフォルト設定を変更するには、**[!UICONTROL Use system value]** チェックボックスをオフにして、フィールドを編集可能にします。

   - **[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

   - メッセージのベースとして使用するテンプレートに&#x200B;**[!UICONTROL Select Email Template]**&#x200B;を設定します。

   - 登録された顧客のみが友達にメールを送信できるようにする必要がある場合は、**[!UICONTROL Allow for Guests]**&#x200B;を`No`に設定します。

   - **[!UICONTROL Max Recipients]**&#x200B;の場合、1つのメッセージの配布リストに登録できる友達の最大数を入力します。

   - **[!UICONTROL Max Products Sent in 1 Hour]**&#x200B;について、1時間の間に1人のユーザーが友人と共有できる製品の最大数を入力します。

   - **[!UICONTROL Limit Sending By]**&#x200B;を次のいずれかの方法に設定して、メールの送信者を特定します。

     `IP Address` - （推奨）電子メールの送信に使用されるコンピューターのIP アドレスで送信者を識別します。

     `Cookie (unsafe)` - ブラウザーのCookieで送信者を識別します。 送信者はCookieを削除して制限を回避できるため、この方法の効果は低くなります。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## ストアフロントの友人にメールを送る

この機能が設定されている場合、ストアユーザーは次の手順に従って製品情報を友人と共有します。

1. カタログページで、顧客は&#x200B;**[!UICONTROL Email]** リンクをクリックします。

1. この機能が登録ユーザー専用に設定されている場合は、次のいずれかの操作を行います。

   - 顧客アカウントにログインします。
   - 新しいアカウントにサインアップします。

1. **[!UICONTROL Message]**&#x200B;を完了し、受信者&#x200B;**[!UICONTROL Name]**&#x200B;および&#x200B;**[!UICONTROL Email Address]**&#x200B;に入力します。

   必要に応じて、お客様は次の受信者を追加できます。

   - **[!UICONTROL Add Invitee]**&#x200B;をクリックします。

   - 追加ユーザーの&#x200B;**[!UICONTROL Name]**&#x200B;と&#x200B;**[!UICONTROL Email Address]**&#x200B;を入力します。

     設定で許可されている数の追加ユーザーにメッセージを送信できます。 **[!DNL Remove]** リンクをクリックすると、追加された招待者を削除できます。

1. メッセージを送信する準備ができたら、**[!UICONTROL Send Email]**&#x200B;をクリックします。

   ![&#x200B; ストアフロントの例 – 友達へのメール &#x200B;](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
