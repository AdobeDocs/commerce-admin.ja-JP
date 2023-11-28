---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: 次のページで設定を確認します： [!UICONTROL Advanced] &gt; [!UICONTROL Developer] コマース管理のページ。
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>これらの設定は、 [開発者モード](../../systems/developer-tools.md#operation-modes) のみ。

## [!UICONTROL Frontend Development Workflow]

![フロントエンド開発ワークフロー](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [フロントエンド開発ワークフロー](../../systems/developer-tools.md#frontend-development-workflow) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | グローバル | 開発時に、クライアント側またはサーバー側でコンパイルを少なくするかどうかを指定します。 オプション： <br/>**`Client side less compilation`**— コンパイルは、ネイティブの less.js ライブラリを使用してブラウザーでおこなわれます。<br/>**`Server side less compilation`**  — コンパイルは、Less PHP ライブラリを使用してサーバー上で行われます。 これは実稼動用のデフォルトのモードです。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Developer Client Restrictions]

![開発者クライアントの制限](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

この設定の変更の詳細については、 [クライアントの制限](../../systems/developer-tools.md#client-restrictions) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | ストア表示 | ストア内許可リストに加えるの顧客に干渉することなく、ライブサイトで開発者ツールを使用できる IP アドレスのを作成します。 開発者ツール ( _インライン翻訳_&#x200B;は、上の IP アドレスからのみ表示され許可リストに加えるます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Template Settings]

![テンプレート設定](./assets/developer-template-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | ストア表示 | 有効化 [シンボリックリンク](https://en.wikipedia.org/wiki/Symbolic_link) では、サイトをセキュリティ上のリスクにさらすことができるので、実稼動用ストアには推奨されません。 |
| [!UICONTROL Minify Html] | ストア表示 | ストアテンプレートのHTMLを最小化するかどうかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Debug]

![デバッグ](./assets/developer-debug.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [テンプレートパスのヒント](../../systems/developer-tools.md#template-path-hints) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | ストア表示 | ページで使用される各テンプレートのパスを示す表記をストアフロントに追加します。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | グローバル | 管理者に、ページで使用される各テンプレートへのパスを示す表記を追加します。 オプション： `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | ストア表示 | テンプレートパスのヒントにブロックの名前が含まれます。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Translate Inline]

![インラインを翻訳](./assets/developer-translate-inline.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [インラインを翻訳](../../systems/developer-tools.md#translate-inline) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | ストア表示 | ストアフロント用のインライントランスレーターをアクティブにします。 インターフェイスのテキストは、ストアの表示ごとに編集できます。 ライブストアに干渉することなくインライントランスレーターを使用するには、IP アドレスを開発者クライアント制限に追加し許可リストに加えるます。 |
| [!UICONTROL Enable for Admin] | グローバル | 管理者用のインライントランスレーターをアクティベートします。 ストアフロントとは異なり、管理者は複数の言語に翻訳できません。 ただし、インターフェイス内のフィールドラベルやその他のテキストは変更できます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JavaScript Settings]

![JavaScript 設定](./assets/developer-javascript-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | ストア表示 | 複数の JavaScript ファイルを 1 つのファイルに結合して、ページの読み込み時間を短縮します。 |
| [!UICONTROL Enable JavaScript Bundling] | ストア表示 | 複数の JavaScript ファイルを 1 つのファイルにバンドルできるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | ストア表示 | 不要な文字、スペースおよびインデントを削除して、コードのサイズを小さくします。 |
| [!UICONTROL Move JS code to the bottom of the page] | グローバル | 有効にすると、JS コードがページの末尾に移動します。 オプション： `Yes` / `No` |
| [!UICONTROL Translation Strategy] | グローバル | システムで使用される翻訳方法を決定します。 オプション： <br/>**`Dictionary`**— ストアフロント側での翻訳。<br/>**`Embedded`**  — 管理者側での翻訳。 |
| [!UICONTROL Log JS Errors to Session Storage] | グローバル | 有効にした場合、機能テストでレポートに使用できます。 オプション： `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | グローバル | 収集された js エラーを取得するために使用されるキーを識別します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CSS Settings]

![CSS 設定](./assets/developer-css-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、 [リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files) （内） _管理システムガイド_.

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | ストア表示 | 複数の CSS ファイルを 1 つのファイルに結合して、ページの読み込み時間を短縮します。 オプション： `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | ストア表示 | 不要な文字、スペースおよびインデントを削除して、コードのサイズを小さくします。 オプション： `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | グローバル | The _CSS クリティカルパス_ で縮小された重要な CSS をインラインで配信 `<head>` とは、非同期で読み込まれる重要でないスタイルをすべて遅延させます。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Image Processing Settings]

![画像処理設定](./assets/developer-image-processing-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | グローバル | イメージのレンダリングに使用するアダプタを指定します。 アダプタの設定を変更した後、カタログイメージのキャッシュをフラッシュします。 オプション： `PHP GD2` / `ImageMagick` <br/><br/>**_注意：_**ICO ファイルタイプは、ImageMagik アダプタでのみサポートされます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Caching Settings]

![キャッシュ設定](./assets/developer-cache-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | グローバル | 有効にすると、ユーザー定義の属性とシステムエンティティ属性値 (EAV) 属性をキャッシュします。 このオプションを使用すると、パフォーマンスが向上しますが、キャッシュに追加の領域が必要になる場合があります。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Static Files Settings]

![静的ファイル設定](./assets/developer-static-files-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | グローバル | 有効にすると、静的ファイルの URL にデジタル署名が追加され、ブラウザーがファイルの新しいバージョンが使用可能かどうかを検出できるようになります。 ファイルの署名がブラウザーのキャッシュに保存されているものと異なる場合は、ファイルの新しいバージョンが使用されます。 署名可能な静的ファイルには、JavaScript、CSS、画像、フォントなどがあります。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Grid Settings]

![グリッド設定](./assets/developer-grid-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | オーダー処理システムエンティティ（オーダー、請求書、出荷、クレジット・メモなど）をグリッドに追加し、再インデックスを作成するタイミングを決定します。 非同期インデックス作成は、保存操作中のデータのロックを回避し、処理時間を短縮するために使用できます。 オプション： <br/>**`Disable`**- （デフォルト）注文関連のエンティティは、様々なタイミングでグリッドに追加されます。 保存時に<br/>**`Enable`**  — 注文関連のエンティティは、スケジュールされた Cron ジョブ中にのみグリッドに追加されます。 Cron は、1 分に 1 回実行するように設定する必要があります。 |

{:style=&quot;table-layout:auto&quot;}
