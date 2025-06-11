---
title: Adobe Stock画像の使用
description: Adobe Stockの画像を使用してストアページを強化します。
exl-id: 8f7d6f0a-511f-4f4b-821d-10a06e18041e
feature: CMS, Media
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Adobe Stock画像の使用

[Adobe Stock](https://stock.adobe.com) 画像は、独自の画像コンテンツのアップロードの代わりに使用できます。 一般的なユースケースの 1 つは、ページの作成時に画像コンテンツをアップロードして配置することです。

[[!DNL Media Gallery]](media-gallery.md) はAdobe Stockとの直接統合を提供し、ギャラリーページから直接ライセンスを取得することが容易になります。

## Adobe Stock検索グリッドへのアクセス

Adobe Stockの検索パネルには、[ ページの追加または編集 ](page-add.md) を実行したとき、[ カテゴリの作成または編集 ](../catalog/category-create.md) を実行したとき、または [ コンテンツエディターを使用して画像を挿入 ](editor-insert-image.md) を実行したときにアクセスできます。

**_Adobe Stock アセットを検索してページにストック画像を追加するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. 「**[!UICONTROL Add a New Page]**」をクリックします。

   既存のページを編集する場合は、「_[!UICONTROL Action]_」列を使用して「**[!UICONTROL Select]**」をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

1. **[!UICONTROL Content]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   - [WYSIWYG Editor を有効にしている場合は ](editor.md) [**[!UICONTROL Show/Hide Editor]**]、[**[!UICONTROL Insert Image]**] の順にクリックします。

   - [ ページビルダーを有効 ](../page-builder/setup.md) にしている場合は、**[!UICONTROL Media]** パネルを展開し、**[!UICONTROL Image]** プレースホルダーをターゲットコンテナにドラッグします。 次に、「**[!UICONTROL Select from Gallery]**」をクリックします。

     ![ ページビルダーステージへの画像のドラッグ ](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Search Adobe Stock]**」をクリックします。

**_Adobe Stock アセットを検索してカテゴリにストック画像を追加するには：_**

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Categories]** に移動します。

1. **[!UICONTROL Add Root Category]** または **[!UICONTROL Add Subcategory]** をクリックします。

   既存のカテゴリに画像を追加する場合は、左側の一覧でカテゴリ名をクリックします。

1. **[!UICONTROL Content]** セクションを展開し、_[!UICONTROL Category Image]_&#x200B;の下の [**[!UICONTROL Select from Gallery]**] をクリックします。

1. 「**[!UICONTROL Search Adobe Stock]**」をクリックします。

Adobe Stock アセットを検索し、WYSIWYG エディターからストック画像を追加するには：

1. 「**[!UICONTROL Show/Hide Editor]**」をクリックします。

1. 「**[!UICONTROL Insert Image]**」をクリックします。

1. 「**[!UICONTROL Search Adobe Stock]**」をクリックします。

   ![Adobe Stock検索結果 ](./assets/adobe-stock-search-grid.png){width="600" zoomable="yes"}

## Adobe Stock アセットのフィルタリングと検索

