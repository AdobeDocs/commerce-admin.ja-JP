---
title: データ転送
description: データ検証を含む、データ転送のサポートについて説明します。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: ae3bb3463df13c30ce34739bb6e476d3f7422671
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# データ転送

読み込みツールと書き出しツールを使用すると、複数のレコードを 1 回の操作で管理できます。 新しい項目を読み込んだり、既存の製品セットを更新、置換、削除したりできます。

例えば、在庫に新しい製品を追加したり、製品データや詳細な価格データを更新したり、既存の製品セットを新しい製品に置き換えたりできます。 読み込みツールおよび書き出しツールを使用すると、データを書き出し、スプレッドシートで編集し、管理画面で複数の操作を行う代わりにストアに読み込むことができるため、大きな製品カタログをより効率的に管理できます。

Adobe Commerceには、読み込みツールと書き出しツールに加えて、次のようなプロセスがあります [SaaS データのエクスポート](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) Commerce サーバーから SaaS サービスに商品データを書き出します。 SaaS データの書き出しは、次のようなCommerce SaaS サービスと統合されています [製品のRecommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview), [カタログサービス](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview)、および [SaaS 価格インデックス作成](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/price-indexer/price-indexing).

## データの検証

すべてのデータは、ストアに読み込む前に、値の品質、精度、整合性を確保するための検証に合格する必要があります。 をクリックすると検証が開始されます **[!UICONTROL Check Data]**. このプロセスでは、インポートファイル内のすべてのエンティティが以下について検証されます。

- **属性**  – 列ヘッダー名は、システム データベース内の対応する属性と一致することを確認するために検証されます。 各属性の値が、データタイプ（decimal、integer、varchar、text および datetime）の要件を満たしているかどうかを確認します。
- **複雑なデータ**  – 定義済みのセット（ドロップダウンや複数選択の入力タイプなど）から取得された値が、定義済みのセットに値が存在することを確認するために検証されます。
- **サービスデータ** - サービスデータ列の値は、プロパティや複雑なデータ値がシステムデータベースで既に定義されているものと一致していることを確認するために検証されます。
- **必要な値**  – 新規エンティティの場合、必要な属性値がファイルに存在するかどうかがチェックされます。 既存のエンティティの場合、必要な属性値の存在を再確認する必要はありません。
- **区切り** - スプレッドシートで表示すると区切り記号は表示されませんが、CSV ファイルのデータ値はコンマで区切られ、テキスト値は二重引用符で囲まれます。 検証プロセスでは、区切り文字の書式と、文字列を囲む引用符のセットが検証されます。

検証の結果は、「検証結果」セクションに表示され、次の情報が含まれます。

- チェックされたエンティティの数
- 無効な行数
- 見つかったエラーの数

データが有効な場合、 _インポートの成功_ メッセージが表示されます。

![システム メッセージ – ファイルは有効です](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

検証に失敗した場合は、各エラーの説明を読み、CSV ファイルで問題を修正します。 例えば、行に無効な SKU が含まれている場合、インポートプロセスは停止し、その行はインポートされず、後続のすべての行はインポートされません。 問題が正しく解決されたら、データを再度インポートします。 多くのエラーが発生した場合は、検証に合格するまでに何度か時間がかかることがあります。

### データ検証メッセージ

#### 検証

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### エラー

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
