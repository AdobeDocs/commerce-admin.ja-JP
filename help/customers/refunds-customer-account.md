---
title: 顧客アカウントダッシュボードでの返金
description: 店舗の顧客は、注文に関連する払い戻し情報を自分のアカウントダッシュボードに表示できます。
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# 顧客アカウントダッシュボードでの返金

{{ee-feature}}

注文の返金が行われた場合、顧客は自分のアカウントダッシュボードで注文に関連する返金情報を表示できます。 を有効にしている場合、 [!UICONTROL _顧客に対する店舗クレジット履歴の表示_] のオプション [クレジット設定を保存](../customers/credit-configure.md)を使用して、 [店舗クレジット](../customers/store-credit.md) 履歴。

## ストアフロントの払い戻しを表示

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 次のいずれかの方法を使用して、順序を検索します。

   * リスト内の順序の検索 **最近の注文** をクリックし、 **[!UICONTROL View]**.
   * 左のパネルで、「 **[!UICONTROL My Orders]**. 次に、リスト内の順序を検索し、「 **[!UICONTROL View]**.

1. 顧客が **[!UICONTROL Refunds]** タブをクリックして返金の詳細を表示します。

   ![店頭の払い戻しの詳細](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## 店舗のクレジット残高と履歴を表示します

メソッド 1: **顧客アカウントダッシュボードから**

1. ストアフロントから、顧客がログインしてアカウントを設定します。

1. 店舗クレジットに払い戻しが適用された場合は、を選択します。 **[!UICONTROL Store Credit]** をクリックします。

1. 店舗クレジットに返済された金額は、アクションの日時と共にリストに表示されます。

   ![クレジットを保存するために払い戻された金額](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >クレジットを保存ページには、顧客が [ギフトカード](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

方法 2: **次から： _レビューと支払い_ ページ**

1. 顧客が買い物かごに製品を追加します。

2. 次に進む： _チェックアウト_ ページに貼り付けます。

3. を渡します。 **[!UICONTROL Shipping]** 手順

4. 店舗クレジットが使用可能な場合、顧客は **[!UICONTROL Use Store Credit]**.

   ![「レビューと支払い」ページのクレジットを保存](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. 顧客がストアクレジットの使用に関する考えを変更した場合は、「 **[!UICONTROL Remove]** （内） _注文の概要_ 」セクションに入力します。

## 管理での支払いアクション

特定の [支払い方法](../configuration-reference/sales/payment-methods.md). 各支払い方法には、異なる支払いアクションのセットがあります。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Capture Online] | 請求書が送信されると、システムは、サードパーティの支払いゲートウェイから支払いをキャプチャします。 管理者ユーザーは、クレジットメモを作成し、請求書を無効にすることができます。 |
| [!UICONTROL Capture Offline] | 請求書が発行されると、システムは支払をキャプチャしません。 支払いはゲートウェイを介して直接取得され、Adobe Commerceを介して取得できないと想定されます。 管理者ユーザーはクレジットメモを作成できますが、請求書を無効にすることはできません。 （注文でオンライン支払いが使用されていた場合でも、請求書は基本的にオフラインの請求書です。） |
| [!UICONTROL Not Capture] | 請求書が発行されると、システムは支払をキャプチャしません。 支払いが後でAdobe Commerceを通じて取り込まれると想定されます。 ここに [!UICONTROL _Capture_] 」ボタンをクリックします。 取り込む前に、請求書を取り消すことができます。 取得後は、クレジットメモを作成し、請求書を無効にすることができます。 |

{style="table-layout:auto"}

>[!WARNING]
>
>を選択します。 [!UICONTROL _キャプチャではありません_] オプションを使用できます。ただし、後でAdobe Commerceを通じて支払いをキャプチャすることが確実な場合は除きます。 クレジット・メモは、 [!UICONTROL _Capture_] 」ボタンをクリックします。
