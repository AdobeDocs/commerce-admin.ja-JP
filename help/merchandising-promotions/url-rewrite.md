---
title: URL の書き換え
description: URL の書き換えと、Commerce URL 書き換えツールを使用した、商品、カテゴリまたはCMSページに関連付けられている URL の変更について説明します。
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL の書き換え

>[!TIP]
>
>Adobe Commerce as a Cloud Serviceについては、Commerce ストアフロントドキュメントの [SEO ガイドライン ](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/) を参照してください

URL 書き換えツールを使用すると、商品、カテゴリまたはCMSページに関連付けられている URL を変更できます。 書き換えが有効になると、前の URL を指すリンクは新しいアドレスにリダイレクトされます。

>[!NOTE]
>
>複数またはすべての製品の URL リライトを同時に更新するには、[ 複数の URL リライト ](url-rewrite-product.md#multiple-url-rewrites) を参照してください。

_rewrite_ および _redirect_ という用語は同じ意味で使用されることが多いですが、意味するプロセスが多少異なります。 URL の書き換えにより、ブラウザーでの URL の表示方法が変更されます。 URL リダイレクトは、サーバーに保存された URL を更新します。 URL リダイレクトは、一時的または永続的に設定できます。 製品、カテゴリまたはページの URL キーを簡単に変更し、既存のリンクを保持できるように、ストアでは URL の書き換えとリダイレクトを使用しています。

デフォルトでは [ 自動 URL リダイレクト ](url-redirect-product-automatic.md) がストアに対して有効になっており、各製品の「URL キー」フィールドで **古い URL の永続的なリダイレクトを作成** チェックボックスが選択されています。

{{url-rewrite-skip}}

{{url-rewrite-params}}

![ 検索エンジンの最適化 – 永続的な URL リダイレクトの作成 ](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## 正規 URL

SEO の目的では、は各 web ページに個別の URL が 1 つだけあることをお勧めします。

複数の URL でアクセス可能な単一のページがある場合、または異なるページに同様のコンテンツが含まれている場合、Googleでは、これらを同じページの重複バージョンと見なします。 Googleでは、1 つの URL を正規バージョンとして選択し、その URL をクロールします。他のすべての URL は重複 URL と見なされ、クロールの頻度が下がります。

どの URL が正規かをGoogleに明示的に伝えない場合、選択が行われるか、または両方の URL が等しい重み付けと見なされる可能性があります。 これにより、望ましくない動作が発生する可能性があり、クロール予算が無効になったり、分散したバックリンクが低くなったりするリスクがあります。

Web サイトの設定方法によっては、インデックスにサイトの複数のバージョンが含まれる場合があります。

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

正規ページを指定するには、[Google Search Central ドキュメント ](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) を参照してください。

## URL の書き換えの設定

Web サーバーの Apache 書き換えの有効化は、Commerceの初期設定の一部です。 Commerceでは、URL の書き換えを定期的に使用して、通常 URL のルートフォルダーの直後に表示されるファイル名 `index.php` を削除します。 Web サーバーの書き換えが有効な場合、システムは各 URL を書き換えて `index.php` を省略します。 書き換えは、検索エンジンや顧客に値を伝えない単語を削除し、パフォーマンスやサイトのランクには影響しません。

Web サーバーの書き換えのない URL

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

Web サーバーの書き換え後の URL

    http://www.yourdomain.com/magento/storeview/url-identifier

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. **[!UICONTROL General]** が展開されている左パネルで、「**[!UICONTROL Web]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Search Engine Optimization]**」セクションを展開します。

   ![ 一般設定 – Web 検索エンジンの最適化 ](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Use Web Server Rewrites]** を好みに合わせて設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## URL 書き換えの作成

URL 書き換えツールを使用すると、ストア内の任意のページの製品およびカテゴリの書き換えやカスタムの書き換えを作成できます。 書き換えが有効になると、前の URL を指す既存のリンクは、新しいアドレスにシームレスにリダイレクトされます。

URL の書き換えを使用すると、値の高いキーワードを追加して、検索エンジンによる製品のインデックス作成方法を改善できます。 書き換えを使用して、一時的な季節的な変更や永続的な変更のために追加の URL を作成することもできます。 書き換えは、CMS コンテンツページを含む、任意の有効なパスに対して作成できます。 内部的には、システムは常に製品とカテゴリを ID で参照します。 URL が頻繁に変更されても、ID は変わりません。 次に、URL 書き換えを使用する方法を示します。

システム URL

    http://www.example.com/catalog/category/id/6

元の URL

    http://www.example.com/peripherals/keyboard.html

リダイレクトされた製品の URL

    http://www.example.com/ergonomic-keyboard.html

追加のカテゴリ URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL 書き換えグリッド ](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerceには、次の URL 書き換えタイプがあります。

* [製品の書き換え](url-rewrite-product.md)
* [カテゴリの書き換え](url-rewrite-category.md)
* [CMSページの書き換え](url-rewrite-cms-page.md)
* [カスタム書き換え](url-rewrite-custom.md)

## URL 書き換えデモ

URL の書き換えの管理については、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
