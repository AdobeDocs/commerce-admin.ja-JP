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

![&#x200B; 製品ページのスウォッチ &#x200B;](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

[&#x200B; 設定可能な製品 &#x200B;](product-create-configurable.md) の場合、カラーは、視覚的なスウォッチ、テキストスウォッチ、入力コントロールで示すことができます。 スウォッチは、製品ページ、製品リスト、[&#x200B; レイヤーナビゲーション &#x200B;](navigation-layered.md) で使用できます。 製品ページでは、スウォッチが同期され、スウォッチが選択されると、対応する製品画像が表示されます。 ユーザーがスウォッチを選択すると、対応する値が入力フィールドに表示され、スウォッチの概要が現在の選択内容に設定されます。

>[!NOTE]
>
>スウォッチ属性は、管理者の [!UICONTROL Attribute Edit] ページで _[!UICONTROL Update Product Preview Image]_&#x200B;オプションの値を `No` に設定することで、スウォッチが選択されたときに対応するシンプルな製品画像を表示しないように設定できます。

## テキストベースのスウォッチ

画像がスウォッチで使用できない場合、属性値はテキストで表示されます。 テキストベースのスウォッチは、テキストラベルを付けたボタンのようなもので、画像を付けたスウォッチと同じように動作します。 テキストベースのスウォッチを使用して使用可能なサイズを表示すると、使用できないサイズは消去されます。

![&#x200B; テキストベースのスウォッチ選択で在庫切れのサイズが表示される &#x200B;](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## レイヤー化されたナビゲーションでのスウォッチ

スウォッチは、color 属性の _[!UICONTROL Use in Layered Navigation]_&#x200B;プロパティが `Yes` に設定されている場合に、レイヤー化されたナビゲーションでも使用できます。 次の例では、レイヤーナビゲーションで、テキストベースのスウォッチとカラー画像スウォッチの両方を表示しています。

![&#x200B; スウォッチをレイヤー化されたナビゲーションで表示 &#x200B;](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## 製品のスウォッチの作成

スウォッチは、`color` 属性のコンポーネントとして定義することも、特定の製品用にローカルに設定して [&#x200B; 製品画像 &#x200B;](product-image.md#upload-an-image) としてアップロードすることもできます。

前述の例では、「シルヴィアカプリ」パンツは、`red`、`green`、`blue` の特定の値で利用できます。 スウォッチは製品画像から取得されたものなので、それぞれが実際の色を表現したものです。 `color` 属性は、すべての製品カラーおよびスウォッチの情報を管理するために使用されます。

### 手順 1：スウォッチを作成する

次のいずれかの方法を使用して、製品のスウォッチを作成します。

#### 方法 1：カラースウォッチを追加する

1. 製品の実際の色を取得するには、画像をフォトエディターで開き、スポイトツールを使用して正確な色を特定し、16 進数値に相当するものをメモします。

   ![16 進数カラー値 &#x200B;](./assets/swatch-hex-values.png){width="400"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**&#x200B;に移動します。

1. グリッドで、_color_ 属性を編集モードで開きます。

1. **[!UICONTROL Catalog Input Type for Store Owner]** が `Visual Swatch` に設定されていることを確認します。

1. 製品表示ページでスウォッチが選択されているときに、対応するシンプルな製品画像を表示しない場合は、**[!UICONTROL Update Product Preview Image]** を `No` に設定します。

1. [_[!UICONTROL Manage Swatch (Values of Your Attribute)]_] で [**[!UICONTROL Add Swatch]**] をクリックし、次の操作を行います。

   ![&#x200B; スウォッチ値の管理 &#x200B;](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - _スウォッチ_ 列で、新しいスウォッチをクリックし、メニューから **[!UICONTROL Choose a color]** を選択します。

     ![&#x200B; スウォッチカラーの選択 &#x200B;](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - カラーピッカーで、「**#**」フィールドにカーソルを置き、現在の値を削除して、新しいカラーの 6 文字の 16 進数値を入力します。

     ![16 進数の値を入力 &#x200B;](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - スウォッチを保存するには、カラーピッカーの右下隅にある _カラーホイール_ （![&#x200B; カラーアイコン &#x200B;](../assets/icon-color-wheel.png)）アイコンをクリックします。

   - _管理者_ 列に、カラーをストア管理者に説明するラベルを入力します。

     該当する場合は、サポートされている各言語のカラーの翻訳を入力することもできます。 次の例では、色が特定の製品にのみ使用されるので、SKU が _Admin_ ラベルに参照用に含まれています。 ラベルにはスペースやアンダースコアを含めることができますが、ハイフンは含めることはできません。

   - _デフォルト_ 列で、デフォルトオプションにするスウォッチを選択します。

   - カラースウォッチの順序を変更するには、_[!UICONTROL Order]_&#x200B;の ![&#x200B; 並べ替え順序アイコン &#x200B;](../assets/icon-sort-order.png) アイコンをクリックし、項目をリストの新しい位置にドラッグします。

     ![&#x200B; スウォッチラベル &#x200B;](./assets/attribute-swatch-labels.png){width="400"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックし、プロンプトが表示されたらキャッシュを更新します。

1. 各製品を編集モードで開き、**カラー** 属性を正しいスウォッチで更新します。

   複数の製品を同時に更新するには、次の手順に従います。

#### 方法 2：スウォッチ画像をアップロードする

1. スウォッチの画像をキャプチャするには、フォトエディターで商品画像を開き、画像の正方形の領域（カラー、パターン、テクスチャを示す）を保存します。

   必要に応じて、製品のバリエーションごとにこのアクションを繰り返すことができます。

   スウォッチのサイズとサイズは、テーマによって決まります。 通常、画像を正方形として保存すると、パターンの縦横比を維持するのに役立ちます。

   ![&#x200B; スウォッチ画像 &#x200B;](./assets/swatch-samples.png){width="400"}

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**&#x200B;に移動します。

1. グリッドで、**[!UICONTROL color]** 属性を編集モードで開きます。

1. **[!UICONTROL Catalog Input Type for Store Owner]** が `Visual Swatch` に設定されていることを確認します。

1. 製品表示ページでスウォッチが選択されているときに、対応するシンプルな製品画像を表示しない場合は、**[!UICONTROL Update Product Preview Image]** を `No` に設定します。

1. 「_[!UICONTROL Manage Swatch]_（属性の値）」で「**[!UICONTROL Add Swatch]**」をクリックし、次の手順を実行します。

   - _[!UICONTROL Swatch]_&#x200B;列で、新しいスウォッチをクリックしてメニューを表示し、**[!UICONTROL Upload a file]**&#x200B;を選択します。

   - 準備したスウォッチファイルに移動し、アップロードするファイルを選択します。

   - 各スウォッチ画像に対して、これらの手順を繰り返します。

   - 管理者およびストアフロントのラベルを入力します。

     この例では、SKU が管理者のラベルに参照用に含まれています。これらの色は特定の製品にのみ使用されるからです。 ラベルにスペースやアンダースコアを含めることはできますが、ハイフンを含めることはできません。

     ![&#x200B; ラベルを入力 &#x200B;](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックし、プロンプトが表示されたらキャッシュを更新します。

1. 各製品を編集モードで開き、**[!UICONTROL Color]** 属性を正しいスウォッチで更新します。

   複数の製品を同時に更新するには、次の手順に従います。

### 手順 2：製品を更新する

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. **[!UICONTROL Filter]** を使用すると、名前または SKU でリストを表示し、該当する製品のみを含めることができます。

1. グリッドで、スウォッチを適用する各製品のチェックボックスを選択します。

1. **[!UICONTROL Actions]** を `Update Attributes` に設定します。

   この例では、ズボンのすべての青い設定が選択されています。

   ![&#x200B; 製品スウォッチ属性の更新 &#x200B;](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Color]** 属性までスクロールダウンし、「**[!UICONTROL Change]**」チェックボックスを選択します。

   ![&#x200B; チェックボックスを変更 &#x200B;](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. 選択した商品に適用されるスウォッチを選択し、「**[!UICONTROL Save]**」をクリックします。

1. プロンプトが表示されたら、キャッシュを更新します。

   ![&#x200B; ストアフロントに表示されるのスウォッチ &#x200B;](./assets/swatch-blue-schmear.png){width="200"}

## シンプルな製品へのスウォッチの追加

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品を編集モードで開き、製品ステータスを確認します（有効にする必要があります）。

1. ボタン（「`Configurations`」タブ **[!UICONTROL Create Configurations]** 下）をクリックします。

1. ポップアップウィンドウで、カラー属性と **[!UICONTROL Next]** を選択します。

1. この製品に含める属性からカラースウォッチを選択します。

1. プログレスバーで、「**[!UICONTROL Next]**」をクリックします。

1. [&#x200B; 画像、価格、数量を設定 &#x200B;](product-create-configurable.md#step-3-configure-the-images-price-and-quantity)。

   このステップでは、各設定の画像、価格、数量を設定します。 使用可能なオプションはそれぞれに対して同じで、1 つのみ選択できます。 すべての SKU に同じ設定を適用することも、各 SKU に一意の設定を適用することも、今は設定をスキップすることもできます。

1. 画像、価格、数量の設定が完了したら、右上隅の「**[!UICONTROL Next]**」をクリックします。

   現在の製品バリエーションは、「設定」セクションの下部に表示されます。 設定に問題がなければ、「**[!UICONTROL Generate Products]**」をクリックします。
