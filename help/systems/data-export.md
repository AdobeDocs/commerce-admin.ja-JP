---
title: データを書き出し
description: データ書き出しフィルターと属性、およびストアからデータを書き出す方法について説明します。
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# データを書き出し

データベースの構造を把握する最善の方法は、データを書き出してスプレッドシートで開くことです。 プロセスに慣れたら、大量の情報を効率的に管理する方法として使用できます。

等号、大なり記号および小なり記号、一重引用符および二重引用符、バックスラッシュ、パイプ、アンパサンド記号などの特殊文字は、データ転送時に問題を引き起こす可能性があります。 このような特殊文字を正しく解釈するために、 _エスケープシーケンス_. 例えば、データに次のような文字列が含まれている場合、 `code="str"`, `code="str2"`を二重引用符で囲むと、元の二重引用符がデータの一部と認識されます。 `"code="str""`. 二重引用符のセットを検出した場合、外側の二重引用符が実際のデータを含んでいることを認識します。

データのエクスポートは非同期操作で、バックグラウンドで実行されるので、操作が完了するのを待たずに管理者で作業を続行できます。 タスクが完了すると、メッセージが表示されます。

## 書き出し条件

書き出しフィルタは、属性値に基づいて、書き出しファイルに含めるデータを指定するために使用します。 さらに、書き出しに含めるまたは除外する属性データを指定できます。

![データエクスポート条件](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### フィルターの書き出し

フィルターを使用して、書き出しファイルに含める SKU を指定できます。 例えば、「製造国」フィルターに値を入力すると、書き出された CSV ファイルには、その国で製造された製品のみが含まれます。

フィルターのタイプは、データタイプに対応します。 日付フィールドの場合、カレンダーから日付を選択できます ![カレンダーアイコン](../assets/icon-calendar.png). 詳しくは、 [属性入力タイプ](../catalog/attributes-input-types.md) を参照してください。

日付の形式は、 [ロケール](../getting-started/store-details.md#locale-options).

SKU など、特定の値を持つレコードのみを含めるには、その値を「フィルター」フィールドに入力します。 「価格」、「重み付け」、「新規として設定」などの一部のフィールドには、開始値/終了値の範囲があります。

### 属性を除外

最初の列のチェックボックスを使用して、エクスポートファイルから属性を除外します。 属性が除外されると、エクスポートデータに関連付けられている列は含まれますが、空になります。

| 除外 | フィルター | 結果 |
|--- |--- |--- |
| ![チェックボックスをオフにする](../assets/checkbox-clear.png) | いいえ | 書き出されたファイルには、既存のすべてのレコードの各属性が含まれます。 |
| ![チェックボックスをオフにする](../assets/checkbox-clear.png) | はい | エクスポートファイルには、フィルターで許可されているレコードのみを含む各属性が含まれています。 |
| ![選択したチェックボックス](../assets/checkbox-selected.png) | いいえ | エクスポートファイルには、除外された属性の列は含まれていませんが、既存のすべてのレコードが含まれています。 |
| ![選択したチェックボックス](../assets/checkbox-selected.png) | はい | エクスポートファイルには、除外された属性の列は含まれず、フィルターで許可されたレコードのみが含まれます。 |

{style="table-layout:auto"}

## データを書き出し

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Adobe Analytics の _書き出し設定_ セクション、設定 **[!UICONTROL Entity Type]** を次のいずれかに変更します。

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![データ書き出し設定](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. デフォルトを受け入れる **[!UICONTROL Export File Format]** を CSV に設定します。

1. データ内の特殊文字を _エスケープシーケンス_&#x200B;を選択し、 **[!UICONTROL Fields Enclosure]** チェックボックス。

1. 必要に応じて、エンティティの属性の表示を変更します。

   デフォルトでは、「エンティティの属性」セクションには、使用可能なすべての属性がアルファベット順に表示されます。 標準 [リストコントロール](../getting-started/admin-grid-controls.md) 特定の属性を検索し、リストを並べ替えるには、をクリックします。 [ 検索とリセットフィルタ ] は、リストの表示を制御しますが、エクスポートファイルに含める属性の選択には影響しません。

   ![データエクスポートフィルター済みエンティティの属性](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. 属性値に基づいて書き出したデータをフィルタリングするには、次の手順を実行します。

   - 特定の属性値を持つレコードのみをエクスポートするには、必要な値を **[!UICONTROL Filter]** 列。 次の例では、特定の SKU のみを書き出します。

   - 書き出しの対象から属性を省略するには、 **[!UICONTROL Exclude]** 」チェックボックスを使用して、データを書き出すことができます。 例えば、 `sku` および `image` 列」で、他のすべての属性のチェックボックスをオンにします。 この列は、値を含まない状態でエクスポートファイルに表示されます。

1. 下にスクロールして、 **[!UICONTROL Continue]** をクリックします。

   タスクが完了すると、ファイルはメッセージキューを通じて処理されます（cron ジョブが実行中であることを確認してください）。 書き出されたファイルは、 `var/export/ folder`. メッセージキューについて詳しくは、 [メッセージキューの管理](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) （内） _設定ガイド_.

   書き出した CSV ファイルをスプレッドシートとして保存または開いた後、データを編集し、ストアに再度読み込むことができます。

   >[!NOTE]
   >
   >デフォルトでは、書き出されるすべてのファイルは、 `<Magento-root-directory>/var/export` フォルダー。 リモートストレージモジュールが有効な場合、書き出されるすべてのファイルは `<remote-storage-root-directory>/import_export/export` フォルダー。

## リソースのトラブルシューティング

データの書き出しに関する問題のトラブルシューティングについては、次のコマースサポートのナレッジベース記事を参照してください。

- [書き出された製品の.csv ファイルが表示されません](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [製品書き出しファイルが管理に表示されない](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [CSV 形式でのオーダーの書き出しに関する問題](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
