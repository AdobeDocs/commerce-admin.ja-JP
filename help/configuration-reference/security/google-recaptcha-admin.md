---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: の設定を確認します。 [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] コマース管理者のページ。
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Google reCAPTCHA を設定する前に、 `PHP.ini` ファイルには次の設定が含まれます。 `allow_url_fopen = 1`. これには、開発者の支援が必要になる場合があります。 参照： [必要な PHP 設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) が含まれる _インストールガイド_.

{{config}}

これらの設定の変更の詳細については、を参照してください [Google reCAPTCHA](../../systems/security-google-recaptcha.md) が含まれる _管理システムガイド_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （「I am not a robot」）](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Size] | グローバル | ログイン時に表示されるGoogle reCAPTCHA ボックスのサイズ。 オプション： `Normal` （デフォルト） / `Compact` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | A [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 非表示](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Invisible Badge Position] | グローバル | 各ページの非表示の reCAPTCHA バッジの位置。 オプション： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | A [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成される web サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられた秘密鍵。 |
| [!UICONTROL Minimum Score Threshold] | グローバル | ユーザーインタラクションを潜在的なリスクとして識別する最小スコア。1.0 は一般的なユーザーインタラクションで、0.0 はボットである可能性が高いです。 デフォルト： `0.5` |
| [!UICONTROL Invisible Badge Position] | グローバル | 各ページの非表示の reCAPTCHA バッジの位置。 オプション： `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション： `Light Theme` （デフォルト） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | A [2 文字コード](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA テキストおよびメッセージングに使用する言語を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失敗メッセージ](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | グローバル | 検証に失敗した場合に管理者に表示されるメッセージ。 デフォルトのテキスト： `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | グローバル | reCAPTCHA が検証結果を返さない場合に管理者に表示されるメッセージ。 デフォルトのテキスト： `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![管理パネル](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>選択する reCAPTCHA タイプは、Google reCAPTCHA アカウントの API キーに関連付けられているタイプと一致する必要があります。

>[!WARNING]
>
>reCAPTCHA バージョン 3 を使用している場合、スコアの低い本物のユーザーは続行できません。 バージョン 2 の場合、スコアの低い正規のユーザーがチャレンジを受け取ります。 スコアの低い正規のユーザーに、課題を解決する機会（バージョン 2）があるか、ブロックされる機会（バージョン 3）がある場合は、慎重に検討します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Enable for Login] | グローバル | で有効になっている reCAPTCHA のタイプを決定します [管理者ログイン](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). オプション：<br/>**`No`**- （デフォルト）管理者ログインを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |
| [!UICONTROL Enable for Forgot Password] | グローバル | をリクエストするために有効になっている reCAPTCHA のタイプを決定します。 [管理者のパスワードリセット](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). オプション：<br/>**`No`**- （デフォルト）パスワードリセット要求を検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーに選択を求める _私はロボットではありません_ チェックボックス。<br />**`Invisible reCAPTCHA v2`**- スコアに基づいてインタラクションを必要とせずに、バックグラウンドでのユーザーの行動を検証します。<br/>**`Invisible reCaptcha v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザーの行動を検証します。 |

{style="table-layout:auto"}
