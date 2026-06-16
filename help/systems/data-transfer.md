---
title: データ転送
description: データ検証など、データ転送のサポートについて説明します。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
TQID: https://experienceleague.adobe.com/G-hJ2wQlhL95wmuLLYivfW8AGsbfdu5Cn0pOdGdTQto
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# データ転送

読み込みツールと書き出しツールを使用して、1回の操作で複数のレコードを管理します。 新しいアイテムを読み込むだけでなく、既存の製品セットを更新、置換、削除することもできます。

たとえば、在庫に新商品を追加したり、商品データと高度な価格データを更新したり、既存の商品のセットを新商品に置き換えたりすることができます。 読み込みツールと書き出しツールを使用すると、管理画面で複数の操作を実行する代わりに、データを書き出し、スプレッドシートで編集し、ストアに読み込むことができるため、大規模な商品カタログをより効率的に管理できます。


>[!NOTE]
>
>Adobe Commerceでは、SaaS データの書き出しをサポートしており、CommerceサーバーからSaaS サービスに商品データを転送できます。 SaaS データ書き出しは、[商品レコメンデーション &#x200B;](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html)、[&#x200B; ライブサーチ &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)、[&#x200B; カタログサービス &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview)などのCommerce SaaS サービスと統合されています。 詳しくは、[SaaS データ書き出しガイド &#x200B;](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)を参照してください。

## データ検証

すべてのデータは、値をストアに読み込む前に、値の品質、正確性、整合性を確保するために検証に合格する必要があります。 **[!UICONTROL Check Data]**&#x200B;をクリックすると、検証が開始されます。 プロセス中に、インポートファイル内のすべてのエンティティで次の点が確認されます。

- **属性** – 列ヘッダー名が、システムデータベース内の対応する属性と一致することを確認するために検証されます。 各属性の値がチェックされ、データタイプ（小数、整数、varchar、テキスト、日時）の要件を満たしていることを確認します。
- **複雑なデータ** - ドロップダウンや複数のselect入力タイプなど、定義されたセットに由来する値が、定義されたセットに値が存在することを確認するために検証されます。
- **サービスデータ** - サービスデータ列の値が検証され、プロパティまたは複雑なデータ値が、システムデータベースで既に定義されているものと一致していることが確認されます。
- **必要な値** – 新しいエンティティの場合、ファイル内に必要な属性値が存在するかどうかを確認します。 既存のエンティティの場合、必要な属性値の存在を再確認する必要はありません。
- **区切り記号** - スプレッドシートで表示する場合、区切り記号は表示されませんが、CSV ファイルのデータ値はコンマで区切られ、テキスト値は二重引用符で囲まれます。 検証プロセスでは、区切り記号と、文字列を囲む引用符の各セットの書式設定が検証されます。

検証の結果は、「検証結果」セクションに表示され、次の情報が含まれます。

- チェックされたエンティティの数
- 無効な行数
- 見つかったエラーの数

データが有効な場合は、_Import Success_ メッセージが表示されます。

![&#x200B; システムメッセージ – ファイルは有効です](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

検証が失敗した場合は、各エラーの説明を読み、CSV ファイルの問題を修正します。 例えば、行に無効なSKUが含まれている場合、読み込みプロセスは停止し、その行は読み込まれず、以降のすべての行は読み込まれません。 問題を正しく解決したら、データを再度インポートします。 多くのエラーが発生した場合、検証をパスするのに数回の試行が必要になることがあります。

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
