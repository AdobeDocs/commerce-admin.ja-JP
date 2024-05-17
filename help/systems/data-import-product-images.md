---
title: 商品画像の読み込み
description: 各画像のパスとファイル名を使用して、製品画像を読み込む方法を説明します。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# 商品画像の読み込み

各種類の複数の商品画像をAdobe CommerceとMagento Open Sourceに読み込み、特定の商品に関連付けることができます。 CSV ファイルに各商品画像のパスとファイル名を入力し、インポートする画像ファイルをCommerce サーバーまたは外部サーバーの対応するパスにアップロードします。

Commerceでは、商品画像をアルファベット順に並べた独自のディレクトリ構造が作成されます。 既存の画像を含む製品データを CSV ファイルに書き出すと、各画像のファイル名の前にアルファベット順のパスが表示されます。 ただし、新しい画像を読み込む場合は、パスを指定する必要はありません。Commerceがディレクトリ構造を自動的に管理するからです。 ただし、インポートする各画像のファイル名の前に、インポートディレクトリへの相対パスを必ず入力してください。

画像をアップロードするには、ログイン資格情報と、サーバー上のCommerce フォルダーにアクセスするための適切な権限が必要です。 正しい資格情報があれば、任意の SFTP ユーティリティを使用して、デスクトップコンピューターからサーバーにファイルをアップロードできます。

多数の画像をインポートする前に、使用するインポート方法の手順を確認し、いくつかの製品を使用してプロセスを実行します。 その仕組みを理解したら、大量の画像を確実にインポートできるようになります。

>[!IMPORTANT]
>
>メモ帳++などの CSV ファイルを編集するには、UTF-8 エンコーディングをサポートするプログラムを使用することをお勧めします。 Microsoft® Excel では、CSV ファイルの列見出しに追加の文字が挿入されるので、データがCommerceにインポートされない可能性があります。

## 方法 1：ローカルサーバーからの画像のインポート

1. Commerce サーバーで、画像ファイルをにアップロードします `var/import/images` フォルダーまたはサブフォルダー（例：） `var/import/images/product_images`. これは、商品画像を読み込むためのデフォルトのルートフォルダーです。

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe CommerceとMagento Open Sourceの概要 `2.3.2` release、で指定されたパス **[!UICONTROL Images File Directory]** は画像のベースディレクトリへのインポート用に連結します –  `<Magento-root-folder>/var/import/images`. 以前のAdobe CommerceおよびMagento Open Sourceのリリースでは、読み込み処理中にフォルダーへのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、正しい行に読み込む各画像ファイルの名前を、次のように入力します。 `sku`を選択し、画像タイプに応じて適切な列に表示されます（`base_image`, `small_image`, `thumbnail_image`、または `additional_images`）に設定します。

   >[!NOTE]
   >
   >デフォルトの読み込みフォルダー内の画像の場合（`var/import/images`）、CSV データのファイル名の前にパスを含めないでください。

   CSV ファイルには、を含める必要があります。 `sku` 列および関連する画像列。

   ![例 – CSV 画像データの読み込み](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 指示に従って～する [import](data-import.md) データ。

1. 読み込むファイルを選択したら、次の相対パスを入力します **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![データインポート画像ファイルディレクトリ](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >移動 _[!UICONTROL Images File Directory]_を使用する場合は空白 `<Magento-root-folder>/var/import/images` ディレクトリ。 Adobe CommerceおよびMagento Open Sourceバージョン 2.3.2 以降、これはデフォルトの import images ベースディレクトリです。

   1 つの画像に対して複数の画像を読み込む場合 `sku`画像をという名前の列に挿入します。 `additional_images` （まだ追加されていない場合は、列をコンマで区切って追加します）。 例： `image02.jpg,image03.jpg`

## 方法 2：外部サーバーからの画像のインポート

1. インポートする画像を外部サーバー上の指定フォルダーにアップロードします。

1. CSV データで、画像タイプ（`base_image`, `small_image`, `thumbnail_image`、または `additional_images`）に設定します。

   ```terminal
   https://example.com/images/image.jpg
   ```

1. 指示に従って～する [import](data-import.md) データ。

## 方法 3：リモートストレージを使用した画像のインポート

1. リモートストレージモジュールで、画像ファイルをにアップロードします。 `var/import/images` フォルダーまたはサブフォルダー（例：） `var/import/images/product_images`. これは、商品画像を読み込むためのデフォルトのルートフォルダーです。

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe CommerceとMagento Open Sourceの概要 `2.3.2` release、で指定されたパス _[!UICONTROL Images File Directory]_はインポート用に画像のベースディレクトリに連結されます。 `<remote-storage-root-folder>/var/import/images`. 以前のAdobe CommerceおよびMagento Open Sourceのリリースでは、読み込み処理中にフォルダーへのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、正しい行に読み込む各画像ファイルの名前を、次のように入力します。 `sku`を選択し、画像タイプに応じて適切な列に表示されます（`base_image`, `small_image`, `thumbnail_image`、または `additional_images`）に設定します。

   >[!NOTE]
   >
   >デフォルトの読み込みフォルダー内の画像の場合（`var/import/images`）、CSV データのファイル名の前にパスを含めないでください。

   CSV ファイルには、を含める必要があります。 `sku` 列および関連する画像列。

   ![例 – CSV 画像データの読み込み](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 指示に従って～する [import](data-import.md) データ。

1. 読み込むファイルを選択したら、次の相対パスを入力します **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >を残す _[!UICONTROL Images File Directory]_を使用する場合は空白 `<Magento-root-folder>/var/import/images` ディレクトリ。 Adobe CommerceおよびMagento Open Sourceバージョン 2.3.2 以降、これはデフォルトの import images ベースディレクトリです。

   1 つの画像に対して複数の画像を読み込む場合 `sku`画像をという名前の列に挿入します。 `additional_images` （まだ追加されていない場合は列を追加）。コンマで区切ります。 `image02.jpg,image03.jpg`

リモート・ストレージ・モジュールの有効化と管理の詳細については、を参照してください [リモートストレージの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) が含まれる _設定ガイド_.

>[!NOTE]
>
>製品画像を読み込んでも、画像のサイズ変更は開始されません。 製品画像は、フロントエンドで次のようにサイズ変更されます。 `pub/get.php`. 次のことを確認します `pub/get.php` は正常に機能しています。正常に機能していない場合は、画像のサイズが変更されない可能性があります。
