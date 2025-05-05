---
title: 小計ゼロのチェックアウト
description: ストアでのオフライン支払い方法としてゼロの小計を設定する方法を説明します。
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 小計ゼロのチェックアウト

_小計ゼロのチェックアウト_ は、割引が適用された後に課税される、小計がゼロの注文に使用できます。 例えば、小計ゼロのチェックアウトは、次のような場合に使用できます。

- 割引は購入価格の全額をカバーし、送料は無料です。

- 顧客が買い物かごに [ ダウンロード可能 ](../catalog/product-create-downloadable.md) または [ 仮想 ](../catalog/product-create-virtual.md) 製品を追加し、価格がゼロに等しい。

- [ シンプル ](../catalog/product-create-simple.md) 商品の価格はゼロで、[ 送料無料 ](shipping-free.md) の方法が利用可能です。

- [ クーポンコード ](../merchandising-promotions/price-rules-cart-coupon.md) は、製品と送料の全額をカバーしています。

時間を節約するために、小計ゼロの注文を自動請求に設定できます。

**_ゼロ小計チェックアウトを設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. 「_[!UICONTROL Other Payment Methods]_」の下の「展開セレクター ![ 「**[!UICONTROL Zero Subtotal Checkout]**」セクション ](../assets/icon-display-expand.png) を展開します。

   ![ 小計ゼロのチェックアウト ](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、最初に「**[!UICONTROL Use system value]**」チェックボックスをオフにして、これらの設定を変更します。

1. 小計ゼロのチェックアウトを有効にするには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. **[!UICONTROL Title]** の場合は、チェックアウト時にゼロ小計メソッドを識別するタイトルを入力します。

1. 注文が通常、承認を待つ場合は、注文が承認されるまで、デフォルト **[!UICONTROL New Order Status]** を `Pending"` として受け入れます。

   必要に応じて、この支払い方法を使用して新しい注文の `Processing` または `Suspected Fraud` のステータスを使用できます。

1. 残高がゼロのすべての品目を自動的に請求する場合は、**[!UICONTROL Automatically Invoice All Items]** を `Yes` に設定します。

   このオプションは、**[!UICONTROL New Order Status]** オプションが `Processing` に設定されている場合にのみ使用できます。

   >[!NOTE]
   >
   >_[!UICONTROL New Order Status]_&#x200B;が `Processing` に設定され、_[!UICONTROL Automatically Invoice All Items]_ が `No` に設定されている場合、「[ 注文ステータス ](order-status.md#custom-order-status)」ページで **[!UICONTROL Order State]** = `Pending` および **[!UICONTROL Default Status]** = `No` マッピングに **[!UICONTROL Order Status]** = `Processing` を割り当てる必要もあります。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. **[!UICONTROL Sort Order]** の場合は、チェックアウト時に表示される支払い方法の一覧で、この項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
