---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] コマース管理のページ。
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![ギフトカードのメール設定](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | ストア表示 | を識別します。 [ストア連絡先](../../getting-started/store-details.md#store-email-addresses) ギフトカードの通知 E メールの送信者として表示される。 デフォルト値： `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | ストア表示 | を決定します。 [テンプレート](../../systems/email-templates.md) ギフトカードの通知 E メールに使用される。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Gift Card General Settings]

![ギフトカードの一般設定](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redeemable] | グローバル | ギフトカードの所有者が現金でその価値を引き換えることができるかどうかを決定します。 オプション： `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | グローバル | カードが有効である日数を判断します。 空白の場合、カードは期限切れになりません。 <br/><br/>**_重要：_**一部の場所では、ギフトカードに有効期限のデータを設定することは違法です。 ギフトカードの有効期間を設定する前に、現地の法律を確認してください。 |
| [!UICONTROL Allow Gift Message] | ストア表示 | ギフトカードを購入した顧客がギフトメッセージを含めるオプションを利用できるかどうかを指定します。 オプション： `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | ストア表示 | ギフトカードメッセージで許可される最大文字数を指定します。 デフォルト値：255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | グローバル | 顧客が注文を行ったとき、または注文が請求されたときに、ギフトカードのアカウントが生成されるかどうかを指定します。 オプション： `Ordered` / `Invoiced` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Email Sent from Gift Card Account Management]

![ギフトカードアカウント管理から送信されたメール](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | ストア表示 | を識別します。 [ストア連絡先](../../getting-started/store-details.md#store-email-addresses) ギフトカードの e メールの送信者として表示される デフォルト値： `General Contact` |
| [!UICONTROL Gift Card Template] | ストア表示 | を決定します。 [テンプレート](../../systems/email-templates.md) ギフトカードの E メールに使用される。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Gift Card Account General Settings]

![ギフトカードアカウントの一般設定](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | グローバル | ギフトカードコードの長さを決定します。 |
| [!UICONTROL Code Format] | グローバル | ギフトカードコードの形式を決定します。 オプション： `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | グローバル | コードの先頭に追加されるプレフィックスを定義します。 |
| [!UICONTROL Code Suffix] | グローバル | コードの末尾に追加されるサフィックスを定義します。 |
| [!UICONTROL Dash Every X Characters] | グローバル | コードにダッシュを含める場合は、各ダッシュの間の文字数をで決定します。 |
| [!UICONTROL New Pool Size] | グローバル | 生成する新しいコードプールのサイズを決定します。 |
| [!UICONTROL Low Code Pool Threshold] | グローバル | プールの補充が必要なアラートをトリガーするコード・プール内のレコード数を決定します。 |
| [!UICONTROL Generate] | グローバル | ギフトカードコードのリストを生成するには、ここをクリックします。 |

{:style=&quot;table-layout:auto&quot;}
