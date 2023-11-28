---
title: 国別税ガイドライン
description: 国に応じて推奨税設定を確認します。
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 国別税ガイドライン

## 米国の税金設定

これらの推奨設定は、米国内の店舗のほとんどの税金設定に使用できます。

| 税オプション | 推奨 |
|--- |--- |
| カタログ価格を読み込み | 税別 |
| FPT | いいえ、FPT は課税されていないので。 |
| 次に基づく税 | 発送元 |
| 税額計算 | 合計 |
| 税送り？ | いいえ |
| 割引の適用 | 税引前 |
| コメント | すべての税ゾーンは同じ優先順位です。理想的には、州のゾーンと郵便番号の参照の 1 つ以上のゾーンです。 |

{style="table-layout:auto"}

### 税区分

| 税区分 | 推奨設定 |
|--- |--- |
| 配送用の税区分 | なし |

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

### デフォルトの税金宛先の計算

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | ビジネスの所在地を示します。 |
| [!UICONTROL Default Post Code] | 税金ゾーンで使用される郵便番号。 |

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

### オーダー、請求書、クレジット・メモおよび表示設定

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 固定製品税 (FPT)

| オプション | 推奨設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`カリフォルニア以外は |

{style="table-layout:auto"}

## 英国の税金設定

これらの推奨設定は、英国内の店舗のほとんどの税金設定に使用できます。

### UK B2C 税構成

| 税オプション | 推奨 |
|--- |--- |
| カタログ価格を読み込み | 税別 |
| FPT | はい（FPT と説明を含む） |
| 次に基づく税 | [!UICONTROL Shipping Address] |
| 税額計算 | 合計 |
| 税送り？ | はい |
| 割引の適用 | 税引き前、税引きを含む価格の割引。 |
| コメント | 仕入先請求書（VAT を含む）をマークアップする商人用。 |

{style="table-layout:auto"}

### 英国 B2B 税構成

| 税オプション | 推奨 |
|--- |--- |
| カタログ価格を読み込み | 税別 |
| FPT | はい（FPT と説明を含む） |
| 次に基づく税 | [!UICONTROL Shipping Address] |
| 税額計算 | 項目 |
| 税送り？ | はい |
| 割引の適用 | 税引き前、税引きを含む価格の割引。 |
| コメント | B2B マーチャントがよりシンプルな VAT サプライチェーンの検討事項を提供するため。 行に対する税金計算も有効ですが、課税管轄区域に確認してください。 商人がサプライチェーンに属し、販売された商品が他のベンダーによって VAT のリベートなどに使用されると想定します。 この定義により、品目別の税金を容易に識別して、リベートの生成を高速化できます。 <br/><br/>**_注意：_**一部の管轄地域では、Commerce で現在サポートされていない様々な端数処理戦略が必要です。また、すべての管轄地域で品目または行レベルの税金が許可されているわけではありません。 |

{style="table-layout:auto"}

## カナダの税金設定

>[!IMPORTANT]
>
>GST/PST 州（モントリオール）に属する商人は、1 つの税務処理基準を作成し、合計税額を表示する必要があります。 ご質問がある場合は、必ず適格な税務当局に問い合わせてください。 特定の都道府県の税金要件の詳細は、次を参照してください。 [レヴュクエベック][1], [サスカチュワン政府][2]、および [ベンダー向けマニトバ情報][3]

| 税オプション | 推奨 |
|--- |--- |
| カタログ価格を読み込み | 税別 |
| FPT | はい（FPT、摘要を含む）。FPT に税を適用します。 |
| 次に基づく税 | 発送元 |
| 税額計算 | 合計 |
| 税送り？ | はい |
| 割引の適用 | 税引前 |

{style="table-layout:auto"}

次の例は、2 つの税率を計算および表示する税ルールを使用して、カナダの GST 税率とサスカチュワンの PST 税率を設定する方法を示しています。 この情報は、構成例の概要を示します。税金管轄区域に対する正しい税率とルールを必ず確認してください。 税金を設定する場合は、ストアの範囲を設定して、該当するすべてのストアおよび Web サイトに設定を適用します。

- 関連商品に対する固定製品税は、製品属性として含まれます。
- ケベックでは、PST は TVQ と呼ばれます。 Quebec のレートを設定する場合は、TVQ を識別子として使用するようにしてください。

### 手順 1：税金計算設定の完了

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. マルチサイト設定の場合は、 **[!UICONTROL Store View]** を web サイトに追加し、設定のターゲットとなるを保存します。

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. をクリックしてページの各セクションを展開し、次の設定を実行します。

#### 税金計算設定

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

#### 税区分

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （送料は課税） |

{style="table-layout:auto"}

#### デフォルトの税金宛先の計算

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | （必要に応じて） |
| [!UICONTROL Default Postal Code] | `*` （アスタリスク） |

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

### ステップ 2：カナダ物品・サービス税 (GST) の設定

請求書および他の販売ドキュメントに対して GST 番号を印刷するには、該当する税率の名前にその番号を含めます。 GST は、任意の注文概要の GST 金額の一部として表示されます。

#### 税ゾーンと税率の管理

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` （アスタリスク） |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 手順 3：カナダの省の消費税 (PST) の設定

該当する都道府県に対して別の税率を設定します。

#### 税率情報

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 手順 4: GST 税ルールの作成

