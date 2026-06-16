---
title: '[!UICONTROL Advanced] > [!UICONTROL Developer]'
description: Commerce管理者の[!UICONTROL Advanced] > [!UICONTROL Developer] ページで設定を確認します。
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
TQID: https://experienceleague.adobe.com/Cl6rp-pqD6LBM-50gDiPC-7Ox2MDzy-szQDesLTecdQ
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c1256247-af4b-46d8-9dca-0c654ecfa157id: cc250cf1-34eb-4863-80d0-d170d45ea067id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>これらの設定設定は、[開発者モード ](../../systems/developer-tools.md#operation-modes)でのみ使用できます。

## [!UICONTROL Frontend Development Workflow]

![ フロントエンド開発ワークフロー](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の[ フロントエンド開発ワークフロー](../../systems/developer-tools.md#frontend-development-workflow)を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | グローバル | 開発中にクライアントサイドまたはサーバーサイドでコンパイルが少なくなるかどうかを決定します。 オプション：<br/>**`Client side less compilation`**- コンパイルは、ネイティブ less.js ライブラリを使用してブラウザーで行われます。<br/>**`Server side less compilation`** - コンパイルは、Less PHP ライブラリを使用してサーバー上で実行されます。 これは実稼動のデフォルトモードです。 |

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![開発者クライアントの制限](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

この設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ クライアントの制限](../../systems/developer-tools.md#client-restrictions)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | ストアビュー | ストア内のお客様に影響を与えることなく、ライブサイトでデベロッパーツールを使用できるIP アドレスの許可リストを作成します。 _インライン翻訳_&#x200B;などの開発者用ツールを使用する際にサイトに加えられた変更は、Web ページのIP アドレスからのみ表示されます。 インライン翻訳などの開発者用ツールを使用する場合、サイトに加えられた変更は、Web 許可リスト上のIP アドレスからのみ表示されます。 |

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![ テンプレート設定](./assets/developer-template-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | ストアビュー | [ シンボリックリンク ](https://en.wikipedia.org/wiki/Symbolic_link)を有効にすると、サイトがセキュリティリスクにさらされる可能性があるため、実稼動ストアには推奨されません。 |
| [!UICONTROL Minify Html] | ストアビュー | ストアテンプレートのHTMLを最小化するかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Debug]

![ デバッグ ](./assets/developer-debug.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ テンプレートのパスヒント ](../../systems/developer-tools.md#template-path-hints)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | ストアビュー | ページで使用される各テンプレートへのパスを示す表記をストアフロントに追加します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | グローバル | ページで使用されている各テンプレートへのパスを示す注釈を管理者に追加します。 オプション：`Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | ストアビュー | テンプレートパスのヒントにブロックの名前を含めます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![ インラインの翻訳](./assets/developer-translate-inline.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ インライン翻訳](../../systems/developer-tools.md#translate-inline)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | ストアビュー | ストアフロントのインライン翻訳機能を有効にします。 インターフェイスのテキストは、ストアビューごとに編集できます。 ライブストアを妨げずにインライントランスレーターを使用するには、Developer Client Restrictionsの許可リストにIP アドレスを追加します。 |
| [!UICONTROL Enable for Admin] | グローバル | 管理者のインライン翻訳者をアクティブにします。 ストアフロントとは異なり、管理者は複数の言語に翻訳できません。 ただし、インターフェイス内のフィールドラベルやその他のテキストは変更できます。 |

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScript設定](./assets/developer-javascript-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | ストアビュー | 複数のJavaScriptファイルを1つのファイルに結合し、ページの読み込み時間を短縮します。 |
| [!UICONTROL Enable JavaScript Bundling] | ストアビュー | 複数のJavaScript ファイルを1つのファイルにバンドルできるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | ストアビュー | 不要な文字、スペース、インデントを削除して、コードのサイズを縮小します。 |
| [!UICONTROL Move JS code to the bottom of the page] | グローバル | 有効にすると、JS コードがページの下部に移動します。 オプション：`Yes` / `No` |
| [!UICONTROL Translation Strategy] | グローバル | システムで使用される翻訳方法を決定します。 オプション：<br/>**`Dictionary`**- ストアフロント側の翻訳。<br/>**`Embedded`** – 管理者側の翻訳。 |
| [!UICONTROL Log JS Errors to Session Storage] | グローバル | 有効にすると、はレポート用の機能テストで使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | グローバル | 収集されたjs エラーの取得に使用されるキーを識別します。 |

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS設定](./assets/developer-css-settings.png)<!-- zoom -->

これらの設定の変更について詳しくは、_管理者システムガイド_&#x200B;の「[ リソースファイルの最適化](../../systems/developer-tools.md#optimizing-resource-files)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | ストアビュー | 複数のCSS ファイルを1つのファイルに結合して、ページの読み込み時間を短縮します。 オプション：`Yes` / `No` |
| [!UICONTROL Minify CSS Files] | ストアビュー | 不要な文字、スペース、インデントを削除して、コードのサイズを縮小します。 オプション：`Yes` / `No` |
| [!UICONTROL Use CSS critical path] | グローバル | _CSS クリティカルパス_&#x200B;は、`<head>`に縮小されたクリティカル CSS インラインを提供し、非同期的に読み込まれるすべての非クリティカル スタイルを延期します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![画像処理設定](./assets/developer-image-processing-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | グローバル | 画像のレンダリングに使用するアダプタを指定します。 アダプター設定を変更した後、カタログ画像キャッシュをフラッシュします。 オプション：`PHP GD2` / `ImageMagick` <br/><br/>**_Note:_** ICO ファイルタイプは、ImageMagik アダプタでのみサポートされています。 |

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![設定のキャッシュ ](./assets/developer-cache-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | グローバル | 有効にすると、ユーザー定義およびシステム エンティティ属性値（EAV）属性がキャッシュされます。 このオプションを選択すると、パフォーマンスが向上する可能性がありますが、キャッシュに追加の容量が必要になります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![静的ファイル設定](./assets/developer-static-files-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | グローバル | 有効にすると、静的ファイルのURLにデジタル署名が追加され、ブラウザーで新しいバージョンのファイルが使用可能な場合に検出できるようになります。 ファイルの署名がブラウザーのキャッシュに保存されているものと異なる場合は、新しいバージョンのファイルが使用されます。 署名できる静的ファイルには、JavaScript、CSS、画像、フォントなどがあります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![ グリッド設定](./assets/developer-grid-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | 注文、請求書、出荷、クレジットメモなどの注文処理システムのエンティティをグリッドに追加し、インデックスを再作成するタイミングを指定します。 非同期インデックス作成を使用すると、保存操作中のデータのロックを回避し、処理時間を短縮できます。 オプション：<br/>**`Disable`**- （デフォルト）注文関連のエンティティは、様々なタイミングでグリッドに追加されます。 自動的にラベル付けされます。<br/>**`Enable`** – 順序関連のエンティティは、スケジュールされたcron ジョブ中にのみグリッドに追加されます。 Cronは、毎分1回実行するように設定する必要があります。 |

{style="table-layout:auto"}
