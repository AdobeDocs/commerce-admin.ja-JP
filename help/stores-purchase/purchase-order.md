---
title: 発注書
description: ストアでのオフラインの支払い方法として発注書を設定する方法を説明します。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 発注書

A _発注書_ （PO）を使用すると、商用のお客様は PO 番号を参照することで、許可された購入に対して支払いを行うことができます。 注文書は、購入を行う会社によって事前に承認および発行されます。 チェックアウト時に、お客様は支払い方法として発注書を選択します。 請求書を受け取ると、会社は支払いシステムで支払いを処理し、購入の支払いを行います。

発注書による支払を受け入れる前に、必ず商業顧客の信用度を確立してください。

**_発注別の支払を構成する手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. 次の下 _[!UICONTROL Other Payment Methods]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL Purchase Order]**セクション。

   ![注文書](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [注文書](../configuration-reference/sales/payment-methods.md#purchase-order) が含まれる _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. この支払方法を有効にするには、次のように設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

1. を設定 **[!UICONTROL New Order Status]** 対象： `Pending` 支払いが承認されるまで。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. を設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** （この支払方法の対象として必要な金額）。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. の場合 **[!UICONTROL Sort Order]**：チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数字を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
