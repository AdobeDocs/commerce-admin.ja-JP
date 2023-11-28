---
title: ダウンロード可能な製品
description: ダウンロード可能な製品を作成し、デジタルファイルとして配信する方法を説明します。
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# ダウンロード可能な製品

ダウンロード可能な製品は、eBook、音楽、ビデオ、ソフトウェアアプリケーション、更新など、ファイルとして配信できるものです。 各曲を個別に販売するアルバムを提供できます。 ダウンロード可能な製品を使用して、製品カタログの電子バージョンを配信することもできます。

ダウンロードは購入後まで利用できないので、本からの抜粋、オーディオファイルからのクリップ、ビデオからのトレーラーなどのサンプルを提供できます。 サンプルとは、顧客が商品を購入する前に試すことができるものです。 ダウンロード可能にするファイルは、サーバーにアップロードすることも、別のサーバーからアップロードすることもできます。

![ダウンロード可能な製品](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

ダウンロード可能な製品は、顧客がリンクを受け取るためにアカウントにログインすることを要求するように設定したり、電子メールで送信して他のユーザーと共有したりできます。 ダウンロードが可能になる前の注文のステータス、デフォルト値、その他の配信オプションが設定で指定されます。 ダウンロード可能なカタログの追加を計画する際は、次の点に注意してください。

- ダウンロード可能な製品は、サーバーにアップロードしたり、インターネット上の別のサーバーからにリンクしたりできます。

- 顧客が製品をダウンロードできる回数を指定できます。

- ダウンロード可能な製品を購入したお客様は、チェックアウトの前にログインする必要があります。

- ダウンロード可能な製品の配信は、注文が `Pending` または `Invoiced` ステータス。

- ダウンロード可能な製品は出荷されないので、 _送料_ 買い物かごにダウンロード可能な製品のみが含まれている場合は、チェックアウトのステップがスキップされます。


## ダウンロードオプションの設定

ダウンロード可能な設定によって、ダウンロード可能な製品のデフォルト値と配信オプションが決まり、ゲストがダウンロードを購入できるかどうかを指定します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Downloadable Product Options]_」セクションに入力します。

   ![ダウンロード可能な製品オプション](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   これらの設定オプションの詳細なリストについては、 [_ダウンロード可能な製品オプション_](../configuration-reference/catalog/catalog.md#downloadable-product-options) （内） _設定リファレンス_.

1. ダウンロードが利用可能になったときの注文プロセスのステータスを判断するには、 **[!UICONTROL Order Item Status to Enable Downloads]** を次のいずれかに変更します。

   - `Pending`
   - `Invoiced`

1. 1 人の顧客が実行できるダウンロード数のデフォルトの制限を設定するには、 **[!UICONTROL Default Maximum Number of Downloads]**.

1. 設定 **[!UICONTROL Shareable]** を次のいずれかに変更します。

   - `Yes` ：ダウンロードリンクを他のユーザーに電子メールで送信することを許可します。
   - `No`  — のお客様がダウンロードリンクにアクセスするためにアカウントにログインする必要があるので、ダウンロードリンクを他のユーザーと共有できなくなります。

1. の場合 **[!UICONTROL Default Sample Title]**」に、選択したサンプルの上に表示する見出しを入力します。

   ![サンプルタイトル](./assets/product-downloadable-config-sample-title.png){width="400"}

1. の場合 **[!UICONTROL Default Link Title]**&#x200B;に設定する場合は、ダウンロードリンクに使用するデフォルトのテキストを入力します。

1. ダウンロードリンクを新しいブラウザーウィンドウで開く場合は、 **[!UICONTROL Opens Links in New Window]** から `Yes`.

   この設定は、ストアを開いたままにブラウザーウィンドウを開くために使用されます。

1. ダウンロード可能なコンテンツの配信方法を決定するには、 **[!UICONTROL Use Content Disposition]** を次のいずれかに変更します。

   - `Attachment`  — ダウンロードリンクを電子メールで添付ファイルとして配信します。
   - `Inline`  — ダウンロードリンクを Web ページ上のリンクとして配信します。

1. ダウンロードを購入する前に、購入者が顧客アカウントに登録してログインする必要がある場合は、 **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ダウンロード可能な製品の作成

以下の手順は、 [製品テンプレート](attribute-sets.md)、必須フィールドおよび基本設定。 各必須フィールドには赤いアスタリスク (`*`) をクリックします。 基本事項を完了したら、必要に応じて、他の製品設定を完了できます。

>[!NOTE]
>
>ダウンロード可能なファイル名には、文字や数字を含めることができます。 単語間のスペースを表すために、ダッシュ文字またはアンダースコア文字を使用できます。 ファイル名に無効な文字が含まれている場合は、アンダースコアに置き換えられます。

### 手順 1：製品タイプの選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 次の日： _[!UICONTROL Add Product]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューを使用して、 `Downloadable Product`.

   ![ダウンロード可能な製品を追加](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### 手順 2：属性セットの選択

サンプルデータには、 [属性セット](attribute-sets.md) 呼び出し _ダウンロード可能_ ダウンロード可能な製品用の特別なフィールドを持つ 製品を保存する前に、既存のテンプレートを使用するか、別のテンプレートを作成することができます。

製品のテンプレートとして使用する属性セットを選択するには、次のいずれかの操作を行います。

- の場合 **[!UICONTROL Search]**」で、属性セットの名前を入力します。

- リストで、 `Downloadable` 属性セット。

フォームが更新され、変更が反映されます。

![属性セットを選択](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### 手順 3：必要な設定を完了する

1. 次を入力します。 **[!UICONTROL Product Name]**.

1. デフォルトを受け入れる **[!UICONTROL SKU]** 製品名に基づくか、別の名前を入力します。

1. 製品を入力 **[!UICONTROL Price]**.

1. 製品の公開準備がまだできていないので、を設定します。 **[!UICONTROL Enable Product]** から `No`.

1. click **[!UICONTROL Save]** 続行します。

   製品を保存すると、 [ストア表示](introduction.md#product-scope) セレクタが左上隅に表示されます。

1. を選択します。 **[!UICONTROL Store View]** 製品を使用できる場所。

   ![ストア表示の選択](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 手順 4：基本設定の完了

1. 設定 **[!UICONTROL Tax Class]** を次のいずれかに変更します。

   - `None`
   - `Taxable Goods`

1. 次を入力します。 **[!UICONTROL Quantity]** 保管されている製品の。

   次の点に注意してください。

   - デフォルトでは、 **[!UICONTROL Stock Status]** が `Out of Stock`.

   - ダウンロード可能な製品は出荷されないので、 **[!UICONTROL Weight]** フィールドが使用されていません。 この機能を有効にすると、 [シンプルな製品](product-create-simple.md) そして _これはダウンロード可能な製品ですか？_ タブは使用できません。

   >[!NOTE]
   >
   >有効にした場合 [Inventory management](../inventory-management/introduction.md)を使用する場合、単一ソースのマーチャントがこのセクションで数量を設定します。 複数ソースのマーチャントは、「ソース」セクションにソースと数量を追加します。 次を参照してください。 _ソースと数量の割り当て (Inventory management)_ 」セクションに入力します。

1. デフォルトを受け入れる **[!UICONTROL Visibility]** の設定 `Catalog, Search`.

1. 製品を [新製品のリスト](../content-design/widget-new-products-list.md)を選択し、 **[!UICONTROL Set Product as New]** チェックボックス。

1. 割り当てるには _[!UICONTROL Categories]_を製品に対して、**[!UICONTROL Select…]**」ボックスに移動し、次のいずれかの操作を行います。

   **既存のカテゴリを選択**:

   - 一致が見つかるまで、ボックスに入力します。

   - 割り当てる各カテゴリのチェックボックスをオンにします。

   **カテゴリの作成**:

   - クリック **[!UICONTROL New Category]**.

   - 次を入力します。 **[!UICONTROL Category Name]** を選択し、 **[!UICONTROL Parent Category]**：内での位置を決定します。 [メニュー構造](category-root.md).

   - クリック **[!UICONTROL Create Category]**.

1. 設定 **[!UICONTROL Format]** を次のいずれかに変更します。

   - `Download`
   - `DVD`

   必要に応じて、 [属性](attribute-product-create.md) をクリックして、さらに値を追加します。

   製品を説明する追加の属性が存在する場合があります。 選択は属性セットによって異なり、後で完了できます。

#### ソースと数量を割り当てる ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### 手順 5：ダウンロード可能な情報を完了する

下にスクロールし、展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Downloadable Information]_」セクションで、**[!UICONTROL Is this downloadable product?]**チェックボックス。

有効にすると、 _[!UICONTROL Downloadable Information]_セクションには 2 つのパーツがあります。 第 1 部では各ダウンロードリンクについて、第 2 部では各サンプルファイルについて説明します。 これらのオプションの多くのデフォルト値は、 [設定](#configure-the-download-options).

![ダウンロード可能な情報](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### リンクを完了

1. Adobe Analytics の _[!UICONTROL Links]_セクションに、**[!UICONTROL Title]**をダウンロードリンクの見出しとして使用する

1. 該当する場合は、 **[!UICONTROL Links can be purchased separately]** チェックボックス。

1. クリック **[!UICONTROL Add Link]** 次の操作を実行します。

   - 次を入力します。 **[!UICONTROL Title]** および **[!UICONTROL Price]** をダウンロードします。

   - 両方に対して **[!UICONTROL File]** および **[!UICONTROL Sample]** ファイルをダウンロードするには、次の配布方法のいずれかを選択します。

      - `Upload File`  — この方法を選択して、配布ファイルをサーバーにアップロードします。 ファイルを参照し、アップロードするファイルを選択します。
      - `URL` - URL から配布ファイルにアクセスするには、この方法を選択します。 ダウンロードファイルの完全な URL を入力します。

   >[!NOTE]
   >
   >外部リソースへのリンクをダウンロード可能な製品として使用することはできません。 有効なリンクドメインは、 `env.php` ファイル ( [env.php リファレンス](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) （内） _設定ガイド_) をクリックします。

   - 設定 **[!UICONTROL Shareable]** を次のいずれかに変更します。

      - `No` ：ダウンロードリンクにアクセスするには、ユーザーがアカウントにログインする必要があります。

      - `Yes`  — 顧客が他のユーザーと共有できるリンクを電子メールで送信します。

      - `Use Config` - [ダウンロード可能な製品オプション](../configuration-reference/catalog/catalog.md) 設定。

   - 次のいずれかの操作を行います。

      - 顧客ごとのダウンロードを制限するには、 **[!UICONTROL Max. Downloads]**.
      - 無制限のダウンロードを許可するには、 **[!UICONTROL Unlimited]** チェックボックス。

   ![リンクの詳細](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. 別のリンクを追加するには、 **[!UICONTROL Add Link]** をクリックし、次の手順を繰り返します。

#### サンプルを完成させます。

1. Adobe Analytics の _[!UICONTROL Samples]_セクションに、**[!UICONTROL Title]**サンプルの見出しとして使用する

1. 各サンプルの情報を入力するには、 **[!UICONTROL Add Link]**.

   ![サンプル](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. リンクの詳細を次のように入力します。

   - 次を入力します。 **[!UICONTROL Title]** 個々のサンプルの

   - 次の配布方法のいずれかを選択します。

      - `Upload File`  — この方法を選択して、配布ファイルをサーバーにアップロードします。 ファイルを参照し、アップロードするファイルを選択します。
      - `URL` - URL から配布ファイルにアクセスするには、この方法を選択します。 ダウンロードファイルの完全な URL を入力します。

   - 別のサンプルを追加するには、 **[!UICONTROL Add Link]** をクリックし、次の手順を繰り返します。

   - サンプルの順序を変更するには、 _変更管理_ ( ![位置コントローラ](../assets/icon-sort-order.png) ) アイコンをクリックし、サンプルを新しい位置にドラッグします。

### 手順 6：製品情報の入力

下にスクロールし、必要に応じて次のセクションの情報を入力します。

- [コンテンツ](product-content.md)
- [画像とビデオ](product-images-and-video.md)
- [検索エンジンの最適化](product-search-engine-optimization.md)
- [関連製品、アップセルおよびクロスセル](related-products-up-sells-cross-sells.md)
- [カスタマイズ可能なオプション](settings-advanced-custom-options.md)
- [Web サイト内の製品](settings-basic-websites.md)
- [デザイン](settings-advanced-design.md)
- [ギフトオプション](product-gift-options.md)

### 手順 7：製品の公開

カタログに商品を公開する準備が整ったら、 **[!UICONTROL Enable Product]** から `Yes` 次のいずれかの操作を行います。

**メソッド 1:** 保存してプレビュー

- 右上隅で、 **[!UICONTROL Save]**.

- ストアで製品を表示するには、 **[!UICONTROL Customer View]** の _管理者_ ( ![メニュー矢印](../assets/icon-menu-down-arrow-black.png) ) メニューを使用します。

  ストアが新しいブラウザータブで開きます。

  ![顧客ビュー](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**方法 2:** 保存して閉じる

次の日： _[!UICONTROL Save]_( ![メニュー矢印](../assets/icon-menu-down-arrow-red.png){width="25"} ) メニューで、「 」を選択します。**[!UICONTROL Save & Close]**.

## ストアフロントエクスペリエンス

顧客アカウントダッシュボードで、 _[!UICONTROL My Downloadable Products]_ダウンロード可能な製品の各注文へのページリンク。 注文が完了すると、顧客のアカウントからダウンロードを利用できるようになります。

![ダウンロード可能な製品](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

次の表に、 _ダウンロード可能な製品_ 値：

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Order#] | The [注文](../stores-purchase/orders.md) ダウンロード可能な製品を購入した場所。 注文の詳細へのリンクを提供します。 |
| [!UICONTROL Date] | オーダーの作成日。 |
| [!UICONTROL Title] | 注文と共に購入したダウンロード可能な製品の名前。 ダウンロード可能な製品へのリンクを提供します。 |
| [!UICONTROL Status] | 注文処理ステータス。 |
| [!UICONTROL Remaining Downloads] | ダウンロードした製品の使用可能なダウンロード数。 |

_**アカウントダッシュボードから製品ファイルをダウンロードするには**_

1. アカウントダッシュボードで、顧客が選択する **[!UICONTROL My Downloadable Products]**.

1. リスト内の順序を検索し、タイトルの後のリンクをクリックします。

1. ダウンロードウィンドウの右下隅で、 _ダウンロード_ アイコン。

1. ファイルをダウンロード場所に配置し、目的の場所に保存します。
