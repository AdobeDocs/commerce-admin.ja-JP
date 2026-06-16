---
title: 在庫のインポートとエクスポート
description: 拡張 [!DNL Inventory Management]  オプションを使用したネイティブのインポートおよびエクスポート機能を使用して、SKUごとにソースと数量を更新します。
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
TQID: https://experienceleague.adobe.com/TrH9Ncak4gPMh-4kejFF0NdCIzjT-xT5-M4eETSQ9FM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# 在庫のインポートとエクスポート

多くの製品を含むカタログの場合は、拡張[!DNL Inventory Management] オプションを含むネイティブの読み込み機能と書き出し機能を使用して、SKUごとにソースと数量を更新します。 これらのオプションを使用すると、新しいソースを追加し、すべてのソースまたは特定のソースの在庫量を更新できます。 例えば、フランス、イギリス、または米国のソースの製品情報に影響を与えることなく、ドイツのソースの製品を書き出すことができます。

- [!DNL Commerce]は、[!DNL Commerce]のアップグレードまたは新しい製品の読み込み時に、Default Sourceを自動的に製品に割り当てます。 カスタムソースが割り当てられている商品を読み込む場合、デフォルトのSourceは引き続き数量0で追加されます。 ソースと数量を更新するには、次のインポート手順を使用します。

- シングルソースのマーチャントは、商品の数量のみを更新するために「インポート」を使用します。 既存および追加されたすべての商品は、デフォルトのSourceに割り当てられます。

- マルチソースのマーチャントは、SKUごとに、行ごとに複数のソースと数量を追加するために「インポート」を使用します。

更新を読み込むには、まず、特定のソースまたはすべてのソースのCSV ファイルを書き出します。 CSV ファイルを編集し、ソースと数量ごとにSKUごとに行を追加します。 ソースを追加して在庫の量を追加するときは、ソースのコードが必要です。 読み込み/書き出し機能を使用してストックを追加または更新することはできません。

## CSV ファイルコンテンツ

export-import ファイルには、ソースに応じて次の情報が含まれます。

- `source_code` - [!DNL Commerce]のソースのコード。 各ソースとSKUに行があります。
- `sku` - [!DNL Commerce]の製品のSKU。 [!DNL Inventory Management] データを適切に更新するには、SKUがストア内の商品と一致する必要があります。
- 在庫切れのための`status` - 0。 1、在庫について。 このソースから在庫を購入するには、この値が1である必要があります。
- `quantity` – このSKUとソースで使用可能なインベントリの合計金額。

アプリケーションインターフェイスを通じて、CSV ファイルを使用して複数の製品と割り当てられたソースをすばやく更新し、在庫記録の不正確さを一度にではなく更新して修正します。 基本ファイルの場合は、最初に書き出して、必要に応じて更新します。

![&#x200B; インポート用のCSV ファイルの例 – インベントリ データのエクスポート &#x200B;](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## すべてのソースの製品データの書き出し

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;に移動します。

1. **[!UICONTROL Entity Type]**&#x200B;に対して、`Stock Sources`を選択します。

   書き出しは、SKUを持つ製品のデータのみを抽出します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

   ファイルが生成され、開いたり編集したりするためにダウンロードされます。

在庫量と商品データを更新した後、ファイルを[!DNL Commerce]に読み込みます。

![商品データとソースのストックソースの書き出し](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## 特定のソースの製品データの書き出し

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**&#x200B;に移動します。

1. **[!UICONTROL Entity Type]**&#x200B;に対して、`Stock Sources`を選択します。

   書き出しは、SKUを持つ製品のデータのみを抽出します。

1. **[!UICONTROL Entity Attributes]**&#x200B;を使用して、特定のソースに対して書き出された製品をフィルタリングします。

   `source_code`の場合は、ソースのコードをフィルターフィールドに入力します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

   ファイルが生成され、開いたり編集したりするためにダウンロードされます。

在庫量と商品データを更新した後、ファイルを[!DNL Commerce]に読み込みます。

## 製品データのインポート

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**&#x200B;に移動します。

1. **[!UICONTROL Entity Type]**&#x200B;に対して、`Stock Sources`を選択します。

   書き出しは、SKUを持つ製品のデータのみを抽出します。

1. **[!UICONTROL Import Behavior]**&#x200B;の設定を選択します。

1. インポートする.csv ファイルを選択します。

1. **[!UICONTROL Check Data]**&#x200B;をクリックして読み込みを完了します。

![製品データとソースの読み込み](assets/inventory-import-sources.png){width="600" zoomable="yes"}
