---
title: ソーシャルメディアと RSS フィード
description: ソーシャルメディアやその他の RSS フィード統合を追加して、ブランドや製品の認知度を高める方法を説明します。
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# ソーシャルメディアと RSS フィード

多くのマーチャントは、ソーシャルメディアやその他のデジタルツールを使用して、ブランドや製品の認知度を高めています。 Marketplace 拡張機能をインストールするか、コンテンツページにプラグインを追加することで、ストアをソーシャルネットワークと統合できます。 RSS フィードを使用すると、商品情報をショッピング集計サイトに発行したり、ニュースレターに含めたりできます。 お客様は RSS フィードを購読して、新製品やプロモーションについて知ることができます。

## ソーシャルネットワーク

ストアにソーシャルネットワークを接続するには、 [Marketplace 拡張機能](../getting-started/commerce-marketplace.md). また、などのソーシャルプラグインを簡単に追加できます _類似_ ストア全体のページに組み込むことができる CMS ブロックのボタンです。

ソーシャルネットワーキングサイトには、ストアに簡単に追加できる多数のプラグインがあります。 また、Commerce Marketplace上には、ストアとソーシャルメディアを統合するために使用できる多くの拡張機能があります。 次の例は、Facebookの追加方法を示しています _類似_ ボタンをストアに追加します。

>[!NOTE]
>
>Adobe Commerceによってネイティブが削除されました _Magento ソーシャル_ Facebookとの統合により、の拡張機能はサポートされなくなりました。 に移動します [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} して、Facebook統合の別の拡張機能を見つけます。

### 手順 1. ボタンコードの取得

1. Meta developers web サイトで、 [ボタン設定](https://developers.facebook.com/docs/plugins/like-button) ページ。

1. の場合 **[!UICONTROL URL to Like]**&#x200B;に、ユーザーに表示するストアのページの URL を入力します _類似_.

   例えば、ストアのホームページの URL を入力できます。

1. を選択します。 **[!UICONTROL Layout]** ボタンの場合。

1. を入力 **[!UICONTROL Width]** ボタンおよび関連するテキストメッセージに対してサイトで使用できるピクセル数。

1. を設定 **[!UICONTROL Action Type]** を次のいずれかに変更します。

   - `Like`
   - `Recommend`

1. クリック **[!UICONTROL Get Code]** 生成されたコードをクリップボードにコピーします。

### 手順 2. コンテンツブロックの作成

1. ストア管理者に戻ります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Block]**.

1. 説明を入力 **[!UICONTROL Block Title]** 内部参照用。

   例： `Facebook Like Button`.

1. 一意のを割り当て **[!UICONTROL Identifier]** ブロックに書き込みます。すべての小文字を使用し、スペースの代わりにアンダースコアを使用します。

   例： `facebook_like_button`.

1. Commerce インスタンスに複数のストア表示がある場合は、それぞれを選択します **[!UICONTROL Store View]** ブロックを使用できる場所。

1. コンテンツツールに応じて、コードスニペットをブロックコンテンツに追加します。

   - 使用時 [!DNL Page Builder]、を追加 [HTMLコード](../page-builder/html-code.md) ステージにブロックし、Facebook サイトからコピーしたコードのスニペットを貼り付けます。 それ以外の場合は、コードのスニペットをに貼り付けます。 **[!UICONTROL Content]** ボックス。

   - エディターで、Facebook サイトからコピーしたコードのスニペットを **[!UICONTROL Content]** ボックス。

1. ブロックの運用を開始する準備ができていない場合は、 **[!UICONTROL Enable Block]** 対象： `No`.

1. 完了したら、 **[!UICONTROL Save Block]**.

### 手順 3. ブロックを配置

