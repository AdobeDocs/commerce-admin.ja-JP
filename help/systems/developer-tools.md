---
title: デベロッパーツール
description: カスタマイズプロジェクトに取り組む開発者をサポートするために使用できる高度な開発者ツールについて説明します。
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---

# デベロッパーツール

高度な開発者ツールを使用して、フロントエンド開発時のコンパイルモードの決定、IP アドレスの許可リストの作成、テンプレートパスヒントの表示を行います。 また、ストアフロントと管理者のインターフェイスで、テキストを簡単にスポット変更するためのツールもあります。

- [アクションログ](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）
- [フロントエンド開発ワークフロー](#frontend-development-workflow)
- [静的ファイル署名の使用](#static-file-signatures)
- [リソースファイルの最適化](#optimizing-resource-files)
- [開発者クライアントの制限](#client-restrictions)
- [テンプレートパスのヒント](#template-path-hints)
- [インライン翻訳](#translate-inline)

## 操作モード

Adobe CommerceまたはMagento Open Sourceインスタンスは、次のいずれかでデプロイして実行できます _実稼動_ または _開発者モード_. 開発者向けに設計されたツールと設定は、ストアがで動作している間のみアクセスできます _開発者モード_.

操作モードは、適切な権限を持つユーザーがサーバーのコマンドラインからのみ変更できます。 参照： [操作モードの設定](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html) が含まれる _設定ガイド_ を参照してください。

マーチャントドキュメントのほとんどのトピックは、実稼動モードで実行されているCommerce インスタンスに適用されます。 ただし、次の設定とツールは、インストールが開発者モードで実行されている場合にのみ使用できます。

## フロントエンド開発ワークフロー

フロントエンド開発ワークフローのタイプは、開発中にクライアントサイドまたはサーバーサイドで少ないコンパイルが行われるかどうかを決定します。 Less は、追加の機能と規則を持ち、合理化されたコードを生成する CSS の拡張機能です。 テーマの開発には、クライアントサイドの LESS コンパイルをお勧めします。 サーバーサイドのコンパイルはデフォルトのモードです。 開発ワークフローオプションは、実稼動モードのストアでは使用できません。
参照： [クライアントサイド LESS コンパイルとサーバーサイドの比較](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/){:target=&quot;_blank&quot;} （Commerce開発者向けドキュメント）。

>[!NOTE]
>
>フロントエンド開発ワークフローの設定は、で利用できます。 [開発者モード](../systems/developer-tools.md#operation-modes) のみ。

![詳細設定 – フロントエンド開発ワークフロー](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Front-end Development Workflow]** セクション。

1. を設定 **[!UICONTROL Workflow Type]** を次のいずれかに変更します。

   - `Client side less compilation` - コンパイルは、ネイティブを使用したブラウザーで実行されます `less.js` ライブラリ。
   - `Server side less compilation` - コンパイルは、Less PHP ライブラリを使用してサーバ上で実行されます。 これは、実稼動用のデフォルトのモードです。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 静的ファイル署名

静的ファイルの URL にデジタル署名を追加すると、ブラウザーはファイルの新しいバージョンが使用可能かどうかを検出できます。 デジタル署名で追跡できる静的ファイルには、JavaScript、CSS、画像、フォントなどがあります。 署名は、ベース URL の直後のパスに追加されます。 ファイルの署名がブラウザーのキャッシュに格納されている署名と異なる場合は、ファイルの新しいバージョンが使用されます。

参照： [静的コンテンツ署名](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html){:target=&quot;_blank&quot;} （Commerce開発者向けドキュメント）。

>[!NOTE]
>
>静的ファイル設定の設定は、で作業しているときにのみ使用できます [開発者モード](../systems/developer-tools.md#operation-modes).

![詳細設定 – 静的ファイルの設定](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

設定の詳細なリストについては、を参照してください [_静的ファイル設定_](../configuration-reference/advanced/developer.md) が含まれる _設定リファレンス_.

**_署名済み静的ファイルを有効にするには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Static Files Settings]** セクション。

1. を設定 **[!UICONTROL Sign Static Files]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

## リソースファイルの最適化

リソースファイルの読み込みに要する時間は、ファイルを結合およびバンドルし、コードを最小限に抑えることで短縮できます。

- 結合すると、同じ種類の別々のファイルが 1 つのファイルに結合されます。
- バンドルは、ページの読み込みに必要な HTTP リクエスト数を減らすために、別々のファイルをグループ化する技術です。
- 縮小によってスペース、改行、コメントは削除されますが、コードの機能には影響しません。 最小化されたファイルは編集できないので、プロセスは、実稼動に移行する準備が整った場合にのみ適用してください。

デフォルトでは、Adobe CommerceとMagento Open Sourceはファイルの結合、バンドル、最小化を行わないので、プロジェクト開発者はどのファイル最適化方法を使用するかを決定する必要があります。

参照： [パフォーマンスのベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html) を参照してください。

>[!NOTE]
>
>CSS ファイルと JavaScript ファイルは、で最適化できます [開発者モード](../systems/developer-tools.md#operation-modes) のみ。

| ファイルタイプ | サポートされる操作 |
| --------------- | -------------------- |
| CSS ファイル | `MergeMinify` |
| JavaScript ファイル | `MergeBundleMinify` |
| テンプレートファイル | `Minify` |

{style="table-layout:auto"}

**_リソースファイルを最適化するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. CSS ファイルを最適化するには、を展開します。 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CSS Settings]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Merge CSS Files]** 対象： `Yes`.
   - を設定 **[!UICONTROL Minify CSS Files]** 対象： `Yes`.

   ![詳細設定 – CSS 設定](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[_CSS 設定_](../configuration-reference/advanced/developer.md)

1. Javascript ファイルを最適化するには、を展開します ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL JavaScript Settings]** を選択し、次の操作を実行します。

   - を設定 **[!UICONTROL Merge JavaScript Files]** 対象： `Yes`.
   - を設定 **[!UICONTROL Minify JavaScript Files]** 対象： `Yes`.

   ![詳細設定 – JavaScript 設定](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. PHTML テンプレートファイルを縮小するには、を展開します ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Template Settings]** セクションとセット **[!UICONTROL Minify Html]** 対象： `Yes`.

   ![詳細設定 – テンプレート設定](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## クライアントの制限

などのツールを使用する前に [テンプレートパスのヒント](#template-path-hints)許可リストに加える ストア内の顧客のショッピングエクスペリエンスを中断しないように、IP アドレスを Developer Client Restrictions に追加してください。 IP アドレスがわからない場合は、オンラインで検索できます。

>[!NOTE]
>
>Developer Client Restrictions は、 [開発者モード](../systems/developer-tools.md#operation-modes) のみ。

技術情報については、を参照してください [リクエストを許可するカスタム VCL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html) が含まれる _クラウドインフラストラクチャー上のCommerce ガイド_.

**_許可リストに加えるに IP アドレスを追加するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Developer Client Restrictions]** セクション。

   ![詳細設定 – デベロッパークライアントの制限](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Allow IPs]**&#x200B;に IP アドレスを入力します。

   複数の IP アドレスからアクセスする必要がある場合は、各アドレスをコンマで区切ります。

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、無効なキャッシュを更新します。

## テンプレートパスのヒント

テンプレートパスヒントは、ページで使用される各テンプレートへのパスを含む表記を追加する診断ツールです。 テンプレートパスのヒントは、ストアフロントまたは管理者に対して有効にできます。

>[!NOTE]
>
>テンプレートパスのヒントは、で編集できます [開発者モード](../systems/developer-tools.md#operation-modes) のみ。

参照： [テンプレート、レイアウト、スタイルを検索する](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/){:target=&quot;_blank&quot;} （Commerce開発者向けドキュメント）。

![ストアフロントの例 – テンプレートのパスのヒント](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### 許可リストに加える手順 1：に IP アドレスを追加する

テンプレートパスヒントを使用する前に、IP アドレスをに追加します [許可リスト](#client-restrictions) 店舗で買い物をしている顧客への干渉を回避する。 完了したら、必ずCommerceのキャッシュをクリアして、ストアからすべてのヒントを削除します。

![詳細設定 – デベロッパークライアントの制限](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### 手順 2：テンプレートパスヒントを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Debug]** を選択し、次の操作を実行します。

   ![詳細設定 – デバッグ](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - ストアに対してテンプレートパスヒントをアクティブにするには、次を設定します **[!UICONTROL Enabled Template Path Hints for Storefront]** 対象： `Yes`.

   - URL に次の値が含まれる場合にのみ、ストアのテンプレートパスヒントを有効にします： `templatehints` パラメーター、設定 **URL パラメーターを使用してストアフロントのヒントを有効にする** 対象： `Yes`. 必要に応じて、パラメーターの値を設定します。 デフォルト値はです `magento`ただし、カスタム値を使用できます。 例えば、値をに変更した場合 `lorem`を使用する場合は、 `mymagento.com?templatehints=lorem` テンプレートのヒントを表示します。

   - 管理者用のテンプレートパスヒントをアクティブにするには、次を設定します **[!UICONTROL Enabled Template Path Hints for Admin]** 対象： `Yes`.

   - ブロック名を含めるには、を設定します **[!UICONTROL Add Block Class Type to Hints]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

### 手順 3：キャッシュのクリア

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 右上隅のをクリックします。 **[!UICONTROL Flush Magento Cache]**.

## インラインで翻訳

で Translate Inline ツールを使用できます。 [開発者モード](../systems/developer-tools.md#operation-modes) 音声やブランドを反映させるために、インターフェイスでテキストにタッチします。 インライン翻訳モードをアクティブにすると、ページ上の編集可能なテキストがすべて赤で描画されます。 フィールドラベル、メッセージなど、ストアフロントおよび管理者全体に表示されるテキストを簡単に編集できます。 例えば、多くのテーマは、次のような用語を使用しています _マイアカウント_, _自分のウィッシュリスト_、および _マイダッシュボード_&#x200B;お客様がスムーズに作業できるように、 ただし、単に単語を使用する方がよいでしょう _アカウント_, _ウィッシュリスト_、および _Dashboard_.

>[!NOTE]
>
>Translate Inline ツールは、で作業しているときにのみ使用できます [開発者モード](../systems/developer-tools.md#operation-modes).

参照： [翻訳の概要](https://developer.adobe.com/commerce/frontend-core/guide/translations/) Commerce開発者向けドキュメント

![ストアフロントの例 – 翻訳可能なテキスト](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

ストアが複数の言語で使用できる場合は、ロケールの翻訳済みテキストを微調整できます。 サーバー上では、インターフェイステキストは、出力ブロックごとに個別の CSV ファイルに保持され、ロケール別に整理されます。 を使用するのではなく、別のアプローチとして使用します _インライン翻訳_ このツールを使用して、CSV ファイルをサーバー上で直接編集することもできます。 翻訳ファイルの保存場所 `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>インライン翻訳ツールを使用するには、ブラウザーでポップアップを許可する必要があります。

### 手順 1：出力キャッシュを無効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 次のチェックボックスをオンにします。

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. を **[!UICONTROL Actions]** コントロール先 `Disable` をクリックして、 **[!UICONTROL Submit]**.

### 手順 2：インライン翻訳ツールを有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 特定のストア表示を使用するには、 **[!UICONTROL Store View]** を更新します。

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Translate Inline]** セクション。

   をクリア **[!UICONTROL Use Website]** これらの設定を変更するには、必要に応じて「」チェックボックスをオンにします。

   この _[!UICONTROL Enabled for Admin]_特定のストア表示を編集する場合は、オプションを使用できません。

   ![詳細設定 – インライン翻訳](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled for Storefront]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、無効なキャッシュを更新しますが、無効なキャッシュは今のところそのままにしておきます。

### 手順 3：テキストを更新

1. ブラウザーでストアフロントを開き、編集するページに移動します。

   必要に応じて、言語選択を使用してストア表示を変更します。 翻訳可能なテキストの各文字列は、赤で囲まれます。 テキストボックスにポインタを合わせると、ブックのアイコン（ ![ブックアイコン](../assets/icon-book.png) ）が表示されます。

1. ブックアイコンをクリックして、 _翻訳_ ウィンドウを開いて、次の手順を実行します。

   - 特定のストア表示に対する変更の場合は、 **[!UICONTROL Store View Specific]** チェックボックス。

   - 新しい **[!UICONTROL Custom]** テキスト。

1. 完了したら、 **[!UICONTROL Submit]**.

   ![カスタムテキストを入力](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. ストアで変更を確認するには、ブラウザーを更新します。

1. ストア内の変更する要素すべてについて、この手順を繰り返します。

### 手順 4：元の設定を復元する

1. ストアの管理者に戻ります。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. を設定 **[!UICONTROL Store View]** を編集した特定のビューに追加します。

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Developer]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Translate Inline]** セクション。

1. を設定 **[!UICONTROL Enabled for Frontend]** 対象： `No`.

1. 完了したら、 **[!UICONTROL Save Config]**.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 以前に無効にした次の出力キャッシュのチェックボックスを選択します。

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. を **[!UICONTROL Actions]** コントロール先 `Enable` をクリックして、 **[!UICONTROL Submit]**.

1. プロンプトが表示されたら、無効なキャッシュを更新します。

### 手順 5：ストアでの変更の検証

ストアフロントに移動し、更新された各ページを調べて、変更が正しいことを確認します。 この例では、 `Customer Login` がに変更されました `Customer Sign In`. 特定のビューを変更した場合は、言語選択を使用して正しいビューに切り替えます。

![ストアフロントの例 – 翻訳済み顧客のログイン](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
