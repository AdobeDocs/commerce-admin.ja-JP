---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: の設定を確認します。 [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] コマース管理者のページ。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![メールテンプレート](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | ストア内の商品に関する電子メールを顧客が友人に送信できるようにするプロセスをアクティブ化します。 オプション： `Yes` / `No` |
| [!UICONTROL Select Email Template] | ストア表示 | によって生成されるメッセージに使用されるメールテンプレートを識別します _友達にメールを送信_ 関数。 デフォルトのテンプレート： `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | ストア表示 | 送信者が製品に関するメールを友人に送信するには、登録済みの顧客である必要があるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Max Recipients] | ストア表示 | 1 通のメールに対して、配信リストに登録できるユーザーの数を制限します。 |
| [!UICONTROL Max Products Sent in 1  Hour] | ストア表示 | 1 時間に 1 人のユーザーが共有できる製品の数を制限します。 |
| [!UICONTROL Limit Sending By] | ストア表示 | 送信者の識別に使用する方法を決定します。 次のようなオプションがあります。 <br/>**`IP Address`**- （推奨）製品メールの送信に使用されるコンピューターの IP アドレスで送信者を識別します。<br/>**`Cookie (unsafe)`**  – 送信者をブラウザーの cookie で識別します。 このメソッドは、ユーザーが制限を回避するために cookie を削除できるので、安全ではありません。 |

{style="table-layout:auto"}
