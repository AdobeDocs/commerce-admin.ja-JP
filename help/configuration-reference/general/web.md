---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Commerce Admin の [!UICONTROL General] &gt; [!UICONTROL Web] ページで設定を確認します。
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > 一般オプション &#x200B;](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | 範囲 | 説明 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web Server Rewrites が有効な場合、は現在のビューのストア・コードを URL に挿入します。 オプション：`Yes`/`No`。 <br /> このフィールドを `Yes` に設定した場合、URL の書き換えが正しくマッピングされ、すべてのページが正常に開かれるように、ブラウザーの URL にストアコードを含める必要があります。 これにより、_404 Page Not Found_ エラーが回避されます。 |
| [!UICONTROL Auto-redirect to Base URL] | ストア表示 | （シングルストア設定の場合）サイトに壊れたリンクがある場合、は、「404 Page Not Found」というメッセージを含んだページではなく、ベース URL にトラフィックをリダイレクトします。 オプション：` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Important:_** マルチストアの設定では、自動リダイレクトをベース URL に使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | 製品およびカテゴリに割り当てる [URL 形式 &#x200B;](../../catalog/catalog-urls.md) を定義します。 オプション：画像バリアントごとの一意のハッシュ（レガシーモード）は、変換されたファイル名を一意のハッシュ値として定義します。 クエリパラメーターに基づく画像の最適化では、クエリパラメーターに応じてプロセスを [&#x200B; 画像の最適化 &#x200B;](../../content-design/media-gallery-image-optimization.md) 定義します。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > 検索エンジンの最適化 &#x200B;](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | ストア表示 | PHP ベースのシステムでは、通常、ルートフォルダーに `index.php` というファイルが含まれます。 デフォルトでは、URL 内で、ルートフォルダー名の直後にファイル名が表示されます。 これが有効な場合、URL から `index.php` が省略されます。 この使いやすさのベストプラクティスにより、各 URL がより簡潔になり、パフォーマンスやサイトのランクには影響しません。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > ベース URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base URL] | ストア表示 | 暗号化（SSL）チャネルで動作していないCommerce ルートフォルダーのフルアドレス。 URL の末尾はスラッシュにする必要があります。 |
| [!UICONTROL Base Link URL] | ストア表示 | ベース URL のプレースホルダーとして使用されるマークアップタグ。 |
| [!UICONTROL Base URL for Static View Files] | ストア表示 | CSS、フォント、画像、JavaScriptなど、テーマで使用される静的ファイルの場所を指すパス。 プレースホルダーは、ベース URL を表すために使用されます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合、サイトごとに異なるフォルダーを使用できます。 静的ビューファイルのベース URL を入力する前に、設定範囲を正しいサイトに設定してください。 Commerceのインストール環境の外部でフォルダーを指定することもできます。 |
| [!UICONTROL Base URL for User Media Files] | ストア表示 | カタログ イメージおよびその他のメディア ファイルの場所を指すパス。 プレースホルダーは、ベース URL を表すために使用されます。 Commerceのインストールに同じフォルダー構造の複数のサイトがある場合、それぞれに異なるメディアフォルダーを使用できます。 これにより、各メディア フォルダを個別にバックアップおよびロールバックできます。 Commerceのインストール環境の外部でメディアフォルダーを指定することもできます。 |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > ベース URL （セキュア） &#x200B;](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | ストア表示 | 暗号化されたセキュア （SSL/TLS） プロトコルで配信されるCommerce ルートフォルダーのフルアドレス。 URL の末尾はスラッシュにする必要があります。 |
| [!UICONTROL Secure Base Link URL] | ストア表示 | 安全なチャネルで実行されるベース URL のプレースホルダーとして使用されるマークアップタグ。 |
| [!UICONTROL Secure Base URL for Static View Files] | ストア表示 | テーマで使用される CSS、フォント、画像、JavaScriptなどの静的ファイルの場所を指すマークアップタグ。 ファイルは、安全でないチャネルまたは安全なチャネルのどちらかに置くことができます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合、サイトごとに異なるフォルダーを使用できます。 静的ビューファイルのベース URL を入力する前に、設定範囲を正しいサイトに設定してください。 Commerceのインストール環境の外部でフォルダーを指定することもできます。 |
| [!UICONTROL Secure Base URL for User Media Files] | ストア表示 | カタログ イメージおよびその他のメディア ファイルの場所を指すパス。 ファイルは、安全でないチャネルまたは安全なチャネルのどちらかに置くことができます。 プレースホルダーは、ベース URL を表すために使用されます。 Commerceのインストールに同じフォルダー構造の複数のサイトがある場合、それぞれに異なるメディアフォルダーを使用できます。 これにより、各メディア フォルダを個別にバックアップおよびロールバックできます。 Commerceのインストール環境の外部でメディアフォルダーを指定することもできます。 |
| [!UICONTROL Use Secure URLs on Storefront] | ストア表示 | ドメインにセキュリティ証明書がある場合は、SSL 暗号化付きまたは SSL 暗号化なしでストアフロントを実行するように選択できます。 オプション：<br />**`Yes`**- ストア URL の先頭は `https` で、暗号化されたセキュアなプロトコルでページが配信されることを示します。<br />**`No`** - ストア URL は `http` で始まり、セキュアなプロトコルを使用せずにページが配信されることを示します。 |
| [!UICONTROL Use Secure URLs in Admin] | グローバル | ドメインにセキュリティ証明書がある場合は、SSL 暗号化の有無にかかわらず、ストア管理を実行するように選択できます。 オプション：<br />**`Yes`**– 管理 URL は `https` で始まり、暗号化された安全なプロトコルでページが配信されることを示します。<br />**`No`** – 管理 URL は `http` で始まり、セキュアなプロトコルを使用せずにページが配信されることを示します。<br /> ストアと管理者の両方でセキュア URL が有効になっている場合、2 つの追加フィールドが表示され、`HSTS` を有効にして設定できます。 |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | ストア表示 | 有効にすると、[`HSTS`](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html) は「man in the middle」攻撃に対するセキュリティ対策を提供し、「invalid certificate」メッセージを上書きするのを防ぎます。 オプション：`Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | ストア表示 | 有効にすると、ブラウザーから受信した保護されていない（`HTTP`）要求が、保護された（`HTTPS`）プロトコルに変換されます。 オプション：`Yes` / `No` |
| [!UICONTROL Offloader Header] | グローバル | クライアントとロード バランサー間のプロトコルを識別するためのサーバー構成の `offloader_header` 値を指定します。 ほとんどのCommerce インストールでは、プロトコルを `X-Forwarded-Proto` または `HTTP` として識別するために、デフォルト値の `HTTPS` （XFP）が使用されています。 |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web/デフォルトページ &#x200B;](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | ストア表示 | ベース URL に関連付けられているランディングページを示します。 これは、Commerce コンテンツ管理システム（CMS）からのページを示すために、デフォルトで「cms」に設定されます。 また、ブログなど、別のタイプのランディングページを使用することもできます。 例えば、`magento/blog` にサーバーにブログがインストールされている場合、選択したページへの相対パスとして「blog」フォルダーの名前を入力できます。 |
| [!UICONTROL CMS Home Page] | ストア表示 | ストアのホームページを選択するには、リストからCMSページを選択します。 デフォルトでは、CMSのホームページには、ストアで使用可能なCMSのページの選択全体が一覧表示されます。 |
| [!UICONTROL Default No-route URL] | ストア表示 | `404 Page not Found` エラーが発生したときに表示されるデフォルトのページの URL が含まれます。 デフォルト値は `cms/noroute/index` です。 |
| [!UICONTROL CMS No Route Page] | ストア表示 | 404 ページが見つからないというエラーが発生した場合に表示する、特定のCMS ページを指定します。 デフォルトのページは「404 Not Found」です。 |
| [!UICONTROL CMS No Cookies Page] | ストア表示 | ブラウザーで Cookie が有効になっていない場合に表示される特定のCMSページを識別します。 このページでは、cookie が使用される理由と、各ブラウザーで cookie を有効にする方法について説明します。 デフォルトのページでは、Cookie を有効にします。 |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | ストア表示 | パンくずリストをカタログ内のすべてのCMS ページに表示するかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![&#x200B; デフォルトのレイアウト &#x200B;](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/ja/docs/commerce-admin/content-design/design/layout/page-layout) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | グローバル | 製品ページにデフォルトで使用される [&#x200B; レイアウト &#x200B;](../../content-design/page-layout.md) を決定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、製品ページのレイアウトのアップデートは使用できません。<br/>**`Empty`** - デフォルトでは、は製品ページに空白のレイアウトを使用します。 <br/>**`1 column`**- デフォルトでは、製品ページに 1 列のレイアウトを使用します。<br/>**`2 columns with left bar`** - デフォルトでは、製品ページ用にサイドバーが左側にある 2 列のレイアウトを使用します。 <br/>**`2 columns with right bar`**- デフォルトでは、は製品ページ用にサイドバーが右側にある 2 列のレイアウトを使用します。<br/>**`3 columns`** - デフォルトでは、は製品ページに対して左右にサイドバーを持つ 3 列のレイアウトを使用します。<br/>**`Page -- Full Width`**- （[!DNL Page Builder] が必要）デフォルトでは、製品ページの「ページ – 全幅」レイアウトを使用します。<br/>**`Category - Full Width`** - （[!DNL Page Builder] が必要）デフォルトでは、製品ページに対して「カテゴリ – 全幅」レイアウトを使用します。 <br/>**`Product - Full Width`**- （[!DNL Page Builder] が必要）デフォルトでは、製品ページに対して「製品 – 全幅」レイアウトを使用します。 |
| [!UICONTROL Default Category Layout] | グローバル | カテゴリページにデフォルトで使用される [&#x200B; レイアウト &#x200B;](../../content-design/page-layout.md) を決定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、カテゴリページのレイアウト更新は使用できません。<br/>**`Empty`** - デフォルトでは、はカテゴリページに空白のレイアウトを使用します。 <br/>**`1 column`**- デフォルトでは、カテゴリページに 1 列のレイアウトを使用します。<br/>**`2 columns with left bar`** - デフォルトでは、は、カテゴリページ用にサイドバーが左側にある 2 列のレイアウトを使用します。 <br/>**`2 columns with right bar`**- デフォルトでは、は、カテゴリページ用にサイドバーが右側にある 2 列のレイアウトを使用します。<br/>**`3 columns`** - デフォルトでは、はカテゴリページに対して左右にサイドバーを持つ 3 列のレイアウトを使用します。<br/>**`Page - Full Width`**- （[!DNL Page Builder] が必要）デフォルトでは、カテゴリページに「ページ – 全幅」レイアウトを使用します。<br/>**`Category - Full Width`** - （[!DNL Page Builder] が必要）デフォルトでは、カテゴリページに対して「カテゴリ – 全幅」レイアウトを使用します。 <br/>**`Product - Full Width`**- （[!DNL Page Builder] が必要）デフォルトでは、カテゴリページに対して「製品 – 全幅」レイアウトを使用します。 |
| 既定のページ レイアウト | グローバル | CMSページに対してデフォルトで使用される [&#x200B; レイアウト &#x200B;](../../content-design/page-layout.md) を指定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、CMS ページのレイアウト更新は使用できません。<br/>**`Empty`** - デフォルトでは、はCMS ページに空白のレイアウトを使用します。 <br/>**`1 column`**- デフォルトでは、CMSページに 1 列のレイアウトを使用します。<br/>**`2 columns with left bar`** - デフォルトでは、CMS ページ用にサイドバーが左側にある 2 列のレイアウトを使用します。<br/>**`2 columns with right bar`**- デフォルトでは、CMS ページの右側にサイドバーがある 2 列のレイアウトを使用します。<br/>**`3 columns`** - デフォルトでは、CMS ページに対して左右にサイドバーを持つ 3 列のレイアウトを使用します。<br/>**`Page - Full Width`**- （[!UICONTROL Page Builder] が必要）デフォルトでは、CMSページに対して「ページ – 全幅」レイアウトを使用します。<br/>**`Category - Full Width`** - （[!UICONTROL Page Builder] が必要）デフォルトでは、CMSページに対して「カテゴリ – 全幅」レイアウトを使用します。 <br/>**`Product - Full Width`**- （[!DNL Page Builder] が必要）デフォルトでは、CMS ページに対して「製品 – 全幅」レイアウトを使用します。 |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web/デフォルトの Cookie 設定 &#x200B;](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | ストア表示 | cookie が自動的に削除されるまでに、その cookie が存在できる期間を決定します。 デフォルト値は 3600 秒（1 時間）です |
| [!UICONTROL Cookie Path] | ストア表示 | Commerce Cookie を使用できるサーバー上のフォルダーを指定します。 インストール内のすべての場所でCommerce Cookie を使用できるようにするには、Cookie のパスをスラッシュ `/` に設定します。 この値には、cookie パスのみを含めることができ、その他の cookie パラメーターを含めることはで **_ません_**。 |
| [!UICONTROL Cookie Domain] | ストア表示 | サブドメインでCommerce Cookie を使用できるかどうかを決定します。 例えば、`mysubdomain`.domain.comをサポートするには、ドメイン名の先頭にピリオドを付けて入力します（例：`.domain.com`）。 この値には、cookie ドメインのみを含めることができ、その他の cookie パラメーターを含めること **_できません_**。 |
| [!UICONTROL Use HTTP Only] | ストア表示 | Commerce Cookie を保護されていないチャネル（http）でのみ使用するか、暗号化されたチャネル（https）でも使用するかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Web サイト | cookie 制限モードが有効かどうかを判断します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > セッションの検証 &#x200B;](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | グローバル | リクエストの IP アドレスが `$_SESSION` のデータと一致することを確認します。 別の IP アドレスが検出されると、セッションは終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | グローバル | 受信プロキシデータを検証し、リクエストのプロキシアドレスが `$_SESSION` のデータと一致することを確認します。 別のプロキシ アドレスが検出されると、セッションは終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | グローバル | 送信プロキシデータを検証し、転送されたリクエストのアドレスが `$_SESSION` のデータと一致するかどうかを確認します。 転送先アドレスに別のアドレスが検出されると、セッションは終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | グローバル | `USER_AGENT` は、web サイトへのアクセスに使用するブラウザーまたはデバイスを指します。 ブラウザーの名前とバージョン、およびオペレーティングシステムが `$_SESSION` のデータと一致するかどうかを確認します。 同じセッション内のあるリクエストから別のリクエストに異なるユーザーエージェントが検出された場合、セッションは終了します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > ブラウザー機能の検出 &#x200B;](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/ja/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| フィールド | [&#x200B; 範囲 &#x200B;](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | ストア表示 | ブラウザーで Cookie が無効になっている場合は、CMSの Cookie が無効ページに自動的にリダイレクトされます。 オプション：`Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | ストア表示 | ブラウザーでJavaScriptが無効になっている場合は、JavaScript オプションを有効にするよう求める次の通知が表示されます。`Yes` / `No` （無効） |
| [!UICONTROL Show Notice if Local Storage is Disabled] | ストア表示 | ローカルキャッシュが無効な場合にメッセージを表示します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}
