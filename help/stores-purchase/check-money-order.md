---
title: 小切手と為替
description: 店舗でのオフライン支払い方法として、小切手とマネーオーダーを設定する方法について説明します。
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
TQID: https://experienceleague.adobe.com/mmlEdLGANV93nvet3YwYoBGZKcft1qYuA6HboQ0Buvw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
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
source-wordcount: 337
ht-degree: 0%

---

# 小切手と為替

Adobe CommerceとMagento Open Sourceでは、小切手またはマネーオーダーによる支払いを受け付けることができます。 お客様の店舗では、デフォルトで&#x200B;_Check / Money Order_&#x200B;支払い方法が有効になっています。 特定の国からのみ小切手やマネーオーダーを受け付けることができ、最小および最大の注文合計制限で設定を微調整できます。

**_小切手または為替による支払いを設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Payment Methods]**&#x200B;を選択します。

1. _[!UICONTROL Other Payment Methods]_&#x200B;で、**[!UICONTROL Check / Money Order]**&#x200B;セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![小切手/為替](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   これらの各設定設定の詳細については、_設定リファレンスガイド_&#x200B;の[Check / Money Order](../configuration-reference/sales/payment-methods.md#check--money-order)を参照してください。

   >[!NOTE]
   >
   >必要に応じて、まず&#x200B;**[!UICONTROL Use system value]** チェックボックスをオフにして、これらの設定を変更します。

1. 小切手または為替によるお支払いを受け付けるには、**[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. 「**[!UICONTROL Title]**」に、チェックアウト時の小切手/マネーオーダーの支払い方法を識別するタイトルを入力します。

1. 注文が通常、承認を待っている場合は、承認されるまでデフォルトの&#x200B;**[!UICONTROL New Order Status]**&#x200B;を`Pending"`として受け入れます。

   ご希望の場合は、この支払い方法で`Processing`または`Suspected Fraud`のステータスを新しい注文に使用できます。

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

1. **[!UICONTROL Make Check Payable To]**&#x200B;に、小切手の支払い先となる関係者の名前を入力します。

1. **[!UICONTROL Send Check To]**&#x200B;の場合、小切手が郵送される住所または私書箱を入力します。

1. **[!UICONTROL Minimum Order Total]**&#x200B;と&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;を、この支払い方法の対象に必要な注文金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まるか、正確に一致するかを判断します。

1. **[!UICONTROL Sort Order]**&#x200B;の場合、チェックアウト時に表示される支払い方法のリストに、この項目の位置を決定する数値を入力します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
