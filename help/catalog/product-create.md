---
title: 製品の作成
description: カタログに作成できる製品のタイプについて説明します。
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 0%

---

# 製品の作成

商品タイプの選択は、商品の作成に最初に行う必要がある操作の 1 つです。 製品カタログの作成を開始したばかりの場合は、サンプル製品をいくつか作成して、各製品タイプを試すことができます。 基本的な製品タイプに加えて、「 _複合製品_ は、様々な色やサイズで使用できる設定可能な製品など、複数のオプションを持つ製品を指す場合に使用されます。

>[!NOTE]
>
>詳しくは、カタログを参照してください。 [ナビゲーション](navigation.md)、設定方法 [カテゴリ](categories.md) および [属性](product-attributes.md)、およびカタログ [URL オプション](catalog-urls.md) 使用可能な これらの概念を理解したら、多くの製品をカタログに追加する最も効率的な方法は、次のとおりです。 [インポート](../systems/data-import.md) CSV ファイルから取得します。

![ストアフロントの製品ページ](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## 製品タイプ

**[シンプルな製品](product-create-simple.md)**  — シンプルな製品は、単一の SKU を持つ物理的な品目です。 シンプルな製品は、製品のバリエーションを販売できるように、様々な価格と入力制御を備えています。 シンプルな製品は、グループ化、バンドル、設定可能な製品と関連付けて使用できます。

**[設定可能な製品](product-create-configurable.md)**  — 設定可能な製品は、各バリエーションのオプションのリストを含む単一の製品と見なされます。 ただし、各オプションは個別のシンプルな製品と個別の SKU を表し、これにより各バリエーションの在庫を追跡できます。

**[グループ化された製品](product-create-grouped.md)**  — グループ化された製品は、複数のスタンドアロン製品をグループとして表示します。 単一のプロダクトのバリエーションをオファーしたり、プロモーション用にグループ化したりできます。 製品は、個別に、またはグループとして購入できます。

**[仮想製品](product-create-virtual.md)**  — 仮想製品は有形製品ではなく、通常、サービス、メンバーシップ、保証、購読などの製品に使用されます。 仮想製品は、グループ化された製品やバンドル製品と関連付けて使用できます。

**[バンドル製品](product-create-bundle.md)**   — バンドル製品を使用すると、顧客は様々なオプションから「独自の」を構築できます。 バンドルは、ギフトバスケット、コンピューター、またはカスタマイズ可能なその他の任意のものにすることができます。 バンドル内の各アイテムは、個別のスタンドアロン製品です。

**[ダウンロード可能な製品](product-create-downloadable.md)**  — デジタルダウンロード可能な製品は、ダウンロードされる 1 つ以上のファイルで構成されます。 ファイルは、サーバー上に配置することも、他のサーバーへの URL として提供することもできます。

**[ギフトカード](product-gift-card-create.md)** - ([Adobe Commerce](../landing/home.md#product-editions) )3 種類のギフトカードがあります。 _仮想_ ギフトカードは e メールで送信されます。 _物理_ ギフトカードが受信者に発送されます。 _組み合わせ_ 仮想カードと物理カードを組み合わせたギフトカード。 それぞれに一意のコードが含まれ、チェックアウト時に引き換えられます。 グループ化された製品にはギフトカードを含めることもできます。

## 製品設定

最も頻繁に使用される製品設定と属性がページの上部に表示され、その後にカスタム属性が表示されます。 その他の製品設定は、ページの下部にある展開可能なセクションに表示されます。

![製品設定](./assets/product-settings.png){width="600" zoomable="yes"}

| 設定 | 説明 |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (When [[!DNL Inventory Management]](../inventory-management/introduction.md) が有効 ) 製品を配布するソースをリストします。 |
| [[!UICONTROL Content]](product-content.md) | ストアフロント製品ページに表示されるメイン製品の説明を入力および編集するために使用します。 |
| [[!UICONTROL Configurations]](product-configurations.md) | プロダクトの既存のバリエーションをリストし、設定可能なプロダクトタイプで使用するバリエーションを生成するために使用できます。 |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | 顧客が製品に対して送信したすべてのレビューを一覧表示します。 |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | 検索エンジンで製品のインデックスを作成する際に使用される「 URL キー」フィールドと「メタデータ」フィールドを指定します。 |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | ストアフロントにシンプルなプロモーションブロックを設定し、顧客が興味を持つ可能性のある追加の製品の選択を示すのに使用します。 |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | カスタマイズ可能なオプションを製品に追加します。 |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | ストア階層に従って、製品が利用可能な各 Web サイトを識別します。 |
| [[!UICONTROL Design]](settings-advanced-design.md) | 製品ページに別のテーマを適用し、列のレイアウトを変更し、製品オプションを表示する場所を決定し、カスタム XML コードを入力するために使用します。 |
| [[!UICONTROL Gift options]](product-gift-options.md) | 製品レベルでのチェックアウト時にギフトメッセージオプションを有効または無効にするために使用します。 |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce用 B2B](../assets/b2b.svg) （で使用可能） [Adobe Commerce用 B2B](../b2b/introduction.md) （のみ）異なる会社のカスタム価格で共有カタログを維持する機能を有効にします。 |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | 製品ダウンロードのパラメーターの定義に使用されます。 |

{style="table-layout:auto"}

## 高度な価格と在庫

高度な価格設定と在庫設定にアクセスするには、以下のリンクをクリックしてください **[!UICONTROL Price]** および **[!UICONTROL Quantity]**. 詳しくは、 [価格の管理](pricing-advanced.md) および [Inventory management](../inventory-management/introduction.md).
