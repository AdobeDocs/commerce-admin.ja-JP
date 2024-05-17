---
title: カタログの画像とビデオ
description: デジタルメディアを使用してカタログ製品ページを強化し、顧客にビジュアルを提供する方法を説明します。
exl-id: 963693d3-669b-42b3-9ac7-cdaed8bb614f
feature: Catalog Management, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---

# カタログの画像とビデオ

一定の割合で高品質の画像を使用すると、カタログが商業的な魅力を持つプロフェッショナルな外観になります。 1 つの製品に複数の画像が含まれる大きなカタログがある場合、管理する製品画像は数千とは言わないまでも、数百個にすることが簡単にできます。 始める前に、画像ファイルの命名規則を確立し、必要に応じてオリジナルを見つけられるように整理します。

![製品画像](./assets/product-images-videos-swatch.png){width="600" zoomable="yes"}

1 つの製品画像が、カタログ全体で異なるサイズでレンダリングされます。 ページ上の画像コンテナの表示サイズは、テーマのスタイルシートで定義します。 ただし、ストア内の画像の表示場所は、画像に割り当てられた役割によって決まります。 メインの商品画像、 _ベース_ 画像は、ズームに必要な倍率を生成するのに十分な大きさにする必要があります。 メイン画像に加えて、同じ画像の小さなバージョンが製品一覧に表示されたり、買い物かごにサムネールとして表示されたりする場合があります。 必要に応じて最大サイズの画像をアップロードすることも、 [Adobe Stock](../content-design/adobe-stock.md) 画像を生成し、Commerceで各用途に必要なサイズをレンダリングできるようにします。 すべての役割に同じ画像を使用することも、各役割に異なる画像を割り当てることもできます。 デフォルトでは、アップロードされた最初の画像が 3 つの役割すべてに割り当てられます。

## ストアフロントメディアブラウザー

製品ページのメディアブラウザーには、製品に関連する複数の画像、ビデオ、スウォッチが表示されます。 各サムネールで、製品の異なるビューやバリエーションを表示できます。 買い物客は、サムネールをクリックして、メディアアセットを参照できます。 メディアブラウザーの位置はテーマによって異なりますが、デフォルトの位置は製品ページのメイン画像のすぐ下です。 アクセシビリティコントロールについては、を参照してください [ナビゲーションのアクセシビリティ](../getting-started/navigation-accessibility.md).

![ストアフロントメディアブラウザー](./assets/storefront-thumbnail-gallery.png){width="700" zoomable="yes"}

### 画像のズーム

次の場合 [ベース画像](product-image.md) はズーム効果を作成するのに十分な大きさです。ユーザーはマウスポインターを置くと、画像の拡大部分を表示できます。 ズームが有効な場合、ユーザーはメイン画像をクリックし、カーソルを動かして画像の様々な部分を拡大できます。 拡大された選択が画像の右側に表示されます。

![画像のズーム](./assets/storefront-image-zoom.png){width="700" zoomable="yes"}

### ライトボックスとスライダー

製品画像のプレゼンテーションを向上させるために使用できるサードパーティのライトボックスやスライダーが多数あります。 で拡張機能を探します [Commerce Marketplace](../getting-started/commerce-marketplace.md).

## リソースのトラブルシューティング

画像とビデオの問題のトラブルシューティングについて詳しくは、Commerce サポートナレッジベースの次の記事を参照してください。

- [インストール後、イメージとスタイル シートはロードされず、テキストのみが表示され、グラフィックスは表示されません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/after-installing-images-and-stylesheets-do-not-load-only-text-displays-no-graphics.html)
- [REST API を使用した製品画像の管理に関する問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-5/mdva-28763-magento-patch-issues-with-managing-product-images-via-rest-api.html)
- [製品の.csv 画像の読み込みが複製されました](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-31969-magento-patch-import-products-.csv-images-duplicated.html)
- [製品編集画像の役割にもかかわらず、製品画像が表示されない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/product-images-do-not-display-despite-product-edit-image-roles.html)
- [デプロイメント後に表示されない画像の保存](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/store-images-not-displayed-after-deployment.html)
