---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Gift Cards] ページで設定を確認します。
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![&#x200B; ギフトカードのメール設定](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | ストアビュー | ギフトカード通知メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を識別します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | ストアビュー | ギフトカード通知メールに使用される[&#x200B; テンプレート &#x200B;](../../systems/email-templates.md)を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![&#x200B; ギフトカードの一般設定](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redeemable] | グローバル | ギフトカードの所有者が現金の価値を引き換えることができるかどうかを決定します。 オプション：`Yes` / `No`。 |
| [!UICONTROL Lifetime (days)] | グローバル | カードが有効な日数を指定します。 空白のままにすると、カードの有効期限は切れません。 <br/><br/>**_Important:_**&#x200B;一部の地域では、ギフトカードに有効期限データを設定することは違法です。 ギフトカードの有効期間を設定する前に、地域の法律を確認してください。 |
| [!UICONTROL Allow Gift Message] | ストアビュー | ギフトカードを購入したお客様が、ギフトメッセージを含めるオプションを利用できるかどうかを指定します。 オプション：`Yes` / `No`。 |
| [!UICONTROL Gift Message Maximum Length] | ストアビュー | ギフトカードメッセージで許可される最大文字数を指定します。 デフォルト値：255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | グローバル | 顧客が注文を行ったときにギフトカードのアカウントが生成されるか、注文が請求されたときに生成されるかを指定します。 オプション：`Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![&#x200B; ギフトカードアカウント管理からメールが送信されました](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | ストアビュー | ギフトカードの電子メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を特定します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Template] | ストアビュー | ギフトカードの電子メールに使用される[&#x200B; テンプレート &#x200B;](../../systems/email-templates.md)を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![&#x200B; ギフトカードアカウントの一般設定](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | グローバル | ギフトカードコードの長さを指定します。 |
| [!UICONTROL Code Format] | グローバル | ギフトカードコードの形式を決定します。 オプション：`Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | グローバル | コードの先頭に追加された任意の接頭辞を定義します。 |
| [!UICONTROL Code Suffix] | グローバル | コードの末尾に追加されたサフィックスを定義します。 |
| [!UICONTROL Dash Every X Characters] | グローバル | コードにダッシュを含める場合は、各ダッシュ間の文字数を指定します。 |
| [!UICONTROL New Pool Size] | グローバル | 生成する新しいコードプールのサイズを決定します。 |
| [!UICONTROL Low Code Pool Threshold] | グローバル | プールの補充が必要なアラートをトリガーするコードプール内のレコードの数を指定します。 |
| [!UICONTROL Generate] | グローバル | クリックして、ギフトカードコードのリストを生成します。 |

{style="table-layout:auto"}
