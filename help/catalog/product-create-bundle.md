---
title: バンドル製品
description: ストア内で買い物客がカスタマイズされた製品を構築できるバンドル製品を作成する方法を説明します。
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: e16fdc9f55cada17f82777fdaaaca44780c91e4b
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 0%

---

# バンドル製品

バンドルは _独自に作成_、カスタマイズ可能な製品。 バンドル内の各項目は、次のいずれかの製品タイプに基づくことができます。

- [シンプルな製品](product-create-simple.md)
- [バーチャル製品](product-create-virtual.md)

![バンドル製品](./assets/product-bundle.png){width="700" zoomable="yes"}

オプションは、顧客がのいずれかをクリックすると表示されます **[!UICONTROL Customize]** または **[!UICONTROL Add to Cart]**. バンドルに含まれる製品は様々なので、SKU、価格、重みを動的または固定値に設定できます。

>[!NOTE]
>
>Minimum Advertised Price （MAP）は、動的な価格を使用するバンドル製品では利用できません。

>[!NOTE]
>
>親バンドル製品は、そのすべての子製品のアップセル製品として常に自動的に表示されます。

次の場合 [即時購入](../stores-purchase/checkout-instant-purchase.md) が使用可能になり、 _即時購入_ ボタンがの下に表示されます _カートに追加_ バンドル内の各項目のボタン。

