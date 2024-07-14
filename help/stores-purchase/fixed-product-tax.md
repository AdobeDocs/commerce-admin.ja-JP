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

一部の税管轄区域には、特定のタイプの製品に追加する必要がある固定税があります。 ストアの税計算に必要に応じて _固定製品税_ （FPT）を設定できます。 一部の国では、FPT を使用して廃電気電子機器（WEEE）税を設定できます。 この税は _エコロジカル税_ または _エコロジカル税_ とも呼ばれ、リサイクルのコストを相殺するために特定の種類の電子機器に対して徴収されます。 これは製品価格のパーセンテージではなく、固定金額です。

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

固定製品税（FPT） [ 入力タイプ ](../catalog/attributes-input-types.md) は、地域ごとに税を管理するためのフィールドのセクションを作成します。

次の手順は、「エコタックス」を例として使用して、店舗の固定製品税を設定する方法を示しています。 税金の範囲と税金が適用される国および州を設定した後、選択したオプションに応じて、入力フィールドは地域の要件に従って変更できます。 詳しくは、[ 製品属性の作成 ](../catalog/attribute-product-create.md) を参照してください。

### 手順 1：固定製品税を有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Tax]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Fixed Product Taxes]**」セクションを展開します。

1. **[!UICONTROL Enable FPT]** を `Yes` に設定します。

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

1. 必要に応じて **[!UICONTROL Apply Tax to FPT]** を設定します。

1. 必要に応じて **[!UICONTROL Include FPT in Subtotal]** を設定します。

   ![ 固定製品税 ](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   これらの各設定の詳細については、『 [ 設定リファレンスガイド _の ](../configuration-reference/sales/tax.md#fixed-product-taxes) 固定製品税_ を参照してください。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### 手順 2:FPT 属性の作成

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Product]**に移動します。

1. 右上隅の「**[!UICONTROL Add New Attribute]**」をクリックして、次の操作を行います。

   - **[!UICONTROL Default Label]**：属性を識別するラベルを入力します。

   - **[!UICONTROL Catalog Input for Store Owner]** を `Fixed Product Tax` に設定します。

   ![ 属性プロパティ ](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. **[!UICONTROL Advanced Attribute Properties]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、プロパティのオプションを設定します。

   - **[!UICONTROL Attribute Code]** - スペースや特殊文字を含まない一意の ID を小文字で入力します。 最大長は 30 文字です。 デフォルトラベル フィールドでは、テキストへのフィールドの入力は省略することができます。

   - **[!UICONTROL Add to Column Options]** - FPT フィールドを [ 製品リスト ](../catalog/products-list.md) に表示する場合は、`Yes` に設定します。

   - **[!UICONTROL Use in Filter Options]** - FPT フィールドの値に基づいてグリッド内の製品を [ フィルタリング ](../getting-started/admin-workspace.md) できるようにする場合は、`Yes` に設定します。

   ![ 詳細属性プロパティ ](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. （オプション）左パネルで「**[!UICONTROL Manage Labels]**」を選択し、各ストアビューのデフォルトのラベルの代わりに使用するラベルを入力します。

   ![ ラベルの管理 ](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Attribute]**」をクリックします。

1. プロンプトが表示されたら、[ キャッシュ ](../systems/cache-management.md) を更新します。

### 手順 3：属性セットへの FPT 属性の追加

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Attributes]_/**[!UICONTROL Attribute Set]**に移動します。

1. リストで属性セットをクリックして、レコードを編集モードで開きます。

   ![ 属性セット一覧 ](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. FPT アトリビュートを右側の **[!UICONTROL Unassigned Attributes]** のリストから中央のカラムの **[!UICONTROL Groups]** のリストにドラッグします。

   各グループフォルダーは、製品情報のセクションに対応しています。 編集モードで製品を開いたときに表示される任意の場所に属性を配置できます。

   ![ 属性セットを編集 ](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. 固定製品税を含める必要がある属性セットごとに、この手順を繰り返します。

### 手順 4：特定の製品への FPT の適用

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 固定製品税を必要とする製品を編集モードで開きます。

1. 属性セットに追加したフィールドの「**[!UICONTROL FPT]**」セクションを検索し、「**[!UICONTROL Add Tax]**」をクリックします。

1. 商品に適用される税金を指定します。

   ![ カナダの固定製品税 ](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - Commerce インスタンスに複数の web サイトがある場合は、適切な **[!UICONTROL Website]** および基本通貨を選択します。 この例では、フィールドはデフォルトで `All Websites [USD]` に設定されています。

   - 固定製品税が適用される地域に **[!UICONTROL Country/State]** を設定します。

   - **[!UICONTROL Tax]** の場合は、固定製品税を小数で入力します。

1. 固定製品税をさらに追加するには、[**[!UICONTROL Add Tax]**] をクリックして手順を繰り返します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。
