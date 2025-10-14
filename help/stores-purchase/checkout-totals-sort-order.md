---
title: チェックアウト合計の並べ替え順序
description: 表示されるチェックアウトの合計と、注文概要でチェックアウトの合計の並べ替え順を設定する方法について説明します。
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# チェックアウト合計の並べ替え順序

注文の確認時には、合計が注文の下部に表示され、割引、送料、店舗クレジット、税金の調整が行われます。 各項目の順序によって計算の順序が決まり、各項目に割り当てられた番号によって設定されます。 たとえば、小計はセクションの最初の項目で、値 10 が割り当てられます。 総計は最後に表示され、100 の値が割り当てられます。 合計セクション内のその他すべての項目には、これらの値の間に値が割り当てられます。

![&#x200B; 注文概要にはチェックアウトの合計が表示されます &#x200B;](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_チェックアウト合計の並べ替え順序を設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」セクションを展開し、その下 **[!UICONTROL Sales]** 選択します。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Checkout Totals Sort Order]**」セクションを展開します。

   ![&#x200B; 並べ替え順を決定するために番号付けされたチェックアウト合計オプション &#x200B;](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   これらの各設定の詳細については、『 [&#x200B; 設定リファレンスガイド _の &#x200B;](../configuration-reference/sales/sales.md#checkout-totals-sort-order) チェックアウト合計の並べ替え順序_ を参照してください。

1. 設定が特定のストア表示の場合は、[&#x200B; ストア表示を選択 &#x200B;](../configuration-reference/scope-change.md#set-the-scope) して設定が適用されます。

   プロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックして続行します。

1. _合計_ セクションの順序を決定するには、各項目に割り当てる番号を変更します。

   値が小さいほど、リスト内の位置が早くなります。 デフォルトの設定では、小計（`10`）が最初で、総計（`100`）が最後です。

   必要に応じて、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの変更を完了します。

1. 「**[!UICONTROL Save Config]**」をクリックします。
