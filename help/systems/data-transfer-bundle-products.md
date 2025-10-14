---
title: バンドル製品の読み込み
description: バンドル製品の製品データの読み込み例を確認します。
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# バンドル製品の読み込み

バンドル製品には様々な商品が表示され、顧客は購入する商品を選択できます。 バンドルを構成するすべての項目は、カタログ内に [&#x200B; シンプル製品 &#x200B;](../catalog/product-create-simple.md) または [&#x200B; 仮想製品 &#x200B;](../catalog/product-create-virtual.md) として存在します。 通常、バンドル製品は管理者が作成および更新します。 ただし、データを読み込んでバンドル製品を作成したり、既存のバンドル製品を書き出してデータを編集し、カタログに読み込むこともできます。 Sprite Yoga Companion Kit は、次の例で使用されるサンプルデータのバンドル製品です。

![&#x200B; バンドル製品 &#x200B;](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## バンドル項目の順序の変更

バンドル製品内の項目の順序を変更する方法は 2 つあります。

### 方法 1：ドラッグ&amp;ドロップ

管理者から [&#x200B; バンドル &#x200B;](../catalog/product-create-bundle.md) 製品を操作する際に、項目とセクションを任意の位置にドラッグ&amp;ドロップできます。

![&#x200B; バンドル項目 &#x200B;](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 方法 2：製品データを編集する

バンドル製品の構造を理解する最善の方法は、製品を書き出し、スプレッドシートでデータを調べることです。 バンドル項目の順序を変更するには、製品をエクスポートし、各項目のデータに位置パラメーターを追加します。 項目データは、書き出された商品の `bundle_values` 列に表示されます。 スプレッドシートで開くと、製品に関連付けられているすべての項目が、長い文字列として 1 つのセルに含まれます。 `bundle_values` の列には、各項目に関する次の要素が含まれます。

- 項目セクションの名前
- 入力制御
- 必須項目指標
- SKU
- カラー
- 価格
- デフォルトのオプションインジケーター
- 既定の数量
- 価格タイプ
- 編集可能な数量インジケーター

#### 手順 1：バンドル製品のエクスポート

このステップでは、Sprite Yoga Companion Kit が（[CSV](data-csv.md) ファイルとしてエクスポートされます。 カタログに含まれている他のバンドル製品を使用できます。

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Export]**&#x200B;に移動します。

1. _書き出し設定_ で、**[!UICONTROL Entity Type]** を `Products` に設定します。

1. 製品属性のリストで、**[!UICONTROL SKU]** まで下にスクロールし、書き出すバンドル製品の SKU を入力します。

   この例では、製品の SKU は `24-WG080` です。

1. セクションの下部までスクロール ダウンし、[**[!UICONTROL Continue]**] をクリックします。

1. _[!UICONTROL File name]_&#x200B;グリッドの&#x200B;_[!UICONTROL Action]_ 列で「**[!UICONTROL Select]**」をクリックし、「`Download`」を選択します。

   ファイルは、ブラウザーが使用するダウンロード場所に表示されます。

#### 手順 2：データを編集する

1. ダウンロードした CSV ファイルをスプレッドシートで開きます。

1. `bundle_values` の列が表示されるまで、右端までスクロールします。

   `bundle_values` データでは、各要素はコンマで区切られ、各バンドル項目は次の項目から縦棒で区切られています。 （最後の項目が縦棒で終わらない。） 書き出されたバンドルデータは、次の例のようになります。

   ![&#x200B; バンドル値 &#x200B;](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 編集を簡単にするために、`bundle_values` のデータをコピーしてテキストエディターに貼り付け、各項目の後ろに改行を追加して、各項目が別々の行に表示されるようにすることができます。

1. データを編集した後、改行を慎重に削除し、編集したデータを `bundle_values` の列に貼り付けます。

   次の図では、ストアリスト内の項目の順序を変更するために、各ヨガストラップに `position=[number]` パラメーターを追加しています。

   ![&#x200B; 位置パラメータ &#x200B;](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. データを編集した後、CSV ファイルを **[!UICONTROL Save]** きます。

#### 手順 3：更新された製品のインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Import]**&#x200B;に移動します。

1. _[!UICONTROL Import Settings]_&#x200B;で、**[!UICONTROL Entity Type]**&#x200B;を `Products` に設定します。

1. **[!UICONTROL Import Behavior]** を `Replace` に設定します。

   このオプションを選択すると、変更内容が追加の項目として追加されるのではなく、バンドル製品の以前のデータが上書きされます。

1. 「インポートするファイル _セクションまでスクロールダウンし_ 「イン **[!UICONTROL Choose File]** ート」をクリックします。

1. 編集した CSV ファイルを選択します。

1. 「**[!UICONTROL Check Data]**」をクリックして、データがチェックされるまで少し待ちます。

1. ファイルが有効な場合は、[**[!UICONTROL Import]**] をクリックします。

1. 処理が完了したら、**[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Cache Management]**&#x200B;に移動し、「**[!UICONTROL Flush Cache Storage]**」をクリックします。

   これにより、更新された製品がストアフロントですぐに使用できるようになります。
