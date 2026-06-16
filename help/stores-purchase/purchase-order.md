---
title: 発注
description: ストアでオフラインの支払い方法として発注書を設定する方法について説明します。
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 296
ht-degree: 0%

---

# 発注

_発注書_ （PO）を使用すると、法人のお客様は、PO番号を参照して承認済みの購入品に対する支払いを行うことができます。 発注書は、購入を行う企業によって事前に承認および発行されます。 チェックアウト時に、お客様は支払い方法として発注書を選択します。 請求書を受け取ると、会社は買掛金システムで支払いを処理し、購入の支払いを行います。

発注書による支払いを受け入れる前に、常に商用顧客の信用価値を確立してください。

**_発注書による支払いを設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Payment Methods]**&#x200B;を選択します。

1. _[!UICONTROL Other Payment Methods]_&#x200B;で、**[!UICONTROL Purchase Order]**&#x200B;セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![発注書](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   これらの各設定設定の詳細については、_設定リファレンスガイド_&#x200B;の[発注](../configuration-reference/sales/payment-methods.md#purchase-order)を参照してください。

   >[!NOTE]
   >
   >必要に応じて、まず&#x200B;**[!UICONTROL Use system value]** チェックボックスをオフにして、これらの設定を変更します。

1. この支払い方法を有効にするには、**[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Title]**&#x200B;に、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

1. 支払いが承認されるまで、**[!UICONTROL New Order Status]**&#x200B;を`Pending`に設定します。

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

1. **[!UICONTROL Minimum Order Total]**&#x200B;と&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;をこの支払い方法の対象に必要な金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まるか、正確に一致するかを判断します。

1. **[!UICONTROL Sort Order]**&#x200B;の場合、チェックアウト時に表示される支払い方法のリストに、この項目の位置を決定する数値を入力します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
