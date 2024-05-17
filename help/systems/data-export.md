---
title: データを書き出し
description: データ書き出しフィルターと属性、およびストアからデータを書き出す方法について説明します。
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# データを書き出し

データベースの構造を理解するには、データを書き出してスプレッドシートで開くことが最適な方法です。 このプロセスに慣れたら、大量の情報を効率的に管理する方法として使用できます。

特殊文字（等号、記号より大きいまたは小さい、一重引用符と二重引用符、バックスラッシュ、パイプ、アンパサンド記号など）は、データ転送中に問題を引き起こす可能性があります。 このような特殊文字を正しく解釈するには、 _エスケープシーケンス_. 例えば、データに次のようなテキスト文字列が含まれている場合 `code="str"`, `code="str2"`テキストを二重引用符で囲むと、元の二重引用符がデータの一部と理解されます。 `"code="str""`. システムが二重引用符の二重セットに遭遇すると、外側の二重引用符セットが実際のデータを囲んでいることを認識します。

データの書き出しは、非同期の操作で、バックグラウンドで実行されるので、操作が完了するのを待たずに管理で作業を続行できます。 タスクが完了すると、メッセージが表示されます。

## 書き出し条件

書き出しフィルターは、属性値に基づいて、書き出しファイルに含めるデータを指定するために使用します。 さらに、書き出しに含める、または書き出しから除外する属性データを指定できます。

![データの書き出し条件](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### フィルターを書き出し

フィルターを使用して、書き出しファイルに含める SKU を指定できます。 例えば、「製造国」フィルターに値を入力した場合、書き出された CSV ファイルには、その国で製造された製品のみが含まれます。

フィルターのタイプは、データタイプに対応します。 日付フィールドには、カレンダーから日付を選択できます ![カレンダーアイコン](../assets/icon-calendar.png). 参照： [属性入力タイプ](../catalog/attributes-input-types.md) を参照してください。

日付の形式は、 [locale](../getting-started/store-details.md#locale-options).

SKU など特定の値を持つレコードのみを含めるには、その値を「フィルター」フィールドに入力します。 一部のフィールド（「価格」、「重量」、「新製品として製品を設定」など）には、開始値/終了値の範囲があります。

### 属性を除外

最初の列のチェックボックスは、エクスポートファイルから属性を除外するために使用します。 属性が除外されている場合は、エクスポートデータ内の関連する列は含まれますが、空になります。

| 除外 | フィルター | 結果 |
|--- |--- |--- |
| ![チェックボックスをオフ](../assets/checkbox-clear.png) | 不可 | 書き出されるファイルには、既存のすべてのレコードの各属性が含まれます。 |
| ![チェックボックスをオフ](../assets/checkbox-clear.png) | はい | エクスポートファイルには、フィルターで許可されたレコードのみを含んだ各属性が含まれています。 |
| ![選択済みチェックボックス](../assets/checkbox-selected.png) | 不可 | エクスポートファイルには、除外属性の列は含まれず、既存のすべてのレコードが含まれます。 |
| ![選択済みチェックボックス](../assets/checkbox-selected.png) | はい | エクスポートファイルには、除外属性の列は含まれておらず、フィルターで許可されたレコードのみが含まれています。 |

{style="table-layout:auto"}

## データを書き出し

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. が含まれる _書き出し設定_ セクション、設定 **[!UICONTROL Entity Type]** を次のいずれかに変更します。

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![データの書き出し設定](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. デフォルトを使用 **[!UICONTROL Export File Format]** （CSV 形式）。

1. データに含まれる可能性のある特殊文字を _エスケープシーケンス_&#x200B;を選択し、 **[!UICONTROL Fields Enclosure]** チェックボックス。

1. 必要に応じて、エンティティ属性の表示を変更します。

   デフォルトでは、「エンティティ属性」セクションには、使用可能なすべての属性がアルファベット順に表示されます。 標準を使用できます [リスト制御](../getting-started/admin-grid-controls.md) 特定の属性を検索したり、リストを並べ替えたりします。 [ 検索 ] および [ フィルタのリセット ] コントロールは、リストの表示をコントロールしますが、書き出しファイルに含める属性の選択には影響しません。

   ![フィルターされたエンティティ属性のデータ エクスポート](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. 属性値に基づいて書き出したデータをフィルタリングするには、次の手順を実行します。

   - 特定の属性値を持つレコードのみをエクスポートするには、必要な値を **[!UICONTROL Filter]** 列。 次の例では、特定の SKU のみを書き出しています。

   - 書き出しから属性を省略するには、 **[!UICONTROL Exclude]** 行の先頭にあるチェックボックス。 例えば、を書き出すためにのみ `sku` および `image` 列を選択し、1 つおきの属性のチェックボックスを選択します。 列はエクスポートファイルに表示されますが、値は表示されません。

1. 下にスクロールして、 **[!UICONTROL Continue]** ページの右下隅

   タスクが完了すると、ファイルはメッセージキューを介して処理されます（cron ジョブが実行中であることを確認してください）。 書き出されたファイルは `var/export/ folder`. メッセージ キューの詳細については、を参照してください。 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) が含まれる _設定ガイド_.

   書き出された CSV ファイルをスプレッドシートとして保存または開き、データを編集してストアに読み込むことができます。

   >[!NOTE]
   >
   >デフォルトでは、書き出されるすべてのファイルは `<Magento-root-directory>/var/export` フォルダー。 リモートストレージモジュールが有効な場合、書き出されたすべてのファイルは `<remote-storage-root-directory>/import_export/export` フォルダー。

## リソースのトラブルシューティング

データの書き出しに関する問題のトラブルシューティングについて詳しくは、Commerce サポートナレッジベースの次の記事を参照してください。

- [書き出された製品の.csv ファイルが表示されない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [製品の書き出しファイルが管理者に表示されない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [注文を CSV 形式で書き出す際の問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
