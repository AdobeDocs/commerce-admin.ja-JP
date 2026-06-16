---
title: ストアクレジットを適用
description: ストア管理者は、ストアクレジットを購入に適用できます。
exl-id: 97b6b206-71db-435c-8736-a781437bb0b4
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/O2EJMZscownPnhjPeFROdwikhYmHuDYdCx4N7NpXlho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 0%

---

# ストアクレジットを適用

{{ee-feature}}

ストア管理者は、顧客アカウントからクレジット残高と履歴を表示し、ストアクレジットを購入に適用することもできます。

![顧客のクレジット残高と履歴](assets/store-credit-balance-history.png){width="600" zoomable="yes"}

## クレジット残高の表示

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. グリッド内の顧客を検索します。

1. _アクション_&#x200B;列で、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. _[!UICONTROL Customer View]_ページをスクロールし、下部の&#x200B;**[!UICONTROL Store Credit Balance]**を表示します。

![店舗クレジット残高](assets/store-credit-balance.png){width="600" zoomable="yes"}

## ストアのクレジット残高の更新

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > _操作_ > **[!UICONTROL All Customers]**&#x200B;に移動します。

1. グリッド内の顧客を検索します。

1. _アクション_&#x200B;列で、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 左側のパネルで、**[!UICONTROL Store Credit]**&#x200B;を選択します。

1. 残高に関連付けるweb サイト（ストアフロント）を選択します。

1. **[!UICONTROL Update Balance]**&#x200B;に新しい値を入力します。

1. 残高の更新を顧客に通知するには、**[!UICONTROL Notify Customer by Email]** チェックボックスを選択し、**[!UICONTROL Send Email Notification From the Following Store View]**&#x200B;からストアビューを選択します。

1. 変更について&#x200B;**[!UICONTROL Comment]**&#x200B;を入力してください。

1. 更新が完了したら、**[!UICONTROL Save and Continue Edit]**&#x200B;または&#x200B;**[!UICONTROL Save Customer]**&#x200B;をクリックします。

更新された残高は&#x200B;**[!UICONTROL Balance History]**&#x200B;に表示されます。

## ストア管理者として注文にクレジット残高を適用する

ストア管理者は、注文の送信など、顧客に代わって様々な操作を行うことができます。 [注文を作成](../stores-purchase/customer-account-create-order.md)する場合、お客様が支払うべきストアクレジット残高を適用できます。 使用可能な残高は、_支払いと配送情報_ セクションに表示されます。 残高を適用するには、**[!UICONTROL Use Store Credit]** チェックボックスを選択します。注文合計が少ない場合は、残高の一部を適用します。

![注文に店舗のクレジット残高を適用する](assets/store-credit-apply.png){width="500" zoomable="yes"}

## チェックアウト時にストアクレジットを適用する

サイトにクレジット残高がある場合、顧客はストアフロントで注文する前に、注文残高にストアクレジットを適用できます。

1. 顧客は、利用可能なストアクレジットの金額を表示します。

   _確認と支払い_&#x200B;の手順では、使用可能な金額は&#x200B;_[!UICONTROL Store Credit]_の下に表示されます。

1. 金額を注文に適用するには、**[!UICONTROL Use Store Credit]**&#x200B;をクリックします。

   >[!INFO]
   >
   >注文合計が再計算され、適用される店舗クレジットの金額が&#x200B;_[!UICONTROL Order Summary]_に表示されます。

   ![注文に適用されたストアのクレジット残高](assets/store-credit-checkout.png){width="700" zoomable="yes"}

1. 準備ができたら、**[!UICONTROL Place Order]**&#x200B;をクリックします。
