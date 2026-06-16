---
title: 税率データの更新
description: ストアの税率を更新するためにエクスポートおよびインポート操作を使用する方法を説明します。
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
TQID: https://experienceleague.adobe.com/QPY-XfiA3XhBSV3eiiYtxb9K-quf5AycMcHDBUBtE0k
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 624
ht-degree: 0%

---

# 税率データの更新

複数の州で事業を行い、大量の商品を出荷する場合、手動で税率を入力するのは非常に時間がかかります。 郵便番号で税率をダウンロードし、Commerceに読み込むほうが、より迅速かつ効率的です。 次の例は、信頼できるソースからダウンロードした州ごとの税率のセットを読み込む方法を示しています。 Avalaraは[税率表](https://www.avalara.com/taxrates/en/download-tax-tables.html)を提供しており、米国の郵便番号ごとに無料でダウンロードできます。

>[!NOTE]
>
>売上の自動化に関心があり、税務コンプライアンスとレポートを使用する場合は、[Commerce Partners](https://solutionpartners.adobe.com/s/directory/?solution=commerce) サイトでCommerceの信頼できるオプションを見つけることができます。

## 手順1:Commerceの税率データのエクスポート

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**&#x200B;に移動します。

1. **[!UICONTROL Export Tax Rates]**&#x200B;をクリックします。

1. Web ブラウザーのダウンロード場所でファイルを探します。

1. スプレッドシートにファイルを保存して開きます。

   この例では、[!DNL OpenOffice Calc]を使用しています。

   書き出されたCommerceの税率データには、次の列が含まれます。
   - コード
   - 国
   - 都道府県
   - 郵便番号
   - レート
   - 範囲
   - 範囲
   - 各ストアビューの列

   ![書き出されたデータ – 税率](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. スプレッドシートの2番目のインスタンスで新しい税率データを開くと、それらを並べて表示できます。

1. 新しい税率データでは、データを読み込む前にストアで設定する必要がある追加の税率データを書き留めます。

   例えば、カリフォルニア州の税率データには、次の項目も含まれます。

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   追加の[税域と税率](../stores-purchase/tax-zones-rates.md)を読み込む必要がある場合は、まずストアの管理者から税域を定義し、必要に応じて[税規則](../stores-purchase/tax-rules.md)を更新する必要があります。 次に、データを書き出し、テキストエディターでファイルを開いて、参照に使用できるようにします。 ただし、この例を簡単にするために、標準税率の列のみを読み込みます。

## 手順2：読み込みデータの準備

2つのスプレッドシートを並べて開きます。 1つはCommerceの書き出しファイル構造を含み、もう1つは読み込む新しい税率データを含みます。

1. 新しい税率データを使用してスプレッドシートで作業する場所を作成するには、Commerceの書き出しファイルからデータを追加するために、必要に応じて右端に空白の列をいくつでも挿入します。 カットアンドペーストを使用してデータを追加し、Commerce書き出しデータファイルの順序に合わせて列を並べ替えます。

1. Commerceの書き出しデータに一致するように、列ヘッダーの名前を変更します。

1. データを持たない列をすべて削除します。

   そうでない場合、読み込みファイルの構造は、元のCommerce書き出しデータと一致する必要があります。

1. ファイルを保存する前に、下にスクロールして、税率の列に数値データのみが含まれていることを確認します。

   税率の列にテキストが見つかると、データが読み込まれなくなります。

1. 準備したデータを.CSV ファイルとして保存します。

   プロンプトが表示されたら、コンマがフィールド区切り文字として使用され、二重引用符がテキスト区切り文字として使用されていることを確認します。 次に、**[!UICONTROL OK]**&#x200B;をクリックします。

## 手順3：税率のインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**&#x200B;に移動します。

1. 「**[!UICONTROL Choose File]**」をクリックし、読み込むCSV税率ファイルを選択します。

1. **[!UICONTROL Import Tax Rates]**&#x200B;をクリックします。

   データの読み込みに数分かかる場合があります。 プロセスが完了すると、`The tax rate has been imported` メッセージが表示されます。 エラーメッセージが表示された場合は、データの問題を修正して、もう一度試してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**&#x200B;に移動します。

   読み込まれたレートがリストに表示されます。

1. ページ管理を使用して、新しい税率を表示します。

   ![&#x200B; データ読み込み税率](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. ストアで複数の郵便番号を持つ顧客を使用してテスト取引を実行し、新しい税率が正しく機能することを確認します。
