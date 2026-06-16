---
title: 各国の租税ガイドライン
description: 国に応じて推奨される税金設定を確認します。
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
TQID: https://experienceleague.adobe.com/hs8-0P0zSc-du-ubuYHiw7Yg9ps7SMPudBxcJgh-VCc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1337
ht-degree: 0%

---

# 各国の租税ガイドライン

## 米国の税構成

これらの推奨設定は、米国内の店舗のほとんどの税金構成に使用できます。

| 税オプション | 推奨事項 |
|--- |--- |
| カタログの価格を読み込む | 税抜き |
| FPT | いいえ、FPTは課税されないからです。 |
| 税金ベース | 発送元 |
| 税計算 | 合計 |
| 送料は？ | いいえ |
| 割引を適用 | 税引前 |
| コメント | すべての税ゾーンは同じ優先度です。州別ゾーンと郵便番号検索のための1つ以上のゾーンが理想的です。 |

{style="table-layout:auto"}

### 税区分

| 税区分 | おすすめの設定 |
|--- |--- |
| 送料の税区分 | なし |

{style="table-layout:auto"}

### 計算設定

| オプション | おすすめの設定 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### デフォルトの税宛先計算

| オプション | おすすめの設定 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | 事業が所在する国。 |
| [!UICONTROL Default Post Code] | 税金ゾーンで使用される郵便番号。 |

{style="table-layout:auto"}

### 価格表示の設定

| オプション | おすすめの設定 |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### ショッピングカートの表示設定

| オプション | おすすめの設定 |
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

### 注文、請求書、クレジットメモ、および表示設定

| オプション | おすすめの設定 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 固定製品税（FPT）

| オプション | おすすめの設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No` （カリフォルニア州を除く）。 |

{style="table-layout:auto"}

## 英国の税構成

これらの推奨設定は、英国内の店舗のほとんどの税金構成に使用できます。

### 英国のB2C税制

| 税オプション | 推奨事項 |
|--- |--- |
| カタログの価格を読み込む | 税抜き |
| FPT | はい（FPTと説明を含む） |
| 税金ベース | [!UICONTROL Shipping Address] |
| 税計算 | 合計 |
| 送料は？ | はい |
| 割引を適用 | 税引前、税込み価格の割引。 |
| コメント | 仕入先請求書（VATを含む）をマークアップするマーチャントの場合。 |

{style="table-layout:auto"}

### 英国のB2B税制

| 税オプション | 推奨事項 |
|--- |--- |
| カタログの価格を読み込む | 税抜き |
| FPT | はい（FPTと説明を含む） |
| 税金ベース | [!UICONTROL Shipping Address] |
| 税計算 | 項目あり |
| 送料は？ | はい |
| 割引を適用 | 税引前、税込み価格の割引。 |
| コメント | B2B企業がsupply chainに関する考慮事項として、VATを提供する場合。 行の税額計算も有効ですが、お客様の課税管轄区域にご確認ください。 設定では、加盟店がsupply chainに存在し、販売された商品がVATのリベートなどに他の業者によって使用されることを前提としています。 この定義は、より迅速なリベート生成のために、アイテムごとに税金を識別することを容易にします。 <br/><br/>**_Note:_**&#x200B;一部の国や地域では、現在Commerceでサポートされていない異なる丸め方式が必要です。また、すべての国で品目レベルまたは行レベルの税が許可されているわけではありません。 |

{style="table-layout:auto"}

## カナダの税構成

>[!IMPORTANT]
>
>GST/PST州（モントリオール）に住んでいるマーチャントは、1つの税ルールを作成し、複合税額を表示する必要があります。 ご質問がある場合は、必ず適格な税務当局にご相談ください。

| 税オプション | 推奨事項 |
|--- |--- |
| カタログの価格を読み込む | 税抜き |
| FPT | はい、FPT、説明、およびFPTへの税金の適用を含みます。 |
| 税金ベース | 発送元 |
| 税計算 | 合計 |
| 送料は？ | はい |
| 割引を適用 | 税引前 |

{style="table-layout:auto"}

次の例は、カナダのGST税率とサスカチュワン州のPST税率を設定し、2つの税率を計算して表示する税則を使用する方法を示しています。 この情報では、設定例の概要を説明します。必ず、税管轄区域の正しい税率と規則を確認してください。 税金を設定する場合は、ストア範囲を設定して、該当するすべてのストアとweb サイトに設定を適用します。

- 固定商品税は、商品属性として関連商品に含まれます。
- ケベック州では、PSTはTVQと呼ばれます。 ケベックのレートを設定する場合は、必ずTVQを識別子として使用してください。

### ステップ 1：税額計算の設定を完了する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. マルチサイト設定の場合は、設定のターゲットとなるweb サイトとストアに&#x200B;**[!UICONTROL Store View]**&#x200B;を設定します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Tax]**&#x200B;を選択します。

1. クリックしてページの各セクションを展開し、次の設定を完了します。

#### 税計算の設定

| フィールド | おすすめの設定 |
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

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` （送料は課税されます） |

{style="table-layout:auto"}

#### デフォルトの税宛先計算

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | （必要に応じて） |
| [!UICONTROL Default Postal Code] | `*` （アスタリスク） |

{style="table-layout:auto"}

#### ショッピングカートの表示設定

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### 固定製品税

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| すべてのFPT表示設定 | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### ステップ 2：カナダ物品サービス税（GST）の設定

請求書やその他の販売文書にGST番号を印刷するには、該当する税率の名前にGST番号を含めます。 GSTは、注文の概要にGST金額の一部として表示されます。

