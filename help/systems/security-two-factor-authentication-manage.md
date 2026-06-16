---
title: 二段階認証の管理
description: 2要素認証を管理し、管理者ユーザーの認証者をリセットする方法について説明します。
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# 二段階認証の管理

2要素認証（2FA）で&#x200B;_管理者_&#x200B;にログインできないユーザーは、同期を試みるか、問題のトラブルシューティングを行うことができます。 アカウントに関連付けられている認証者をリセットすることもできます。 リセット時に、ユーザーは再度ログインし、必要な認証者を再設定する必要があります。

2FAでログインする際に問題が発生した場合は、次の点を考慮してください。

- 一部のモバイルアプリには、同期オプションが用意されています。 このオプションは、アプリとサーバーを再接続し、デバイスとサーバーの時間設定を同期します。
- デバイスの取り消しや認証者のリセットは、ユーザーの接続に役立ちます。
- Adobe CommerceまたはMagento Open Source インストール用のweb キャッシュとCookieの消去も役立ちます。 Googleなどの認証者は、生成されたCookieを使用して、アクセス権と期間を保存します。 特定のブラウザーとストアドメインのCookieを消去します。
- Cookieをブロックすると、[!DNL Google Authenticator]などの一部の認証者が検証プロセスを完了できなくなります。 Adobe Commerceのインストール時にCookieを許可するルールをブラウザーに追加します。

コマンドラインから認証者をリセットし、より高度なトラブルシューティング情報を得るには、開発者ドキュメントの[2要素認証](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/)を参照してください。

**_ユーザーアカウントの認証者をリセットするには:_**

>[!NOTE]
>
>他のユーザーの2FA プロバイダーをリセットするには、`All`権限を持つ&#x200B;_管理者_&#x200B;であるか、[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth]および[!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users]を選択した役割に`Custom`権限が必要です。 詳しくは、[&#x200B; ユーザーの役割](permissions-user-roles.md)を参照してください。

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**&#x200B;に移動します。

1. ユーザーを選択し、アカウントを編集モードで開きます。

1. _[!UICONTROL Current User Identity Verification]_&#x200B;セクションまでスクロールして、パスワードを入力します。

1. 左側のパネルで、**[!UICONTROL 2FA]**&#x200B;をクリックします。

1. _[!UICONTROL Configuration reset]_&#x200B;セクションで、**[!UICONTROL Reset]**&#x200B;と&#x200B;**[!UICONTROL OK]**&#x200B;をクリックして確定します。

   ![&#x200B; ユーザーアカウント - 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}を有効にする

   ユーザーが必要な2FA メソッドをアカウントに復元する場合は、_サインオン_ ページからそれぞれ再構成する必要があります。

1. 完了したら、**[!UICONTROL Save User]**&#x200B;をクリックします。
