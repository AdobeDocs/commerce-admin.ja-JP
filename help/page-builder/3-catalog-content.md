---
title: '[!DNL Page Builder] チュートリアル第 3 部：カタログのコンテンツ'
description: ページに製品リストを追加する方法  [!DNL Page Builder]  説明します。
exl-id: f2a0dc29-6d8f-4b97-a947-72659c01d0cb
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1494'
ht-degree: 0%

---

# [!DNL Page Builder] チュートリアル第 3 部：カタログのコンテンツ

この演習では、製品リストをページに追加したり、製品ページをカスタマイズしたり、[!DNL Page Builder] ワークスペースを製品属性セットに追加するカスタム属性を作成したりするのがいかに簡単かを示します。

![&#x200B; 製品リスト &#x200B;](./assets/pb-add-content-products-list.png){width="600" zoomable="yes"}

この演習では、前提条件やダウンロード済みのサンプルファイルを含め、[&#x200B; パート 1：簡単なページ &#x200B;](1-simple-page.md) および [&#x200B; パート 2：ブロック &#x200B;](2-blocks.md) が完了していることを前提としています。 この演習の 3 つの部分を順番に実行します。

## パート 1：製品リストの追加

[!DNL Page Builder] を使用すると、製品リストをステージに簡単に追加できます。 この例では、製品リストがページに直接追加されます。

### 手順 1：ステージへの製品リストの追加

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. 最初の演習で作成し、2 番目の演習で変更した _シンプルなページ_ を見つけ、**[!UICONTROL Edit]** の列の _[!UICONTROL Action]_&#x200B;を選択します。

1. ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**[!UICONTROL Content]**」セクションを展開し、コンテンツプレビュー領域 **[!UICONTROL Edit with Page Builder]** または内側をクリックします。

1. [!DNL Page Builder] の下の _[!UICONTROL Layout]_&#x200B;パネルで、**[!UICONTROL Row]**&#x200B;をステージの上部にドラッグします。

1. [!DNL Page Builder] パネルで **[!UICONTROL Add Content]** を展開し、**[!UICONTROL Products]** プレースホルダーを新しい行にドラッグします。

   ![&#x200B; 製品プレースホルダーを行にドラッグ &#x200B;](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

### 手順 2：条件を作成する

1. 空の products コンテナにポインタを合わせてツールボックスを表示し、「_設定_」（![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![&#x200B; 製品ツールボックス &#x200B;](./assets/pb-add-content-products-toolbox.png){width="600" zoomable="yes"}

1. **[!UICONTROL Select Products By]** の場合は、「`Condition`」を選択します。

1. 条件を追加します。

   - _追加_ （![&#x200B; 追加アイコン &#x200B;](../assets/icon-add-green-circle.png)）アイコンをクリックします。

   - 「_[!UICONTROL Product Attribute]_」で、「**[!UICONTROL Category]**」を選択します。

     ![&#x200B; 条件のカテゴリ属性の選択 &#x200B;](./assets/pb-add-content-products-settings-condition.png){width="600" zoomable="yes"}

   - 条件の _[!UICONTROL Category is]..._ の一部を完了するには、その他（...）アイコンをクリックし、_選択_ （![&#x200B; 選択アイコン &#x200B;](../assets/icon-list-chooser.png)）アイコンをクリックします。

     ![&#x200B; 条件の定義 &#x200B;](./assets/pb-add-content-products-settings-condition-category-is.png){width="600" zoomable="yes"}

   - カテゴリツリーで、**Women > Tops** カテゴリにドリルダウンし、「**Tees**」チェックボックスを選択します。

     ![&#x200B; ツリーでのカテゴリの選択 &#x200B;](./assets/pb-add-content-products-settings-condition-category-tree.png){width="600" zoomable="yes"}

   - チェックマーク（![&#x200B; チェックマークアイコン &#x200B;](../assets/icon-checkmark-green-circle.png)）アイコンをクリックします。

     対応するカテゴリ ID がフィールドに表示され、条件が完了します。

### 手順 3：設定を完了する

1. **[!UICONTROL Number of Products to Display]** を入力します。

   デフォルトでは、リストには 5 つの製品が表示されます。

1. 必要に応じて、残りの設定を完了します。

   必要に応じて、[&#x200B; コンテンツを追加 – 製品 &#x200B;](products.md) ページの最後にあるフィールドの説明を参照するために使用します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックして設定を保存し、[!DNL Page Builder] ワークスペースに戻ります。

   ![&#x200B; ステージ内の商品リスト &#x200B;](./assets/pb-add-content-products-list-stage.png){width="600" zoomable="yes"}

1. ステージの右上隅にある _フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる &#x200B;](./assets/pb-icon-reduce.png){width="20"}）アイコンをクリックします。

   このアイコンをクリックすると、ページの「_[!UICONTROL Content]_」セクションに戻り、プレビューが表示されます。

1. 右上隅の **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

## 第 2 部：製品ページのカスタマイズ

>[!NOTE]
>
>管理者ユーザーが [!UICONTROL Content] のボタンを表示し、ページビルダーを使用するには、[&#x200B; 役割の範囲 &#x200B;](../systems/permissions-user-roles.md) に対する [!UICONTROL Edit with Page Builder] 権限が必要です。

演習のこの部分では、製品ページ上の一連のタブの下にビデオを配置することで、製品ページを簡単にカスタマイズする方法を説明します。 [&#x200B; カテゴリページ &#x200B;](../catalog/categories-content-settings.md) コンテンツを更新する手順は、基本的に同じです。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. この例で使用できる簡単な製品を見つけて、編集モードで開きます。

1. 下にスクロールして、「![」セクションの &#x200B;](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Content]** を展開します。

1. 「_[!UICONTROL Description]_」の横にある「**[!UICONTROL Edit with Page Builder]**」をクリックします。

   ![&#x200B; 製品説明の内容 &#x200B;](./assets/pb-catalog-product-content.png){width="600" zoomable="yes"}

   商品の説明が以前に [!DNL Page Builder] なしで入力された場合、現在の説明は、[HTML コード &#x200B;](html-code.md) コンテナでHTMLとして表示されます。 Luma テーマを使用すると、製品の説明が「詳細」タブに表示されます。

1. [!DNL Page Builder] の下の _[!UICONTROL Layout]_&#x200B;パネルで、**[!UICONTROL Row]**&#x200B;をステージにドラッグして、HTML コードコンテナの下に配置します。

   行が正しい位置にあるときに表示される赤いガイドラインを探します。

   ![&#x200B; 行のステージへのドラッグ &#x200B;](./assets/catalog-product-content-stage-row-drag.png){width="600" zoomable="yes"}

1. [!DNL Page Builder] パネルで **[!UICONTROL Media]** を展開し、**[!UICONTROL Video]** プレースホルダーを新しい行にドラッグします。

   ![&#x200B; 行内のビデオプレースホルダー &#x200B;](./assets/tutorial3-product-drag-video.png){width="600" zoomable="yes"}

1. 空のビデオコンテナにカーソルを合わせてツールボックスを表示し、_設定_ （![&#x200B; 設定アイコン &#x200B;](./assets/pb-icon-settings.png){width="20"}）アイコンを選択します。

   ![&#x200B; ビデオツールボックス &#x200B;](./assets/pb-tutorial3-product-video-toolbox.png){width="500" zoomable="yes"}

1. **[!UICONTROL Video URL]** を入力します。

   ビデオは [YouTube](https://www.youtube.com/) または [Vimeo](https://vimeo.com/) でホストできます。 この例のビデオは、YouTubeの次の URL で見つかります。

   `https://www.youtube.com/watch?v=ZpFrNyD4100`

   ![&#x200B; ビデオの編集 &#x200B;](./assets/pb-tutorial3-product-edit-video.png){width="500" zoomable="yes"}

1. ビデオディスプレイの **[!UICONTROL Maximum Width]** をピクセル単位で入力します。

   このオプションを空白のままにすると、ビデオは使用可能なスペースいっぱいに表示されます。

1. 「**[!UICONTROL Save]**」をクリックして設定を保存し、[!DNL Page Builder] ワークスペースに戻ります。

   ![&#x200B; コンテンツステージのビデオ &#x200B;](./assets/pb-tutorial3-product-video.png){width="600" zoomable="yes"}

1. ステージの右上隅にある _フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる &#x200B;](./assets/pb-icon-reduce.png){width="20"}）アイコンをクリックします。

   このアイコンをクリックすると、ページの「_[!UICONTROL Content]_」セクションに戻り、プレビューが表示されます。

1. 右上隅の **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

ストアフロントでは、ビデオは一連のタブの下に表示されます。 モバイルデバイスでのページの外観を確認するには、ウィンドウのサイズを変更します。

![&#x200B; 製品ページの動画 &#x200B;](./assets/pb-tutorial3-product-video-storefront.png){width="600" zoomable="yes"}

**これで完了です。** カタログのコンテンツ チュートリアルの 2 番目のパートを完了しました。 作成した作業は保持しておくと、後で参照できます。

## 第 3 部：カスタム属性の追加

[!DNL Page Builder] カスタム属性を使用して、魅力的なコンテンツの作成に使用できる、完全に機能する [!DNL Page Builder] ワークスペースを製品ページに追加します。 演習のこのパートでは、[!DNL Page Builder] 入力タイプを使用してカスタム属性を作成し、カタログの製品ページに適用する方法を学びます。 これらの属性について詳しくは、[&#x200B; 製品属性 &#x200B;](../catalog/product-attributes.md) を参照してください。

### 手順 1：製品を作成する

ライブストアが変更されないようにするには、説明されたプロパティを使用して製品を作成します。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 右上隅の「**[!UICONTROL Add Product]**」をクリックします。

1. 次のプロパティを持つ製品を作成します。

   - &#x200B;
     [!UICONTROL 属性セット]: Default
   - [!UICONTROL Product Name]: My Product
   - &#x200B;
     [!UICONTROL SKU]: Tutorial
   - &#x200B;
     [!UICONTROL Price]: 75.00
   - &#x200B;
     [!UICONTROL Quantity]: 100
   - [!UICONTROL Stock Status]：在庫あり
   - &#x200B;
     [!UICONTROL Weight]: 1
   - [!UICONTROL Categories]：女性/トップス/T 型

1. 右上隅の **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

### 手順 2：カスタム属性の作成

この手順では、[!DNL Page Builder] とテキストエディターの入力タイプを使用する方法を示す 2 つの新しいカスタム属性を作成します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**&#x200B;に移動します。

1. 右上隅の「**[!UICONTROL Add New Attribute]**」をクリックします。

1. 属性の **[!UICONTROL Default Label]** を入力します。

   この例では、ラベルに `My Page Builder Attribute` を使用します。

1. **[!UICONTROL Catalog Input Type for Store Owner]** を `Page Builder` に設定します。

   カスタム アトリビュートを作成する場合は、`Page Builder` または標準のWYSIWYG `Text Editor` として、アプリケーションに最適なエディタを指定できます。

   ![[!DNL Page Builder] 入力タイプ &#x200B;](./assets/pb-attribute-page-builder.png){width="600" zoomable="yes"}

1. ![&#x200B; のセクションの &#x200B;](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Advanced Attribute Properties]** を展開し、次の設定を行います。

   - [!UICONTROL Attribute Code]：属性コードをスペースではなくハイフンを使用して、小文字で入力します。 この例では、`my_page_builder_attribute` を使用します。
   - [!UICONTROL Scope]: デフォルト値 `Store View` を使用します。
   - [!UICONTROL Default Value]：属性のデフォルト値を入力します。
   - &#x200B;
     [!UICONTROL Unique Value]: `No`
   - &#x200B;
     [!UICONTROL Add to Column Options]: `No`
   - &#x200B;
     [!UICONTROL Use in Filter Options]: `Yes`

1. 左側の _[!UICONTROL Attribute Information]_&#x200B;パネルで「**[!UICONTROL Storefront Properties]**」を選択し、次の設定を行います。

   - &#x200B;
     [!UICONTROL Use for Promo Rule Conditions]: `Yes`
   - &#x200B;
     [!UICONTROL Visible on Catalog Pages on Storefront]: `Yes`
   - &#x200B;
     [!UICONTROL Used in Product Listing]: `Yes`

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

1. 上記の手順を繰り返して、同じ基本プロパティを持ち、テキストエディター入力タイプが次のような 2 番目の属性を作成します。

   - [!UICONTROL Default Label]: My Text Editor 属性
   - [!UICONTROL Catalog Input Type for Store Owner]：テキストエディター
   - &#x200B;
     [!UICONTROL 属性コード]: `my_text_editor_attribute`

### 手順 3：製品属性セットの更新

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Attribute Set]**&#x200B;に移動します。

   この例では、新しい属性を一時的に `default` 属性セットに追加します。 この演習の最後では、カタログに影響を与えないように、属性セットから属性を削除します。

   >[!NOTE]
   >
   >ライブストアを変更しない場合は、属性セットを更新せずにそれに従うことができます。

1. リストで _[!UICONTROL Default]_&#x200B;属性セットを見つけてダブルクリックし、編集モードで開きます。

1. _未割り当て属性_ リストで、作成した新しい属性を見つけて、_[!UICONTROL Groups]_&#x200B;の下の&#x200B;**[!UICONTROL Content]**&#x200B;の列にドラッグします。

   [!UICONTROL Groups] 列内の属性の場所によって、ページ上の表示場所が決まります。

   ![&#x200B; コンテンツグループに追加された新しい属性 &#x200B;](./assets/pb-product-attribute-set.png){width="600" zoomable="yes"}

1. 「属性セット」リストに戻るには、「**[!UICONTROL Save]**」をクリックします。

1. プロンプトが表示されたら、ページ上部の **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

### 手順 4：製品をアップデートする

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品グリッドで _My Product_ を探し、編集モードで開きます。

1. 下にスクロールして、「![」セクションの &#x200B;](../assets/icon-display-expand.png) 展開セレクター **[!UICONTROL Content]** を展開します。

   セクションの上部には、製品コンテンツの 2 つの標準属性があります。

   - _簡単な説明_：標準のWYSIWYG [&#x200B; エディター &#x200B;](../content-design/editor.md) を使用します。
   - _説明_:[!DNL Page Builder] プレビューが表示されます。

   ![&#x200B; 製品コンテンツ &#x200B;](./assets/pb-product-content-edit-with-page-builder.png){width="600" zoomable="yes"}

   セクションの下半分までスクロールすると、作成して割り当てた属性が 2 つあります。

   - _My [!DNL Page Builder] Attribute_:[!DNL Page Builder] プレビューを表示します。
   - _My Text Editor Attribute_：標準のWYSIWYG エディターを使用します。

   ![&#x200B; 製品コンテンツの編集 &#x200B;](./assets/pb-product-content-my-attributes.png){width="600" zoomable="yes"}

1. **My Text Editor Attribute** エディタで、`Text Editor Attribute placeholder text` と入力します。

   - 右上隅の **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

1. 「**マイページビルダー属性**」で「**[!UICONTROL Edit with Page Builder]**」をクリックし、説明テキストを追加します。

   - [!DNL Page Builder] パネルで **[!UICONTROL Elements]** を展開し、**[!UICONTROL Text object]** をステージにドラッグします。

   - `Page Builder attribute placeholder text` と入力します。

   - ステージの右上隅にある _フルスクリーンを閉じる_ （![&#x200B; フルスクリーンアイコンを閉じる &#x200B;](./assets/pb-icon-reduce.png){width="20"}）アイコンをクリックします。

     ![&#x200B; プレースホルダーテキストを含むカスタム属性 &#x200B;](./assets/pb-product-content-attributes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Description]** までスクロールし、**[!UICONTROL Edit with Page Builder]** をクリックし、前の手順と同じ方法を使用して任意のテキストを追加します。

1. 製品ページの右上隅にある **[!UICONTROL Save]** 矢印をクリックし、「**[!UICONTROL Save & Close]**」を選択します。

1. プロンプトが表示されたら、ページ上部のメッセージに含まれている **[!UICONTROL Cache Management]** リンクをクリックし、無効なキャッシュを更新します。

### 手順 5：結果の表示

1. ストアフロントのサンプル製品ページに移動します。

   この例では、製品は上部ナビゲーションの女性/ トップス / T 型の下にあります。

1. _My Page Builder 属性_ 情報までスクロールします。

   製品ページ上の属性の位置は、テーマによって決定されます。 Luma テーマでは、新しい属性は製品の説明の直後に配置されます。

   ストアフロントの ![[!DNL Page Builder] およびテキストエディター属性 &#x200B;](./assets/pb-storefront-product-attribute.png){width="600" zoomable="yes"}

[!DNL Page Builder] カタログのコンテンツの演習を完了しました。 作成した作業は保持しておくと、後で参照できます。
