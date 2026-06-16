---
title: 銀行振込
description: オフラインの支払い方法として銀行振込をストアで設定する方法について説明します。
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
TQID: https://experienceleague.adobe.com/uIYk-S9M8nsKxo3O71N1z25Y-K5WaYOOAM26k9HLVoQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 銀行振込

Adobe CommerceとMagento Open Sourceでは、お客様の銀行口座から転送され、加盟店の銀行口座に入金される支払いを受け付けることができます。

**_銀行振込の支払いを設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Payment Methods]**&#x200B;を選択します。

1. _その他の支払い方法_&#x200B;で、**[!UICONTROL Bank Transfer Payment]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![銀行振込お支払い](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、まず&#x200B;**[!UICONTROL Use system value]** チェックボックスをオフにして、これらの設定を変更します。

1. 銀行振込を有効にするには、**[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Title]**&#x200B;に、チェックアウト時の銀行振込の支払い方法を示すタイトルを入力します。

1. 支払いが承認されるまで、**[!UICONTROL New Order Status]**&#x200B;を`Pending`に設定します。

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、この支払い方法を使用できます。

   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

1. お客様が銀行振込を設定するために従う必要がある&#x200B;**[!UICONTROL Instructions]**&#x200B;を入力します。

   銀行が所在する国と銀行の要件に応じて、次の情報を含めることができます。

   - 銀行口座名
   - 銀行口座番号
   - 銀行のルーティングコード
   - 銀行名
   - 銀行住所

1. **[!UICONTROL Minimum Order Total]**&#x200B;と&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;を、この支払い方法を使用する条件を満たすために必要な金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まるか、正確に一致するかを判断します。

1. **[!UICONTROL Sort Order]**&#x200B;の場合、チェックアウト時に表示される支払い方法のリストに、この項目の位置を決定する数値を入力します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
