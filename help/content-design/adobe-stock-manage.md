---
title: Adobe Stock画像の使用
description: Adobe Stockの画像を使用してストアのページを拡張します。
exl-id: 8f7d6f0a-511f-4f4b-821d-10a06e18041e
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 1%

---

# Adobe Stock画像の使用

[Adobe Stock](https://stock.adobe.com) 独自の画像コンテンツをアップロードする代わりに画像を使用できます。 一般的な使用例の 1 つは、ページの作成時に画像コンテンツをアップロードして配置する場合です。

The [[!DNL Media Gallery]](media-gallery.md) はAdobe Stockと直接統合され、ギャラリーページから直接画像のライセンスを取得しやすくします。

## Adobe Stock検索グリッドへのアクセス

Adobe Stockの検索パネルは、 [ページを追加または編集](page-add.md)、 [カテゴリの作成または編集](../catalog/category-create.md)、または [コンテンツエディターで画像を挿入する](editor-insert-image.md).

**_Adobe Stock Assets を検索してページに Stock 画像を追加するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. クリック **[!UICONTROL Add a New Page]**.

   既存のページを編集する場合は、 _[!UICONTROL Action]_列をクリック&#x200B;**[!UICONTROL Select]**を選択します。**[!UICONTROL Edit]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Content]** 」セクションで次の操作を実行します。

   - 次の条件を満たす [WYSIWYG エディタが有効](editor.md)をクリックし、 **[!UICONTROL Show/Hide Editor]** 次に、「 **[!UICONTROL Insert Image]**.

   - 次の条件を満たしている場合： [Page Builder が有効](../page-builder/setup.md)、を展開します。 **[!UICONTROL Media]** パネルとドラッグ **[!UICONTROL Image]** プレースホルダーをターゲットコンテナに追加します。 次に、「 **[!UICONTROL Select from Gallery]**.

     ![ページビルダーステージへの画像のドラッグ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Search Adobe Stock]**.

**_Adobe Stock Assets を検索してカテゴリに在庫画像を追加するには：_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. クリック **[!UICONTROL Add Root Category]** または **[!UICONTROL Add Subcategory]**.

   既存のカテゴリに画像を追加する場合は、左側のリストでカテゴリ名をクリックします。

1. を展開します。 **[!UICONTROL Content]** セクションと _[!UICONTROL Category Image]_click **[!UICONTROL Select from Gallery]**.

1. クリック **[!UICONTROL Search Adobe Stock]**.

Adobe Stock Assets を検索し、WYSIWYG エディターから Stock 画像を追加するには、次の手順を実行します。

1. click **[!UICONTROL Show/Hide Editor]**.

1. クリック **[!UICONTROL Insert Image]**.

1. クリック **[!UICONTROL Search Adobe Stock]**.

   ![Adobe Stock Search Results](./assets/adobe-stock-search-grid.png){width="600" zoomable="yes"}

## Adobe Stockアセットのフィルタリングと検索

The [Adobe Stock search Grid](#access-the-adobe-stock-search-grid) には、 [!DNL Commerce] ストア。

デフォルトでは、表示される検索結果は、Adobe Stockが厳選した、数百件の結果を集めたギャラリーです。 独自のキーワード検索を適用すると、Adobe Stockで使用可能な数百万のアセットを検索します。

### キーワードによるAdobe Stockアセットの検索

1. [Adobe Stock Search グリッドへのアクセス](#access-the-adobe-stock-search-grid).

1. キーワード検索を **[!UICONTROL Search by keyword]** 左上の入力フィールドを開き、虫眼鏡アイコンをクリックするか、 **入力**.

   ![Adobe Stock 「mango」キーワードの検索結果](./assets/adobe-stock-search-keyword.png){width="600" zoomable="yes"}

### Adobe Stock Assets のフィルタリング

1. [Adobe Stock Assets のキーワード検索の実行](#search-for-adobe-stock-assets-by-keywords).

1. クリック **[!UICONTROL Filters]**.

   検索結果を絞り込むためのフィルターがいくつかあります。

   | フィルター | 説明 |
   |---|---|
   | [!UICONTROL Subcategory] | 次の画像のフィルター **写真** または **図** |
   | [!UICONTROL Orientation] | サイズ、形状、縦横比で画像をフィルタリングする |
   | [!UICONTROL Color] | カラーパレットを使用して画像をカラーでフィルタリングする |
   | [!UICONTROL Price] | コストに基づいて画像をフィルタリング |
   | [!UICONTROL Safe search] | セーフ検索を有効または無効にする |
   | [!UICONTROL Isolated Assets] | 表示を次のみに制限 _分離資産_&#x200B;その背景には、単独で被写体が現れる |

   {style="table-layout:auto"}

   ![Adobe Stock検索フィルター](./assets/adobe-stock-filters.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Apply Filters]**.

   検索結果のグリッドが、絞り込まれた検索で更新されます。

## 画像の詳細を表示

各画像には、表示可能な詳細情報が含まれます。 追加の画像固有のアクション（例： ） [画像プレビューを保存中](adobe-stock-save-preview.md) または [画像の保存（およびオプションでライセンス付け）](adobe-stock-license-image.md)は、この詳細ビューから使用できます。

1. [Adobe Stock検索グリッドへのアクセス](#access-the-adobe-stock-search-grid).

1. 検索結果内の画像をクリックします。

   その他の画像の詳細が表示されます。例：

   - 画像の大きいバージョン
   - 画像メタデータ（例： ） _[!UICONTROL Dimensions]_,_[!UICONTROL File type]_, _[!UICONTROL Category]_,_[!UICONTROL File]_、および _キーワード_
   - 関連する画像（同じ画像からの画像など） _シリーズ_ または _モデル_
   - アクションボタン（例： ） [[!UICONTROL Save Preview]](adobe-stock-save-preview.md) および [[!UICONTROL Save (and optionally license) Image]](adobe-stock-license-image.md)

     ![Adobe Stockの画像の詳細](./assets/adobe-stock-image-details.png){width="600" zoomable="yes"}

## Adobeアカウントにログイン

画像に対する完全なアクセス権を取得し、Adobe Stockの透かしを排除するには、次の手順を実行します。 [ログインアカウントでAdobe](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html) 画像を使用する権利をライセンスするクレジットを購入します。

1. [Adobe Stock Search グリッドへのアクセス](#access-the-adobe-stock-search-grid).

1. クリック **[!UICONTROL Sign In]** 右上に

   新しいブラウザーウィンドウが表示され、 [Adobeサインインプロセス](https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html).

   ログインプロセスが完了すると、画像のライセンス状態が検索結果にラベルとして表示されます。

   ![Adobeのログイン](./assets/adobe-stock-account-login.png){width="600" zoomable="yes"}

### 検索結果のライセンス状態の表示

[Adobeアカウントにログイン](#log-in-to-your-adobe-account).

ライセンスが必要な画像は、Adobeアカウントに関連付けられているすべての画像にラベルが表示され、ライセンスを取得した画像が明確になります。

![Adobe Stockライセンス済み画像を使用した検索結果](./assets/adobe-stock-licensed-images.png){width="600" zoomable="yes"}

### メディアストレージに画像を保存

Adobe Stock統合を使用して検索された画像は、 [!DNL Commerce] [メディアストレージ](media-storage.md) すべてのユーザーが簡単に再利用できるように [!DNL Commerce] ストア。

次の 2 種類の画像を保存できます。 [画像プレビュー](adobe-stock-save-preview.md) または [ライセンス済み画像](adobe-stock-license-image.md).

#### 画像プレビューの保存

画像プレビューは、透かし入りのAdobe Stockアセットです。 画像のプレビューは無料で、特定の画像のライセンスを購入して実稼動ストアで使用する前に、様々な画像を試す良い方法です。

1. [Adobe Stock検索グリッドへのアクセス](#access-the-adobe-stock-search-grid).

1. 宛先 [画像の詳細を表示](#view-image-details)をクリックし、検索グリッドで画像をクリックします。

1. クリック **[!UICONTROL Save Preview]**.

   この操作を実行すると、イメージをメディアストレージに保存する際に使用するファイル名を指定するプロンプトが表示されます。 デフォルトのファイル名が指定されますが、設定に合わせて名前をカスタマイズできます。

   ![Adobe Stockのプレビュー画像を保存](./assets/adobe-stock-save-preview.png){width="500" zoomable="yes"}

1. クリック **[!UICONTROL Confirm]**.

   ページはメディアストレージにリダイレクトされ、保存したプレビューが表示されます。

#### ライセンス済み画像の保存

実稼動用に使用するAdobe Stockアセット [!DNL Commerce] ストアのライセンスが必要です。 ライセンスを使用すると、画像に法的にアクセスでき、すべての画像に存在するAdobe Stockの透かしを排除できます [画像のプレビュー](adobe-stock-save-preview.md). 画像のライセンスを取得したり、ライセンスを取得済みの画像を保存するには、Adobeアカウントにログインする必要があります。

1. [Adobeアカウントにログイン](#log-in-to-your-adobe-account).

1. 宛先 [画像の詳細を表示](#view-image-details)をクリックし、検索グリッドで画像をクリックします。

1. イメージの現在のライセンス状態に応じて、次のいずれかの操作を行います。

   - 画像が既にライセンスされている場合は、 **[!UICONTROL Save]**.

   - 画像が _not_ ライセンス済み、クリック **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >使用可能である必要があります [Adobe Stock単位](https://helpx.adobe.com/stock/help/credit-packs.html) 」をクリックして、画像のライセンスを取得します。

   この操作を実行すると、イメージを [メディアストレージ](media-storage.md). デフォルトのファイル名が指定されますが、設定に合わせて名前をカスタマイズできます。

1. クリック **[!UICONTROL Confirm]**.

   ページはメディアストレージにリダイレクトされ、保存したプレビューが表示されます。
