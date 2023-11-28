---
title: ソーシャルメディアおよび RSS フィード
description: ソーシャルメディアやその他の RSS フィードの統合を追加して、ブランドや製品に対する認知度を高める方法を説明します。
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1171'
ht-degree: 0%

---

# ソーシャルメディアおよび RSS フィード

多くの商人は、ソーシャルメディアや他のデジタルツールを使用して、ブランドや製品の認知度を高めています。 Marketplace 拡張機能をインストールするか、コンテンツページにプラグインを追加することで、ストアとソーシャルネットワークを統合できます。 RSS フィードを使用して、製品情報を買い物集計サイトに公開し、ニュースレターに含めます。 顧客は、RSS フィードを購読して、新しい製品やプロモーションについて知ることができます。

## ソーシャルネットワーク

ストアは、 [Marketplace 拡張機能](../getting-started/commerce-marketplace.md). また、 _次に類似_ ボタンを使用して、ストア全体のページに組み込むことができる CMS ブロックに切り替えます。

ソーシャルネットワーキングサイトには、ストアに簡単に追加できる多数のプラグインがあります。 さらに、ストアとソーシャルメディアの統合に使用できるCommerce Marketplaceには、多くの拡張機能があります。 次の例は、Facebook _次に類似_ 」ボタンをクリックして、ストアに追加します。

>[!NOTE]
>
>Adobe Commerceがネイティブ _Magentoソーシャル_ Facebook統合のサポートを終了しました。 次に移動： [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} : Facebook統合用の代替拡張機能を検索します。

### 手順 1. ボタンコードを取得する

