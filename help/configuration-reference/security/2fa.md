---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: 次のページで設定を確認します： [!UICONTROL Security] &gt; [!UICONTROL 2FA] コマース管理のページ。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>AdobeIdentity Managementサービス (IMS) の認証を有効にしたストアでは、ネイティブのAdobe CommerceとMagento Open Sourceの 2 要素認証 (2FA) が無効になっています。 Adobe資格情報を使用してAdobe Commerceインスタンスにログインしている管理者ユーザーは、多くの管理者タスクを再認証する必要はありません。 認証は、管理者Adobe IMSが現在のセッションにログインする際にユーザーによって処理されます。 詳しくは、 [Adobe CommerceとのAdobe IMSの概要](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

これらの設定の変更について詳しくは、 [二段階認証 (2FA)](../../systems/security-two-factor-authentication.md) （内） _管理システムガイド_.

## [!UICONTROL General]

![一般](./assets/2fa-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | グローバル | 必要な 2 要素認証方式を示します。 複数のプロバイダーを選択した場合、各ユーザーは次回ログイン時に各 2FA メソッドを設定する必要があります。 |
| [!UICONTROL Configuration Email URL for Web API] | グローバル | カスタム実装の場合、に送信される代替電子メール設定リンクの URL _管理者_ 初回ログイン時のユーザー。 E メールテンプレートで、プレースホルダーを使用します。 `:tfat` を使用して、トークンが挿入される場所を示します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | グローバル | Google Authenticator で生成される各 1 回限りのパスワード (OTP) の有効期間（秒）です。 デフォルト： `30` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Duo Security]

![Duo セキュリティ](./assets/2fa-duo-security.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | グローバル | 統合キー ( [!DNL Duo Security] アカウント。 |
| [!UICONTROL Secret Key] | グローバル | 次の秘密鍵： [!DNL Duo Security] アカウント。 |
| [!UICONTROL API Hostname] | グローバル | 次の API ホスト名 [!DNL Duo Security] アカウント。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API Key] | グローバル | の API キー [!DNL Authy] アカウント。 |
| [!UICONTROL OneTouch Message] | グローバル | メッセージが [!DNL Authy] ログイン時の認証子。 デフォルト： `Login request to your Magento Admin` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL U2F Key]

![U2F キー](./assets/2fa-u2f-key.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | グローバル | 発行および処理に使用されるドメイン [!DNL WebAuthn] カスタム WebAPI 実装の課題。 |

{:style=&quot;table-layout:auto&quot;}
