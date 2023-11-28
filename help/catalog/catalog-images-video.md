---
title: カタログ画像とビデオ
description: デジタルメディアを使用してカタログ製品ページを拡張し、顧客に視覚的な情報を提供する方法について説明します。
exl-id: 963693d3-669b-42b3-9ac7-cdaed8bb614f
feature: Catalog Management, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# カタログ画像とビデオ

一貫した比率の高い高品質の画像を使用すると、カタログは商業的な魅力を持つプロフェッショナルな外観になります。 1 つの製品につき複数の画像を含む大規模なカタログがある場合、管理する製品画像が数千もない場合でも、数百も簡単に使用できます。 作業を開始する前に、画像ファイルの命名規則を設定し、必要に応じて元の画像を見つけるために整理します。

![製品画像](./assets/product-images-videos-swatch.png){width="600" zoomable="yes"}

単一の製品イメージは、カタログ全体で異なるサイズでレンダリングされます。 ページ上の画像コンテナの表示サイズは、テーマのスタイルシートで定義されます。 ただし、ストア内で画像が表示される場所は、画像に割り当てられている役割によって決まります。 メイン製品の画像、または _ベース_ 画像は、ズームに必要な倍率を生成できる大きさにする必要があります。 メイン画像に加えて、同じ画像の小さいバージョンが製品リストに、または買い物かごのサムネールとして表示される場合があります。 画像は、必要な最大サイズでアップロードするか、 [Adobe Stock](../content-design/adobe-stock.md) 画像を使用し、各用途に必要なサイズを Commerce でレンダリングできるようにします。 すべての役割で同じ画像を使用することも、役割ごとに異なる画像を割り当てることもできます。 デフォルトでは、アップロードされる最初の画像は 3 つの役割すべてに割り当てられます。

## ストアフロントメディアブラウザー

製品ページのメディアブラウザーには、製品に関連する複数の画像、ビデオまたはスウォッチが表示されます。 各サムネールには、製品の異なる表示やバリエーションを表示できます。 買い物客はサムネールをクリックして、メディアアセットを参照できます。 メディアブラウザーの位置はテーマによって異なりますが、デフォルトの位置は製品ページ上のメイン画像のすぐ下にあります。 アクセシビリティコントロールについては、 [ナビゲーションのアクセシビリティ](../getting-started/navigation-accessibility.md).

![ストアフロントメディアブラウザー](./assets/storefront-thumbnail-gallery.png){width="700" zoomable="yes"}

### 画像ズーム

次の場合、 [ベース画像](product-image.md) は、ズーム効果を作成するのに十分な大きさで、マウスオーバーで画像の拡大部分を表示できます。 ズームを有効にすると、ユーザーはメイン画像をクリックし、カーソルを動かして画像の様々な部分を拡大できます。 拡大された選択範囲が画像の右側に表示されます。

![画像ズーム](./assets/storefront-image-zoom.png){width="700" zoomable="yes"}

### ライトボックスとスライダ

製品イメージの表示を強化するために使用できる、多くのサードパーティ製のライトボックスとスライダーがあります。 での拡張機能を探す [Commerce Marketplace](../getting-started/commerce-marketplace.md).

## リソースのトラブルシューティング

画像とビデオの問題のトラブルシューティングについては、次のコマースサポートのナレッジベース記事を参照してください。

- [インストール後、画像とスタイルシートは読み込まれず、テキストのみが表示され、グラフィックは表示されません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/after-installing-images-and-stylesheets-do-not-load-only-text-displays-no-graphics.html)
- [REST API を介した製品画像の管理に関する問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-5/mdva-28763-magento-patch-issues-with-managing-product-images-via-rest-api.html)
- [重複する製品.csv 画像をインポート](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-31969-magento-patch-import-products-.csv-images-duplicated.html)
- [製品編集の画像の役割にもかかわらず、製品の画像は表示されません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/product-images-do-not-display-despite-product-edit-image-roles.html)
- [デプロイ後に表示されない画像を保存](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/store-images-not-displayed-after-deployment.html)
