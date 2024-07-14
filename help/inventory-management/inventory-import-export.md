---
title: 在庫の読み込みと書き出し
description: 拡張オプションを使用したネイティブのインポート機能およびエクスポ  [!DNL Inventory Management]  ト機能を使用して、SKU 別のソースと数量を更新します。
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# 在庫の読み込みと書き出し

多数の製品を含むカタログの場合、ネイティブのインポート機能およびエクスポート機能を使用し、拡張された [!DNL Inventory Management] オプションを使用して、SKU 別にソースと数量を更新します。 これらのオプションを使用すると、新規ソースを追加し、すべてまたは特定のソースの在庫数量を更新できます。 例えば、フランス、英国または米国のソースの製品情報に影響を与えずに、ドイツのソースの製品を書き出すことができます。

- ア [!DNL Commerce] プグレード時や新しい商品の読み込み時に、デフォルトのSourceが商品 [!DNL Commerce] 自動的に割り当てられます。 カスタムソースが割り当てられている商品を読み込む場合、デフォルトのSourceは数量 0 で追加されます。 ソースと数量を更新するには、次のインポート手順を使用します。

- 単一ソースマーチャントは、読み込みを使用して製品の数量のみを更新します。 既存の商品と追加された商品はすべて、デフォルトのSourceに割り当てられます。

- マルチソースマーチャントは、インポートを使用して、SKU ごとに 1 行に複数のソースと数量を追加します。

更新を読み込むには、まず特定またはすべてのソースの CSV ファイルを書き出します。 CSV ファイルを編集し、ソースと数量ごとに SKU ごとに行を追加します。 ソースを追加して在庫数を追加する場合は、ソースのコードが必要です。 インポート/エクスポート機能を使用して在庫を追加または更新することはできません。

## CSV ファイルコンテンツ

書き出しインポートファイルには、ソースに応じて次の情報が含まれます。

- `source_code` - [!DNL Commerce] のソースのコード。 ソースと SKU ごとに行があります。
- `sku` - [!DNL Commerce] の製品の SKU。 データを正しく更新するには、SKU がストアの製品と一致する必要 [!DNL Inventory Management] あります。
- 在庫切れの場合は `status` ～ 0 を指定します。 在庫がある場合は 1。 このソースから在庫を購入するには、この値を 1 にする必要があります。
- `quantity` – この SKU とソースで使用可能な在庫の合計数。

CSV ファイルを使用して、複数の製品と割り当てられたソースをすばやく更新し、アプリケーションインターフェイスから 1 つずつインベントリ記録に不正確な情報を更新して修正します。 基本ファイルの場合は、最初にエクスポートし、必要に応じて更新します。

![ 読み込み用の CSV ファイルの例 – 在庫データの書き出し ](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## すべてのソースの製品データのエクスポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Export]**に移動します。

1. **[!UICONTROL Entity Type]** の場合は、「`Stock Sources`」を選択します。

   書き出しでは、SKU を持つ製品のデータのみが抽出されます。

1. 「**[!UICONTROL Continue]**」をクリックします。

   ファイルが生成され、開いて編集するためにダウンロードされます。

在庫金額と製品データを更新した後、ファイルを [!DNL Commerce] にインポートします。

![ 製品データおよびソース用のストックソースのエクスポート ](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## 特定のソースの製品データのエクスポート

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Export]**に移動します。

1. **[!UICONTROL Entity Type]** の場合は、「`Stock Sources`」を選択します。

   書き出しでは、SKU を持つ製品のデータのみが抽出されます。

1. **[!UICONTROL Entity Attributes]** を使用して、特定のソースについて書き出された製品をフィルタリングします。

   `source_code`: ソースのコードを「フィルター」フィールドに入力します。

1. 「**[!UICONTROL Continue]**」をクリックします。

   ファイルが生成され、開いて編集するためにダウンロードされます。

在庫金額と製品データを更新した後、ファイルを [!DNL Commerce] にインポートします。

## 製品データの読み込み

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Data Transfer]_/**[!UICONTROL Import]**に移動します。

1. **[!UICONTROL Entity Type]** の場合は、「`Stock Sources`」を選択します。

   書き出しでは、SKU を持つ製品のデータのみが抽出されます。

1. **[!UICONTROL Import Behavior]** の設定を選択します。

1. インポートする.csv ファイルを選択します。

1. 「**[!UICONTROL Check Data]**」をクリックして、読み込みを完了します。

![ 製品データおよびソースのインポート ](assets/inventory-import-sources.png){width="600" zoomable="yes"}
