---
title: '[!UICONTROL Customers] > [!UICONTROL Invitations]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Invitations] ページで設定を確認します。
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![一般](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | グローバル | 招待モジュールが有効かどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | web サイト | 招待をストアフロントから管理できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Referred Customer Group] | ストアビュー | 招待者の顧客グループを決定します。 オプション：<br/>**`Same as Inviter`**– 招待者は、招待した顧客と同じ顧客グループに自動的に割り当てられます。<br/>**`Default Customer Group from Configuration`** – 招待者には、デフォルトの[顧客グループ ](../../customers/customer-groups.md)が自動的に設定されます。 |
| [!UICONTROL New Accounts Registration] | ストアビュー | 招待者がアカウントを作成する方法を指定します。 オプション：<br/>**`By Invitation Only`**– 招待されたユーザーは、アカウントを作成するために、招待メールのリンクに従う必要があります。<br/>**`Available to All`** – 招待者は、店舗で利用可能なアカウント登録フォームを使用できます。 |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | ストアビュー | 招待フォームに、招待者が電子メールで招待者に送信するカスタムメッセージを追加できるフィールドがあるかどうかを指定します。 これは、管理者が招待にメッセージを追加する機能には影響しません。 オプション：`Yes` / `No`。 |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | ストアビュー | 招待者が一度に送信できる招待状の最大数を指定します。 招待者がフォームに含める各電子メールアドレスに異なる招待状が送信されます。 これにより、大量の招待状が一度に送信されるのを防ぐことにより、サーバーのリソースを保護し、招待状がスパムとして送信される可能性が低くなります。 |

{style="table-layout:auto"}

## [!UICONTROL Email]

![電子メール ](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | ストアビュー | 招待メールの送信時に招待者が受け取るメールの送信者を指定します。 デフォルト値：`General Contact` |
| [!UICONTROL Customer Invitation Email Template] | ストアビュー | 招待メールの送信時に招待者が受け取るメールのテンプレートを指定します。 既定のテンプレート：`Customer Invitation` |

{style="table-layout:auto"}
