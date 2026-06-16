---
title: 送料無料
description: ストアに送料無料オプションを設定する方法について説明します。
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/bLvgCzOtiYjpSdTm7f0Te5fjWbiaL3mfC4DN8ONbOLs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 395
ht-degree: 0%

---

# 送料無料

_送料無料_&#x200B;は、最も効果的なプロモーションの1つです。 最低購入額に基づいて設定することも、一連の条件が満たされたときに適用される[&#x200B; カート価格ルール &#x200B;](../merchandising-promotions/price-rules-cart.md)として設定することもできます。 両方が同じ注文に適用される場合、設定設定は買い物かごルールよりも優先されます。

>[!NOTE]
>
>送料無料に必要な追加の設定については、配送業者の設定を確認してください。

## ステップ 1：送料無料の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Delivery Methods]**&#x200B;を選択します。

1. **[!UICONTROL Free Shipping]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   >[!NOTE]
   >
   >必要に応じて、最初に&#x200B;**[!UICONTROL Use system value]** チェックボックスの選択を解除し、説明に従って次の設定を変更します。

1. **[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Title]**&#x200B;の場合、チェックアウト時に送料無料の方法を識別するタイトルと、それを説明する&#x200B;**[!UICONTROL Method Name]**&#x200B;を入力します。

1. **[!UICONTROL Minimum Order Amount]**&#x200B;の場合、送料無料に適格な最小合計値を入力します。

   >[!TIP]
   >
   >[表の料金](shipping-table-rate.md)で送料無料を利用するには、_[!UICONTROL Minimum Order Amount]_&#x200B;を高くして、満たされないようにします。 この高い値を使用すると、価格規則によってトリガーされない限り、送料無料が有効になりません。

1. **[!UICONTROL Include Tax to Amount]**&#x200B;を設定：

   - `Yes` – 最低注文金額（小計+税 – 割引）を計算する際に税金が含まれます。
   - `No` – 最低注文金額（小計 – 割引）を計算する際に税金が含まれていません。

   ![送料無料](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. **[!UICONTROL Displayed Error Message]**&#x200B;について、送料無料が利用できなくなった場合に表示されるメッセージを入力します。

1. **[!UICONTROL Ship to Applicable Countries]**&#x200B;を設定：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、送料無料を利用できます。

   - `Specific Countries` – この値を選択すると、_[!UICONTROL Ship to Specific Countries]_&#x200B;リストが表示されます。 送料無料を利用できる国をリストから選択します。

1. **[!UICONTROL Show Method if Not Applicable]**&#x200B;を設定：

   - `Yes` – 適用されない場合でも、常に送料無料の方法を表示します。
   - `No` – 該当する場合にのみ、送料無料の方法を表示します。

1. **[!UICONTROL Sort Order]**&#x200B;の場合、チェックアウト時の配送方法のリストに、送料無料の位置を決定する番号を入力します。

   `0` = first、`1` = second、`2` = thirdなど。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## 手順2: キャリア設定で送料無料を有効にする

送料無料で使用する各キャリアに必要な設定を完了してください。 例えば、[UPS設定](ups.md)が完了した場合は、次の設定を更新して送料無料を有効にして設定します。

1. _[!UICONTROL Delivery Methods]_&#x200B;設定で、**[!UICONTROL UPS]**&#x200B;セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Free Method]**&#x200B;を`UPS Ground`または送料無料で指定する別の種類に設定します。

1. 送料無料の最低注文を必要とするには、**[!UICONTROL Enable Free Shipping Threshold]**&#x200B;を`Enable`に設定します。

   最低注文を使用する場合は、**[!UICONTROL Free Shipping Amount Threshold]**&#x200B;に必要な金額を入力してください。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。