![バンドルをカスタマイズ](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

以下の手順により、を使用してバンドル製品を作成する手順が説明されます。 [製品テンプレート](attribute-sets.md)、必須フィールド、基本設定です。 各必須フィールドには、赤いアスタリスク（`*`）に設定します。 基本を完了したら、必要に応じて他の製品設定を完了できます。

## 手順 1：製品タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. の右上隅にある _[!UICONTROL Add Product]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Bundle Product]**.

   ![バンドル製品を追加](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## 手順 2：属性セットの選択

を選択します [属性セット](attribute-sets.md) このテンプレートを使用して、次のいずれかの操作を行います。

- の場合 **[!UICONTROL Search]**：属性セットの名前を入力します。
- リストで、使用する属性セットを選択します。

フォームが更新され、変更が反映されます。

![テンプレートを選択](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 手順 3：必要な設定を完了する

1. 製品を入力 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れるか **[!UICONTROL SKU]** これは製品名に基づいている、または別の値を入力します。

   各バンドル項目に割り当てられる SKU のタイプを確認するには、次の手順を実行します。

   - A **[!UICONTROL Dynamic SKU]** デフォルトの SKU にサフィックスを追加すると、各バンドル項目に自動的に割り当てることができます。 デフォルトでは、に設定されています。 `Yes`.

   - バンドル項目ごとに一意の SKU を割り当てる場合は、を設定します **[!UICONTROL Dynamic SKU]** 対象： `No`.

   ![動的な SKU と価格](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. バンドルの価格を確認するには、次のいずれかの操作を行います。

   - 顧客が選択したオプションを価格に反映させるには、次のように設定します **[!UICONTROL Dynamic Price]** 対象： `Yes` と終了します **[!UICONTROL Price]** 空白。 この場合、バンドル製品にはカタログから独自の価格はなく、製品価格はバンドルに含まれる個々の製品の価格から派生します。

   - バンドルの固定価格を請求するには、を設定します **[!UICONTROL Dynamic Price]** 対象： `No` を入力し、 **[!UICONTROL Price]** バンドルの料金を請求します。

   >[!NOTE]
   >
   >[!UICONTROL Special Price] および [!UICONTROL Customer Group Price] （階層価格）は、常にすべてのバンドル製品タイプの割引率として設定されます。

1. 製品の公開準備がまだ整っていないので、を設定します **[!UICONTROL Enable Product]** 対象： `No`.

1. クリック **[!UICONTROL Save]** そして続けて。

   商品を保存すると、 [ストア表示](introduction.md#product-scope) 選択が左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品の入手先。

   ![ストア表示を選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 手順 4：基本設定を完了する

1. バンドルの価格が固定されている場合は、を設定します **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

   バンドルに動的価格設定がある場合、税金は次の項目について決定されます **_それぞれ_** バンドル項目。 バンドルに固定価格が設定されている場合、税は **_全体_** バンドル製品。

1. 次のことに注意してください。

   - この **[!UICONTROL Quantity]** 値がバンドル項目ごとに決定されるので、は使用できません。

   - デフォルトでは、 **[!UICONTROL Stock Status]** はに設定されています。 `In Stock`.

1. バンドルの重みを判断するには、次のいずれかの操作を行います。

   - 顧客が選択したオプションを重み付けに反映させるには、次のように設定します **[!UICONTROL Dynamic Weight]** set `Yes` と終了します **[!UICONTROL Weight]** 空白。

   - バンドルに固定ウェイトを割り当てるには、 **[!UICONTROL Dynamic Weight]** 対象： `No` を入力し、 **[!UICONTROL Weight]** をバンドルに含めます。

   ![動的ウェイト](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. 製品をリストに表示するには [新製品](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. デフォルトを使用 **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 割り当てる _[!UICONTROL Categories]_製品に移動するには、**[!UICONTROL Select…]**次のいずれかの操作を行います。

   **既存のカテゴリを選択：**

   - 一致するものが見つかるまで、ボックスに入力を開始します。

   - 割り当てる各カテゴリのチェックボックスを選択します。

   ![バンドル製品の 1 つ以上のカテゴリを選択](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **カテゴリを作成します。**

   - クリック **[!UICONTROL New Category]**.

   - を入力 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：メニュー構造内の位置を指定します。

   - クリック **[!UICONTROL Create Category]**.

1. を選択します。 **[!UICONTROL Country of Manufacture]**.

   製品を説明する追加の属性がある場合があります。 選択によってアトリビュート セットが異なり、後で完成させることができます。

## 手順 5：バンドル項目を追加

この _[!UICONTROL Bundle Items]_セクションを使用すると、バンドル製品タイプに項目を追加したり、現在選択している項目を編集したりできます。

![製品に対して定義されたバンドル項目](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. にスクロール ダウンします。 _バンドル項目_ セクションとセット **[!UICONTROL Ship Bundle Items]** を次のいずれかに変更します。

   - `Separately`
   - `Together`

   を選択する場合 `Together`、すべてのバンドル項目に同じ値を割り当てる必要があります [ソース](../inventory-management/sources-manage.md).

1. クリック **[!UICONTROL Add Option]** 次の手順を実行します。

   - を入力 **[!UICONTROL Option Title]** フィールドラベルとして使用されます。

   - を設定 **[!UICONTROL Input Type]** を次のいずれかに変更します。

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - フィールドを必須入力にするには、 **[!UICONTROL Required]** チェックボックス。

   - クリック **[!UICONTROL Add Products to Option]** このオプションに含める各製品のチェックボックスをオンにします。

     製品が多数ある場合は、リストフィルターとページネーションコントロールを使用して、必要な製品を見つけます。

   - クリック **[!UICONTROL Add Selected Products]**.

     ![選択した製品を追加](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - に項目が表示された後 _オプション_ セクションで、要素にする項目を選択します **[!UICONTROL Default]** 選択。

   - が含まれる _既定の数量_ 列には、顧客が品目を選択したときにバンドルに追加される各品目の数量を入力します。

   - 顧客がバンドル品目の数量を変更できるようにするには、 **[!UICONTROL User Defined]**.


     >[!NOTE]
     >
     >量は、プリセット値またはユーザー定義値にすることができます。 ただし、は割り当てません _[!UICONTROL User Defined]_チェックボックスまたは複数選択の入力タイプのプロパティ。

     デフォルトでは、バンドル品目に含まれるデフォルト数量を顧客が変更することはできません。 ただし、顧客は、バンドルに含める品目の数量を入力できます。

     例えば、スプライトステータスボールのデフォルトの量がに設定されている場合 `2` およびお客様の注文 `4` このバンドルオプションで購入されたボールの合計数は、です。 `8`.

     ![アイテムの詳細](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. バンドルに追加する項目ごとに、これらの手順を繰り返します。

1. バンドルセクション内の項目の順序を変更するには、 _移動_ （ ![移動アイコン](../assets/icon-move.png) ）アイコンをクリックし、項目を位置にドラッグします。

   ![バンドル項目の順序の変更](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   また、書き出されたバンドル製品のデータで項目の順序を変更し、カタログに再度読み込むこともできます。 詳しくは、を参照してください [バンドル製品の読み込み](../systems/data-transfer-bundle-products.md).

   ワークスペースを見やすくするには、最初に各セクションを折りたたんでから、適切な位置にドラッグします。

1. バンドルから項目を削除するには、 **[!UICONTROL Delete]** （ ![ごみ箱アイコン](../assets/icon-delete-trashcan.png) ） アイコンをクリックします。

1. 完了したら、 **[!UICONTROL Save]**.

## 手順 6：製品情報の入力

下にスクロールして、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイトの製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

## 手順 7：製品を公開する

1. カタログに製品を公開する準備が整ったら、次のように設定します **[!UICONTROL Enable Product]** 対象： `Yes` （ ![「はい」を切り替え](../assets/toggle-yes.png) ）に設定します。

1. 次のいずれかの操作を行います。

   **メソッド 1:** 保存とプレビュー

   - 右上隅のをクリックします。 **[!UICONTROL Save]**.

   - ストアで商品を表示するには、次を選択します **[!UICONTROL Customer View]** 日 _Admin_ （ ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ） メニューを使用できます。

     ストアが新しいブラウザータブで開きます。

   ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **メソッド 2:** 保存して閉じる

   日 _[!UICONTROL Save]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## 入力コントロール

| 制御 | 説明 | 例 |
|--- |--- |--- |
| [!UICONTROL Drop-down] | 製品名と価格を含むオプションのドロップダウン リストを表示します。 選択できる項目は 1 つだけです。 | ![ドロップダウン](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | 各オプションのラジオボタンを表示し、その後に製品名と価格を表示します。 選択できる項目は 1 つだけです。 | ![ラジオボタン](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | 各オプションのチェックボックスに続いて製品名と価格が表示されます。 複数の項目を選択できます。 | ![Checkbox](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | 製品名と価格を含むオプションのリストを表示します。 複数の項目を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各項目をクリックします。 | ![複数選択](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL SKU] | 各項目に変数 SKU または動的 SKU を割り当てるか、バンドルに固定 SKU を使用するかを決定します。 オプション： `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | 選択した項目に基づいて重みを計算するか、バンドル全体の固定重みにするかを指定します。 オプション： `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | 製品価格を、最も安価な価格から最も高価な価格（価格範囲）または最も安価な価格（安値）として表示する範囲として表示するかどうかを決定します。 オプション： `Price Range` / `As Low As` |
| バンドル品目の出荷 | 個々の品目を個別に出荷できるかどうかを指定します。 |

{style="table-layout:auto"}

## バンドル製品の在庫ステータス

バンドル製品の在庫ステータスはです **_自動変更されて在庫切れ_** 次のいずれかのシナリオが発生した場合：

- すべてのオプションはオプションで、関連する製品はすべて次のとおりです _在庫切れ_.

- 必須オプションと、必須オプションに関連付けられている製品は次のとおりです _在庫切れ_.

バンドル製品の在庫ステータスはです **_在庫切れに自動的に変更されない_** 次のいずれかのシナリオが発生した場合：

- すべてのオプションはオプションで、少なくとも 1 つの関連製品はです。 _在庫あり_.

- 一部のオプションが必要で、それぞれの必須オプションに少なくとも 1 つの関連製品が必要です _在庫あり_.

## 注意事項

![Checkbox](../assets/checkbox.png) 顧客は次のことができます _独自に作成_ バンドル製品。

![Checkbox](../assets/checkbox.png) バンドル項目は、カスタムオプションなしのシンプル製品または仮想製品にすることができます。

![Checkbox](../assets/checkbox.png) 「価格ビュー」は、次のいずれかに設定できます `Price Range` または `As Low As`.

![Checkbox](../assets/checkbox.png) SKU と重み付けには、 `Fixed` または `Dynamic`.

![Checkbox](../assets/checkbox.png) 量は、プリセット値またはユーザー定義値にすることができます。 ただし、は割り当てません _[!UICONTROL User Defined]_チェックボックスまたは複数選択の入力タイプのプロパティ。

![Checkbox](../assets/checkbox.png) バンドル品目は、一緒に出荷することも、個別に出荷することもできます。

![Checkbox](../assets/checkbox.png) 親バンドル製品は、そのすべての子製品のアップセル製品として常に自動的に表示されます。

![Checkbox](../assets/checkbox.png) [!UICONTROL Special Price] および [!UICONTROL Customer Group Price] （階層価格）は、常にすべてのバンドル製品タイプの割引率として設定されます。
