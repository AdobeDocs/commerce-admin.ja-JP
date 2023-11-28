---
title: 送料無料
description: 店舗の無料配送オプションを設定する方法を説明します。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# 送料無料

_送料無料_ は、提供できる最も効果的なプロモーションの 1 つです。 最小購入数に基づいて設定することも、 [買い物かごの価格ルール](../merchandising-promotions/price-rules-cart.md) これは、一連の条件が満たされたときに適用されます。 両方が同じ順序に当てはまる場合は、設定が買い物かごのルールよりも優先されます。

>[!NOTE]
>
>送料の無料配送に必要な追加設定については、配送業者の設定を確認してください。

## 手順 1：送料無料の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Free Shipping]** 」セクションに入力します。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、次の設定を変更します。

1. 設定 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時に送料無料方法を識別するタイトルと **[!UICONTROL Method Name]** それを説明する

1. の場合 **[!UICONTROL Minimum Order Amount]**、送料無料に該当する最小合計値を入力します。

   >[!TIP]
   >
   >で送料を無料で使用するには [表レート](shipping-table-rate.md)を設定し、 _[!UICONTROL Minimum Order Amount]_あまりに高くて決して会わない この高い値を使用すると、価格ルールによってトリガーされない限り、送料の無料利用が有効になりません。

1. 設定 **[!UICONTROL Include Tax to Amount]**:

   - `Yes`  — 最小受注額（小計+税金 — 割引）の計算時に税金が含まれます。
   - `No`  — 最小受注額（小計 — 割引）の計算時に税金は含まれません。

   ![送料無料](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Displayed Error Message]**、送料が無料になった場合に表示するメッセージを入力します。

1. 設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) お使いのストア設定で指定されたものは、無料配送を使用できます。

   - `Specific Countries`  — この値を選択した後、 _[!UICONTROL Ship to Specific Countries]_リストが表示されます。 リスト内の各国を選択し、送料無料を使用できます。

1. 設定 **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes`  — 該当しない場合でも、常に無料配送方法を表示します。
   - `No`  — 該当する場合にのみ、[ 送料無料 ] メソッドを表示します。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時の配送方法のリストで、送料の無料位置を決定する番号を入力します。

   `0` =最初 `1` =秒 `2` = 3 番目、など。

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：配送業者の設定で送料無料を有効にする

送料無料に使用する予定の各配送業者に必要な設定を必ず完了してください。 例えば、 [UPS 構成](ups.md) が完了していない場合は、次の設定を更新して無料配送を有効にして設定します。

1. Adobe Analytics の _[!UICONTROL Delivery Methods]_設定、展開 ![拡張セレクター](../assets/icon-display-expand.png) の&#x200B;**[!UICONTROL UPS]**」セクションに入力します。

1. 設定 **[!UICONTROL Free Method]** から `UPS Ground` または別のタイプを指定して無料で送料を提供します。

1. 送料を無料で受け取るための最小注文を要求するには、 **[!UICONTROL Enable Free Shipping Threshold]** から `Enable`.

   最小注文額を使用する場合は、次の項目に必要な金額を入力します。 **[!UICONTROL Free Shipping Amount Threshold]**.

1. クリック **[!UICONTROL Save Config]**.
