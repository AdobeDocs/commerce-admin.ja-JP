---
title: 会社クレジットの管理
description: 会社の与信明細行、パラメーターの設定、およびアカウントでの支払い処理について説明します。
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 会社クレジットの管理

設定で [ アカウントでの支払い ](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) が有効になっている場合、企業は、会社に付与された与信限度額を上限としてアカウントで購入を行うことができます。 有効にすると、顧客はアカウントダッシュボードから会社クレジットのステータスを確認できます。

![ 企業信用 ](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

各会社プロファイルに対して、次のクレジット関連パラメーターを設定できます。

- クレジット通貨
- 与信限度額
- 与信限度額を超えることを許可
- 変更の理由

会社の残高がある場合、管理者から表示すると、販売注文の上部に店舗管理者への通知が表示されます。 詳しくは、[ 会社アカウントの作成 ](account-company-create.md) を参照してください。

## 会社の信用活動

会社プロファイルの「[!UICONTROL Company Credit]」セクションには、顧客クレジット活動の概要が、会社クレジット履歴のグリッドと共に表示されます。

![ 企業信用活動 ](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Date] | トランザクションの日付。 日付と時刻を表示するには、日付の上にポインタを合わせます。 |
| [!UICONTROL Operation] | トランザクションに関連付けられている活動のタイプ。 値：<br/>**[!UICONTROL Allocated]**– 会社に割り当てられたクレジット。<br/>**[!UICONTROL Updated]** – 次のいずれかのフィールドに変更が適用されました：[!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**– 注文が行われました。<br/>**[!UICONTROL Reimbursed]** – 未払残高が返済されました。 <br/>**[!UICONTROL Refunded]**- クレジット・メモ金額が払戻された場合。<br/>**[!UICONTROL Reverted]** – 注文がキャンセルされ、クレジット残高に返された金額。 |
| [!UICONTROL Amount] | 次の取引タイプに関連付けられている取引の金額：`Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/> 購買金額の場合、金額は店舗の表示通貨およびクレジット通貨設定の形式で表示され、その後に現在の換算レート（該当する場合）が続きます。 例：<br/>EUR 20,000.00 （$22,400.00） <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 払い戻された金額から、分割払い方法を使用して行われたすべての注文の合計金額を差し引いた金額。 金額は、正または負の値として表示される場合があります。 <br/>**[!UICONTROL Positive value]**– 前払いは正の値で表されます。<br/>**[!UICONTROL Negative value]** – 未払額は負の値で表されます。 |
| [!UICONTROL Available Credit] | _[!UICONTROL Credit Limit]_と_[!UICONTROL Outstanding Balance]_ の合計。 会社が与信限度額を超えた場合、金額は負の値として表示されます。 |
| [!UICONTROL Credit Limit] | 会社に対して延長されるクレジットの金額。 |
| [!UICONTROL Updated By] | 操作を開始したユーザーの名前。 |
| [!UICONTROL Custom Reference Number] | トランザクションに関連付けられているカスタム参照番号。 |
| [!UICONTROL Comment] | 操作タイプに従った `Reason for Change` フィールドからの値のコンパイル。 <br/>**[!UICONTROL Purchased]**– 購入からのコメント、注文番号、注文へのリンクが含まれます。<br/>**[!UICONTROL Reimbursed]** – 払い戻されたトランザクションからのコメントが含まれます。 |
| [!UICONTROL Action] | `Reimbursed` 操作のみ。 **[!UICONTROL Edit]** – 償還金額を更新できます。 |

{style="table-layout:auto"}

## クレジット情報の更新

顧客がマーチャントに未処理のクレジットを支払う場合、店舗管理者は管理者で顧客クレジット情報を更新する必要があります。

1. _管理者_ サイドバーで、**顧客/会社** に移動します。

1. グリッドで会社を見つけ、_編集_ モードで開きます。

1. 「**会社クレジット**」セクションを展開します。

1. 「**与信限度額**」に新しい値を入力します。

1. 必要に応じて、他の値を変更します。

1. 更新が完了したら、[**[!UICONTROL Save]**] をクリックします。

## 支払いの受信

払い戻し残高は、会社が口座の残高に対して行うオフライン支払いです。 店舗管理者は、「残高の払い戻し _ボタンを使用して、会社プロファイルに手動で金額を入力し_ す。 金額が発行されると、未処理残高と使用可能な会社クレジットが再計算され、その処理が会社クレジット履歴に記録されます。 設定で指定されているように、返済金額はクレジット通貨で入力されます。

### 会社アカウントへの支払いの適用

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. リストで会社レコードを見つけ、**[!UICONTROL Edit]** モードで開きます。

1. ページの上部で、「残高の返済 **をクリックし** す。

1. ダイアログで、支払い情報を追加します。

   ![ 差引残高 ](./assets/company-reimburse-balance.png){width="500"}

   - 支払の **金額** を入力します。

     金額は正または負の値として入力できます。

   - 該当する場合は、参照用に **カスタム参照番号** を入力します。

     払い戻しごとに入力できるカスタム参照番号は 1 つだけです。 複数の発注に支払を適用するには、それぞれの発注に対して個別の返済を作成します。

   - 必要に応じて、償還を説明する **コメント** を入力します。

1. **払い戻し** をクリックします。

   会社の残高と利用可能なクレジットは再計算され、会社のクレジット履歴は払い戻しを反映するように更新されます。

### 償還の編集

1. **[!UICONTROL Edit]** モードで会社プロファイルを開きます。

1. ![ 拡張セレクター ](../assets/icon-display-expand.png) 「**会社クレジット**」セクションを展開します。

1. グリッドで償還トランザクションを検索し、「**[!UICONTROL Edit]**」をクリックします。

1. **カスタム参照番号** および **コメント** に必要な変更を加えます。

   払い戻し金額は変更できません。

1. 「**[!UICONTROL Save]**」をクリックします。

## ストアフロントのクレジット情報

会社の管理者の場合、アカウントダッシュボードに _会社クレジット_ セクションが表示されます。 現在の未処理残高、使用可能なクレジット、会社アカウントに割り当てられたクレジット制限に続いて、未処理請求書のリストが提供されます。

マーチャントが会社クレジットに請求された注文をキャンセルした場合、注文金額が会社の残高に返され、_クレジット配分履歴_ にはアクションの記録が含まれます。

![ 企業信用 ](./assets/company-credit.png){width="700" zoomable="yes"}

## 会社クレジットデモ

このデモビデオで会社のクレジットの管理について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
