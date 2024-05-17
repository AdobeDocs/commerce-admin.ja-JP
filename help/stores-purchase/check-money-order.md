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

Adobe CommerceとMagento Open Sourceでは、小切手またはマネーオーダーで支払いを受け入れることができます。 この _小切手/送金_ ストアの支払い方法はデフォルトで有効になっています。 特定の国からの小切手とマネーオーダーのみを受け入れることができ、注文の合計制限の最小値と最大値で設定を微調整できます。

**_小切手または送金による支払を構成する手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. 次の下 _[!UICONTROL Other Payment Methods]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL Check / Money Order]**セクション。

   ![小切手/送金](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [小切手/送金](../configuration-reference/sales/payment-methods.md#check--money-order) が含まれる _設定リファレンスガイド_.

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. 小切手または送金による支払いを受け付けるには、次のように設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時の小切手/送金方法を識別するタイトルを入力します。

1. 注文が通常、承認を待つ場合は、デフォルトのを使用します **[!UICONTROL New Order Status]** as `Pending"` 承認されるまで。

   必要に応じて、を使用できます `Processing` または `Suspected Fraud` この支払い方法を使用する新しい注文のステータス。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. の場合 **[!UICONTROL Make Check Payable To]**：小切手を支払う必要のある関係者の名前を入力します。

1. の場合 **[!UICONTROL Send Check To]**：小切手が郵送される住所（私書箱）を入力します。

1. を設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** ご注文の金額は、この支払い方法の対象として必要です。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. の場合 **[!UICONTROL Sort Order]**：チェックアウト時に表示される支払い方法のリストでのこの項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
