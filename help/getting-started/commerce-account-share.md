---
title: ' [!DNL Commerce]  アカウントを共有'
description: 他の [!DNL Commerce]  アカウント所有者に対して [!DNL Commerce]  アカウントへの制限付きアクセス権を付与する方法について説明します。
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: 593bad9ca83e96a145beeceb0265e0080e5f7930
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# [!DNL Commerce] アカウントを共有

お客様の[!DNL Commerce] アカウントには、サイトの管理を支援する信頼できる従業員およびサービスプロバイダーが利用できる情報が含まれています。 アカウントへのアクセスを共有しても、請求履歴やクレジットカード情報などの機密情報はすべて保護され、他のユーザーは利用できなくなります。

プライマリ アカウント所有者には、他の[!DNL Commerce] アカウント所有者への制限付きアクセス権を付与する権限があります。 共有アクセスは取り消すことができますが、転送することはできません。 ``Cloud Shared Access from MAG[XYZ]``件のエントリの場合、ユーザーレコード **をここで削除することはできませんが**、アクセス **は引き続き失効させることができます**。

適切な権限を持つプライマリアカウント所有者のみが、正式に共有アクセス権を付与できます。 プライマリの口座名義人がアクセスできなくなったか、会社を退社した場合、お客様は[Commerce アカウント転送プロセス ](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-transfer)を使用して所有権を新しい連絡先に移行する必要があります。 Commerce サポートチームは、限られたシナリオにおいてお客様になりすますことができる場合がありますが、セキュリティと責任のリスクを軽減するために、お客様が共有アクセスを設定する必要があります。


![共有アクセス設定](./assets/shared-access.png){width="600" zoomable="yes"}

「請求履歴」セクションには、請求システムの変更前に作成された古い請求書のみが表示されます。 新しい請求書が表示されない場合、それらの請求書は新しいシステムに移行され、このビューからアクセスできません。

>[!IMPORTANT]
>
>共有アクセス権を持つユーザーが実行したすべてのアクションは、プライマリアカウント所有者のみが責任を負います。 Adobeは、お客様のアカウントへの共有アクセス権を持つユーザーが行ったアクションについては一切責任を負いません。

## 共有アカウントの設定

1. 開始する前に、**新しい共有アクセス権限者**&#x200B;の[!DNL Commerce] アカウントから次の情報を取得します。

   - ユーザーは既にaccount.adobe.comでアカウントに登録しており、account.magento.comを通じてログインしている必要があります。 詳しくは、[Commerce アカウントの作成](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)を参照してください。
   - `MAGE ID/Account ID (MAG00XXXXXXX)`は、_[!UICONTROL Magento]_タブの左上隅、**ログアウト**リンクのすぐ上に表示されます。
   - アカウントに関連付けられている`Email` アドレス。

1. [[!DNL Commerce]  アカウント ](commerce-account-create.md)にログインします。

1. 左側のナビゲーションパネルで、**[!UICONTROL Shared Access]**&#x200B;をクリックします。

