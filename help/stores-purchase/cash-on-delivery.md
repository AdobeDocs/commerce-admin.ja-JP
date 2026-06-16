---
title: 代金引換（COD）
description: オンラインストアのオフライン支払い方法として、代金引換を設定する方法について説明します。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
TQID: https://experienceleague.adobe.com/xKFjuGpjrF-XfVnNqWR2St8v3D4Lnr74WozkrynBbdo
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
source-wordcount: 336
ht-degree: 0%

---

# 代金引換（COD）

Adobe CommerceとMagento Open Sourceでは、購入時に&#x200B;_代金引換_ （COD）支払いを受け付けることができます。 特定の国からのみCOD支払いを受け付けることができ、最小注文合計制限と最大注文合計制限で設定を微調整できます。

配送業者は、配達時に顧客から支払いを受け取り、次にあなたに転送されます。 配送業者サービスが請求する手数料については、送料と処理手数料で調整することができます。

**_代金引換の支払いを設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Payment Methods]**&#x200B;を選択します。

1. _その他の支払い方法_&#x200B;で、**[!UICONTROL Cash On Delivery Payment]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![代金引換](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   これらの各設定設定の詳細については、_設定リファレンスガイド_&#x200B;の「[代金引換](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment)」を参照してください。

   >[!NOTE]
   >
   >必要に応じて、まず&#x200B;**[!UICONTROL Use system value]** チェックボックスをオフにして、これらの設定を変更します。

1. 代金引換の支払いを有効にするには、**[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Title]**&#x200B;に、チェックアウト時のCOD支払い方法を示すタイトルを入力します。

1. 決済が確認されるまで&#x200B;**[!UICONTROL New Order Status]**&#x200B;を`Pending`に設定します。

   ご希望の場合は、この支払い方法で`Processing`または`Suspected Fraud`のステータスを新しい注文に使用できます。

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、各オプションをクリックします。

1. COD注文の配達を受け付けるための&#x200B;**[!UICONTROL Instructions]**&#x200B;を入力します。

1. **[!UICONTROL Minimum Order Total]**&#x200B;と&#x200B;**[!UICONTROL Maximum Order Total]**&#x200B;を、COD支払いの条件を満たすために必要な注文金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小または最大の注文合計の間にあるか、一致するかを条件とします。

1. **[!UICONTROL Sort Order]**&#x200B;の場合、チェックアウト時に表示される支払い方法のリストに、この項目の位置を決定する数値を入力します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
