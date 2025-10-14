---
title: 代金引換払い（COD）
description: ストアでのオフラインの支払い方法として代金引換を設定する方法を説明します。
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 代金引換払い（COD）

Adobe CommerceとMagento Open Sourceでは、購入に対する _代金引換_ （COD）支払いを受け入れることができます。 特定の国からのみ代金引換払いを受け付けることができ、最小注文と最大注文の合計制限で設定を微調整できます。

配送業者は、配送時に顧客から支払いを受け取り、それはあなたに転送されます。 配送料および手数料に関して、配送業者サービスが請求する料金を調整することができます。

**_代金引換支払を設定する手順は、次のとおりです。_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. _その他の支払い方法_ の下で、![&#x200B; 拡張セレクター &#x200B;](../assets/icon-display-expand.png) の「**[!UICONTROL Cash On Delivery Payment]**」セクションを展開します。

   ![&#x200B; 代金交付金 &#x200B;](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   これらの各構成設定の詳細は、『 [&#x200B; 構成リファレンス ガイド _の「代金引換払い &#x200B;](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) を参照してください_。

   >[!NOTE]
   >
   >必要に応じて、最初に「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

1. 代金引換払いを有効にするには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]** の場合は、チェックアウト時の代金引換払い方法を識別するタイトルを入力します。

1. 支払の受領が確認されるまで、**[!UICONTROL New Order Status]** を `Pending` に設定します。

   必要に応じて、この支払い方法を使用して新しい注文の `Processing` または `Suspected Fraud` のステータスを使用できます。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [&#x200B; 国 &#x200B;](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. 代金引換払い注文の配送を受け付けるための **[!UICONTROL Instructions]** を入力します。

1. 代金引換払いの対象として必要な注文金額に **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** を設定します。

   >[!NOTE]
   >
   >注文は、合計が最小注文の合計と最大注文の合計の間にあるか、合計と一致するかを検証します。

1. **[!UICONTROL Sort Order]** の場合は、チェックアウト時に表示される支払い方法の一覧で、この項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
