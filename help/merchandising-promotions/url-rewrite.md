---
title: URL の書き換え
description: URL の書き換えと、コマース URL の書き換えツールを使用して、製品、カテゴリ、または CMS ページに関連付けられた URL を変更する方法について説明します。
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL の書き換え

URL 書き換えツールを使用すると、製品、カテゴリまたは CMS ページに関連付けられている URL を変更できます。 書き換えが有効になると、以前の URL を指すリンクは新しいアドレスにリダイレクトされます。

>[!NOTE]
>
>複数またはすべての製品の URL 書き換えを同時に更新するには、 [複数の URL の書き換え](url-rewrite-product.md#multiple-url-rewrites).

用語 _書き換え_ および _redirect_ は同じ意味で使用されることが多いが、少し異なるプロセスを指す。 URL の書き換えにより、URL がブラウザーで表示される方法が変更されます。 URL リダイレクトは、サーバーに保存されている URL を更新します。 URL のリダイレクトは、一時的または永続的に設定できます。 ストアでは URL の書き換えとリダイレクトを使用して、製品、カテゴリまたはページの URL キーを簡単に変更し、既存のリンクを保持できるようにします。

デフォルトでは、 [URL の自動リダイレクト](url-redirect-product-automatic.md) がストアおよび **古い URL の永続的なリダイレクトを作成** 各製品の「 URL キー」フィールドでチェックボックスがオンになっている。

{{url-rewrite-skip}}

{{url-rewrite-params}}

![検索エンジンの最適化 — 永続的な URL リダイレクトの作成](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## 正規 URL

SEO の目的では、各 Web ページに 1 つの個別の URL のみが含まれるという考え方をお勧めします。

複数の URL からアクセスできる単一のページがある場合、または類似したコンテンツを持つ別のページがある場合、Googleでは、これらを同じページの重複バージョンと見なします。 Googleは、1 つの URL を正規バージョンとして選択してクロールします。他のすべての URL は重複した URL と見なされ、クロールの頻度が低くなります。

どの URL が正規の URL かを明示的にGoogleに示さない場合は、自分用に選択するか、両方の URL を同じ重みと見なすかもしれません。 これにより、望ましくない動作が発生し、無効なクロール予算と低分散バックリンクのリスクが発生します。

Web サイトの設定方法によっては、次のような複数のバージョンのサイトがインデックスに含まれる場合があります。

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

正規ページを指定するには、 [Google Search Central ドキュメント](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## URL の書き換えを設定

Web サーバーの Apache Rewrites の有効化は、コマースの初期設定に含まれています。 Commerce は定期的に URL の書き換えを使用してファイル名を削除します `index.php` これは通常、URL のルートフォルダーの直後に表示されます。 Web サーバーの書き換えが有効な場合、省略する各 URL を書き換えます `index.php`. この書き換えにより、検索エンジンや顧客に価値を伝えない単語が削除され、パフォーマンスやサイトのランクに影響を与えません。

Web サーバー書き換えのない URL

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

Web サーバー書き換えを使用した URL

    http://www.yourdomain.com/magento/storeview/url-identifier

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで **[!UICONTROL General]** は展開済みで、「 **[!UICONTROL Web]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Optimization]** 」セクションに入力します。

   ![一般設定 — Web 検索エンジンの最適化](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Use Web Server Rewrites]** を選択します。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## URL の書き換えを作成

URL 書き換えツールを使用して、ストア内の任意のページに対して、製品とカテゴリの書き換え、カスタムの書き換えを作成できます。 書き換えが有効になると、以前の URL を指す既存のリンクはすべて新しいアドレスにシームレスにリダイレクトされます。

URL の書き換えを使用して、価値の高いキーワードを追加し、検索エンジンによる製品のインデックス作成方法を改善できます。 また、書き換えを使用して、一時的な季節の変更や永続的な変更に対応する追加の URL を作成することもできます。 書き換えは、CMS コンテンツページを含む任意の有効なパスに対して作成できます。 内部的には、システムは常に ID で製品とカテゴリを参照します。 URL の変更頻度に関わらず、ID は同じです。 URL の書き換えを使用する方法を次に示します。

システム URL

    http://www.example.com/catalog/category/id/6

元の URL

    http://www.example.com/peripherals/keyboard.html

リダイレクトされた製品 URL

    http://www.example.com/ergonomic-keyboard.html

追加のカテゴリ URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL 書き換えグリッド](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce では、次の URL 書き換えタイプを提供します。

* [製品の書き換え](url-rewrite-product.md)
* [カテゴリの書き換え](url-rewrite-category.md)
* [CMS ページの書き換え](url-rewrite-cms-page.md)
* [カスタム書き換え](url-rewrite-custom.md)

## URL でデモを書き換える

URL の書き換えの管理については、このビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
