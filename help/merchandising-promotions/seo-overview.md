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

_検索エンジンの最適化_ （SEO）は、サイトのコンテンツと表示を微調整して、検索エンジンによるページのインデックス作成方法を改善する手法です。 Commerceには、継続的な SEO の取り組みをサポートする様々な機能が含まれています。

## メタデータ

豊富なキーワードの追加と強化の詳細を説明します [メタデータ](meta-data.md) サイトやストアの場合。

## サイトマップの使用

A [サイトマップ](sitemap-xml.md) 検索エンジンでストアのインデックスを作成する方法を改善し、Web クローラーによって見落とされる可能性のあるページを検索するように設計します。 サイトマップは、すべてのページと画像のインデックスを作成するように設定できます。

## URL の書き換え

この [URL の書き換え](url-rewrite.md) ツールを使用すると、製品、カテゴリまたは CMS ページに関連付けられている URL を変更できます。

## 検索エンジンロボット

Commerce設定には、サイトのインデックスを作成する web クローラーとボットの手順を生成および管理する設定が含まれています。 次に対するリクエストの場合： `robots.txt` （物理ファイルではなく）Commerceに到達すると、ロボット コントローラに動的にルーティングされます。 指示は、ほとんどの検索エンジンで認識され、その後に続くディレクティブです。

Commerceで生成される robots.txt ファイルには、システムで内部的に使用されるファイルを含んだサイトの特定の部分のインデックスを作成しない web クローラー向けの手順が、デフォルトで含まれています。 デフォルト設定を使用することも、すべてまたは特定の検索エンジン用に独自のカスタム手順を定義することもできます。 このテーマを詳しく解説する記事はオンライン上にたくさんあります。

### カスタム手順の例

**フルアクセスを許可**

    User-agent:*
    禁止：

**すべてのフォルダーへのアクセスを許可しない**

    User-agent:*
    許可しない：/

**デフォルトの手順**

    User-agent: *
    許可しない：/index.php/
    許可しない：/*?
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

### 設定 `robots.txt`

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. の検索 **[!UICONTROL Global]** グリッドの最初の行にある設定をクリックし、 **[!UICONTROL Edit]**.

   ![グローバル設計設定](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 下にスクロールして展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Search Engine Robots]** を選択し、次の操作を実行します。

   ![設計設定 – 検索エンジンロボット](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - を設定 **[!UICONTROL Default Robots]** を次のいずれかに変更します。

     | オプション | 説明 |
     |------|------------|
     | `INDEX, FOLLOW` | は、Web クローラーに対して、サイトのインデックスを作成し、後で変更を確認するように指示します。 |
     | `NOINDEX, FOLLOW` | では、Web クローラーに対して、サイトのインデックスを作成しないようにし、後で変更を確認するように指示します。 |
     | `INDEX, NOFOLLOW` | では、Web クローラーに対し、サイトのインデックスを 1 回だけ作成し、後で変更をチェックしないように指示します。 |
     | `NOINDEX, NOFOLLOW` | では、Web クローラーに対して、サイトのインデックス作成を避け、後で変更をチェックしないように指示します。 |

     {style="table-layout:auto"}

   - 必要に応じて、にカスタム手順を入力します **[!UICONTROL Edit Custom instruction of robots.txt file]** ボックス。 例えば、サイトが開発中の場合に、すべてのフォルダーへのアクセスを許可しないことをお勧めします。

   - デフォルトの手順に戻すには、をクリックします **[!UICONTROL Reset to Default]**.

1. 完了したら、 **[!UICONTROL Save Configuration]**.
