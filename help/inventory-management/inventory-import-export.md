---
title: 在庫のインポートとエクスポート
description: 拡張されたネイティブのインポートおよびエクスポート機能を使用 [!DNL Inventory Management] オプションを使用して、SKU ごとにソースと数量を更新できます。
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 在庫のインポートとエクスポート

多くの製品を含むカタログの場合は、拡張されたネイティブの読み込みおよび書き出し機能を使用します。 [!DNL Inventory Management] オプションを使用して、SKU ごとにソースと数量を更新できます。 これらのオプションを使用すると、すべてのまたは特定のソースの新しいソースを追加し、在庫数量を更新できます。 例えば、フランス、イギリス、米国のソースの製品情報に影響を与えることなく、ソースの製品をドイツで書き出すことができます。

- [!DNL Commerce] アップグレード時に、デフォルトのソースを製品に自動的に割り当てます [!DNL Commerce] または新しい製品を読み込む。 カスタムソースが割り当てられた製品をインポートする場合、「デフォルトのソース」に数量 0 の値が追加されます。 ソースと数量を更新するには、これらのインポート手順を使用します。

- 単一ソースの商人は、製品の数量のみを更新するためにインポートを使用します。 既存の製品と追加された製品はすべて、デフォルトのソースに割り当てられます。

- 複数ソースの商人が import を使用して、SKU ごとに 1 行に複数のソースと数量を追加します。

更新をインポートするには、まず特定のソースまたはすべてのソースの CSV ファイルを書き出します。 CSV ファイルを編集し、ソースと数量ごとに SKU ごとに行を追加します。 ソースを追加し、在庫を数量を追加する場合は、ソースのコードが必要です。 インポート/エクスポート機能を使用して在庫を追加または更新することはできません。

## CSV ファイルコンテンツ

書き出し/読み込みファイルには、ソースに応じて次の情報が含まれます。

- `source_code`  — 内のソースのコード [!DNL Commerce]. ソースと SKU ごとに行が表示されます。
- `sku`  — の製品の SKU [!DNL Commerce]. SKU がストア内の製品と一致している場合、正しく更新されます [!DNL Inventory Management] データ。
- `status` - 0（在庫切れの場合） 1 は在庫中です。 このソースから在庫を購入するには、この値を 1 にする必要があります。
- `quantity`  — この SKU およびソースで使用可能な在庫の合計金額。

CSV ファイルを使用すると、複数の製品と割り当てられたソースをすばやく更新し、アプリケーションインターフェイスを通じて一度に 1 つではなく、在庫レコード内の不正確なデータを更新および修正できます。 ベースファイルの場合は、最初に書き出し、必要に応じて更新します。

![インポート用の CSV ファイルの例 — 在庫データのエクスポート](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## すべてのソースの製品データを書き出し

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. の場合 **[!UICONTROL Entity Type]**&#x200B;を選択します。 `Stock Sources`.

   書き出しは、SKU を持つ製品のデータのみを抽出します。

1. クリック **[!UICONTROL Continue]**.

   ファイルが生成され、開いて編集するためのダウンロードが行われます。

在庫金額と製品データを更新した後、ファイルをにインポートし直します。 [!DNL Commerce].

![製品のデータとソースの在庫ソースのエクスポート](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## 特定のソースの製品データを書き出す

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. の場合 **[!UICONTROL Entity Type]**&#x200B;を選択します。 `Stock Sources`.

   書き出しは、SKU を持つ製品のデータのみを抽出します。

1. 以下を使用します。 **[!UICONTROL Entity Attributes]** をクリックして、特定のソースに対してエクスポートした製品をフィルタリングします。

   の場合 `source_code`で、ソースのコードをフィルターフィールドに入力します。

1. クリック **[!UICONTROL Continue]**.

   ファイルが生成され、開いて編集するためのダウンロードが行われます。

在庫金額と製品データを更新した後、ファイルをにインポートし直します。 [!DNL Commerce].

## 製品データを読み込む

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. の場合 **[!UICONTROL Entity Type]**&#x200B;を選択します。 `Stock Sources`.

   書き出しは、SKU を持つ製品のデータのみを抽出します。

1. の設定を選択 **[!UICONTROL Import Behavior]**.

1. インポートする.csv ファイルを選択します。

1. クリック **[!UICONTROL Check Data]** 読み込みを完了します。

![製品のデータとソースのインポート](assets/inventory-import-sources.png){width="600" zoomable="yes"}
