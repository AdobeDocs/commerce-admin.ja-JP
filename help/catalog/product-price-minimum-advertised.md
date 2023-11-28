---
title: 最小広告価格
description: 特別価格で製造元の要件に準拠するために、最小アドバタイズ価格 (MAP) 機能を使用する方法を説明します。
exl-id: ccd44cfe-3967-4d82-b5b2-3f92701d152e
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 0%

---

# 最小広告価格

マーチャントは、製造元が提示する小売価格 (MSRP) より低い価格を表示することを禁止される場合があります。 最小広告価格 (MAP) を使用すると、お客様により高い価格を提供しながら、製造元の要件に準拠し続けることができます。 要件は製造元によって異なるので、ストアを設定して、許可されていないページに実際の価格が表示されないようにすることができます。

MAP 機能により、専用の _クリックして価格_ リンクを使用して、通常の製品価格の代わりに使用できます。 ストア内の価格がその商品の最小設定価格を下回る場合、価格情報をストアフロントで処理する方法は 2 つあります。 1 つ目の方法は、価格が表示されないことです。 購入者が _クリックして価格_ ボタンが表示され、その後、製品を販売する実際の価格が表示されます。 2 つ目の方法は、価格が低いことを強調するために、取り消し線付きでリスト/市場価格が表示される点です。

また、MAP 機能を使用すると、いくつかの改善点を提案できます。 例えば、顧客が買い物かごにこのような製品を追加した場合、その顧客は買い物かごにリダイレクトされず、代わりにオファーが表示され、購入者は次の操作を実行できます。

- 買い物かごから品目を削除します（購入者が価格を明確にしたいだけで、まだ購入を決定していない場合に実行できます）。

- 買い物かごに入れて、買い物を続ける

- チェックアウトに進みます。

## MAP ロジック

一部の製品には、カスタムオプションや、独自の SKU および在庫管理を持つシンプルな製品など、選択したオプションに応じた価格が設定されています。 これらの製品に対して、製品のタイプと価格の設定に応じて、次のロジックが適用されます。 実際の価格は、注文管理、顧客管理ツール、およびレポートで使用されます。

## 製品タイプでの MAP の使用

| 製品タイプ | 説明 |
|--- |--- |
| [シンプル](product-create-simple.md), [仮想](product-create-virtual.md) | 実際の価格は、カタログリストおよび商品ページに自動的には表示されませんが、 [!UICONTROL Display Actual Price] 設定。 カスタムオプションの価格は通常どおり表示されます。 |
| [グループ化](product-create-grouped.md) | 関連するシンプルな製品の価格は、カタログリストや製品ページには自動的に表示されませんが、 [!UICONTROL Display Actual Price] 設定。 |
| [設定可能](product-create-configurable.md) | 実際の価格は、カタログリストおよび商品ページに自動的には表示されませんが、 [!UICONTROL Display Actual Price] 設定。 オプションの価格は正常に表示されます。 |
| [バンドル](product-create-bundle.md) （固定価格で） | 実際の価格は、カタログページには自動的に表示されませんが、 [!UICONTROL Display Actual Price] 設定。 バンドルアイテムの価格は正常に表示されます。 MAP は、動的な価格設定を持つバンドル製品では使用できません。 |
| [ダウンロード可能](product-create-downloadable.md) | 実際の価格は、カタログリストおよび商品ページに自動的には表示されませんが、 [!UICONTROL Display Actual Price] 設定。 各ダウンロードリンクに関連付けられている価格は、通常どおり表示されます。 |

{style="table-layout:auto"}

## 価格設定での MAP の使用

| 価格設定 | 説明 |
|--- |--- |
| 主な価格 | MAP をメイン価格に適用すると、オプション、バンドル品目、および関連製品（メイン価格から追加または差し引く）の価格が通常どおりに表示されます。 |
| 関連製品価格 | 製品にメイン価格がなく、その価格が関連する製品価格（グループ化された製品など）から導き出される場合、関連する製品の MAP 設定が適用されます。 |
| [MSRP](product-price-minimum-advertised.md) | 買い物かご内の製品に製造元の提示小売価格 (MSRP) が指定されている場合、価格はクロスアウトされません。 |
| [価格帯](product-price-tier.md) | 階層価格が設定されている場合、階層価格メッセージはカタログに表示されません。 製品ページに、一定の数量を超える注文時に価格が安くなる可能性があるが、割引はパーセンテージでのみ表示されることを示す通知が表示されます。 グループ化された製品に関連する製品の場合、割引は製品ページに表示されません。 階層価格は、「実際の価格を表示」設定に従って表示されます。 |
| [特別価格](product-price-special.md) | [ 特別価格 ] が指定されている場合は、[ 実際の価格を表示 ] の設定に従って特別価格が表示されます。 |

