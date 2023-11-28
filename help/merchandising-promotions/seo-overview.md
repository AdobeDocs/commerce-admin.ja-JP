---
title: 検索エンジンの最適化
description: コマースサイトの検索エンジン最適化 (SEO) ツールと、最適な SEO のベストプラクティスについて説明します。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO の概要

_検索エンジンの最適化_ (SEO) は、検索エンジンによるページのインデックス作成方法を改善するために、サイトのコンテンツと表示を微調整する方法です。 コマースには、継続的な SEO 作業をサポートする様々な機能が含まれています。

## メタデータ

キーワードを豊富に追加し、強化する方法の詳細を説明します [メタデータ](meta-data.md) サイトおよびストアの

## サイトマップの使用

A [サイトマップ](sitemap-xml.md) は、検索エンジンによってストアのインデックスが作成される方法を改善し、web クローラーが見落とす可能性のあるページを見つけるように設計されています。 サイトマップは、すべてのページと画像のインデックスを作成するように設定できます。

## URL の書き換え

The [URL の書き換え](url-rewrite.md) ツールを使用すると、製品、カテゴリ、CMS ページに関連付けられた任意の URL を変更できます。

## 検索エンジンロボット

コマースの設定には、サイトのインデックスを作成する Web クローラーとボットの手順を生成および管理するための設定が含まれています。 次をリクエストした場合： `robots.txt` （物理ファイルではなく）コマースに到達すると、ロボットコントローラに動的にルーティングされます。 指示は、認識され、その後にほとんどの検索エンジンが続くディレクティブです。

既定では、Commerce で生成される robots.txt ファイルには、Web クローラーに関する指示が含まれており、システムで内部的に使用されるファイルを含むサイトの特定の部分にインデックスを作成しないようにします。 デフォルト設定を使用するか、すべての検索エンジンに対して独自のカスタム手順を定義するか、特定の検索エンジンに対して独自のカスタム手順を定義できます。 この問題を詳細に調査する記事は、オンライン上に多数あります。

### カスタム手順の例

**フルアクセスを許可**

    User-agent:*
    許可しない：

**すべてのフォルダへのアクセスを許可しない**

    User-agent:*
    許可しない： /

**デフォルトの手順**

    ユーザーエージェント： *
    許可しない場合： /index.php/
    許可しない： /*?
    許可しない： /checkout/
    許可しない： /app/
    許可しない： /lib/
    許可しない： /*.php$
    許可しない場合： /pkginfo/
    許可しない： /report/
    許可しない： /var/
    許可しない： /catalog/
    許可しない： /customer/
    許可しない： /sendfriend/
    許可しない： /review/
    許可しない： /*SID=

### 設定 `robots.txt`

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 次を検索： **[!UICONTROL Global]** グリッドの 1 行目の設定で、 **[!UICONTROL Edit]**.

   ![グローバルデザイン設定](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 下にスクロールして展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Search Engine Robots]** 」セクションで次の操作を実行します。

   ![デザイン設定 — 検索エンジンロボット](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - 設定 **[!UICONTROL Default Robots]** を次のいずれかに変更します。

     | オプション | 説明 |
     |------|------------|
     | `INDEX, FOLLOW` | Web クローラーに対して、サイトのインデックスを作成し、後で変更を確認するように指示します。 |
     | `NOINDEX, FOLLOW` | Web クローラーに対して、サイトのインデックス作成を避け、後で変更を確認するように指示します。 |
     | `INDEX, NOFOLLOW` | Web クローラーに対し、サイトのインデックスを 1 回作成するが、後で変更を確認しないように指示します。 |
     | `NOINDEX, NOFOLLOW` | Web クローラーに対して、サイトのインデックス作成を回避し、後で変更を確認しないように指示します。 |

     {style="table-layout:auto"}

   - 必要に応じて、 **[!UICONTROL Edit Custom instruction of robots.txt file]** ボックス。 例えば、サイトが開発中の場合、すべてのフォルダーへのアクセスを許可しないようにすることができます。

   - デフォルトの手順を復元するには、 **[!UICONTROL Reset to Default]**.

1. 完了したら、「 **[!UICONTROL Save Configuration]**.
