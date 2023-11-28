---
title: 発注書
description: 店舗でのオフライン支払い方法として発注書を設定する方法を説明します。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 発注書

A _発注書_ (PO) を使用すると、商用の顧客は、発注番号を参照して、許可された購入に対して支払うことができます。 発注は、発注元の会社が事前に承認し、発行します。 チェックアウト時に、顧客は支払い方法として発注を選択します。 請求書を受け取ると、会社は支払いシステムで支払いを処理し、購入に対して支払いを行います。

発注による支払いを受け入れる前に、常に商業顧客の信用度を確立します。

**_発注別の支払を構成する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. の下 _[!UICONTROL Other Payment Methods]_、展開 ![拡張セレクター](../assets/icon-display-expand.png) の&#x200B;**[!UICONTROL Purchase Order]**」セクションに入力します。

   ![発注書](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [発注書](../configuration-reference/sales/payment-methods.md#purchase-order) （内） _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. この支払い方法を有効にするには、次を設定します： **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

1. 設定 **[!UICONTROL New Order Status]** から `Pending` 支払いが許可されるまで

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** をこの支払い方法に適合するために必要な金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間にあるか、または完全に一致する場合に認定されます。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数値を入力します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
