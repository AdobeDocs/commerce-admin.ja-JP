---
title: 読み込み階層の価格
description: 価格設定データを書き出し、更新されたデータを読み込む方法について説明します。
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# 読み込み階層の価格

各製品の[階層の価格](../catalog/product-price-tier.md)を手動で入力するのではなく、価格データを[&#x200B; インポート &#x200B;](data-import.md)する方が効率的です。 始める前に、テンプレートとして使用できる、書き出された階層価格データのサンプルファイルを作成します。

![&#x200B; ストアフロントの例 – 階層制](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 手順1：階層価格データのエクスポート

次の例では、1つの製品の階層価格データを書き出します。 次に、書き出されたデータを、階層価格データの一括読み込みのテンプレートとして使用できます。 高度な価格データの書き出しについて詳しくは、[高度な価格データ &#x200B;](data-attributes-product.md#advanced-pricing-attributes)を参照してください。

![製品の階層価格](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;に移動します。

1. _[!UICONTROL Export Settings]_&#x200B;で、**[!UICONTROL Entity Type]**&#x200B;を`Advanced Pricing`に設定します。

1. **[!UICONTROL Entity Attributes]** グリッドで、SKU属性までスクロールダウンし、次の操作を行います。

   - 割引率に基づく階層価格の場合は、書き出す各製品のSKUをコンマで区切って入力します。

     ![&#x200B; データ書き出し – 製品SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 固定金額に基づく価格帯の場合は、各商品のSKUを入力します。

   - 下にスクロールして、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. Web ブラウザーのダウンロード場所でエクスポートファイルを探し、ファイルを開きます。

   ![例 – 書き出された顧客グループの割引階層価格データ &#x200B;](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_書き出された階層価格データ_**

書き出されたデータには、次の列が含まれます。

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

書き出されたデータは、階層の価格データを読み込むためのテンプレートとして使用します。

## 手順2：データの更新

1. 必要に応じて、各製品のティア価格データを更新します。

   価格が更新されていない製品は、CSV ファイルから削除できます。 変更されていない製品を再インポートする必要はありません。

1. **[!UICONTROL Save]**&#x200B;更新されたCSV ファイル。

>[!NOTE]
>
>読み込みファイルのサイズは2 MBを超えることはできません。

## 手順3：更新されたデータのインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;に移動します。

1. _設定の読み込み_&#x200B;で、**[!UICONTROL Entity Type]**&#x200B;を`Advanced Pricing`に設定します。

1. **[!UICONTROL Import Behavior]**&#x200B;を`Add/Update`に設定します。

1. **[!UICONTROL File to Import]**&#x200B;で「**[!UICONTROL Choose File]**」をクリックし、ディレクトリから読み込む準備ができたファイルを選択します。

1. 右上隅の「**[!UICONTROL Check Data]**」をクリックします。

1. ファイルが有効な場合は、**[!UICONTROL Import]**&#x200B;をクリックします。

   それ以外の場合は、メッセージにリストされているデータに関する各問題を修正し、ファイルの読み込みを再試行してください。
