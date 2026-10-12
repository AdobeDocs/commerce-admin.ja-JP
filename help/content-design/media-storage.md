---
title: メディアストレージ
description: メディアストレージを使用して、サーバーに保存されているCommerce メディアファイルを整理し、アクセスできるようにする方法について説明します。
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: 4ca54350-01cb-5b22-8966-5f2873dc6d90
    internal-label: Media
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%
---
# メディアストレージ

メディアストレージは、サーバーに保存されているメディアファイルを整理し、アクセスできるようにします。 ファイルの場所へのパスは、[ ベース URL](../stores-purchase/store-urls.md)設定によって決まります。 メディアストレージ内のファイルは、ページと静的ブロックの作業中にエディターからアクセスできます。 通常、メディアストレージは、[!DNL Commerce] プログラムファイルと同じサーバー上のファイルシステムにあります。

または、メディアファイルは[ データベース ](media-storage-database.md)または別のサーバーまたは[ コンテンツ配信ネットワーク ](media-storage-content-delivery-network.md)で管理できます。 代替ストレージを使用する利点は、メディアの同期に必要な労力を最小限に抑えることです。 同期パフォーマンスは、同じ画像、CSS ファイル、その他のメディアファイルにアクセスする必要がある異なるサーバーにシステムの複数のインスタンスがデプロイされた場合に特に影響を受けます。

エディターは、カテゴリまたは製品説明のカタログコンテンツに静的または[動的メディア URL](../catalog/catalog-urls.md#configure-catalog-media-url-format)を使用するように設定できます。

![[!DNL Commerce] メディアストレージ ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージへのファイルの追加

最初の2つの手順は、画像を挿入する場合と同じです。

1. [ エディター](editor.md) ツールバーで、_画像を挿入_ アイコンをクリックします。

   ![画像を挿入アイコン ](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   このアクションにより、_[!UICONTROL Insert/edit image]_ダイアログが開きます。

1. _[!UICONTROL Source]_の後、_&#x200B;検索&#x200B;_アイコン （![検索アイコン ](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}）をクリックします。

1. 左側のディレクトリツリーで、次のいずれかの操作を行います。

   - アップロードした画像を保存するフォルダーに移動します。

   - フォルダーを作成する場所に移動し、**フォルダーを作成**&#x200B;をクリックします。

     フォルダーを追加するには、フォルダー名を入力し、**[!UICONTROL OK]**&#x200B;をクリックします。

1. 1つ以上のファイルをMedia Storageに追加するには、システムからファイルをアップロードするか、[Adobe Stock統合](adobe-stock.md)を使用します。

   システムからファイルをアップロードするには、**[!UICONTROL Choose Files]**&#x200B;をクリックし、次の操作を行います。

   - ローカルコンピューターのディレクトリで、画像の場所に移動します。

   - アップロードする各画像を選択します。

   - **[!UICONTROL Open]**&#x200B;をクリックします。

   [統合](adobe-stock.md)を使用してAdobe Stockのアセットを使用するには：

   - **[!UICONTROL Search Adobe Stock]**&#x200B;をクリックします。

   - Adobe Stockからプレビューまたはライセンス済みの画像を追加します（[Adobe Stock画像の使用](adobe-stock-manage.md)を参照）。

画像は、サーバー上の現在のMedia Storage フォルダーにアップロードされます。

![[!DNL Commerce] メディアストレージ ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージからの画像の挿入

編集するページまたはブロックを開きます。 次のいずれかの方法を使用して、メディアストレージから画像を挿入します。

### 方法1:WYSIWYGモード

1. [ エディター](editor.md) ツールバーで、_画像を挿入_ アイコンをクリックします。

1. _[!UICONTROL Source]_の後、_&#x200B;検索&#x200B;_アイコン （![検索アイコン ](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}）をクリックします。

   ![検索アイコンの選択](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. 左側のディレクトリツリーで、画像が保存されているフォルダーに移動します。

1. 画像のタイルを選択し、**[!UICONTROL Add Selected]**&#x200B;をクリックします。

### 方法2:HTMLモード

1. `<img>` タグを挿入するコード内にカーソルを置きます。

1. **[!UICONTROL Insert Image]**&#x200B;をクリックします。

   ![画像を挿入（HTML モード） ](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
