---
title: 製品の作成
description: カタログに作成できる製品のタイプについて説明します。
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# 製品の作成

製品タイプの選択は、製品を作成するために最初に行う必要がある操作の 1 つです。 製品カタログの作成を開始したばかりの場合は、いくつかのサンプル製品を作成して、各製品タイプで実験することができます。 基本商品タイプに加えて、という用語 _複合生成物_ は、複数のオプションを持つ製品を参照するために使用される場合があります。例えば、様々な色やサイズの設定可能な製品などです。

>[!NOTE]
>
>詳しくは、カタログを参照してください。 [ナビゲーション](navigation.md)、設定方法 [カテゴリ](categories.md) および [属性](product-attributes.md)、およびカタログ [URL オプション](catalog-urls.md) 使用可能です。 これらの概念を理解したら、多くの製品をカタログに効率的に追加するには、次の操作を行います [import](../systems/data-import.md) CSV ファイルからのオファー

![ストアフロントの製品ページ](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## 製品タイプ

**[シンプル製品](product-create-simple.md)**  – 単純な製品とは、単一の SKU を持つ物理的なアイテムのことです。 シンプルな製品には、さまざまな価格と入力制御があり、製品のバリエーションを販売することができます。 シンプルな製品は、グループ化された製品、バンドルされた製品、設定可能な製品と関連付けて使用できます。

**[設定可能な製品](product-create-configurable.md)**  – 設定可能な製品は、各バリエーションのオプションのリストを含む単一の製品のように見えます。 ただし、各オプションは、個別の SKU を持つ個別のシンプルな製品を表しているので、各バリエーションの在庫を追跡できます。

**[グループ化された製品](product-create-grouped.md)** - グループ化された製品は、複数のスタンドアロン製品をグループとして表します。 単一の製品のバリエーションをオファーしたり、プロモーション用にグループ化したりできます。 製品は個別に購入することも、グループとして購入することもできます。

**[バーチャル製品](product-create-virtual.md)**  – 仮想製品は具体的な製品ではなく、通常、サービス、メンバーシップ、保証、サブスクリプションなどの製品に使用されます。 仮想製品は、グループ化された製品やバンドル製品と関連付けて使用できます。

**[バンドル製品](product-create-bundle.md)**  - バンドル製品を使用すると、お客様はさまざまなオプションから「独自に構築」できます。 バンドルには、ギフトバスケットやコンピューターなど、カスタマイズ可能なすべてのものを使用できます。 バンドル内の各項目は、個別のスタンドアロン製品です。

**[ダウンロード可能な製品](product-create-downloadable.md)** - ダウンロードされる 1 つ以上のファイルで構成される、デジタル ダウンロード可能な製品。 ファイルは、サーバー上に存在することも、他のサーバーへの URL として提供することもできます。

**[ギフトカード](product-gift-card-create.md)** - （[Adobe Commerce](../landing/home.md#product-editions) のみ）ギフトカードには 3 種類あります。 _仮想_ ギフトカードは電子メールで送信されます。 _物理_ ギフトカードは受取人に出荷されます。 _組み合わせ_ 仮想と物理の組み合わせであるギフトカード。 それぞれに一意のコードがあり、チェックアウト時に引き換えられます。 ギフトカードは、グループ化された製品に含めることもできます。

## 製品設定

最も頻繁に使用される製品設定および属性がページ上部に表示され、その後にカスタム属性が表示されます。 その他の製品設定は、ページ下部の展開可能なセクションにあります。

![製品設定](./assets/product-settings.png){width="600" zoomable="yes"}

| 設定 | 説明 |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | （条件 [[!DNL Inventory Management]](../inventory-management/introduction.md) 有効）製品を配布できるソースを一覧表示します。 |
| [[!UICONTROL Content]](product-content.md) | ストアフロントの製品ページに表示されるメインの製品説明を入力および編集するために使用されます。 |
| [[!UICONTROL Configurations]](product-configurations.md) | 製品の既存のバリエーションを一覧表示します。設定可能な製品タイプで使用するバリエーションの生成に使用できます。 |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | 顧客が商品に対して送信したすべてのレビューをリストします。 |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | 製品のインデックスを作成するために検索エンジンで使用される URL キーおよびメタデータフィールドを指定します。 |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | 顧客が興味を持つ可能性のある追加の製品の選択を提示する簡単なプロモーションブロックをストアフロントに設定するために使用します。 |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | 製品にカスタマイズ可能なオプションを追加します。 |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | ストア階層に従って、製品が使用可能な各 web サイトを識別します。 |
| [[!UICONTROL Design]](settings-advanced-design.md) | 製品ページに異なるテーマを適用したり、列のレイアウトを変更したり、製品オプションの表示場所を決定したり、カスタム XML コードを入力したりするために使用します。 |
| [[!UICONTROL Gift options]](product-gift-options.md) | 商品レベルでのチェックアウト中にギフトメッセージオプションを有効または無効にするために使用します。 |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) （で利用可能 [Adobe Commerce B2B](../b2b/introduction.md) のみ）を使用すると、異なる会社のカスタム価格で共有カタログを管理できます。 |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | 製品ダウンロードのパラメーターを定義するために使用されます。 |

{style="table-layout:auto"}

## 高度な価格設定と在庫

詳細な価格設定および在庫設定にアクセスするには、下のリンクをクリックしてください **[!UICONTROL Price]** および **[!UICONTROL Quantity]**. 詳しくは、を参照してください [価格設定の管理](pricing-advanced.md) および [Inventory management](../inventory-management/introduction.md).
