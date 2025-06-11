---
title: ページ設定
description: ストアページのメイン部分のデフォルトを設定する方法を説明します。
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# ページ設定

ページの主要なセクションは、一部は一連の標準HTML タグによって制御されます。 これらのタグの一部は、ページの各セクションで使用されるフォント、カラー、サイズ、背景色および画像の選択を決定するために使用できます。 その他の設定は、ヘッダーのロゴやフッターの著作権表示などのページ要素を制御します。 これらのセクションは、HTMLページの基盤となる構造に対応しており、多くの基本的なプロパティは管理者で設定できます。

- [HTMLヘッド](#html-head)
- [ヘッダー](#header)
- [フッター](#footer)

![HTMLページセクション ](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTMLヘッド

「HTML Head」セクションの設定は、HTML ページの `<head>` タグに対応し、各ストアビューに対して設定できます。 このセクションには、ページタイトル、説明およびキーワードのメタデータに加えて、favicon およびその他のスクリプトへのリンクが含まれています。 検索エンジンロボットの手順とストアデモ通知の表示についても、この節で設定します。

### HTML ヘッドの設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 設定するストア表示を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. _その他の設定_ の下で、「**[!UICONTROL HTML Head]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

   ![HTML Head の設定 ](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. 必要に応じて [favicon](../getting-started/storefront-branding.md#add-a-favicon) を更新します。

1. 必要に応じて、ページタイトル設定を更新します。

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   サフィックスやプレフィックスをデフォルトのタイトルと共に使用して、2 つまたは 3 つの部分から成るタイトルを作成できます。 接頭辞または接尾辞とデフォルトのタイトルの間の区切り文字として、縦棒またはコロンを追加できます。

1. 検索エンジン最適化（SEO）をサポートし、検索結果から顧客をストアに誘導するのに役立つメタデータを追加または変更します。

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. 必要に応じて **[!UICONTROL Scripts and Style Sheets]** を入力します。

   >[!NOTE]
   >
   >「[!UICONTROL Scripts and Style Sheets]」フィールドに入力するJavaScriptは、コンテンツセキュリティポリシー（CSP）設定で許可リストに登録する必要があります。登録しない場合、チェックアウトページでは実行されません。 詳しくは、[ コンテンツセキュリティポリシー ](https://developer.adobe.com/commerce/php/development/security/content-security-policies) を参照してください。


1. 必要に応じて、[demo store notice](../getting-started/storefront-branding.md#set-the-store-demo-notice) を有効または無効にします。

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

### HTMLの「見出し」フィールドの説明

| フィールド | 対象範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | ストア表示 | ブラウザーのアドレスバーとタブに表示される小さなグラフィック画像をアップロードします。 許可されるファイルタイプ：ICO、PNG、APNG、GIF、JPG（JPEG）。 すべてのブラウザーがこれらの形式をサポートしているわけではありません。 |
| [!UICONTROL Default Page Title] | ストア表示 | ブラウザーで表示された際に各ページのタイトルバーに表示されるタイトル。 個々のページに別のタイトルを指定しない限り、デフォルトのタイトルはすべてのページに使用されます。 |
| [!UICONTROL Page Title Prefix] | ストア表示 | タイトルの前にプレフィックスを追加して、2 つまたは 3 つの部分から成るタイトルを作成できます。 メインタイトルのテキストと区別するために、プリフィックスの末尾に縦棒またはコロンを区切り文字として使用することができます。 |
| [!UICONTROL Page Title Suffix] | ストア表示 | タイトルの後にサフィックスを追加して、2 つまたは 3 つの部分のタイトルを作成できます。 メインタイトルのテキストと区別するために、プリフィックスの末尾に縦棒またはコロンを区切り文字として使用することができます。 |
| [!UICONTROL Default Meta Description] | ストア表示 | 説明には、検索エンジンの一覧用にサイトの概要が記載されています。160 文字以下にする必要があります。 |
| [!UICONTROL Default Meta Keywords] | ストア表示 | ストアを説明する一連のキーワード。各キーワードはコンマで区切ります。 |
| [!UICONTROL Scripts and Style Sheets] | ストア表示 | 終了 `<head>` タグの前にHTMLに含める必要があるスクリプトが含まれます。 例えば、`<body>` タグの前に配置する必要があるサードパーティのJavaScriptは、ここに入力できます。 |
| [!UICONTROL Display Demo Store Notice] | ストア表示 | ページ上部でのデモストア通知の表示を制御します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## ヘッダー

ヘッダー設定は、ストアのロゴのパスを識別し、ロゴの代替テキストとようこそメッセージを指定します。

![ ヘッダー設定 ](./assets/configuration-header.png){width="400" zoomable="yes"}

### ヘッダーの設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 設定するストア表示を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. _その他の設定_ の下で、「**[!UICONTROL Header]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. ストア表示に必要な変更を加えます。

   - [ ロゴ ](../getting-started/storefront-branding.md#upload-your-logo) 設定
   - [ ようこそメッセージ ](../getting-started/storefront-branding.md#change-the-welcome-message) 設定

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

### ヘッダーフィールドの説明

| フィールド | 対象範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Logo Image] | ストア表示 | ヘッダーに表示されるロゴへのパスを識別します。 サポートされているファイルタイプ：PNG、GIF、JPG（JPEG） |
| [!UICONTROL Logo Attribute Width] | ストア表示 | ロゴ画像の幅（ピクセル単位）。 |
| [!UICONTROL Logo Attribute Height] | ストア表示 | ロゴ画像の高さ（ピクセル単位）。 |
| [!UICONTROL Welcome Text] | ストア表示 | ウェルカムメッセージはページのヘッダーに表示され、ログインした顧客の名前が含まれます。 |
| [!UICONTROL Logo Image Alt] | ストア表示 | ロゴに関連付けられている代替テキストです。 |
| [!UICONTROL Translate Title] | ストア表示 | `Page Title` または `Meta Title` を翻訳する必要があるかどうかを決定します。 |

{style="table-layout:auto"}

## フッター

フッター設定セクションでは、ページの下部に表示される [ 著作権表示 ](../getting-started/storefront-branding.md#change-the-copyright-notice) を更新したり、終了 `<body>` タグの前に配置しなければならないその他のスクリプトを入力したりできます。

![ フッター設定 ](./assets/configuration-footer.png){width="400" zoomable="yes"}

### フッターの設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 設定するストア表示を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. _その他の設定_ の下で、「**[!UICONTROL Footer]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. **[!UICONTROL Copyright]** と **[!UICONTROL Miscellaneous HTML]** の設定に対して必要な変更を加えます。

   >[!NOTE]
   >
   >「[!UICONTROL Miscellaneous HTML]」フィールドに入力するJavaScriptは、コンテンツセキュリティポリシー（CSP）設定で許可リストに登録する必要があります。登録しない場合、チェックアウトページでは実行されません。 詳しくは、[ コンテンツセキュリティポリシー ](https://developer.adobe.com/commerce/php/development/security/content-security-policies) を参照してください。

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。

## フッターフィールドの説明

| フィールド | 対象範囲 | 説明 |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | ストア表示 | 終了 `<body>` タグの直前に配置する必要があるその他のスクリプトをサーバーにアップロードできる入力ボックス。 |
| [!UICONTROL Copyright] | ストア表示 | 各ページの下部に表示される著作権情報。 著作権記号を含めるには、次のようにHTMLのキャラクターエンティティ `\&copy;` を使用します。`\&copy; 2021 Commerce Demo Store. All Rights Reserved.` 必ず、サンプルの著作権表示を独自の表示に置き換えてください。 |
| [!UICONTROL Display Report Bugs Link] | ストア表示 | バグ報告のリンク （一部のテーマでサポートされています）が有効になっているか無効になっているかを判断します。 |

{style="table-layout:auto"}
