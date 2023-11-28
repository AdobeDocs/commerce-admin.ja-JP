---
title: 製品画像のインポート
description: 各画像のパスとファイル名を使用して、製品画像を読み込む方法を説明します。
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# 製品画像のインポート

各タイプの複数の製品画像をAdobe CommerceやMagento Open Sourceに読み込み、特定の製品に関連付けることができます。 各製品画像のパスとファイル名が CSV ファイルに入力され、読み込む画像ファイルが Commerce サーバーまたは外部サーバーの対応するパスにアップロードされます。

Commerce は、アルファベット順に整理された製品画像用に独自のディレクトリ構造を作成します。 既存の画像を含む製品データを CSV ファイルに書き出すと、各画像のファイル名の前に、アルファベット順のパスが表示されます。 ただし、新しい画像を読み込む場合、パスを指定する必要はありません。Commerce はディレクトリ構造を自動的に管理するからです。 ただし、インポートする各画像のファイル名の前に、インポートディレクトリの相対パスを必ず入力してください。

画像をアップロードするには、サーバー上の Commerce フォルダーにアクセスするためのログイン資格情報と正しい権限が必要です。 正しい資格情報があれば、任意の SFTP ユーティリティを使用して、デスクトップコンピューターからサーバーにファイルをアップロードできます。

多数の画像を読み込む前に、使用する読み込み方法の手順を確認し、いくつかの製品でプロセスを実行します。 動作を理解したら、大量の画像を読み込む自信を持つことができます。

>[!IMPORTANT]
>
>UTF-8 エンコーディングをサポートするプログラム (Notepad++など ) を使用して CSV ファイルを編集することをお勧めします。 Microsoft® Excel は、CSV ファイルの列ヘッダーに追加の文字を挿入します。これにより、データが Commerce にインポートされなくなります。

## 方法 1：ローカルサーバーから画像をインポートする

1. Commerce サーバーで、画像ファイルを `var/import/images` フォルダーまたはサブフォルダー（例： ） `var/import/images/product_images`. これは、製品画像を読み込むためのデフォルトのルートフォルダです。

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe CommerceとMagento Open Sourceの使用 `2.3.2` release: **[!UICONTROL Images File Directory]** イメージベースディレクトリへの読み込み用の連結 — `<Magento-root-folder>/var/import/images`. Adobe CommerceとMagento Open Sourceの以前のリリースでは、インポートプロセス中にフォルダーのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、正しい行にインポートする各画像ファイルの名前を、 `sku`を指定し、画像タイプ (`base_image`, `small_image`, `thumbnail_image`または `additional_images`) をクリックします。

   >[!NOTE]
   >
   デフォルトの読み込みフォルダー (`var/import/images`) を含める場合、CSV データのファイル名の前にパスを含めないでください。

   CSV ファイルには、 `sku` 列と関連する画像列

   ![例 — CSV 画像データのインポート](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 手順に従って、 [インポート](data-import.md) データ。

1. インポートするファイルを選択した後、次の相対パスを入力します。 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![データインポート画像ファイルディレクトリ](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   終了 _[!UICONTROL Images File Directory]_空白： `<Magento-root-folder>/var/import/images` ディレクトリ。 Adobe CommerceおよびMagento Open Sourceバージョン 2.3.2 以降では、これがデフォルトのインポート画像ベースディレクトリになっています。

   1 つに対して複数の画像を読み込む場合 `sku`、という名前の列に画像を挿入します。 `additional_images` （まだ列を追加していない場合は列を追加します）をコンマで区切ります。 例： `image02.jpg,image03.jpg`

## 方法 2：外部サーバーから画像をインポートする

1. 読み込む画像を、外部サーバーの指定されたフォルダーにアップロードします。

1. CSV データで、各画像ファイルの完全な URL を画像タイプ別の正しい列に入力します (`base_image`, `small_image`, `thumbnail_image`または `additional_images`) をクリックします。

   ```terminal
   https://example.com/images/image.jpg
   ```

1. 手順に従って、 [インポート](data-import.md) データ。

## 方法 3：リモートストレージを使用したイメージのインポート

1. リモートストレージモジュールで、画像ファイルを `var/import/images` フォルダーまたはサブフォルダー（例： ） `var/import/images/product_images`. これは、製品画像を読み込むためのデフォルトのルートフォルダです。

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe CommerceとMagento Open Sourceの使用 `2.3.2` release: _[!UICONTROL Images File Directory]_読み込み用の連結を画像ベースディレクトリに設定します。 `<remote-storage-root-folder>/var/import/images`. 以前のAdobe CommerceおよびMagento Open Sourceリリースでは、インポートプロセス中にフォルダーのパスが指定されている限り、Commerce サーバー上で別のフォルダーを使用できます。

1. CSV データで、正しい行にインポートする各画像ファイルの名前を、 `sku`を指定し、画像タイプ (`base_image`, `small_image`, `thumbnail_image`または `additional_images`) をクリックします。

   >[!NOTE]
   >
   デフォルトの読み込みフォルダー (`var/import/images`) を含める場合、CSV データのファイル名の前にパスを含めないでください。

   CSV ファイルには、 `sku` 列と関連する画像列

   ![例 — CSV 画像データのインポート](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 手順に従って、 [インポート](data-import.md) データ。

1. インポートするファイルを選択した後、次の相対パスを入力します。 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   を残します。 _[!UICONTROL Images File Directory]_空白： `<Magento-root-folder>/var/import/images` ディレクトリ。 Adobe CommerceおよびMagento Open Sourceバージョン 2.3.2 以降では、これがデフォルトのインポート画像ベースディレクトリになっています。

   1 つに対して複数の画像を読み込む場合 `sku`、という名前の列に画像を挿入します。 `additional_images` （まだ列を追加していない場合は、列を追加します）をコンマで区切ります。 `image02.jpg,image03.jpg`

リモートストレージモジュールの有効化と管理の詳細については、 [リモートストレージの構成](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) （内） _設定ガイド_.

>[!NOTE]
>
製品画像を読み込んでも、画像のサイズ変更は開始されません。 商品画像は、次の条件でフロントエンド上でサイズ変更されます。 `pub/get.php`. 次の項目を確認します。 `pub/get.php` が正常に動作していない場合は、画像のサイズが変更されない場合があります。
