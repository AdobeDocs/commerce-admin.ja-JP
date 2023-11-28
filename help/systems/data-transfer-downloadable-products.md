---
title: ダウンロード可能な製品を読み込む
description: ダウンロード可能な製品の製品データのインポート例を確認します。
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# ダウンロード可能な製品を読み込む

ダウンロード可能な製品を読み込むフローは、 [製品をバンドル](data-transfer-bundle-products.md) または [設定可能な製品](data-transfer-configurable-products.md). 違いは、ダウンロード可能な製品に [ダウンロード可能なリンク](../catalog/product-create-downloadable.md) および [ダウンロード可能なサンプル](../catalog/product-create-downloadable.md) 画像を含んだ

ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは、 `<Magento-root-folder>/pub/media/import`. リモートストレージモジュールが有効な場合、ダウンロード可能なリンクとサンプルのデフォルトのルートディレクトリは、 `<remote-storage-root-folder>/media/import` ディレクトリ。

CSV ファイルには、 `downloadable_links` および `downloadable_samples`.

- **ダウンロード可能なリンク画像**  — 次の例では、ダウンロード可能なリンク画像 (`red.jpg` および `black.jpg`) が `<Magento-root-folder>/pub/media/import/test` フォルダー。 リモートストレージが有効な場合、これらのイメージは `<remote-storage-root-folder>/media/import/test` フォルダー。

  ![サンプルデータ — ダウンロード可能なリンクを含むダウンロード可能な製品](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **ダウンロード可能なサンプル画像**  — 次の例では、ダウンロード可能なサンプルイメージ (`white.jpg`) が `<Magento-root-folder>/pub/media/import/test` フォルダー。 リモートストレージが有効な場合、このイメージは `<remote-storage-root-folder>/media/import/test` フォルダー。

  ![サンプルデータ — ダウンロード可能なサンプルを含むダウンロード可能な製品](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

リモートストレージモジュールの有効化と管理の詳細については、 [リモートストレージの構成](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) （内） _設定ガイド_.
