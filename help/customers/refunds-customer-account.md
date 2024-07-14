---
title: 顧客アカウントダッシュボードでの払戻
description: ストアのお客様は、アカウントダッシュボードで、注文に関連付けられた払い戻し情報を表示できます。
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 顧客アカウントダッシュボードでの払戻

{{ee-feature}}

注文の払い戻しが発行されている場合、お客様はアカウントダッシュボードで注文に関連する払い戻し情報を表示できます。 [ ストアクレジット設定 ](../customers/credit-configure.md) に対して「[!UICONTROL _顧客にストアクレジット履歴を表示_]」オプションを有効にしている場合、顧客は [ ストアクレジット ](../customers/store-credit.md) 履歴にもアクセスできます。

## ストアフロントの払い戻しの表示

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 次のいずれかの方法を使用して、順序を検索します。

   * **最近の注文** のリストで注文を見つけて、クリック **[!UICONTROL View]** ます。
   * 左側のパネルで「**[!UICONTROL My Orders]**」を選択します。 次に、リスト内の順序を見つけて「**[!UICONTROL View]**」をクリックします。

1. お客様は「**[!UICONTROL Refunds]**」タブをクリックして、返金の詳細を表示します。

   ![ 店頭での払い戻し明細 ](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## ストアフロントでの店舗クレジット残高と履歴の表示

方法 1:**顧客アカウントダッシュボードから**

1. ストアフロントから、顧客はにログインします。

1. 払い戻しがストアクレジットに適用された場合、左側のパネルで **[!UICONTROL Store Credit]** を選択します。

1. ストアクレジットに払い戻された金額は、アクションの日時と共にリストに表示されます。

   ![ 店舗信用供与等払戻額 ](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >「ストアクレジット」ページには、顧客が [ ギフトカード ](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card) を引き換えるためのリンクも表示されます。

方法 2:**レビューと支払 _ページから_**

1. 顧客が商品を買い物かごに追加します。

2. 「チェックアウト _ページに進み_ す。

3. **[!UICONTROL Shipping]** のステップに合格します。

4. ストアクレジットを利用できる場合は、顧客は「**[!UICONTROL Use Store Credit]**」をクリックします。

   ![ レビューと支払ページのストアクレジット ](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. 顧客が店舗クレジットの使用に関する考えを変えた場合は、「注文概要 _セクションの&#x200B;**[!UICONTROL Remove]**をクリック_ ます。

## 管理者の支払いアクション

特定の [ 支払い方法 ](../configuration-reference/sales/payment-methods.md) に対して支払いアクションを設定できます。 各支払い方法には、異なる支払いアクションのセットがあります。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Capture Online] | 請求書が送信されると、システムはサードパーティの支払いゲートウェイから支払いをキャプチャします。 その後、管理者ユーザーはクレジット・メモを作成し、請求書を無効にできます。 |
| [!UICONTROL Capture Offline] | 請求書が送信されると、システムは支払をキャプチャしません。 支払いはゲートウェイを通じて直接取得され、支払いはAdobe Commerceを通じて取得できないと想定されています。 その後、管理者ユーザーはクレジット・メモを作成できますが、請求書を無効化することはできません。 （注文がオンライン支払を使用していた場合でも、請求書は基本的にオフライン請求書です。） |
| [!UICONTROL Not Capture] | 請求書が送信されると、システムは支払をキャプチャしません。 支払いは、後でAdobe Commerceを通じて取得されると想定されます。 完了した請求書には「[!UICONTROL _キャプチャ_]」ボタンがあります。 キャプチャする前に、請求書をキャンセルできます。 取得後、クレジット・メモを作成し、請求書を無効にできます。 |

{style="table-layout:auto"}

>[!WARNING]
>
>後でAdobe Commerceを通じて支払いをキャプチャすることが確実でない限り、「[!UICONTROL _キャプチャしない_]」オプションを選択します。 「[!UICONTROL _取得_]」ボタンを使用して支払を取得するまでは、クレジット・メモを作成できません。
