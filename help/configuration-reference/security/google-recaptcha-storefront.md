---
title: '[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]'
description: Commerce管理者の[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront] ページで設定を確認します。
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/Hl5Ivzg-z8tu96TaZN45UFCMMJ4g05fU5t-Jwok1jZE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1480
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Google reCAPTCHAを設定する前に、`PHP.ini` ファイルに次の設定が含まれていることを確認する必要があります：`allow_url_fopen = 1`。 これには開発者のサポートが必要になる場合があります。 _インストールガイド_&#x200B;の[PHP設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)を参照してください。

{{config}}

Google reCAPTCHAを使用してストアを保護する方法について詳しくは、_管理者システムガイド_&#x200B;のGoogle [reCAPTCHA](../../systems/security-google-recaptcha.md)を参照してください。

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （&quot;I am not a robot&quot;） ](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | web サイト | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | web サイト | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Size] | web サイト | お客様がアカウントにログインしたときに表示されるGoogle reCAPTCHA ボックスのサイズ。 オプション：`Normal` （既定値） / `Compact` |
| [!UICONTROL Theme] | web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | ストアビュー | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | web サイト | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | web サイト | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Invisible Badge Position] | web サイト | 各ページの非表示のreCAPTCHA バッジの位置。 オプション：`Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | ストアビュー | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | web サイト | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | web サイト | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Minimum Score Threshold] | グローバル | ユーザーインタラクションを潜在的なリスクとして特定する最小スコア。1.0は典型的なユーザーインタラクション、0.0はボットである可能性が高い。 既定：`0.5` |
| [!UICONTROL Invisible Badge Position] | web サイト | 各ページの非表示のreCAPTCHA バッジの位置。 オプション：`Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | ストアビュー | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE SaaSのみ]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクト（Adobeで管理されるSaaS インフラストラクチャ）にのみ適用されます。"}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Site Key] | web サイト | Google reCAPTCHA Enterprise アカウントの登録時に作成されるサイトキー。 |
| [!UICONTROL Google Cloud Project ID] | web サイト | プロジェクト IDは、プロジェクトのダッシュボードの&#x200B;**プロジェクト情報** セクションに表示されます。 |
| [!UICONTROL Service Account JSON] | web サイト | Google Cloud コンソールからサービスアカウントキーをダウンロードし、その内容をこのフィールドに貼り付けます。 |
| [!UICONTROL Minimum Score Threshold] | web サイト | ユーザーインタラクションを潜在的なリスクとして特定する最小スコア。1.0は典型的なユーザーインタラクション、0.0はボットである可能性が高い。 既定：`0.5` |
| [!UICONTROL Badge Position] | web サイト | 各ページの非表示のreCAPTCHA バッジの位置。 オプション：`Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | ストアビュー | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 ユーザーのブラウザーのデフォルト言語を使用するには、フィールドを空白のままにします。 |
| [!UICONTROL Validation Failure Message] | ストアビュー | 検証が失敗したときに表示されるメッセージ。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失敗メッセージ ](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | ストアビュー | 検証が失敗した場合にストアフロントに表示されるメッセージ。 既定のテキスト：`reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | ストアビュー | reCAPTCHAが検証結果を返せない場合にストアフロントに表示されるメッセージ。 既定のテキスト：`Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![ ストアフロント ](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>選択するreCAPTCHA タイプは、Google reCAPTCHA アカウントのAPI キーに関連付けられているタイプと一致している必要があります。

>[!WARNING]
>
>reCAPTCHA バージョン 3を使用する場合、スコアが低い正規版ユーザーは続行できません。 バージョン 2では、スコアが低い本物のユーザーに課題が課されます。 スコアが低い正規のユーザーに対して、課題を解決する機会（バージョン 2）やブロックする機会（バージョン 3）を提供する場合は、慎重に検討します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | web サイト | 顧客[がアカウントにサインイン ](../../customers/customer-sign-in.md)したときに使用されるreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）ログイン要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Forgot Password] | web サイト | 顧客が[ パスワードリセット ](../../customers/password-reset.md)をリクエストするときに使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）パスワード リセット リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Create New Customer Account] | web サイト | お客様が[新しいアカウント ](../../customers/account-create.md)にサインアップするときに使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）アカウント要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Edit Customer Account] | web サイト | 顧客が[ アカウント情報](../../customers/account-dashboard-account-information.md)を変更する際に使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）アカウント要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Create New Company Account] | web サイト | ![Adobe Commerce B2B](../../assets/b2b.svg) （Adobe Commerce B2Bでのみ使用可能）新しい[会社アカウント ](../../b2b/account-company-create.md)を作成するときに使用するreCAPTCHAの種類を指定します。 オプション：<br/>**`No`**- （デフォルト）アカウント要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Contact Us] | web サイト | ストアの[お問い合わせ](../../getting-started/store-details.md#contact-us-form) ページからメッセージを送信するために使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）メッセージリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Product Review] | web サイト | 顧客が[製品レビュー](../../merchandising-promotions/product-reviews.md)を送信するときに使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）製品レビューリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Newsletter Subscription] | web サイト | 顧客が[ ニュースレターのサブスクリプションにサインアップする際に使用される非表示のreCAPTCHAのタイプを指定します](../../merchandising-promotions/newsletter-subscribers.md)。 オプション：<br/>**`No`**- （デフォルト）ニュースレター購読リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Gift Card] | web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）お客様が[ ギフトカード ](../../catalog/product-gift-card-create.md) コードを入力したときに使用されるreCAPTCHAの種類を指定します。 オプション：<br/>**`No`**- （デフォルト）ギフトカードコードの送信が検証されません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでのユーザー行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Invitation Create Account] | web サイト | 顧客がアカウント作成[招待状](../../merchandising-promotions/invitations.md) コードを送信するときに使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）招待メール送信が検証されません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでのユーザー行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Send to Friend] | web サイト | 顧客[が製品](../../stores-purchase/email-a-friend.md)を友人と共有する際に使用するreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）電子メール送信が検証されません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Wishlist Sharing] | web サイト | 顧客[がウィッシュリスト ](../../stores-purchase/wishlist-storefront.md#share-the-wish-list)を共有する際に使用されるreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）メッセージとメール送信が検証されません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでのユーザー行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Coupon Codes] | web サイト | 顧客が[ クーポンコード ](../../merchandising-promotions/price-rules-cart-coupon.md)を入力したときに使用されるreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （既定値）クーポンコードの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでのユーザー行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | web サイト | 顧客が[PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md)で購入した場合に使用されるreCAPTCHAのタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）パスワード リセット リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |

{style="table-layout:auto"}
