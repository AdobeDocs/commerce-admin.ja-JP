---
title: 国別の税金ガイドライン
description: 国に応じて、推奨される税金設定をレビューします。
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 0%

---

# 国別の税金ガイドライン

## 米国の税金構成

これらの推奨設定は、米国内の店舗のほとんどの税金設定に使用できます。

| 税オプション | 推奨事項 |
|--- |--- |
| カタログ価格の読み込み | 税抜き |
| FPT | いいえ。FPT には課税されないからです。 |
| 課税基準 | 発送元 |
| 税計算 | 合計 |
| 送税？ | 不可 |
| 割引を適用 | 税引前 |
| コメント | すべての税金ゾーンは同じ優先度です。州のゾーンと郵便番号の参照用の 1 つ以上のゾーンが理想的です。 |

{style="table-layout:auto"}

### 税クラス

| 税クラス | 推奨設定 |
|--- |--- |
| 配送用の税クラス | なし |

{style="table-layout:auto"}

### 計算設定

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 既定の税宛先計算

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | ビジネスがある州。 |
| [!UICONTROL Default Post Code] | 税ゾーンで使用される郵便番号。 |

{style="table-layout:auto"}

### 価格の表示設定

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 買い物かごの表示設定

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 受注、請求書、クレジット・メモおよび表示設定

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 固定製品税（FPT）

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`（カリフォルニア州を除く） |

{style="table-layout:auto"}

## 英国の税構成

これらの推奨設定は、英国内の店舗のほとんどの税金設定に使用できます。

### 英国 B2C 税金構成

| 税オプション | 推奨事項 |
|--- |--- |
| カタログ価格の読み込み | 税抜き |
| FPT | はい（FPT と説明を含む） |
| 課税基準 | [!UICONTROL Shipping Address] |
| 税計算 | 合計 |
| 送税？ | はい |
| 割引を適用 | 税引前、税込み値引き。 |
| コメント | 仕入先請求書（VAT を含む）をマークアップするマーチャントの場合。 |

{style="table-layout:auto"}

### 英国 B2B 税のコンフィギュレーション

| 税オプション | 推奨事項 |
|--- |--- |
| カタログ価格の読み込み | 税抜き |
| FPT | はい（FPT と説明を含む） |
| 課税基準 | [!UICONTROL Shipping Address] |
| 税計算 | アイテム時 |
| 送税？ | はい |
| 割引を適用 | 税引前、税込み値引き。 |
| コメント | B2B マーチャント向けに、VAT のサプライチェーンに関する考慮事項を簡素化します。 行の税金計算も有効ですが、課税管轄区域を確認してください。 設定では、販売者がサプライ チェーンにあり、販売された商品が他の仕入先によって VAT リベートなどに使用されることを前提としています。 この定義により、品目ごとに税金を簡単に識別できるので、リベートの生成が迅速化されます。 <br/><br/>**_注意：_**一部の国や地域では、現在Commerceでサポートされていない異なる丸め方法が必要です。また、すべての国や地域で品目税または行レベルの税が許可されているわけではありません。 |

{style="table-layout:auto"}

## カナダの税構成

>[!IMPORTANT]
>
>GST/PST 州（モントリオール）のマーチャントは、1 つの税務処理基準を作成し、合計の税額を表示する必要があります。 ご質問がある場合は、必ず税務当局にお問い合わせください。 特定の都道府県の税要件について詳しくは、次を参照してください。 [レヴヌ ケベック][1], [サスカチュワン政府][2]、および [ベンダー向けマニトバ情報][3]

| 税オプション | 推奨事項 |
|--- |--- |
| カタログ価格の読み込み | 税抜き |
| FPT | はい（FPT、説明を含む）、FPT への税金の適用。 |
| 課税基準 | 発送元 |
| 税計算 | 合計 |
| 送税？ | はい |
| 割引を適用 | 税引前 |

{style="table-layout:auto"}

次の例では、カナダの GST 税率とサスカチュワンの PST 税率を、2 つの税率を計算して表示する税務処理基準とともに設定する方法を示します。 この情報は、設定例を示しています。税管轄区域に適した税率とルールを必ず確認してください。 税金を設定する場合は、該当するすべての店舗と web サイトに設定を適用するように店舗の範囲を設定します。

- 関連商品に対する固定製品税は製品属性として含まれます。
- ケベックでは、PST は TVQ と呼ばれます。 Quebec のレートを設定する場合は、必ず TVQ を識別子として使用してください。

### 手順 1：税金計算設定の完了

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. マルチサイト設定の場合、次のように設定します **[!UICONTROL Store View]** ：設定のターゲットである web サイトとストアに移動します。

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. クリックしてページの各セクションを展開し、次の設定を行います。

#### 税金計算の設定

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` （使用可能な場合） |

{style="table-layout:auto"}

#### 税金クラス

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （送料は課税されます） |

{style="table-layout:auto"}

#### デフォルト税金宛先計算

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | （適宜） |
| [!UICONTROL Default Postal Code] | `*` アスタリスク） |

{style="table-layout:auto"}

#### 買い物かごの表示設定

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### 固定製品税

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| すべての FPT 表示設定 | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### 手順 2：カナダの物品サービス税（GST）を設定する

請求書およびその他の営業文書に GST 番号を印刷するには、該当する税率の名前に GST 番号を含めます。 GST は、注文概要の GST 金額の一部として表示されます。

