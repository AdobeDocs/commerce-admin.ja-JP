---
title: ページ
description: に含まれるコアコンテンツページの詳細を説明します。 [!DNL Commerce] デモストアを作成し、「デフォルトページ」設定を変更します。
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# ページ

コンテンツは、店舗内の他の製品と同様に、保存期間の観点から表示できます。 ソーシャルメディアコンテンツの保存期間が 24 時間未満であることをご存知でしたか？ 作成するコンテンツの保存期間が、リソースをどこに投資するかを決定するのに役立ちます。

保存期間が長いコンテンツは、 _常緑成分_. エバーグリーンコンテンツの例としては、顧客の成功事例、 _方法_ 手順およびよくある質問 (FAQ) を参照してください。 これに対し、自然によって損なわれやすいコンテンツには、イベント、業界のニュース、プレスリリースが含まれます。

![サンプルの Luma ストアに含まれている会社概要ページ ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## コアコンテンツページ

The [!DNL Commerce] デモストアには、使い始めるのに役立つコアコンテンツページの例が用意されています。 これらのページはすべて、ニーズに合わせて変更できます。 ストア内の次のページを見て、コンテンツがメッセージ、音声、ブランドを伝えていることを確認します。

### ホーム

デモ [ホーム](../getting-started/storefront.md#home-page) ページには、バナー、画像カルーセル、リンクを含む複数の静的ブロックおよび新製品のリストが含まれます。

### プライバシーポリシー

ストア [プライバシーポリシー](../getting-started/privacy-policy.md) ページを独自の情報で更新する必要があります。 ベストプラクティスとして、プライバシーポリシーは、会社が収集する情報の種類と使用方法を顧客に説明する必要があります。

### 404 が見つかりません

404 ページが見つからない場合に返される応答コードのページ名は、404 ページが見つからないページです。 URL リダイレクトを使用すると、このページの表示回数を減らすことができます。 ただし、必要な場合は、顧客が興味を持つ可能性のある製品へのリンクを提供する機会を活用することもできます。

### アクセス拒否

{{b2b-feature}}

The [アクセス拒否](../b2b/account-company-roles-permissions.md) ページは、会社のユーザーに割り当てられている権限がページへのアクセスを禁止した場合に表示されます。

### Cookie の有効化

The [Cookie の有効化](../getting-started/compliance-cookie-law.md) サイトの訪問者のブラウザーで cookie が有効になっていない場合に、ページが表示されます。 このページには、最頻使用ブラウザーで cookie を有効にする手順が順を追って記載されています。

### サービス利用不可

The [503 サービスを利用できません](../configuration-reference/general/general.md) サーバーが使用できない場合に返される応答コードのページ名が指定されます。

### 会社概要

会社情報ページは、ストアのフッターからリンクされています。 画像、ビデオ、プレスリリースおよびお知らせへのリンクを含めることができます。 サンプルページの右側には画像が表示され、ページの終わりを示す装飾用の画像が表示されます。

### カスタマーサービス

顧客サービスページは、ページ階層の別のノードです。 ページ上の 2 つのヘッダーには、顧客がヘッダーをクリックしたときにのみ表示されるコンテンツが含まれています。

![ストアフロントの顧客サービスページ](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## デフォルトページの設定

The _デフォルトのページ_ 設定によって、 [ベース URL](../stores-purchase/store-urls.md) と対応するホームページ。 また、 _ページが見つかりません_ エラーが発生し、 [パンくずリスト](../catalog/navigation-breadcrumb-trail.md) が各ページの上部に表示されます。

1. 次の日： _管理者_ サイドバー、移動  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default Pages]** 」セクションに入力します。

   ![デフォルトのページ](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | ストア表示 | ベース URL に関連付けられているランディングページを示します。 デフォルトでは、このフィールドはに設定されています。 `cms` ページを [!DNL Commerce] コンテンツ管理システム。 また、ブログなど、別の種類のランディングページを使用することもできます。 例えば、ブログがサーバーにインストールされている場合は、 `magento/blog`を使用する場合は、フォルダー名を入力できます `blog` を、ページの選択範囲への相対パスとして指定します。 |
   | [!UICONTROL CMS Home Page] | ストア表示 | ストアのホームページを選択するには、リストから CMS ページを選択します。 デフォルトでは、CMS のホームページには、ストアで使用可能な CMS ページの選択がすべて一覧表示されます。 |
   | [!UICONTROL Default No-route URL] | ストア表示 | デフォルトページで `404 Page not Found` エラーが発生しました。 デフォルト値は `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | ストア表示 | 「404（ページが見つかりません）」というエラーが発生した場合に表示する特定の CMS ページを識別します。 デフォルトのページは、 `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | ストア表示 | ブラウザーで cookie が有効になっていない場合に表示される特定の CMS ページを識別します。 このページでは、Cookie が使用される理由と、各ブラウザーで Cookie を有効にする方法について説明します。 デフォルトのページは、 `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | ストア表示 | カタログ内のすべての CMS ページにパンくずリストを表示するかどうかを指定します。 オプション： `Yes` / `No` |

   {style="table-layout:auto"}

1. の場合 **[!UICONTROL Default Web URL]**」に値を入力し、 [!DNL Commerce] ランディングページを含むインストール。

   デフォルト設定は、 `cms`は、 [!DNL Commerce] コンテンツ管理システム。

   >[!NOTE]
   >
   >特定のストア表示の場合は、 **[!UICONTROL Use Default]** 横のチェックボックス _[!UICONTROL Default Web URL]_、およびその他の変更するデフォルト設定。

1. 設定 **[!UICONTROL CMS Home Page]** を、ホームページとして使用する CMS ページに追加します。 作成した他のページは、次のように、ホームページとして使用できます。

   - 専用オンラインストアへようこそ
   - 報酬ポイント
   - 会社概要
   - カスタマーサービス
   - Cookie の有効化
   - プライバシーポリシー
   - 会社：アクセスが拒否されました

1. の場合 **[!UICONTROL Default No-route URL]**」に値を入力し、 [!DNL Commerce] ページがリダイレクトされるインストール。 _404 ページが見つかりません_ エラーが発生しました。

   デフォルト値は `cms/index/noRoute`.

1. 設定 **[!UICONTROL CMS No Route Page]** を CMS ページに追加します。 _404 ページが見つかりません_ エラーが発生しました。

1. 設定 **[!UICONTROL CMS No Cookies Page]** を CMS ページに追加します。 このページでは、Cookie が使用される理由と、各ブラウザーで Cookie を有効にする方法について説明します。 デフォルトのページは、 `Enable Cookies`.

1. すべての CMS ページの先頭にパンくずリストを表示する場合は、 **[!UICONTROL Show Breadcrumbs for CMS Pages]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.
