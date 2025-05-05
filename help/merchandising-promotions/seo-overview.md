---
title: 検索エンジンの最適化
description: Commerce Sites 向けの検索エンジン最適化（SEO）ツールと、最適な SEO のベストプラクティスについて説明します。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO の概要

_検索エンジン最適化_ （SEO）は、サイトのコンテンツと表示を微調整して、検索エンジンによるページのインデックス作成方法を改善する手法です。 Commerceには、継続的な SEO の取り組みをサポートする様々な機能が含まれています。

## メタデータ

サイトやストアに対してキーワードが豊富な [ メタデータ ](meta-data.md) を追加および強化する方法について説明します。

## サイトマップの使用

[ サイト マップ ](sitemap-xml.md) を使用すると、検索エンジンによるストアのインデックス作成方法が向上し、Web クローラーによって見落とされる可能性のあるページを検索できます。 サイトマップは、すべてのページと画像のインデックスを作成するように設定できます。

## URL の書き換え

[URL 書き換え ](url-rewrite.md) ツールを使用すると、製品、カテゴリ、CMS ページに関連付けられている URL を変更できます。

## 検索エンジンロボット

Commerce設定には、サイトのインデックスを作成する web クローラーとボットの手順を生成および管理する設定が含まれています。 `robots.txt` のリクエストが（物理ファイルではなく）Commerceに到達すると、ロボットコントローラに動的にルーティングされます。 指示は、ほとんどの検索エンジンで認識され、その後に続くディレクティブです。

Commerceで生成される robots.txt ファイルには、システムで内部的に使用されるファイルを含んだサイトの特定の部分のインデックスを作成しない web クローラー向けの手順が、デフォルトで含まれています。 デフォルト設定を使用することも、すべてまたは特定の検索エンジン用に独自のカスタム手順を定義することもできます。 このテーマを詳しく解説する記事はオンライン上にたくさんあります。

### カスタム手順の例

**フルアクセスを許可**

    User-agent:*
    Disallow:

**すべてのフォルダーへのアクセスを許可しない**

     ユーザーエージェント：*
     許可しない：/

**デフォルトの手順**

    User-agent: *
    Disallow: /index.php/
    Disallow: /*?
     許可しない：/checkout/
     許可しない：/app/
     許可しない：/lib/
     許可しない：/*.php$
     許可しない：/pkginfo/
     許可しない：/report/
     許可しない：/var/
     許可しない：/catalog/
     許可しない：/customer/
     許可しない：/sendfriend/
     許可しない：/review/
     許可しない：/*SID=

### `robots.txt` の設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. グリッドの最初の行で **[!UICONTROL Global]** 設定を見つけ、「**[!UICONTROL Edit]**」をクリックします。

   ![ グローバル設計設定 ](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 下にスクロールして、「**[!UICONTROL Search Engine Robots]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、次の操作を行います。

   ![ 設計構成 – 検索エンジンロボット ](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - **[!UICONTROL Default Robots]** を次のいずれかに設定します。

     | オプション | 説明 |
     |------|------------|
     | `INDEX, FOLLOW` | は、Web クローラーに対して、サイトのインデックスを作成し、後で変更を確認するように指示します。 |
     | `NOINDEX, FOLLOW` | では、Web クローラーに対して、サイトのインデックスを作成しないようにし、後で変更を確認するように指示します。 |
     | `INDEX, NOFOLLOW` | では、Web クローラーに対し、サイトのインデックスを 1 回だけ作成し、後で変更をチェックしないように指示します。 |
     | `NOINDEX, NOFOLLOW` | では、Web クローラーに対して、サイトのインデックス作成を避け、後で変更をチェックしないように指示します。 |

     {style="table-layout:auto"}

   - 必要に応じて、**[!UICONTROL Edit Custom instruction of robots.txt file]** のボックスにカスタム手順を入力します。 例えば、サイトが開発中の場合に、すべてのフォルダーへのアクセスを許可しないことをお勧めします。

   - 既定の手順に戻すには、[**[!UICONTROL Reset to Default]**] をクリックします。

1. 完了したら、「**[!UICONTROL Save Configuration]**」をクリックします。
