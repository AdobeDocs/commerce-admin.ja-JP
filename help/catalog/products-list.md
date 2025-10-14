---
title: 商品リスト
description: 製品を作成し、既存の製品を編集できる、管理者の_[!UICONTROL Products]_ ページについて説明します。
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# 商品リスト

カタログ内のすべての製品には、管理者の _[!UICONTROL Products]_&#x200B;ページからアクセスできます。このページで、製品を作成したり、既存の製品を編集したりできます。 マルチサイトインストールの場合、同じカタログから販売される異なる製品を各 web サイトで選択できます。

_[!UICONTROL Products]_&#x200B;リストには、カタログ内のすべての製品が含まれ、製品が使用可能な web サイトと、現在販売が有効な web サイトが示されます。 [&#x200B; 共有カタログ &#x200B;](../b2b/catalog-shared.md) が有効になっているAdobe Commerce B2B インストールの場合、グリッドには、共有カタログで代替割引価格が設定されている商品を示す列が含まれます。

ページごとにリストページを参照するか、特定の製品を検索できます。 標準の [&#x200B; コントロール &#x200B;](../getting-started/admin-grid-controls.md) を使用してリストの並べ替えとフィルタリングを行い、選択した製品に [&#x200B; アクション &#x200B;](../getting-started/admin-actions-control.md) を適用します。

![&#x200B; 製品グリッド &#x200B;](./assets/products-grid.png){width="700" zoomable="yes"}

## 製品表示を制限

大きなカタログのパフォーマンスを向上させるには、グリッドに表示する製品数を制限することをお勧めします。 表示される商品グリッドは、次の項目に限定できます。

- 製品ページ
- 関連/アップセル/クロスセル製品の追加
- バンドル製品への製品の追加
- 製品をグループ製品に追加
- 注文を作成（管理者）

この製品の表示制限の設定は、デフォルトで無効になっています。 有効にすると、グリッド内の製品数を特定の値に制限できます。 有効になっていて、グリッド表示に一致する製品の数がレコード制限を超えている場合、限られたレコードのコレクションが返されます。 制限に達すると、検出された合計レコード数、選択したレコード数、ページネーション要素がグリッドヘッダーに表示されません。

>[!NOTE]
>
>製品グリッドを制限しない場合は、より正確にフィルターを使用し、「_[!UICONTROL Records Limit]_」フィールドで指定された数よりも項目数が少ないコレクションを作成します。

**_製品の表示制限を設定するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL Admin]**」を選択します。

1. **[!UICONTROL Admin Grids]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - **[!UICONTROL Limit Number of Products in Grid]** を `Yes` に設定します。

   - （オプション）「**[!UICONTROL Records Limit]**」フィールドに値を入力して、グリッド内の製品数を特定の値に制限します。 デフォルトの最小値は `20000` です。

   ![&#x200B; 管理グリッドの設定 &#x200B;](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## ページコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Add Product] | 新しいシンプルな製品を作成するプロセスを開始します。 特定の製品タイプを選択するには、下向き矢印をクリックします。 オプション：[[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | リストで選択した製品に適用できるすべてのアクションをリストします。 製品または製品グループにアクションを適用するには、各製品の最初の列にあるチェックボックスを選択します。 オプション：`Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | 現在のフィルターに基づいてカタログ検索を開始します。 |
| [!UICONTROL Default View] | 現在のグリッド列のレイアウトを示します。 保存されているグリッド列ビューがある場合は、別のものを選択できます。 |
| [!UICONTROL Columns] | リストで選択した製品に適用できるすべてのアクションをリストします。 製品または製品グループにアクションを適用するには、各製品の最初の列にあるチェックボックスを選択します。 |
| [!UICONTROL Search by keyword] | 左上隅の検索ボックスを使用して、キーワードで製品を検索します。 |
| [!UICONTROL Edit] | 製品を編集モードで開きます。 行の任意の場所をクリックして、同じことを達成できます。 |

{style="table-layout:auto"}

## デフォルトの列

| 列 | 説明 |
|--- |--- |
| （チェックボックス） | アクションの対象となる複数のレコードを選択します。 選択した各レコードの最初の列のチェックボックスがマークされます。 オプション：<br/>**[!UICONTROL Select All]**– 現在のフィルター設定に一致するレコードがすべて選択されます。<br/>**[!UICONTROL Select All on This Page]** – 現在のページで見つかった、フィルター設定に一致するレコードのみを選択します。 |
| [!UICONTROL ID] | 新しい商品が初めて保存されるときに割り当てられる一意の連続番号。 |
| [!UICONTROL Thumbnail] | メインの製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | 商品名。 |
| [!UICONTROL Type] | 商品タイプ。 |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。 |
| [!UICONTROL SKU] | 商品に割り当てられる一意の最小在庫管理単位。 |
| [!UICONTROL Price] | 商品の単価。 |
| [!UICONTROL Quantity] | 在庫がある数量。 |
| [!UICONTROL Salable Quantity] | この商品の使用可能なすべての単位の合計。 |
| [!UICONTROL Visibility] | カタログ内で商品が表示される場所を示します。 オプション：`Not Visible Individually`/`Catalog`/`Search`/`Catalog, Search` |
| [!UICONTROL Status] | 商品のステータスを示します。 オプション：`Enabled` および `Disabled` |
| [!UICONTROL Websites] | 製品が使用可能な web サイトを示します。 |
| [!UICONTROL Action] | 製品を編集モードで開きます。 |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) （[Adobe Commerce B2B](./b2b/../introduction.md) でのみ使用可能）商品のカスタム価格を含む共有カタログを示します。 |

{style="table-layout:auto"}

## その他の列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Short Description] | 商品の簡単な説明。 |
| [!UICONTROL Special Price From Date] | 特別価格昇格の最初の日付。 |
| [!UICONTROL Special Price To Date] | 特別価格昇格の最終日。 |
| [!UICONTROL Cost] | 品目の実際のコスト。 |
| [!UICONTROL Manufacturer] | 商品の製造元。 |
| [!UICONTROL Meta Keywords] | 商品のメタキーワード。 |
| [!UICONTROL Color] | 商品の色。 |
| [!UICONTROL Set Product as New from Date] | 新しいプロモーションとして設定された製品の最初の日付。 |
| [!UICONTROL Set Product as New to Date] | 新しいプロモーションとして設定された商品の最終日付。 |
| [!UICONTROL Active From / To] | 製品の開始日と終了日。 |
| [!UICONTROL Layout] | 製品のレイアウト。 |
| [!UICONTROL Minimum Advertised Price] | 商品の広告された最低価格。 |
| [!UICONTROL Allow Gift Message] | ギフトカードを購入した顧客に対するギフトメッセージ。 |
| [!UICONTROL Special Price] | 商品の特別価格。 |
| [!UICONTROL Weight] | 製品の重み。 |
| [!UICONTROL Meta Title] | 商品のメタタイトル。 |
| [!UICONTROL Meta Description] | 製品メタデータの説明。 |
| [!UICONTROL Country of Manufacture] | 製造国。 |
| [!UICONTROL New Theme] | カスタムテーマが製品に適用されました。 |
| [!UICONTROL URL Key] | 商品の URL キー。 |
| [!UICONTROL Tax Class] | 製品税クラス。 |
| [!UICONTROL Allow Gift Message] | 商品のギフト メッセージ オプションの利用可能性を表示します。 |

{style="table-layout:auto"}
