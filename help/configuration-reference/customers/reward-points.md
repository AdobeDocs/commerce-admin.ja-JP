---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] コマース管理のページ。
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 1ae3e1fd10e29de690f7f159c36101a9817dea91
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>[為替レートの報酬](../../merchandising-promotions/reward-exchange-rates.md) チェックアウト時に、顧客および管理者による報酬ポイントの引き換えには、設定が必要です。

## [!UICONTROL Reward Points]

![報酬ポイント](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | グローバル | 報酬ポイントを有効または無効にします。 オプション： `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Web サイト | 有効にすると、顧客はアクティビティを通じてポイントを獲得し、チェックアウト時にポイントを交換できます。 無効にした場合、管理者ユーザーのみが顧客に代わってポイントを割り当て、利用できます。 オプション： `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Web サイト | 有効にすると、顧客は、アカウントダッシュボードで、発生、償還および報酬ポイントの有効期限を示す詳細な履歴を確認できます。 オプション： `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Web サイト | お客様は、ご注文に対して引き換えを行う前に、最低限のポイントバランスを取る必要があります。 最小値を指定しない場合は空白のままにします。 |
| [!UICONTROL Cap Reward Points Balance At] | Web サイト | 顧客がこの最大ポイント残高を超えて計上するのを防ぎます。 最大値を指定しない場合は空白のままにします。 |
| [!UICONTROL Reward Points Expire in (days)] | Web サイト | 報酬ポイントの有効期間を日単位で示します。 別々のアクティビティで獲得したポイントの各バッチには、別々の有効期間があります。 報酬ポイント履歴の各バッチは、ポイントの有効期限が切れるまでの残り日数を示します。 履歴は、お客様のアカウントダッシュボード（有効な場合）および管理者から確認できます。 有効期限を設定しない場合は空白のままにします。 |
| [!UICONTROL Reward Points Expiry Calculation] | Web サイト | 報酬ポイントの有効期限を判断する方法を決定します。 オプション： <br/>**`Static`**— 設定に設定された日数に基づいて、報酬ポイントの残りの有効期間を決定します。 設定の有効期限が変更されても、既存のポイントの有効期限は変更されません。<br/>**`Dynamic`**  — 報酬ポイント残高が増加するたびに残り日数を計算します。 設定の有効期限が変更されると、既存のすべてのポイントの有効期限の計算がそれに応じて更新されます。 |
| [!UICONTROL Refund Reward Points Automatically] | グローバル | 利用可能な報酬ポイントが自動的に払い戻されるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | グローバル | この機能が有効な場合、購入によって獲得した報酬ポイントが注文の返金に対して完全に無効になるか、部分的に無効になるかを決定します。 その注文が払い戻された場合、その注文からの報酬ポイントのみが影響を受けます。 オプション： `Yes` / `No`. |
| [!UICONTROL Landing Page] | ストア表示 | 報酬ポイントプログラムを説明する CMS ページを指定します。 デフォルトの報酬ページへのリンクがストア内のポイントを獲得できる場所に表示されます。 |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![顧客別報酬ポイント獲得の訴え](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Web サイト | 設定された [為替レートの報酬](../../merchandising-promotions/reward-exchange-rates.md). オプション： `Yes` / `No` |
| [!UICONTROL Registration] | Web サイト | 顧客アカウントを開くときに獲得したポイント数を指定します。 |
| [!UICONTROL Newsletter Signup] | Web サイト | ニュースレターを購読した登録ユーザーが獲得したポイント数を指定します。 （ゲストのサブスクリプションではポイントは利用できません。） 顧客が配信停止してから再度配信登録した場合、2 回目の配信登録でポイントが獲得されることはありません。 |
| [!UICONTROL Converting Invitation to Customer] | Web サイト | 受信者が顧客アカウントを開いたときに、招待を送信した顧客が獲得したポイント数を指定します。 |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Web サイト | 招待状を送信する顧客のポイント獲得に使用できる招待状のコンバージョンの数を制限します。 制限なしの場合は空白のままにします。 |
| [!UICONTROL Converting Invitation to Order] | Web サイト | 受信者が最初の注文を行ったときに、招待を送信した顧客が獲得したポイント数を指定します。 |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Web サイト | 招待状の送信者のポイントを獲得できる注文コンバージョンの数を制限します。 空白の場合、最大値はありません。 |
| [!UICONTROL Invitation Conversion to Order Reward] | Web サイト | 招待者が購入した場合に、顧客が報酬ポイントを獲得できる頻度を示します。 オプション： <br/>**`Each`**— 顧客は、招待者が行った請求済み注文ごとに報酬ポイントを受け取ります。 報酬ポイントは、ウェブサイトと顧客グループとの必要な組み合わせに対して設定された為替レートに従って与えられる。<br/>**`First`**  — 顧客は、招待者が最初に請求した注文に対する報酬ポイントのみを受け取ります。 複数の招待者が登録し、注文を行う場合、最初の注文の金額のみが報酬ポイントに変換され、顧客に付与されます。 |
| [!UICONTROL Review Submission] | Web サイト | 公開の承認を得たレビューを送信した顧客が獲得したポイント数を決定します。 |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Web サイト | 顧客ごとのポイント獲得に使用できるレビューの数を制限します。 制限なしの場合は空白のままにします。 |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![電子メール通知設定](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Sender] | ストア表示 | 残高の更新と有効期限の通知 E メールの送信者として表示される店舗連絡先を決定します。 |
| [!UICONTROL Subscribe Customers by Default] | グローバル | 残高更新通知と有効期限通知 E メールの両方について、顧客のデフォルトの購読ステータスを決定します。 |
| [!UICONTROL Balance Update Email] | ストア表示 | 顧客のポイントバランスが更新されるたびに顧客に送信される通知に使用するテンプレートを決定します。 デフォルトのテンプレート： `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | ストア表示 | ポイントのバッチで有効期限の警告制限に達した場合に顧客が受け取る E メールのテンプレートを決定します。 デフォルトのテンプレート： `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | グローバル | 通知を送信するポイントの有効期限までの日数を指定します。 有効期限通知を送信しない場合は空白のままにします。 入力した日数が残りの期間を超える場合、通知は送信されません。 |

{style="table-layout:auto"}
