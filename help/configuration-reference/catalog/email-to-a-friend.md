---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Commerce管理者の[!UICONTROL Catalog] > [!UICONTROL Email to a Friend] ページで設定を確認します。
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![&#x200B; メールテンプレート &#x200B;](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

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
