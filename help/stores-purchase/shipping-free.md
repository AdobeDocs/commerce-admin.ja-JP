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

_送料無料_ は、あなたが提供できる最も効果的なプロモーションの 1 つです。 これは、最小購入に基づくことも、一連の条件を満たした場合に適用される [ 買い物かご価格ルール ](../merchandising-promotions/price-rules-cart.md) として設定することもできます。 両方が同じ注文に適用される場合、設定は買い物かごルールよりも優先されます。

>[!NOTE]
>
>無料配送に必要な追加の設定については、配送業者の設定を確認してください。

## 手順 1：送料無料の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Delivery Methods]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Free Shipping]**」セクションを展開します。

   >[!NOTE]
   >
   >必要に応じて、まず「**[!UICONTROL Use system value]**」チェックボックスの選択を解除し、説明に従って次の設定を変更します。

1. **[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]** しくは、チェックアウト時の送料無料方法を識別するタイトルと、その説明 **[!UICONTROL Method Name]** を入力します。

1. **[!UICONTROL Minimum Order Amount]** に、送料無料の対象となる最小合計値を入力します。

   >[!TIP]
   >
   >[ テーブル料金 ](shipping-table-rate.md) で送料無料を使用するには、_[!UICONTROL Minimum Order Amount]_が満たされないほど高くします。 この高い値を使用すると、価格ルールによってトリガーされない限り、送料無料が有効になりません。

1. Set **[!UICONTROL Include Tax to Amount]**:

   - `Yes` – 最小注文金額を計算する際に税金を含みます（小計+税金 – 割引）。
   - `No` – 最小注文金額（小計 – 割引）の計算時に税金を含まない。

   ![ 送料無料 ](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. **[!UICONTROL Displayed Error Message]**：送料無料が利用できなくなった場合に表示するメッセージを入力します。

1. Set **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) のお客様は送料無料を使用できます。

   - `Specific Countries` – この値を選択すると、_[!UICONTROL Ship to Specific Countries]_リストが表示されます。 リストから、送料無料を使用できる国を 1 つずつ選択します。

1. Set **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` – 適用できない場合でも、常に送料無料の方法を表示します。
   - `No` – 該当する場合にのみ送料無料の方法を表示します。

1. **[!UICONTROL Sort Order]**：送料無料の位置を決定する番号を、チェックアウト時に配送方法のリストに入力します。

   `0` = 1 番目、`1` = 2 番目、`2` = 3 番目など。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 手順 2：通信事業者設定で送料無料を有効にする

送料無料のために使用する予定の各通信事業者に必要な設定を完了してください。 例えば、[UPS 設定 ](ups.md) が完了していない場合は、次の設定を更新して送料無料を有効にし、設定します。

1. _[!UICONTROL Delivery Methods]_設定で、「拡張セレクター ![ の「**[!UICONTROL UPS]**」セクション ](../assets/icon-display-expand.png) 展開します。

1. **[!UICONTROL Free Method]** を `UPS Ground` または送料無料に指定する別のタイプに設定します。

1. 送料無料の最低注文を要求するには、**[!UICONTROL Enable Free Shipping Threshold]** を `Enable` に設定します。

   最小注文を使用する場合は、**[!UICONTROL Free Shipping Amount Threshold]** に必要な金額を入力します。

1. 「**[!UICONTROL Save Config]**」をクリックします。
