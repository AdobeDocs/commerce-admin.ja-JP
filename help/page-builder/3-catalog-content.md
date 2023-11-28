---
title: '''[!DNL Page Builder] ウォークスルーパート 3：カタログコンテンツ`'
description: 製品リストを [!DNL Page Builder] ページに貼り付けます。
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!DNL Page Builder] ウォークスルーパート 3：カタログの内容

この演習では、製品リストをページに追加し、製品ページをカスタマイズし、カスタム属性を作成して [!DNL Page Builder] ワークスペースを製品属性セットに設定します。

![製品リスト](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

この演習は、が完了していることを前提としています。 [第 1 部：シンプルなページ](1-simple-page.md) および [パート 2：ブロック](2-blocks.md)（前提条件やダウンロードしたサンプルファイルを含む） この演習の 3 つの部分を順番に実行します。

## パート 1：製品リストの追加

[!DNL Page Builder] を使用すると、製品リストをステージに簡単に追加できます。 この例では、製品リストがページに直接追加されます。

### 手順 1：ステージに製品リストを追加する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 次を検索： _単純なページ_ 最初の演習で作成し、2 番目の演習で変更した後、「 」を選択します。 **[!UICONTROL Edit]** （内） _[!UICONTROL Action]_列。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Edit with Page Builder]** または、コンテンツプレビュー領域内に配置します。

1. Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、**[!UICONTROL Row]**をステージの上にドラッグします。

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Add Content]** をクリックし、 **[!UICONTROL Products]** プレースホルダーを新しい行に追加します。

   ![製品プレースホルダーを行にドラッグする](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### 手順 2：条件の作成

1. 空の製品コンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![製品ツールボックス](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Select Products By]**&#x200B;を選択します。 `Condition`.

1. 条件を追加します。

   - 次をクリック： _追加_ (![追加アイコン](../assets/icon-add-green-circle.png)) アイコンをクリックします。

   - の下 _[!UICONTROL Product Attribute]_を選択します。**[!UICONTROL Category]**.

     ![条件のカテゴリ属性の選択](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - 次を完了： _[!UICONTROL Category is]..._ 条件の一部を選択するには、その他 (...) アイコンをクリックし、 _選択_ (![選択アイコン](../assets/icon-list-chooser.png)) アイコンをクリックします。

     ![条件の定義](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - カテゴリツリーで、 **女性/トップス** カテゴリを選択し、 **Tees** チェックボックス。

     ![ツリーでのカテゴリの選択](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - チェックマーク (![チェックマークアイコン](../assets/icon-checkmark-green-circle.png)) アイコンをクリックします。

     対応するカテゴリ ID が、条件を完了するためにフィールドに表示されます。

### 手順 3：設定を完了する

1. 次を入力します。 **[!UICONTROL Number of Products to Display]**.

   デフォルトでは、リストには 5 つの製品が表示されます。

1. 必要に応じて、残りの設定を完了します。

   必要に応じて、 [コンテンツを追加 — 製品](products.md) ページを参照してください。

1. 完了したら、「 **[!UICONTROL Save]** 設定を保存し、に戻るには、以下の手順に従います。 [!DNL Page Builder] ワークスペース。

   ![ステージ内の製品リスト](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ ( ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_」セクションにプレビューが表示されます。

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

## 第 2 部：製品ページのカスタマイズ

>[!NOTE]
>
>管理者ユーザーは、 [!UICONTROL Content] 権限 [役割の範囲](../systems/permissions-user-roles.md) 見る [!UICONTROL Edit with Page Builder] ボタンを使用してページビルダーを使用できる。

この練習のこの部分では、製品ページのタブセットの下にビデオを配置して、製品ページをカスタマイズする方法を学びます。 更新するプロセス [カテゴリページ](../catalog/categories-content-settings.md) コンテンツは基本的に同じです。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. この例で使用できるシンプルな製品を見つけ、編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに入力します。

1. 次の隣 _[!UICONTROL Description]_をクリックし、**[!UICONTROL Edit with Page Builder]**.

   ![製品説明のコンテンツ](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   製品の説明が [!DNL Page Builder]を指定した場合、現在の説明はHTMLとして [HTMLコード](html-code.md) コンテナ。 Luma テーマを使用すると、製品の説明が「詳細」タブに表示されます。

1. Adobe Analytics の [!DNL Page Builder] 下のパネル _[!UICONTROL Layout]_、**[!UICONTROL Row]**をステージに追加し、「HTMLコード」コンテナの下に配置します。

   行が正しい位置にある場合に表示される赤いガイドラインを探します。

   ![行をステージにドラッグ](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Media]** をクリックし、 **[!UICONTROL Video]** プレースホルダーを新しい行に追加します。

   ![行のビデオプレースホルダー](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. 空のビデオコンテナの上にマウスポインターを置いてツールボックスを表示し、 _設定_ ( ![設定アイコン](./assets/pb-icon-settings.png){width="20"} ) アイコンをクリックします。

   ![ビデオツールボックス](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Video URL]**.

   このビデオは次の場所でホストできます： [YouTube][1] または [Vimeo][2]. この例のビデオは、YouTubeの次の URL にあります。

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![ビデオの編集](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. 次を入力します。 **[!UICONTROL Maximum Width]** ビデオ表示のピクセル単位で指定します。

   このオプションを空白のままにすると、空きスペースがビデオで埋められます。

1. クリック **[!UICONTROL Save]** 設定を保存し、に戻るには、以下の手順に従います。 [!DNL Page Builder] ワークスペース。

   ![コンテンツステージのビデオ](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. ステージの右上隅で、 _全画面表示を閉じる_ ( ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ) アイコンをクリックします。

   このアイコンをクリックすると、 _[!UICONTROL Content]_」セクションにプレビューが表示されます。

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

ストアフロントでは、ビデオがタブセットの下に表示されます。 モバイルデバイス上でのページの表示を確認するには、ウィンドウのサイズを変更します。

![製品ページに表示されるビデオ](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**おめでとうございます。** 「カタログコンテンツ」チュートリアルの第 2 部を完了しました。 後で参照できるように、作成した作業を保持します。

## パート 3：カスタム属性の追加

以下を使用します。 [!DNL Page Builder] 完全に機能するを追加するためのカスタム属性 [!DNL Page Builder] ワークスペースを製品ページに追加します。このページを使用して、魅力的なコンテンツを作成できます。 この練習のこの部分では、 [!DNL Page Builder] タイプを入力し、カタログ内の製品ページに適用します。 これらの属性について詳しくは、 [製品属性](../catalog/product-attributes.md).

### 手順 1：製品の作成

ライブストアに対する変更を避けるには、説明されているプロパティを使用して製品を作成します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 右上隅で、 **[!UICONTROL Add Product]**.

1. 次のプロパティを使用して製品を作成します。

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
   - [!UICONTROL Categories]：女性/トップス/ティー

1. 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

### 手順 2：カスタム属性の作成

この手順では、2 つの新しいカスタム属性を作成し、 [!DNL Page Builder] およびテキストエディターの入力タイプを使用できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 右上隅で、 **[!UICONTROL Add New Attribute]**.

1. を入力します。 **[!UICONTROL Default Label]** 属性の。

   この例では、 `My Page Builder Attribute` ラベルの

1. 設定 **[!UICONTROL Catalog Input Type for Store Owner]** から `Page Builder`.

   カスタム属性を作成する際に、アプリケーションに最適なエディターを次のいずれかとして指定できます。 `Page Builder` 標準の WYSIWYG `Text Editor`.

   ![[!DNL Page Builder] 入力タイプ](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Attribute Properties]** 」セクションで次の設定を行います。

   - [!UICONTROL Attribute Code]：属性コードを小文字で入力し、スペースの代わりにハイフンを使用します。 この例では、 `my_page_builder_attribute`.
   - [!UICONTROL Scope]：デフォルト値をそのまま使用します。 `Store View`.
   - [!UICONTROL Default Value]：属性のデフォルト値を入力します。
   - 
     [!UICONTROL Unique Value]: `No`
   - 
     [!UICONTROL Add to Column Options]: `No`
   - 
     [!UICONTROL Use in Filter Options]: `Yes`

1. Adobe Analytics の _[!UICONTROL Attribute Information]_左側のパネルで、を選択します。**[!UICONTROL Storefront Properties]**次の設定を行います。

   - 
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - 
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - 
     [!UICONTROL Used in Product Listing]: `Yes`

1. 完了したら、「 **[!UICONTROL Save Attribute]**.

1. 上記の手順を繰り返し、同じ基本プロパティを持つ 2 つ目の属性を、次のようなテキストエディタの入力タイプで作成します。

   - [!UICONTROL Default Label]:My Text Editor 属性
   - [!UICONTROL Catalog Input Type for Store Owner]：テキストエディター
   - 
     [!UICONTROL 属性コード]: `my_text_editor_attribute`

### 手順 3：製品属性セットの更新

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

   この例では、新しい属性を一時的に `default` 属性セット。 この練習の最後で、属性セットから属性を削除し、カタログに影響を与えないようにします。

   >[!NOTE]
   >
   >ライブストアを変更しない場合は、属性セットを更新せずにフォローできます。

1. 次を検索： _[!UICONTROL Default]_属性セットをリストに追加し、ダブルクリックして編集モードで開きます。

1. Adobe Analytics の _未割り当ての属性_ リストで、作成した新しい属性を見つけ、それぞれを _[!UICONTROL Groups]_列、下&#x200B;**[!UICONTROL Content]**.

   内の属性の場所 [!UICONTROL Groups] 列は、ページ上で表示する場所を決定します。

   ![コンテンツグループに追加された新しい属性](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save]** をクリックして、「属性セット」(Attribute Sets) リストに戻ります。

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** リンクをクリックして、無効なキャッシュを更新します。

### 手順 4：製品のアップデート

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品グリッドで、を探します。 _マイ製品_ を開き、編集モードで開きます。

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションに入力します。

   セクションの上部に、製品コンテンツの次の 2 つの標準属性があります。

   - _短い説明_（標準の WYSIWYG を使用） [編集者](../content-design/editor.md).
   - _説明_: [!DNL Page Builder] プレビュー。

   ![製品コンテンツ](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   セクションの下半分までスクロールすると、2 つの属性を作成して割り当てます。

   - _マイ [!DNL Page Builder] 属性_: [!DNL Page Builder] プレビュー。
   - _テキストエディタの属性_：標準の WYSIWYG エディターを使用します。

   ![製品コンテンツの編集](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. Adobe Analytics の **テキストエディタの属性** editor, enter `Text Editor Attribute placeholder text`.

   - 右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. の場合 **マイ Page Builder 属性**&#x200B;をクリックし、 **[!UICONTROL Edit with Page Builder]** 説明テキストを追加します。

   - Adobe Analytics の [!DNL Page Builder] パネル、展開 **[!UICONTROL Elements]** をクリックし、 **[!UICONTROL Text object]** をステージに追加します。

   - 入力 `Page Builder attribute placeholder text`.

   - ステージの右上隅で、 _全画面表示を閉じる_ ( ![全画面表示アイコンを閉じる](./assets/pb-icon-reduce.png){width="20"} ) アイコンをクリックします。

     ![プレースホルダーテキストを含むカスタム属性](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. 上にスクロール **[!UICONTROL Description]**&#x200B;をクリックし、 **[!UICONTROL Edit with Page Builder]**&#x200B;をクリックし、前の手順と同じ方法で使用する任意のテキストを追加します。

1. 製品ページの右上隅で、 **[!UICONTROL Save]** 矢印と選択 **[!UICONTROL Save & Close]**.

1. プロンプトが表示されたら、 **[!UICONTROL Cache Management]** リンクをクリックして、無効なキャッシュを更新します。

### 手順 5：結果を表示する

1. ストアフロントのサンプル製品ページに移動します。

   この例では、製品は上部のナビゲーションの Women/Tops/Tees で検索できます。

1. 下にスクロールして、 _マイ Page Builder 属性_ 情報。

   製品ページ上での属性の位置は、テーマによって決まります。 Luma テーマでは、新しい属性は製品の説明のすぐ後に配置されます。

   ![[!DNL Page Builder] ストアフロントのテキストエディター属性](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

これで [!DNL Page Builder] カタログコンテンツの演習。 後で参照できるように、作成した作業を保持します。

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
