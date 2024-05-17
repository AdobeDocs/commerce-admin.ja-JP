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

バンドル製品には様々な商品が表示され、顧客は購入する商品を選択できます。 バンドルを構成するすべての項目は、次のいずれかとしてカタログに存在します [シンプル製品](../catalog/product-create-simple.md) または [バーチャル製品](../catalog/product-create-virtual.md). 通常、バンドル製品は管理者が作成および更新します。 ただし、データを読み込んでバンドル製品を作成したり、既存のバンドル製品を書き出してデータを編集し、カタログに読み込むこともできます。 Sprite Yoga Companion Kit は、次の例で使用されるサンプルデータのバンドル製品です。

![バンドル製品](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## バンドル項目の順序の変更

バンドル製品内の項目の順序を変更する方法は 2 つあります。

### 方法 1：ドラッグ&amp;ドロップ

を使用する場合 [バンドル](../catalog/product-create-bundle.md) 製品：管理者から、項目とセクションを任意の位置にドラッグ&amp;ドロップできます。

![バンドル項目](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 方法 2：製品データを編集する

バンドル製品の構造を理解する最善の方法は、製品を書き出し、スプレッドシートでデータを調べることです。 バンドル項目の順序を変更するには、製品をエクスポートし、各項目のデータに位置パラメーターを追加します。 項目データはにあります `bundle_values` 書き出された商品の列。 スプレッドシートで開くと、製品に関連付けられているすべての項目が、長い文字列として 1 つのセルに含まれます。 この `bundle_values` 列には、各項目の次の要素が含まれます。

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

このステップでは、Sprite Yoga Companion Kit は（[CSV](data-csv.md) ファイル。 カタログに含まれている他のバンドル製品を使用できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 次の下 _書き出し設定_、設定 **[!UICONTROL Entity Type]** 対象： `Products`.

1. 製品属性のリストで、まで下にスクロールします。 **[!UICONTROL SKU]** 書き出すバンドル製品の SKU を入力します。

   SKU は `24-WG080` この例の製品の場合。

1. セクションの下部までスクロール ダウンし、 **[!UICONTROL Continue]**.

1. が含まれる _[!UICONTROL Action]_の列_[!UICONTROL File name]_ グリッド、クリック **[!UICONTROL Select]** を選択します `Download`.

   ファイルは、ブラウザーが使用するダウンロード場所に表示されます。

#### 手順 2：データを編集する

1. ダウンロードした CSV ファイルをスプレッドシートで開きます。

1. 右端までスクロールして、次の項目を表示します `bundle_values` 列。

   が含まれる `bundle_values` データの場合、各要素はコンマで区切られ、各バンドル項目は次の項目から縦棒で区切られます。 （最後の項目が縦棒で終わらない。） 書き出されたバンドルデータは、次の例のようになります。

   ![バンドル値](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 編集を容易にするために、をコピーできます `bundle_values` データをテキストエディターに貼り付け、各項目の後ろに改行を追加して、各項目が別々の行になるようにします。

1. データを編集した後、慎重に改行を削除し、編集したデータを元のに貼り付けます `bundle_values` 列。

   次の図では、 `position=[number]` 各ヨガストラップにパラメーターを追加して、ストアリスト内の項目の順序を変更します。

   ![位置パラメーター](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. データの編集後、 **[!UICONTROL Save]** csv ファイル。

#### 手順 3：更新された製品のインポート

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 次の下 _[!UICONTROL Import Settings]_、設定&#x200B;**[!UICONTROL Entity Type]**対象： `Products`.

1. を設定 **[!UICONTROL Import Behavior]** 対象： `Replace`.

   このオプションを選択すると、変更内容が追加の項目として追加されるのではなく、バンドル製品の以前のデータが上書きされます。

1. にスクロール ダウンします。 _インポートするファイル_ セクションでクリック **[!UICONTROL Choose File]**.

1. 編集した CSV ファイルを選択します。

1. クリック **[!UICONTROL Check Data]** データがチェックされるまでしばらく待ちます。

1. ファイルが有効な場合、 **[!UICONTROL Import]**.

1. 処理が完了したら、に移動します。 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**をクリックして、**[!UICONTROL Flush Cache Storage]**.

   これにより、更新された製品がストアフロントですぐに使用できるようになります。
