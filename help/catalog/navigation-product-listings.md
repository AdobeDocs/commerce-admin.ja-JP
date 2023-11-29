---
title: 製品リスト
description: 製品リストの設定を変更する方法、1 ページに表示される製品の数、およびリストの並べ替えに使用する属性を決定する方法について説明します。
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# 製品リスト

製品リストは、デフォルトでリストまたはグリッドとして表示されるように設定できます。 また、1 ページに表示される製品の数や、リストの並べ替えに使用する属性を指定することもできます。 製品リストには、製品の並べ替え、リストの形式の変更、属性での並べ替え、ページ間の移動に使用できる一連のコントロールが含まれています。

>[!NOTE]
>
>カテゴリを製品属性で並べ替えると、同じ属性値を持つ製品も、製品属性で並べ替えられます _[!UICONTROL Product ID]_昇順に並べ替えられます。

![グリッドとして表示される製品](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## 製品リストの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Storefront]** 」セクションに入力します。

   ![ストアフロント設定オプション](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   これらのオプションの詳細なリストについては、 [ストアフロント](../configuration-reference/catalog/catalog.md#storefront) （内） _設定リファレンス_.

   >[!NOTE]
   >
   >商品とその価格を、 _価格別の商品並べ替え_&#x200B;で、価格設定が [消費税構成](../configuration-reference/sales/tax.md) 同じ値 (`Excluding Tax` **または** `Including Tax`) をクリックします。 の _[!UICONTROL Calculation Settings]_、**[!UICONTROL Catalog Prices]**の値です。 および_[!UICONTROL Price Display Settings]_、 **[!UICONTROL Display Product Prices in Catalog]** の値です。 値が異なる場合は、階層化されたナビゲーションの価格フィルターで、製品を正しくフィルタリングして価格で並べ替えることができない場合があります。

1. デフォルトを設定 **[!UICONTROL List Mode]** を次のいずれかに変更します。

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. の場合 **[!UICONTROL Products per Page on Grid Allowed Values]**」には、グリッド形式で表示する場合に、1 ページに表示する製品の数を入力します。

   値の選択を入力するには、各数値をコンマで区切ります。

1. の場合 **[!UICONTROL Products per Page on Grid Default Value]**」では、1 ページのグリッドに表示する製品のデフォルト数を入力します。

1. の場合 **[!UICONTROL Products per Page on List Allowed Values]**」では、リスト形式で表示する際に、1 ページに表示する製品の数を入力します。

   値の選択を入力するには、各数値をコンマで区切ります。

1. の場合 **[!UICONTROL Products per page on List Default Value]**」では、リストに表示される製品のデフォルトの数（ページごと）を入力します。

1. 設定 **[!UICONTROL Product Listing Sorted by]** をデフォルトの属性に追加します。この属性は、最初にリストの並べ替えに使用されます。

1. すべての製品をリストするオプションを顧客に与えるには、 **[!UICONTROL Allow All Products on Page]** から `Yes`.

1. 顧客がカタログリストを閲覧して、すべてのページネーション設定を保持する場合は、 **[!UICONTROL Remember Category Pagination]** から `Yes`.

   この設定を有効にすると、買い物客が 1 つのカテゴリから別のカテゴリに移動しても、リストまたはグリッドに表示される製品の数が確実に保持されます。 デフォルトでは、このフィールドはに設定されています。 `No` これは、より多くのキャッシュストレージを使用し、検索エンジンによるページのインデックス作成方法に影響を与える可能性があるためです。

1. を使用している場合、 [フラットカタログ](catalog-flat.md) (**推奨されません**)、次の操作を実行します。

   - 製品のフラットカテゴリリストを表示するには、 **[!UICONTROL Use Flat Catalog Category]** から `Yes`.

   - フラットな製品リストを表示するには、 **[!UICONTROL Use Flat Catalog Product]** から `Yes`.

1. カテゴリ URL と製品 URL のメディアアセットの動的参照を許可する場合は、 **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## ページコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL View As] | 製品をグリッド形式またはリスト形式で表示します。 |
| [!UICONTROL Sort By] | リストの並べ替え順を変更します。 |
| [!UICONTROL Show Per Page] | 1 ページに表示される製品の数を指定します。 |
| ページネーションリンク | ナビゲーションリンクを他のページに移動します。 |

{style="table-layout:auto"}

## ページネーションコントロール

リストの上部と下部に「ページネーション」設定が表示され、製品リストのページネーションリンクの形式を制御します。 コントロールに表示するリンクの数を設定し、「次へ」リンクと「前へ」リンクを設定できます。 ページネーションリンクを表示するには、製品リスト設定の 1 ページに許可されている数より多い製品がリストに存在する必要があります。

![ページネーションコントロール](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### ストアフロントのページネーションコントロール

| 制御 | 説明 |
|--- |--- |
| ![グリッドを表示](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As]  — リストをグリッド形式またはリスト形式で表示します。 |
| ![並べ替え基準](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By]  — リストの並べ替え順を変更します。 The _[!UICONTROL Used for Sorting in Product Listing]_storefront プロパティによって、 [製品属性](../catalog/product-attributes.md) を使用してリストを並べ替えることができます。 |
| ![1 ページにつき表示](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - 1 ページに表示される製品の数を決定します。 |
| ![ページネーションリンク](./assets/control-pagination.png) | ページネーションリンク — 他のページへのナビゲーションリンク。 |

{style="table-layout:auto"}

### ページネーションコントロールの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストアビューを、およびで見つけます。 **[!UICONTROL Action]** 列、クリック **[!UICONTROL Edit]**.

1. の下 **[!UICONTROL Other Settings]**、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Pagination]** 」セクションに入力します。

   ![ページ編集](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   これらの設定について詳しくは、 [デザイン設定](../content-design/configuration.md).

1. の場合 **[!UICONTROL Pagination Frame]**」には、ページネーションコントロールに表示するリンクの数を入力します。

1. の場合 **[!UICONTROL Pagination Frame Skip]**」をクリックして、先にスキップするリンクの数を入力します。この数を超えると、ページネーションコントロールに次の一連のリンクが表示されます。

   例えば、ページネーションフレームに 5 つのリンクがあり、次の 5 つのリンクにジャンプする場合、先にスキップするリンクの数を指定します。 値を 4 に設定した場合 (`4`) の場合、前のセットの最後のリンクが、次のセットの最初のリンクになります。

1. の場合 **[!UICONTROL Anchor Text for Previous]**「前へ」リンクに表示するテキストを入力します。

   デフォルトの矢印を使用する場合は空白のままにします。

1. の場合 **[!UICONTROL Anchor Text for Next]**&#x200B;に、「次へ」リンクに表示するテキストを入力します。 デフォルトの矢印を使用する場合は空白のままにします。

1. 完了したら、「 **[!UICONTROL Save Configuration]**.
