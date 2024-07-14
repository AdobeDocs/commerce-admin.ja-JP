---
title: 小切手注文とマネーオーダー
description: ストア上でオフラインの支払い方法として小切手とマネーオーダーを設定する方法を説明します。
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 小切手注文とマネーオーダー

Adobe CommerceとMagento Open Sourceでは、小切手またはマネーオーダーで支払いを受け入れることができます。 _小切手/マネーオーダー_ の支払い方法は、デフォルトでストアに対して有効になっています。 特定の国からの小切手とマネーオーダーのみを受け入れることができ、注文の合計制限の最小値と最大値で設定を微調整できます。

**_小切手または送金による支払を構成するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. 「_[!UICONTROL Other Payment Methods]_」の下の「展開セレクター ![ 「**[!UICONTROL Check / Money Order]**」セクション ](../assets/icon-display-expand.png) を展開します。

   ![ 小切手/送金 ](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   各設定の詳細については、『設定リファレンスガイド _の [ 小切手/マネーオーダー ](../configuration-reference/sales/payment-methods.md#check--money-order) を参照してくだ_ い。

   >[!NOTE]
   >
   >必要に応じて、最初に「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

1. 小切手または送金による支払いを受け付けるには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]**：チェックアウト時の小切手/送金方法を識別するタイトルを入力します。

1. 注文が通常、承認を待つ場合は、承認されるまでデフォルト **[!UICONTROL New Order Status]** を `Pending"` として受け入れます。

   必要に応じて、この支払い方法を使用して新しい注文の `Processing` または `Suspected Fraud` のステータスを使用できます。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. **[!UICONTROL Make Check Payable To]**：小切手を支払う必要があるパーティの名称を入力します。

1. **[!UICONTROL Send Check To]**：小切手が郵送される住所または私書箱を入力します。

1. この支払い方法の対象として必要な注文金額に **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** を設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. **[!UICONTROL Sort Order]** の場合は、チェックアウト時に表示される支払い方法の一覧で、この項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
