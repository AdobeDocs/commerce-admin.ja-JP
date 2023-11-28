---
title: 輸入階層価格
description: 階層別の価格データをエクスポートし、更新されたデータをインポートする方法を説明します。
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 輸入階層価格

入力する代わりに [段階価格](../catalog/product-price-tier.md) 各製品に対して手動でおこなうと、 [インポート](data-import.md) 価格データ。 作業を開始する前に、テンプレートとして使用できる、エクスポートされた階層価格データのサンプルファイルを作成します。

![ストアフロントの例 — 階層型価格](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 手順 1：階層価格データをエクスポートする

次の例では、1 つの製品の階層別価格データをエクスポートしています。 次に、エクスポートされたデータを階層価格データの一括インポートのテンプレートとして使用できます。 高度な価格データのエクスポートについて詳しくは、 [高度な価格データ](data-attributes-product.md#advanced-pricing-attributes).

![製品階層型価格](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. オン _管理者_ サイドバー、移動  **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. の下 _[!UICONTROL Export Settings]_，設定&#x200B;**[!UICONTROL Entity Type]**から `Advanced Pricing`.

1. Adobe Analytics の **[!UICONTROL Entity Attributes]** グリッドで、SKU 属性まで下にスクロールし、次の操作をおこないます。

   - 割引率に基づく価格帯の場合は、エクスポートする各製品の SKU をコンマで区切って入力します。

     ![データの書き出し — 製品 SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 固定金額に基づく階層価格の場合は、各製品の SKU を入力します。

   - 下にスクロールして、 **[!UICONTROL Continue]**.

1. Web ブラウザーのダウンロード場所で書き出しファイルを探し、ファイルを開きます。

   ![例 — エクスポートされた顧客グループ割引階層価格データ](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_エクスポートされた階層価格データ_**

次の列が、エクスポートされたデータに含まれます。

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

エクスポートしたデータを、階層価格データをインポートするためのテンプレートとして使用します。

## 手順 2：データの更新

1. 必要に応じて、各製品の階層価格データを更新します。

   価格が更新されていない製品は、CSV ファイルから削除できます。 変更されていない製品を再読み込みする必要はありません。

1. **[!UICONTROL Save]** 更新された CSV ファイル。

>[!NOTE]
>
>インポートファイルのサイズは 2 MB 以下にする必要があります。

## 手順 3：更新されたデータをインポート

1. オン _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. の下 _読み込み設定_，設定 **[!UICONTROL Entity Type]** から `Advanced Pricing`.

1. 設定 **[!UICONTROL Import Behavior]** から `Add/Update`.

1. の下 **[!UICONTROL File to Import]**&#x200B;をクリックし、 **[!UICONTROL Choose File]** をクリックし、インポートする準備をしたファイルをディレクトリから選択します。

1. 右上隅で、 **[!UICONTROL Check Data]**.

1. ファイルが有効な場合は、 **[!UICONTROL Import]**.

   それ以外の場合は、メッセージに表示されるデータの問題を修正し、もう一度ファイルをインポートしてみてください。
