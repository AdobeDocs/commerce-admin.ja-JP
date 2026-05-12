---
title: 製品ビデオを追加
description: Google アカウントからYouTube data API キーを必要とするストアの商品ビデオを設定し、商品のビデオリンクを追加する方法を説明します。
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: d9d964d36a7debebaed327111b5c4d76d0a1a005
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 製品ビデオを追加

商品ビデオを追加するには、まずGoogle アカウントからAPI キーを取得し、ストアのコンフィギュレーションに入力する必要があります。 次に、製品からビデオにリンクできます。

## 手順1:YouTube API キーを取得する

1. Google アカウントにログインし、[Google Developers Console](https://console.developers.google.com/)にアクセスします。

1. 上部の検索フィールドに「`YouTube Data API v3`」と入力し、検索アイコンをクリックします。

1. API ページが表示されたら、有効になっていることを確認します。

1. 左側のパネルで、**[!UICONTROL Credentials]**&#x200B;を選択します。

1. 資格情報があるかどうかに応じて、次のいずれかの操作を行います。

   - 必要な資格情報が既にある場合は、_API キー_ テーブルにキーをコピーします。

   - このAPIの資格情報をまだ持っていない場合は、上部の&#x200B;**[!UICONTROL Create Credentials]**&#x200B;をクリックし、プロンプトに従って必要な資格情報を作成します。 _資格情報を取得_&#x200B;で、API キーをコピーして&#x200B;**[!UICONTROL Done]**&#x200B;をクリックします。

1. API キーをクリップボードにコピーします。

1. 右側の編集アイコンをクリックし、制限を設定して、API キーが正しいリファラーに制限されていることを確認します。

1. キーが生成されるまでしばらく待ってから、キーをクリップボードにコピーします。

   次のステップでは、キーをストアの設定に貼り付けます。

## 手順2:Commerceでキーを設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Catalog]**」を展開し、下の「**[!UICONTROL Catalog]**」を選択します。

1. _[!UICONTROL Product Video]_&#x200B;セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL YouTube API key]**&#x200B;を貼り付けます。

   ![製品ビデオ設定](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、キャッシュを更新します。

## 手順3：ビデオへのリンク

1. 商品を編集モードで開きます。

1. にスクロールして、_[!UICONTROL Images and Videos]_&#x200B;セクションを展開します。

   ![画像とビデオ &#x200B;](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. **[!UICONTROL Add Video]**&#x200B;をクリックします。

   YouTube API キーをまだ設定していない場合は、**[!UICONTROL OK]**&#x200B;をクリックして続行します。 YouTube ビデオにリンクすることはできませんが、プロセスを実行できます。

1. **[!UICONTROL Url]**&#x200B;に、YouTubeまたはVimeo ビデオのURLを入力します。

   ![製品](./assets/product-video-add.png){width="600" zoomable="yes"}の新しいビデオ

1. フィールドの外側をクリックし、API キーまたはビデオのフィードバックを待ちます。

   チェックアウトが完了すると、YouTubeにビデオの基本情報が表示されます

1. ビデオの&#x200B;**[!UICONTROL Title]**&#x200B;と&#x200B;**[!UICONTROL Description]**&#x200B;を入力します。

1. **[!UICONTROL Preview Image]**&#x200B;をアップロードするには、画像を参照してファイルを選択します。

   >[!NOTE]
   >
   >アップロード後、表示されるプレビュー画像は、外部ビデオサービスプロバイダーによって自動的に生成されます。 Adobe Commerce管理者から画像を編集することはできません。

1. ビデオのメタデータ データを使用する場合は、**[!UICONTROL Get Video Information]**&#x200B;をクリックします。

1. ストアでのビデオの使用方法を確認するには、該当する各&#x200B;**[!UICONTROL Role]**&#x200B;のチェックボックスを選択します。

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   >[!NOTE]
   >
   >_[!UICONTROL Autostart base video]_&#x200B;コンフィギュレーションオプションが`Yes`に設定されていても、ビデオが自動的に再生されない場合は、自動再生ポリシーがブラウザーによって適用され、Adobe Commerceで制御できない可能性があります。 サポートされている各ブラウザーには独自の自動再生ポリシーがあり、時間の経過とともに変更される可能性があり、ビデオが今後自動再生されない可能性があります。 推奨されるベストプラクティスとして、ビジネスに不可欠な機能は自動再生に依存しないでください。また、サポートされている各ブラウザーで、ストア内のビデオ自動再生動作をテストする必要があります。

## ストアビューレベルでの動画の役割の管理

特定のストアビュースコープ（**[!UICONTROL All Store Views]**&#x200B;ではなく）での作業中にビデオを追加または編集すると、ビデオダイアログの各&#x200B;**[!UICONTROL Role]** オプションに&#x200B;**[!UICONTROL Use Default Value]** ボタンが表示されます。 このボタンをクリックすると、その役割のデフォルトのスコープから役割の割り当てを継承します。

![新しいビデオ – ストアビュー](./assets/product-video-add-store-scope.png){width="600" zoomable="yes"}

## API アクセスの維持

Google開発者[利用条件](https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services)によると、YouTubeは、90日以上非アクティブだったアカウントのAPI アクセスを無効にすることができます。 この問題が発生すると、ビデオが表示されない可能性があります。 API アクセスを最新の状態に保つには、cron ジョブを使用してAPIに定期的にpingを実行します。

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## フィールドリファレンス

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL URL] | 関連するビデオのURL。 |
| [!UICONTROL Title] | ビデオタイトル。 |
| [!UICONTROL Description] | ビデオの説明。 |
| [!UICONTROL Preview Image] | ストア内のビデオのプレビューとして使用されるアップロードされた画像。 |
| [!UICONTROL Get Video Information] | ホストサーバーに保存されているビデオメタデータを取得します。 元のデータを使用することも、必要に応じて更新することもできます。 |
| [!UICONTROL Role] | プレビュー画像をストアでどのように使用するかを指定します。 オプションの任意の組み合わせを選択できます：`Base Image`、`Small Image`、`Thumbnail`、`Swatch Image`、`Hide from Product Page` |

{style="table-layout:auto"}
