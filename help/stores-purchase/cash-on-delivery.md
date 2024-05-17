---
title: 代金引換払い（COD）
description: ストアでのオフラインの支払い方法として代金引換を設定する方法を説明します。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 代金引換払い（COD）

Adobe CommerceとMagento Open Sourceでは、以下を受け入れることができます。 _代金引換払い_ （COD）購入の支払い。 特定の国からのみ代金引換払いを受け付けることができ、最小注文と最大注文の合計制限で設定を微調整できます。

配送業者は、配送時に顧客から支払いを受け取り、それはあなたに転送されます。 配送料および手数料に関して、配送業者サービスが請求する料金を調整することができます。

**_代金引換支払を設定する手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. 次の下 _その他のお支払方法_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Cash On Delivery Payment]** セクション。

   ![代金引換払い](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [代金引換支払](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) が含まれる _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. 代金引換支払を有効にするには、次を設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時の代金引換払い方法を識別するタイトルを入力します。

1. を設定 **[!UICONTROL New Order Status]** 対象： `Pending` 支払いの受領が確認されるまで。

   必要に応じて、を使用できます `Processing` または `Suspected Fraud` この支払い方法を使用する新しい注文のステータス。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. を入力 **[!UICONTROL Instructions]** 代金引換注文の配送を受け付ける場合。

1. を設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** 代金引換払いの対象として必要な金額を注文に記載します。

   >[!NOTE]
   >
   >注文は、合計が最小注文の合計と最大注文の合計の間にあるか、合計と一致するかを検証します。

1. の場合 **[!UICONTROL Sort Order]**：チェックアウト時に表示される支払い方法のリストでのこの項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
