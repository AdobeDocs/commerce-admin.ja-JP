---
title: バンドル製品のインポート
description: バンドル製品の製品データを読み込む例を確認します。
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/UeGDyElWBOH7kUeeb7Bhqksp-hQ-jq5FkoYTWMShF6A
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 628
ht-degree: 0%

---

# バンドル製品のインポート

バンドル商品では、商品の選択肢が提示され、顧客は購入する商品を選択できます。 バンドルを構成するすべてのアイテムは、カタログに[&#x200B; シンプル製品](../catalog/product-create-simple.md)または[仮想製品](../catalog/product-create-virtual.md)として存在します。 通常、バンドル製品は管理者から作成および更新されます。 ただし、データを読み込んでバンドル製品を作成したり、既存のバンドル製品を書き出してデータを編集し、カタログに読み込むこともできます。 Sprite Yoga Companion Kitは、サンプルデータに含まれるバンドル製品で、次の例で使用されます。

![&#x200B; バンドル製品](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## バンドルアイテムの順序の変更

バンドル製品内のアイテムの順序を変更するには、2つの方法があります。

### 方法1：ドラッグ&amp;ドロップ

管理者から[&#x200B; バンドル &#x200B;](../catalog/product-create-bundle.md)製品を操作する場合、アイテムとセクションをドラッグ&amp;ドロップして配置できます。

![&#x200B; バンドルアイテム &#x200B;](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 方法2：製品データを編集する

バンドル製品の構造を理解する最良の方法は、製品を書き出してスプレッドシートでデータを調べることです。 商品を書き出し、各商品のデータに位置パラメーターを追加することで、バンドルアイテムの順序を変更できます。 アイテム データは、エクスポートされた製品の`bundle_values`列にあります。 スプレッドシートで開くと、製品に関連付けられたすべてのアイテムが、長いテキスト文字列として1つのセルに表示されます。 `bundle_values`列には、各項目に対する次の要素が含まれています。

- アイテムセクションの名前
- 入力制御
- 必須アイテム指標
- SKU
- カラー
- 価格
- デフォルトのオプションインジケーター
- 既定の数量
- 価格タイプ
- 編集可能な数量指標

#### 手順1：バンドル製品の書き出し

この手順では、Sprite Yoga Companion Kitを（[CSV](data-csv.md) ファイルとして書き出します。 カタログに含まれている他のバンドル製品を使用できます。

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;に移動します。

1. _書き出し設定_&#x200B;で、**[!UICONTROL Entity Type]**&#x200B;を`Products`に設定します。

1. 製品属性のリストで、**[!UICONTROL SKU]**&#x200B;までスクロールし、書き出すバンドル製品のSKUを入力します。

   この例では、製品のSKUは`24-WG080`です。

1. セクションの一番下までスクロールして、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. _[!UICONTROL File name]_&#x200B;グリッドの&#x200B;_[!UICONTROL Action]_&#x200B;列で、**[!UICONTROL Select]**&#x200B;をクリックし、`Download`を選択します。

   ファイルは、ブラウザーが使用するダウンロード場所に表示されます。

#### 手順2：データの編集

1. ダウンロードしたCSV ファイルをスプレッドシートで開きます。

1. `bundle_values`列が表示されるまで、右端までスクロールします。

   `bundle_values` データでは、各要素はコンマで区切られ、各バンドル項目は縦の棒で次の要素から区切られます。 （最後の項目は縦棒で終わりません）。 書き出されたバンドルデータは、次の例のようになります。

   ![&#x200B; バンドル値](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 編集しやすくするために、`bundle_values` データをコピーしてテキストエディターに貼り付け、次に、各項目の後に改行を追加して、各項目が別々の行になるようにします。

1. データを編集したら、改行を慎重に削除し、編集したデータを`bundle_values`列に貼り付けます。

   次の図では、ストアリストのアイテムの順序を変更するために、各ヨガストラップに`position=[number]` パラメーターを追加しています。

   ![位置パラメーター](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. データの編集後、CSV ファイルを&#x200B;**[!UICONTROL Save]**&#x200B;します。

#### 手順3：更新した製品の読み込み

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;に移動します。

1. _[!UICONTROL Import Settings]_&#x200B;で、**[!UICONTROL Entity Type]**&#x200B;を`Products`に設定します。

1. **[!UICONTROL Import Behavior]**&#x200B;を`Replace`に設定します。

   このオプションは、変更内容を追加アイテムとして追加するのではなく、バンドル製品の以前のデータを上書きします。

1. 「_インポートするファイル_」セクションまで下にスクロールし、**[!UICONTROL Choose File]**&#x200B;をクリックします。

1. 編集したCSV ファイルを選択します。

1. **[!UICONTROL Check Data]**&#x200B;をクリックし、データがチェックされるまでしばらく待ちます。

1. ファイルが有効な場合は、**[!UICONTROL Import]**&#x200B;をクリックします。

1. プロセスが完了したら、**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;に移動し、**[!UICONTROL Flush Cache Storage]**&#x200B;をクリックします。

   これにより、更新された商品がストアフロントですぐに利用できるようになります。
