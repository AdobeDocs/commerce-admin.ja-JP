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

注文の払い戻しが発行されている場合、お客様はアカウントダッシュボードで注文に関連する払い戻し情報を表示できます。 を有効にしている場合 [!UICONTROL _顧客に店舗の与信履歴を表示_] オプション [ストアクレジットの設定](../customers/credit-configure.md)の場合、ユーザーも次にアクセスできます [店舗クレジット](../customers/store-credit.md) 履歴。

## ストアフロントの払い戻しの表示

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 次のいずれかの方法を使用して、順序を検索します。

   * リストでの順序の検索 **最近の注文** とクリック **[!UICONTROL View]**.
   * 左パネルで、を選択します。 **[!UICONTROL My Orders]**. 次に、リスト内の順序を見つけて、 **[!UICONTROL View]**.

1. ユーザーが **[!UICONTROL Refunds]** tab キーを押すと払い戻しの詳細が表示されます。

   ![ストアフロントの払い戻し詳細](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## ストアフロントでの店舗クレジット残高と履歴の表示

メソッド 1: **顧客アカウントダッシュボードから**

1. ストアフロントから、顧客はにログインします。

1. 返金が店舗クレジットに適用された場合、は選択します **[!UICONTROL Store Credit]** 左側のパネルで次の操作を行います。

1. ストアクレジットに払い戻された金額は、アクションの日時と共にリストに表示されます。

   ![ストアクレジットに払い戻された金額](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >「ストアクレジット」ページには、顧客が引き換えるリンクもあります。 [ギフトカード](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

メソッド 2: **から _レビューと支払い_ ページ**

1. 顧客が商品を買い物かごに追加します。

2. に進みます _チェックアウト_ ページ。

3. は成功します **[!UICONTROL Shipping]** ステップ。

4. ストアクレジットを利用できる場合は、顧客がクリックします **[!UICONTROL Use Store Credit]**.

   ![「検討および支払」ページからのクレジットの格納](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. ストアクレジットの使用に関するお客様の考えを変える場合は、をクリックします **[!UICONTROL Remove]** が含まれる _注文概要_ セクション。

## 管理者の支払いアクション

特定の顧客に対して支払いアクションを設定できます [支払い方法](../configuration-reference/sales/payment-methods.md). 各支払い方法には、異なる支払いアクションのセットがあります。

| 支払いアクション | 説明 |
|--- |---|
| [!UICONTROL Capture Online] | 請求書が送信されると、システムはサードパーティの支払いゲートウェイから支払いをキャプチャします。 その後、管理者ユーザーはクレジット・メモを作成し、請求書を無効にできます。 |
| [!UICONTROL Capture Offline] | 請求書が送信されると、システムは支払をキャプチャしません。 支払いはゲートウェイを通じて直接取得され、支払いはAdobe Commerceを通じて取得できないと想定されています。 その後、管理者ユーザーはクレジット・メモを作成できますが、請求書を無効化することはできません。 （注文がオンライン支払を使用していた場合でも、請求書は基本的にオフライン請求書です。） |
| [!UICONTROL Not Capture] | 請求書が送信されると、システムは支払をキャプチャしません。 支払いは、後でAdobe Commerceを通じて取得されると想定されます。 次のものがあります [!UICONTROL _キャプチャ_] 完了した請求書のボタン キャプチャする前に、請求書をキャンセルできます。 取得後、クレジット・メモを作成し、請求書を無効にできます。 |

{style="table-layout:auto"}

>[!WARNING]
>
>「」を選択します [!UICONTROL _キャプチャしない_] 後でAdobe Commerceを通じて支払いをキャプチャすることが確実でない限り、オプション。 を使用して支払が取り込まれるまで、クレジット・メモを作成できません。 [!UICONTROL _キャプチャ_] ボタン。
