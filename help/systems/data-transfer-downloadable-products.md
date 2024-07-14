---
title: ダウンロード可能な製品のインポート
description: ダウンロード可能な製品の製品データのインポート例を確認します。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# ダウンロード可能な製品のインポート

ダウンロード可能な製品の読み込みのフローは、[ バンドル製品 ](data-transfer-bundle-products.md) または [ 設定可能な製品 ](data-transfer-configurable-products.md) の場合と同じです。 違いは、ダウンロード可能な製品には、画像と共に [ ダウンロード可能なリンク ](../catalog/product-create-downloadable.md) と [ ダウンロード可能なサンプル ](../catalog/product-create-downloadable.md) があることです。

ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは `<Magento-root-folder>/pub/media/import` です。 リモートストレージモジュールが有効な場合、ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは `<remote-storage-root-folder>/media/import` ディレクトリです。

CSV ファイルには、`downloadable_links` と `downloadable_samples` に別々の列があります。

- **ダウンロード可能なリンク画像** – 次の例では、ダウンロード可能なリンク画像（`red.jpg` および `black.jpg`）は `<Magento-root-folder>/pub/media/import/test` フォルダーにあります。 リモート記憶域が有効な場合、これらのイメージは `<remote-storage-root-folder>/media/import/test` フォルダーにあります。

  ![ サンプルデータ – ダウンロード可能な製品とダウンロード可能なリンク ](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **ダウンロード可能なサンプル画像** – 次の例では、ダウンロード可能なサンプル画像（`white.jpg`）は `<Magento-root-folder>/pub/media/import/test` フォルダーにあります。 リモート記憶域が有効な場合、このイメージは `<remote-storage-root-folder>/media/import/test` フォルダーにあります。

  ![ サンプルデータ – ダウンロード可能なサンプルを含むダウンロード可能な製品 ](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

リモート記憶域モジュールの有効化と管理の詳細については、[ 構成ガイド ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) の _リモート記憶域の構成_ を参照してください。