1. コンテンツツールに応じて、ブロックを追加します。

   - 使用時 [!UICONTROL Page Builder]。手順に従います [ブロックを追加](../page-builder/block.md) ステージに移動します。

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add Widget]** 次の手順を実行します。

   - ![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能） _設定_ セクション、設定 **[!UICONTROL Type]** 対象： `CMS Static Block` をクリックして、 **[!UICONTROL Continue]**.

   - を確認します。 **[!UICONTROL Design Theme]** 現在のテーマに設定されます。

   - クリック **[!UICONTROL Continue]**.

1. が含まれる **[!UICONTROL Storefront Properties]** セクションで、次の操作を行います。

   - の場合 **[!UICONTROL Widget Title]**&#x200B;内部参照のタイトルを入力します。

   - を設定 **[!UICONTROL Assign to Store Views]** 対象： `All Store Views`または、アプリを使用するビューに追加します。 複数のビューを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   - に数値を入力してください **[!UICONTROL Sort Order]** 他のコンテンツ要素と同じページ上の場所に表示するように割り当てられているブロックの順序を決定するフィールド。 一番上の位置はゼロです。

1. が含まれる _[!UICONTROL Layout Updates]_セクションで、をクリック&#x200B;**[!UICONTROL Add Layout Update]**およびを設定&#x200B;**[!UICONTROL Display On]**ブロックを表示するカテゴリ、製品またはページに移動します。

   例えば、 `All Pages` ヘッダーまたはフッターのいずれかにブロックを配置すると、ブロックはストアのすべてのページの同じ場所に表示されます。

   特定のページにブロックを配置するには、次の手順を実行します。

   - を設定 **[!UICONTROL Display On]** 対象： `Specified Page` を選択し、 **[!UICONTROL Page]** ブロックを表示する場所。

   - を選択します。 **[!UICONTROL Block Reference]** ブロックを配置するページ上の場所を識別します。

   - のデフォルト設定を使用 **[!UICONTROL Template]**。に設定されています。 `CMS Static Block Default Template`.

   - クリック **[!UICONTROL Save and Continue Edit]**.

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block…]** そして、配置するブロックを選択します。

1. 完了したら、 **[!UICONTROL Save]**.

1. プロンプトが表示されたら、ワークスペースの上部にある手順に従って、インデックスとページキャッシュを更新します。

   ウィジェットがに表示されます。 _[!UICONTROL Widgets]_リスト。

### 手順 4. ストア内の場所の確認

ストアフロントに戻り、ブロックが正しい場所にあることを確認します。 ブロックを移動するには、別のページまたはブロック参照を試してウィジェットを再度開きます。

## RSS フィード

RSS （Really Simple Syndication）は、オンラインでの情報配信に使用される XML ベースのデータ形式です。 顧客は RSS フィードを購読して、新しい製品やプロモーションについて知ることができます。 また、RSS フィードを使用して、商品情報をショッピング集計サイトに発行したり、ニュースレターに含めることもできます。

RSS フィードを有効にすると、製品、スペシャル、カテゴリ、およびクーポンへの追加が各フィードの購読者に自動的に送信されます。 公開するすべての RSS フィードへのリンクが、ストアのフッターに表示されます。

![RSS フィードアイコン](./assets/icon-rss.png){width="100"}<br/>

RSS フィードを読み取るために必要なソフトウェアはフィード リーダーと呼ばれ、人々はヘッドライン、ブログ、ポッドキャストなどを購読できます。 Google Readerは、オンラインで無料で利用できる多くのフィードリーダーの 1 つです。

![ストアフロントの例 – RSS フィード](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### RSS フィードを設定する利点

- ストアまたはブログから最新の更新をダウンロードします
- 軽広告
- 普通株式
- SEO の向上
- 売上の増加

### RSS フィードの種類

| RSS フィード | 説明 |
|--- |--- |
| [!UICONTROL Wish List] | 有効化すると、顧客のウィッシュリストページの上部に RSS フィードリンクが表示されます。 また、ウィッシュリスト共有ページには、共有ウィッシュリストからのフィードへのリンクを含めることができるチェックボックスが含まれています。 |
| [!UICONTROL New Products] | カタログに追加された新製品の通知を公開します。 |
| [!UICONTROL Special Products] | 特別価格の製品に関する通知を公開します。 |
| [!UICONTROL Coupons / Discounts] | ストアで利用可能な特別なクーポンや割引の通知を公開します。 |
| [!UICONTROL Top Level Category] | カタログの最上位のカテゴリ構造に対する変更の通知を公開します。この通知は、メインメニューに反映されます。 |
| [!UICONTROL Customer Order Status] | 顧客が RSS フィードで注文の状態を追跡できるようにします。 有効化すると、RSS フィードリンクがオーダーに表示されます。 |

{style="table-layout:auto"}

### ストアの RSS フィードを設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 右上隅で、を設定します **[!UICONTROL Store View]** に設定する必要があります。

   確認のメッセージが表示されたら、 **[!UICONTROL OK]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL RSS Feeds]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Rss Config]** セクションとセット **[!UICONTROL Enable RSS]** 対象： `Enable`.

   ![カタログ設定 – RSS フィード](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   必要に応じて、 **[!UICONTROL Use Default]** チェックボックスをオンにして、デフォルト値を変更します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Wish List]** セクションとセット **[!UICONTROL Enable RSS]** 対象： `Enable`.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Catalog]** セクションおよびその他のフィードをに設定します `Enable` 必要に応じて。

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![カタログ - RSS フィードの設定](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order]** セクションとセット **[!UICONTROL Customer Order Status Notification]** 対象： `Enable`.

1. 完了したら、 **[!UICONTROL Save Config]**.

1. 次を使用してストアフロントで結果を確認します `/rss` ページ URL の末尾に配置されます。

