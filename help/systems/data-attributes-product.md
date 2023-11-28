---
title: 製品データ属性リファレンス
description: 製品データのインポートおよびエクスポートを操作する場合は、製品データ属性のこの参照を使用します。
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2469'
ht-degree: 0%

---

# 製品データ属性リファレンス

次の表に、標準的な製品エクスポートの属性を、デフォルトの表示順に示します。 各属性は CSV ファイル内で列として表され、製品レコードは行で表されます。 アンダースコアで始まる列には、複雑なデータのプロパティやオプション値などのサービスデータが含まれます。 以下が可能です。 [書き出し](data-export.md) カタログの製品を使用して、各属性がデータでどのように表されているかを確認します。

このデータの書き出しに使用するインストールには、サンプルデータがインストールされており、2 つの Web サイトと複数のストア表示があります。 このリストには、通常、書き出されるすべての列が含まれますが、 `sku` が唯一の必須の値です。 データをインポートするには、変更を含む列のみを含めることができます。 The `sku` は最初の列ですが、残りの属性の順序は関係ありません。

## シンプルな製品 CSV ファイル構造

| 属性 | 説明 |
|--- |--- |
| `sku` | （必須）在庫管理単位は、在庫の追跡に使用される一意の英数字の識別子です。 SKU の長さは最大 64 文字です。 例： `sku123`<br/>**_注意：_**64 文字を超える SKU を使用すると、インポートが失敗します。 |
| `store_view_code` | 製品が使用可能な特定のストア表示を識別します。 空白の場合、製品はデフォルトのストア表示で使用できます。 例： `storeview1`, `english`, `spanish` |
| `attribute_set_code` | プロダクトタイプに従って、プロダクトを特定の属性セットまたはプロダクトテンプレートに割り当てます。 製品を作成した後は、属性セットを変更できません。 例： `default` |
| `product_type` | 製品のタイプを示します。 値：<br/>`simple`  — 通常、単一単位または一定数量で販売される有形品。<br/>`grouped`  — セットとして販売される、別々の製品のグループ。<br/>`configurable`  — 顧客が購入する前に選択する必要がある複数のオプションを持つ製品。 在庫は個別の SKU を持つ個別の製品を表しているので、バリエーションのセットごとに管理できます。 例えば、設定可能な製品の色とサイズの組み合わせが、カタログ内の特定の SKU に関連付けられているとします。<br/>`virtual`  — 出荷を必要とせず、在庫に保管されない非有形製品。 例としては、サービス、メンバーシップ、購読などがあります。<br/>`bundle`  — 一緒に販売されるシンプルな製品のカスタマイズ可能な製品セット。 |
| `categories` | 製品に割り当てられている各カテゴリを示します。 カテゴリとサブカテゴリはフォワードスラッシュで区切ります。 複数のカテゴリパスを指定するには、各パスをパイプで区切ります |記号。 例： `Default Category/Gear&#124;Default Category/Gear/Bags` |
| `product_websites` | 製品が入手可能な各 Web サイトの Web サイトコード。 1 つの製品を複数の Web サイトに割り当てることも、1 つに制限することもできます。 複数の Web サイトを指定する場合は、それぞれをコンマで区切り、スペースは入れません。 例： `base` または `base,website2` |
| `name` | 製品名は、すべての製品リストに表示され、顧客が製品を識別するために使用する名前です。 |
| `description` | 製品の説明には、製品に関する詳細情報が表示されます。簡単なHTMLタグを含めることもできます。 |
| `short_description` | 短い製品説明の使用方法は、テーマによって異なります。 製品リストに表示され、ショッピングサイトに送信される RSS フィードリストに使用される場合があります。 |
| `weight` | 個々の製品の重み。 実際の製品の重量は、出荷時に運送業者によって決定されます。 |
| product_online | 商品がストアで販売できるかどうかを指定します。 値：<br/>`1` — （はい）製品は有効で、販売可能です。<br/>`2` — (No) 製品は無効で、販売できません。 |
| `tax_class_name` | この製品に関連付けられている税区分の名前。 |
| `visibility` | 商品がカタログに表示され、検索に使用できるかどうかを指定します。 値：<br/>`Not Visible Individually`  — 製品は製品リストに含まれていませんが、別の製品のバリエーションとして使用できる場合があります。<br/>`Catalog`  — すべてのカタログリストに製品が表示されます。<br/>`Search`  — プロダクトは検索操作に使用できます。<br/>`Catalog, Search`  — 商品はカタログリストに含まれ、検索にも使用できます。 |
| `price` | ストアでの商品の販売価格。 |
| `special_price` | 指定した日付範囲での製品の割引価格。 |
| `special_price_from_date` | 特別価格が有効な期間の開始日。 |
| `special_price_to_date` | 特別価格が有効になる期間の最終日。 |
| `url_key` | 製品を識別する URL の一部。 デフォルト値は製品名に基づきます。 例： `product-name` |
| save_rewrites_history | 値と共に指定する場合 `1` 新しい `url_key`に値を指定しない場合、古い URL が新しい URL にリダイレクトされるように、新しい 301 URL の書き換えが生成されます。 |
| `meta_title` | メタタイトルは、ブラウザーおよび検索結果のリストのタイトルバーおよびタブに表示されます。 メタタイトルは、製品ごとに一意で、価値の高いキーワードを組み込み、長さが 70 文字未満である必要があります。 |
| `meta_keywords` | メタキーワードは検索エンジンに対してのみ表示され、一部の検索エンジンでは無視されます。 値の大きいキーワードをコンマで区切って選択します。 例： `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | メタ説明は、検索結果リストに表示される製品の概要を示します。 メタ記述の長さは 150 ～ 160 文字にするのが理想的ですが、フィールドには最大 255 文字まで入力できます。 |
| `base_image` | 製品ページ上のメイン画像の相対パス。 Commerce では、内部的にはアルファベット順のフォルダ構造でファイルが格納されます。 書き出されたデータ内の各画像の正確な場所を確認できます。 例： `/sample_data/m/b/mb01-blue-0.jpg`<br/>新しい画像をアップロードしたり、既存の画像を書き込んだりするには、ファイル名の前にスラッシュを付けて入力します。 例： `/image.jpg` |
| `base_image_label` | ベース画像に関連付けられているラベル。 |
| `small_image` | カタログページで使用される小さい画像のファイル名。先頭にスラッシュが付きます。 例： `/image.jpg` |
| `small_image_label` | 小さい画像に関連付けられたラベル。 例： `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | 製品ページ上のギャラリーに表示するサムネール画像のファイル名。先頭にスラッシュが付きます。 例： `/image.jpg` |
| `thumbnail_image_label` | 任意のサムネール画像に関連付けられているラベル。 例： `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | 製品が作成された日付を示します。 製品の作成時に日付が自動的に生成されますが、後で編集できます。 |
| `updated_at` | 製品が最後に更新された日付を示します。 |
| `new_from_date` | 新しい製品リストの「開始日」を指定し、製品が新しい製品として取り上げられるかどうかを指定します。 |
| `new_to_date` | 新しい製品リストの「終了日」を指定し、製品が新しい製品として取り上げられるかどうかを指定します。 |
| `display_product_options_in` | 製品に複数のオプションがある場合は、が製品ページで表示する場所を決定します。 値：情報列の後の製品情報列/ブロック |
| `map_price` | 商品の最低広告価格。 （MAP が有効な場合にのみ表示されます）。 |
| `msrp_price` | 製造元が商品の推奨小売価格。 （MAP が有効な場合にのみ表示されます）。 |
| `map_enabled` | 設定で [ 最小アドバタイズ価格 ] が有効になっているかどうかを確認します。 値：<br/>`1` — （はい） MAP が有効になっています。<br/>`0` （または空白）: （いいえ） MAP は有効になっていません。 |
| `gift_message_available` | 商品の購入にギフトメッセージを含めることができるかどうかを指定します。 値：<br/>`1` — （はい）ギフトメッセージを含めるオプションがお客様に表示されます。<br/>`0` （または空白）:（いいえ）ギフトメッセージを含めるオプションは、お客様には表示されません。 |
| `custom_design` | 製品ページに適用できるテーマの一覧が表示されます。 |
| `custom_design_from` | 選択したテーマが製品ページに適用される開始日を指定します。 |
| `custom_design_to` | 選択したテーマが製品ページに適用される終了日を指定します。 |
| `custom_layout_update` | レイアウトとして製品ページに適用される追加の XML コード。 |
| `page_layout` | 商品ページのページレイアウトを決定します。 値：<br/>`No layout updates`  — ページレイアウトは変更されません。<br/>`1 column`  — 製品ページに 1 列のレイアウトを適用します。<br/>`2 columns with left bar`  — 製品ページに左にサイドバーのある 2 列のレイアウトを適用します。<br/>`2 columns with right bar`  — 製品ページに右側のサイドバーを持つ 2 列のレイアウトを適用します。<br/>`3 columns`  — 製品ページに 3 列のレイアウトを適用します。<br/>`empty`  — 製品ページに空白のレイアウトを適用します。 |
| `product_options_container` | 製品に複数のオプションがある場合は、が製品ページで表示する場所を決定します。 値：情報列の後の製品情報列/ブロック |
| `msrp_display_actual_price_type` | 製品の実際の価格を顧客に表示する場所を決定します。 値：<br/>`In Cart`  — 買い物かごの実際の製品価格を表示します。<br/>`Before Order Confirmation`  — チェックアウトプロセスの最後、注文が確認される直前の実際の製品価格を表示します。<br/>`On Gesture`  — 顧客が _クリックして価格_ または _これは何だ？_ リンク。 |
| `country_of_manufacture` | 製品が製造された国を示します。 |
| `additional_attributes` | 製品に対して作成された追加の属性。 例： <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | 現在在庫にある製品の数量。 |
| `out_of_stock_qty` | 在庫切れにする製品を決定する在庫レベルです。 |
| `use_config_min_qty` | 設定のデフォルト値を使用するかどうかを決定し、「 Use Config Settings 」チェックボックスに対応します。 値：<br/>`1` — （はい）この属性の値にはデフォルトの設定が使用されます。<br/>`0` （または空白） — （いいえ）この属性の値に対してデフォルトの設定を上書きできます。 |
| `is_qty_decimal` | qty 属性に 10 進数値が含まれているかどうかを指定します。 値：<br/>`1` — （はい）qty 属性の値は 10 進値です。<br/>`0` （または空白） — （いいえ）qty 属性の値は整数です。 |
| `allow_backorders` | ストアでバックオーダーを許可するかどうか、およびバックオーダーの管理方法を決定します。 |
| `use_config_backorders` | バックオーダーのデフォルトの設定を使用するかどうかを決定し、「構成設定を使用」チェックボックスの状態に対応します。 値：<br/>`1` — （はい）qty 属性の値は 10 進値です。<br/>`0` （または空白） — （いいえ）qty 属性の値は整数です。 |
| `min_cart_qty` | 1 回の注文で購入できる品目の最小数量を指定します。 |
| `use_config_min_sale_qty` | 最小数量のデフォルトの設定を使用するかどうかを指定し、[ 構成設定を使用 ] チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `max_cart_qty` | 1 回の注文で購入できる製品の最大数量を指定します。 |
| `use_config_max_sale_qty` | 最大数量のデフォルトの設定を使用するかどうかを指定し、「設定を使用」(Use Config Settings) チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `is_in_stock` | 製品が在庫にあるかどうかを示します。 |
| `notify_on_stock_below` | 在庫レベルを指定します。トリガーは、 _在庫切れ_ 通知。 |
| `use_config_notify_stock_qty` | デフォルトの設定を使用して在庫レベルの通知をトリガーするかどうかを指定し、「構成設定を使用」チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `manage_stock` | 在庫管理を製品の管理に使用するかどうかを決定します。 値：<br/>`1` — （はい）製品の在庫レベルを管理するために、在庫管理を完全に有効化します。<br/>`0` （または空白） — （いいえ）現在在庫にある品目の数は追跡されません。 |
| `use_config_manage_stock` | 在庫管理のデフォルトの設定を使用するかどうかを指定し、「構成設定を使用」チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `use_config_qty_increments` | 数量の増分に対するデフォルトの設定を使用するかどうかを指定し、[ 構成設定を使用 ] チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `qty_increments` | 数量の増分を構成する製品の数を指定します。 |
| `use_config_enable_qty_inc` | 数量増分を有効にするデフォルトの設定を使用するかどうかを指定し、「設定を使用」チェックボックスの状態に対応します。 値：<br/>`1` — （はい）<br/>`0` （または空白） — （いいえ） |
| `enable_qty_increments` | 製品の数量増分が有効かどうかを指定します。 |
| `is_decimal_divided` | 製品の部品を別々に出荷できるかどうかを指定します。 オプション： `Yes` / `No` |
| `website_id` | 複数の Web サイトを使用したインストールの場合、は製品が使用可能な特定の Web サイトを識別します。 空白の場合、製品はすべての Web サイトで使用できます。 |
| `related_skus` | 関連製品として識別された各製品の SKU を一覧表示します。 例： `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | related_sku 列に Related Products と表示される SKU の位置（並べ替え順）を決定します。 例： `1,2,3,4` |
| `crosssell_skus` | クロス販売として識別された各製品の SKU を一覧表示します。 |
| `crosssell_position` | SKU の位置（並べ替え順）を決定し、 `crosssell_skus` 列。 |
| `upsell_skus` | アップセルとして識別された各製品の SKU を一覧表示します。 |
| `upsell_position` | SKU の位置（並べ替え順）を決定します。SKU が `upsell_skus` 列。 |
| `additional_images` | 製品に関連付ける追加の画像のファイル名。先頭にスラッシュが付きます。 例： `/image.jpg` |
| `additional_image_labels` | 追加の画像に関連付けられたラベル。 例： `Label 1`, `Label 2` |
| `custom_options` | 各カスタムオプションに割り当てるプロパティと値を指定します。 例： <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## 製品バリエーションのサービスデータ

