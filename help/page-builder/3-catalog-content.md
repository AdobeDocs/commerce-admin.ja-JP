---
title: '''[!DNL Page Builder] チュートリアル第 3 部：カタログのコンテンツ'
description: に製品リストを追加する方法を説明します [!DNL Page Builder] ページ。
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# [!DNL Page Builder] ウォークスルー（パート 3）：カタログのコンテンツ

この演習では、製品リストのページへの追加、製品ページのカスタマイズ、を追加するカスタム属性の作成がどれほど簡単であるかを示します [!DNL Page Builder] 製品属性セットへのワークスペース。

![商品リスト](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

この演習では、を完了していることを前提としています [第 1 部：シンプルなページ](1-simple-page.md) および [パート 2：ブロック](2-blocks.md)（前提条件とダウンロードしたサンプルファイルを含む）。 この演習の 3 つの部分を順番に実行します。

## パート 1：製品リストの追加

[!DNL Page Builder] を使用すると、ステージへの製品リストの追加が簡単になります。 この例では、製品リストがページに直接追加されます。

### 手順 1：ステージへの製品リストの追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. の検索 _シンプルなページ_ 最初の練習で作成し、2 番目の練習で修正した内容を選択します **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクションでクリック **[!UICONTROL Edit with Page Builder]** またはコンテンツプレビュー領域内です。

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、ドラッグ：**[!UICONTROL Row]**ステージの一番上に移動します。

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をドラッグします。 **[!UICONTROL Products]** 新しい行へのプレースホルダー。

   ![製品プレースホルダーを行にドラッグ](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### 手順 2：条件を作成する

1. 空の products コンテナにポインタを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![製品ツールボックス](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Select Products By]**、を選択 `Condition`.

1. 条件を追加します。

   - 「」をクリックします _追加_ （![アイコンを追加](../assets/icon-add-green-circle.png)） アイコンをクリックします。

   - 次の下 _[!UICONTROL Product Attribute]_、を選択&#x200B;**[!UICONTROL Category]**.

     ![条件のカテゴリ属性の選択](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - を完了する _[!UICONTROL Category is]..._ 条件の一部を作成するには、その他（...）アイコンをクリックし、 _選択_ （![選択アイコン](../assets/icon-list-chooser.png)） アイコンをクリックします。

     ![条件の定義](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - カテゴリツリーで、にドリルダウンします **女性 > トップス** カテゴリを選択し、 **ティー** チェックボックス。

     ![ツリーでのカテゴリの選択](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - チェックマーク（![チェックマークアイコン](../assets/icon-checkmark-green-circle.png)） アイコンをクリックします。

     対応するカテゴリ ID がフィールドに表示され、条件が完了します。

### 手順 3：設定を完了する

1. を入力 **[!UICONTROL Number of Products to Display]**.

   デフォルトでは、リストには 5 つの製品が表示されます。

1. 必要に応じて、残りの設定を完了します。

   必要に応じて、の最後にあるフィールドの説明を使用します。 [コンテンツを追加 – 製品](products.md) を参照してください。

1. 完了したら、 **[!UICONTROL Save]** 設定を保存し、に戻ります [!DNL Page Builder] ワークスペース。

   ![ステージの商品リスト](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. ステージの右上隅にあるをクリックします _全画面表示を閉じる_ （ ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ） アイコンをクリックします。

   このアイコンをクリックすると、に戻ります _[!UICONTROL Content]_プレビューが表示されたページの「」セクション。

1. 右上隅のをクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

## 第 2 部：製品ページのカスタマイズ

>[!NOTE]
>
>管理者ユーザーには次が必要です [!UICONTROL Content] ユーザーの権限 [役割スコープ](../systems/permissions-user-roles.md) 見る [!UICONTROL Edit with Page Builder] をクリックし、ページビルダーを使用できます。

演習のこの部分では、製品ページ上の一連のタブの下にビデオを配置することで、製品ページを簡単にカスタマイズする方法を説明します。 更新するプロセス [カテゴリページ](../catalog/categories-content-settings.md) コンテンツは基本的に同じです。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. この例で使用できる簡単な製品を見つけて、編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

1. 次の _[!UICONTROL Description]_を選択し、**[!UICONTROL Edit with Page Builder]**.

   ![商品説明コンテンツ](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   商品の説明が以前に次の値なしで入力された場合 [!DNL Page Builder]現在の説明がHTMLとして [HTMLコード](html-code.md) コンテナ。 Luma テーマを使用すると、製品の説明が「詳細」タブに表示されます。

1. が含まれる [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、ドラッグ：**[!UICONTROL Row]**ステージに移動し、HTMLコードコンテナの下に配置します。

   行が正しい位置にあるときに表示される赤いガイドラインを探します。

   ![行をステージにドラッグ](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をドラッグします。 **[!UICONTROL Video]** 新しい行へのプレースホルダー。

   ![行のビデオプレースホルダー](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. 空のビデオコンテナにカーソルを合わせてツールボックスを表示し、 _設定_ （ ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ） アイコンをクリックします。

   ![ビデオツールボックス](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. を入力 **[!UICONTROL Video URL]**.

   ビデオは次のいずれかでホストできます [YouTube][1] または [Vimeo][2]. この例のビデオは、YouTubeの次の URL で見つかります。

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![ビデオの編集](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. を入力 **[!UICONTROL Maximum Width]** ビデオディスプレイのピクセル数。

   このオプションを空白のままにすると、ビデオは使用可能なスペースいっぱいに表示されます。

1. クリック **[!UICONTROL Save]** 設定を保存し、に戻ります [!DNL Page Builder] ワークスペース。

   ![コンテンツステージのビデオ](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. ステージの右上隅にあるをクリックします _全画面表示を閉じる_ （ ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ） アイコンをクリックします。

   このアイコンをクリックすると、に戻ります _[!UICONTROL Content]_プレビューが表示されたページの「」セクション。

1. 右上隅のをクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

ストアフロントでは、ビデオは一連のタブの下に表示されます。 モバイルデバイスでのページの外観を確認するには、ウィンドウのサイズを変更します。

![製品ページに表示されるビデオ](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**これで、** カタログコンテンツのチュートリアルの 2 番目のパートを完了しました。 作成した作業は保持しておくと、後で参照できます。

## 第 3 部：カスタム属性の追加

の使用 [!DNL Page Builder] 完全に機能するようにを追加するためのカスタム属性 [!DNL Page Builder] 魅力的なコンテンツの作成に使用できる製品ページへのワークスペース。 演習のこのパートでは、を使用してカスタム属性を作成する方法を説明します [!DNL Page Builder] 入力タイプを入力し、カタログの製品ページに適用します。 これらの属性の詳細については、を参照してください [製品属性](../catalog/product-attributes.md).

### 手順 1：製品を作成する

ライブストアが変更されないようにするには、説明されたプロパティを使用して製品を作成します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Product]**.

1. 次のプロパティを持つ製品を作成します。

   - 
     [!UICONTROL 属性セット]: Default
   - [!UICONTROL Product Name]：マイ製品
   - 
     [!UICONTROL SKU]: Tutorial
   - 
     [!UICONTROL Price]: 75.00
   - 
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]：在庫あり
   - 
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]：女性/ トップス / T 型

1. 右上隅のをクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

### 手順 2：カスタム属性の作成

この手順では、2 つの新しいカスタム アトリビュートを作成して、 [!DNL Page Builder] およびテキストエディターの入力タイプを使用できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Attribute]**.

1. を入力 **[!UICONTROL Default Label]** 属性のを参照してください。

   この例では、を使用します `My Page Builder Attribute` をラベルに使用します。

1. を設定 **[!UICONTROL Catalog Input Type for Store Owner]** 対象： `Page Builder`.

   カスタム アトリビュートを作成する場合、アプリケーションに最適なエディタを次のいずれかとして指定できます `Page Builder` または標準の WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] 入力タイプ](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Attribute Properties]** を選択し、次の設定を行います。

   - [!UICONTROL Attribute Code]：スペースの代わりにハイフンを使用して、小文字で属性コードを入力します。 この例では、を使用します `my_page_builder_attribute`.
   - [!UICONTROL Scope]：デフォルト値を使用します。 `Store View`.
   - [!UICONTROL Default Value]：属性のデフォルト値を入力します。
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. が含まれる _[!UICONTROL Attribute Information]_左側のパネルで、**[!UICONTROL Storefront Properties]**さらに、次の設定を行います。

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. 完了したら、 **[!UICONTROL Save Attribute]**.

1. 上記の手順を繰り返して、同じ基本プロパティを持ち、テキストエディター入力タイプが次のような 2 番目の属性を作成します。

   - [!UICONTROL Default Label]：マイテキストエディターの属性
   - [!UICONTROL Catalog Input Type for Store Owner]：テキストエディター
   - 
     [!UICONTROL 属性コード]: `my_text_editor_attribute`

### 手順 3：製品属性セットの更新

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   この例では、新しい属性を一時的にに追加します。 `default` 属性セット。 この演習の最後では、カタログに影響を与えないように、属性セットから属性を削除します。

   >[!NOTE]
   >
   >ライブストアを変更しない場合は、属性セットを更新せずにそれに従うことができます。

1. の検索 _[!UICONTROL Default]_リストで設定した属性をダブルクリックして、編集モードで開きます。

1. が含まれる _未割り当て属性_ リストを表示し、作成した新しい属性を見つけて、 _[!UICONTROL Groups]_列、下&#x200B;**[!UICONTROL Content]**.

   内の属性の場所 [!UICONTROL Groups] 列は、ページ上の表示場所を決定します。

   ![コンテンツグループに追加された新しい属性](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]** 属性セット リストに戻ります。

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** ページの上部にあるリンクをクリックして、無効なキャッシュを更新します。

### 手順 4：製品をアップデートする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品グリッドで、を検索します _マイ製品_ そして、編集モードで開きます。

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Content]** セクション。

   セクションの上部には、製品コンテンツの 2 つの標準属性があります。

   - _簡単な説明_（標準の WYSIWYG を使用） [エディター](../content-design/editor.md).
   - _説明_。この中には、 [!DNL Page Builder] プレビュー。

   ![製品コンテンツ](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   セクションの下半分までスクロールすると、作成して割り当てた属性が 2 つあります。

   - _マイ [!DNL Page Builder] 属性_。この中には、 [!DNL Page Builder] プレビュー。
   - _テキスト エディタの属性_&#x200B;標準の WYSIWYG エディターを使用する。

   ![製品コンテンツの編集](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. が含まれる **テキスト エディタの属性** エディタ、入力 `Text Editor Attribute placeholder text`.

   - 右上隅のをクリックします **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. の場合 **マイページビルダー属性**&#x200B;を選択し、 **[!UICONTROL Edit with Page Builder]** 説明テキストを追加します。

   - が含まれる [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をドラッグします。 **[!UICONTROL Text object]** ステージに移動します。

   - Enter `Page Builder attribute placeholder text`.

   - ステージの右上隅にあるをクリックします _全画面表示を閉じる_ （ ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ） アイコンをクリックします。

     ![プレースホルダーテキストを含むカスタム属性](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. Scroll up to **[!UICONTROL Description]**&#x200B;を選択し、 **[!UICONTROL Edit with Page Builder]**&#x200B;をクリックし、前の手順と同じ方法を使用して任意のテキストを追加します。

1. 製品ページの右上隅にある「 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** ページ上部のメッセージ内のリンクをクリックし、無効なキャッシュを更新します。

### 手順 5：結果の表示

1. ストアフロントのサンプル製品ページに移動します。

   この例では、製品は上部ナビゲーションの女性/ トップス / T 型の下にあります。

1. にスクロール ダウンします。 _マイページビルダー属性_ 情報。

   製品ページ上の属性の位置は、テーマによって決定されます。 Luma テーマでは、新しい属性は製品の説明の直後に配置されます。

   ![[!DNL Page Builder] ストアフロントのおよびテキストエディター属性](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

が完了しました [!DNL Page Builder] カタログのコンテンツに関する演習 作成した作業は保持しておくと、後で参照できます。

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