#### 税ゾーンと税率の管理

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` （アスタリスク） |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### ステップ 3：カナダの州売上税（PST）を設定する

該当する都道府県に別の税率を設定します。

#### 税率に関する情報

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` （アスタリスク） |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 手順4:GST税ルールの作成

税の配合を避け、計算された税をGSTとPSTの個別の品目として正しく表示するには、各ルールに異なる優先順位を設定し、**小計のみ計算** チェックボックスを選択します。 各税金は個別の品目として表示されますが、税額は配合されません。

#### 税ルール情報

| フィールド | おすすめの設定 |
|--- |--- |
| 名前 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスをオンにします。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### ステップ 5:SaskatchewanのPST税ルールを作成する

この税ルールでは、優先度を0に設定し、「**小計のみ計算**」チェックボックスを選択します。 各税金は個別の品目として表示されますが、税額は配合されません。

#### 税ルール情報

| フィールド | おすすめの設定 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | このチェックボックスをオンにします。 |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 手順6：結果を保存してテストする

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. ストアフロントに戻り、サンプル注文を作成して結果をテストします。

## EUの税構成

次の例は、フランスに拠点を置き、フランスで100,000 ユーロ以上、ドイツで100,000 ユーロ以上を販売する店舗を示しています。

- 税金の計算は、web サイトのレベルで管理されます。
- 通貨換算および税表示オプションは、ストアビューレベルで個別に制御されます（デフォルトを上書きするには、「Web サイトを使用」チェックボックスを選択します）。
- デフォルトの税国を設定すると、その法域の正しい税を動的に表示できます。
- 固定商品税は、商品属性として関連商品に含まれます。
- カタログが正しいカテゴリ/web サイト/ストアビューに表示されるように、カタログを編集する必要がある場合があります。

### 手順1:3つの製品税クラスを作成する

この例では、複数のVAT減税された製品税クラスは必要ないと仮定します。

1. VAT-Standard製品税区分を作成します。

1. VAT減税された製品税区分を作成します。

1. VAT フリーの商品税区分を作成します。

### ステップ 2：フランスとドイツの税率を作成する

次の税率を作成します。

| 税率 | 設定 |
|--- |--- |
| フランス標準VAT | 国：フランス <br/>州/地域：* <br/>郵便番号：* <br/>料金：20% |
| France-ReducedVAT | 国：フランス <br/>州/地域：* <br/>郵便番号：* <br/>料金：5% |
| Germany-StandardVAT | 国：ドイツ <br/>州/地域：* <br/>郵便番号：*料金：19% |
| Germany-ReducedVAT | 国：ドイツ <br/>州/地域：* <br/>郵便番号：* <br/>料金：7% |

{style="table-layout:auto"}

### 手順3：税ルールの設定

次の税ルールを作成します。

| 税ルール | 設定 |
|--- |--- |
| Retail-France-StandardVAT | 顧客クラス：小売顧客<br/>税区分：VAT-Standard <br/>税率：France-StandardVAT <br/>優先度：0 <br/>並べ替え順序：0 |
| Retail-France-ReducedVAT | 顧客クラス：小売顧客<br/>税区分：VAT引き下げ<br/>税率：フランス – VAT引き下げ<br/>優先度：0 <br/>並べ替え順序：0 |
| Retail-Germany-StandardVAT | 顧客クラス：小売顧客<br/>税区分：VAT-Standard <br/>税率：ドイツ – StandardVAT <br/>優先度：0 <br/>並べ替え順序：0 |
| Retail-Germany-ReducedVAT | 顧客クラス：小売顧客<br/>税区分：VAT-Reduced <br/>税率：ドイツ – ReducedVAT <br/>優先度：0 <br/>並べ替え順序：0 |

{style="table-layout:auto"}

### ステップ 4：ドイツのストアビューを設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**に移動します。

1. デフォルトのweb サイトで、**[!UICONTROL Germany]**&#x200B;のストアビューを作成します。

1. 次に、次の操作を行います。

   - _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

   - 左上隅で、**[!UICONTROL Default Config]**&#x200B;をフランス語ストアに設定します。

   - 一般ページで、**[!UICONTROL Countries Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、デフォルトの国を`France`に設定します。

   - 必要に応じて、ロケールオプションを完了します。

1. 左上隅で、ドイツ語の&#x200B;**[!UICONTROL Store View]**&#x200B;を選択します。

1. _一般_ ページで、![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]**&#x200B;を展開し、デフォルトの国を`Germany`に設定します。

1. 必要に応じて、ロケールオプションを完了します。

### ステップ 5：フランスの税金設定の設定

次の一般的な税金設定を完了します。

| フィールド | おすすめの設定 |
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
| [!UICONTROL Default Postal Code] | `*` （アスタリスク） |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 手順6：ドイツの税金設定の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 右上隅で、**[!UICONTROL Store View]**&#x200B;をドイツ語ストアのビューに設定し、**[!UICONTROL OK]**&#x200B;をクリックして確定します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Tax]**&#x200B;を選択します。

1. **[!UICONTROL Default Tax Destination Calculation]** セクションで、次の操作を行います。

   - 各フィールドの後に&#x200B;**[!UICONTROL Use Website]** チェックボックスをオフにします。

   - サイトの出荷設定[発信元](shipping-settings.md#point-of-origin)に一致させるには、次の値を更新します。

      - デフォルトの国
      - Default State
      - 既定の郵便番号

     この設定により、商品の価格に税金が含まれている場合に、税金が正しく計算されるようになります。

     ![既定の税宛先計算](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