| 属性 | 説明 | 適用先 |
|--- |--- | --- |
| `_super_products_sku` | 設定可能な製品バリエーションに対して生成された SKU。 例： WB03-XS-Green | 設定可能な製品 |
| `_super_attribute_code` | 設定可能な製品バリエーションの属性コード。 例： color | 設定可能な製品 |
| `_super_attribute_option` | 設定可能な製品バリエーションの値。 例：green | 設定可能な製品 |
| `_super_attribute_price_corr` | 設定可能な製品バリエーションに関連付けられた価格調整。 | 設定可能な製品 |
| `_associated_sku` | グループ化された製品に関連付けられている製品の SKU。 | グループ化された製品 <br/>製品をバンドル |
| `_associated_default_qty` | 含まれる関連製品の数量を決定します。 | 設定可能な製品<br/>グループ化された製品<br/>製品をバンドル |
| `_associated_position` | 他の関連製品と共に表示される場合の、関連製品の位置を決定します。 | 設定可能な製品<br/>グループ化された製品<br/>製品をバンドル |

{style="table-layout:auto"}

## 複雑な製品データ属性

複雑なデータという用語は、複数の製品オプションに関連付けられたデータを指します。 次の製品タイプでは、別々の製品から生成されるデータを使用して、製品のバリエーションと複数のオプションを作成します。

