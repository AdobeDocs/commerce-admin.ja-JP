---
title: AEMへのメディアファイルの移行
description: Adobe Commerceまたは外部ソースからAEM Assets DAMにメディアファイルを移行します。
feature: CMS, Media, Integration
exl-id: fead5732-b014-4cd3-a776-98a055a696ab
TQID: https://experienceleague.adobe.com/2eqYvVrxPO-yFYKtRPUExzxPPxXUy1v9KhR4LYjIBZY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: da3860b0-d637-47df-bef0-273751180266id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 892
ht-degree: 0%

---

# AEM Assets DAMへのメディアファイルの移行

Adobe CommerceとAdobe Experience Manager（AEM）の両方に、CommerceからAEM Assets DAMへのメディアファイルの移行を効率化する機能が組み込まれています。 他のソースからメディアファイルを移行することもできます。

## 前提条件

| カテゴリ | 要件 |
|----------|-------------|
| **必要システム構成** | <ul><li>AEM AssetsでプロビジョニングされたAEM as a Cloud Service環境</li><li>十分なストレージ容量</li><li>大規模なファイル転送に対応するネットワーク帯域幅</li></ul> |
| **必要なアクセスと権限** | <ul><li>AEM Assets as a Cloud Serviceへの管理者アクセス</li><li>メディアファイルが保存されているソースシステム（Adobe Commerceまたは外部システム）へのアクセス</li><li>クラウドストレージサービスにアクセスするための適切な権限</li></ul> |
| **クラウドストレージアカウント** | <ul><li>AWS S3またはAzure Blob Storage アカウント</li><li>プライベートコンテナ/バケット設定</li><li>認証情報</li></ul> |
| **Source コンテンツ** | <ul><li>移行用に整理されたメディアファイル</li><li>AEM Assets</a>でサポートされている<a href="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats">形式の画像およびビデオファイル。</li><li>重複を排除したクリーンなアセット</li></li> |
| **メタデータの準備** | <ul><li><a href="https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">Commerce assets用に設定されたAEM Assets メタデータプロファイル </a></li><li>各アセットのマッピングされたメタデータ値</li><li>CSV ファイルエディター（例：Microsoft Excel）</li></ul> |

## 移行のベストプラクティス

1. 未使用および重複するコンテンツを削除して、移行前にアセットをキュレートします。
1. サイズ、形式、ユースケースごとに、アセットを論理的に整理します。
1. 大規模な移行を小規模なバッチに分割することを検討する。
1. オフピーク時に、リソース集約的なインポートをスケジューリングします。
1. 完全に読み込む前に、メタデータマッピングを検証します。

## 移行ワークフロー

移行ワークフローに従って、Adobe Commerceまたは他の外部システムからメディアファイルを書き出し、AEM Assets DAMに読み込みます。

### 手順1：既存のデータソースからコンテンツを書き出す

Adobe Commerceを利用している販売者は、リモートストレージモジュールを使用して、Commerceからメディアファイルを書き出し、AEM Assetsに読み込む効率的な方法を利用できます。 このモジュールを使用すると、AWS S3などのリモートストレージサービスにメディアファイルを保存および管理できるため、移行プロセスがより効率的になります。 Commerce インスタンスのリモートストレージを設定するには、*Commerce設定ガイド*&#x200B;の[ リモートストレージの設定](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3)を参照してください。

Adobe Commerce以外にメディアファイルが保存されている場合は、AEM as a Cloud Serviceでサポートされている[ データソース ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites)のいずれかに直接アップロードします。

### 手順2：メタデータマッピング用のCSV ファイルの作成

メタデータマッピングファイルをCSV形式で作成し、メディアファイルを含むソースフォルダーにアップロードします。 このファイルは、必要なメタデータを各アセットにマッピングし、以下を行います。

- DAM内のアセットを整理して分類し、容易に発見
- Adobe CommerceとAEM Assetsの適切な同期を有効にする
- 移行後にアセットと製品の関係を維持する

移行するメディアファイルごとに、次の表に示すように、Commerce assetsの[AEM Assets メタデータプロファイル ](aem-assets-configure-aem.md)に含まれるメタデータフィールドの値を指定します。

| メタデータ | 説明 | 値 |
|-------|-------------|--------|
| assetPath | アセットがAEM Assets リポジトリに保存されるフルパス。<br><br> パスを使用してサブフォルダーを作成し、Commerce アセットを整理します（例：`content/dam/commerce/<brand>/<type>`）。 | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc:title | AEM Assetsでのアセットの表示タイトル | 文字列値（例：`Sample 1`） |
| dam:status | AEM Assetsでのアセットの承認ステータス | `approved` |
| commerce:positions | 製品ギャラリー内のアセットの位置/順序 | 数値（例：「1」） |
| commerce:isCommerce | アセットがコマースで使用されているかどうかを示すフラグ | `Yes` |
| commerce:skus | このアセットに関連付けられた製品SKU | 文字列値（例：`sample1`） |
| commerce:roles | アセットの役割または画像の種類（例：`thumbnail`、`main image`、`swatch`） | セミコロンで区切られた複数の値（例：「thumbnail; image; swatch_image; small_image」） |

+++CSV コード

このサンプルのCSV コードを使用して、コードエディターまたはMicrosoft Excelなどのスプレッドシートアプリケーションでファイルを作成します。

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

### ステップ 3:AssetsをAEM Assetsに一括読み込む

メタデータマッピングファイルを作成したら、AEM Assetsの一括読み込みツールを使用してアセットを読み込みます。

次に、ツールの概要を示します。

1. [AEM Assets as a Cloud Service オーサー環境](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem)にログインします。

1. Experience Manager ツール ビューから、**[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]**&#x200B;を選択します。

   ![AEM Assets オーサリング ](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. 一括読み込み設定から、**[!UICONTROL Create]**&#x200B;を選択して設定フォームを開きます。

   ![AEM Assets オーサリング ](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. 設定を設定して保存します。

   次のようなものがあります。

   - データソースの認証情報
   - 読み込んだファイルが保存されるAEM Assetsのターゲットフォルダー
   - インポート設定をカスタマイズするためのMIME タイプ、ファイルサイズおよびその他のパラメーターに関する情報（オプション）
   - クラウドストレージインスタンスにアップロードしたメタデータマッピング CSV ファイルへのパス。

   詳細な手順については、*AEM Assets as a Cloud Service ユーザーガイド*&#x200B;の「[一括読み込みツールの設定](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool)」を参照してください。

1. 設定を保存した後、一括読み込みツールを使用してテストし、読み込み操作を実行します。

>[!MORELIKETHIS]
>
>[ ツールビデオの一括読み込みデモ ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[ ヒント、ベストプラクティス、制限事項](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[APIを使用したアセットのアップロードまたは取り込み](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)
