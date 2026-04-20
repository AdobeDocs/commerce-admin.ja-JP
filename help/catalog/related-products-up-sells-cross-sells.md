---
title: 製品設定 – [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: 製品の場合、[!UICONTROL Related Products, Up-Sells, and Cross-Sells]設定は、製品ページ上の簡単なプロモーションブロックを定義し、その他の製品の選択を強調表示します。
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 837da039e03db94014056fbb4e945c47fa37b7c1
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# 製品設定 – [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

「_[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_」セクションを使用して、顧客が関心を持つ可能性のある製品の選択肢を提示するシンプルなプロモーションブロックを設定します。 詳しくは、[製品の関係](../merchandising-promotions/product-relationships.md)を参照してください。

![関連製品、アップセル、クロスセル &#x200B;](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

各ブロックは、特定のオプションに属する製品のリストで構成されます。

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL ID] | 製品エンティティに割り当てられる一意の数値識別子。 |
| [!UICONTROL Thumbnail] | 製品サムネイル画像。 |
| [!UICONTROL Name] | 製品の名前。 |
| [!UICONTROL Status] | 製品ステータスを示します。 オプション：`Enabled` / `Disabled`。 無効な製品は、フロントエンドのブロックに表示されません。 |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。 |
| [!UICONTROL SKU] | 製品に割り当てられている一意の在庫保管単位。 |
| [!UICONTROL Price] | 製品の単価。 |
| [!UICONTROL Action] | オプション：`Remove`。 ブロックから製品を削除します。 |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ） **Adobe AIを活用した商品レコメンデーション**&#x200B;は、人工知能とマシンラーニング アルゴリズムを使用して、集約された訪問者データを詳細に分析することで、商品の関係を定義するプロセスを簡素化します。 このデータをAdobe Commerceカタログと組み合わせることで、買い物客にとって魅力的で関連性の高い、パーソナライズされた体験を実現できます。
><br/>
>このAdobeで開発した拡張機能を、手動で設定した商品レコメンデーションやアップセルの代わりに使用する方法について詳しくは、_[商品レコメンデーションガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=ja)_&#x200B;を参照してください。

## 関連製品

関連商品は、お客様が閲覧している商品に加えて購入することを目的としています。 顧客はチェックボックスをクリックするだけで、ショッピングカートに商品を追加できます。 _関連製品_ ブロックの配置は、定義されたテーマとページレイアウトによって異なります。 以下の例では、_製品ビュー_ ページの下部に&#x200B;_関連製品_ ブロックが表示されています。 2列レイアウトでは、_関連製品_ ブロックが右側のサイドバーに表示されることがよくあります。

![関連製品](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

関連製品を設定するには：

1. 製品を編集モードで開きます。

1. 下にスクロールして、![&#x200B; セクションの](../assets/icon-display-expand.png)拡張セレクター&#x200B;**[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**&#x200B;を展開します。

1. **[!UICONTROL Add Related Products]**&#x200B;をクリックします。

1. [&#x200B; フィルターコントロール &#x200B;](../getting-started/admin-grid-controls.md)を使用して、必要な製品を見つけます。

1. リストで、関連製品としてフィーチャーする製品のチェックボックスを選択します。

   ![関連製品](./assets/products-related-add.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Add Selected Products]**&#x200B;をクリックします。

## アップセル

アップセル商品とは、現在検討されている商品ではなく、顧客が好む可能性のある商品のことです。 アップセルとして提供される商品は、より高品質で、より人気のある商品であったり、より優れた利益率であったりします。 アップセル商品は、商品ページの&#x200B;_などの見出しの下に表示されます。次の商品にも興味を持っている可能性があります_。

![&#x200B; アップセル &#x200B;](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

アップセル商品を選択するには：

1. 製品を編集モードで開きます。

1. 下にスクロールして、![&#x200B; セクションの](../assets/icon-display-expand.png)拡張セレクター&#x200B;**[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**&#x200B;を展開します。

1. **[!UICONTROL Add Up-Sell Products]**&#x200B;をクリックします。

1. [&#x200B; フィルターコントロール &#x200B;](../getting-started/admin-grid-controls.md)を使用して、必要な製品を見つけます。

1. リストで、アップセル商品としてフィーチャーしたい商品のチェックボックスをオンにします。

   ![製品のアップセル &#x200B;](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Add Selected Products]**&#x200B;をクリックします。

>[!NOTE]
>
>親バンドル製品は、すべての子製品に対して常にアップセル製品として自動的に表示されます。

## クロスセル

クロスセル商品は、レジのレジの隣にあるインパルス購入と似ています。 クロスセルとして提供される商品は、顧客が決済プロセスを開始する直前に、ショッピングカートページに表示されます。

>[!NOTE]
>
>ストアビューごとにクロスセル項目を表示または非表示にするには、ショッピングカートの[という](../configuration-reference/sales/checkout.md) チェックアウト/ショッピングカート _[!UICONTROL Show Cross-sell Items]_&#x200B;オプションを参照してください。 特定のセールス中にクロスセルを非表示にしたり、ストアビューでA/B テストを行ったりすることもできます。

![&#x200B; ショッピングカートでのクロスセル &#x200B;](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_クロスセル製品を選択するには:_**

1. 製品を編集モードで開きます。

1. 下にスクロールして、![&#x200B; セクションの](../assets/icon-display-expand.png)拡張セレクター&#x200B;**[!UICONTROL Related Products, Up-Sells, and Cross-Sells]**&#x200B;を展開します。

1. **[!UICONTROL Add Cross-Sell Products]**&#x200B;をクリックします。

1. [&#x200B; フィルターコントロール &#x200B;](../getting-started/admin-grid-controls.md)を使用して、必要な製品を見つけます。

1. リストで、クロスセル商品としてフィーチャーしたい商品のチェックボックスをオンにします。

   ![製品のクロスセル &#x200B;](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Add Selected Products]**&#x200B;をクリックします。
