---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Commerce管理者の[!UICONTROL Catalog] > [!UICONTROL Email to a Friend] ページで設定を確認します。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![ メールテンプレート ](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストアビュー | ストア内の商品について、顧客が友人にメールを送信できるプロセスをアクティブ化します。 オプション：`Yes` / `No` |
| [!UICONTROL Select Email Template] | ストアビュー | _Email a Friend_&#x200B;関数によって生成されたメッセージに使用される電子メールテンプレートを識別します。 既定のテンプレート：`Send Product to Friend` |
| [!UICONTROL Allow for Guests] | ストアビュー | 製品に関する電子メールを友人に送信するために、送信者が登録済みの顧客である必要があるかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Max Recipients] | ストアビュー | 1つのメールの配信リストに登録できるユーザーの数を制限します。 |
| [!UICONTROL Max Products Sent in 1  Hour] | ストアビュー | 1時間の間に1人のユーザーが共有できる製品数を制限します。 |
| [!UICONTROL Limit Sending By] | ストアビュー | 送信者の識別に使用する方法を指定します。 オプション：<br/>**`IP Address`**- （推奨）製品メールの送信に使用されるコンピューターのIP アドレスで送信者を識別します。<br/>**`Cookie (unsafe)`** - ブラウザーのCookieで送信者を識別します。 ユーザーは制限を回避するためにCookieを削除できるため、このメソッドは安全ではありません。 |

{style="table-layout:auto"}
