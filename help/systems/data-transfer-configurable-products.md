---
title: 設定可能な製品のインポート
description: 設定可能な商品の商品データの読み込み例を確認してください。
exl-id: bb8b2a6d-867e-4ab2-bdfd-98a01d79c457
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# 設定可能な製品のインポート

設定可能な商品データの構造を理解する最善の方法は、設定可能な商品とそのバリエーションを書き出し、スプレッドシートでデータを調べることです。

次の例では、新しいサイズの商品バリエーションのセットを各カラーに追加します。 まず、設定可能なプロダクトをエクスポートして、データ構造を調べます。 次に、データを更新し、カタログに読み込みます。 データの書き出しの演習を行わない場合は、例で使用されている CSV ファイルをダウンロードできます。

![ ストアフロントの例 – サイズ属性とカラー属性 ](./assets/storefront-hoodie-new-size.png){width="700" zoomable="yes"}

## 手順 1：属性の設定と値を確認する

1. 開始する前に、製品バリエーションに使用される属性に、必要なプロパティ設定があることを確認します。

   - [**[!UICONTROL Scope]**](../getting-started/websites-stores-views.md#scope-settings) - `Global`
   - [**[!UICONTROL Catalog Input Type for Store Owner]**](data-attributes-product.md) – 製品バリエーションに使用する属性の入力タイプは、次のいずれかである必要があります。

      - `Dropdown`
      - `Visual Swatch`
      - `Text Swatch`
      - `Multi-Select`

   - **[!UICONTROL Values Required]** - `Yes`

1. サイズや色を追加する場合や、既存の属性に他の変更を加える場合は、必ず新しい値で属性を更新してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**に移動します。

1. リストで属性を見つけ、編集モードで開きます。

1. 新しい値を属性に追加します。

   次の例では、新しいサイズがテキストスウォッチに追加されます。

   ![ 製品属性 – 新しい値を追加 ](./assets/data-transfer-configurable-product-add-new-attribute-value.png){width="500" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

1. 属性を追加する場合は、開始する前に、指示に従って [ 属性を作成 ](../catalog/attribute-product-create.md) します。

## 手順 2：設定可能な商品のエクスポート

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 書き出す設定可能な製品を見つけます。

   - 「**[!UICONTROL Filters]**」をクリックします。
   - **[!UICONTROL Type]** を `Configurable Product` に設定し、「**[!UICONTROL Apply Filters]**」をクリックします。
   - テスト書き出しに使用する設定可能な製品を選択し、**[!UICONTROL SKU]** をメモします。

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Export]**に移動します。

   ![ データ書き出し設定 ](./assets/data-transfer-export-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Export Setting]s_ で次の操作を行います。

   - **[!UICONTROL Entity Type]** を `Products` に設定します。

   - **[!UICONTROL Export File Format]** を `CSV` に設定します。

1. _[!UICONTROL Entity Attributes]_の下で、下にスクロールするか、属性ラベルフィルターを使用して&#x200B;**[!UICONTROL SKU]**属性を見つけて、次の操作を行います。

   - 書き出すために選択した設定可能な商品の SKU を入力し、「**[!UICONTROL Continue]**」をクリックします。

     ![ データ書き出し SKU](./assets/data-transfer-export-sku.png){width="600" zoomable="yes"}

   - Web ブラウザーのダウンロード場所でファイルを探し、スプレッドシートとして開きます。

     CSV ファイルには、シンプルな製品バリエーションごとに別々の行と、設定可能な製品ごとに 1 つの行があります。 `product_type column` の図は、1 つの設定可能な製品に関連付けられた複数のシンプルな製品バリエーションを示しています。

     ![ サンプルデータ – バリエーションを持つ設定可能な製品 ](./assets/data-transfer-csv-configurable-product.png){width="600" zoomable="yes"}

   - ワークシートの右端までスクロールして、次の列を探します。

      - `configurable_variations` – 設定可能な商品レコードと各バリエーションの間の 1 対多の関係を定義します。
      - `configurable_variation_labels` – 各バリエーションを識別するラベルを定義します。

     この例では、データは CG 列および CH 列にあります。 バリエーションの数によっては、`configurable_variations` 列内のデータの文字列が長くなる場合があります。 データは、関連する製品バリエーションへのインデックスとして使用されます。このデータの構造は以下のとおりです。

     ```text
     sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}| sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}
     ```

     各 SKU はパイプ記号（|）で区切られ、属性はコンマで区切られます。 各属性の値は、属性ラベルではなく属性コードで表されます。 実際のデータは次のように表示されます。

     ```text
     sku=MH01-XS-Black,size=XS,color=Black|sku=MH01-XS-Gray,size=XS,color=Gray|sku=MH01-XS-Orange,size=XS,color=Orange</pre>
     ```

1. 設定可能なプロダクトデータの構造を理解したら、データを編集したり、新しいバリエーションを CSV ファイルに直接追加したりできます。

   詳しくは、[ 複雑なデータ ](data-attributes-product.md#complex-product-data-attributes) を参照してください。

## 手順 3：データの編集

次の例では、XL サイズのセットをコピーしてワークシートに貼り付け、各色で新しいサイズの製品バリエーションのセットを作成します。

1. 新製品のテンプレートとして使用する製品バリエーションのセットをコピーします。

   ![ 書き出されたデータ – 製品バリエーションのコピー ](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. コピーした行レコードをワークシートに挿入します。

   これで、シンプルな製品バリエーションの同一のセットが 2 つ作成されました。

   ![CSV データ – 製品バリエーションの追加 ](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. 必要に応じて、新しいバリエーションの次の列のデータを更新します。

   - `sku`
   - `name`
   - `url_key`
   - `additional_attributes`

   この例では、すべての `XL` 参照が `XXL` に変更されます。

1. 新しいバリエーションが設定可能な製品の一部として含まれるように、設定可能な製品レコードの「`product_variations`」列の情報を更新します。

   設定可能な製品レコードがある行で、`product_variations` データを含むセルをクリックします。 次に、式バーで、パイプ記号から始まる最後のパラメータ セットをコピーします。

   ![product_variations data](./assets/data-transfer-export-configurable-product-product-variations-data.png){width="600" zoomable="yes"}

1. パラメーターをデータの最後に貼り付け、新しいバリエーションに必要に応じて編集します。

   この例では、`sku` パラメーターと `size` パラメーターが新しい XXL サイズに更新されます。

1. データをカタログにインポートする前に、変更されていない行を削除します。

   この例では、新しいサイズの 3 つの新しいバリエーションと、更新された設定可能な製品を含む行のみがカタログに読み込まれます。 その他の行は、CSV ファイルから削除できます。 ただし、列ラベル付きのヘッダー行は削除しないでください。

   ![ 読み込む CSV データ ](./assets/data-transfer-csv-configurable-product-data-ready-to-import.png){width="600" zoomable="yes"}

1. CSV ファイルを **[!UICONTROL Save]** きます。

   データをカタログにインポートする準備が整いました。

   >[!NOTE]
   >
   >インポート ファイルのサイズは 2 MB 以下にする必要があります。

## 手順 4：更新したデータのインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Import]**に移動します。

1. _[!UICONTROL Import Settings]_で、**[!UICONTROL Entity Type]**を `Products` に設定します。

1. _[!UICONTROL Import Behavior]_で、**[!UICONTROL Import Behavior]**を `Add/Update` に設定します。

   ![ データの読み込み動作 ](./assets/data-transfer-configurable-product-import-behavior.png){width="600" zoomable="yes"}

1. _[!UICONTROL File to Import]_の下で「**[!UICONTROL Choose File]**」をクリックし、読み込み用に準備した CSV ファイルに移動して、ファイルを選択します。

   ![ データインポートファイル ](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Check Data]**」をクリックします。

1. ファイルが有効な場合は、[**[!UICONTROL Import]**] をクリックします。

   それ以外の場合は、データで見つかった問題を修正して、もう一度試してください。

   ![ システムメッセージ – ファイルは有効です ](./assets/data-transfer-configurable-product-import-validation-results.png){width="600" zoomable="yes"}

1. 読み込みが完了したら、ページ上部のメッセージで「**[!UICONTROL Cache Management]**」をクリックし、無効なキャッシュをすべて更新します。

   新しい製品バリエーションが、管理者からのカタログとストアフロントで使用できるようになりました。 この例では、パーカーはすべての色でサイズ XXL で使用できます。
