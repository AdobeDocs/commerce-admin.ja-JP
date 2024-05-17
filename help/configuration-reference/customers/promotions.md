---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: の設定を確認します。 [!UICONTROL Customers] &gt; [!UICONTROL Promotions] コマース管理者のページ。
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![自動メールリマインダールール](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | グローバル | 自動メール リマインダーを有効にします。 「いいえ」を選択すると、残りの設定は無視されます。 オプション： `Yes` / `No` |
| [!UICONTROL Frequency] | グローバル | 自動メールリマインダーの対象となる新規のお客様をCommerceが確認する頻度を示します。 オプション： <br/>**`Minute Intervals`**– 選択した間隔でメールを送信します。 （5 分、10 分、15 分、20 分、30 分）<br/>**`Hourly`**  – 毎時、指定した時間の後の分にメールを送信します。 0 ～ 59 の範囲で値を入力してください。 <br/>**`Daily`**– 開始時刻から毎日メールを送信します。 |
| [!UICONTROL Interval] | グローバル | 間隔は、cron.php の起動期間以上にする必要があります。 オプション： `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | グローバル | 電子メールを送信する日、分、および秒を設定します。 サーバーのシステム時刻に基づいて、24 時間形式で指定します。 |
| [!UICONTROL Maximum Emails per One Run] | グローバル | スケジュールされたブロックで送信されるメールの数を制限します。 |
| [!UICONTROL Email Send Failure Threshold] | グローバル | リマインダーが特定のメールアドレスに通知を送信しようとして失敗した回数。 値を 0 に設定すると、しきい値がなくなり、エラーが発生しても通知が引き続き送信されます。 |
| [!UICONTROL Reminder Email Sender] | ストア表示 | メールの送信者として表示されるストア ID。 |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![自動生成された特定のクーポンコード](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | グローバル | 接頭辞、接尾辞および区切り記号を除く、クーポンコードの長さを定義します。 |
| [!UICONTROL Code Format] | グローバル | クーポンコードの形式を定義します。 次のようなオプションがあります。 <br/>**`Alphanumeric`**– 文字と数字の任意の組み合わせ。<br/>**`Alphabetical`**  – 文字のみ。 <br/>**`Numeric`**– 数値のみ。 |
| [!UICONTROL Code Prefix] | グローバル | すべてのクーポンコードの先頭に追加される値。 プレフィックスを使用しない場合は、フィールドを空白のままにします。 |
| [!UICONTROL Code Suffix] | グローバル | すべてのコードの末尾に追加される値。 サフィックスを使用しない場合は、フィールドを空白のままにします。 |
| [!UICONTROL Dash Every X Characters] | グローバル | すべてのクーポン コードにダッシュ （–）を挿入する間隔です。 ダッシュを使用しない場合は、フィールドを空白のままにします。 <br/>_**注意：**_ ダッシュのみが異なるクーポンコードは、異なるコードと見なされます。 |

{style="table-layout:auto"}
