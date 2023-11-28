---
title: 小切手と送金
description: 店舗での支払いのオフラインの方法として小切手と送金を設定する方法を学びます。
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 小切手と送金

Adobe CommerceとMagento Open Sourceでは、小切手や送金で支払いを受け入れることができます。 The _小切手/通貨注文_ デフォルトでは、お客様の店舗に対して支払い方法が有効になっています。 特定の国からのみ小切手や送金を受け付け、最小限および最大限の注文合計制限で構成を微調整できます。

**_小切手または送金による支払を構成する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. の下 _[!UICONTROL Other Payment Methods]_、展開 ![拡張セレクター](../assets/icon-display-expand.png) の&#x200B;**[!UICONTROL Check / Money Order]**」セクションに入力します。

   ![小切手/通貨注文](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [小切手/通貨注文](../configuration-reference/sales/payment-methods.md#check--money-order) （内） _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. 小切手または送金順で支払を受け入れるには、次の手順に従います。 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時の小切手/通貨注文の支払い方法を識別するタイトルを入力します。

1. 注文が通常承認を待つ場合は、デフォルトを受け入れます **[!UICONTROL New Order Status]** as `Pending"` 承認されるまで

   必要に応じて、 `Processing` または `Suspected Fraud` この支払い方法での新規注文のステータス。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. の場合 **[!UICONTROL Make Check Payable To]**：小切手を支払う必要がある当事者の名前を入力します。

1. の場合 **[!UICONTROL Send Check To]**、小切手の郵送先住所または PO Box を入力します。

1. 設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** をこの支払い方法に適合するために必要な注文金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間にあるか、または完全に一致する場合に認定されます。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数値を入力します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
