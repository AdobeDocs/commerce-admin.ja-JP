---
title: チェックアウト合計の並べ替え順
description: 表示されるチェックアウト合計と、注文概要でチェックアウト合計の並べ替え順序を設定する方法について説明します。
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 257
ht-degree: 0%

---

# チェックアウト合計の並べ替え順

注文レビュー中は、割引、配送料、店舗クレジット、税金の調整が行われ、合計が注文の下部に表示されます。 各項目の順序は計算の順序を決定し、各項目に割り当てられた番号で設定されます。 例えば、小計はセクションの最初の項目で、値10が割り当てられます。 Grand Totalは最後に表示され、100の値が割り当てられます。 合計セクション内の他のすべての項目には、これらの値の間に値が割り当てられます。

![注文概要にチェックアウトの合計が表示されます](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_チェックアウト合計の並べ替え順序を設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」セクションを展開し、下の「**[!UICONTROL Sales]**」を選択します。

1. **[!UICONTROL Checkout Totals Sort Order]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![並べ替え順序を決定するために番号付けされたチェックアウト合計オプション ](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   これらの各構成設定について詳しくは、_構成リファレンスガイド_&#x200B;の「[ チェックアウト合計の並べ替え順](../configuration-reference/sales/sales.md#checkout-totals-sort-order)」を参照してください。

1. 設定が特定のストアビューの場合、[設定が適用されるストアビュー](../configuration-reference/scope-change.md#set-the-scope)を選択します。

   プロンプトが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックして続行します。

1. _合計_ セクションの順序を判断するには、各項目に割り当てられている番号を変更します。

   値が低いほど、リスト内の配置が早くなります。 デフォルト設定では、小計（`10`）が最初で、総計（`100`）が最後です。

   必要に応じて、**[!UICONTROL Use system value]** チェックボックスをオフにして、これらの変更を完了します。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。
