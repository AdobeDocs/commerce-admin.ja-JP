---
title: 表料金の送料
description: 店舗のテーブルレートの配送オプションを設定する方法を説明します。
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# 表料金の送料

The _表率_ 発送方法は、次のような条件の組み合わせに基づいて送料を計算するデータのテーブルを参照します。

- 重み付け v.宛先
- 価格 v.宛先
- 項目数 v.宛先

例えば、倉庫がロサンゼルスにある場合、サンディエゴへの配送料はバーモントへの配送料よりも低くなります。 定額料金の配送を使用して、顧客に割引額を渡すことができます。

テーブルのレートの計算に使用されるデータは、スプレッドシートで作成され、ストアにインポートされます。 顧客が見積もりをリクエストすると、結果が買い物かごの出荷見積もりセクションに表示されます。

>[!NOTE]
>
>一度にアクティブにできるテーブルレートデータのセットは 1 つだけです。

![買い物かごの注文概要の「表レートの配送」オプション](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## 手順 1：デフォルト設定を完了する

最初の手順は、表レートのデフォルト設定を完了することです。 設定の範囲を変更せずに、この手順を完了できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Adobe Analytics の _[!UICONTROL Sales]_「 」セクションで、「 」を選択します。**[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Table Rates]** 」セクションに入力します。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、次の設定を変更します。

   ![表レート](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** から `Yes`.

1. 次を入力します。 **[!UICONTROL Title]** をチェックアウト時に、テーブルレートセクションに表示する

   デフォルトのタイトルはです。 `Best Way`.

1. 次を入力します。 **[!UICONTROL Method Name]** 買い物かご内の計算済みレートの横にラベルとして表示する

1. 設定 **[!UICONTROL Condition]** を次のいずれかの計算方法に設定します。

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. 仮想製品を含む注文の場合は、 **[!UICONTROL Include Virtual Products in Price Calculation]** から `Yes` 仮想製品を計算に含める場合。

   >[!NOTE]
   >
   >仮想製品（サービスなど）には重みがないので、重み付け v.宛先条件に基づく計算結果を変更することはできません。 ただし、仮想製品は、価格 v.宛先または品目数と宛先の条件に基づく計算の結果を変更できます。

1. 必要に応じて、取り扱い料金オプションを設定します。

   手数料はオプションで、送料に追加される追加料金として表示されます。 手数料を含める場合は、次の手順を実行します。

   - 設定 **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - 次を入力します。 **[!UICONTROL Handling Fee]** 料金の計算に使用される方法に従った料金。

     例えば、料金が固定料金に基づく場合は、金額を小数で入力します。例： `4.90`. ただし、手数料が注文のパーセンテージに基づいている場合は、金額をパーセンテージで入力します。 例えば、注文の 6%を請求する場合は、値に「 」と入力します。 `.06`.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキストボックスにはデフォルトのメッセージがあらかじめ設定されていますが、この配信方法が使用できなくなった場合に表示する別のメッセージを入力できます。

1. 設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この配信方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Ship to Specific Countries]_リストが表示されます。 この配信方法を使用できる国をリストから選択します。

1. 設定 **[!UICONTROL Show Method if Not Applicable]** から `Yes` 常に表レートを表示する場合

1. の場合 **[!UICONTROL Sort Order]**、数値を入力して、チェックアウト時に他の配信方法と共にリストに表示された場合に表の料金の配送が表示される順序を決定します。

   `0` =最初 `1` =秒 `2` = 3 番目、など。

1. クリック **[!UICONTROL Save Config]**.

## 手順 2：テーブルレートデータの準備

1. 左上隅で、 **[!UICONTROL Store View]** から `Main Website`、または設定が適用される他の Web サイトにドラッグします。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、次の設定を変更します。

1. 次を変更： **[!UICONTROL Condition]** 必要に応じて。

1. クリック **[!UICONTROL Export CSV]**.

   ![CSV を書き出し](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. を保存します。 `tablerates.csv` ファイルをシステムに保存します。

1. スプレッドシートアプリケーションでファイルを開きます。

1. 配送先の計算条件に適した値でテーブルを完成させます。

   - 任意のカテゴリで使用可能なすべての値を表すワイルドカードとしてアスタリスク (*) を使用します。
   - The _[!UICONTROL Country]_列には次を含める必要があります： [有効な 3 文字コード][1] 各行に対して
   - データの並べ替え基準 _[!UICONTROL Region/State]_したがって、特定の場所はリストの上部に、ワイルドカードの場所は下部に表示されます。 この方法を使用すると、絶対値が先に、ワイルドカード値が後に設定されたルールが処理されます。
   - 値 _[!UICONTROL Weight (and above)]_列には、小数点以下 4 桁まで ( `2.5075`) をクリックします。 データで小数点以下の桁数を増やすと、インポートが失敗します。

   ![重み付けと宛先（オーストラリア）](./assets/table-rates-weight-destination-csv.png){width="500"}

1. を保存します。 `tablerates.csv` ファイル。

## 手順 3：テーブルレートデータのインポート

1. に戻ります。 **[!UICONTROL Table Rates]** ストア設定のセクションに含める必要があります。

1. 左上隅で、 **[!UICONTROL Store View]** を、このメソッドが使用される web サイトに追加します。

1. の場合 **[!UICONTROL Import]**&#x200B;をクリックし、 **[!UICONTROL Choose File]** 完了したを選択します。 `tablerates.csv` ファイルを使用してレートをインポートします。

   ![テーブルレートのインポート](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

## 手順 4：レートの確認

表レートのデータが正しいことを確認するには、複数の異なる住所を持つ支払いプロセスを実行し、送料と処理料が正しく計算されていることを確認します。

### 例 1：価格と宛先

この例では、Price v. Destination 条件を使用して、米国大陸、アラスカおよびハワイ州の注文小計に基づいて、3 種類の異なる送料のセットを作成します。 アスタリスク (*) は、すべての値を表すワイルドカードです。

| 国 | 地域/州（米国） | 郵便番号 | 注文の小計（およびそれ以降） | 送料 |
|--- |--- |--- |--- |--- |
| USA | HI | * | 100 | 10 |
| USA | HI | * | 50 | 15 |
| USA | HI | * | 0 | 20 |
| USA | AK | * | 100 | 10 |
| USA | AK | * | 50 | 15 |
| USA | AK | * | 0 | 20 |
| USA | * | * | 100 | 5 |
| USA | * | * | 50 | 10 |
| USA | * | * | 0 | 15 |

{style="table-layout:auto"}

### 例 2：重み付けと宛先

この例では、「重み付け v.宛先」条件を使用して、注文の重み付けに基づいて異なる送料を作成します。

| 国 | 地域/州（米国） | 郵便番号 | 重み付け（およびそれ以降） | 送料 |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### 例 3：送料無料を米国大陸に制限する

1. の作成 `tablerates.csv` 送料無料を提供するすべての都道府県の宛先を含むファイル。

1. 次の設定を使用して、テーブルレート設定を完了します。

   | 設定 | 値 |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. 左上隅で、 **[!UICONTROL Store View]** から `Main Website`、または設定が適用される他の Web サイトにドラッグします。

1. の場合 **[!UICONTROL Import]**&#x200B;をクリックし、 **[!UICONTROL Choose File]** 完了したを選択します。 `tablerates.csv` ファイルを使用してレートをインポートします。


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
