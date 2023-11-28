---
title: SKU 別の注文
description: 顧客の利便性を考慮して、SKU による注文をサポートするようにストアを設定する方法を説明します。
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# SKU 別の注文

{{ee-feature}}

「SKU」は「在庫管理単位」です。 SKU は、一般に、オンライン販売者が、サイズ、色、価格、素材など、最も重要な製品特性を特定するのに役立ちます。 製品 ID は SKU とは異なります。

- The `Product ID` は、内部的に製品の識別に使用され、顧客は利用できない一連の数字です。
- The `SKU` は、通常、マーケティングまたは内部トラッキングの製品名と属性に基づいて、販売者によって生成されます。 例：青、綿 T シャツ、サイズ中： T-COT-MED-BL。 SKU は、必要に応じて、販売者が変更する場合があります。

通常、SKU には製品の識別特性を示す一連の略語が含まれます。 SKU の最大長は 64 文字です。 在庫を効果的に追跡および管理するには、SKU が重要なので、e コマースでは正しく設定することが重要です。

_SKU 別の注文_ は [widget](../content-design/widgets.md) すべての買い物客の便宜を図ってストアに表示したり、特定の顧客グループの買い物客のみが利用できるようにします。 買い物客は、SKU と数量の情報を「SKU ごとの並べ替え」ブロックに直接入力するか、顧客アカウントから csv ファイルをアップロードできます。 設定に関係なく、店舗管理者は常に SKU 順に並べ替えることができます。

![ストアフロントの SKU による並べ替え](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## SKU ごとの並べ替えの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** 「 」セクションで「 」を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order by SKU Settings]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable Order by SKU on my Account in Storefront]** を次のいずれかに変更します。

   - `Yes, for Everyone` - SKU ごとの並べ替えブロックは、各買い物客のストアで利用できます。
   - `Yes, for Specified Customer Groups` - SKU ごとの注文は、特定の顧客グループのメンバー（例： ）のみが利用できます。 `Wholesale`.
   - `No`  — ストアフロントには「 SKU ごとの並べ替え」ブロックが表示されず、顧客アカウントでは「 SKU ごとの並べ替え」ページは使用できません。

   ![SKU 設定別の順序](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B(Adobe Commerceのみ )) _**「SKU ごとの並べ替え」機能を有効にするには、「クイックオーダー」機能を無効にします。**_

1. に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL B2B Features]**

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL B2B Features]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable Quick Order]** から `No`.

   The [クイックオーダー機能](../b2b/quick-order.md) では、顧客とゲストが SKU または製品名に基づいて迅速に注文をおこなうことができます。

## ストアフロントエクスペリエンス

この機能がストアに対して設定されている場合、顧客は、 _SKU 別の注文_ ウィジェットまたはアカウントダッシュボードから。

### ページブロックからの SKU 順の並べ替え

1. Adobe Analytics の _SKU 別の注文_ ブロックを使用する場合、顧客が **[!UICONTROL SKU]** および **[!UICONTROL Qty]** の値を指定します。

1. 別の項目を追加するには、「 **[!UICONTROL Add Row]** プロセスを繰り返します。

1. クリック数 **[!UICONTROL Add to Cart]**.

### 顧客アカウントからの SKU 別の注文

1. ストアフロントから、顧客は自分のアカウントにログインします。

1. 左側のパネルで、を選択します。 **[!UICONTROL Order by SKU]**.

1. 環境設定に従って個々の項目を追加します。

   _**各項目を SKU 別に追加します。**_

   - 次に入る **[!UICONTROL SKU]** および **[!UICONTROL Qty]** の値を指定します。

   - 必要に応じて他の項目を追加するには、「 」をクリックします。 _行を追加_ ![プラス記号ボタン](../assets/button-add-item.png) およびは、必要な数の項目に対して繰り返します。

   - クリック数 **[!UICONTROL Add to Cart]**.

   _**複数の項目の CSV ファイルをアップロードします。**_

   - を準備します。 [データ CSV を読み込み](../systems/data-csv.md) （コンマ区切り値）ファイル。 `SKU` および `Qty`.

   ![読み込む SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - CSV ファイルをアップロードするには、「 」をクリックします。 **[!UICONTROL Choose File]** をクリックし、アップロードするファイルを選択します。

   - クリック数 **[!UICONTROL Add to Cart]**.

   いずれかの製品に追加のオプションがある場合、顧客は買い物かごから、製品に注意が必要な旨のプロンプトを受け取ります。

   ![製品に注意が必要](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >重複する SKU がある場合、数量は買い物かご内の 1 つの行項目に組み合わされます。 顧客は、任意の品目の数量を変更し、 **[!UICONTROL Update Shopping Cart]** ：合計を再計算します。

