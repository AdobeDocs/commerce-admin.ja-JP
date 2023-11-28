---
title: 店舗クレジットの適用
description: 店舗管理者は、購入に店舗クレジットを適用できます。
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# 店舗クレジットの適用

{{ee-feature}}

店舗管理者は、顧客アカウントからクレジット残高と履歴を表示し、店舗クレジットを購入に適用することもできます。

![顧客のクレジット残高と履歴](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## クレジット残高の表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッド内の顧客を検索します。

1. Adobe Analytics の _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. スクロール _[!UICONTROL Customer View]_ページとビュー&#x200B;**[!UICONTROL Store Credit Balance]**下に

![店舗クレジット残高](assets/store-credit-balance.png){width="600" zoomable="yes"}

## 店舗クレジット残高の更新

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > _運用_ > **[!UICONTROL All Customers]**.

1. グリッド内の顧客を検索します。

1. Adobe Analytics の _アクション_ 列、クリック **[!UICONTROL Edit]**.

1. 左側のパネルで、を選択します。 **[!UICONTROL Store Credit]**.

1. 残高に関連付ける Web サイト（ストアフロント）を選択します。

1. の場合 **[!UICONTROL Update Balance]**&#x200B;に値を入力し、新しい値を入力します。

1. 残高の更新を顧客に通知するには、「 **[!UICONTROL Notify Customer by Email]** チェックボックスをオンにして、次の場所からストア表示を選択します。 **[!UICONTROL Send Email Notification From the Following Store View]**.

1. を入力します。 **[!UICONTROL Comment]** 変化について。

1. 更新が完了したら、 **[!UICONTROL Save and Continue Edit]** または **[!UICONTROL Save Customer]**.

更新された残高がに表示されます。 **[!UICONTROL Balance History]**.

## 店舗管理者としての注文にクレジット残高を適用

店舗管理者は、顧客に代わって、注文の送信など、様々な操作をおこなうことができます。 次の場合： [注文を作成する](../stores-purchase/customer-account-create-order.md)に設定すると、顧客が支払う店舗クレジット残高を適用できます。 使用可能な残高が _支払いと配送先情報_ 」セクションに入力します。 を選択します。 **[!UICONTROL Use Store Credit]** チェックボックスを選択して残高を適用します。注文の合計が少ない場合は残高の一部を適用します。

![店舗クレジット残高を注文に適用](assets/store-credit-apply.png){width="500" zoomable="yes"}

## チェックアウト時に店舗クレジットを適用

サイトにクレジット残高がある場合、顧客は店頭に注文を配置する前に、店舗クレジットを注文残高に適用できます。

1. 顧客が利用可能な店舗クレジットの金額を表示します。

   期間 _レビューと支払い_ 手順を実行すると、使用可能な量が次の場所に表示されます。 _[!UICONTROL Store Credit]_.

1. 注文に金額を適用するには、次をクリックします。 **[!UICONTROL Use Store Credit]**.

   >[!INFO]
   >
   >注文の合計が再計算され、適用される店舗クレジットの額が _[!UICONTROL Order Summary]_.

   ![注文に適用された店頭クレジット残高](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 準備が整ったら、クリックします **[!UICONTROL Place Order]**.
