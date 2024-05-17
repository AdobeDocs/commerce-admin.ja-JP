---
title: ページ設定
description: ストアページのメイン部分のデフォルトを設定する方法を説明します。
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 0%

---

# ページ設定

ページのメインセクションは、その一部が一連の標準HTMLタグによって制御されます。 これらのタグの一部は、ページの各セクションで使用されるフォント、カラー、サイズ、背景色および画像の選択を決定するために使用できます。 その他の設定は、ヘッダーのロゴやフッターの著作権表示などのページ要素を制御します。 これらのセクションは、HTMLページの基盤となる構造に対応しており、多くの基本的なプロパティは管理者から設定できます。

- [HTMLヘッド](#html-head)
- [ヘッダー](#header)
- [フッター](#footer)

![HTMLページセクション](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTMLヘッド

「HTMLヘッド」セクションの設定は、 `<head>` HTMLページのタグで、ストア表示ごとに設定できます。 このセクションには、ページタイトル、説明およびキーワードのメタデータに加えて、favicon およびその他のスクリプトへのリンクが含まれています。 検索エンジンロボットの手順とストアデモ通知の表示についても、この節で設定します。

### HTMLヘッドの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _その他の設定_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL HTML Head]** セクション。

   ![HTMLヘッドの設定](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. を更新 [favicon](../getting-started/storefront-branding.md#add-a-favicon) 必要に応じて、

1. 必要に応じて、ページタイトル設定を更新します。

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   サフィックスやプレフィックスをデフォルトのタイトルと共に使用して、2 つまたは 3 つの部分から成るタイトルを作成できます。 接頭辞または接尾辞とデフォルトのタイトルの間の区切り文字として、縦棒またはコロンを追加できます。

1. 検索エンジン最適化（SEO）をサポートし、検索結果から顧客をストアに誘導するのに役立つメタデータを追加または変更します。

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. 次のいずれかを入力 **[!UICONTROL Scripts and Style Sheets]** 必要に応じて。

1. を有効または無効にする [デモストアのお知らせ](../getting-started/storefront-branding.md#set-the-store-demo-notice) 必要に応じて、

1. 完了したら、 **[!UICONTROL Save Configuration]**.

### HTML見出しフィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | ストア表示 | ブラウザーのアドレスバーとタブに表示される小さなグラフィック画像をアップロードします。 許可されるファイルタイプ：ICO、PNG、APNG、GIF、JPG（JPEG）。 すべてのブラウザーがこれらの形式をサポートしているわけではありません。 |
| [!UICONTROL Default Page Title] | ストア表示 | ブラウザーで表示された際に各ページのタイトルバーに表示されるタイトル。 個々のページに別のタイトルを指定しない限り、デフォルトのタイトルはすべてのページに使用されます。 |
| [!UICONTROL Page Title Prefix] | ストア表示 | タイトルの前にプレフィックスを追加して、2 つまたは 3 つの部分から成るタイトルを作成できます。 メインタイトルのテキストと区別するために、プリフィックスの末尾に縦棒またはコロンを区切り文字として使用することができます。 |
| [!UICONTROL Page Title Suffix] | ストア表示 | タイトルの後にサフィックスを追加して、2 つまたは 3 つの部分のタイトルを作成できます。 メインタイトルのテキストと区別するために、プリフィックスの末尾に縦棒またはコロンを区切り文字として使用することができます。 |
| [!UICONTROL Default Meta Description] | ストア表示 | 説明には、検索エンジンの一覧用にサイトの概要が記載されています。160 文字以下にする必要があります。 |
| [!UICONTROL Default Meta Keywords] | ストア表示 | ストアを説明する一連のキーワード。各キーワードはコンマで区切ります。 |
| [!UICONTROL Scripts and Style Sheets] | ストア表示 | 終了する前にHTMLに含める必要があるスクリプトが含まれます `<head>` タグ。 例えば、以下より前に配置する必要があるサードパーティ JavaScript です。 `<body>` タグはここで入力できます。 |
| [!UICONTROL Display Demo Store Notice] | ストア表示 | ページ上部でのデモストア通知の表示を制御します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## ヘッダー

ヘッダー設定は、ストアのロゴのパスを識別し、ロゴの代替テキストとようこそメッセージを指定します。

![ヘッダー設定](./assets/configuration-header.png){width="400" zoomable="yes"}

### ヘッダーの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _その他の設定_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Header]** セクション。

1. ストア表示に必要な変更を加えます。

   - [ロゴ](../getting-started/storefront-branding.md#upload-your-logo) 設定
   - [ようこそメッセージ](../getting-started/storefront-branding.md#change-the-welcome-message) 設定

1. 完了したら、 **[!UICONTROL Save Configuration]**.

### ヘッダーフィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Logo Image] | ストア表示 | ヘッダーに表示されるロゴへのパスを識別します。 サポートされているファイルタイプ：PNG、GIF、JPG（JPEG） |
| [!UICONTROL Logo Attribute Width] | ストア表示 | ロゴ画像の幅（ピクセル単位）。 |
| [!UICONTROL Logo Attribute Height] | ストア表示 | ロゴ画像の高さ（ピクセル単位）。 |
| [!UICONTROL Welcome Text] | ストア表示 | ウェルカムメッセージはページのヘッダーに表示され、ログインした顧客の名前が含まれます。 |
| [!UICONTROL Logo Image Alt] | ストア表示 | ロゴに関連付けられている代替テキストです。 |
| [!UICONTROL Translate Title] | ストア表示 | 次のかどうかを判断します `Page Title` または `Meta Title` 翻訳する必要があります。 |

{style="table-layout:auto"}

## フッター

フッター設定セクションでは、を更新できます [著作権表示](../getting-started/storefront-branding.md#change-the-copyright-notice) ページの下部に表示され、終了する前に配置する必要があるその他のスクリプトを入力します `<body>` タグ。

![フッター設定](./assets/configuration-footer.png){width="400" zoomable="yes"}

### フッターの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 設定するストア表示を見つけて、クリックします **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 次の下 _その他の設定_、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Footer]** セクション。

1. に必要な変更を加えます **[!UICONTROL Copyright]** および **[!UICONTROL Miscellaneous HTML]** 設定。

1. 完了したら、 **[!UICONTROL Save Configuration]**.

## フッターフィールドの説明

| フィールド | 範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | ストア表示 | 終了する直前に配置する必要があるその他のスクリプトをサーバーにアップロードできる入力ボックス `<body>` タグ。 |
| [!UICONTROL Copyright] | ストア表示 | 各ページの下部に表示される著作権情報。 著作権記号を含めるには、HTML文字エンティティを使用します `\&copy;` 例えば、次のようになります。 `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` サンプルの著作権表示は必ず独自のものに置き換えてください。 |
| [!UICONTROL Display Report Bugs Link] | ストア表示 | バグ報告のリンク （一部のテーマでサポートされています）が有効になっているか無効になっているかを判断します。 |

{style="table-layout:auto"}
