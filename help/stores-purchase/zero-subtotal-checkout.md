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

_小計ゼロのチェックアウト_ 小計が 0 の注文で、割引が適用された後に課税される場合に使用できます。 例えば、小計ゼロのチェックアウトは、次のような場合に使用できます。

- 割引は購入価格の全額をカバーし、送料は無料です。

- 顧客がを追加します [ダウンロード可能](../catalog/product-create-downloadable.md) または [仮想](../catalog/product-create-virtual.md) 商品が買い物かごに入っており、価格が 0 に等しい。

- の価格 [シンプル](../catalog/product-create-simple.md) product がゼロで、 [送料無料](shipping-free.md) メソッドを使用できます。

- A [クーポンコード](../merchandising-promotions/price-rules-cart-coupon.md) 製品と送料の全額をカバーします。

時間を節約するために、小計ゼロの注文を自動請求に設定できます。

**_小計ゼロのチェックアウトを構成するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. 次の下 _[!UICONTROL Other Payment Methods]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL Zero Subtotal Checkout]**セクション。

   ![小計ゼロ チェックアウト](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. 小計ゼロのチェックアウトを有効化するには、を設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時のゼロ小計メソッドを識別するタイトルを入力します。

1. 注文が通常、承認を待つ場合は、デフォルトのを使用します **[!UICONTROL New Order Status]** as `Pending"` 注文が承認されるまで。

   必要に応じて、を使用できます `Processing` または `Suspected Fraud` この支払い方法を使用する新しい注文のステータス。

1. を設定 **[!UICONTROL Automatically Invoice All Items]** 対象： `Yes` 残高がゼロのすべての品目を自動的に請求する場合。

   このオプションは、 **[!UICONTROL New Order Status]** オプションの設定 `Processing`.

   >[!NOTE]
   >
   >次の場合 _[!UICONTROL New Order Status]_はに設定されています。 `Processing` および_[!UICONTROL Automatically Invoice All Items]_ はに設定されています。 `No`を割り当てる必要があります **[!UICONTROL Order Status]** = `Processing` の場合 **[!UICONTROL Order State]** = `Pending` および **[!UICONTROL Default Status]** = `No` のマッピング [注文ステータス](order-status.md#custom-order-status) ページ。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. の場合 **[!UICONTROL Sort Order]**：チェックアウト時に表示される支払い方法のリストでのこの項目の位置を決定する数値を入力します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
