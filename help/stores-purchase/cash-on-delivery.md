---
title: 現金配送 (COD)
description: 店舗でのオフライン支払い方法として、配送時に現金を設定する方法を説明します。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 現金配送 (COD)

Adobe CommerceとMagento Open Sourceを使用すると、 _受渡現金_ (COD) 購入に対する支払い。 特定の国からのみ COD の支払いを受け入れ、最小および最大の注文合計制限で設定を微調整できます。

配送業者は、配送時に顧客から支払いを受け取り、その後、お客様に転送されます。 配送料と取扱料で、運送業者サービスが請求した手数料の調整を行うことができます。

**_受渡支払に現金を設定する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. の下 _その他の支払い方法_、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Cash On Delivery Payment]** 」セクションに入力します。

   ![引渡現金支払](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [現金引渡支払](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) （内） _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. 配送時に現金を有効にするには、次を設定します。 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時に COD 支払い方法を識別するタイトルを入力します。

1. 設定 **[!UICONTROL New Order Status]** から `Pending` 支払いの受領が確認されるまで。

   必要に応じて、 `Processing` または `Suspected Fraud` この支払い方法での新規注文のステータス。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 次を入力します。 **[!UICONTROL Instructions]** COD 命令の引渡しを受け入れるために

1. 設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** を COD 支払の条件を満たすために必要な注文金額に追加します。

   >[!NOTE]
   >
   >合計が最小または最大の注文合計の間にあるか、一致する場合に、注文が評価されます。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数値を入力します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
