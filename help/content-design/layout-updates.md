---
title: レイアウトの更新
description: レイアウトの更新を使用してページのレイアウトをカスタマイズする方法を説明します。
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 0%

---

# レイアウトの更新

カスタムレイアウトの更新に取り組む前に、ストアのページの作成方法と、*レイアウト* および *レイアウトの更新* という用語の違いを理解しておくことが重要です。 レイアウトとは、ページの視覚的かつ構造的な構成を指します。 レイアウトの更新とは、ページの作成方法を上書きまたはカスタマイズできる、特定の XML 命令のセットを指します。

[!DNL Commerce] ストアの XML レイアウトは、コンテナとブロックの階層構造です。 すべてのページに表示される要素もあれば、特定のページにのみ表示される要素もあります。 レイアウト、コンテナ、ブロックについて詳しくは、[ フロントエンド開発者ガイド ](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) の _レイアウトの概要_ を参照してください。

[ ウィジェット ](widgets.md) ツールを使用すると、既存の [ コンテンツブロック ](blocks.md) をページのデフォルトレイアウトに簡単に追加できます。 より高度な更新を行うには、XML レイアウトの更新コードをサーバーに保存し、そのファイルを管理者からカスタムレイアウトの更新として参照する必要があります。 プロセスの概要については、[ レイアウト更新を使用 ](layout-updates.md#place-a-block-using-layout-updates) を参照してください。

次の図では、コンテナを参照する名前は黒で、ブロックの種類（ブロック クラス パス）は青です。

![ 標準ブロックレイアウト図 ](./assets/page-layout-default.png){width="500" zoomable="yes"}

| ブロックタイプ | 説明 |
|--- |--- |
| `page/html` | このブロックの名前は `root` で、レイアウト内の数少ないルートブロックの 1 つです。 独自のブロックを作成して `root` という名前を付けることもできます。これは、このタイプのブロックの標準的な名前です。 このタイプのブロックは、ページごとに 1 つだけ存在できます。 |
| `page/html_head` | ブロック名は `head` で、ルート ブロックの子です。 このタイプのブロックは、ページごとに 1 つのみ存在できるので、削除しないでください。 |
| `page/html_notices` | ブロック名は `global_notices` で、ルート ブロックの子です。 このブロックがレイアウトから削除されると、グローバル通知はページに表示されません。 このタイプのブロックは、ページごとに 1 つだけ存在できます。 |
| `page/html_header` | ブロック名は `header` で、ルート ブロックの子です。 このブロックは、ページの上部にあるビジュアルヘッダーに対応し、いくつかの標準ブロックが含まれています。 このタイプのブロックは、ページごとに 1 つのみ存在できるので、削除しないでください。 |
| `page/html_wrapper` | デフォルトのレイアウトに含まれていますが、このブロックは非推奨であり、後方互換性を確保するためにのみ含まれています。 このタイプのブロックは使用しないでください。 |
| `page/html_breadcrumbs` | このブロックの名前は `breadcrumbs` であり、ヘッダーブロックの子です。 このブロックには、現在のページのパンくずリストが表示されます。 このタイプのブロックは、ページごとに 1 つだけ存在できます。 |
| `page/html_footer` | ブロック名は `footer` で、ルート ブロックの子です。 フッターブロックは、ページの下部にある視覚的なフッターに対応し、いくつかの標準ブロックが含まれています。 このタイプのブロックは、ページごとに 1 つのみ存在できるので、削除しないでください。 |
| `page/template_links` | 標準レイアウトには、このタイプのブロックが 2 つあります。 `top.links` ブロックはヘッダーブロックの子で、上部のナビゲーションメニューに対応します。 `footer_links` ブロックは footer ブロックの子で、下部のナビゲーションメニューに対応します。 <br/><br/>**_メモ：_**&#x200B;例に示すように、テンプレートリンクを操作できます。 |
| `page/switch` | 標準レイアウトには、このタイプのブロックが 2 つあります。 `store_language` ブロックはヘッダーブロックの子で、最上位の言語スイッチャーに対応します。 `store_switcher` ブロックは footer ブロックの子で、下部のストア切り替えボタンに対応します。 |
| コア/メッセージ | 標準レイアウトには、このタイプのブロックが 2 つあります。 `global_messages` ブロックには、グローバル メッセージが表示されます。 `messages` ブロックは、他のすべてのメッセージを表示するために使用します。 これらのブロックを削除すると、メッセージは表示されません。 |
| `core/text_list` | このタイプのブロックは、[!DNL Commerce] 全体で子ブロックをレンダリングするためのプレースホルダーとして広く使用されています。 |
| `core/profiler` | このタイプのブロックのインスタンスは、ページごとに 1 つだけです。 内部 [!DNL Commerce] プロファイラーに使用されるので、他の目的には使用しないでください。 |

{style="table-layout:auto"}

## レイアウトの更新を使用してブロックを配置する

[ レイアウトの更新 ](layout-updates.md) ページのレイアウトをカスタマイズできるようにします。 レイアウトの更新は [ ウィジェット ](widgets.md) よりも柔軟性がありますが、サーバーへのアクセスと XML の基本知識が必要です。

次の手順は、レイアウトの更新を使用してページにブロックを配置する方法を示しています。 具体的な例と構文のヘルプについては、『 [ フロントエンド開発者ガイド _の ](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 一般的なレイアウトのカスタマイズタスク_ を参照してください。

### 手順 1：ブロックの作成

1. 配置する [ ブロック ](block-add.md) を作成します。

1. `block_id` は、レイアウトの更新手順で使用されるので、メモに注意してください。

### 手順 2:XML でレイアウトの更新を作成する

1. レイアウト手順を XML で作成して、[CMS ブロックを参照 ](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/) します。

1. テーマの XML ファイルが保存されるレイアウトフォルダーのサーバーに [ レイアウトの手順 ](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) を保存します。

   例：

   `<theme_dir>/<Namespace>_<Module>/layout`

   レイアウトハンドルは、`cms_page_view_selectable_` で始まり、その後にCMS ページの URL キー、レイアウト更新オプション、`xml` ファイルサフィックスが続くファイル名です。 次の例では、`customer-service` はページの URL キーで、`ChatTool` はレイアウトの更新をページに適用するために選択するオプションです。

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | 要素 | 説明 |
   |--- |--- |
   | CMSページ識別子 | スラッシュ（`/`）をアンダースコア（`_`）に置換したページの URL キー。 |
   | レイアウト更新名 | _カスタムレイアウトの更新_ のために表示されるオプション。 |

   {style="table-layout:auto"}

### 手順 3：ページからレイアウトの更新を参照する

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Elements]_/**[!UICONTROL Pages]**&#x200B;に移動します。

1. ブロックを配置するページを見つけて、編集モードで開きます。

1. 下にスクロールして、「**[!UICONTROL Design]**」セクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. ページに関連付けられている使用可能なすべてのレイアウト更新を表示するには、「**[!UICONTROL Custom Layout Update]**」メニューをクリックします。

   ![ カスタムレイアウトの更新リスト ](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. ページに適用するレイアウトの更新を選択します。

### 手順 4：キャッシュを保存して更新する

1. 完了したら、「**[!UICONTROL Save & Close]**」をクリックします。

1. ワークスペースの上部にあるメッセージで「**[!UICONTROL Cache Management]**」をクリックし、無効なキャッシュ項目をすべて更新します。
