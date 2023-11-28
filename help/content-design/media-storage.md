---
title: メディアストレージ
description: メディアストレージを使用して、サーバーに保存されているコマースメディアファイルを整理し、アクセス権を取得する方法を説明します。
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# メディアストレージ

メディアストレージを使用すると、サーバーに保存されているメディアファイルを整理し、そのファイルにアクセスできます。 ファイルの場所へのパスは、 [ベース URL](../stores-purchase/store-urls.md) 設定。 メディアストレージ内のファイルは、ページや静的ブロックで作業している間、エディターからアクセスできます。 通常、メディアストレージは、 [!DNL Commerce] プログラムファイル。

また、メディアファイルは [データベース](media-storage-database.md)または別のサーバーまたは [コンテンツ配信ネットワーク](media-storage-content-delivery-network.md). 代替ストレージを使用する利点は、メディアを同期するのに必要な作業を最小限に抑えることです。 同期のパフォーマンスは、同じ画像、CSS ファイル、および他のメディアファイルにアクセスする必要がある異なるサーバーにシステムの複数のインスタンスがデプロイされている場合に特に影響を受けます。

エディターは、静的または [ダイナミックメディアの URL](../catalog/catalog-urls.md#configure-catalog-media-url-format) （カテゴリまたは製品の説明のカタログコンテンツ）

![[!DNL Commerce] メディアストレージ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージにファイルを追加する

最初の 2 つの手順は、画像を挿入する場合と同じです。

1. 次の日： [編集者](editor.md) ツールバーで、 _画像を挿入_ アイコン。

   ![画像挿入アイコン](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   このアクションを実行すると、 _[!UICONTROL Insert/edit image]_ダイアログ。

1. 後 _[!UICONTROL Source]_をクリックし、_&#x200B;検索&#x200B;_アイコン (![検索アイコン](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}) をクリックします。

1. 左側のディレクトリツリーで、次のいずれかの操作を行います。

   - アップロードした画像を保存するフォルダーに移動します。

   - フォルダーを作成する場所に移動し、「 」をクリックします。 **フォルダーを作成**.

     フォルダーを追加する場合は、フォルダー名を入力し、 **[!UICONTROL OK]**.

1. 1 つ以上のファイルをメディアストレージに追加するには、システムからファイルをアップロードするか、 [Adobe Stock統合](adobe-stock.md):

   システムからファイルをアップロードするには、 **[!UICONTROL Choose Files]** 次の操作を実行します。

   - ローカルコンピューターのディレクトリ内で、画像の場所に移動します。

   - アップロードする各画像を選択します。

   - クリック **[!UICONTROL Open]**.

   を使用してAdobe Stockのアセットを使用するには [統合](adobe-stock.md):

   - クリック **[!UICONTROL Search Adobe Stock]**.

   - Adobe Stockからプレビューまたはライセンスを取得した画像を追加する ( [Adobe Stock Images の使用](adobe-stock-manage.md)) をクリックします。

画像は、サーバー上の現在のメディアストレージフォルダーにアップロードされます。

![[!DNL Commerce] メディアストレージ](./assets/media-storage.png){width="650" zoomable="yes"}

## メディアストレージから画像を挿入する

編集するページまたはブロックを開きます。 次に、次のいずれかの方法を使用して、メディアストレージから画像を挿入します。

### 方法 1:WYSIWYG モード

1. 次の日： [編集者](editor.md) ツールバーで、 _画像を挿入_ アイコン。

1. 後 _[!UICONTROL Source]_をクリックし、_&#x200B;検索&#x200B;_アイコン (![検索アイコン](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}) をクリックします。

   ![検索アイコンの選択](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. 左側のディレクトリツリーで、画像が保存されているフォルダーに移動します。

1. 画像のタイルを選択し、 **[!UICONTROL Add Selected]**.

### メソッド 2:HTMLモード

1. コード内で、 `<img>` タグを挿入します。

1. クリック **[!UICONTROL Insert Image]**.

   ![画像の挿入 (HTMLモード )](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
