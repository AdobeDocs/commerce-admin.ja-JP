---
title: 発送設定
description: ストアの発送元と配送ポリシーを定義する配送設定の設定方法を説明します。
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# 発送設定

出荷構成では、すべての出荷の原産地点、出荷方針、および複数の所在地への出荷処理が設定されます。

## 原点

出荷元は、店舗または倉庫から行われた出荷の請求を計算するために使用され、また販売された製品の税率を決定します。 [EU 税 ](international-tax-guidelines.md#eu-tax-configuration) を計算する場合は、各ストア表示の [ デフォルトの税宛先計算 ](../configuration-reference/sales/tax.md) が出荷設定の起源に対応していることを確認してください。

![ 接触チャネル ](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. **[!UICONTROL Origin]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を完了します。

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] （必要に応じて 2 行目）

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 配送ポリシー

配送ポリシーでは、会社の配送に関するビジネスルールとガイドラインを説明する必要があります。 例えば、送料無料をトリガーとする価格ルールがある場合、送料ポリシーの条件を説明できます。

![ チェックアウト時の送料 ](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

チェックアウト時に配送ポリシーを表示するには、設定の配送ポリシーパラメーターを入力します。 このテキストは、お客様がチェックアウト時に _配送ポリシーを参照_ をクリックすると表示されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Shipping Settings]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Shipping Policy Parameters]**」セクションを展開します。

1. **[!UICONTROL Apply Custom Shipping Policy]** を `Yes` に設定します。

1. テキストボックスに **[!UICONTROL Shipping Policy]** を貼り付けるか入力します。

   >[!NOTE]
   >
   >ワードプロセッサーを使用してテキストを作成する場合は、ドキュメントを.txt ファイルとして保存して、テキストから制御文字を削除してください。 次に、テキストをコピーして「出荷ポリシー」テキストボックスに貼り付けます。

   ![ 配送ポリシーのパラメーター ](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 複数のアドレス

複数の住所配送オプションを使用すると、お客様はチェックアウト時に注文を複数の住所に発送し、注文を発送できる最大住所数を決定できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Multishipping Settings]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Options]**」セクションを展開します。

   ![ 複数の住所を使用する配送オプション ](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Allow Shipping to Multiple Addresses]** を `Yes` に設定します。

1. **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** を入力します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B）配送先住所が複数ある注文の場合、[ 対顧客払い ](../b2b/enable-basic-features.md#configure-payment-on-account) の支払い方法は、有効になっている場合でも、チェックアウト時には使用できません。
