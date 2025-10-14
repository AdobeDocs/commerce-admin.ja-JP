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

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. _その他の支払い方法_ の下で、![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) の「**[!UICONTROL Bank Transfer Payment]**」セクションを展開します。

   ![&#x200B; 振替支払 &#x200B;](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、最初に「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

1. 銀行振込を有効化するには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]** に、チェックアウト時の銀行振込支払方法を識別するタイトルを入力します。

1. 支払いが承認されるまで **[!UICONTROL New Order Status]** を `Pending` に設定します。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [&#x200B; 国 &#x200B;](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。

   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. 顧客が銀行振込を設定する際に従う必要がある **[!UICONTROL Instructions]** を入力します。

   銀行の所在国と銀行の要件に応じて、次の情報を含めることができます。

   - 銀行口座名
   - 銀行口座番号
   - 銀行のルーティング コード
   - 銀行名
   - 銀行住所

1. この支払い方法を使用するために必要な金額を **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. **[!UICONTROL Sort Order]** の場合は、チェックアウト時に表示される支払い方法の一覧で、この項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
