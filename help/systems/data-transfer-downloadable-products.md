---
title: ダウンロード可能な製品のインポート
description: ダウンロード可能な製品の製品データをインポートする例を確認します。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# ダウンロード可能な製品のインポート

ダウンロード可能な製品を読み込むフローは、[ バンドル製品](data-transfer-bundle-products.md)または[構成可能な製品](data-transfer-configurable-products.md)と同じです。 違いは、ダウンロード可能な製品には、[ ダウンロード可能なリンク ](../catalog/product-create-downloadable.md)と[ ダウンロード可能なサンプル ](../catalog/product-create-downloadable.md)とその画像が含まれていることです。

ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは`<Magento-root-folder>/pub/media/import`です。 リモートストレージモジュールが有効になっている場合、ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは`<remote-storage-root-folder>/media/import` ディレクトリです。

CSV ファイルには、`downloadable_links`と`downloadable_samples`の別々の列があります。

- **ダウンロード可能なリンク画像** – 次の例では、ダウンロード可能なリンク画像（`red.jpg`および`black.jpg`）が`<Magento-root-folder>/pub/media/import/test` フォルダーにあります。 リモートストレージが有効になっている場合、これらの画像は`<remote-storage-root-folder>/media/import/test` フォルダーにあります。

  ![ データ例 – ダウンロード可能なリンクを含むダウンロード可能な製品](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **ダウンロード可能なサンプル画像** – 次の例では、ダウンロード可能なサンプル画像（`white.jpg`）が`<Magento-root-folder>/pub/media/import/test` フォルダーにあります。 リモートストレージが有効になっている場合、この画像は`<remote-storage-root-folder>/media/import/test` フォルダーにあります。

  ![ サンプル データ – ダウンロード可能なサンプルを含むダウンロード可能な製品](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

リモートストレージモジュールの有効化と管理について詳しくは、_設定ガイド_&#x200B;の[ リモートストレージの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html)を参照してください。
