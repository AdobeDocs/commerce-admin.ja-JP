---
title: 報酬およびロイヤルティプログラム
description: 顧客エンゲージメントを促進し、顧客の忠誠度を高めるために使用できる報酬ポイントシステムについて説明します。
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 9d775e8e8521032dc58f6cd1ed7796595db745a0
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# 報酬およびロイヤルティプログラム

{{ee-feature}}

The _報酬ポイント_ Adobe Commerceのシステムを使用すると、顧客エンゲージメントを促進し、顧客の忠誠度を高める独自のプログラムを実装できます。 多様な取引や顧客活動に対してポイントを付与でき、ポイント割り当て、残高、有効期限を制御する設定が可能です。 顧客は、報酬ポイントと通貨の間で設定したコンバージョン率に基づいて、購入に向けたポイントを引き換えることができます。

## 買い物かごの価格ルール

ポイントは、 [買い物かごルール](price-rules-cart.md). 報酬は、価格ルールの唯一のアクションとして、または割引と共に与えることができます。

## 顧客残高

報酬ポイント残高は、管理者ユーザーが顧客ごとに管理できます。 ストアフロントで有効にした場合、顧客はポイントバランスの詳細を表示することもできます。

## リデームポイント

>[!NOTE]
>
>[為替レートの報酬](reward-exchange-rates.md) 設定は、チェックアウト時に、お客様および管理者ユーザーによる報酬ポイントの引き換えに必要です。

ポイントは、チェックアウト時に管理者ユーザーおよび顧客が（有効になっている場合に）引き換えることができます。 「支払い方法」セクションで、有効な支払い方法の上に「報酬ポイントを使用」チェックボックスが表示されます。 利用可能なポイントと金融為替レートが含まれます。 使用可能な残高が注文の総計より大きい場合、追加の支払い方法は必要ありません。 注文に適用される報酬ポイントの数は、店舗のクレジットカードやギフトカードと同様に、注文の合計と共に表示され、総計から減算されます。 店舗クレジットやギフトカードと共に報酬ポイントを使用する場合は、まず報酬ポイントを差し引きます。 その後、注文の合計が償還可能な報酬ポイント数を超える場合は、店舗クレジットまたはギフトカードが差し引かれます。

>[!NOTE]
>
>注文が請求されるまで支払いの受領を確認できないため、報酬ポイントは、COD 購入での使用には推奨されません。

## 報酬ポイントへの返金

報酬ポイントが付された注文は、その注文で償還された金額まで、報酬ポイントに対して払い戻しが可能です。 次の日： [_新規クレジットメモ_ ページ](../stores-purchase/credit-memo-create.md)の場合は、顧客の残高に適用するポイント数を入力できます。 デフォルトでは、このフィールドには、順序で使用された完全なポイント数が含まれます。

## ストアの報酬ポイント操作を有効にする

報酬ポイント設定は、店舗での報酬ポイントの表示方法を決定し、基本的な操作パラメータを定義します。

