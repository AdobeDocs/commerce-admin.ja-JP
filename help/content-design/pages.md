---
title: ページ
description: ' [!DNL Commerce] demo ストアに含まれているコアコンテンツページと、デフォルトページ設定の変更について詳しく説明します。'
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# ページ

コンテンツは、店舗のあらゆる製品と同様に、賞味期限の観点から表示できます。 ソーシャルメディアのコンテンツの有効期限が 24 時間未満であることをご存知ですか？ 作成するコンテンツの有効期限の可能性は、リソースを投資する場所を決定するのに役立ちます。

保存期限が長いコンテンツは、_エバーグリーンコンテンツ_ と呼ばれることもあります。 エバーグリーンコンテンツの例としては、カスタマーサクセスストーリー、_ハウツー_ 説明、よくある質問（FAQ）などがあります。 これに対し、生鮮食品のコンテンツには、イベント、業界ニュース、プレスリリースなどが含まれます。

![ サンプル Luma ストアに含まれている会社概要ページ ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## コアコンテンツページ

[!DNL Commerce] デモストアには、開始に役立つコアコンテンツページの例が含まれています。 これらのページはすべて、ニーズに合わせて変更できます。 ストア内の次のページを見て、コンテンツがメッセージ、音声、ブランドを伝えていることを確認します。

### ホーム

デモ [ ホーム ](../getting-started/storefront.md#home-page) ページには、バナー、画像カルーセル、リンク付きの静的ブロック、新製品のリストが含まれています。

### プライバシーポリシー

ストア [ プライバシーポリシー ](../getting-started/privacy-policy.md) ページは、独自の情報で更新する必要があります。 ベストプラクティスとして、プライバシーポリシーは、会社が収集する情報の種類とその使用方法を顧客に説明する必要があります。

### 404 が見つかりません

404 Page Not Found ページは、ページが見つからないときに返される応答コードに対して命名されます。 URL リダイレクトを使用すると、このページが表示される回数が減ります。 ただし、必要な場合は、この機会を利用して、顧客が興味を持つ可能性のある製品へのリンクを提供する方がよいでしょう。

### アクセス拒否

{{b2b-feature}}

[ アクセス拒否 ](../b2b/account-company-roles-permissions.md) ページは、会社のユーザーに割り当てられた権限でページへのアクセスが許可されていない場合に表示されます。

### Cookie を有効にする

[Cookie を有効にする ](../getting-started/compliance-cookie-law.md) ページは、サイトの訪問者がブラウザーで cookie を有効にしていない場合に表示されます。 このページでは、最も一般的なブラウザーで cookie を有効にする手順を、イラストを使って順を追って説明します。

### サービスを利用できません

[503 Service Unavailable](../configuration-reference/general/general.md) ページの名前は、サーバーが使用できないときに返される応答コードに対応しています。

### 会社情報

「会社概要」ページは、ストアのフッターからリンクされています。 画像、ビデオ、プレスリリースおよびアナウンスへのリンクを含めることができます。 サンプルページの右側に画像があり、ページの終わりを示す装飾画像があります。

### 顧客サービス

Customer Service ページは、ページ階層内の別のノードです。 ページ上の 2 つのヘッダーには、顧客がヘッダーをクリックした場合にのみ表示されるコンテンツがあります。

![ ストアフロントのカスタマーサービスページ ](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## デフォルトページの設定

_デフォルトページ_ の設定によって、[ ベース URL](../stores-purchase/store-urls.md) および対応するホームページに関連付けられるランディングページが決まります。 また、_ページが見つかりません_ エラーが発生した場合や、各ページの上部に [ パンくずリスト ](../catalog/navigation-breadcrumb-trail.md) が表示された場合に表示されるページも決定します。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. _[!UICONTROL General]_の下の左パネルで、「**[!UICONTROL Web]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Default Pages]**」セクションを展開します。

   ![ デフォルトページ ](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | フィールド | [ 範囲 ](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | ストア表示 | ベース URL に関連付けられているランディングページを示します。 デフォルトでは、このフィールドは `cms` に設定されており、[!DNL Commerce] コンテンツ管理システムからのページを示します。 また、ブログなど、別のタイプのランディングページを使用することもできます。 例えば、`magento/blog` にサーバーにブログがインストールされている場合、選択したページへの相対パスとして `blog` というフォルダー名を入力できます。 |
   | [!UICONTROL CMS Home Page] | ストア表示 | ストアのホームページを選択するには、リストから CMS ページを選択するだけです。 デフォルトでは、CMS のホームページには、ストアで使用可能な CMS ページの選択全体が一覧表示されます。 |
   | [!UICONTROL Default No-route URL] | ストア表示 | `404 Page not Found` エラーが発生したときに表示されるデフォルトのページの URL が含まれます。 デフォルト値は `cms/noroute/index` です。 |
   | [!UICONTROL CMS No Route Page] | ストア表示 | 404 ページが見つからないというエラーが発生した場合に表示する特定の CMS ページを識別します。 デフォルトページは `404 Not Found` です。 |
   | [!UICONTROL CMS No Cookies Page] | ストア表示 | ブラウザーで Cookie が有効になっていない場合に表示される特定の CMS ページを識別します。 このページでは、cookie が使用される理由と、各ブラウザーで cookie を有効にする方法について説明します。 デフォルトページは `Enable Cookies` です。 |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | ストア表示 | カタログ内のすべての CMS ページにパンくずリストを表示するかどうかを決定します。 オプション：`Yes` / `No` |

   {style="table-layout:auto"}

1. **[!UICONTROL Default Web URL]**：ランディングページを含む [!DNL Commerce] インストールのフォルダーの相対パスを入力します。

   デフォルト設定 `cms` は、[!DNL Commerce] コンテンツ管理システムからのページを示します。

   >[!NOTE]
   >
   >特定のストア表示の場合は、_[!UICONTROL Default Web URL]_の横にある「**[!UICONTROL Use Default]**」チェックボックスをオフにし、その他の変更するデフォルト設定をオフにします。

1. ホームページとして使用する CMS ページに **[!UICONTROL CMS Home Page]** を設定します。 次のように、その他に作成されたページがホームページとして使用される場合があります。

   - 限定オンラインストアへようこそ
   - 報酬ポイント
   - 会社情報
   - 顧客サービス
   - Cookie を有効にする
   - プライバシーポリシー
   - 会社：アクセスが拒否されました

1. **[!UICONTROL Default No-route URL]**: _404 Page Not Found_ エラーが発生した場合にページがリダイレクトされる [!DNL Commerce] インストールのフォルダーの相対パスを入力します。

   デフォルト値は `cms/index/noRoute` です。

1. _404 Page Not Found_ エラーが発生した場合に表示される CMS ページに **[!UICONTROL CMS No Route Page]** を設定します。

1. ブラウザーで Cookie が無効になっている場合に表示される CMS ページに **[!UICONTROL CMS No Cookies Page]** を設定します。 このページでは、cookie が使用される理由と、各ブラウザーで cookie を有効にする方法について説明します。 デフォルトページは `Enable Cookies` です。

1. パンくずリストをすべての CMS ページの上部に表示する場合は、**[!UICONTROL Show Breadcrumbs for CMS Pages]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
