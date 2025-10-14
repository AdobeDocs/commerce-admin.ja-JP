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

![&#x200B; 顧客の与信残高と履歴 &#x200B;](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## 貸方残高の表示

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL All Customers]** に移動します。

1. グリッドで顧客を検索します。

1. _アクション_ 列の「**[!UICONTROL Edit]**」をクリックします。

1. ページ _[!UICONTROL Customer View]_&#x200B;スクロールし、下部の&#x200B;**[!UICONTROL Store Credit Balance]**&#x200B;を表示します。

![&#x200B; 店舗の貸方残高 &#x200B;](assets/store-credit-balance.png){width="600" zoomable="yes"}

## 店舗クレジット残高の更新

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/_運営_/**[!UICONTROL All Customers]** に移動します。

1. グリッドで顧客を検索します。

1. _アクション_ 列の「**[!UICONTROL Edit]**」をクリックします。

1. 左側のパネルで「**[!UICONTROL Store Credit]**」を選択します。

1. 残高に関連付ける Web サイト（ストアフロント）を選択します。

1. **[!UICONTROL Update Balance]**：新しい値を入力します。

1. 残高の更新を顧客に通知するには、「**[!UICONTROL Notify Customer by Email]**」チェックボックスを選択し、**[!UICONTROL Send Email Notification From the Following Store View]** からストア表示を選択します。

1. 変更に関する **[!UICONTROL Comment]** を入力します。

1. 更新が完了したら、「**[!UICONTROL Save and Continue Edit]**」または「**[!UICONTROL Save Customer]**」をクリックします。

更新された残高は **[!UICONTROL Balance History]** に表示されます。

## 店舗管理者として注文にクレジット残高を適用する

ストア管理者は、顧客に代わって注文の送信など、様々な操作を実行できます。 [&#x200B; 注文の作成 &#x200B;](../stores-purchase/customer-account-create-order.md) 時に、顧客が支払うストアクレジット残高を適用できます。 使用可能な残高は、「支払および配送情報 _セクションに表示さ_ ます。 「**[!UICONTROL Use Store Credit]**」チェックボックスを選択して残高を適用するか、受注合計が少ない場合は残高の一部を適用します。

![&#x200B; 注文への店舗クレジット残高の適用 &#x200B;](assets/store-credit-apply.png){width="500" zoomable="yes"}

## チェックアウト時の店舗クレジットの適用

サイトのクレジット残高がある場合、顧客は、ストアフロントに注文を配置する前に、注文残高にストアクレジットを適用できます。

1. 顧客は、使用可能なストアクレジットの量を表示します。

   _レビューと支払い_ ステップ中に、使用可能な金額が _[!UICONTROL Store Credit]_&#x200B;の下に表示されます。

1. 金額を注文に適用するには、「**[!UICONTROL Use Store Credit]**」をクリックします。

   >[!INFO]
   >
   >注文合計が再計算され、適用されたストアクレジットの額が _[!UICONTROL Order Summary]_&#x200B;に表示されます。

   ![&#x200B; 注文に適用された店舗のクレジット残高 &#x200B;](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 準備ができたら、「**[!UICONTROL Place Order]**」をクリックします。
