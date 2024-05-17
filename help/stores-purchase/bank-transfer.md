---
title: 銀行振込
description: ストアでのオフライン支払い方法として銀行振込を設定する方法を説明します。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 銀行振込

Adobe CommerceとMagento Open Sourceを使用すると、お客様の銀行口座から送金され、お客様の商業銀行口座に入金された支払いを受け入れることができます。

**_銀行振込支払を構成する手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. 次の下 _その他のお支払方法_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Bank Transfer Payment]** セクション。

   ![銀行振込による支払い](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. 銀行振替を有効化するには、次のように設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時の銀行振込支払方法を識別するタイトルを入力します。

1. を設定 **[!UICONTROL New Order Status]** 対象： `Pending` 支払いが承認されるまで。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。

   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. を入力 **[!UICONTROL Instructions]** 顧客が銀行振込を設定する際に従う必要があること。

   銀行の所在国と銀行の要件に応じて、次の情報を含めることができます。

   - 銀行口座名
   - 銀行口座番号
   - 銀行のルーティング コード
   - 銀行名
   - 銀行住所

1. を設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** （この支払方法の使用に必要な金額）。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. の場合 **[!UICONTROL Sort Order]**：チェックアウト時に表示される支払い方法のリストでのこの項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