![顧客設定 — 報酬ポイント](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### 手順 1. 報酬ポイントの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Reward Points]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Reward Points]** 」セクションで次の操作を実行します。

   - 報酬ポイントを有効にするには、 **[!UICONTROL Enable Reward Points Functionality]** から `Yes`.

   - 顧客が自分の報酬ポイントを獲得できるようにするには、 **[!UICONTROL Enable Reward Points Functionality on Storefront]** から `Yes`.

   - 顧客が報酬の詳細な履歴を表示できるようにするには、 **[!UICONTROL Customers May See Reward Point History]** から `Yes`.

1. の場合 **[!UICONTROL Reward Points Balance Redemption Threshold]**&#x200B;をクリックし、引き換え前に引き継ぐ必要があるポイントの数を入力します（最小値を指定しない場合は空白）。

1. の場合 **[!UICONTROL Cap Reward Points Balance At]**、顧客が発生する最大ポイント数を入力します（制限なしの場合は空白）。

1. の場合 **[!UICONTROL Reward Points Expire in (days)]**、報酬ポイントの有効期限が切れるまでの日数を入力します（有効期限がない場合は空白）。

1. 設定 **[!UICONTROL Reward Points Expiry Calculation]** を次のいずれかに変更します。

   - `Static`  — 設定に設定された日数に基づいて、報酬ポイントの残りの有効期間を決定します。 設定の有効期限が変更されても、既存のポイントの有効期限は変更されません。

   - `Dynamic`  — 報酬ポイント残高が増加するたびに残りの日数を計算します。 設定の有効期限が変更されると、既存のポイントの有効期限もそれに応じて更新されます。

1. 利用可能な報酬ポイントを自動的に払い戻す場合は、 **[!UICONTROL Refund Reward Points Automatically]** から `Yes`.

1. ポイントを獲得した注文が完全に返金された場合、または一部返金された場合に、購入によって獲得した報酬ポイントを無効にするには、 **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** から `Yes`.

   >[!NOTE]
   >
   >払い戻される注文で獲得したポイントのみが影響を受けます。

1. 設定 **[!UICONTROL Landing Page]** 報酬ポイントプログラムを説明するコンテンツページに移動します。

   デフォルトの報酬ポイントページを、必ず独自の情報で更新してください。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 手順 2. 顧客アクティビティが獲得したポイントの設定

このステップでは、各種顧客活動に対して獲得可能な報酬ポイント数を指定する。 顧客がポイントが割り当てられたアクションを完了すると、獲得したポイント数を示すメッセージが顧客に表示されます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Actions for Acquiring Reward Points by Customer]** 」セクションに入力します。

   ![顧客設定 — 顧客別の報酬ポイントを獲得するアクション](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. 買い物かごに、購入に対して獲得した報酬ポイントと顧客の現在の報酬ポイント残高を含むメッセージを表示するには、 **[!UICONTROL Purchase]** から `Yes`.

   >[!NOTE]
   >
   >報酬を得るには _first_ 注文の場合、顧客を登録する必要があります _前_ トランザクションは支払い方法でキャプチャされます。 ほとんどの支払い方法は、トランザクションをキャプチャするように設定できます _自動的に_ 注文が行われた時に _前_ 顧客アカウントの登録が完了しました。

1. の場合 **[!UICONTROL Registration]**、顧客アカウントを開いたときに獲得したポイント数を入力します。

1. の場合 **[!UICONTROL Newsletter Signup]**、ニュースレターを購読した登録ユーザーが獲得したポイント数を入力します。

1. の場合 **[!UICONTROL Converting Invitation to Customer]**「 」で、招待状を送信した顧客が獲得したポイント数を入力し、受信者が顧客アカウントを開きます。

   招待状を送信する顧客のポイント獲得に使用できる招待状のコンバージョンの数を制限できます（制限なしの場合は空白）。 これをおこなうには、「 **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** フィールドに入力します。

1. の場合 **[!UICONTROL Converting Invitation to Order]**&#x200B;をクリックし、受信者に招待を送信し、その受信者が受け取ったポイント数を入力します。その後、注文をおこない、次の操作を実行します。

   - の場合 **受注換算数量制限への招待**、受信者が最初の注文をしたときに顧客が招待を送信した際に獲得したポイント数を入力します（制限なしの場合は空白）。

   - の場合 **[!UICONTROL Invitation Conversion to Order Reward]**&#x200B;を選択し、 `Each` 受信者の注文ごとにポイントを獲得するオプション、または `First` オプションを使用して、受信者による最初の注文に対してのみポイントを獲得できます。

1. の場合 **[!UICONTROL Review Submission]**「 」には、公開の承認を得たレビューを送信した顧客が獲得したポイント数を入力します。

1. 次に、顧客ごとのポイント獲得に使用できるレビューの数を制限するには、 **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** フィールド（制限なしの場合は空白）。

1. 完了したら、「 **[!UICONTROL Save Config]**.

### 手順 3. 電子メール通知設定を完了します

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Email Notification Settings]** 」セクションに入力します。

   ![顧客の設定 — ポイントの電子メール通知を報奨](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Email Sender]** 残高の更新と有効期限の通知の送信者として表示される店舗連絡先。

