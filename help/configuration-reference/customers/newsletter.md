---
title: '[!UICONTROL Customers] > [!UICONTROL Newsletter]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Newsletter] ページで設定を確認します。
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
TQID: https://experienceleague.adobe.com/rqG5WOxVnMnlKTSiSHYgl-3Q5Yy4nIKWOjAev35UYHA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Newsletter]

{{config}}

>[!NOTE]
>
>ニュースレターは、顧客にニュース、割引、その他のマーケティングメールを送信できるマーケティング手段の一部です。 登録済みのお客様は、[&#x200B; アカウントダッシュボード &#x200B;](../../customers/account-dashboard-my-account.md)からサブスクリプションを管理できます。

## [!UICONTROL General Options]

![一般オプション &#x200B;](./assets/newsletter-general-options.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストアビュー | ストアビューのスコープでニュースレターを有効にするかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![&#x200B; サブスクリプションオプション &#x200B;](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/newsletters/newsletters) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Guest Subscription] | ストアビュー | 未登録のゲストがニュースレターを購読できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Need to Confirm] | ストアビュー | サブスクリプションのリクエストを確認する必要があるかどうかを決定します。 このダブルオプトイン方法は、個人の同意なしに購読されるのを防ぐ検証措置です。 オプション：`Yes` / `No` |
| [!UICONTROL Confirmation Email Sender] | ストアビュー | 購読リクエストを確認するために送信されたメールの送信者として表示されるストア連絡先を識別します。 |
| [!UICONTROL Confirmation Email Template] | ストアビュー | ニュースレターの購読リクエストを確認するために送信される通知に使用されるメールテンプレートを決定します。 既定のテンプレート：`Newsletter subscription confirmation` |
| 成功メール送信者 | ストアビュー | ニュースレターの購読に成功したユーザーに送信されたメールの送信者として表示されるストア連絡先を識別します。 |
| [!UICONTROL Success Email Template] | ストアビュー | ニュースレターを正常に購読したユーザーに送信される通知に使用される電子メールテンプレートを決定します。 既定のテンプレート：`Newsletter subscription success` |
| [!UICONTROL Unsubscription Email Sender] | ストアビュー | ニュースレターの購読の終了をリクエストするユーザーに送信されたメールの送信者として表示されるストア連絡先を識別します。 |
| [!UICONTROL Unsubscription Email Template] | ストアビュー | ニュースレターの購読の終了をリクエストするユーザーに送信される通知に使用されるメールテンプレートを決定します。 既定のテンプレート：`Newsletter unsubscription success` |

{style="table-layout:auto"}