[Adobe Stock検索グリッド ](#access-the-adobe-stock-search-grid) には、クエリとフィルターの機能が用意されており、[!DNL Commerce] ストアに最適な画像を見つけることができます。

デフォルトで表示される検索結果は、Adobe Stockがキュレートした、数百件の結果のギャラリーです。 独自のキーワード検索を適用すると、Adobe Stockで使用可能な数百万のアセットが検索されます。

### キーワードでAdobe Stock アセットを検索

1. [Adobe Stock検索グリッドへのアクセス ](#access-the-adobe-stock-search-grid)。

1. 左上の **[!UICONTROL Search by keyword]** 入力フィールドにキーワード検索を入力し、虫眼鏡をクリックするか、**Enter** キーを押します。

   ![ 「mango」キーワードのAdobe Stock検索結果 ](./assets/adobe-stock-search-keyword.png){width="600" zoomable="yes"}

### Adobe Stock アセットのフィルタリング

1. [Adobe Stock アセットのキーワード検索を実行します ](#search-for-adobe-stock-assets-by-keywords)。

1. 「**[!UICONTROL Filters]**」をクリックします。

   検索結果を絞り込むために使用できるフィルターはいくつかあります。

   | フィルター | 説明 |
   |---|---|
   | [!UICONTROL Subcategory] | 画像が **写真** または **イラスト** であるかどうかのフィルター |
   | [!UICONTROL Orientation] | サイズ、シェイプ、アスペクトで画像をフィルタリング |
   | [!UICONTROL Color] | カラーパレットを使用してカラーで画像をフィルタリングする |
   | [!UICONTROL Price] | コストに基づく画像のフィルタリング |
   | [!UICONTROL Safe search] | セーフ検索を有効または無効にする |
   | [!UICONTROL Isolated Assets] | 表示を、無地の背景にサブジェクトが単独で表示される _分離されたアセット_ のみに制限します |

   {style="table-layout:auto"}

   ![Adobe Stock検索フィルター ](./assets/adobe-stock-filters.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Apply Filters]**」をクリックします。

   絞り込んだ検索で検索結果グリッドが更新されます。

## 画像の詳細を表示

各画像には、表示可能な詳細があります。 [ 画像プレビューの保存 ](adobe-stock-save-preview.md) または [ 画像の保存（およびオプションでライセンスの付与） ](adobe-stock-license-image.md) など、画像固有の追加アクションは、この詳細ビューで実行できます。

1. [Adobe Stock検索グリッドへのアクセス ](#access-the-adobe-stock-search-grid)。

1. 検索結果の画像をクリックします。

   次のような画像の詳細が表示されます。

   - 画像の大きいバージョン
   - 画像メタデータ（_[!UICONTROL Dimensions]_、_[!UICONTROL File type]_、_[!UICONTROL Category]_、_[!UICONTROL File]_、_キーワード_ など）
   - 関連する画像（同じ _シリーズ_ または _モデルの画像など_
   - アクションボタン（[[!UICONTROL Save Preview]](adobe-stock-save-preview.md)、[[!UICONTROL Save (and optionally license) Image]](adobe-stock-license-image.md) など）

     ![Adobe Stock画像の詳細 ](./assets/adobe-stock-image-details.png){width="600" zoomable="yes"}

## Adobe アカウントにログインします

画像への完全なアクセス権を取得し、Adobe Stockの透かしを削除するには、[Adobe アカウントでログイン ](https://helpx.adobe.com/jp/manage-account/using/access-adobe-id-account.html) し、画像を使用するライセンス権限に対するクレジットを購入する必要があります。

1. [Adobe Stock検索グリッドへのアクセス ](#access-the-adobe-stock-search-grid)。

1. 右上の「**[!UICONTROL Sign In]**」をクリックします。

   [Adobeのログインプロセス ](https://helpx.adobe.com/jp/manage-account/using/access-adobe-id-account.html) を順を追って新しいブラウザーウィンドウが表示されます。

   ログインプロセスが完了すると、検索結果に、ライセンス済みの画像の状態がラベルとして表示されます。

   ![Adobeへのログイン ](./assets/adobe-stock-account-login.png){width="600" zoomable="yes"}

### 検索結果のライセンス済み状態の表示

[Adobe アカウントにログインします ](#log-in-to-your-adobe-account)。

Adobe アカウントに関連付けられているライセンス済み画像にはすべてラベルが表示され、ライセンスを取得した画像が明確になります。

![ ライセンス取得済み画像のAdobe Stock検索結果 ](./assets/adobe-stock-licensed-images.png){width="600" zoomable="yes"}

### 画像をメディアストレージに保存

Adobe Stock統合を使用して検索された画像を [!DNL Commerce] [ メディアストレージ ](media-storage.md) に保存して、[!DNL Commerce] ストア全体で簡単に再利用できます。

2 種類の画像を保存できます。[ 画像プレビュー ](adobe-stock-save-preview.md) または [ ライセンス取得済み画像 ](adobe-stock-license-image.md) です。

#### 画像プレビューを保存

画像プレビューは、Adobe Stock アセットに透かしを入れたものです。 画像プレビューは無料で、特定の画像用のライセンスを購入して実稼動ストアで使用する前に、様々な画像を試すのに良い方法です。

1. [Adobe Stock検索グリッドへのアクセス ](#access-the-adobe-stock-search-grid)。

1. [ 画像の詳細を表示 ](#view-image-details) するには、検索グリッドで画像をクリックします。

1. 「**[!UICONTROL Save Preview]**」をクリックします。

   この操作を実行すると、イメージをメディア ストレージに保存するために使用するファイル名を指定するようプロンプトが表示されます。 デフォルトのファイル名が提供されますが、この名前は好みに合わせてカスタマイズできます。

   ![Adobe Stockのプレビュー画像を保存 ](./assets/adobe-stock-save-preview.png){width="500" zoomable="yes"}

1. 「**[!UICONTROL Confirm]**」をクリックします。

   ページがメディアストレージにリダイレクトされ、保存されたプレビューが表示されます。

#### ライセンス取得済み画像の保存

実稼動 [!DNL Commerce] ードストアに使用するAdobe Stock アセットには、ライセンスを付与する必要があります。 ライセンスを取得すると、画像への法的アクセスが確保され、すべての [ 画像プレビュー ](adobe-stock-save-preview.md) に存在するAdobe Stockの透かしが排除されます。 画像のライセンスを取得したり、既にライセンスを取得している画像を保存したりするには、Adobe アカウントにログインする必要があります。

1. [Adobe アカウントにログインします ](#log-in-to-your-adobe-account)。

1. [ 画像の詳細を表示 ](#view-image-details) するには、検索グリッドで画像をクリックします。

1. イメージの現在のライセンス ステータスに応じて、次のいずれかの操作を行います。

   - 画像がライセンス済みの場合は、「**[!UICONTROL Save]**」をクリックします。

   - 画像がライセンス済み _ない_ 場合は、「**[!UICONTROL License and Save]**」をクリックします。

     >[!NOTE]
     >
     >画像のライセンスを取得するには、アカウントで利用可能な [&#128279;](https://helpx.adobe.com/jp/stock/help/credit-packs.html)0&rbrace;Adobe Stock クレジット &rbrace; が必要です。

   この操作を実行すると、イメージを [ メディア ストレージ ](media-storage.md) に保存するために使用するファイル名を指定するよう求めるメッセージが表示されます。 デフォルトのファイル名が提供されますが、この名前は好みに合わせてカスタマイズできます。

1. 「**[!UICONTROL Confirm]**」をクリックします。

   ページがメディアストレージにリダイレクトされ、保存されたプレビューが表示されます。
