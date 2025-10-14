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

_発注書_ （PO）を使用すると、商用のお客様は、PO 番号を参照することで、許可された購入に対する支払いを行うことができます。 注文書は、購入を行う会社によって事前に承認および発行されます。 チェックアウト時に、お客様は支払い方法として発注書を選択します。 請求書を受け取ると、会社は支払いシステムで支払いを処理し、購入の支払いを行います。

発注書による支払を受け入れる前に、必ず商業顧客の信用度を確立してください。

**_発注による支払を構成する手順は、次のとおりです。_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. 「_[!UICONTROL Other Payment Methods]_」の下の「展開セレクター ![&#x200B; 「**[!UICONTROL Purchase Order]**」セクション &#x200B;](../assets/icon-display-expand.png) を展開します。

   ![&#x200B; 注文書 &#x200B;](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   これらの各構成設定の詳細は、『 [&#x200B; 構成リファレンス・ガイド _の &#x200B;](../configuration-reference/sales/payment-methods.md#purchase-order) 発注_ を参照してください。

   >[!NOTE]
   >
   >必要に応じて、最初に「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

1. この支払方法を有効にするには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]** の場合は、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

1. 支払いが承認されるまで **[!UICONTROL New Order Status]** を `Pending` に設定します。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [&#x200B; 国 &#x200B;](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. この支払方法の対象として必要な金額を **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. **[!UICONTROL Sort Order]** の場合は、チェックアウト時に表示される支払い方法の一覧で、この項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
