---
title: 会社クレジットの管理
description: 会社のクレジットライン、パラメーターの設定、およびアカウントでの支払い処理について説明します。
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# 会社クレジットの管理

次の場合 [アカウントでの支払い](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) を設定で有効にすると、会社は、会社に付与されるクレジット制限まで、自社のアカウントで購入を行うことができます。 有効にすると、顧客は自社のクレジットのステータスをアカウントダッシュボードで確認できます。

![会社クレジット](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

各会社プロファイルに対して、次のクレジット関連パラメーターを設定できます。

- クレジット通貨
- クレジット制限
- 与信限度額超過の許可
- 変更の理由

会社に未処理の残高がある場合は、店舗管理者への通知が、管理者から表示される際に、販売注文の一番上に表示されます。 詳しくは、 [会社アカウントの作成](account-company-create.md).

## 会社のクレジット活動

The [!UICONTROL Company Credit] 「 」セクションには、顧客クレジット活動の概要と、会社クレジット履歴のグリッドが表示されます。

![会社クレジットアクティビティ](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Date] | トランザクションの日付。 日付と時刻を表示するには、日付の上にマウスポインターを置きます。 |
| [!UICONTROL Operation] | トランザクションに関連付けられているアクティビティのタイプ。 値： <br/>**[!UICONTROL Allocated]**— 会社に割り当てられたクレジット。<br/>**[!UICONTROL Updated]**  — 次のフィールドの 1 つに変更が適用されました： [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**— 注文がおこなわれました。<br/>**[!UICONTROL Reimbursed]** ・残高は償還済み。 <br/>**[!UICONTROL Refunded]**・クレジット・メモ額は払い戻し済み。<br/>**[!UICONTROL Reverted]**  — 注文が取り消され、クレジット残高に返却された金額。 |
| [!UICONTROL Amount] | 次のトランザクション・タイプに関連付けられたトランザクションの金額。 `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>購入金額の場合、金額は店舗の表示通貨と、クレジット通貨設定の形式で表示され、その後に現在の換算レート（該当する場合）が続きます。 例： <br/>EUR 20,000.00 ($22,400.00) <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 払い戻された金額は、「口座支払」方法を使用して行われたすべての注文からの合計支払額を下回ります。 金額は正または負の値として表示されます。 <br/>**[!UICONTROL Positive value]**— 前払いは正の値で表されます。<br/>**[!UICONTROL Negative value]**  — 支払額は負の値で表されます。 |
| [!UICONTROL Available Credit] | の合計 _[!UICONTROL Credit Limit]_そして_[!UICONTROL Outstanding Balance]_. 会社がクレジット制限を超えた場合は、金額は負の値として表示されます。 |
| [!UICONTROL Credit Limit] | 会社に対して延長されたクレジットの額。 |
| [!UICONTROL Updated By] | 操作を開始した人の名前。 |
| [!UICONTROL Custom Reference Number] | トランザクションに関連付けられているカスタム参照番号。 |
| [!UICONTROL Comment] | 値のコンパイル `Reason for Change` フィールドに値を入力します。 <br/>**[!UICONTROL Purchased]**— 購入からのコメント、注文番号、注文へのリンクが含まれます。<br/>**[!UICONTROL Reimbursed]**  — 償還済みトランザクションからのコメントが含まれます。 |
| [!UICONTROL Action] | の場合 `Reimbursed` 操作のみ。 **[!UICONTROL Edit]**  — 償還金額の更新を許可します。 |

{style="table-layout:auto"}

## クレジット情報の更新

顧客が商人に対して未処理のクレジットの支払いを行う場合、店舗管理者は管理者で顧客クレジット情報を更新する必要があります。

1. 次の日： _管理者_ サイドバー、移動 **顧客/会社**.

1. グリッド内の会社を検索し、で開きます。 _編集_ モード。

1. を展開します。 **会社クレジット** 」セクションに入力します。

1. の場合 **クレジット制限**&#x200B;に値を入力し、新しい値を入力します。

1. 必要に応じて、他の値を変更します。

1. 更新が完了したら、「 **[!UICONTROL Save]**.

## 支払いを受け取る

払い戻し後の残高とは、会社が自社の口座の残高に対して行うオフラインの支払いです。 ストア管理者が、 _償還差額_ 」ボタンをクリックします。 金額が提出されると、未払残高と利用可能な会社クレジットが再計算され、会社与信履歴に処理が記録されます。 払い戻された金額は、構成で指定されたクレジット通貨で入力されます。

### 会社アカウントに支払を適用する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. リスト内の会社レコードを検索し、で開きます。 **[!UICONTROL Edit]** モード。

1. ページ上部で、「 **償還差額**.

1. ダイアログで、支払い情報を追加します。

   ![償還差額](./assets/company-reimburse-balance.png){width="500"}

   - 次を入力します。 **金額** 支払いの。

     金額は正または負の値で入力できます。

   - 該当する場合は、 **カスタム参照番号** 参照用。

     1 回の償還で入力できるカスタム参照番号は 1 つだけです。 複数の発注に支払いを適用するには、各発注に対して個別に償還を行います。

   - 必要に応じて、 **コメント** を参照してください。

1. クリック **償還**.

   会社の残高と利用可能なクレジットが再計算され、会社のクレジット履歴が更新され、償還が反映されます。

### 償還の編集

1. で会社プロファイルを開きます。 **[!UICONTROL Edit]** モード。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **会社クレジット** 」セクションに入力します。

1. グリッド内の償還トランザクションを検索し、 **[!UICONTROL Edit]**.

1. 必要に応じて変更を加えます。 **カスタム参照番号** および **コメント**.

   償還金額は変更できません。

1. クリック **[!UICONTROL Save]**.

## 店頭クレジット情報

会社管理者の場合、アカウントダッシュボードに _会社クレジット_ 」セクションに入力します。 現在の残高、利用可能なクレジット、および会社アカウントに割り当てられたクレジット制限を提供し、その後に未処理の請求書のリストが表示されます。

商人が会社クレジットに請求された注文を取り消すと、注文額が会社残高と _クレジット配分履歴_ には、アクションのレコードが含まれます。

![会社クレジット](./assets/company-credit.png){width="700" zoomable="yes"}

## 会社のクレジットデモ

次のデモビデオを見て、会社のクレジットを管理する方法を学びます。

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
