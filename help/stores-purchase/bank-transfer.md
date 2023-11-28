---
title: 銀行振替
description: 店舗でのオフライン支払い方法として銀行振込を設定する方法を説明します。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 銀行振替

Adobe CommerceとMagento Open Sourceを使用すると、顧客の銀行口座から振り込まれ、お客様の商業銀行口座に振り込まれた支払いを受け入れることができます。

**_銀行振替支払を構成する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. の下 _その他の支払い方法_、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Bank Transfer Payment]** 」セクションに入力します。

   ![銀行振替支払](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. 銀行振替を有効化するには、次を設定します。 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時に銀行振替支払い方法を識別するタイトルを入力します。

1. 設定 **[!UICONTROL New Order Status]** から `Pending` 支払いが許可されるまで

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。

   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 次を入力します。 **[!UICONTROL Instructions]** 顧客が銀行振込を設定する際に従う必要があることを示します。

   銀行の所在国および銀行の要件に応じて、次の情報を含めることができます。

   - 銀行口座名
   - 銀行口座番号
   - 銀行ルーティングコード
   - 銀行名
   - 銀行の住所

1. 設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** を、この支払い方法の使用資格を得るために必要な金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間にあるか、または完全に一致する場合に認定されます。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数値を入力します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
