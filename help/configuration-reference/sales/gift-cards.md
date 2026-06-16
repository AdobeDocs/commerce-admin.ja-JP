---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Gift Cards] ページで設定を確認します。
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/J-VH-mdaM7HrMRHJMNmmbBPggm1hjtHHWTh3q-5en0w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d9ced453-36f4-4eb5-b2f3-1d593e32476b
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
source-wordcount: 333
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![&#x200B; ギフトカードのメール設定](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | ストアビュー | ギフトカード通知メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を識別します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | ストアビュー | ギフトカード通知メールに使用される[&#x200B; テンプレート &#x200B;](../../systems/email-templates.md)を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![&#x200B; ギフトカードの一般設定](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

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

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | ストアビュー | ギフトカードの電子メールの送信者として表示される[&#x200B; ストア連絡先](../../getting-started/store-details.md#store-email-addresses)を特定します。 デフォルト値：`General Contact` |
| [!UICONTROL Gift Card Template] | ストアビュー | ギフトカードの電子メールに使用される[&#x200B; テンプレート &#x200B;](../../systems/email-templates.md)を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![&#x200B; ギフトカードアカウントの一般設定](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

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
