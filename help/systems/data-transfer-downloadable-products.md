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

ダウンロード可能な製品の読み込みのフローは、と同じです [バンドル製品](data-transfer-bundle-products.md) または [設定可能な製品](data-transfer-configurable-products.md). 違いは、ダウンロード可能な製品には次のものがあります [ダウンロード可能なリンク](../catalog/product-create-downloadable.md) および [ダウンロード可能なサンプル](../catalog/product-create-downloadable.md) 画像を使用して。

ダウンロード可能なリンクおよびサンプルのデフォルトのルートディレクトリは、です。 `<Magento-root-folder>/pub/media/import`. リモートストレージモジュールが有効な場合、ダウンロード可能なリンクおよびサンプルのデフォルトのルートディレクトリはです `<remote-storage-root-folder>/media/import` ディレクトリ。

CSV ファイルには、用の個別の列があります `downloadable_links` および `downloadable_samples`.

- **ダウンロード可能なリンク画像**  – 次の例では、ダウンロード可能なリンク イメージ （`red.jpg` および `black.jpg`）は `<Magento-root-folder>/pub/media/import/test` フォルダー。 リモート記憶域が有効になっている場合、これらのイメージは `<remote-storage-root-folder>/media/import/test` フォルダー。

  ![サンプルデータ – ダウンロード可能なリンクを含むダウンロード可能な製品](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **ダウンロード可能なサンプル画像**  – 次の例では、ダウンロード可能なサンプル イメージ （`white.jpg`）が含まれる `<Magento-root-folder>/pub/media/import/test` フォルダー。 リモート記憶域が有効な場合、このイメージは `<remote-storage-root-folder>/media/import/test` フォルダー。

  ![サンプルデータ – ダウンロード可能なサンプルを含むダウンロード可能な製品](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

リモート ストレージ モジュールの有効化と管理の詳細については、を参照してください。 [リモートストレージの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) が含まれる _設定ガイド_.
