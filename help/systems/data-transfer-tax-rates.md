---
title: 税率データの更新
description: 書き出し操作と読み込み操作を使用して、ストアの税率を更新する方法を説明します。
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# 税率データの更新

複数の州でビジネスを行い、大量の製品を出荷する場合、手動で税率を入力すると非常に時間がかかる場合があります。 税率を郵便番号でダウンロードしてCommerceに読み込む方が、より速くて効率的です。 次の例は、信頼できるソースからダウンロードした州固有の税率のセットをインポートする方法を示しています。 Avalara は、米国のすべての郵便番号に対して無料でダウンロードできる [&#x200B; 税率表 &#x200B;](https://www.avalara.com/taxrates/en/download-tax-tables.html) を提供しています。

>[!NOTE]
>
>売上の自動化、税務コンプライアンスおよびレポートの使用に関心がある場合は、[Commerce パートナー &#x200B;](https://solutionpartners.adobe.com/s/directory/?solution=commerce) サイトでCommerceの信頼できるオプションを検索できます。

## 手順 1:Commerceの税率データのエクスポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Import/Export Tax Rates]**&#x200B;に移動します。

1. 「**[!UICONTROL Export Tax Rates]**」をクリックします。

1. Web ブラウザーのダウンロード場所でファイルを探します。

1. ファイルをスプレッドシートに保存して開きます。

   この例では、[!DNL OpenOffice Calc] を使用します。

   書き出されるCommerceの税率データには、次の列が含まれます。
   - コード
   - 国
   - 都道府県
   - 郵便番号/Postコード
   - 評価
   - 範囲
   - 範囲から
   - 各ストア表示の列

   ![&#x200B; 書き出されたデータ – 税率 &#x200B;](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. 新しい税率データをスプレッドシートの 2 番目のインスタンスで開くと、横に並べて表示できます。

1. 新しい税率データでは、データをインポートする前にストアで設定する必要がある追加の税率データをメモしておきます。

   例えば、カリフォルニア州の税率データには次も含まれます。

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   追加の [&#x200B; 税ゾーンと税率 &#x200B;](../stores-purchase/tax-zones-rates.md) をインポートする必要がある場合は、まずストアの管理者から定義し、必要に応じて [&#x200B; 税規則 &#x200B;](../stores-purchase/tax-rules.md) を更新する必要があります。 次に、データを書き出し、ファイルをテキストエディターで開いて、参照に使用できるようにします。 ただし、この例では単純にするために、標準の税率列のみをインポートします。

## 手順 2：インポートデータの準備

2 つのスプレッドシートを左右に並べて開いています。 1 つにはCommerce書き出しファイル構造が含まれ、もう 1 つには読み込む新しい税率データが含まれます。

1. 新しい税率データを使用してスプレッドシートで作業する場所を作成するには、必要な数の空白の列を右端に挿入して、Commerce書き出しファイルからデータを追加します。 カット&amp;ペーストを使用してデータを追加し、Commerce書き出しデータファイルの順序と一致するように列を並べ替えます。

1. Commerceの書き出しデータに一致するように、列ヘッダーの名前を変更します。

1. データのない列を削除します。

   そうでない場合、インポートファイルの構造が元のCommerce エクスポートデータと一致する必要があります。

1. ファイルを保存する前に、下にスクロールして、税率列に数値データのみが含まれていることを確認します。

   税率列にテキストが見つかると、データはインポートされません。

1. 準備したデータを.CSV ファイルとして保存します。

   プロンプトが表示されたら、コンマがフィールド区切り文字として使用され、二重引用符がテキスト区切り文字として使用されていることを確認します。 次に、「**[!UICONTROL OK]**」をクリックします。

## 手順 3：税率のインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Import/Export Tax Rates]**&#x200B;に移動します。

1. 「**[!UICONTROL Choose File]**」をクリックし、インポート用に準備した CSV 税率ファイルを選択します。

1. 「**[!UICONTROL Import Tax Rates]**」をクリックします。

   データの読み込みに数分かかる場合があります。 処理が完了すると、`The tax rate has been imported` のメッセージが表示されます。 エラーメッセージが表示された場合は、データの問題を修正して、もう一度試してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Zones and Rates]**&#x200B;に移動します。

   読み込まれたレートがリストに表示されます。

1. 新しい税率を表示するには、ページ管理を使用します。

   ![&#x200B; データ輸入税率 &#x200B;](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. 異なる郵便番号の顧客とストアで一部のテストトランザクションを実行して、新しい税率が正しく機能することを確認します。
