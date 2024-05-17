---
title: 店舗クレジットの適用
description: ストア管理者は、購入にストアクレジットを適用できます。
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 店舗クレジットの適用

{{ee-feature}}

ストア管理者は、顧客アカウントからクレジット残高と履歴を表示でき、購入にストアクレジットを適用することもできます。

![顧客のクレジット残高と履歴](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## 貸方残高の表示

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客を検索します。

1. が含まれる _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. Scroll _[!UICONTROL Customer View]_をページおよび表示します&#x200B;**[!UICONTROL Store Credit Balance]**下部にあります。

![店舗の貸方残高](assets/store-credit-balance.png){width="600" zoomable="yes"}

## 店舗クレジット残高の更新

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > _運用_ > **[!UICONTROL All Customers]**.

1. グリッドで顧客を検索します。

1. が含まれる _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. 左パネルで、を選択します。 **[!UICONTROL Store Credit]**.

1. 残高に関連付ける Web サイト（ストアフロント）を選択します。

1. の場合 **[!UICONTROL Update Balance]**、新しい値を入力します。

1. 残高の更新を顧客に通知するには、 **[!UICONTROL Notify Customer by Email]** チェックボックスをオンにして、次からストア表示を選択します **[!UICONTROL Send Email Notification From the Following Store View]**.

1. を入力 **[!UICONTROL Comment]** 変更について。

1. 更新が完了したら、 **[!UICONTROL Save and Continue Edit]** または **[!UICONTROL Save Customer]**.

更新された残高はに表示されます。 **[!UICONTROL Balance History]**.

## 店舗管理者として注文にクレジット残高を適用する

ストア管理者は、顧客に代わって注文の送信など、様々な操作を実行できます。 実行する場合 [オーダーの作成](../stores-purchase/customer-account-create-order.md)を使用する場合は、顧客が支払うストアクレジット残高を適用できます。 使用可能な残高は _お支払いと配送情報_ セクション。 「」を選択します **[!UICONTROL Use Store Credit]** 残高を適用する場合はチェックボックス、注文合計が少ない場合は残高の一部。

![注文への店舗クレジット残高の適用](assets/store-credit-apply.png){width="500" zoomable="yes"}

## チェックアウト時の店舗クレジットの適用

サイトのクレジット残高がある場合、顧客は、ストアフロントに注文を配置する前に、注文残高にストアクレジットを適用できます。

1. 顧客は、使用可能なストアクレジットの量を表示します。

   期間中に _レビューと支払い_ 使用可能な量がの下に表示されます。 _[!UICONTROL Store Credit]_.

1. 金額を注文に適用するには、をクリックします **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >注文合計が再計算され、適用されたストアクレジットの額がに表示されます _[!UICONTROL Order Summary]_.

   ![注文に適用された店舗の貸方残高](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 準備ができたら、クリックします **[!UICONTROL Place Order]**.
