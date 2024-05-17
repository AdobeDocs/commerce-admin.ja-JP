---
title: 固定製品税（FPT）
description: 特定のタイプの製品に追加する必要がある固定製品税（FPT）の設定方法を説明します。
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---

# 固定製品税（FPT）

一部の税管轄区域には、特定のタイプの製品に追加する必要がある固定税があります。 を設定できます _固定製品税_ ストアの税額計算に必要な FPT。 一部の国では、FPT を使用して廃電気電子機器（WEEE）税を設定できます。 この税金は次のものとしても知られています _生態学的税_ または _エコ税_、およびリサイクルのコストを相殺するために、特定の種類の電子機器に収集されます。 これは製品価格のパーセンテージではなく、固定金額です。

固定製品税は、製品に基づいて品目レベルで適用されます。 一部の国や地域では、この税に対して % の税金が別途計算されます。 また、税管轄区域によっては、税金付きまたは税金なしの製品価格が顧客にどのように表示されるかに関するルールが存在する場合があります。 ルールを理解し、それに応じて FPT 表示オプションを設定してください。

価格の違いが注文の顧客の信頼に影響を与える可能性があるので、メールで FPT 価格を見積もる際は注意が必要です。 例えば、FPT を表示せずに注文レビューの価格を表示すると、関連する FPT を持つ品目を購入した顧客には、FPT の税額を含み、項目別の内訳のない合計が表示されます。 価格の違いにより、一部の顧客は、合計が予想される金額と異なるので、買い物かごを放棄する可能性があります。

## FPT 表示価格

| FPT | ディスプレイの設定と計算 | |
|--- |--- |---|
| 非課税 | **[!UICONTROL Excluding FPT]** | FPT は、買い物かごに個別の行として表示され、その値は適切な税金計算で使用されます。 |
| | **[!UICONTROL Including FPT]** | FPT は品目の基本価格に追加されますが、税務処理基準ベースの計算には含まれません。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 価格は、FPT の金額や説明なしで表示されます。 FPT は、税務処理基準ベースの計算には含まれません。 |
| Taxed | **[!UICONTROL Excluding FPT]** | FPT は、買い物かごに個別の行として表示され、その値は適切な税金計算で使用されます。 |
| | **[!UICONTROL Including FPT]** | FPT は品目の価格に含まれており、税金計算の変更は必要ありません。 |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 価格は、FPT の金額や説明なしで表示されます。 ただし、FPT は税務処理基準ベースの計算に含まれます。 |

{style="table-layout:auto"}

## FPT の設定

固定製品税（FPT） [入力タイプ](../catalog/attributes-input-types.md) 各地域の税金を管理するためのフィールドのセクションを作成します。

次の手順は、「エコタックス」を例として使用して、店舗の固定製品税を設定する方法を示しています。 税金の範囲と税金が適用される国および州を設定した後、選択したオプションに応じて、入力フィールドは地域の要件に従って変更できます。 詳しくは、 [製品属性の作成](../catalog/attribute-product-create.md).

### 手順 1：固定製品税を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Fixed Product Taxes]** セクション。

1. を設定 **[!UICONTROL Enable FPT]** 対象： `Yes`.

1. 店舗価格での固定製品税の使用方法を決定するには、次の各価格表示場所に対して FPT 設定を選択します。

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   オプション（それぞれに同じ）:

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. を設定 **[!UICONTROL Apply Tax to FPT]** 必要に応じて。

1. を設定 **[!UICONTROL Include FPT in Subtotal]** 必要に応じて。

   ![固定製品税](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [固定製品税](../configuration-reference/sales/tax.md#fixed-product-taxes) が含まれる _設定リファレンスガイド_.

1. 完了したら、 **[!UICONTROL Save Config]**.

### 手順 2:FPT 属性の作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Attribute]** 次の手順を実行します。

   - の場合 **[!UICONTROL Default Label]**：属性を識別するラベルを入力します。

   - を設定 **[!UICONTROL Catalog Input for Store Owner]** 対象： `Fixed Product Tax`.

   ![属性プロパティ](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Attribute Properties]** セクションに移動して、プロパティのオプションを設定します。

   - **[!UICONTROL Attribute Code]** - スペースや特殊文字を含めず、小文字で一意の ID を入力します。 最大長は 30 文字です。 デフォルトラベル フィールドでは、テキストへのフィールドの入力は省略することができます。

   - **[!UICONTROL Add to Column Options]** - FPT フィールドをに表示する場合 [商品リスト](../catalog/products-list.md)、に設定 `Yes`.

   - **[!UICONTROL Use in Filter Options]**  – 次の操作を行う必要がある場合 [フィルター](../getting-started/admin-workspace.md) fpt フィールドの値に基づくグリッドの製品（に設定） `Yes`.

   ![詳細属性プロパティ](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. （オプション）左側のパネルで、 **[!UICONTROL Manage Labels]** そして、各ストア表示のデフォルトのラベルの代わりに使用するラベルを入力します。

   ![ラベルの管理](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Attribute]**.

1. プロンプトが表示されたら、 [キャッシュ](../systems/cache-management.md).

### 手順 3：属性セットへの FPT 属性の追加

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. リストで属性セットをクリックして、レコードを編集モードで開きます。

   ![属性セット リスト](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. リストから FPT アトリビュートをドラッグします **[!UICONTROL Unassigned Attributes]** ～の右側に **[!UICONTROL Groups]** 中央の列のリスト。

   各グループフォルダーは、製品情報のセクションに対応しています。 編集モードで製品を開いたときに表示される任意の場所に属性を配置できます。

   ![属性セットを編集](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save]**.

1. 固定製品税を含める必要がある属性セットごとに、この手順を繰り返します。

### 手順 4：特定の製品への FPT の適用

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 固定製品税を必要とする製品を編集モードで開きます。

1. の検索 **[!UICONTROL FPT]** 属性セットに追加したフィールドのセクションで、 **[!UICONTROL Add Tax]**.

1. 商品に適用される税金を指定します。

   ![カナダの固定製品税](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - Commerce インスタンスに複数の web サイトがある場合は、適切なものを選択します **[!UICONTROL Website]** と基本通貨。 この例では、フィールドはデフォルトでに設定されています `All Websites [USD]`.

   - を設定 **[!UICONTROL Country/State]** 固定製品税が適用される地域。

   - の場合 **[!UICONTROL Tax]**&#x200B;で、固定製品税を小数で入力します。

1. 固定製品税をさらに追加するには、次をクリックします： **[!UICONTROL Add Tax]** そしてプロセスを繰り返します。

1. 完了したら、 **[!UICONTROL Save]**.
