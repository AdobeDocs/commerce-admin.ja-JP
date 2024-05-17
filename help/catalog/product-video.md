---
title: 製品ビデオを追加
description: Google アカウントからのYouTube Data API キーが必要なストアの商品ビデオを設定し、商品のビデオリンクを追加する方法を説明します。
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# 製品ビデオを追加

商品ビデオを追加するには、まずGoogle アカウントから API キーを取得し、ストアの設定に入力する必要があります。 次に、製品からビデオにリンクできます。

## 手順 1:YouTube API キーの取得

1. Google アカウントにログインし、 [Google開発者コンソール][1].

1. 上部の検索フィールドに、 `YouTube Data API v3` 検索アイコンをクリックします。

1. API ページが表示されたら、有効になっていることを確認します。

1. 左パネルで、を選択します。 **[!UICONTROL Credentials]**.

1. 資格情報があるかどうかに応じて、次のいずれかの操作を行います。

   - 必要な資格情報が既にある場合は、キーを _API キー_ テーブル。

   - この API に対する認証情報がまだない場合は、 **[!UICONTROL Create Credentials]**  上部で、画面の指示に従って必要な資格情報を作成します。 次の下 _資格情報を取得_&#x200B;を入力し、API キーをコピーして、 **[!UICONTROL Done]**.

1. API キーをクリップボードにコピーします。

1. 右側の「編集」アイコンをクリックし、API キーが正しいリファラーに制限されていることを確認するように制限を設定します。

1. キーが生成されるまでしばらく待ってから、キーをクリップボードにコピーします。

   次の手順で、ストアの設定にキーを貼り付けます。

## 手順 2:Commerceでのキーの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この _[!UICONTROL Product Video]_「」セクションを選択して、**[!UICONTROL YouTube API key]**.

   ![製品ビデオの設定](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、キャッシュを更新します。

## 手順 3：ビデオへのリンク

1. 製品を編集モードで開きます。

1. スクロールして「」を展開します _[!UICONTROL Images and Videos]_セクション。

   ![画像とビデオ](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. click **[!UICONTROL Add Video]**.

   YouTube API キーをまだ設定していない場合は、 **[!UICONTROL OK]** 続行します。 YouTube ビデオにリンクすることはできませんが、手順は完了します。

1. の場合 **[!UICONTROL Url]**&#x200B;を選択し、YouTubeまたは Vimeo ビデオの URL を入力します。

   ![製品の新しいビデオ](./assets/product-video-add.png){width="600" zoomable="yes"}

1. フィールドの外側をクリックして、API キーまたはビデオのフィードバックを待ちます。

   すべてがチェックアウトされると、YouTubeはビデオの基本情報を提供します

1. を入力 **[!UICONTROL Title]** および **[!UICONTROL Description]** ビデオの

1. をアップロードするには **[!UICONTROL Preview Image]**&#x200B;画像を参照し、ファイルを選択します。

   >[!NOTE]
   >
   >アップロード後、表示されるプレビュー画像は、外部のビデオサービスプロバイダーによって自動的に生成されます。 Adobe Commerce Admin からは画像を編集できません。

1. ビデオ メタデータを使用する場合は、 **[!UICONTROL Get Video Information]**.

1. ビデオがストアでどのように使用されるかを判断するには、それぞれのチェックボックスをオンにします **[!UICONTROL Role]** 次の場合に適用されます。

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. 完了したら、 **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >次の場合 _[!UICONTROL Autostart base video]_設定オプションがに設定されています `Yes` ただし、ビデオの再生が自動的に開始されるわけではありません。ブラウザーによって適用され、Adobe Commerceで制御できない自動再生ポリシーが原因である可能性があります。 サポートされている各ブラウザーには、時間の経過と共に変化する可能性のある独自の自動再生ポリシーがあり、ビデオは今後自動再生されない可能性があります。 推奨されるベストプラクティスとして、ビジネス上の重要な機能で自動再生を使用しないでください。また、サポートされている各ブラウザーで、ストアでのビデオの自動再生動作をテストする必要があります。

## API アクセスの管理

Googleの開発者によると [利用条件]、YouTubeは、90 日以上非アクティブになっているアカウントの API アクセスを無効にすることができます。 この問題が発生すると、ビデオが表示されない場合があります。 API アクセスを最新の状態に保つには、cron ジョブを使用して、一定の間隔で API に ping を実行します。

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## フィールド参照

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL URL] | 関連付けられたビデオの URL。 |
| [!UICONTROL Title] | ビデオのタイトル。 |
| [!UICONTROL Description] | ビデオの説明。 |
| [!UICONTROL Preview Image] | ストアでビデオのプレビューとして使用される、アップロードされた画像。 |
| [!UICONTROL Get Video Information] | ホストサーバーに保存されているビデオメタデータを取得します。 元のデータを使用することも、必要に応じて更新することもできます。 |
| [!UICONTROL Role] | ストアでのプレビュー画像の使用方法を決定します。 次のオプションを任意に組み合わせて選択できます。 `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[利用条件]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
