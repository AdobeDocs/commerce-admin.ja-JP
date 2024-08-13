---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Commerce Admin の [!UICONTROL Security] &gt; [!UICONTROL 2FA] ページで設定を確認します。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>AdobeIdentity Management サービス（IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceおよびMagento Open Source二要素認証（2FA）が無効になっています。 Adobe資格情報を使用してAdobe Commerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 [Adobe CommerceとAdobe IMSの統合：概要 ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html) を参照してください。

{{config}}

これらの設定の変更について詳しくは、『 [ 管理システムガイド _の ](../../systems/security-two-factor-authentication.md)2 要素認証（2FA）_ を参照してください。

## [!UICONTROL General]

![ 一般 ](./assets/2fa-general.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | グローバル | 必要な 2 要素認証方式を示します。 複数のプロバイダを選択した場合、各ユーザーは次回ログイン時に各 2FA メソッドを構成する必要があります。 |
| [!UICONTROL Configuration Email URL for Web API] | グローバル | カスタム実装の場合、最初のログイン時に _管理者_ ユーザーに送信される代替メール設定リンクの URL です。 メールテンプレートで、プレースホルダー `:tfat` を使用して、トークンの挿入場所を示します。 |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | グローバル | アカウントが一時的に無効になるまでに管理者が [!DNL one-time password (OTP)] を入力できる回数を決定します。 デフォルト：`10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | グローバル | アカウントが一時的に無効になるまでに、管理者が [!DNL one-time password (OTP)] ールを入力するのを待つ時間（秒）を決定します。 デフォルト：`300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | グローバル | システムが管理者の [!DNL one-time-password (OTP)] ールの有効期限が切れてから受け入れる時間（秒）を決定します。 単一の OTP の有効期間（通常は 30 秒）よりも長くすることはできません。 デフォルト：`29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo セキュリティ ](./assets/2fa-duo-security.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | グローバル | [!DNL Duo Security] アカウントの統合キー。 |
| [!UICONTROL Secret Key] | グローバル | [!DNL Duo Security] アカウントの秘密鍵。 |
| [!UICONTROL API Hostname] | グローバル | [!DNL Duo Security] アカウントの API ホスト名。 |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API Key] | グローバル | [!DNL Authy] アカウントからの API キー。 |
| [!UICONTROL OneTouch Message] | グローバル | ログイン時に [!DNL Authy] 認証システムに表示されるメッセージです。 デフォルト：`Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F キー ](./assets/2fa-u2f-key.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | グローバル | カスタム WebAPI 実装の課題の発行と処理 [!DNL WebAuthn] 使用されるドメイン。 |

{style="table-layout:auto"}
