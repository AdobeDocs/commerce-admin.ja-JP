---
title: '[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Commerce管理者の[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel] ページで設定を確認します。
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/hUSNxEvyF010uV6Rp4-osf4azLHtOxtTBSR-XW2m1fA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 610
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Google reCAPTCHAを設定する前に、`PHP.ini` ファイルに次の設定が含まれていることを確認する必要があります：`allow_url_fopen = 1`。 これには開発者のサポートが必要になる場合があります。 _インストールガイド_&#x200B;の[必要なPHP設定](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)を参照してください。

{{config}}

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の[Google reCAPTCHA](../../systems/security-google-recaptcha.md)を参照してください。

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 （&quot;I am not a robot&quot;） ](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Size] | グローバル | ログイン時に表示されるGoogle reCAPTCHA ボックスのサイズ。 オプション：`Normal` （既定値） / `Compact` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Invisible Badge Position] | グローバル | 各ページの非表示のreCAPTCHA バッジの位置。 オプション：`Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Google API Website Key] | グローバル | Google reCAPTCHA アカウントの登録時に作成されるweb サイトキー。 |
| [!UICONTROL Google API Secret Key] | グローバル | Google reCAPTCHA アカウントに関連付けられている秘密鍵。 |
| [!UICONTROL Minimum Score Threshold] | グローバル | ユーザーインタラクションを潜在的なリスクとして特定する最小スコア。1.0は典型的なユーザーインタラクション、0.0はボットである可能性が高い。 既定：`0.5` |
| [!UICONTROL Invisible Badge Position] | グローバル | 各ページの非表示のreCAPTCHA バッジの位置。 オプション：`Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | グローバル | Google reCAPTCHA ボックスのスタイルを指定します。 オプション：`Light Theme` （既定値） / `Dark Theme` |
| [!UICONTROL Language Code] | グローバル | Google reCAPTCHA テキストとメッセージに使用される言語を指定する[2文字コード ](https://developers.google.com/recaptcha/docs/language)。 |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![失敗メッセージ ](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | グローバル | 検証が失敗した場合に管理者に表示されるメッセージ。 既定のテキスト：`reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | グローバル | reCAPTCHAが検証結果を返せない場合に管理者に表示されるメッセージ。 既定のテキスト：`Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![管理者パネル ](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>選択するreCAPTCHA タイプは、Google reCAPTCHA アカウントのAPI キーに関連付けられているタイプと一致している必要があります。

>[!WARNING]
>
>reCAPTCHA バージョン 3を使用する場合、スコアが低い正規版ユーザーは続行できません。 バージョン 2では、スコアが低い本物のユーザーに課題が課されます。 スコアが低い正規のユーザーに対して、課題を解決する機会（バージョン 2）やブロックする機会（バージョン 3）を提供する場合は、慎重に検討します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--|--|--|
| [!UICONTROL Enable for Login] | グローバル | [管理者ログイン ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html)に対して有効になっているreCAPTCHAのタイプを決定します。 オプション：<br/>**`No`**- （デフォルト）管理者ログインが検証されません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCAPTCHA v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |
| [!UICONTROL Enable for Forgot Password] | グローバル | [管理者パスワードのリセット ](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password)をリクエストするために有効になっているreCAPTCHAのタイプを決定します。 オプション：<br/>**`No`**- （デフォルト）パスワード リセット リクエストを検証しません。<br />**`reCAPTCHA v2 ("I am not a robot")`** - ユーザーは&#x200B;_I&#39;m not a robot_ チェックボックスを選択する必要があります。<br />**`Invisible reCAPTCHA v2`**- スコアに基づくインタラクションを必要とせずに、バックグラウンドでユーザーの行動を検証します。<br/>**`Invisible reCaptcha v3`** - （推奨）インタラクションスコアに基づいて、バックグラウンドでのユーザー行動を検証します。 |

{style="table-layout:auto"}