1. Meta developers Web サイトで、にアクセスします。 [ボタンの設定](https://developers.facebook.com/docs/plugins/like-button) ページに貼り付けます。

1. の場合 **[!UICONTROL URL to Like]**、ユーザーに表示するストア内のページの URL を入力します _次に類似_.

   例えば、ストアのホームページの URL を入力できます。

1. を選択します。 **[!UICONTROL Layout]** （ボタン）。

1. 次を入力します。 **[!UICONTROL Width]** サイト上でボタンと関連するテキストメッセージに使用できるピクセル単位です。

1. 設定 **[!UICONTROL Action Type]** を次のいずれかに変更します。

   - `Like`
   - `Recommend`

1. クリック **[!UICONTROL Get Code]** をクリックして、生成されたコードをクリップボードにコピーします。

### 手順 2. コンテンツブロックの作成

1. ストア管理者に戻ります。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 右上隅で、 **[!UICONTROL Add New Block]**.

1. 説明的な **[!UICONTROL Block Title]** 内部参照用。

   例： `Facebook Like Button`.

1. ユニークを割り当て **[!UICONTROL Identifier]** をブロックに追加します。すべての小文字を使用し、スペースの代わりにアンダースコアを使用します。

   例： `facebook_like_button`.

1. コマースインスタンスに複数のストア表示がある場合は、各 **[!UICONTROL Store View]** ブロックを使用できる場所。

1. コンテンツツールに応じて、コードスニペットをブロックコンテンツに追加します。

   - を使用する場合 [!DNL Page Builder]、を追加します。 [HTMLコード](../page-builder/html-code.md) をステージにブロックし、Facebookサイトからコピーしたコードのスニペットを貼り付けます。 それ以外の場合は、コードのスニペットを **[!UICONTROL Content]** ボックス。

   - エディターで、Facebookサイトからコピーしたコードのスニペットをに貼り付けます。 **[!UICONTROL Content]** ボックス。

1. ブロックがライブになる準備ができていない場合は、 **[!UICONTROL Enable Block]** から `No`.

1. 完了したら、「 **[!UICONTROL Save Block]**.

### 手順 3. ブロックを配置する

1. コンテンツツールに応じて、ブロックを追加します。

   - を使用する場合 [!UICONTROL Page Builder]を使用する場合は、次の手順に従います。 [ブロックを追加](../page-builder/block.md) をステージに追加します。

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 右上隅で、 **[!UICONTROL Add Widget]** 次の操作を実行します。

   - ![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B ではAdobe Commerceでのみ使用可能 ) _設定_ セクション、設定 **[!UICONTROL Type]** から `CMS Static Block` をクリックします。 **[!UICONTROL Continue]**.

   - を確認します。 **[!UICONTROL Design Theme]** が現在のテーマに設定されている。

   - クリック **[!UICONTROL Continue]**.

1. Adobe Analytics の **[!UICONTROL Storefront Properties]** セクションで、以下の操作を実行します。

   - の場合 **[!UICONTROL Widget Title]**、内部参照のタイトルを入力します。

   - 設定 **[!UICONTROL Assign to Store Views]** から `All Store Views`またはアプリを使用可能にするビューにドラッグします。 複数のビューを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

   - 数値を **[!UICONTROL Sort Order]** フィールドを使用して、割り当てられたブロックが他のコンテンツ要素と同じ場所のページに表示されるかどうかを指定します。 上の位置がゼロです。

1. Adobe Analytics の _[!UICONTROL Layout Updates]_セクションで、**[!UICONTROL Add Layout Update]**と設定します。**[!UICONTROL Display On]**を、ブロックを表示するカテゴリ、製品またはページに追加します。

   例えば、 `All Pages` をクリックし、ヘッダーまたはフッターのいずれかにブロックを配置すると、そのブロックはストアの各ページの同じ場所に表示されます。

   ブロックを特定のページに配置するには、次の操作を行います。

   - 設定 **[!UICONTROL Display On]** から `Specified Page` をクリックし、 **[!UICONTROL Page]** ブロックを表示する場所です。

   - を選択します。 **[!UICONTROL Block Reference]** を使用して、ブロックを配置するページ上の場所を特定します。

   - のデフォルト設定を受け入れる **[!UICONTROL Template]**（に設定） `CMS Static Block Default Template`.

   - クリック **[!UICONTROL Save and Continue Edit]**.

1. 左側のパネルで、を選択します。 **[!UICONTROL Widget Options]**.

1. クリック **[!UICONTROL Select Block…]** をクリックし、配置するブロックを選択します。

1. 完了したら、「 **[!UICONTROL Save]**.

1. インデックスとページキャッシュを更新するよう求められたら、ワークスペースの上部にある手順に従います。

   ウィジェットが _[!UICONTROL Widgets]_リスト。

### 手順 4. ストア内の場所を確認します。

ストアフロントに戻り、ブロックが正しい場所にあることを確認します。 ブロックを移動するには、ウィジェットを再度開いて別のページまたはブロック参照を試すことができます。

## RSS フィード

RSS(Really Simple Syndication) は、XML ベースのデータ形式で、オンラインで情報を配信するために使用されます。 顧客は、RSS フィードを購読して、新しい製品やプロモーションについて知ることができます。 RSS フィードは、製品情報を買い物集計サイトに公開する場合にも使用でき、ニュースレターに含めることができます。

RSS フィードを有効にすると、製品、スペシャル、カテゴリ、クーポンに追加した内容が、各フィードの購読者に自動的に送信されます。 ストアのフッターには、公開するすべての RSS フィードへのリンクが表示されます。

![RSS フィードアイコン](./assets/icon-rss.png){width="100"}<br/>

RSS フィードを読むのに必要なソフトウェアは、フィードリーダーと呼ばれ、人々がヘッドライン、ブログ、ポッドキャストなどに登録できます。 GoogleReaderは、無料でオンラインで利用できる多くのフィードリーダーの 1 つです。

![ストアフロントの例 — RSS フィード](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### RSS フィードを設定するメリット

- ストアまたはブログから最新の更新をダウンロード
- 広告（明）
- 普通株
- SEO を押す
- 売り上げを増やす

### RSS フィードのタイプ

| RSS フィード | 説明 |
|--- |--- |
| [!UICONTROL Wish List] | 有効にすると、顧客のウィッシュリストページの上部に RSS フィードリンクが表示されます。 また、ウィッシュリスト共有ページには、共有ウィッシュリストからフィードへのリンクを含めるためのチェックボックスが含まれています。 |
| [!UICONTROL New Products] | カタログに追加された新しい製品の通知を発行します。 |
| [!UICONTROL Special Products] | 特別な価格の製品に関する通知を発行します。 |
| [!UICONTROL Coupons / Discounts] | ストアで利用可能な特別なクーポンまたは割引の通知を発行します。 |
| [!UICONTROL Top Level Category] | カタログの最上位カテゴリ構造に対する変更の通知をパブリッシュします。この変更はメインメニューに反映されます。 |
| [!UICONTROL Customer Order Status] | 顧客が RSS フィードで注文ステータスを追跡できるようにします。 有効にすると、RSS フィードのリンクが注文に表示されます。 |

{style="table-layout:auto"}

### ストアの RSS フィードを設定する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 右上隅で、 **[!UICONTROL Store View]** を追加します。

   確認するメッセージが表示されたら、「 **[!UICONTROL OK]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL RSS Feeds]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Rss Config]** セクションとセット **[!UICONTROL Enable RSS]** から `Enable`.

   ![カタログの設定 — RSS フィード](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   必要に応じて、 **[!UICONTROL Use Default]** チェックボックスを使用してデフォルト値を変更します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Wish List]** セクションとセット **[!UICONTROL Enable RSS]** から `Enable`.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Catalog]** 」セクションに移動して、他のフィードを `Enable` 必要に応じて。

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![カタログ — RSS フィード設定](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order]** セクションとセット **[!UICONTROL Customer Order Status Notification]** から `Enable`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. を使用してストアフロントで結果を確認する `/rss` ページ URL の最後に配置されます。

