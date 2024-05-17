---
title: 二要素認証の管理
description: 二要素認証を管理し、管理者ユーザーの認証者をリセットする方法を説明します。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# 二要素認証の管理

にログインできないユーザー _Admin_ 2 要素認証（2FA）を使用すると、問題の同期またはトラブルシューティングを試みることができます。 また、アカウントに関連付けられた認証をリセットすることもできます。 リセットした場合、ユーザーは再度ログインし、必要な認証を再設定する必要があります。

2FA でのログインに問題がある場合は、次の点を考慮してください。

- 一部のモバイルアプリには同期オプションが含まれています。 このオプションは、アプリとサーバーを再接続し、デバイスとサーバーの時間設定を同期します。
- デバイスを取り消したり、認証システムをリセットしたりすると、ユーザーが接続しやすくなります。
- Adobe CommerceまたはMagento Open Sourceのインストール用の web キャッシュと Cookie のクリアも役に立ちます。 Googleなどの認証者は、生成された Cookie を使用してアクセスと期間を保存します。 特定のブラウザーおよびストアドメインの Cookie をクリアします。
- Cookie をブロックすると、次のような一部の認証を防ぐことができます [!DNL Google Authenticator]：検証プロセスの完了から。 ブラウザーに、Adobe Commerceのインストールに対して cookie を許可するルールを追加します。

コマンドラインからオーセンティケータをリセットする方法や、より詳細なトラブルシューティング情報については、を参照してください。 [二要素認証](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) 開発者向けドキュメント

**_ユーザー・アカウントの認証をリセットするには：_**

>[!NOTE]
>
>他のユーザーの 2FA プロバイダーをリセットするには、 _管理者_ （を使用） `All` 権限、または持つ `Custom` での役割の権限 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] および [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] を選択しました。 詳しくは、 [ユーザーの役割](permissions-user-roles.md).

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. ユーザーを選択し、アカウントを編集モードで開きます。

1. にスクロール ダウンします。 _[!UICONTROL Current User Identity Verification]_セクションとパスワードを入力します。

1. 左側のパネルで、 **[!UICONTROL 2FA]**.

1. が含まれる _[!UICONTROL Configuration reset]_セクションで、をクリック&#x200B;**[!UICONTROL Reset]**および&#x200B;**[!UICONTROL OK]**を確認します。

   ![ユーザーアカウント - 2FA の有効化](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   ユーザーが必要な 2FA メソッドを自分のアカウントにリストアする場合は、 _サインオン_ ページ。

1. 完了したら、 **[!UICONTROL Save User]**.
