---
title: 戻り値の設定
description: ストアの返品を有効にする方法と、サポートされる配送方法を設定する方法について説明します。
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 戻り値の設定

{{ee-feature}}

有効化すると、顧客がストアフロントから RMA リクエストを送信できるようになります。 RMA は、返品可能な品目が注文にある場合にのみ生成できます。 個々の項目を返すリクエストは、 _RMA を有効にする_ 各製品レコードの属性。 デフォルトでは、設定が製品に適用されます（_[!UICONTROL Use Config Settings]_が選択されている）。 次の場合_[!UICONTROL Enable RMA]_ はに設定されています。 `No`その場合、製品は返品可能な項目のリストには表示されません。 変更した場合 _RMA を有効にする_ 設定すると、新規注文と既存注文の両方に適用されます。

## ストアの RMA を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL RMA Settings]** セクション。

   ![RMA 設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable RMA on Storefront]** 対象： `Yes`.

   この設定により、顧客がストアフロントからの RMA リクエストを作成および表示できるかどうかが決まります。 RMA は、新規注文と既存注文の両方に適用できます。

1. を設定 **[!UICONTROL Enable RMA on Product Level]** 対象： `Yes`.

   この設定により、の動作が決まります _RMA を有効にする_ ストアフロントの個々の製品の属性：

   - 条件 [!UICONTROL Enable RMA on Product Level] はに設定されています。 `Yes`を使用すると、ストアフロントの顧客は、個々の製品をすべて返すことができます。 次の両方が含まれます _[!UICONTROL Enable RMA]_= `Yes` および_[!UICONTROL Enable RMA]_ = `No` 製品属性値。
   - 条件 [!UICONTROL Enable RMA on Product Level] はに設定されています。 `No`を使用すると、ストアフロントにいるお客様は、 _[!UICONTROL Enable RMA]_= `Yes` 製品属性値。

1. を設定 **[!UICONTROL Use Store Address]** を次のいずれかの値に変更します。

   - `Yes`  – 返品された商品をストアアドレスに送信します。
   - `No`  – 製品の返品用の代替住所を入力します。

   ![代替アドレスを使用した RMA 設定](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 返品用の出荷方法の構成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. 再来訪サービスに使用する通信事業者のセクションを展開します。例えば、次のようになります **[!UICONTROL UPS]**.

   ![通信事業者の RMA サービスを有効にする](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled for RMA]** 対象： `Yes`.

1. クリック **[!UICONTROL Save Config]**.

## 製品レベルでの許可された RMA の変更

ストアの RMA を有効にし、カタログに返品を許可してはいけない製品が含まれている場合は、製品レベルで設定を変更できます。

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Autosettings]** セクション。

1. をクリア **[!UICONTROL Use Config Setting]** 必要に応じて、チェックボックスをオンにします。

1. を切り替え **[!UICONTROL Enable RMA]** をに設定しています `No`.

   ![製品の RMA を無効にする](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]**.
