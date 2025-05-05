---
title: データ転送
description: データ検証を含む、データ転送のサポートについて説明します。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# データ転送

読み込みツールと書き出しツールを使用すると、複数のレコードを 1 回の操作で管理できます。 新しい項目を読み込んだり、既存の製品セットを更新、置換、削除したりできます。

例えば、在庫に新しい製品を追加したり、製品データや詳細な価格データを更新したり、既存の製品セットを新しい製品に置き換えたりできます。 読み込みツールおよび書き出しツールを使用すると、データを書き出し、スプレッドシートで編集し、管理画面で複数の操作を行う代わりにストアに読み込むことができるため、大きな製品カタログをより効率的に管理できます。


>[!NOTE]
>
>Adobe Commerceは、Commerce サーバーから SaaS サービスに商品データを転送するための SaaS データの書き出しもサポートしています。 SaaS データの書き出しは、[Product Recommendations](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=ja)、[Live Search](https://experienceleague.adobe.com/ja/docs/commerce/live-search/overview)、[ カタログサービス ](https://experienceleague.adobe.com/ja/docs/commerce/catalog-service/guide-overview) などのCommerce SaaS サービスと統合されています。 詳細については、「[SaaS データ書き出しガイド ](https://experienceleague.adobe.com/ja/docs/commerce/saas-data-export/overview)」を参照してください。

## データの検証

すべてのデータは、ストアに読み込む前に、値の品質、精度、整合性を確保するための検証に合格する必要があります。 [**[!UICONTROL Check Data]**] をクリックすると、検証が開始されます。 このプロセスでは、インポートファイル内のすべてのエンティティが以下について検証されます。

- **属性** – 列ヘッダー名がシステムデータベース内の対応する属性に一致することを確認するために検証されます。 各属性の値が、データタイプ（decimal、integer、varchar、text および datetime）の要件を満たしているかどうかを確認します。
- **複合データ** – 定義済みのセット（ドロップダウンや複数の選択入力タイプなど）から取得された値が、定義済みのセットに値が存在することを確認します。
- **サービスデータ** - サービスデータ列の値は、プロパティや複雑なデータ値がシステムデータベースで既に定義されているものと一致することを確認するために検証されます。
- **必要な値** – 新しいエンティティの場合、ファイル内に必要な属性値が存在するかどうかが確認されます。 既存のエンティティの場合、必要な属性値の存在を再確認する必要はありません。
- **区切り記号** - スプレッドシートで表示すると区切り記号は表示されませんが、CSV ファイル内のデータ値はコンマで区切られ、テキスト値は二重引用符で囲まれます。 検証プロセスでは、区切り文字の書式と、文字列を囲む引用符のセットが検証されます。

検証の結果は、「検証結果」セクションに表示され、次の情報が含まれます。

- チェックされたエンティティの数
- 無効な行数
- 見つかったエラーの数

データが有効な場合は、_インポートの成功_ メッセージが表示されます。

![ システムメッセージ – ファイルは有効です ](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

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