税の複合を避け、計算された税を GST と PST の個別の明細項目として正しく表示するには、各ルールに異なる優先順位を設定し、 **小計のみを計算** チェックボックス。 各税金は別々の明細品目として表示されますが、税額は複合されません。

#### 税務処理基準情報

| フィールド | 推奨設定 |
|--- |--- |
| 名前 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスをオンにします。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### ステップ 5：サスカチュワンの PST 税ルールを作成する

この税務処理基準では、優先度を 0 に設定し、 **小計のみを計算** チェックボックス。 各税金は別々の明細品目として表示されますが、税額は複合されません。

#### 税務処理基準情報

| フィールド | 推奨設定 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスをオンにします。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 手順 6：結果を保存してテストする

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. ストアフロントに戻り、結果をテストするためのサンプルの順序を作成します。

## EU 税設定

次の例では、フランスをベースにした店舗で、フランスで 100k+ユーロ、ドイツで 100k+ユーロを販売しています。

- 税金の計算は Web サイトレベルで管理されます。
- 通貨換算および税金の表示オプションは、店舗表示レベルで個別に制御します（デフォルトを上書きするには、「 Web サイトを使用」チェックボックスを選択します）。
- デフォルトの税金国を設定すると、管轄区域に対する正しい税金を動的に表示できます。
- 関連商品に対する固定製品税は、製品属性として含まれます。
- カタログが正しいカテゴリ、Web サイト、ストアの表示に表示されるように、カタログを編集する必要が生じる場合があります。

### 手順 1: 3 つの製品税区分を作成します。

この例では、複数の VAT-Reduced 製品税区分が必要ないと想定しています。

1. VAT-Standard 製品税区分を作成します。

1. VAT-Reduced 製品税区分を作成します。

1. VAT-Free 製品税区分を作成します。

### ステップ 2：フランスとドイツの税率の作成

次の税率を作成します。

| 税率 | 設定 |
|--- |--- |
| フランス — 標準 VAT | 国：フランス <br/>都道府県/地域： * <br/>郵便番号： * <br/>率： 20% |
| フランス — 還元 VAT | 国：フランス <br/>都道府県/地域： * <br/>郵便番号： * <br/>料金： 5% |
| ドイツ — 標準 VAT | 国：ドイツ <br/>都道府県/地域： * <br/>郵便番号： *率： 19% |
| ドイツ — 還元 VAT | 国：ドイツ <br/>都道府県/地域： * <br/>郵便番号： * <br/>料金： 7% |

{style="table-layout:auto"}

### 手順 3：税務処理基準の設定

次の税務処理基準を作成します。

| 税ルール | 設定 |
|--- |--- |
| 小売 — フランス — 標準 VAT | 顧客クラス：小売顧客 <br/>税区分： VAT — 標準 <br/>税率：フランス — 標準 VAT <br/>優先度：0 <br/>並べ替え順： 0 |
| 小売 — フランス — 還元 VAT | 顧客クラス：小売顧客 <br/>税区分：減価税 <br/>税率：フランス — 還元 VAT <br/>優先度：0 <br/>並べ替え順： 0 |
| 小売 — ドイツ — 標準 VAT | 顧客クラス：小売顧客 <br/>税区分： VAT — 標準 <br/>税率：ドイツ — 標準 VAT <br/>優先度：0 <br/>並べ替え順： 0 |
| 小売 — ドイツ — 還元 VAT | 顧客クラス：小売顧客 <br/>税区分： VAT-Reduced <br/>税率：ドイツ — 還元 VAT <br/>優先度：0 <br/>並べ替え順： 0 |

{style="table-layout:auto"}

### 手順 4：ドイツのストア表示の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. デフォルトの Web サイトの下で、 **[!UICONTROL Germany]**.

1. 次に、以下の手順を実行します。

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - 左上隅で、 **[!UICONTROL Default Config]** フランスの店に

   - 一般ページで、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Countries Options]** 」セクションに移動し、デフォルトの国を `France`.

   - 必要に応じて、ロケールのオプションを設定します。

1. 左上隅で、ドイツ語を選択します。 **[!UICONTROL Store View]**.

1. 次の日： _一般_ ページ、展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** デフォルトの国をに設定します。 `Germany`.

1. 必要に応じて、ロケールのオプションを設定します。

### 手順 5：フランスの税設定を構成する

次の一般税設定を実行します。

| フィールド | 推奨設定 |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （送料は課税） |
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
| [!UICONTROL Default Postal Code] | `*` （アスタリスク） |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 手順 6：ドイツの税設定を構成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 右上隅で、 **[!UICONTROL Store View]** をクリックして、ドイツのストアのビューに移動し、 **[!UICONTROL OK]** をクリックして確定します。

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. Adobe Analytics の **[!UICONTROL Default Tax Destination Calculation]** セクションで、以下の操作を実行します。

   - 次をクリア： **[!UICONTROL Use Website]** 各フィールドの後にあるチェックボックス

   - サイトの配送設定に合わせるには [原点](shipping-settings.md#point-of-origin)、次の値を更新します。

      - デフォルトの国
      - デフォルトの状態
      - デフォルトの Post コード

     この設定は、製品価格に税が含まれる場合に、税が正しく計算されるようにします。

     ![デフォルトの税金宛先の計算](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
