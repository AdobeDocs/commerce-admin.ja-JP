---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] ページで設定を確認します。
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![ ギフト カード E メールの設定 ](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | ストア表示 | ギフト カード通知 E メールの送信者として表示される [ 店舗連絡先 ](../../getting-started/store-details.md#store-email-addresses) を識別します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | ストア表示 | ギフト カード通知 E メールに使用する [ テンプレート ](../../systems/email-templates.md) を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![ ギフト カードの一般設定 ](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redeemable] | グローバル | ギフトカードの所有者が現金に対する価値を引き換えることができるかどうかを決定します。 オプション：`Yes`/`No`。 |
| [!UICONTROL Lifetime (days)] | グローバル | カードが有効な日数を決定します。 空白のままにすると、カードの有効期限は切れません。 <br/><br/>**_重要：_**一部の場所では、ギフトカードに有効期限データを設定することは違法です。 ギフトカードの有効期間を設定する前に、地域の法律を確認してください。 |
| [!UICONTROL Allow Gift Message] | ストア表示 | ギフトカードを購入したお客様がギフトメッセージを含めるオプションを利用できるかどうかを決定します。 オプション：`Yes`/`No`。 |
| [!UICONTROL Gift Message Maximum Length] | ストア表示 | ギフト カード メッセージで許可される最大文字数を決定します。 デフォルト値：255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | グローバル | 顧客が注文を行うとき、または注文が請求されるときにギフト カード アカウントが生成されるかどうかを決定します。 オプション：`Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![ ギフト カード アカウント管理から送信された電子メール ](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | ストア表示 | ギフト カード E メールの送信者として表示される [ 店舗連絡先 ](../../getting-started/store-details.md#store-email-addresses) を識別します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Template] | ストア表示 | ギフト カードの電子メールに使用する [ テンプレート ](../../systems/email-templates.md) を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![ ギフト カード アカウントの一般設定 ](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | グローバル | ギフト カード コードの長さを決定します。 |
| [!UICONTROL Code Format] | グローバル | ギフト カード コードの形式を決定します。 オプション：`Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | グローバル | コードの先頭に追加するプレフィックスを定義します。 |
| [!UICONTROL Code Suffix] | グローバル | コードの末尾に追加するサフィックスを定義します。 |
| [!UICONTROL Dash Every X Characters] | グローバル | コードにダッシュを含める場合、は各ダッシュの文字数を決定します。 |
| [!UICONTROL New Pool Size] | グローバル | 生成される新しいコード プールのサイズを決定します。 |
| [!UICONTROL Low Code Pool Threshold] | グローバル | プールの補充が必要な警告をトリガーするコード プール内のレコード数を指定します。 |
| [!UICONTROL Generate] | グローバル | クリックして、ギフト カード コードの一覧を生成します。 |

{style="table-layout:auto"}
