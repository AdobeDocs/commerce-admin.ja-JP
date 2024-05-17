---
title: ダウンロード可能な製品
description: デジタルファイルとして配信できるダウンロード可能な製品の作成方法を説明します。
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# ダウンロード可能な製品

ダウンロード可能な製品とは、電子書籍、音楽、ビデオ、ソフトウェアアプリケーション、アップデートなど、ファイルとして提供できるすべての製品です。 あなたは販売のためにアルバムを提供し、各曲を個別に販売することができます。 ダウンロード可能な製品を使用して、製品カタログの電子バージョンを配信することもできます。

ダウンロードは購入後まで利用できないので、書籍からの抜粋、オーディオファイルからのクリップ、ビデオからのトレーラーなどのサンプルを提供できます。 サンプルとは、お客様が商品を購入する前に試すことができるものです。 ダウンロード可能にしたファイルは、サーバーにアップロードすることも、別のサーバーからアップロードすることもできます。

![ダウンロード可能な製品](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

ダウンロード可能な製品は、顧客がアカウントにログインしてリンクを受け取るか、メールで送信して他の人と共有するように設定できます。 設定では、ダウンロードが使用可能になる前の注文のステータス、デフォルト値、その他の配信オプションが設定されます。 ダウンロード可能なカタログの追加を計画する際は、次の点に注意してください。

- ダウンロード可能な製品は、サーバーにアップロードすることも、インターネット上の別のサーバーからにリンクすることもできます。

- 顧客が製品をダウンロードできる回数を指定できます。

- ダウンロード可能な製品を購入したお客様は、チェックアウト前にログインする必要が生じる場合があります。

- ダウンロード可能な製品の配信は、注文が次のいずれかの場合に行うことができます `Pending` または `Invoiced` ステータス。

- ダウンロード可能な製品は出荷されないので、 _送料_ ダウンロード可能な商品のみがカートに含まれている場合、チェックアウトのステップはスキップされます。


## ダウンロードオプションの設定

ダウンロード可能な構成設定は、ダウンロード可能な製品のデフォルト値と配信オプションを決定し、ゲストがダウンロードを購入できるかどうかを指定します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Downloadable Product Options]_セクション。

   ![ダウンロード可能な製品オプション](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   これらの設定オプションの詳細なリストについては、を参照してください [_ダウンロード可能な製品オプション_](../configuration-reference/catalog/catalog.md#downloadable-product-options) が含まれる _設定リファレンス_.

1. ダウンロードが使用可能になったときの注文プロセスのステータスを判断するには、次のように設定します **[!UICONTROL Order Item Status to Enable Downloads]** を次のいずれかに変更します。

   - `Pending`
   - `Invoiced`

1. 1 人の顧客が実行できるダウンロード数のデフォルト制限を設定するには、次の数を入力します **[!UICONTROL Default Maximum Number of Downloads]**.

1. を設定 **[!UICONTROL Shareable]** を次のいずれかに変更します。

   - `Yes`  – 顧客がダウンロードリンクを他のユーザーにメールで送信できます。
   - `No`  – 顧客が自分のアカウントにログインしてダウンロードリンクにアクセスするように求めることで、顧客がダウンロードリンクを他のユーザーと共有できないようにします。

1. の場合 **[!UICONTROL Default Sample Title]**&#x200B;を選択し、選択したサンプルの上に表示する見出しを入力します。

   ![サンプルタイトル](./assets/product-downloadable-config-sample-title.png){width="400"}

1. の場合 **[!UICONTROL Default Link Title]**：ダウンロードリンクに使用するデフォルトのテキストを入力します。

1. ダウンロードリンクを新しいブラウザーウィンドウで開く場合は、次のように設定します。 **[!UICONTROL Opens Links in New Window]** 対象： `Yes`.

   この設定は、ストアへのブラウザーウィンドウを開いたままにするために使用されます。

1. ダウンロード可能なコンテンツの配信方法を決定するには、次のように設定します **[!UICONTROL Use Content Disposition]** を次のいずれかに変更します。

   - `Attachment` - ダウンロードリンクをメールで添付ファイルとして配信します。
   - `Inline` - ダウンロードリンクを Web ページ上のリンクとして配信します。

1. 購入者が顧客アカウントに登録し、ダウンロードを購入する前にログインする必要がある場合は、次のように設定します **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## ダウンロード可能な製品を作成

以下の手順は、を使用してダウンロード可能な製品を作成するプロセスを示しています。 [製品テンプレート](attribute-sets.md)、必須フィールド、基本設定です。 各必須フィールドには、赤いアスタリスク（`*`）に設定します。 基本を完了したら、必要に応じて他の製品設定を完了できます。

>[!NOTE]
>
>ダウンロード可能なファイル名には、文字および数字を含めることができます。 ダッシュまたはアンダースコア文字を使用して、単語間のスペースを表すことができます。 ファイル名に無効な文字がある場合は、アンダースコアに置き換えられます。

### 手順 1：製品タイプの選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 日 _[!UICONTROL Add Product]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ）メニューを選択し、 `Downloadable Product`.

   ![ダウンロード可能な製品を追加](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

サンプルデータには以下が含まれます [属性セット](attribute-sets.md) 呼び出し _ダウンロード可能_ ダウンロード可能な製品の特別なフィールドがあります。 製品を保存する前に、既存のテンプレートを使用することも、別のテンプレートを作成することもできます。

製品のテンプレートとして使用する属性セットを選択するには、次のいずれかの操作を行います。

- の場合 **[!UICONTROL Search]**&#x200B;属性セットの名前を入力します。

- リストで、 `Downloadable` 属性セット。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### 手順 3：必要な設定を完了する

1. を入力 **[!UICONTROL Product Name]**.

1. デフォルトを使用 **[!UICONTROL SKU]** これは製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだ整っていないので、を設定します **[!UICONTROL Enable Product]** 対象： `No`.

1. click **[!UICONTROL Save]** そして続けて。

   商品を保存すると、 [ストア表示](introduction.md#product-scope) 選択が左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品の入手先。

   ![ストア表示を選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 手順 4：基本設定を完了する

1. を設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

1. を入力 **[!UICONTROL Quantity]** 在庫がある商品の。

   次のことに注意してください。

   - デフォルトでは **[!UICONTROL Stock Status]** はに設定されています。 `Out of Stock`.

   - ダウンロード可能な製品は出荷されないので、 **[!UICONTROL Weight]** フィールドは使用されません。 この機能を有効にすると、 [シンプル製品](product-create-simple.md) および _これはダウンロード可能な製品ですか？_ tab キーは使用できません。

   >[!NOTE]
   >
   >有効にする場合 [Inventory management](../inventory-management/introduction.md)、単一ソースのマーチャントがこのセクションで数量を設定します。 マルチソースマーチャントは、「ソース」セクションでソースと数量を追加します。 以下を参照してください _ソースと数量の割り当て（Inventory management）_ セクション。

1. デフォルトを使用 **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. で製品を使用するには [新製品のリスト](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. 割り当てる _[!UICONTROL Categories]_製品に移動するには、**[!UICONTROL Select…]**次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致するものが見つかるまで、ボックスに入力を開始します。

   - 割り当てる各カテゴリのチェックボックスを選択します。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - を入力 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**。このオブジェクトの位置は、 [メニュー構造](category-root.md).

   - クリック **[!UICONTROL Create Category]**.

1. を設定 **[!UICONTROL Format]** を次のいずれかに変更します。

   - `Download`
   - `DVD`

   必要に応じて、を編集できます [属性](attribute-product-create.md) をクリックして値を追加します。

   製品を説明する追加の属性がある場合があります。 選択は属性セットによって異なり、後で完了できます。

#### ソースと数量の割り当て（[!DNL Inventory Management]）

{{$include /help/_includes/inventory-assign-sources.md}}

### 手順 5：ダウンロード可能な情報の入力

下にスクロール、展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Downloadable Information]_「」セクションを選択し、**[!UICONTROL Is this downloadable product?]**チェックボックス。

有効にすると、 _[!UICONTROL Downloadable Information]_セクションは 2 つの部分で構成されています。 最初のパートでは各ダウンロードリンクについて説明し、2 番目のパートでは各サンプルファイルについて説明します。 これらの多くのオプションのデフォルト値は、 [設定](#configure-the-download-options).

![ダウンロード可能な情報](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### リンクを完成させる

1. が含まれる _[!UICONTROL Links]_「」セクションに、**[!UICONTROL Title]**をダウンロードリンクの見出しとして使用する。

1. 該当する場合、 **[!UICONTROL Links can be purchased separately]** チェックボックス。

1. クリック **[!UICONTROL Add Link]** 次の手順を実行します。

   - を入力 **[!UICONTROL Title]** および **[!UICONTROL Price]** （ダウンロード）。

   - 両方について **[!UICONTROL File]** および **[!UICONTROL Sample]** ファイルをダウンロードするには、次のいずれかの配布方法を選択します。

      - `Upload File`  – 配布ファイルをサーバーにアップロードする場合は、この方法を選択します。 ファイルを参照し、アップロードするファイルを選択します。
      - `URL`  – この方法を選択して、URL から配布ファイルにアクセスします。 ダウンロードファイルの完全な URL を入力します。

   >[!NOTE]
   >
   >外部リソースへのリンクは、ダウンロード可能な製品として使用することはできません。 有効なリンクドメインは、 `env.php` ファイル（ [env.php リファレンス](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) が含まれる _設定ガイド_）に設定します。

   - を設定 **[!UICONTROL Shareable]** を次のいずれかに変更します。

      - `No`  – 顧客がダウンロードリンクにアクセスするには、アカウントにログインする必要があります。

      - `Yes`  – 顧客が他のユーザーと共有できるリンクをメールで送信します。

      - `Use Config`  – で指定されたメソッドを使用します [ダウンロード可能な製品オプション](../configuration-reference/catalog/catalog.md) 設定。

   - 次のいずれかの操作を行います。

      - 顧客ごとのダウンロードを制限するには、次の最大数を入力します **[!UICONTROL Max. Downloads]**.
      - 無制限にダウンロードできるようにするには、 **[!UICONTROL Unlimited]** チェックボックス。

   ![リンクの詳細](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. 別のリンクを追加するには、をクリックします **[!UICONTROL Add Link]** 上記の手順を繰り返します。

#### サンプルを完成させる

1. が含まれる _[!UICONTROL Samples]_「」セクションに、**[!UICONTROL Title]**をサンプルの見出しとして使用します。

1. 各サンプルの情報を入力するには、 **[!UICONTROL Add Link]**.

   ![サンプル](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. リンクの詳細を次のように入力します。

   - を入力 **[!UICONTROL Title]** 個々のサンプルの。

   - 次のいずれかの配布方法を選択します。

      - `Upload File`  – 配布ファイルをサーバーにアップロードする場合は、この方法を選択します。 ファイルを参照し、アップロードするファイルを選択します。
      - `URL`  – この方法を選択して、URL から配布ファイルにアクセスします。 ダウンロードファイルの完全な URL を入力します。

   - 別のサンプルを追加するには、をクリックします **[!UICONTROL Add Link]** 上記の手順を繰り返します。

   - サンプルの順序を変更するには、 _変更依頼_ （ ![位置コントローラ](../assets/icon-sort-order.png) ） アイコンをクリックし、サンプルを新しい位置にドラッグします。

### 手順 6：製品情報の入力

下にスクロールして、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイトの製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

### 手順 7：製品を公開する

カタログに製品を公開する準備が整ったら、次のように設定します **[!UICONTROL Enable Product]** 対象： `Yes` 次のいずれかの操作を行います。

**メソッド 1:** 保存とプレビュー

- 右上隅のをクリックします。 **[!UICONTROL Save]**.

- ストアで商品を表示するには、次を選択します **[!UICONTROL Customer View]** 日 _Admin_ （ ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ） メニューを使用できます。

  ストアが新しいブラウザータブで開きます。

  ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**メソッド 2:** 保存して閉じる

日 _[!UICONTROL Save]_（ ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ） メニュー、を選択&#x200B;**[!UICONTROL Save & Close]**.

## ストアフロントの経験

顧客アカウントダッシュボードで、 _[!UICONTROL My Downloadable Products]_ダウンロード可能な製品の各注文へのページリンク。 ダウンロードは、注文が完了すると、顧客のアカウントから利用できるようになります。

![ダウンロード可能な製品](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

以下の表で、 _ダウンロード可能な製品_ 値：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Order#] | この [順序](../stores-purchase/orders.md) ダウンロード可能な製品が購入された。 注文詳細へのリンクを提供します。 |
| [!UICONTROL Date] | オーダー作成日。 |
| [!UICONTROL Title] | 注文と共に購入されたダウンロード可能な製品の名前。 ダウンロード可能な製品へのリンクを提供します。 |
| [!UICONTROL Status] | 注文処理ステータス。 |
| [!UICONTROL Remaining Downloads] | ダウンロードされた製品の使用可能なダウンロードの数。 |

_**アカウントダッシュボードから製品ファイルをダウンロードするには**_

1. アカウントダッシュボードで、顧客は次のいずれかを選択します **[!UICONTROL My Downloadable Products]**.

1. リスト内の順序を検索し、タイトルの後のリンクをクリックします。

1. ダウンロードウィンドウの右下隅にあるをクリックします _download_ アイコン。

1. ダウンロードした場所でファイルを検索し、目的の場所にファイルを保存します。
