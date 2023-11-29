---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Invitations] コマース管理のページ。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![一般](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | グローバル | 招待モジュールを有効にするかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Web サイト | 招待をストアフロントから管理できるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | ストア表示 | 招待者の顧客グループを決定します。 オプション： <br/>**`Same as Inviter`**— 招待者は、招待した顧客と同じ顧客グループに自動的に割り当てられます。<br/>**`Default Customer Group from Configuration`**  — 招待者が自動的にデフォルトを持つ [顧客グループ](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | ストア表示 | 招待者がアカウントを作成する方法を指定します。 オプション： <br/>**`By Invitation Only`**— 招待者は、アカウントを作成するために、招待用電子メールのリンクに従う必要があります。<br/>**`Available to All`**  — 招待者は、ストアで利用可能なアカウント登録フォームを使用できます。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | ストア表示 | 招待者が電子メールで招待者に送信するカスタムメッセージを追加できるフィールドが招待フォームにあるかどうかを指定します。 これは、管理者が招待にメッセージを追加する機能には影響しません。 オプション： `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | ストア表示 | 招待者が一度に送信できる招待の最大数を指定します。 招待者がフォームに含める電子メールアドレスごとに異なる招待メールが送信されます。 これにより、多数の招待が一度に送信されるのを防ぐことで、サーバーのリソースを保護し、招待がスパムとして送信される可能性を低くします。 |

{style="table-layout:auto"}

## [!UICONTROL Email]

![電子メール](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://docs.magento.com/user-guide/marketing/invitations-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | ストア表示 | 招待メールの送信者が招待メールの送信時に受け取る電子メールの送信者を指定します。 デフォルト値： `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | ストア表示 | 招待 E メールの送信時に招待者が受け取る E メールのテンプレートを指定します。 デフォルトのテンプレート： `Customer Invitation` |

{style="table-layout:auto"}
