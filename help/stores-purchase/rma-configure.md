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

有効化すると、顧客がストアフロントから RMA リクエストを送信できるようになります。 RMA は、返品可能な品目が注文にある場合にのみ生成できます。 個々の項目を返すリクエストは、各製品レコードの _RMA を有効にする_ 属性で管理されます。 デフォルトでは、設定が製品に適用されます（_[!UICONTROL Use Config Settings]_&#x200B;が選択されています）。_[!UICONTROL Enable RMA]_ を `No` に設定した場合、製品は返品可能な項目のリストには表示されません。 _RMA を有効化_ 設定を変更すると、新規注文と既存注文の両方に適用されます。

## ストアの RMA を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、その下の「**[!UICONTROL Sales]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL RMA Settings]**」セクションを展開します。

   ![RMA 設定 ](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable RMA on Storefront]** を `Yes` に設定します。

   この設定により、顧客がストアフロントからの RMA リクエストを作成および表示できるかどうかが決まります。 RMA は、新規注文と既存注文の両方に適用できます。

1. **[!UICONTROL Enable RMA on Product Level]** を `Yes` に設定します。

   この設定により、ストアフロントの個々の製品の _RMA を有効にする_ 属性の動作が決まります。

   - [!UICONTROL Enable RMA on Product Level] を `Yes` に設定すると、ストアフロントのお客様は、個々の製品をすべて返すことができます。 _[!UICONTROL Enable RMA]_= `Yes` と&#x200B;_[!UICONTROL Enable RMA]_ = `No` の製品属性値の両方が含まれます。
   - [!UICONTROL Enable RMA on Product Level] を `No` に設定すると、ストアフロントの顧客は、_[!UICONTROL Enable RMA]_= `Yes` 製品属性値を持つ製品のみを返すことができます。

1. **[!UICONTROL Use Store Address]** を次のいずれかの値に設定します。

   - `Yes` – 返品された商品をストアアドレスに送信します。
   - `No` – 製品の返品用の代替所在地を入力します。

   ![ 代替アドレスを使用した RMA 設定 ](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 返品用の出荷方法の構成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Delivery Methods]**」を選択します。

1. 再来訪サービスに使用する通信事業者のセクション（例：**[!UICONTROL UPS]**）を展開します。

   ![ 通信事業者の RMA サービスを有効にする ](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled for RMA]** を `Yes` に設定します。

1. 「**[!UICONTROL Save Config]**」をクリックします。

## 製品レベルでの許可された RMA の変更

ストアの RMA を有効にし、カタログに返品を許可してはいけない製品が含まれている場合は、製品レベルで設定を変更できます。

1. 製品を編集モードで開きます。

1. 下にスクロールして、「**[!UICONTROL Autosettings]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. 必要に応じて、「**[!UICONTROL Use Config Setting]**」チェックボックスをオフにします。

1. **[!UICONTROL Enable RMA]** 設定を `No` に切り替えます。

   ![ 製品の RMA の無効化 ](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Save]**」をクリックします。
