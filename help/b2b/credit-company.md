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

次の場合 [分割払い](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) が設定で有効になっている場合、会社は、会社に付与された与信限度額を上限として自分のアカウントで購入を行うことができます。 有効にすると、顧客はアカウントダッシュボードから会社クレジットのステータスを確認できます。

![会社クレジット](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

各会社プロファイルに対して、次のクレジット関連パラメーターを設定できます。

- クレジット通貨
- 与信限度額
- 与信限度額を超えることを許可
- 変更の理由

会社の残高がある場合、管理者から表示すると、販売注文の上部に店舗管理者への通知が表示されます。 詳しくは、 [会社アカウントの作成](account-company-create.md).

## 会社の信用活動

この [!UICONTROL Company Credit] 会社プロファイルの「」セクションには、顧客信用活動の概要が、会社の信用履歴のグリッドと共に表示されます。

![会社クレジット アクティビティ](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Date] | トランザクションの日付。 日付と時刻を表示するには、日付の上にポインタを合わせます。 |
| [!UICONTROL Operation] | トランザクションに関連付けられている活動のタイプ。 値： <br/>**[!UICONTROL Allocated]**– 会社に割り当てられているクレジット。<br/>**[!UICONTROL Updated]**  – 次のいずれかのフィールドに変更が適用されました： [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**– 注文が行われました。<br/>**[!UICONTROL Reimbursed]** ・未払分を払い戻した。 <br/>**[!UICONTROL Refunded]**- クレジット・メモの金額は払い戻されました。<br/>**[!UICONTROL Reverted]**  – 注文がキャンセルされ、クレジット残高に返された金額。 |
| [!UICONTROL Amount] | 次の取引タイプに関連付けられている取引金額。 `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>購入金額の場合、金額はストアの表示通貨とクレジット通貨設定の形式で表示され、その後に現在のコンバージョンレート（該当する場合）が表示されます。 例： <br/>20,000.00 ユーロ（22,400.00 ドル） <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 払い戻された金額から、分割払い方法を使用して行われたすべての注文の合計金額を差し引いた金額。 金額は、正または負の値として表示される場合があります。 <br/>**[!UICONTROL Positive value]**– 前払いは正の値で表されます。<br/>**[!UICONTROL Negative value]**  – 未払額は負の値で表されます。 |
| [!UICONTROL Available Credit] | の合計 _[!UICONTROL Credit Limit]_および_[!UICONTROL Outstanding Balance]_. 会社が与信限度額を超えた場合、金額は負の値として表示されます。 |
| [!UICONTROL Credit Limit] | 会社に対して延長されるクレジットの金額。 |
| [!UICONTROL Updated By] | 操作を開始したユーザーの名前。 |
| [!UICONTROL Custom Reference Number] | トランザクションに関連付けられているカスタム参照番号。 |
| [!UICONTROL Comment] | からの値のコンパイル `Reason for Change` 操作タイプに応じたフィールド。 <br/>**[!UICONTROL Purchased]**– 購入からのコメント、注文番号、注文へのリンクが含まれます。<br/>**[!UICONTROL Reimbursed]**  – 返済済トランザクションからのコメントが含まれます。 |
| [!UICONTROL Action] | の場合 `Reimbursed` 操作のみ。 **[!UICONTROL Edit]**  – 償還金額を更新できます。 |

{style="table-layout:auto"}

## クレジット情報の更新

顧客がマーチャントに未処理のクレジットを支払う場合、店舗管理者は管理者で顧客クレジット情報を更新する必要があります。

1. 日 _Admin_ サイドバー、に移動 **顧客/会社**.

1. グリッドで会社を見つけて、で開く _編集_ モード。

1. を展開します。 **会社クレジット** セクション。

1. の場合 **与信限度額**、新しい値を入力します。

1. 必要に応じて、他の値を変更します。

1. 更新が完了したら、 **[!UICONTROL Save]**.

## 支払いの受信

払い戻し残高は、会社が口座の残高に対して行うオフライン支払いです。 ストア管理者は、を使用して、会社プロファイルに手動で金額を入力します _払戻残高_ ボタン。 金額が発行されると、未処理残高と使用可能な会社クレジットが再計算され、その処理が会社クレジット履歴に記録されます。 設定で指定されているように、返済金額はクレジット通貨で入力されます。

### 会社アカウントへの支払いの適用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. リストで会社レコードを検索し、で開きます **[!UICONTROL Edit]** モード。

1. ページの上部で、 **払戻残高**.

1. ダイアログで、支払い情報を追加します。

   ![払戻残高](./assets/company-reimburse-balance.png){width="500"}

   - を入力 **量** 支払いの。

     金額は正または負の値として入力できます。

   - 該当する場合、 **カスタム参照番号** を参照してください。

     払い戻しごとに入力できるカスタム参照番号は 1 つだけです。 複数の発注に支払を適用するには、それぞれの発注に対して個別の返済を作成します。

   - 必要に応じて、を入力します **コメント** 払い戻しの説明。

1. クリック **返済**.

   会社の残高と利用可能なクレジットは再計算され、会社のクレジット履歴は払い戻しを反映するように更新されます。

### 償還の編集

1. で会社プロファイルを開きます。 **[!UICONTROL Edit]** モード。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **会社クレジット** セクション。

1. グリッドで償還トランザクションを検索し、 **[!UICONTROL Edit]**.

1. 必要な変更を加えて次の操作を行います **カスタム参照番号** および **コメント**.

   払い戻し金額は変更できません。

1. クリック **[!UICONTROL Save]**.

## ストアフロントのクレジット情報

会社管理者の場合、アカウントダッシュボードにが表示されます _会社クレジット_ セクション。 現在の未処理残高、使用可能なクレジット、会社アカウントに割り当てられたクレジット制限に続いて、未処理請求書のリストが提供されます。

マーチャントが会社クレジットに請求された注文をキャンセルした場合、注文金額は会社の残高および _与信配賦履歴_ アクションのレコードを含みます。

![会社クレジット](./assets/company-credit.png){width="700" zoomable="yes"}

## 会社クレジットデモ

このデモビデオで会社のクレジットの管理について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
