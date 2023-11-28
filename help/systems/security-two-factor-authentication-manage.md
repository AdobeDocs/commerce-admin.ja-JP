---
title: 2 要素認証の管理
description: 2 要素認証を管理し、管理者ユーザーの認証子をリセットする方法を説明します。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# 2 要素認証の管理

にログインできないユーザー _管理者_ 2 要素認証 (2FA) を使用すると、問題の同期やトラブルシューティングを試みることができます。 また、アカウントに関連付けられた認証子をリセットすることもできます。 リセット時に、ユーザーは再度サインインし、必要な認証子を再設定する必要があります。

2FA を使用したログインで問題が発生した場合は、以下の点を考慮してください。

- 一部のモバイルアプリには同期オプションが含まれています。 このオプションは、アプリとサーバーに再接続し、デバイスとサーバーの時間設定を同期します。
- デバイスの取り消しや認証子のリセットは、ユーザーの接続に役立ちます。
- また、Adobe CommerceまたはMagento Open Sourceのインストールで Web キャッシュと Cookie を消去することも役立ちます。 Googleなどの認証子は、生成された Cookie を使用して、アクセスと期間を保存します。 特定のブラウザーおよびストアドメインの cookie をクリアします。
- Cookie をブロックすると、 [!DNL Google Authenticator]検証プロセスの完了から。 Adobe Commerceのインストールに対する cookie を許可するルールをブラウザーに追加します。

コマンドラインから認証子をリセットする方法と詳細なトラブルシューティング情報については、 [二段階認証](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) （開発者向けドキュメント）。

**_ユーザー・アカウントの認証子をリセットするには、次の手順に従います。_**

>[!NOTE]
>
>他のユーザーの 2FA プロバイダーをリセットするには、 _administrator_ 次を使用 `All` 権限、または `Custom` の役割に対する権限 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] および [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] 選択済み 詳しくは、 [ユーザーの役割](permissions-user-roles.md).

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. ユーザーを選択し、編集モードでアカウントを開きます。

1. 下にスクロールして、 _[!UICONTROL Current User Identity Verification]_」セクションに入力し、パスワードを入力します。

1. 左側のパネルで、 **[!UICONTROL 2FA]**.

1. Adobe Analytics の _[!UICONTROL Configuration reset]_セクションで、**[!UICONTROL Reset]**および&#x200B;**[!UICONTROL OK]**をクリックして確定します。

   ![ユーザーアカウント — 2FA を有効にする](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   必要な 2FA メソッドをアカウントに復元する場合は、 _サインオン_ ページに貼り付けます。

1. 完了したら、「 **[!UICONTROL Save User]**.
