---
title: 戻り値の設定
description: ストアの返品を有効にし、サポートされる発送方法を設定する方法を説明します。
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 戻り値の設定

{{ee-feature}}

有効にすると、お客様はストアフロントから RMA 要求を送信できます。 RMA は、返品可能な受注品目がある場合にのみ生成できます。 個々の項目を返すリクエストは、 _RMA の有効化_ 各製品レコードの属性。 デフォルトでは、設定は製品 (_[!UICONTROL Use Config Settings]_が選択されている )。 次の場合_[!UICONTROL Enable RMA]_ が `No`の場合、製品は返品可能な品目のリストに表示されません。 次の項目を変更した場合、 _RMA の有効化_ 設定の場合、新規注文と既存注文の両方に適用されます。

## ストアの RMA を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL RMA Settings]** 」セクションに入力します。

   ![RMA 設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable RMA on Storefront]** から `Yes`.

   この設定は、顧客がストアフロントから RMA 要求を作成および表示できるかどうかを決定します。 RMA は、新規受注と既存受注の両方に適用できます。

1. 設定 **[!UICONTROL Enable RMA on Product Level]** から `Yes`.

   この設定によって、 _RMA の有効化_ ストアフロントの個々の製品の属性：

   - 条件 [!UICONTROL Enable RMA on Product Level] が `Yes`を使用すると、ストアフロントのお客様は個々の製品をすべて返すことができます。 これには、両方が含まれます _[!UICONTROL Enable RMA]_= `Yes` および_[!UICONTROL Enable RMA]_ = `No` 製品属性値。
   - 条件 [!UICONTROL Enable RMA on Product Level] が `No`を使用すると、ストアフロントのお客様は、 _[!UICONTROL Enable RMA]_= `Yes` 製品属性値。

1. 設定 **[!UICONTROL Use Store Address]** を次のいずれかの値に変更します。

   - `Yes`  — 返品された製品をストアのアドレスに送信します。
   - `No`  — 製品返品の別の住所を入力します。

   ![RMA 設定と代替アドレス](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 返品の発送方法の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 次のように、返品サービスに使用する運送業者のセクションを展開します。 **[!UICONTROL UPS]**.

   ![運送業者の RMA サービスを有効にする](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled for RMA]** から `Yes`.

1. クリック **[!UICONTROL Save Config]**.

## 製品レベルでの許可 RMA の変更

店舗の RMA を有効にし、カタログに返品を許可しない製品が含まれている場合は、製品レベルで設定を変更できます。

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Autosettings]** 」セクションに入力します。

1. 次をクリア： **[!UICONTROL Use Config Setting]** チェックボックス（必要に応じて）

1. 切り替え **[!UICONTROL Enable RMA]** に設定します。 `No`.

   ![製品の RMA の無効化](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.
