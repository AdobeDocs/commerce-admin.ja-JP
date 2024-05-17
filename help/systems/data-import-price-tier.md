---
title: 階層の価格のインポート
description: 階層価格データをエクスポートし、更新されたデータをインポートする方法を説明します。
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---

# 階層の価格のインポート

入るのではなく [階層価格](../catalog/product-price-tier.md) 製品ごとに手動で行う方が、次の操作を行う際に効率的です [import](data-import.md) 価格データ。 開始する前に、テンプレートとして使用できる、書き出された階層価格データのサンプルファイルを作成します。

![ストアフロントの例 – 階層化された価格](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 手順 1：階層価格データのエクスポート

次の例では、1 つの製品の階層価格データを書き出します。 次に、書き出されたデータを、階層価格データの一括読み込みのテンプレートとして使用できます。 詳細価格データのエクスポートについて詳しくは、 [高度な価格データ](data-attributes-product.md#advanced-pricing-attributes).

![製品の階層化された価格](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. 日付： _Admin_ サイドバー、に移動  **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 次の下 _[!UICONTROL Export Settings]_、設定&#x200B;**[!UICONTROL Entity Type]**対象： `Advanced Pricing`.

1. が含まれる **[!UICONTROL Entity Attributes]** グリッドで、下にスクロールして SKU 属性を選択し、次の手順を実行します。

   - 割引率に基づく階層価格の場合、書き出す各製品の SKU をコンマで区切って入力します。

     ![データのエクスポート – 製品 SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 固定金額に基づく階層価格については、各製品の SKU を入力します。

   - 下にスクロールして、 **[!UICONTROL Continue]**.

1. Web ブラウザーのダウンロード先にあるエクスポートファイルを探して開きます。

   ![例 – 書き出された顧客グループ割引階層の価格データ](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_エクスポートされた階層価格データ_**

書き出されたデータには、次の列が含まれます。

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

書き出されたデータを、階層価格データの読み込みのテンプレートとして使用します。

## 手順 2：データを更新する

1. 必要に応じて、各製品の階層価格データを更新します。

   階層価格アップデートのない製品は、CSV ファイルから削除できます。 変更されていない製品を再インポートする必要はありません。

1. **[!UICONTROL Save]** 更新された CSV ファイル。

>[!NOTE]
>
>インポート ファイルのサイズは 2 MB 以下にする必要があります。

## 手順 3：更新したデータのインポート

1. 日付： _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 次の下 _設定を読み込み_、設定 **[!UICONTROL Entity Type]** 対象： `Advanced Pricing`.

1. を設定 **[!UICONTROL Import Behavior]** 対象： `Add/Update`.

1. 次の下 **[!UICONTROL File to Import]**&#x200B;を選択し、 **[!UICONTROL Choose File]** ディレクトリからインポートするファイルを選択します。

1. 右上隅のをクリックします。 **[!UICONTROL Check Data]**.

1. ファイルが有効な場合、 **[!UICONTROL Import]**.

   それ以外の場合は、メッセージにリストされているデータの各問題を修正し、ファイルを再度インポートしてください。
