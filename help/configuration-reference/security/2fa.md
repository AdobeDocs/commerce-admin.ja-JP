---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: の設定を確認します。 [!UICONTROL Security] &gt; [!UICONTROL 2FA] コマース管理者のページ。
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: d6f9c5186276b28cada318cbe765e2271d34bb58
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>AdobeIdentity Management サービス（IMS）認証を有効にしているストアでは、ネイティブのAdobe CommerceおよびMagento Open Source二要素認証（2FA）が無効になっています。 Adobe資格情報を使用してAdobe Commerce インスタンスにログインしている管理者ユーザーは、多くの管理タスクで再認証する必要はありません。 Adobe IMSは、管理者ユーザーが現在のセッションにログインする際に認証を処理します。 参照： [Adobe CommerceとAdobe IMSの統合：概要](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

これらの設定の変更の詳細については、を参照してください [2 要素認証（2FA）](../../systems/security-two-factor-authentication.md) が含まれる _管理システムガイド_.

## [!UICONTROL General]

![一般](./assets/2fa-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | グローバル | 必要な 2 要素認証方式を示します。 複数のプロバイダを選択した場合、各ユーザーは次回ログイン時に各 2FA メソッドを構成する必要があります。 |
| [!UICONTROL Configuration Email URL for Web API] | グローバル | カスタム実装の場合、に送信される代替メール設定リンクの URL です _Admin_ 初回ログイン時のユーザー。 メールテンプレートで、プレースホルダーを使用します `:tfat` トークンの挿入場所を示します。 |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | グローバル | 管理者のワンタイムパスワード（OTP）の有効期限が切れてから、システムがその OTP を受け入れる時間（秒）を決定します。 単一の OTP の有効期間（通常は 30 秒）よりも長くすることはできません。 デフォルト： `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo セキュリティ](./assets/2fa-duo-security.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | グローバル | の統合キー [!DNL Duo Security] アカウント。 |
| [!UICONTROL Secret Key] | グローバル | の秘密鍵 [!DNL Duo Security] アカウント。 |
| [!UICONTROL API Hostname] | グローバル | からの API ホスト名 [!DNL Duo Security] アカウント。 |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![作成者](./assets/2fa-authy.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL API Key] | グローバル | からの API キー [!DNL Authy] アカウント。 |
| [!UICONTROL OneTouch Message] | グローバル | に表示されるメッセージ [!DNL Authy] ログイン時に認証します。 デフォルト： `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F キー](./assets/2fa-u2f-key.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | グローバル | 発行および処理に使用されるドメイン [!DNL WebAuthn] カスタム WebAPI 実装の課題。 |

{style="table-layout:auto"}
