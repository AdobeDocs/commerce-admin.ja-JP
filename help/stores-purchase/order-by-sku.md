---
title: SKU で並べ替え
description: 顧客の利便性を考慮して SKU での並べ替えをサポートするようにストアを設定する方法を説明します。
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# SKU で並べ替え

{{ee-feature}}

「SKU」は「在庫管理単位」です。 SKU は通常、オンラインセラーがサイズ、色、価格、素材などの最も重要な製品特性を識別するのに役立ちます。 製品 ID は SKU とは異なります。

- この `Product ID` は、内部的に製品を識別するために使用される一連の数値で、顧客は使用できません。
- この `SKU` 通常、マーケティングまたは内部トラッキングの製品名および属性に基づいて、販売者によって生成されます。 例：青色の綿 T シャツ、サイズ中間：T-COT-MED-BL。 SKU は、必要に応じて販売者によって変更される場合があります。

通常、SKU には製品の際立った特徴を示す略語のセットが含まれます。 SKU の長さは最大 64 文字です。 SKU は在庫を効果的に追跡および管理するために重要なので、SKU を正しく設定することは、e コマースにとって重要です。

_SKU で並べ替え_ が [ウィジェット](../content-design/widgets.md) すべての買い物客の便宜のためにストアに表示することも、特定の顧客グループの買い物客のみが利用できるようにすることもできます。 買い物客は、SKU および数量情報を Order by SKU ブロックに直接入力するか、顧客アカウントから CSV ファイルをアップロードできます。 設定に関係なく、ストア管理者は常に SKU で注文できます。

![ストアフロントでの SKU による並べ替え](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## SKU による順序の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** セクションで選択 **[!UICONTROL Sales]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order by SKU Settings]** セクション。

1. を設定 **[!UICONTROL Enable Order by SKU on my Account in Storefront]** を次のいずれかに変更します。

   - `Yes, for Everyone`  – 並べ替え SKU ブロックは、すべての買い物客に対してストアで使用できます。
   - `Yes, for Specified Customer Groups` - SKU による並べ替えは、次のような特定の顧客グループのメンバーのみが使用できます `Wholesale`.
   - `No` - ストアフロントに「SKU で注文」ブロックが表示されず、お客様のアカウントでは「SKU で注文」ページを使用できません。

   ![SKU 設定で並べ替え](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B のみ） _**「SKU で並べ替え」機能を有効にするには、「クイックオーダー」機能を無効にします。**_

1. に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL B2B Features]**

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL B2B Features]** セクション。

1. を設定 **[!UICONTROL Enable Quick Order]** 対象： `No`.

   この [クイックオーダー機能](../b2b/quick-order.md) を使用すると、顧客およびゲストは SKU または製品名に基づいてすばやく注文できます。

## ストアフロントの経験

ストアの機能が設定されると、顧客は次の機能を含むすべてのページから SKU で注文できます _SKU で並べ替え_ ウィジェットまたはアカウントダッシュボードから。

### ページブロックからの SKU で並べ替え

1. が含まれる _SKU で並べ替え_ ブロックすると、顧客は **[!UICONTROL SKU]** および **[!UICONTROL Qty]** 注文する品目の。

1. 別の項目を追加するには、をクリックします **[!UICONTROL Add Row]** そしてプロセスを繰り返します。

1. クリック数 **[!UICONTROL Add to Cart]**.

### 顧客アカウントからの SKU による注文

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 左側のパネルで、を選択します **[!UICONTROL Order by SKU]**.

1. 環境設定に従って個別の項目を追加します。

   _**SKU ごとに各項目を追加します：**_

   - エントリ数： **[!UICONTROL SKU]** および **[!UICONTROL Qty]** 注文する品目の。

   - 必要に応じて項目を追加するには、をクリックします _行を追加_ ![プラス記号ボタン](../assets/button-add-item.png) およびは、必要な数の項目に対して繰り返されます。

   - クリック数 **[!UICONTROL Add to Cart]**.

   _**複数項目の CSV ファイルをアップロードします。**_

   - 準備： [データ CSV を読み込む](../systems/data-csv.md) （コンマ区切り値）ファイルに含まれる、以下の列 `SKU` および `Qty`.

   ![インポートする SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - CSV ファイルをアップロードするには、をクリックします **[!UICONTROL Choose File]** アップロードするファイルを選択します。

   - クリック数 **[!UICONTROL Add to Cart]**.

   いずれかの製品に追加のオプションがある場合、買い物かごから、製品に注意が必要であることを尋ねられます。

   ![注意が必要な製品](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >SKU が重複している場合、買い物かごで数量が 1 つの行項目に結合されます。 顧客は任意の品目の数量を変更し、 **[!UICONTROL Update Shopping Cart]** 合計を再計算します。

