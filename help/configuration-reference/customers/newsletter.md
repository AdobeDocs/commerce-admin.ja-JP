---
title: '[!UICONTROL Customers] > [!UICONTROL Newsletter]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Newsletter] ページで設定を確認します。
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '237'
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
