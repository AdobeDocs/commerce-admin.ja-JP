---
title: 製品画像の読み込み
description: 各画像のパスとファイル名を使用して製品画像を読み込む方法について説明します。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
TQID: https://experienceleague.adobe.com/xqaM2qAUDV1yKXS5-90b7aQJUgEW-ZHg03UFo-dfKME
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 845
ht-degree: 0%

---

# 製品画像の読み込み

Adobe CommerceやMagento Open Sourceに読み込んだり、特定の商品に関連付けたりして、各タイプの複数の商品画像を使用できます。 各商品画像のパスとファイル名をCSV ファイルに入力し、インポートする画像ファイルをCommerce サーバーまたは外部サーバーの対応するパスにアップロードします。

Commerceでは、アルファベット順に配置された商品画像用の独自のディレクトリ構造を作成します。 既存の画像を含む製品データをCSV ファイルに書き出すと、各画像のファイル名の前にアルファベット順のパスが表示されます。 ただし、新しい画像を読み込む場合は、Commerceがディレクトリ構造を自動的に管理するため、パスを指定する必要はありません。 ただし、読み込む各画像のファイル名の前に、読み込みディレクトリへの相対パスを必ず入力してください。

画像をアップロードするには、ログイン資格情報と、サーバー上のCommerce フォルダーにアクセスするための正しい権限が必要です。 正しい資格情報を使用すると、任意のSFTP ユーティリティを使用して、デスクトップコンピューターからサーバーにファイルをアップロードできます。

多くの画像を読み込む前に、使用する読み込み方法の手順を確認し、いくつかの製品を含むプロセスを実行します。 仕組みを理解すれば、大量の画像を自信を持ってインポートできるようになります。

>[!IMPORTANT]
>
>UTF-8 エンコーディングをサポートするプログラムを使用して、メモ帳++などのCSV ファイルを編集することをお勧めします。 Microsoft® Excelは、CSV ファイルの列ヘッダーに追加の文字を挿入します。これにより、データがCommerceにインポートされるのを防ぐことができます。

## 方法1：ローカルサーバーから画像を読み込む

1. Commerce サーバーで、画像ファイルを`var/import/images` フォルダーまたは`var/import/images/product_images`などのサブフォルダーにアップロードします。 これは、製品画像を読み込むためのデフォルトのルートフォルダーです。

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe CommerceとMagento Open Source `2.3.2` リリース以降、**[!UICONTROL Images File Directory]**&#x200B;で指定されたパスは、images ベースディレクトリ `<Magento-root-folder>/var/import/images`へのインポート用に連結されます。 以前のAdobe CommerceおよびMagento Open Source リリースでは、インポートプロセス中にフォルダーへのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、読み込む各画像ファイルの名前を、画像タイプ （`base_image`、`small_image`、`thumbnail_image`、または`additional_images`）に従って、正しい行（`sku`）に入力します。

   >[!NOTE]
   >
   >デフォルトの読み込みフォルダー（`var/import/images`）内の画像の場合、CSV データにファイル名の前のパスを含めないでください。

   CSV ファイルには、`sku`列と関連する画像列のみを含める必要があります。

   ![例 – CSV画像データの読み込み](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. データを[&#x200B; インポート &#x200B;](data-import.md)する手順に従います。

1. 読み込むファイルを選択したら、**[!UICONTROL Images File Directory]**&#x200B;の後に相対パスを入力します。

   ```
   var/import/images
   ```

   ![&#x200B; データ読み込み画像ファイル ディレクトリ &#x200B;](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >`<Magento-root-folder>/var/import/images` ディレクトリを使用するには、_[!UICONTROL Images File Directory]_&#x200B;を空白のままにします。 Adobe CommerceおよびMagento Open Source バージョン 2.3.2以降では、これはデフォルトの読み込み画像ベースディレクトリです。

   1つの`sku`に複数の画像を読み込む場合は、画像を`additional_images`という名前の列に挿入します（まだ追加されていない場合は列を追加します）。コンマで区切ります。 例：`image02.jpg,image03.jpg`

## 方法2：外部サーバーから画像をインポートする

1. 読み込む画像を外部サーバーの指定フォルダーにアップロードします。

1. CSV データで、各画像ファイルの完全なURLを、画像タイプ （`base_image`、`small_image`、`thumbnail_image`、または`additional_images`）別の適切な列に入力します。

   ```
   https://example.com/images/image.jpg
   ```

1. データを[&#x200B; インポート &#x200B;](data-import.md)する手順に従います。

## 方法3：リモートストレージを使用して画像を読み込む

1. リモート ストレージ モジュールで、画像ファイルを`var/import/images` フォルダーまたは`var/import/images/product_images`などのサブフォルダーにアップロードします。 これは、製品画像を読み込むためのデフォルトのルートフォルダーです。

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe CommerceとMagento Open Source `2.3.2` リリース以降、_[!UICONTROL Images File Directory]_&#x200B;で指定されたパスは、画像の基本ディレクトリ `<remote-storage-root-folder>/var/import/images`に読み込むために連結されます。 以前のAdobe CommerceおよびMagento Open Source リリースでは、インポートプロセス中にフォルダーへのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、読み込む各画像ファイルの名前を、画像タイプ （`base_image`、`small_image`、`thumbnail_image`、または`additional_images`）に従って、正しい行（`sku`）に入力します。

   >[!NOTE]
   >
   >デフォルトの読み込みフォルダー（`var/import/images`）内の画像の場合、CSV データにファイル名の前のパスを含めないでください。

   CSV ファイルには、`sku`列と関連する画像列のみを含める必要があります。

   ![例 – CSV画像データの読み込み](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. データを[&#x200B; インポート &#x200B;](data-import.md)する手順に従います。

1. 読み込むファイルを選択したら、**[!UICONTROL Images File Directory]**&#x200B;の後に相対パスを入力します。

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >`<Magento-root-folder>/var/import/images` ディレクトリを使用するには、_[!UICONTROL Images File Directory]_&#x200B;を空白のままにします。 Adobe CommerceおよびMagento Open Source バージョン 2.3.2以降では、これはデフォルトの読み込み画像ベースディレクトリです。

   1つの`sku`に複数の画像を読み込む場合は、`additional_images`という名前の列に画像を挿入します（まだ追加されていない場合は列を追加します）。コンマで区切ります：`image02.jpg,image03.jpg`

リモートストレージモジュールの有効化と管理について詳しくは、_設定ガイド_&#x200B;の[&#x200B; リモートストレージの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html)を参照してください。

>[!NOTE]
>
>製品画像を読み込むと、画像のサイズ変更が開始されません。 製品画像はフロントエンドで`pub/get.php`によってサイズ変更されます。 `pub/get.php`が正しく動作していることを確認してください。それ以外の場合は、画像のサイズが変更されない可能性があります。
