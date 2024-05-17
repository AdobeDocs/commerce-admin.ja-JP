---
title: メディアストレージ
description: サーバーに保存されているCommerce メディアファイルを整理し、アクセスできるようにするメディアストレージの仕組みについて説明します。
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# メディアストレージ

メディアストレージを使用すると、サーバーに保存されているメディアファイルを整理し、アクセスできます。 ファイルの場所へのパスは、 [ベース URL](../stores-purchase/store-urls.md) 設定。 メディアストレージ内のファイルは、ページや静的ブロックの作業中にエディターからアクセスできます。 通常、メディアストレージは、と同じサーバー上のファイルシステムに存在します。 [!DNL Commerce] プログラム ファイル。

または、以下でメディアファイルを管理できます [データベース](media-storage-database.md)、または別のサーバー上 [コンテンツ配信ネットワーク](media-storage-content-delivery-network.md). 代替ストレージを使用する利点は、メディアの同期に必要な労力を最小限に抑えることです。 同じ画像、CSS ファイル、その他のメディアファイルへのアクセスが必要な異なるサーバーにシステムの複数のインスタンスがデプロイされている場合、同期のパフォーマンスは特に影響を受けます。

エディターは、静的または [dynamic media の URL](../catalog/catalog-urls.md#configure-catalog-media-url-format) カテゴリまたは製品の説明のカタログコンテンツの場合。

![[!DNL Commerce] メディアストレージ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージへのファイルの追加

最初の 2 つの手順は、画像を挿入する場合と同じです。

1. 日 [エディター](editor.md) ツールバーで、 _画像の挿入_ アイコン。

   ![画像を挿入アイコン](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   このアクションにより、が開きます _[!UICONTROL Insert/edit image]_ダイアログ。

1. 後 _[!UICONTROL Source]_を選択し、_&#x200B;検索&#x200B;_アイコン （![検索アイコン](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}）に設定します。

1. 左側のディレクトリツリーで、次のいずれかの操作を行います。

   - アップロードした画像を保存するフォルダーに移動します。

   - フォルダーを作成する場所に移動し、をクリックします **フォルダーを作成**.

     フォルダーを追加する場合は、フォルダー名を入力し、 **[!UICONTROL OK]**.

1. 1 つ以上のファイルをメディアストレージに追加するには、システムからファイルをアップロードするか、を使用します [Adobe Stockの統合](adobe-stock.md):

   システムからファイルをアップロードするには、 **[!UICONTROL Choose Files]** 次の手順を実行します。

   - ローカルコンピューターのディレクトリで、画像の場所に移動します。

   - アップロードする各画像を選択します。

   - クリック **[!UICONTROL Open]**.

   を使用してAdobe Stockのアセットを使用するには [統合](adobe-stock.md):

   - クリック **[!UICONTROL Search Adobe Stock]**.

   - Adobe Stockからのプレビュー画像またはライセンス画像の追加（を参照） [Adobe Stock画像の使用](adobe-stock-manage.md)）に設定します。

画像は、サーバー上の現在のメディアストレージフォルダーにアップロードされます。

![[!DNL Commerce] メディアストレージ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージからの画像の挿入

編集するページまたはブロックを開きます。 次に、次のいずれかの方法を使用して、メディアストレージから画像を挿入します。

### 方法 1:WYSIWYG モード

1. 日 [エディター](editor.md) ツールバーで、 _画像の挿入_ アイコン。

1. 後 _[!UICONTROL Source]_を選択し、_&#x200B;検索&#x200B;_アイコン （![検索アイコン](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}）に設定します。

   ![検索アイコンの選択](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. 左側のディレクトリツリーで、画像が格納されているフォルダーに移動します。

1. 画像のタイルを選択し、 **[!UICONTROL Add Selected]**.

### 方法 2:HTMLモード

1. コード内でカーソルを `<img>` タグが挿入されます。

1. クリック **[!UICONTROL Insert Image]**.

   ![画像を挿入（HTMLモード）](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
