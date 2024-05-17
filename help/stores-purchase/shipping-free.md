---
title: 送料無料
description: ストアに送料無料オプションを設定する方法を説明します。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 送料無料

_送料無料_ は、提供できる最も効果的なプロモーションの 1 つです。 最小購入に基づくことも、 [買い物かご価格ルール](../merchandising-promotions/price-rules-cart.md) これは、一連の条件が満たされた場合に適用されます。 両方が同じ注文に適用される場合、設定は買い物かごルールよりも優先されます。

>[!NOTE]
>
>無料配送に必要な追加の設定については、配送業者の設定を確認してください。

## 手順 1：送料無料の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Free Shipping]** セクション。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、説明に従って次の設定を変更します。

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;に入力します。ここでは、チェックアウト時の送料無料の方法を識別します。 **[!UICONTROL Method Name]** 説明します。

1. の場合 **[!UICONTROL Minimum Order Amount]**、送料無料の対象となる最小合計値を入力します。

   >[!TIP]
   >
   >で送料無料を使用するには [テーブル率](shipping-table-rate.md)、を作成 _[!UICONTROL Minimum Order Amount]_非常に高いので、それが満たされることはありません。 この高い値を使用すると、価格ルールによってトリガーされない限り、送料無料が有効になりません。

1. を設定 **[!UICONTROL Include Tax to Amount]**:

   - `Yes`  – 最小注文金額を計算する際に税金を含みます（小計+税金 – 割引）。
   - `No`  – 最小注文金額（小計 – 割引）の計算時に税金を含まない。

   ![送料無料](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Displayed Error Message]**&#x200B;を入力します。送料無料が利用できなくなったときに表示されるメッセージを入力します。

1. を設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストアの設定で指定した場合は、送料無料を使用できます。

   - `Specific Countries`  – この値を選択すると、 _[!UICONTROL Ship to Specific Countries]_リストが表示されます。 リストから、送料無料を使用できる国を 1 つずつ選択します。

1. を設定 **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes`  – 該当しない場合でも、常に送料無料の方法を表示します。
   - `No`  – 該当する場合にのみ送料無料の方法を表示します。

1. の場合 **[!UICONTROL Sort Order]**、送料無料の位置を決定する番号を、チェックアウト時に配信方法のリストに入力します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：通信事業者設定で送料無料を有効にする

送料無料のために使用する予定の各通信事業者に必要な設定を完了してください。 例えば、次のような場合 [UPS の構成](ups.md) が完了していない場合は、次の設定を更新して送料無料を有効にし、設定します。

1. が含まれる _[!UICONTROL Delivery Methods]_設定、展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL UPS]**セクション。

1. を設定 **[!UICONTROL Free Method]** 対象： `UPS Ground` または、送料無料で指定する別のタイプ。

1. 送料無料の最低注文を要求するには、次のように設定します **[!UICONTROL Enable Free Shipping Threshold]** 対象： `Enable`.

   最小注文を使用する場合は、必要な金額を入力します **[!UICONTROL Free Shipping Amount Threshold]**.

1. クリック **[!UICONTROL Save Config]**.
