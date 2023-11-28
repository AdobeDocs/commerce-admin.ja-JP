---
title: データ転送
description: データの検証を含む、データ転送のサポートについて説明します。
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: 62978d10bc1b53d3a7983b0a37ccd64e6ab0f740
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# データ転送

1 回の操作で複数のレコードを管理するには、インポートおよびエクスポートツールを使用します。 新しい品目をインポートしたり、既存の製品セットを更新、置換、削除したりできます。

例えば、在庫に新しい製品を追加し、製品データと高度な価格データを更新し、既存の製品のセットを新しい製品で置き換えることができます。 読み込みおよび書き出しツールを使用すると、データを書き出し、スプレッドシートで編集し、管理で複数の操作を実行する代わりにストアに読み込み戻すことができるので、大きな商品カタログの管理をより効率的におこなえます。

Adobe Commerceには、読み込みおよび書き出しツールに加えて、次のような処理があります。 [カタログ同期](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) Commerce サーバーから SaaS サービスに製品データを書き出す 次のような機能の場合 [製品Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html)を使用して、この同期を実行すると、正しい名前、価格、可用性を持つレコメンデーションを正確に返すことができます。

## データの検証

値をストアにインポートする前に、すべてのデータが検証に合格して、値の品質、精度、整合性を確認する必要があります。 クリック時に検証が開始されます **[!UICONTROL Check Data]**. 処理中に、インポートファイル内のすべてのエンティティが以下の点を検証します。

- **属性**  — 列ヘッダー名は、システム・データベース内の対応する属性と一致することを確認します。 各属性の値が、データ型 (decimal、integer、varchar、text、datetime) の要件を満たしているかどうかがチェックされます。
- **複雑なデータ**  — ドロップダウンや複数の選択入力タイプなど、定義済みのセットから派生する値は、定義済みのセットに値が存在することを確認します。
- **サービスデータ**  — サービスデータ列の値は、プロパティまたは複雑なデータ値が、システムデータベースで既に定義されている値と一致することを検証します。
- **必須の値**  — 新しいエンティティの場合は、ファイル内に必要な属性値が存在するかどうかがチェックされます。 既存のエンティティの場合、必要な属性値の存在を再確認する必要はありません。
- **区切り文字**  — スプレッドシートで表示した場合、区切り文字は表示されませんが、CSV ファイル内のデータ値はコンマで区切られ、テキスト値は二重引用符で囲まれます。 検証プロセス中に、区切り文字の書式と、文字列を囲む引用符の各セットが検証されます。

検証の結果は「検証結果」セクションに表示され、次の情報が含まれます。

- チェックされたエンティティの数
- 無効な行の数
- 見つかったエラーの数

データが有効な場合、 _インポート成功_ メッセージが表示されます。

![システムメッセージ — ファイルが有効です](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

検証に失敗した場合は、各エラーの説明を読み、CSV ファイルの問題を修正します。 例えば、行に無効な SKU が含まれている場合、インポートプロセスは停止し、その行とそれ以降の行はすべてインポートされません。 問題が正しく発生したら、データを再度インポートします。 多数のエラーが発生した場合は、検証に合格するまでに何度かの試みが必要になる場合があります。

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
