---
title: 検索エンジン最適化
description: Commerceサイトの検索エンジン最適化（SEO）ツールと、SEOを最適化するベストプラクティスについて解説します。
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
TQID: https://experienceleague.adobe.com/cEXR2743G7ZzRSKqb9r344Osipo-R-GlqxNZwC-u-Nk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 0%

---

# SEOの概要

_検索エンジン最適化_ （SEO）は、検索エンジンによるページのインデックス作成方法を改善するために、サイトのコンテンツとプレゼンテーションを微調整する方法です。 Commerceには、継続的なSEOの取り組みをサポートする、さまざまな機能が搭載されています。

>[!TIP]
>
>Adobe Commerce as a Cloud Serviceについては、Commerce Storefront ドキュメントの[SEO ガイドライン &#x200B;](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)を参照してください

## メタデータ

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

サイトとストアにキーワードが豊富な[&#x200B; メタデータ &#x200B;](meta-data.md)を追加および強化する方法について説明します。

## サイトマップの使用

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

[&#x200B; サイトマップ &#x200B;](sitemap-xml.md)は、検索エンジンによるストアのインデックス作成方法を改善し、web web クローラーが見落とす可能性のあるページを見つけるように設計されています。 サイトマップでは、すべてのページと画像にインデックスを作成するように設定できます。

## URLの書き換え

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

[URL書き換え](url-rewrite.md) ツールを使用すると、商品、カテゴリ、またはCMS ページに関連付けられている任意のURLを変更できます。

## 検索エンジンのロボット

Commerceの設定には、サイトをインデックス化するweb web クローラーおよびボットの手順を生成および管理するための設定が含まれています。 `robots.txt`のリクエストが（物理ファイルではなく）Commerceに到達した場合、robots controllerに動的にルーティングされます。 指示は、ほとんどの検索エンジンで認識され、その後に続くディレクティブです。

デフォルトでは、Commerceによって生成されるrobots.txt ファイルには、web web クローラーの手順が含まれており、システムで内部的に使用されるファイルを含むサイトの特定の部分のインデックス作成を避けることができます。 デフォルト設定を使用するか、またはすべての場合や特定の検索エンジンに対して独自のカスタム手順を定義できます。 ネット上には、このテーマについて詳しく解説する記事がたくさんあります。

### カスタム手順の例

**完全なアクセスを許可**

    User-agent:*
    許可しない：

**すべてのフォルダーへのアクセスを許可しない**

    User-agent:*
    許可しない：/

**既定の手順**

    User-agent: *
    Disallow: /index.php/
    Disallow: /*?
    Disallow: /checkout/
    Disallow: /app/
    Disallow: /lib/
    Disallow: /*.php$
    Disallow: /pkginfo/
    Disallow: /report/
    Disallow: /var/
    Disallow: /customer/
    Disallow: /sendfriend/
    Disallow: /14&rbrace; /*SID=

    
    

### `robots.txt`の設定

1. _管理者_ サイドバーで、**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. グリッドの最初の行にある&#x200B;**[!UICONTROL Global]**&#x200B;設定を見つけて、**[!UICONTROL Edit]**&#x200B;をクリックします。

   ![&#x200B; グローバルデザイン設定](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. 下にスクロールして、**[!UICONTROL Search Engine Robots]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![&#x200B; デザイン設定 – 検索エンジンロボット &#x200B;](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - **[!UICONTROL Default Robots]**&#x200B;を次のいずれかに設定します：

     | オプション | 説明 |
     |------|------------|
     | `INDEX, FOLLOW` | Web web クローラーに対して、サイトのインデックスを作成し、後で変更内容を確認するように指示します。 |
     | `NOINDEX, FOLLOW` | Web web クローラーに対して、サイトのインデックス作成を避けながら、後で変更点を確認するように指示します。 |
     | `INDEX, NOFOLLOW` | Web web クローラーに対して、サイトのインデックスを1回だけ作成するように指示します。ただし、ページ上のリンクには従わないでください。 |
     | `NOINDEX, NOFOLLOW` | Web web クローラーに対して、サイトのインデックス作成を避け、ページ上のリンクに従わないように指示します。 |

     {style="table-layout:auto"}

   - 必要に応じて、カスタムの指示を&#x200B;**[!UICONTROL Edit Custom instruction of robots.txt file]** ボックスに入力します。 例えば、サイトの開発中に、すべてのフォルダーへのアクセスを許可しない場合があります。

   - 既定の指示を復元するには、**[!UICONTROL Reset to Default]**&#x200B;をクリックします。

1. 完了したら、**[!UICONTROL Save Configuration]**&#x200B;をクリックします。