## MAP 設定

Minimum Advertised Price(MAP) 機能は、デフォルトでは有効になっていません。 この機能をストアに追加する場合は、この機能を有効にして、製品の MAP 設定を構成する必要があります。 MAP 設定は、カタログ内のすべての製品に適用することも、特定の製品に対して設定することもできます。 MAP がグローバルに有効になっている場合、ストアフロント内のすべての製品価格は表示されません。 製造元との契約条件に従い、顧客により良い価格を提供しながら、様々な設定オプションを使用できます。

![実際の価格は「ジェスチャー時」と表示される](./assets/storefront-msrp-on-gesture.png){width="700" zoomable="yes"}

グローバルレベルで、MAP を有効または無効にし、すべての製品に適用し、実際の価格の表示方法を定義できます。 ストアに表示される関連メッセージや情報ヒントのテキストを編集することもできます。

MAP が有効になっている場合は、製品レベルの MAP 設定が使用可能になります。 MSRP を入力し、実際の価格をストアに表示する方法を選択することで、個々の製品に MAP を適用できます。 製品レベルの MAP 設定は、グローバル MAP 設定に優先します。

![クリックして価格](./assets/storefront-price-map.png){width="700" zoomable="yes"}

### 手順 1：ストア表示の MAP を有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 該当する場合は、 **[!UICONTROL Store View]** が、設定が適用されるビューの右上隅に表示されます。

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の _[!UICONTROL Minimum Advertised Price]_」セクションに入力します。

1. 必要に応じて、 **MAP を有効にする** から `Yes`.

   ![MAP 設定](./assets/sales-minimum-advertised-price.png){width="600" zoomable="yes"}

   これらの設定オプションの詳細なリストについては、 [_最小広告価格_](../configuration-reference/sales/sales.md#minimum-advertised-price) （内） _設定リファレンス_.

### 手順 2: MAP 設定を指定する

次のいずれかの方法を使用して、MAP 設定を指定します。

#### 方法 1：すべての製品の MAP を設定する

1. 実際の価格を顧客に表示するタイミングと場所を決定するには、次の手順を実行します。

   - デフォルト値を変更するには、「 **[!UICONTROL Use system value]** チェックボックス。

   - 設定 **実際の価格を表示** を次のいずれかに変更します。
      - `In Cart`
      - `Before Order Confirmation`
      - `On Gesture (on click)`

1. に表示するテキストを入力します **[!UICONTROL Default Popup Text Message]**.

1. 表示する追加の説明を **[!UICONTROL Default "What's This" Text Message]**.

1. 完了したら、「 **[!UICONTROL Save Config]**.

#### メソッド 2：単一の製品に対して MAP を設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Inventory]** > **[!UICONTROL Products]**.

1. で製品を開きます。 **[!UICONTROL Edit]** モード。

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced Settings]** を選択します。 **[!UICONTROL Advanced Pricing]**.

   >[!NOTE]
   >
   >The [!UICONTROL Manufacturer's Suggested Retail Price] および [!UICONTROL Display Actual Price] フィールドは次の場合にのみ表示されます： [最小広告価格](../configuration-reference/sales/sales.md#minimum-advertised-price) が設定で有効になっている。

1. 次を入力します。 **[!UICONTROL Manufacturer's Suggested Retail Price]** (MSRP)。

   この例では、製品価格は$54.00 で、MSRP は 59.95 です。

   ![製造元の推奨小売価格](./assets/product-price-msrp.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display Actual Price]** を次のいずれかに変更します。

   - `Use config` - （デフォルト）表示設定を [設定済み](../configuration-reference/sales/sales.md#minimum-advertised-price) ストアの。 |
   - `On Gesture`  — 顧客が _クリックして価格_ または _これは何だ？_ リンク。
   - `In Cart`  — 買い物かごの実際の製品価格を表示します。
   - `Before Order Confirmation`  — チェックアウトプロセスの最後、注文が確認される直前の実際の製品価格を表示します。

1. 完了したら、「 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.
