---
title: 製品レビュー
description: 製品レビューで店舗を強化し、製品の信頼性を高める方法を説明します。
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 製品レビュー

製品レビューはコミュニティの感覚を構築するのに役立ち、広告のお金が買うことができるよりも信頼できると考えられています。 実際、一部の検索エンジンでは、製品レビューのあるサイトのランキングがそうでないサイトよりも高くなっています。 特定の製品を検索してサイトを見つけたユーザーにとって、製品レビューは基本的にストアのランディングページです。 製品レビューは、顧客が店舗を見つけ、顧客の関心を維持し、多くの場合、販売につなげるのに役立ちます。

Commerceには、管理者から管理できるネイティブの製品レビュー機能が含まれています。 から拡張機能を使用することもできます [Commerce Marketplace](../getting-started/commerce-marketplace.md) ホステッド・レビュー管理システムを使用する。

>[!NOTE]
>
>Adobe CommerceおよびMagento Open Sourceリリース 2.4.0 から 2.4.3 には、Yotpo ベンダーが開発した拡張機能が含まれています。 2.4.4 リリース以降、このCommerce Marketplaceはコアリリースにバンドルされなくなり、拡張機能からインストールおよび更新する必要があります。 また、Marketplace では、拡張機能開発者が提供する最新のドキュメントにもアクセスできます。
><br><br>
>バンドルされた拡張機能を有効にして設定してある場合は、2.4.4 のアップグレードプロセスの一環として composer.json ファイルを更新し、今後、拡張機能の更新を管理する必要があります。 参照： [アップグレードモジュール](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) が含まれる _アップグレードガイド_ を参照してください。

## ストアフロントでの商品レビュー

ネイティブの製品レビュー機能が有効になっている場合、顧客はカタログ内の任意の製品のレビューを記述できます。 レビューは、以下をクリックして製品ページから書き込むことができます。

- **レビューを追加** 既存のレビューがある製品の場合。

- **この製品を初めて確認する** レビューが存在しない製品の場合。

この [!UICONTROL Reviews] タブには、現在のすべてのレビューと、レビューの送信に使用されたフォームが一覧表示されます。

設定によって、顧客が商品レビューを書く前にストアでアカウントを開く必要があるか、または顧客がレビューをゲストとして送信できるかどうかを決定します。 レビュー担当者にアカウントのオープンを要求すると、匿名の送信が防止され、レビューの品質が向上します。

![ストアフロントの例 – レビューの追加](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

星の数は、製品の満足度評価を示します。 訪問者は、リンクをクリックしてレビューを読み、自分で書くことができます。 インセンティブとして、お客様はレビューを送信する際に報酬ポイントを受け取ることができます。 レビューが送信されると、管理者に送信され、モデレートされます。 承認されると、レビューがストアに公開されます。

![ストアフロントの例 – 「レビュー」タブ](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

この _[!UICONTROL My Product Reviews]_顧客アカウントダッシュボードの「」セクションには、顧客が送信し、公開用に承認されたすべてのレビューが一覧表示されます。 各レビューの概要には、レビューが送信された日付、製品ページへのリンク、レビューの詳細が含まれます。

![マイ製品レビュー](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. アカウントのサイドバーで、顧客が次を選択します **[!UICONTROL My Product Reviews]**.

1. レビュー全体を表示するには、をクリックします **[!UICONTROL See Details]**.

   ![詳細を確認](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## 製品レビュー機能の有効化

Commerceの製品レビュー機能は、デフォルトで有効になっています。

>[!NOTE]
>
>これらのフィールドを次のように設定します `No` Commerce製品レビューを無効にするには、 **システム値を使用** チェックボックス。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択して、 **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Product Reviews]** セクション。

   ![カタログの設定 – Commerce製品レビュー](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

   これは、製品レビューを有効にするデフォルト設定です。

1. を設定 **[!UICONTROL Allow Guests to Write Reviews]** 対象： `Yes`.

   これは、顧客が商品レビューを書くことができるように、ストアでアカウントを開く必要があるかどうかを決定するデフォルトの設定です。

1. 完了したら、 **[!UICONTROL Save Config]**.

## カスタム評価の作成

Commerce商品レビューを使用すると、お客様は商品レビューを送信する際に評価を割り当てることができます。 デフォルトの評価は、品質、価格、値です。 これらに加えて、独自のカスタム評価を追加できます。 カタログページに表示される 5 つ星の評価は、各製品の平均です。

![ストアフロントの例 – カスタム評価](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Rating]**.

   ![Admin - Ratings](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. が含まれる _[!UICONTROL Rating Title]_「」セクションに、**[!UICONTROL Default Value]**新しい評価に使用します。

   該当する場合は、各ストア表示の翻訳も入力します。

   ![評価タイトルの設定](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. が含まれる _評価の表示_ セクション、設定 **[!UICONTROL Visibility In]** 評価を使用するストア表示に移動します。

   複数のストアビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

   >[!NOTE]
   >
   >評価は、ストア表示に割り当てられていない限り、表示されません。

1. の場合 **[!UICONTROL Sort Order]**&#x200B;を入力します。この評価の順序を決定するための数値が他のユーザーとリストされます。

1. ストアフロントに評価を表示する場合は、 **[!UICONTROL Is Active]** チェックボックス。

   ![評価の表示設定](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Rating]**.

   すべてのレビューの平均評価は、カタログの製品グリッドページに製品ごとに表示されます。

   ![カタログページ](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
