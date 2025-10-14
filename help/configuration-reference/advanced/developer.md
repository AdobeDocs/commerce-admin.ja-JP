---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: Commerce Admin の [!UICONTROL Advanced] &gt; [!UICONTROL Developer] ページで設定を確認します。
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>これらの設定は、[&#x200B; 開発者モード &#x200B;](../../systems/developer-tools.md#operation-modes) でのみ使用できます。

## [!UICONTROL Frontend Development Workflow]

![&#x200B; フロントエンド開発ワークフロー &#x200B;](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

これらの設定の変更について詳しくは、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#frontend-development-workflow) フロントエンド開発ワークフロー_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | グローバル | 開発中にクライアント側またはサーバー側で LESS コンパイルが行われるかどうかを決定します。 オプション：<br/>**`Client side less compilation`**- コンパイルは、ネイティブの less.js ライブラリを使用してブラウザーで行われます。<br/>**`Server side less compilation`** - Less PHP ライブラリを使用して、サーバー上でコンパイルが行われます。 これは、実稼動用のデフォルトのモードです。 |

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![Developer Client の制限 &#x200B;](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

この設定の変更方法については、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#client-restrictions) クライアントの制限_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | ストア表示 | ストア内の顧客に干渉することなく、ライブサイトで開発者ツールを使用できる IP アドレスの許可リストを作成します。 _インライン翻訳_ などのデベロッパーツールを使用している場合、サイトに加えられた変更は、許可リストの IP アドレスからのみ表示されます。 |

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![&#x200B; テンプレート設定 &#x200B;](./assets/developer-template-settings.png)<!-- zoom -->

これらの設定の変更方法については、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#optimizing-resource-files) リソースファイルの最適化_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | ストア表示 | [&#x200B; シンボリックリンク &#x200B;](https://en.wikipedia.org/wiki/Symbolic_link) を有効にすると、サイトがセキュリティリスクにさらされる可能性があるので、実稼動ストアには推奨されません。 |
| [!UICONTROL Minify Html] | ストア表示 | ストアテンプレートのHTMLを最小化するかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Debug]

![&#x200B; デバッグ &#x200B;](./assets/developer-debug.png)<!-- zoom -->

これらの設定の変更について詳しくは、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#template-path-hints) テンプレートパスのヒント_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | ストア表示 | ページで使用される各テンプレートへのパスを示す表記法をストアフロントに追加します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | グローバル | ページで使用される各テンプレートへのパスを示す表記を管理者に追加します。 オプション：`Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | ストア表示 | テンプレートパスのヒントにブロックの名前を含めます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![&#x200B; インライン翻訳 &#x200B;](./assets/developer-translate-inline.png)<!-- zoom -->

これらの設定の変更について詳しくは、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#translate-inline) インライン翻訳_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | ストア表示 | ストアフロントのインライン トランスレータをアクティブにします。 インターフェイスのテキストは、ストア表示ごとに編集できます。 許可リストに加える ライブストアに干渉せずに Inline Translator を使用するには、IP アドレスを Developer Client Restrictions に追加します。 |
| [!UICONTROL Enable for Admin] | グローバル | 管理者用のインライン翻訳をアクティブにします。 ストアフロントとは異なり、管理者を複数の言語に翻訳することはできません。 ただし、インターフェイスのフィールドラベルやその他のテキストは変更できます。 |

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScriptの設定 &#x200B;](./assets/developer-javascript-settings.png)<!-- zoom -->

これらの設定の変更方法については、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#optimizing-resource-files) リソースファイルの最適化_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | ストア表示 | 複数のJavaScript ファイルを 1 つのファイルに結合して、ページの読み込み時間を短縮します。 |
| [!UICONTROL Enable JavaScript Bundling] | ストア表示 | 複数のJavaScript ファイルを 1 つのファイルにバンドルできるかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | ストア表示 | 不要な文字、スペース、インデントを削除して、コードのサイズを小さくします。 |
| [!UICONTROL Move JS code to the bottom of the page] | グローバル | 有効にすると、JS コードがページの下部に移動します。 オプション：`Yes` / `No` |
| [!UICONTROL Translation Strategy] | グローバル | システムで使用される翻訳方法を決定します。 オプション：<br/>**`Dictionary`**- ストアフロント側での翻訳。<br/>**`Embedded`** – 管理者側での翻訳。 |
| [!UICONTROL Log JS Errors to Session Storage] | グローバル | 有効にすると、機能テストでレポートに使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | グローバル | 収集された js エラーを取得するために使用されるキーを識別します。 |

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS 設定 &#x200B;](./assets/developer-css-settings.png)<!-- zoom -->

これらの設定の変更方法については、『 [&#x200B; 管理システムガイド _の &#x200B;](../../systems/developer-tools.md#optimizing-resource-files) リソースファイルの最適化_ を参照してください。

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | ストア表示 | 複数の CSS ファイルを 1 つのファイルに結合して、ページの読み込み時間を短縮します。 オプション：`Yes` / `No` |
| [!UICONTROL Minify CSS Files] | ストア表示 | 不要な文字、スペース、インデントを削除して、コードのサイズを小さくします。 オプション：`Yes` / `No` |
| [!UICONTROL Use CSS critical path] | グローバル | _CSS 重要パス_ は、縮小された重要な CSS を `<head>` でインライン配信し、非同期で読み込まれる重要でないすべてのスタイルを延期します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![&#x200B; 画像処理設定 &#x200B;](./assets/developer-image-processing-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | グローバル | イメージのレンダリングに使用するアダプタを指定します。 アダプターの設定を変更した後、カタログ画像のキャッシュをフラッシュします。 オプション：`PHP GD2` / `ImageMagick` <br/><br/>**_注意：_**&#x200B;ICO ファイルタイプは ImageMagik アダプタでのみサポートされています。 |

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![&#x200B; キャッシュ設定 &#x200B;](./assets/developer-cache-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | グローバル | 有効な場合、はユーザー定義の属性およびシステムエンティティ属性値（EAV）属性をキャッシュします。 このオプションを使用するとパフォーマンスが向上する可能性がありますが、キャッシュ用に追加のスペースが必要になることもあります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![&#x200B; 静的ファイル設定 &#x200B;](./assets/developer-static-files-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | グローバル | 有効にすると、静的ファイルの URL にデジタル署名が追加され、ブラウザーでファイルの新しいバージョンが使用可能かどうかを検出できるようになります。 ファイルの署名がブラウザーのキャッシュに格納されている署名と異なる場合は、ファイルの新しいバージョンが使用されます。 署名可能な静的ファイルには、JavaScript、CSS、画像、フォントなどがあります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![&#x200B; グリッド設定 &#x200B;](./assets/developer-grid-settings.png)<!-- zoom -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | 注文、請求書、出荷、クレジット メモなどの注文処理システム エンティティをグリッドに追加し、インデックスを再作成するタイミングを決定します。 非同期インデックス作成を使用すると、保存操作中のデータのロックを回避し、処理時間を短縮できます。 オプション：<br/>**`Disable`**- （デフォルト）順序に関連するエンティティは、様々なタイミングでグリッドに追加されます。 保存されたとおりに。<br/>**`Enable`** – 注文関連のエンティティは、スケジュールされた cron ジョブの実行中にのみグリッドに追加されます。 Cron は 1 分ごとに 1 回実行されるように設定する必要があります。 |

{style="table-layout:auto"}
