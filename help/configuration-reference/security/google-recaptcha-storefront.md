---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Commerce Admin の [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] ページで設定を確認します。
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '1444'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Google reCAPTCHA を設定する前に、`PHP.ini` ファイルに次の設定が含まれていることを確認する必要があります：`allow_url_fopen = 1`。 これには、開発者の支援が必要になる場合があります。 『インストールガイド [&#x200B; の &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=ja)PHP 設定 _を参照してくだ_ い。

{{config}}

Google reCAPTCHA を使用してストアを保護する方法について詳しくは、『 [&#x200B; 管理システムガイド &#x200B;](../../systems/security-google-recaptcha.md) 』のGoogle _reCAPTCHA_ を参照してください。

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （&quot;I am not a robot&quot;） &#x200B;](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Size] | Web サイト | 顧客がアカウントにログインしたときに表示されるGoogle reCAPTCHA ボックスのサイズです。 オプション：`Normal` （デフォルト）/`Compact` |
| [!UICONTROL Theme] | Web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （デフォルト）/`Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定する [2 文字のコード &#x200B;](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 非表示 &#x200B;](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Invisible Badge Position] | Web サイト | 各ページの非表示の reCAPTCHA バッジの位置。 オプション：`Inline`/`Bottom Right`/`Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （デフォルト）/`Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定する [2 文字のコード &#x200B;](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 非表示 &#x200B;](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | Web サイト | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | Web サイト | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Minimum Score Threshold] | グローバル | ユーザーインタラクションを潜在的なリスクとして識別する最小スコア。1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性が高いです。 デフォルト：`0.5` |
| [!UICONTROL Invisible Badge Position] | Web サイト | 各ページの非表示の reCAPTCHA バッジの位置。 オプション：`Inline`/`Bottom Right`/`Bottom Left` |
| [!UICONTROL Theme] | Web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （デフォルト）/`Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定する [2 文字のコード &#x200B;](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE SaaS のみ &#x200B;]{type=Positive url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service プロジェクトにのみ適用されます（Adobeで管理される SaaS インフラストラクチャ）。"}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Site Key] | Web サイト | Google reCAPTCHA Enterprise アカウントの登録時に作成されるサイトキー。 |
| [!UICONTROL Google Cloud Project ID] | Web サイト | プロジェクト ID は、プロジェクトのダッシュボードの「**プロジェクト情報**」セクションに表示されます。 |
| [!UICONTROL Service Account JSON] | Web サイト | Google Cloud Console からサービスアカウントキーをダウンロードし、その内容をこのフィールドに貼り付けます。 |
| [!UICONTROL Minimum Score Threshold] | Web サイト | ユーザーインタラクションを潜在的なリスクとして識別する最小スコア。1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性が高いです。 デフォルト：`0.5` |
| [!UICONTROL Badge Position] | Web サイト | 各ページの非表示の reCAPTCHA バッジの位置。 オプション：`Inline`/`Bottom Right`/`Bottom Left` |
| [!UICONTROL Theme] | Web サイト | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （デフォルト）/`Dark Theme` |
| [!UICONTROL Language Code] | ストア表示 | Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定する [2 文字のコード &#x200B;](https://developers.google.com/recaptcha/docs/language)。 ユーザーのブラウザーのデフォルト言語を使用する場合は、フィールドを空白のままにします。 |
| [!UICONTROL Validation Failure Message] | ストア表示 | 検証が失敗した場合に表示するメッセージ。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![&#x200B; 失敗メッセージ &#x200B;](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | ストア表示 | 検証に失敗した場合にストアフロントに表示されるメッセージ。 既定のテキスト：`reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | ストア表示 | reCAPTCHA が検証結果を返さない場合にストアフロントに表示されるメッセージ。 既定のテキスト：`Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![&#x200B; ストアフロント &#x200B;](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>選択する reCAPTCHA タイプは、Google reCAPTCHA アカウントの API キーに関連付けられているタイプと一致する必要があります。

>[!WARNING]
>
>reCAPTCHA バージョン 3 を使用している場合、スコアの低い本物のユーザーは続行できません。 バージョン 2 の場合、スコアの低い正規のユーザーがチャレンジを受け取ります。 スコアの低い正規のユーザーに、課題を解決する機会（バージョン 2）があるか、ブロックされる機会（バージョン 3）がある場合は、慎重に検討します。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Web サイト | 顧客がアカウントに [&#x200B; ログイン &#x200B;](../../customers/customer-sign-in.md) したときに使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）ログインリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Forgot Password] | Web サイト | 顧客が [&#x200B; パスワードのリセット &#x200B;](../../customers/password-reset.md) を要求したときに使用される reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）パスワードリセットリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Create New Customer Account] | Web サイト | 顧客が [&#x200B; 新規アカウント &#x200B;](../../customers/account-create.md) に新規登録する際に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Edit Customer Account] | Web サイト | 顧客が [&#x200B; アカウント情報 &#x200B;](../../customers/account-dashboard-account-information.md) を変更したときに使用される reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Create New Company Account] | Web サイト | ![Adobe Commerce B2B](../../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）新しい [&#x200B; 会社アカウント &#x200B;](../../b2b/account-company-create.md) の作成時に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）アカウントのリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Contact Us] | Web サイト | ストアの [&#x200B; お問い合わせ &#x200B;](../../getting-started/store-details.md#contact-us-form) ページからメッセージを送信するために使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）メッセージリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Product Review] | Web サイト | 顧客が [&#x200B; 製品レビュー &#x200B;](../../merchandising-promotions/product-reviews.md) を送信する際に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）製品レビューリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Newsletter Subscription] | Web サイト | 顧客が [&#x200B; ニュースレター購読 &#x200B;](../../merchandising-promotions/newsletter-subscribers.md) に新規登録する際に使用する、非表示の reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）ニュースレターの購読リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Gift Card] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）お客様が [&#x200B; ギフトカード &#x200B;](../../catalog/product-gift-card-create.md) コードを入力したときに使用される reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）ギフトカードコードの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Invitation Create Account] | Web サイト | 顧客がアカウント作成 [&#x200B; 招待 &#x200B;](../../merchandising-promotions/invitations.md) コードを送信する際に使用される reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）招待メールの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Send to Friend] | Web サイト | 顧客が友人と [&#x200B; 製品を共有 &#x200B;](../../stores-purchase/email-a-friend.md) する際に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）メール送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Wishlist Sharing] | Web サイト | 顧客が [&#x200B; ウィッシュリストを共有 &#x200B;](../../stores-purchase/wishlist-storefront.md#share-the-wish-list) する際に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）メッセージとメールの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Coupon Codes] | Web サイト | 顧客が [&#x200B; クーポンコード &#x200B;](../../merchandising-promotions/price-rules-cart-coupon.md) を入力したときに使用される reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）クーポンコードの送信を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいたインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Web サイト | 顧客が [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md) で購入の支払いを行う際に使用する reCAPTCHA のタイプを指定します。 オプション：<br/>**`No`**- （デフォルト）パスワードリセットリクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - 「自分はロボットではない _チェックボックスをユーザーが選択する必要が_ ります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |

{style="table-layout:auto"}
