---
title: 製品リスト
description: 製品を作成し、既存の製品を編集できる管理者の_[!UICONTROL Products]_ ページについて説明します。
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
TQID: https://experienceleague.adobe.com/tCvjmMlTzn0ejytHyuLPIKKpHn7CGiVkrAwJWmvN-Ro
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 836
ht-degree: 0%

---

# 製品リスト

カタログ内のすべての製品は、管理者の&#x200B;_[!UICONTROL Products]_&#x200B;ページからアクセスできます。このページでは、製品を作成したり、既存の製品を編集したりできます。 マルチサイトインストールの場合、各web サイトで同じカタログから異なる製品を販売できます。

_[!UICONTROL Products]_&#x200B;リストには、カタログ内のすべての製品が含まれ、利用可能なweb サイトと、現在販売が有効なweb サイトが示されます。 [共有カタログ &#x200B;](../b2b/catalog-shared.md)が有効になっているAdobe Commerce B2B インストールでは、グリッドには、共有カタログに代替割引価格が設定されている商品を示す列が含まれています。

リストページからページ別に閲覧したり、特定の商品を検索したりできます。 標準の[&#x200B; コントロール &#x200B;](../getting-started/admin-grid-controls.md)を使用してリストを並べ替えおよびフィルタリングし、選択した製品に[&#x200B; アクション &#x200B;](../getting-started/admin-actions-control.md)を適用します。

![製品グリッド &#x200B;](./assets/products-grid.png){width="700" zoomable="yes"}

## 商品表示を制限

大きなカタログのパフォーマンスを向上させるには、グリッドに表示される商品数を制限することをお勧めします。 表示される商品グリッドは、次の場合に制限できます。

- 製品ページ
- 関連/アップセル/クロスセル商品の追加
- 製品をバンドル製品に追加
- 製品をグループ製品に追加
- 注文の作成（管理者）

製品表示制限のこの設定設定は、デフォルトでは無効になっています。 これを有効にすると、グリッド内の商品数を特定の値に制限できます。 これが有効で、グリッド表示の一致する製品数がレコードの上限を超える場合、限られたレコードのコレクションが返されます。 制限に達すると、見つかったレコードの合計、選択したレコードの数、ページネーション要素がグリッドヘッダーに表示されません。

>[!NOTE]
>
>商品グリッドを制限しない場合は、フィルターをより正確に使用して、_[!UICONTROL Records Limit]_&#x200B;フィールドで指定された数よりも少ない項目を持つコレクションを生成します。

**_製品表示の制限を設定するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. **[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL Admin]**&#x200B;を選択します。

1. **[!UICONTROL Admin Grids]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   - **[!UICONTROL Limit Number of Products in Grid]**&#x200B;を`Yes`に設定します。

   - （オプション）グリッド内の製品数を特定の値に制限するには、**[!UICONTROL Records Limit]** フィールドに値を入力します。 デフォルトの最小値は`20000`です。

   ![管理者グリッドの設定設定](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## ページコントロール

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Add Product] | 新しいシンプルな製品を作成するプロセスを開始します。 特定の製品タイプを選択するには、下向き矢印をクリックします。 オプション：[[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | リスト内で選択した製品に適用できるすべてのアクションを一覧表示します。 製品または製品グループにアクションを適用するには、各製品の最初の列にあるチェックボックスを選択します。 オプション：`Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | 現在のフィルターに基づいてカタログ検索を開始します。 |
| [!UICONTROL Default View] | 現在のグリッド列レイアウトを示します。 グリッド列ビューが保存されている場合は、別のビューを選択できます。 |
| [!UICONTROL Columns] | リスト内で選択した製品に適用できるすべてのアクションを一覧表示します。 製品または製品グループにアクションを適用するには、各製品の最初の列にあるチェックボックスを選択します。 |
| [!UICONTROL Search by keyword] | 左上隅の検索ボックスは、キーワードで商品を検索するために使用されます。 |
| [!UICONTROL Edit] | 製品を編集モードで開きます。 行の任意の場所をクリックすると、同じことを達成できます。 |

{style="table-layout:auto"}

## デフォルトの列

| 列 | 説明 |
|--- |--- |
| （チェックボックス） | アクションの対象となる複数のレコードを選択します。 選択した各レコードの最初の列のチェックボックスがマークされます。 オプション：<br/>**[!UICONTROL Select All]**– 現在のフィルター設定に一致するレコードをすべて選択します。<br/>**[!UICONTROL Select All on This Page]** - フィルター設定に一致する、現在のページで見つかったレコードのみを選択します。 |
| [!UICONTROL ID] | 新しい製品が初めて保存されたときに割り当てられる、一意の連続番号。 |
| [!UICONTROL Thumbnail] | メイン製品画像のサムネールを表示します。 |
| [!UICONTROL Name] | 製品名です。 |
| [!UICONTROL Type] | 商品タイプ： |
| [!UICONTROL Attribute Set] | 製品のテンプレートとして使用される属性セットの名前。 |
| [!UICONTROL SKU] | 製品に割り当てられている一意の在庫保管単位。 |
| [!UICONTROL Price] | 製品の単価。 |
| [!UICONTROL Quantity] | 在庫のある数量。 |
| [!UICONTROL Salable Quantity] | この製品の利用可能なすべての単位の合計。 |
| [!UICONTROL Visibility] | 商品がカタログ内のどこに表示されているかを示します。 オプション：`Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | 製品のステータスを示します。 オプション：`Enabled`および`Disabled` |
| [!UICONTROL Websites] | 製品が使用可能なweb サイトを示します。 |
| [!UICONTROL Action] | 製品を編集モードで開きます。 |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) （[Adobe Commerce B2B](./b2b/../introduction.md)でのみ利用可能）商品のカスタム価格を含む共有カタログを示します。 |

{style="table-layout:auto"}

## その他の列

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Short Description] | 製品の簡単な説明。 |
| [!UICONTROL Special Price From Date] | 特別値上げ開始日。 |
| [!UICONTROL Special Price To Date] | 特別値上げプロモーションの最終日。 |
| [!UICONTROL Cost] | 品目の実際のコスト。 |
| [!UICONTROL Manufacturer] | 製品のメーカー。 |
| [!UICONTROL Meta Keywords] | 商品のMetaキーワード。 |
| [!UICONTROL Color] | 商品カラー。 |
| [!UICONTROL Set Product as New from Date] | 新しいプロモーションとして設定された製品の最初の日付。 |
| [!UICONTROL Set Product as New to Date] | 新しいプロモーションとして設定された製品の最終日。 |
| [!UICONTROL Active From / To] | 製品の開始日と終了日。 |
| [!UICONTROL Layout] | 商品レイアウト。 |
| [!UICONTROL Minimum Advertised Price] | 製品の最低広告価格。 |
| [!UICONTROL Allow Gift Message] | ギフトカードを購入されたお客様へのギフトメッセージ。 |
| [!UICONTROL Special Price] | 製品の特別価格。 |
| [!UICONTROL Weight] | 商品の重み。 |
| [!UICONTROL Meta Title] | 商品のMeta タイトル。 |
| [!UICONTROL Meta Description] | 製品メタデータの説明。 |
| [!UICONTROL Country of Manufacture] | 製造の国。 |
| [!UICONTROL New Theme] | 製品にカスタムテーマを適用しました。 |
| [!UICONTROL URL Key] | 製品のURL キー。 |
| [!UICONTROL Tax Class] | 製品税区分。 |
| [!UICONTROL Allow Gift Message] | 製品のギフトメッセージオプションの利用可能性を表示します。 |

{style="table-layout:auto"}

