---
title: 共有： [!DNL Commerce] アカウント
description: 制限付きアクセスを許可する方法を学ぶ [!DNL Commerce] その他の [!DNL Commerce] アカウント所有者。
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 11b2f3f9558bf5a36199015247fb96d559bb5fdc
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# 共有： [!DNL Commerce] アカウント

お使いの [!DNL Commerce] アカウントには、サイトの管理に役立つ信頼できる従業員やサービスプロバイダーが利用できる情報が含まれています。 主要アカウント所有者は、他のアカウントに限定的なアクセスを許可する権限を持ちます [!DNL Commerce] アカウント所有者。 共有アクセスは取り消すことができますが、別のユーザーに転送することはできません。

The [!DNL Commerce] サポートチームはアカウントへのアクセス権を持っていないので、共有アクセスを設定できません。 適切な権限を持つプライマリアカウント所有者のみが共有アクセスを設定できます。 アカウントを共有すると、請求履歴やクレジットカード情報などのすべての機密情報は保護されたままとなり、他のユーザーとはいつでも共有されません。

>[!NOTE]
>
>共有アクセス権を持つユーザーが実行するすべてのアクションは、プライマリアカウント所有者のみが責任を負います。 Adobeは、お客様のアカウントへのアクセスを共有したユーザーによるアクションに対して責任を負いません。

![共有アクセス設定](./assets/shared-access.png){width="600" zoomable="yes"}

## 共有アカウントの設定

1. 開始する前に、次の情報を [!DNL Commerce] のアカウント **新しい共有アクセス権付与者**:

   - ユーザーは、既にaccount.adobe.comのアカウントに登録し、account.magento.comからログインしている必要があります。
   - The `Account ID` の左上隅に表示される _[!UICONTROL Magento]_タブ、ちょうど上&#x200B;**ログアウト**リンク。
   - The `Email` アカウントに関連付けられているアドレス。

1. にログインします。 [[!DNL Commerce] アカウント](commerce-account-create.md).

1. 左側のナビゲーションパネルで、 **[!UICONTROL Shared Access]**.

1. クリック **[!UICONTROL Add New User]**.

   ![新しいユーザーを追加](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. の下 [!UICONTROL _New User Information]_、以下の操作を実行します。

   - 次を入力します。 **[!UICONTROL Account ID]** 新しいユーザーの [!DNL Commerce] アカウント。
   - 次を入力します。 **[!UICONTROL Email]** 新しいユーザーの [!DNL Commerce] アカウント。

   ![新しいユーザー情報](./assets/shared-new-user.png){width="600"}

1. の下 _[!UICONTROL Shared Information]_、次の操作を実行します。

   - 共有アカウントを識別するには、 **[!UICONTROL Share Name]**. この名前は内部参照用で、自分とアカウントを共有しているユーザーのみに表示されます。
   - 新しいユーザーと個人の連絡先情報を共有する場合は、 **[!UICONTROL Your Email]** および **[!UICONTROL Your Phone]**.

1. の下 _[!UICONTROL Grant Account Permissions]_、各 [!DNL Commerce] 共有する製品およびサービス。

   ![アカウント権限の付与](./assets/shared-permissions.png){width="600"}

1. 完了したら、「 **[!UICONTROL Create Shared Access]**.

   新しいユーザー情報が _[!UICONTROL Manage Permissions]_」セクションに追加され、共有アカウントへのアクセス方法が記載された招待メールが新しいユーザーに送信されます。

   ![共有アクセスの権限を管理](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

## 共有アカウントへのアクセス

共有アカウントへの招待を受け取る共有ユーザーの観点から、次の手順が記述されます。

1. 共有アカウントへの招待メールを受け取ったら、電子メールに記載されている手順に従って、自分のアカウントにログインします [!DNL Commerce] アカウント。

   アカウントの左側のナビゲーションパネルに、新しい _[!UICONTROL Shared with me]_タブをクリックします。 The_[!UICONTROL Switch Accounts]_ 右上隅のコントロールには、次のオプションがあります： `My Account` 共有アカウントの名前。

   ![自分と共有済み](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. 共有アカウントにアクセスするには、 **[!UICONTROL Switch Accounts]** を共有アカウントの名前に追加します。

   ![共有アカウントに切り替え](./assets/shared-switch.png){width="600" zoomable="yes"}

   共有アカウントには、お知らせメッセージと連絡先情報が表示されます。 左側のナビゲーションパネルには、使用権限のある項目のみが含まれます。

1. 共有アカウントをヘルプセンターに接続するには、 **[!UICONTROL Support]** 共有アカウントの左側のナビゲーションパネル

   ![サポート](./assets/shared-support.png){width="600" zoomable="yes"}

   以下を使用すると、 [Adobe Commerce Help Center](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) 共有アカウントから記事やトラブルシューティング情報を検索し、既知の問題のパッチを見つけて、サポートチケットを作成します。

   >[!NOTE]
   >
   >共有アクセス権を受け取ったユーザーは、 [[!DNL Commerce] アカウント](https://account.magento.com/customer/account/login)に移動します。 _共有アクセス_&#x200B;をクリックし、 **[!UICONTROL Support]** タブをクリックします。 このアクションは、 [Adobe Commerce Support Knowledge Base](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html) が `SSO` を呼び出します。

1. 自分のアカウントに戻るには、 **戻る** ( ブラウザーコントロールおよび **[!UICONTROL Switch Accounts]** から `My Account`.

## 共有アクセスを取り消す

1. コマースアカウントにサインインします。

1. 左側のナビゲーションパネルで、 **[!UICONTROL Shared Access]**.

1. 取り消されるアカウントを検索します。 _[!UICONTROL Managing Users & Permissions]_をクリックします。**[!UICONTROL Delete]**.

1. 確認するメッセージが表示されたら、「 **[!UICONTROL Delete User]**.

>[!NOTE]
>
>共有名が _MAG からのクラウド共有アクセス[XYZ]_ 」と入力します。 詳しくは、 [クラウドプロジェクトを介して共有アクセス権を付与されたユーザーを削除する方法を教えてください。](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
