---
title: テーブル レート配送
description: ストアに定額配送オプションを設定する方法を説明します。
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 3%

---

# テーブル レート配送

この _テーブル率_ 出荷方法では、データのテーブルが参照され、次のような条件の組合せに基づいて出荷率が計算されます。

- 重み付けと宛先
- 価格 v.目的地
- 項目の数 v.宛先

例えば、倉庫がロサンゼルスにある場合、バーモントよりもサンディエゴに発送する方が費用は安くなります。 定額料金による配送を使用して、節約分をお客様に渡すことができます。

テーブル レートの計算に使用されるデータは、スプレッドシートで準備され、ストアにインポートされます。 顧客が見積を要求すると、結果は買い物かごの「出荷見積」セクションに表示されます。

>[!NOTE]
>
>一度にアクティブにできるテーブル・レート・データのセットは 1 つだけです。

![表ショッピング・カート受注要約のレート出荷オプション](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## 手順 1：デフォルト設定の完了

最初の手順は、テーブルのレートのデフォルト設定を完了することです。 この手順は、設定の範囲を変更せずに完了できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. が含まれる _[!UICONTROL Sales]_左パネルの「」セクションで、**[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Table Rates]** セクション。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、説明に従って次の設定を変更します。

   ![テーブル率](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

1. を入力 **[!UICONTROL Title]** チェックアウト時にテーブルの料金セクションに表示する項目。

   デフォルトのタイトルはです。 `Best Way`.

1. を入力 **[!UICONTROL Method Name]** 買い物かごで計算された料金の横にラベルとして表示する場合。

1. を設定 **[!UICONTROL Condition]** を次のいずれかの計算方法に変更します。

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. 仮想製品を含む注文の場合は、次のように設定します **[!UICONTROL Include Virtual Products in Price Calculation]** 対象： `Yes` 計算に仮想製品を含めることができるかどうか。

   >[!NOTE]
   >
   >サービスなどの仮想製品には重み付けがないため、重み付け v.宛先条件に基づく計算結果は変更できません。 ただし、仮想製品は、「価格 v.宛先」または「品目数 vs 宛先条件」のいずれかに基づく計算の結果を変更できます。

1. 要件に応じて手数料オプションを設定します。

   手数料は任意で、送料に加算される追加料金として表示されます。 手数料を含める場合は、次の操作を行います。

   - を設定 **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - を入力 **[!UICONTROL Handling Fee]** 手数料の計算に使用される方法に従ったレート。

     例えば、料金が固定料金に基づいている場合は、次のように金額を小数で入力します `4.90`. ただし、手数料が注文のパーセンテージに基づいている場合は、パーセンテージで金額を入力します。 例えば、注文の 6% を請求する場合は、値を `.06`.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキストボックスにはデフォルトのメッセージが事前に設定されていますが、この配信方法が使用できなくなった場合に表示する別のメッセージを入力できます。

1. を設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたこの配信方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Ship to Specific Countries]_リストが表示されます。 リストで、この配信方法を使用できる国を選択します。

1. を設定 **[!UICONTROL Show Method if Not Applicable]** 対象： `Yes` テーブルの料率を常に表示する場合

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の配信方法と共にリストされた場合に表の料金による配送が表示される順序を決定します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：テーブルレートデータを準備

1. 左上隅にを設定します **[!UICONTROL Store View]** 対象： `Main Website`、または設定が適用される他の web サイトに移動します。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、説明に従って次の設定を変更します。

1. 変更： **[!UICONTROL Condition]** 必要に応じて。

1. クリック **[!UICONTROL Export CSV]**.

   ![CSV を書き出し](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. を保存します `tablerates.csv` ファイルをお使いのシステムに送信します。

1. ファイルをスプレッドシートアプリケーションで開きます。

1. 出荷計算条件の適切な値を使用して、表を完成させます。

   - ワイルドカードとしてアスタリスク （*）を使用し、任意のカテゴリの使用可能なすべての値を表します。
   - この _[!UICONTROL Country]_列にはを含める必要があります [有効な 3 文字コード][1] 各行。
   - データ並べ替え基準 _[!UICONTROL Region/State]_つまり、特定の場所がリストの上部に、ワイルドカードの場所が下部に表示されます。 このメソッドを使用すると、最初に絶対値でルールが処理され、後でワイルドカード値でルールが処理されます。
   - の値 _[!UICONTROL Weight (and above)]_列の小数点以下 4 桁は最大にできます（例：） `2.5075`）に設定します。 データで小数点以下の桁数を増やすと、読み込みが失敗します。

   ![重み付け対宛先（オーストラリア）](./assets/table-rates-weight-destination-csv.png){width="500"}

1. を保存します `tablerates.csv` ファイル。

## 手順 3：テーブルレートデータのインポート

1. に戻る **[!UICONTROL Table Rates]** ストア設定の「」セクション。

1. 左上隅にを設定します **[!UICONTROL Store View]** ：このメソッドを使用する web サイト

1. の場合 **[!UICONTROL Import]**&#x200B;を選択し、 **[!UICONTROL Choose File]** を選択して完了します `tablerates.csv` レートをインポートするファイル。

   ![インポート テーブルの料率](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 手順 4：レートの検証

テーブルレートデータが正しいことを確認するには、いくつかの異なるアドレスで支払いプロセスを実行して、送料と手数料が正しく計算されていることを確認します。

### 例 1：価格と目的地

この例では、「価格 v.宛先」条件を使用して、米国本土、アラスカおよびハワイの注文の小計の金額に基づいて、3 つの異なる配送料のセットを作成します。 アスタリスク（*）は、すべての値を表すワイルドカードです。

| 国 | 地域/州 | 郵便番号 | 注文の小計（と以上） | 送料 |
|--- |--- |--- |--- |--- |
| 米国 | こんにちは | * | 100 | 10 |
| 米国 | こんにちは | * | 50 | 15 |
| 米国 | こんにちは | * | 0 | 20 |
| 米国 | AK | * | 100 | 10 |
| 米国 | AK | * | 50 | 15 |
| 米国 | AK | * | 0 | 20 |
| 米国 | * | * | 100 | 5 |
| 米国 | * | * | 50 | 10 |
| 米国 | * | * | 0 | 15 |

{style="table-layout:auto"}

### 例 2：重み付けと宛先

この例では、重み付け v.宛先条件を使用して、注文の重み付けに基づいて異なる配送料を作成しています。

| 国 | 地域/州 | 郵便番号 | 重み付け（以上） | 送料 |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | ワ | * | 9 | 39.95 |
| AUS | ワ | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### 例 3：米国本土への送料無料の制限

1. を作成 `tablerates.csv` 送料無料を提供する意思のあるすべての州の宛先を含むファイル。

1. テーブル レートの設定を次の設定で行います。

   | 設定 | 値 |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. 左上隅にを設定します **[!UICONTROL Store View]** 対象： `Main Website`、または設定が適用される他の web サイトに移動します。

1. の場合 **[!UICONTROL Import]**&#x200B;を選択し、 **[!UICONTROL Choose File]** を選択して完了します `tablerates.csv` レートをインポートするファイル。


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
