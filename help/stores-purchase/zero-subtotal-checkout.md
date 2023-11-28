---
title: 小計チェックアウトなし
description: 店舗でのオフライン支払い方法としてゼロ小計を設定する方法を説明します。
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 小計チェックアウトなし

_小計チェックアウトなし_ は、割引が適用された後に課税される、小計が 0 の注文に使用できます。 例えば、次の状況で、小計ゼロのチェックアウトが使用される場合があります。

- 割引は購入の価格全体をカバーし、送料は追加料金ではありません。

- 顧客が [ダウンロード可能](../catalog/product-create-downloadable.md) または [仮想](../catalog/product-create-virtual.md) 製品を買い物かごに追加し、価格が 0 に等しくなります。

- の価格 [単純](../catalog/product-create-simple.md) 製品がゼロで、 [無料送料](shipping-free.md) メソッドを使用できます。

- A [クーポンコード](../merchandising-promotions/price-rules-cart-coupon.md) 製品と出荷の全価格をカバーします。

時間を節約するために、自動請求書に小計注文を 0 に設定できます。

**_ゼロ小計チェックアウトを設定する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. の下 _[!UICONTROL Other Payment Methods]_、展開 ![拡張セレクター](../assets/icon-display-expand.png) の&#x200B;**[!UICONTROL Zero Subtotal Checkout]**」セクションに入力します。

   ![小計ゼロのチェックアウト](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. 小計ゼロのチェックアウトを有効にするには、 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**」に、チェックアウト時に「0 小計」メソッドを識別するタイトルを入力します。

1. 注文が通常承認を待つ場合は、デフォルトを受け入れます **[!UICONTROL New Order Status]** as `Pending"` 注文が承認されるまで。

   必要に応じて、 `Processing` または `Suspected Fraud` この支払い方法での新規注文のステータス。

1. 設定 **[!UICONTROL Automatically Invoice All Items]** から `Yes` 残高がゼロのすべての品目を自動的に請求する場合。

   このオプションは、 **[!UICONTROL New Order Status]** オプションが `Processing`.

   >[!NOTE]
   >
   >次の場合 _[!UICONTROL New Order Status]_が `Processing` および_[!UICONTROL Automatically Invoice All Items]_ が `No`を設定する場合は、 **[!UICONTROL Order Status]** = `Processing` （の） **[!UICONTROL Order State]** = `Pending` および **[!UICONTROL Default Status]** = `No` マッピング [注文ステータス](order-status.md#custom-order-status) ページに貼り付けます。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. の場合 **[!UICONTROL Sort Order]**、チェックアウト時に表示される支払い方法のリストで、この項目の位置を決定する数値を入力します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
