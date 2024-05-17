---
title: 製品スウォッチ
description: 設定可能な製品リストのスウォッチを定義する方法について説明します。
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 0%

---

# 製品スウォッチ

顧客は色の選択に大きな期待を抱いており、製品の説明で、使用可能な各色、パターンまたはテクスチャを正確に表すことが重要です。 たとえば、次の例のズボンは、赤、緑、および青では使用できません。 むしろ、赤、緑、青の特定の色合いでのみ利用可能です。これはおそらくこの製品に固有のものです。

![製品ページのスウォッチ](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

の場合 [設定可能な製品](product-create-configurable.md)の色は、視覚的なスウォッチ、テキストスウォッチまたは入力コントロールで示すことができます。 スウォッチは製品ページ、製品リストおよび [階層型ナビゲーション](navigation-layered.md). 製品ページでは、スウォッチが同期され、スウォッチが選択されると、対応する製品画像が表示されます。 ユーザーがスウォッチを選択すると、対応する値が入力フィールドに表示され、スウォッチの概要が現在の選択内容に設定されます。

>[!NOTE]
>
>スウォッチ属性は、を設定することで、スウォッチが選択されたときに対応するシンプルな商品画像を表示しないように設定できます。 _[!UICONTROL Update Product Preview Image]_オプションの値： `No` 日 [!UICONTROL Attribute Edit] 管理画面の「」ページ。

## テキストベースのスウォッチ

画像がスウォッチで使用できない場合、属性値はテキストで表示されます。 テキストベースのスウォッチは、テキストラベルを付けたボタンのようなもので、画像を付けたスウォッチと同じように動作します。 テキストベースのスウォッチを使用して使用可能なサイズを表示すると、使用できないサイズは消去されます。

![テキストベースのスウォッチ選択で在庫切れのサイズが表示される](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## レイヤー化されたナビゲーションでのスウォッチ

スウォッチは、次のような場合、階層化されたナビゲーションでも使用できます _[!UICONTROL Use in Layered Navigation]_color 属性のプロパティがに設定されている `Yes`. 次の例では、レイヤーナビゲーションで、テキストベースのスウォッチとカラー画像スウォッチの両方を表示しています。

![のスウォッチをレイヤー化されたナビゲーションで表示](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## 製品のスウォッチの作成

スウォッチは、 `color` 特定の製品に対して属性を設定するか、ローカルに設定して、次のようにアップロードします [製品画像](product-image.md#upload-an-image).

前述の例では、「Sylvia Capri」パンツは、次の特定の値で使用できます `red`, `green`、および `blue`. スウォッチは製品画像から取得されたものなので、それぞれが実際の色を表現したものです。 この `color` 属性は、すべての製品カラーとスウォッチの情報を管理するために使用します。

### 手順 1：スウォッチを作成する

次のいずれかの方法を使用して、製品のスウォッチを作成します。

#### 方法 1：カラースウォッチを追加する

1. 製品の実際の色を取得するには、画像をフォトエディターで開き、スポイトツールを使用して正確な色を特定し、16 進数値に相当するものをメモします。

   ![16 進数のカラー値](./assets/swatch-hex-values.png){width="400"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. グリッドで、 _色_ 編集モードの属性。

1. を確認します。 **[!UICONTROL Catalog Input Type for Store Owner]** はに設定されています。 `Visual Swatch`.

1. 製品表示ページでスウォッチが選択されているときに、対応するシンプルな製品画像を表示しないようにするには、次のように設定します **[!UICONTROL Update Product Preview Image]** 対象： `No`.

1. 次の下 _[!UICONTROL Manage Swatch (Values of Your Attribute)]_を選択し、**[!UICONTROL Add Swatch]**次の手順を実行します。

   ![スウォッチ値の管理](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - が含まれる _スウォッチ_ 列で、新しいスウォッチをクリックし、 **[!UICONTROL Choose a color]** メニューから。

     ![スウォッチカラーの選択](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - カラーピッカーで、 **#** フィールドで、現在の値を削除し、新しいカラーの 6 文字の 16 進数値を入力します。

     ![16 進数値を入力](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - スウォッチを保存するには、 _カラーホイール_ （ ![カラーアイコン](../assets/icon-color-wheel.png) ） アイコンをクリックします。

   - が含まれる _Admin_ 列に、色をストア管理者に説明するラベルを入力します。

     該当する場合は、サポートされている各言語のカラーの翻訳を入力することもできます。 次の例では、参照用に SKU がに含まれています _Admin_ 特定の商品に対してのみ色が使用されるので、ラベルを付けます。 ラベルにはスペースやアンダースコアを含めることができますが、ハイフンは含めることはできません。

   - が含まれる _デフォルト_ 列で、デフォルトオプションにするスウォッチを選択します。

   - カラースウォッチの順序を変更するには、 _[!UICONTROL Order]_![並べ替え順アイコン](../assets/icon-sort-order.png) アイコンをクリックして、リスト内の新しい位置に項目をドラッグします。

     ![スウォッチラベル](./assets/attribute-swatch-labels.png){width="400"}

1. 完了したら、 **[!UICONTROL Save Attribute]** プロンプトが表示されたらキャッシュを更新します。

1. 各製品を編集モードで開き、 **カラー** 属性に正しいスウォッチが付きます。

   複数の製品を同時に更新するには、次の手順に従います。

#### 方法 2：スウォッチ画像をアップロードする

1. スウォッチの画像をキャプチャするには、フォトエディターで商品画像を開き、画像の正方形の領域（カラー、パターン、テクスチャを示す）を保存します。

   必要に応じて、製品のバリエーションごとにこのアクションを繰り返すことができます。

   スウォッチのサイズとサイズは、テーマによって決まります。 通常、画像を正方形として保存すると、パターンの縦横比を維持するのに役立ちます。

   ![スウォッチ画像](./assets/swatch-samples.png){width="400"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. グリッドで、 **[!UICONTROL color]** 編集モードの属性。

1. を確認します。 **[!UICONTROL Catalog Input Type for Store Owner]** はに設定されています。 `Visual Swatch`.

1. 製品表示ページでスウォッチが選択されているときに、対応するシンプルな製品画像を表示しないようにするには、次のように設定します **[!UICONTROL Update Product Preview Image]** 対象： `No`.

1. 次の下 _[!UICONTROL Manage Swatch]_（属性の値）を選択し、**[!UICONTROL Add Swatch]**次の手順を実行します。

   - が含まれる _[!UICONTROL Swatch]_列で、新しいスウォッチをクリックしてメニューを表示し、**[!UICONTROL Upload a file]**.

   - 準備したスウォッチファイルに移動し、アップロードするファイルを選択します。

   - 各スウォッチ画像に対して、これらの手順を繰り返します。

   - 管理者およびストアフロントのラベルを入力します。

     この例では、SKU が管理者のラベルに参照用に含まれています。これらの色は特定の製品にのみ使用されるからです。 ラベルにスペースやアンダースコアを含めることはできますが、ハイフンを含めることはできません。

     ![ラベルを入力](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Attribute]** プロンプトが表示されたらキャッシュを更新します。

1. 各製品を編集モードで開き、 **[!UICONTROL Color]** 属性に正しいスウォッチが付きます。

   複数の製品を同時に更新するには、次の手順に従います。

### 手順 2：製品を更新する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. の使用 **[!UICONTROL Filter]** リストを名前または SKU で表示し、該当する製品のみを含めます。

1. グリッドで、スウォッチを適用する各製品のチェックボックスを選択します。

1. を設定 **[!UICONTROL Actions]** 対象： `Update Attributes`.

   この例では、ズボンのすべての青い設定が選択されています。

   ![製品スウォッチ属性の更新](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. にスクロール ダウンします。 **[!UICONTROL Color]** 属性とを選択し、 **[!UICONTROL Change]** チェックボックス。

   ![チェックボックスを変更](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. 選択した商品に適用されるスウォッチを選択し、 **[!UICONTROL Save]**.

1. プロンプトが表示されたら、キャッシュを更新します。

   ![ストアフロントに表示されるのスウォッチ](./assets/swatch-blue-schmear.png){width="200"}

## シンプルな製品へのスウォッチの追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開き、製品ステータスを確認します（有効にする必要があります）。

1. クリック **[!UICONTROL Create Configurations]** ボタン（ `Configurations` タブ）。

1. ポップアップウィンドウで、カラー属性を選択し、 **[!UICONTROL Next]**.

1. この製品に含める属性からカラースウォッチを選択します。

1. プログレスバーで、 **[!UICONTROL Next]**.

1. [画像、価格、数量を設定](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   このステップでは、各設定の画像、価格、数量を設定します。 使用可能なオプションはそれぞれに対して同じで、1 つのみ選択できます。 すべての SKU に同じ設定を適用することも、各 SKU に一意の設定を適用することも、今は設定をスキップすることもできます。

1. 画像、価格、数量の設定が完了したら、 **[!UICONTROL Next]** 右上隅

   現在の製品バリエーションは、「設定」セクションの下部に表示されます。 設定に問題がなければ、 **[!UICONTROL Generate Products]**.