#### 税金ゾーンおよび税率の管理

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` アスタリスク） |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 手順 3: カナダの州売上税（PST）の設定

該当する都道府県に別の税率を設定します。

#### 税率情報

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 手順 4:GST 税務処理基準の作成

税金の複合化を回避し、計算された税金を GST と PST の別々の明細項目として正しく表示するには、各基準に異なる優先度を設定し、 **小計のみを計算** チェックボックス。 各税金は個別の明細項目として表示されますが、税額は合計されません。

#### 税務処理基準情報

| フィールド | 推奨設定 |
|--- |--- |
| 名前 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスを選択します。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 手順 5: Saskatchewan の PST 税務処理基準の作成

この税務処理基準では、必ず優先度を 0 に設定し、 **小計のみを計算** チェックボックス。 各税金は個別の明細項目として表示されますが、税額は合計されません。

#### 税務処理基準情報

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスを選択します。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 手順 6：結果を保存してテストする

1. 完了したら、 **[!UICONTROL Save Config]**.

1. ストアフロントに戻り、サンプル注文を作成して結果をテストします。

## EU 税務コンフィギュレーション

次の例は、フランスを拠点とする店舗で、フランスで 100k 以上のユーロ、ドイツで 100k 以上のユーロを販売している様子を示しています。

- 税計算は、web サイトレベルで管理されます。
- 通貨換算と税金表示のオプションは、ストア表示レベルで個別に制御されます（デフォルトを上書きする場合は、「Web サイトを使用」チェックボックスを選択します）。
- デフォルトの税国を設定すると、管轄区域に対する正しい税金を動的に表示できます。
- 関連商品に対する固定製品税は製品属性として含まれます。
- カタログが正しいカテゴリ、web サイト、ストアの表示に表示されるように、カタログを編集する必要が生じる場合があります。

### 手順 1: 3 つの製品税区分の作成

この例では、複数の VAT-Reduced 製品税クラスが不要であると想定しています。

1. VAT 標準製品税区分を作成します。

1. VAT 控除済製品税区分を作成します。

1. VAT 非課税製品税クラスを作成します。

### 手順 2：フランスとドイツの税率の作成

次の税率を作成します。

| 税率 | 設定 |
|--- |--- |
| フランス - StandardVAT | 国：フランス <br/>都道府県/地域：* <br/>郵便番号：* <br/>割合：20% |
| フランス – ReducedVAT | 国：フランス <br/>都道府県/地域：* <br/>郵便番号：* <br/>割合：5% |
| Germany-StandardVAT | 国：ドイツ <br/>都道府県/地域：* <br/>郵便番号：*料金：19% |
| Germany-ReducedVAT | 国：ドイツ <br/>都道府県/地域：* <br/>郵便番号：* <br/>割合：7% |

{style="table-layout:auto"}

### 手順 3：税務処理基準の設定

次の税務処理基準を作成します。

| 税務処理基準 | 設定 |
|--- |--- |
| 小売 – フランス - StandardVAT | 顧客クラス：小売顧客 <br/>税金区分：VAT 標準 <br/>税率：France-StandardVAT <br/>優先度：0 <br/>並べ替え順：0 |
| 小売 – フランス – ReducedVAT | 顧客クラス：小売顧客 <br/>税金区分：VAT 減額 <br/>税率：フランスから減額された VAT <br/>優先度：0 <br/>並べ替え順：0 |
| 小売 – ドイツ – StandardVAT | 顧客クラス：小売顧客 <br/>税金区分：VAT 標準 <br/>税率：Germany-StandardVAT <br/>優先度：0 <br/>並べ替え順：0 |
| 小売 – ドイツ – ReducedVAT | 顧客クラス：小売顧客 <br/>税金区分：VAT 減額 <br/>税率：ドイツの VAT 減額 <br/>優先度：0 <br/>並べ替え順：0 |

{style="table-layout:auto"}

### 手順 4：ドイツのストア表示の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. デフォルトの web サイトで、のストア表示を作成します。 **[!UICONTROL Germany]**.

1. 次に、以下の手順を実行します。

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - 左上隅にを設定します **[!UICONTROL Default Config]** フランスの店に。

   - 一般ページで、を展開します。 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Countries Options]** セクションで、デフォルトの国をに設定します。 `France`.

   - 必要に応じてロケールオプションを入力します。

1. 左上隅の「ドイツ語」を選択します **[!UICONTROL Store View]**.

1. 日 _一般_ ページ、展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** デフォルトの国をに設定します。 `Germany`.

1. 必要に応じてロケールオプションを入力します。

### 手順 5：フランスの税金設定の構成

次の一般税金設定を入力します。

| フィールド | 推奨設定 |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （送料は課税されます） |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` アスタリスク） |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 手順 6：ドイツの税金設定の構成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 右上隅で、を設定します **[!UICONTROL Store View]** ドイツのストアのビューに移動し、 **[!UICONTROL OK]** を確認します。

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. が含まれる **[!UICONTROL Default Tax Destination Calculation]** セクションで、次の操作を行います。

   - をクリア **[!UICONTROL Use Website]** 各フィールドの後のチェックボックス、

   - サイトの配送設定に合わせるには [原点](shipping-settings.md#point-of-origin)、次の値を更新します。

      - デフォルトの国
      - デフォルトの状態
      - 既定の Post コード

     この設定により、製品価格に税金が含まれる場合に税金が正しく計算されます。

     ![デフォルト税金宛先計算](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
