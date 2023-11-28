---
title: 製品設定 — [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: 製品の場合、 [!UICONTROL Related Products, Up-Sells, and Cross-Sells] 設定は、製品ページで、追加の製品の選択を強調表示する単純なプロモーションブロックを定義します。
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 製品設定 — [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

以下を使用します。 _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_」セクションを使用して、お客様が興味を持つ可能性のある追加製品の選択を提示するシンプルなプロモーションブロックを設定します。 詳しくは、 [製品の関係](../merchandising-promotions/product-relationships.md).

![関連製品、アップセルおよびクロスセル](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

各ブロックは、特定のオプションに属する製品のリストで構成されます。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 製品エンティティに割り当てられる一意の数値識別子。 |
| [!UICONTROL Thumbnail] | 製品のサムネール画像。 |
| [!UICONTROL Name] | 製品の名前。 |
| [!UICONTROL Status] | 製品のステータスを示します。 オプション： `Enabled` / `Disabled`. 障害のある製品は、フロントエンドのブロックには表示されません。 |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。 |
| [!UICONTROL SKU] | 製品に割り当てられる一意の在庫管理単位。 |
| [!UICONTROL Price] | 製品の単価。 |
| [!UICONTROL Action] | オプション： `Remove`. ブロックから商品を削除します。 |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) **Adobe Senseiを活用した製品Recommendations** は、人工知能と機械学習アルゴリズムを使用して集計された訪問者データの深い分析を実行することで、製品の関係を定義するプロセスを簡略化します。 このデータをAdobe Commerceカタログと組み合わせると、買い物客のエクスペリエンスを非常に魅力的で関連性が高く、パーソナライズされたデータにすることができます。
><br/>
>このAdobeで開発した拡張機能を、手動で設定した製品のレコメンデーションやアップセルの代わりに使用する方法について詳しくは、 _[製品Recommendationsガイド](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## 関連製品

顧客が閲覧している品目に加えて、関連製品も購入することを意図しています。 顧客は、チェックボックスをクリックするだけで、買い物かごに品目を配置できます。 の配置 _関連製品_ ブロックは、定義されたテーマとページのレイアウトに応じて異なります。 次の例では、 _関連製品_ ブロックが _製品表示_ ページに貼り付けます。 2 列レイアウトの場合、 _関連製品_ ブロックは、右側のサイドバーに表示されることがよくあります。

![関連製品](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

関連製品を設定する手順は、次のとおりです。

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** 」セクションに入力します。

1. クリック **[!UICONTROL Add Related Products]**.

1. 以下を使用します。 [フィルターコントロール](../getting-started/admin-grid-controls.md) をクリックして、必要な製品を検索します。

1. リストで、関連製品として機能させる製品のチェックボックスを選択します。

   ![関連製品](./assets/products-related-add.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Add Selected Products]**.

## アップセル

アップセル製品とは、顧客が現在検討中の製品の代わりに好む可能性のある品目です。 アップセルとして提供される品目は、より高い品質、より人気がある、またはより良い利益率を持つ可能性があります。 アップセル製品は、製品ページの「 _次の製品にも興味がある場合があります。_.

![アップセル](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

アップセル製品を選択する手順は、次のとおりです。

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** 」セクションに入力します。

1. クリック **[!UICONTROL Add Up-Sell Products]**.

1. 以下を使用します。 [フィルターコントロール](../getting-started/admin-grid-controls.md) をクリックして、必要な製品を検索します。

1. リストで、アップセル製品として機能させる製品のチェックボックスを選択します。

   ![アップセル製品](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Add Selected Products]**.

## クロスセル

クロス販売品目は、チェックアウトラインのキャッシュレジスタの横に配置されるインパルス購入に似ています。 クロス販売として提供された製品は、顧客がチェックアウトプロセスを開始する直前に、買い物かごページに表示されます。

>[!NOTE]
>
>ストア表示ごとのクロス販売品目の表示/非表示を切り替えるには、 [チェックアウト/買い物かご](../configuration-reference/sales/checkout.md) オプション： _[!UICONTROL Show Cross-sell Items]_」と入力します。 特定の販売中またはストア表示での A/B テスト中にクロス販売を非表示にすることができます。

![買い物かごでのクロス販売](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_クロス販売製品を選択する手順は、次のとおりです。_**

1. 製品を編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** 」セクションに入力します。

1. クリック **[!UICONTROL Add Cross-Sell Products]**.

1. 以下を使用します。 [フィルターコントロール](../getting-started/admin-grid-controls.md) をクリックして、必要な製品を検索します。

1. リストで、クロス販売製品として特集する製品のチェックボックスを選択します。

   ![クロスセル製品](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Add Selected Products]**.
