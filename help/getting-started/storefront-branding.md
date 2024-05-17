---
title: ストアフロントのブランディング
description: ストアのブランドアイデンティティを定義する要素の変更について説明します。
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# ストアフロントのブランディング

最初にあなたがやりたいことの 1 つは次のとおりです [ロゴの変更](#upload-your-logo) ヘッダー内および [お気に入りのアップロード](#add-a-favicon) ブラウザーの場合。 次に、以下を行います [ようこそメッセージを追加](#change-the-welcome-message) および [著作権表示の更新](#change-the-copyright-notice) フッターで。 これらのタスクは、すぐに対処できるシンプルなデザイン要素です。 ストアが開発中の間に、次の操作を実行できます [デモの保存に関する通知を表示](#set-the-store-demo-notice)を選択し、起動する準備が整ったら削除します。

![ストアフロントブランディング要素](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## ロゴをアップロード

ヘッダー内のロゴのサイズと場所は、ストアテーマによって決まります。 ロゴは、GIF、PNG またはJPG（JPEG）ファイルタイプとして保存し、ストアの管理者からアップロードできます。

![ヘッダー内のロゴ](./assets/storefront-header-logo.png){width="600"}

ロゴ画像はサーバー上の次の場所にあります。 という名前の任意の画像ファイル `logo.svg` は、デフォルトのテーマロゴとして使用されます。

フルパス - `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

相対パス -  `images/logo.svg`

テーマで使用されるロゴやその他の画像のサイズがわからない場合は、ブラウザーでページを開き、画像を右クリックして、要素を調べます。

>[!NOTE]
>
>ヘッダーのロゴに加えて、のロゴも表示されます [メールテンプレート](../systems/email-templates.md#prepare-your-email-logo) およびに [PDF請求書](../stores-purchase/sales-documents.md) およびその他の営業文書 メールテンプレートと請求書に使用されるロゴは、サイズの要件が異なり、別々にアップロードする必要があります。

サポートされるロゴファイル形式：

| ファイル形式 | 説明 |
|--- |--- |
| PNG | （Portable Network Graphics） GIFフォーマットに代わるこの新しいフォーマットは、最大 1600 万色（24 ビット）をサポートします。 可逆圧縮形式では、テキストは鮮明になるが、一部の形式よりもファイルサイズが大きい、高品質のビットマップ画像が生成されます。 PNG 形式は、透明レイヤーをサポートし、オンライン表示とストリーミング用に設計されています。 |
| GIF | （Graphics Interchange Format）広くサポートされている古いビットマップ形式で、256 色（8 ビット）に制限されています。 GIFフォーマットは、単純なアニメーションと透明レイヤーをサポートしています。 |
| JPG（JPEG） | （Joint Photographic Expert Group）ほとんどのデジタルカメラで使用される圧縮ビットマップ形式。 非可逆圧縮によってデータがやや失われますが、テキストのぼやけた点として目立つ場合があります。 |

{style="table-layout:auto"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![デザイン設定ページ](./assets/design-configuration.png){width="700"}

1. 設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Header]** セクション。

   ![ヘッダー設定](./assets/configuration-header.png){width="600"}

1. 新しいロゴをアップロードするには、をクリックします **[!UICONTROL Upload]** そして、システムからファイルを選択します。

1. を入力 **[!UICONTROL Logo Image Width]** および **[!UICONTROL Logo Image Height]** ピクセル単位。

1. の場合 **[!UICONTROL Logo Image Alt]**&#x200B;で、画像の上にマウスポインターが置かれたときに表示されるテキストを入力します。

1. 完了したら、 **[!UICONTROL Save Configuration]**.

## お気に入りの追加

_Favicon_ を短くする _お気に入りのアイコン_ 各ブラウザーページのタブにある小さなアイコンを指します。 ブラウザーによっては、favicon がアドレスバーの URL の直前にも表示されます。

favicon は通常、16 x 16 ピクセルまたは 32 x 32 ピクセルのサイズです。 [!DNL Commerce] は ICO、PNG、APNG、GIF、JPG（JPEG）のファイルタイプを受け入れますが、すべてのブラウザーがこれらのフォーマットをサポートしているわけではありません。 favicon で最も広くサポートされているファイル形式は ICO です。 他の画像ファイルタイプを使用することもできますが、一部のブラウザーではその形式がサポートされていない場合があります。 ICO 画像を生成したり、画像をその形式に変換したりできる無料のツールがオンラインで多数用意されています。

![ブラウザータブの Favicon](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] では、favicon として以下のファイル形式がサポートされています。

| ファイル形式 | 説明 |
|--- |--- |
| ICO | この画像ファイル形式は、小さいサイズのコンピューターアイコン画像用に設計されています。 主にMicrosoft® Windows OS で使用される ICO フォーマットは、最大 256 x 256 ピクセルと 8 ビットの透明度を持つ 1600 万色（24 ビット）の画像を含めることができます。 |
| PNG | （Portable Network Graphics） GIFフォーマットに代わるこの新しいフォーマットは、最大 1600 万色（24 ビット）をサポートします。 可逆圧縮形式では、テキストは鮮明になるが、一部の形式よりもファイルサイズが大きい、高品質のビットマップ画像が生成されます。 PNG 形式は、透明レイヤーをサポートし、オンライン表示とストリーミング用に設計されています。 |
| APNG | （Animated Portable Network Graphics）単純なアニメーションをサポートする PNG に似たファイル形式。 |
| GIF | （Graphics Interchange Format）広くサポートされている古いビットマップ形式で、256 色（8 ビット）に制限されています。 GIFフォーマットは、単純なアニメーションと透明レイヤーをサポートしています。 |
| JPG（JPEG） | （Joint Photographic Expert Group）ほとんどのデジタルカメラで使用される圧縮ビットマップ形式。 非可逆圧縮によってデータがやや失われますが、テキストのぼやけた点として目立つ場合があります。 |

{style="table-layout:auto"}

### 手順 1:favicon の作成

1. 任意の画像エディターを使用して、ロゴの 16 x 16 または 32 x 32 のグラフィック画像を作成します。

1. （オプション）使用可能なオンラインツールのいずれかを使用して、ファイルを.ico 形式に変換し、コンピューターに保存します。

### 手順 2:favicon をストアにアップロードする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _[!UICONTROL Other Settings]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL HTML Head]**セクション。

   ![HTMLヘッドの設定](./assets/configuration-html-head.png){width="600"}

1. 現在の favicon を削除するには、 _削除_ （![ごみ箱アイコン](../assets/icon-delete-trashcan.png)）アイコンをクリックします。

1. クリック **[!UICONTROL Upload]** 準備した favicon ファイルを開きます。

   ![Uploaded favicon](./assets/favicon-upload.png){width="400"}

1. 完了したら、 **[!UICONTROL Save Configuration]**.

### 手順 3：キャッシュを更新

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** ワークスペースの上部にあるメッセージのリンク。

1. リストで、 **[!UICONTROL Page Cache]** マークされているチェックボックス `Invalidated`.

1. を設定 **[!UICONTROL Actions]** 対象： `Refresh` をクリックして、 **[!UICONTROL Submit]**.

1. 新しいお気に入りを表示するには、ストアフロントに戻ってブラウザーを更新します。

## ようこそメッセージの変更

ヘッダーのウェルカムメッセージが展開され、ログインした顧客の名前が表示されます。 ストアを起動する前に、必ずデフォルトを変更してください _ようこそ_ 各ストア表示のテキスト。

![ようこそメッセージ](./assets/storefront-welcome-message.png){width="600"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _[!UICONTROL Other Settings]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL Header]**セクション。

1. の場合 **[!UICONTROL Welcome Text]**&#x200B;で、ストアのヘッダーに表示するようこそメッセージのテキストを入力します。

   ![ヘッダー設定](./assets/configuration-header.png){width="600"}

1. 完了したら、 **[!UICONTROL Save Configuration]**.

1. ページキャッシュを更新するよう求められたら、 **[!UICONTROL Cache Management]** ワークスペースの上部にあるリンクをクリックし、指示に従ってキャッシュを更新します。

## 著作権表示の変更

ストアの各ページのフッターには著作権表示が表示されます。 ベストプラクティスとして、著作権表示には現在の年を含め、自社をサイト上のコンテンツの法的所有者として識別する必要があります。

![著作権表示の例](./assets/storefront-footer-copyright.png){width="600"}

この `&copy;` 文字コードは、次の例に示すように、著作権記号を挿入するために使用されます。

- 長い形式の例

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- 短い形式の例

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_著作権表示を更新するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _その他の設定_、を展開 ![展開セレクター](../assets/icon-display-expand.png)この **[!UICONTROL Footer]** セクション。

   ![フッターデザイン設定](./assets/configuration-footer.png){width="600"}

1. の場合 **[!UICONTROL Copyright]**&#x200B;を選択し、各ページのフッターに表示する著作権表示を入力します。

   の使用 `&copy;` 著作権記号を挿入するための文字コード。

1. 完了したら、 **[!UICONTROL Save Configuration]**.

## デモ用ストア通知の設定

店舗がオンラインでも建設中の場合は、ページの上部に店舗デモ通知を表示して、店舗がまだ営業していないことを知らせることができます。 準備ができたら _運用開始_&#x200B;メッセージを削除するだけです。 窓にぶら下がっている看板を反転させることに似ています _クローズ_ 対象： _開く_. デモ通知の形式は、ストアのテーマによって決まります。

![ストアフロントデモのお知らせ](./assets/storefront-demo-notice.png){width="600"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. グリッドで、設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _[!UICONTROL Other Settings]_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この&#x200B;**[!UICONTROL HTML Head]**セクション。

   ![HTMLヘッド](./assets/configuration-html-head.png){width="600"}

1. 一番下までスクロールし、 **[!UICONTROL Display Demo Store Notice]** ご希望に合わせてください。

1. 完了したら、 **[!UICONTROL Save Configuration]**.

1. キャッシュの更新を求めるメッセージが表示されたら、 **[!UICONTROL Cache Management]** システムメッセージで、手順に従ってキャッシュを更新します。
