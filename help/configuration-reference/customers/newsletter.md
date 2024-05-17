---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Newsletter]'
description: の設定を確認します。 [!UICONTROL Customers] &gt; [!UICONTROL Newsletter] コマース管理者のページ。
exl-id: a97003ca-985e-47fa-9ff3-677e05ef3729
feature: Configuration, Customers, Communications
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Newsletter]

{{config}}

>[!NOTE]
>
>ニュースレターは、顧客にニュース、割引、その他のマーケティング電子メールを送信できるマーケティング手段の一部です。 登録済みのお客様は、こちらからサブスクリプションを管理できます [アカウントダッシュボード](../../customers/account-dashboard-my-account.md).

## [!UICONTROL General Options]

![一般オプション](./assets/newsletter-general-options.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | ストア表示 | ストア表示範囲に対してニュースレターを有効にするかどうかを決定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Subscription Options]

![購読オプション](./assets/newsletter-subscription-options.png)<!-- zoom -->

<!-- [Subscription Options](https://docs.magento.com/user-guide/marketing/newsletter-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Guest Subscription] | ストア表示 | 未登録のゲストがニュースレターを購読できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Need to Confirm] | ストア表示 | 購読リクエストを確認する必要があるかどうかを決定します。 このダブルオプトイン方法は、ユーザーが同意なしに購読できないようにする検証手段です。 オプション： `Yes` / `No` |
| [!UICONTROL Confirmation Email Sender] | ストア表示 | 購読リクエストの確認のために送信されるメールの送信者として表示されるストアの連絡先を識別します。 |
| [!UICONTROL Confirmation Email Template] | ストア表示 | ニュースレターの購読リクエストを確認するために送信される通知に使用されるメールテンプレートを決定します。 デフォルトのテンプレート： `Newsletter subscription confirmation` |
| 成功したメールの送信者 | ストア表示 | ニュースレターの購読に成功したユーザーに送信されるメールの送信者として表示されるストア連絡先を識別します。 |
| [!UICONTROL Success Email Template] | ストア表示 | ニュースレターの購読に成功したユーザーに送信される通知に使用されるメールテンプレートを決定します。 デフォルトのテンプレート： `Newsletter subscription success` |
| [!UICONTROL Unsubscription Email Sender] | ストア表示 | ニュースレターの購読の終了をリクエストするユーザーに送信されるメールの送信者として表示されるストア連絡先を識別します。 |
| [!UICONTROL Unsubscription Email Template] | ストア表示 | ニュースレター購読の終了をリクエストするユーザーに送信される通知に使用されるメールテンプレートを決定します。 デフォルトのテンプレート： `Newsletter unsubscription success` |

{style="table-layout:auto"}
