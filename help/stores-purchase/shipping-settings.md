---
title: 発送設定
description: ストアの出発地点と発送ポリシーを定義する発送設定を構成する方法を説明します。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# 発送設定

出荷設定は、すべての出荷の原産地点、お客様の出荷ポリシー、複数の住所への出荷の処理を設定します。

## 原点

原産地点は、店舗や倉庫からの出荷に対する料金を計算し、販売された製品の税率を決定するために使用されます。 計算時 [EU 税](international-tax-guidelines.md#eu-tax-configuration)を使用して、 [デフォルトの税金宛先の計算](../configuration-reference/sales/tax.md) 各ストア表示は、発送元の設定に対応します。

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Shipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Origin]** 「 」セクションで以下の手順を実行します。

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] （必要に応じて行 2）

1. クリック **[!UICONTROL Save Config]**.

## 発送ポリシー

出荷ポリシーは、貴社のビジネスルールと出荷のガイドラインを説明する必要があります。 例えば、送料が無料である価格ルールがある場合、トリガーの送料ポリシーの条件を説明することができます。

![チェックアウト時の配送ポリシー](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

チェックアウト時に出荷ポリシーを表示するには、構成の「出荷ポリシー・パラメータ」に入力します。 このテキストは、ユーザーが _発送ポリシーを参照_ チェックアウト時に。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Shipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Shipping Policy Parameters]** 」セクションに入力します。

1. 設定 **[!UICONTROL Apply Custom Shipping Policy]** から `Yes`.

1. 貼り付けるか、 **[!UICONTROL Shipping Policy]** をテキストボックスに挿入します。

   >[!NOTE]
   >
   >テキストの作成にワープロを使用する場合は、ドキュメントを.txt ファイルとして保存し、テキストから制御文字を削除します。 次に、テキストをコピーし、「発送ポリシー」テキストボックスに貼り付けます。

   ![発送ポリシーのパラメーター](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 複数のアドレス

複数の住所の配送オプションを使用すると、顧客はチェックアウト時に複数の住所に注文を配送でき、注文を発送できる最大住所数を決定できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Multishipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Options]** 」セクションに入力します。

   ![複数住所の配送オプション](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Allow Shipping to Multiple Addresses]** から `Yes`.

1. 次を入力します。 **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. クリック **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce用 B2B](../assets/b2b.svg) (Adobe Commerceの場合 B2B) 複数の配送先住所を持つ注文の場合、 [アカウントでの支払い](../b2b/enable-basic-features.md#configure-payment-on-account) 支払い方法は、有効になっている場合でも、チェックアウト時に使用できません。