1. **[!UICONTROL Add New User]**&#x200B;をクリックします。

   ![新しいユーザーを追加](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. [!UICONTROL _New User Information]_で、次の操作を行います。

   - 新規ユーザーの[!DNL Commerce] アカウントから&#x200B;**[!UICONTROL Account ID]**&#x200B;を入力します。
   - 新しいユーザーの[!DNL Commerce] アカウントに関連付けられている&#x200B;**[!UICONTROL Email]** アドレスを入力します。

   ![新規ユーザー情報](./assets/shared-new-user.png){width="600"}

1. _[!UICONTROL Shared Information]_で、次の操作を行います。

   - 共有アカウントを特定するには、**[!UICONTROL Share Name]**&#x200B;を入力します。 この名前は内部参照用であり、ユーザーとアカウントを共有するユーザーにのみ表示されます。

     組織名を[!UICONTROL Share Name]として使用することをお勧めします。 `CLOUD SHARED ACCESS FROM MAG XYX`で始まる名前は使用しないでください。
   - 新しいユーザーと個人の連絡先情報を共有する場合は、**[!UICONTROL Your Email]**&#x200B;と&#x200B;**[!UICONTROL Your Phone]**&#x200B;を入力します。

1. _[!UICONTROL Grant Account Permissions]_で、共有する各[!DNL Commerce]製品とサービスのチェックボックスを選択します。

   ![ アカウントに権限を付与](./assets/shared-permissions.png){width="600"}

1. **[!UICONTROL Create Shared Access]**&#x200B;をクリックします。

   新しいユーザー情報が共有アクセス ページの&#x200B;_[!UICONTROL Manage Permissions]_セクションに表示され、共有アカウントへのアクセス手順を記載したメール招待状が新しいユーザーに送信されます。

   ![共有アクセスの権限を管理](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>_[!UICONTROL Security Tool]_へのアクセスを共有する必要はありません。MAGE IDを持つすべてのユーザーは、自分のアカウントでセキュリティスキャンツールを設定できます。 サイトに変更を加え、[必要なメソッド ](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)）のいずれかを使用してドメインの所有権を検証するために必要な権限だけが必要です。

## 共有アカウントへのアクセス

共有アカウントへの招待を受け取った共有ユーザーの視点から、次の手順が記述されます。

1. 共有アカウントへの招待を受け取ったら、電子メールの指示に従って、自分の[!DNL Commerce] アカウントにログインします。

   アカウントの左側のナビゲーションパネルに新しい&#x200B;_[!UICONTROL Shared with me]_タブがあります。 右上隅の_[!UICONTROL Switch Accounts]_ コントロールには、`My Account`のオプションと共有アカウントの名前があります。

   ![自分と共有](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   _[!UICONTROL Switch Accounts]_コントロールが表示されない場合は、プライマリのアカウント所有者に連絡し、正しい[ アカウント情報](#set-up-a-shared-account)を入力したことを確認してください。


1. 共有アカウントにアクセスするには、共有アカウントの名前に&#x200B;**[!UICONTROL Switch Accounts]**&#x200B;を設定します。

   ![共有アカウントに切り替え](./assets/shared-switch.png){width="600" zoomable="yes"}

   共有アカウントには、ウェルカムメッセージと連絡先情報が表示されます。 左側のナビゲーションパネルには、使用する権限を持つ項目のみが含まれます。

1. 共有アカウントをヘルプセンターに接続するには、共有アカウントの左側のナビゲーションパネルで「**[!UICONTROL Support]**」をクリックします。

   ![ サポート ](./assets/shared-support.png){width="600" zoomable="yes"}

   共有アカウントの[Adobe Commerce ヘルプセンター](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)を使用して、記事とトラブルシューティング情報の検索、既知の問題に対するパッチの検索、サポートチケットの作成を行うことができます。

   >[!NOTE]
   >
   >共有アクセスを受け取った後、Experience Leagueで[ サポートケース ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)を送信するには、まず左側の列で「（[!DNL Commerce]）」で終わる組織名を選択してください。

1. 自分のアカウントに戻るには、ブラウザーコントロールで&#x200B;**戻る**&#x200B;をクリックし、**[!UICONTROL Switch Accounts]**&#x200B;を`My Account`に設定します。

## 共有アクセスを取り消す

1. Commerce アカウントにログインします。

1. 左側のナビゲーションパネルで、**[!UICONTROL Shared Access]**&#x200B;をクリックします。

1. _[!UICONTROL Managing Users & Permissions]_で失効するアカウントを見つけ、**[!UICONTROL Delete]**をクリックします。

   >[!NOTE]
   >
   > **[!UICONTROL Delete]**&#x200B;が表示されない場合は、**[!UICONTROL Share Name]**&#x200B;に命名パターン `Cloud Shared Access from MAG0XYZ`が含まれているかどうかを確認してください。 アカウントに[名前付けパターンがあり、削除できない](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)場合、これは、Shared Accessが[Commerce アカウント ](https://account.magento.com/)から直接ではなく、APIによって作成されたためです。
   > 
   > 削除できない場合は、アカウント所有者が共有アクセスアカウントを変更し、「アカウント権限を付与」で、すべての項目のチェックを外します。 このアップデートの後、ユーザーはアカウントリソースにアクセスできなくなります。
   > ![画像](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > また、ユーザーがメール通知を受け取らないように、ユーザーがプロジェクトから削除されていることを確認します。[以前のチームメンバーは、Adobe Commerce クラウド通知メールを受け取ります](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. 確認を求められたら、**[!UICONTROL Delete User]**&#x200B;をクリックします。

>[!NOTE]
>
>このインターフェイスでは、MAG[XYZ ]_から共有名_ Cloud Shared Accessのユーザーを削除することはできません。 [ クラウドプロジェクトを介して共有アクセスが許可されたユーザーを削除する方法を参照してください。](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)。

## 関連トピックス

[共有アクセスのトラブルシューティング](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)

