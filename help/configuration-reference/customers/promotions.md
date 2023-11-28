---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Promotions] コマース管理のページ。
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![自動電子メールリマインダールール](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | グローバル | 電子メールのリマインダーを自動化できます。 [ いいえ ] に設定した場合、残りの設定は無視されます。 オプション： `Yes` / `No` |
| [!UICONTROL Frequency] | グローバル | 自動電子メールリマインダーの条件を満たす新規顧客を Commerce が確認する頻度を示します。 オプション： <br/>**`Minute Intervals`**— 選択した間隔で電子メールを送信します。 （5 分、10 分、15 分、20 分、30 分）<br/>**`Hourly`**  — 指定した時間の後の分に、1 時間ごとに電子メールを送信します。 0 ～ 59 の値を入力します。 <br/>**`Daily`**- Start Time から毎日電子メールを送信します。 |
| [!UICONTROL Interval] | グローバル | 間隔は、cron.php の起動期間と等しいか、それより大きい必要があります。 オプション： `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | グローバル | E メールの送信日、分、秒を設定します。 サーバー上のシステム時刻に基づいて 24 時間形式で指定します。 |
| [!UICONTROL Maximum Emails per One Run] | グローバル | スケジュール済みブロックで送信される E メールの数を制限します。 |
| [!UICONTROL Email Send Failure Threshold] | グローバル | リマインダーが特定の電子メールアドレスに通知を送信しようとして失敗した回数。 値を 0 に設定すると、しきい値はなく、エラーが発生した場合でも通知は引き続き送信されます。 |
| [!UICONTROL Reminder Email Sender] | ストア表示 | E メールの送信者として表示されるストア ID。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![自動生成された特定のクーポンコード](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Code Length] | グローバル | プレフィックス、サフィックス、区切り文字を除く、クーポンコードの長さを定義します。 |
| [!UICONTROL Code Format] | グローバル | クーポンコードの形式を定義します。 オプションは次のとおりです。 <br/>**`Alphanumeric`**— 文字と数字の組み合わせ。<br/>**`Alphabetical`**  — 文字のみ。 <br/>**`Numeric`**— 数字のみ。 |
| [!UICONTROL Code Prefix] | グローバル | すべてのクーポンコードの先頭に追加される値です。 プレフィックスを使用しない場合は、「 」フィールドを空白のままにします。 |
| [!UICONTROL Code Suffix] | グローバル | すべてのコードの末尾に追加される値です。 サフィックスを使用しない場合は、このフィールドを空白のままにします。 |
| [!UICONTROL Dash Every X Characters] | グローバル | すべてのクーポンコードにダッシュ (-) を挿入する間隔。 ダッシュを使用しない場合は、このフィールドを空白のままにします。 <br/>_**注意：**_ ダッシュ以外のクーポンコードは、異なるコードと見なされます。 |

{:style=&quot;table-layout:auto&quot;}
