---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: の設定を確認します。 [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] コマース管理者のページ。
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Google reCAPTCHA を設定する前に、 `PHP.ini` ファイルには次の設定が含まれます。 `allow_url_fopen = 1`. これには、開発者の支援が必要になる場合があります。 参照： [PHP 設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) が含まれる _インストールガイド_.

{{config}}

Google reCAPTCHA を使用してストアを保護する方法について詳しくは、Googleを参照してください [reCAPTCHA](../../systems/security-google-recaptcha.md) が含まれる _管理システムガイド_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （「I am not a robot」）](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Size] | Web サイト | 顧客がアカウントにログインしたときに表示されるGoogle reCAPTCHA ボックスのサイズです。 オプション： `Normal` （デフォルト） / `Compact` |
| [!UICONTROL Theme] | Web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | この [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 非表示](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Invisible Badge Position] | Web サイト | 各ページの非表示の reCAPTCHA バッジの位置。 オプション： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | A [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Minimum Score Threshold] | グローバル | ユーザーインタラクションを潜在的なリスクとして識別する最小スコア。1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性が高いです。 デフォルト： `0.5` |
| [!UICONTROL Invisible Badge Position] | Web サイト | 各ページの非表示の reCAPTCHA バッジの位置。 オプション： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | A [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失敗メッセージ](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | ストア表示 | 検証に失敗した場合にストアフロントに表示されるメッセージ。 デフォルトのテキスト： `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | ストア表示 | reCAPTCHA が検証結果を返さない場合にストアフロントに表示されるメッセージ。 デフォルトのテキスト： `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![ストアフロント](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>選択する reCAPTCHA タイプは、Google reCAPTCHA アカウントの API キーに関連付けられているタイプと一致する必要があります。

>[!WARNING]
>
>reCAPTCHA バージョン 3 を使用している場合、スコアの低い本物のユーザーは続行できません。 バージョン 2 の場合、スコアの低い正規のユーザーがチャレンジを受け取ります。 スコアの低い正規のユーザーに、課題を解決する機会（バージョン 2）があるか、ブロックされる機会（バージョン 3）がある場合は、慎重に検討します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Web サイト | 顧客が使用する reCAPTCHA のタイプを指定します [ログイン](../../customers/customer-sign-in.md) アカウントに追加します。 オプション：<br/>**`No`**- （デフォルト）ログインリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Forgot Password] | Web サイト | 顧客がをリクエストする際に使用される reCAPTCHA のタイプを指定します [パスワードのリセット](../../customers/password-reset.md). オプション：<br/>**`No`**- （デフォルト）パスワードリセット要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Create New Customer Account] | Web サイト | 顧客がに新規登録する際に使用する reCAPTCHA のタイプを指定 [新しいアカウント](../../customers/account-create.md). オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Edit Customer Account] | Web サイト | 顧客がを変更するときに使用する reCAPTCHA のタイプを指定します [アカウント情報](../../customers/account-dashboard-account-information.md). オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Create New Company Account] | Web サイト | ![Adobe Commerce B2B](../../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）新しいの場合に使用する reCAPTCHA のタイプを指定します [会社アカウント](../../b2b/account-company-create.md) が作成されました。 オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Contact Us] | Web サイト | からメッセージを送信するために使用する reCAPTCHA のタイプを指定します [お問い合わせ](../../getting-started/store-details.md#contact-us-form) ストアのページ。 オプション：<br/>**`No`**- （デフォルト）メッセージリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Product Review] | Web サイト | 顧客がを送信する際に使用する reCAPTCHA のタイプを指定します [製品レビュー](../../merchandising-promotions/product-reviews.md). オプション：<br/>**`No`**- （デフォルト）製品レビューリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Newsletter Subscription] | Web サイト | 顧客がに新規登録する際に使用する、非表示の reCAPTCHA のタイプを指定します [ニュースレター購読](../../merchandising-promotions/newsletter-subscribers.md). オプション：<br/>**`No`**- （デフォルト）ニュースレターの購読リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Gift Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）ユーザーがを入力する際に使用する reCAPTCHA のタイプを指定します [ギフトカード](../../catalog/product-gift-card-create.md) コード。 オプション：<br/>**`No`**- （デフォルト）ギフトカードコードの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Invitation Create Account] | Web サイト | 顧客がアカウント作成を送信する際に使用される reCAPTCHA のタイプを指定します [招待](../../merchandising-promotions/invitations.md) コード。 オプション：<br/>**`No`**- （デフォルト）招待メールの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Send to Friend] | Web サイト | 顧客が使用する reCAPTCHA のタイプを指定します [製品の共有](../../stores-purchase/email-a-friend.md) 友達と一緒に。 オプション：<br/>**`No`**- （デフォルト）メール送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Wishlist Sharing] | Web サイト | 顧客が使用する reCAPTCHA のタイプを指定します [ウィッシュリストの共有](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). オプション：<br/>**`No`**- （デフォルト）メッセージとメール送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Coupon Codes] | Web サイト | 顧客がを入力する際に使用する reCAPTCHA のタイプを指定します [クーポンコード](../../merchandising-promotions/price-rules-cart-coupon.md). オプション：<br/>**`No`**- （デフォルト）クーポンコードの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Web サイト | 顧客がで購入に対して支払いを行うときに使用する reCAPTCHA のタイプを指定します [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). オプション：<br/>**`No`**- （デフォルト）パスワードリセット要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |

{style="table-layout:auto"}