1. デフォルトで顧客を購読して残高更新と今後の有効期限を通知する場合は、 **[!UICONTROL Subscribe Customers by Default]** から `Yes`.

1. 設定 **[!UICONTROL Balance Update Email]** を、顧客のポイント残高が更新されるたびに顧客に送信される通知に使用するテンプレートに設定します。

1. 設定 **[!UICONTROL Reward Points Expiry Warning Email]** を、一連のポイントの有効期限に達したときに顧客に送信される通知に使用するテンプレートに設定します。

1. の場合 **[!UICONTROL Expiry Warning Before (days)]**」に、通知を送信するポイントの有効期限が切れるまでの日数を入力します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 報酬ポイントの残高を更新

報酬ポイント残高は、管理者から更新できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッド内の顧客を検索し、 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. の下 _顧客情報_、選択 **[!UICONTROL Reward Points]** 」セクションに入力します。

1. 次の数を入力： **[!UICONTROL Update Points]**:

   - 報酬ポイントの金額を更新するには、ポイントの総残高を増やす数を入力します。
   - 報酬ポイントの金額を減算するには、ポイントの合計残高を減らす負の数を入力します。

1. 入力 **[!UICONTROL Comments]** 必要に応じて、報酬ポイントの調整に関連します。

   ![報酬ポイント残高](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. （オプション）顧客を購読登録 _報奨ポイントの通知_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. クリック **[!UICONTROL Save Customer]**.

報酬ポイントに関連するすべてのアクションが、顧客の _[!UICONTROL Reward Points History]_店頭のアカウントにブロックします。

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Balance] | クライアントの報酬ポイントの現在の残高 |
| [!UICONTROL Amount Balance] | 現在の現金残高の金額 |
| [!UICONTROL Points] | 加算または減算されたポイントの数 |
| [!UICONTROL Amount] | 加算または減算された金額 |
| [!UICONTROL Rate] | The [報酬交換率](reward-exchange-rates.md) |
| [!UICONTROL Website] | 報酬ポイント履歴を割り当てるウェブサイト |
| [!UICONTROL Reason] | ポイントを授与する理由：<br>**[!UICONTROL Making purchases]**— お客様が購入するたびに、ポイントを獲得できます。<br>**[!UICONTROL Registering on the site]**  — 登録時（1 回）に発生。<br>**[!UICONTROL Subscribing to a newsletter]**— 初回サブスクリプション（1 回）に対して積み立てられます。<br>**[!UICONTROL Sending Invitations]**  — 友人を招待してサイトに参加し、ポイントを獲得します。<br>**[!UICONTROL Converting Invitations to Customer]**— 送信する招待のポイントを獲得し、サイトに登録する主要な友人。<br>**[!UICONTROL Converting Invitations to Order]**  — 招待状の送信によって、各セールのポイントを獲得できます。<br>**[!UICONTROL Review Submission]**— 製品レビューを送信するポイントを獲得します。 |
| [!UICONTROL Created] | 報酬ポイントの更新日時 |
| [!UICONTROL Expired] | 期限切れの報酬ポイント数 |
| [!UICONTROL Comment] | ポイントを追加または差し引く際のコメント |

{style="table-layout:auto"}

## リソースのトラブルシューティング

報酬ポイントの問題のトラブルシューティングについては、次の Commerce Support Knowledge Base 記事を参照してください。

- [部分的な注文のロイヤルティポイント](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404 エラー — マルチシッピングチェックアウトで報酬ポイントを削除](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
