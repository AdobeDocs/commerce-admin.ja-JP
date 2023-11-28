---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: 次のページで設定を確認します： [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] コマース管理のページ。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![メールテンプレート](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://docs.magento.com/user-guide/marketing/email-template-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | 顧客がストア内の製品に関する電子メールを友人に送信できるようにするプロセスをアクティブ化します。 オプション： `Yes` / `No` |
| [!UICONTROL Select Email Template] | ストア表示 | が生成するメッセージに使用する電子メールテンプレートを識別します。 _友達にメールを送信_ 関数に置き換えます。 デフォルトのテンプレート： `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | ストア表示 | 友達に製品に関する E メールを送信するために、送信者が登録済みの顧客である必要があるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Max Recipients] | ストア表示 | 1 件の E メールの配信リストに登録できる人数を制限します。 |
| [!UICONTROL Max Products Sent in 1  Hour] | ストア表示 | 1 時間の間に 1 人のユーザーが共有できる製品の数を制限します。 |
| [!UICONTROL Limit Sending By] | ストア表示 | 送信者の識別に使用する方法を決定します。 オプションは次のとおりです。 <br/>**`IP Address`**- （推奨）製品の E メールの送信に使用されるコンピューターの IP アドレスで送信者を識別します。<br/>**`Cookie (unsafe)`**  — 送信者をブラウザーの Cookie で識別します。 ユーザーは制限を避けるために Cookie を削除できるので、このメソッドは安全ではありません。 |

{:style=&quot;table-layout:auto&quot;}