- [設定可能](../catalog/product-create-configurable.md)
- [グループ化](../catalog/product-create-grouped.md)
- [バンドル](../catalog/product-create-bundle.md)

設定可能な製品を書き出すと、単純な製品を構成する標準属性に加えて、複雑なデータを管理するために必要な追加の属性が見つかります。

![構成可能な製品 — 書き出したデータ](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### 設定可能な製品

| 属性 | 説明 |
|--- |--- |
| `configurable_variation_labels` | 製品のバリエーションを識別するラベル。 例： `Choose Color:` または `Choose Size:` |
| `configurable_variations` | 製品のバリエーションに関連付けられた値を記述します。 例： `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### グループ化された製品

| 属性 | 説明 |
|--- |--- |
| `associated_skus` | グループを構成する個々の製品の SKU を識別します。 |

{style="table-layout:auto"}

### 製品のバンドル

| 属性 | 説明 |
|--- |--- |
| `bundle_price_type` | バンドル項目の価格が固定か動的かを指定します。 |
| `bundle_sku_type` | 各項目に変数、動的 SKU が割り当てられているか、またはバンドルに固定 SKU が使用されているかを決定します。 オプション：固定/動的 |
| `bundle_weight_type` | バンドル項目の重み付けが可変か固定かを決定します。 |
| `bundle_values` | バンドルオプションに関連付けられた teach 値を表します。 例： `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## 高度な価格属性

高度な価格のインポート/エクスポートを使用すると、製品グループと階層価格の価格情報を迅速に更新できます。 次の処理を実行します。 [インポート](data-import.md) および [書き出し](data-export.md) 高度な価格データは、他のエンティティタイプと同じです。 サンプルの CSV ファイルには、高度な価格設定をサポートする各製品タイプの階層とグループ価格が含まれています。 高度な価格設定を変更しても、製品レコードの残りの部分には影響しません。

![エクスポートデータの例 — 高度な価格設定](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| 属性 | 説明 |
|--- |--- |
| `sku` | （必須）在庫管理単位は、在庫の追跡に使用される一意の英数字の識別子です。 SKU の長さは最大 64 文字です。 例： `sku123`<br/>**_注意：_**64 文字を超える SKU を使用すると、インポートが失敗します。 |
| `tier_price_website` | The [web サイトコード](../stores-purchase/stores.md#add-websites) は、階層価格を利用できる各 web サイトを示しています。 例： `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | を識別します。 [顧客グループ](../customers/customer-groups.md) ここでは、階層価格を利用できます。 例： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | 階層価格が利用可能な顧客グループを特定します。 例： `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | 階層価格割引を受けるために注文する必要がある製品の数量。 |
| `tier_price` | 製品の割引価格。 の場合 [バンドル製品](../catalog/product-create-bundle.md)の場合、階層価格はパーセンテージで計算されます。 |
| `group_price_website` | The [web サイトコード](../stores-purchase/stores.md#add-websites) を参照してください。 複数の Web サイトを指定する場合は、それぞれをコンマで区切り、スペースは入れません。 例： `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | グループ価格が使用可能な顧客のグループを特定します。 例： `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | 製品の割引されたグループ価格。 の場合 [バンドル製品](../catalog/product-create-bundle.md)の場合、グループ価格は割合で計算されます。 |

{style="table-layout:auto"}
