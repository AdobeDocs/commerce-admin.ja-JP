---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: 次のページで設定を確認します： [!UICONTROL General] &gt; [!UICONTROL Web] コマース管理のページ。
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web /一般オプション](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| フィールド | 範囲 | 説明 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web サーバーの書き換えが有効な場合、現在のビューのストアコードを URL に挿入します。 オプション： `Yes` / `No`. <br />このフィールドが `Yes`を使用する場合、URL の書き換えが正しくマッピングされ、すべてのページが正常に開かれるようにするには、ブラウザーの URL にストアコードを含める必要があります。 これで回避できます _404 ページが見つかりません_ エラー。 |
| [!UICONTROL Auto-redirect to Base URL] | ストア表示 | （シングルストアの設定の場合）サイトに壊れたリンクがある場合、は「404 Page Not Found」メッセージを含むページではなく、トラフィックをベース URL にリダイレクトします。 オプション：` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_重要：_**マルチストアの設定では、ベース URL への自動リダイレクトを使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | を定義します。 [URL フォーマット](../../catalog/catalog-urls.md) 製品およびカテゴリに割り当てられました。 オプション：画像バリアントごとの一意のハッシュ（レガシーモード）では、変換されたファイル名を一意のハッシュ値として定義します。 クエリパラメーターに基づく画像の最適化の定義 [画像最適化](../../content-design/media-gallery-image-optimization.md) プロセスを実行できます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Optimization]

![Web /検索エンジン最適化](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | ストア表示 | 通常、PHP ベースのシステムには、 `index.php` をルートフォルダーに追加します。 デフォルトでは、ファイル名は URL 内のルートフォルダーの名前の直後に表示されます。 これを有効にすると、システムは省略します。 `index.php` を URL から取得します。 この操作性のベストプラクティスは、各 URL をより簡潔にし、パフォーマンスやサイトランクに影響を与えません。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs]

![Web /ベース URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base URL] | ストア表示 | 暗号化 (SSL) チャネルで実行されていないコマースルートフォルダーの完全なアドレス。 URL の末尾はスラッシュにする必要があります。 |
| [!UICONTROL Base Link URL] | ストア表示 | ベース URL のプレースホルダーとして使用されるマークアップタグ。 |
| [!UICONTROL Base URL for Static View Files] | ストア表示 | CSS、フォント、画像、JavaScript など、テーマで使用される静的ファイルの場所を指すパス。 ベース URL を表すためにプレースホルダーが使用されます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトが含まれる場合、サイトごとに異なるフォルダーを持つことができます。 静的ビューファイルのベース URL を入力する前に、設定範囲を正しいサイトに設定します。 コマースインストール以外のフォルダを指定することもできます。 |
| [!UICONTROL Base URL for User Media Files] | ストア表示 | カタログ画像およびその他のメディアファイルの場所を指すパス。 ベース URL を表すためにプレースホルダーが使用されます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合、それぞれに異なるメディアフォルダーを設定できます。 これにより、各メディアフォルダーを個別にバックアップおよびロールバックできます。 コマースインストール以外のメディアフォルダを指定することもできます。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs (Secure)]

![Web /ベース URL (Secure)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | ストア表示 | 暗号化されたセキュア (SSL/TLS) プロトコルで配信される Commerce ルートフォルダーの完全なアドレス。 URL の末尾はスラッシュにする必要があります。 |
| [!UICONTROL Secure Base Link URL] | ストア表示 | セキュアなチャネルを経由して実行されるベース URL のプレースホルダーとして使用されるマークアップタグです。 |
| [!UICONTROL Secure Base URL for Static View Files] | ストア表示 | テーマで使用される CSS、フォント、画像、JavaScript などの静的ファイルの場所を指すマークアップタグ。 ファイルは、セキュリティで保護されていないチャネルまたはセキュリティで保護されていないチャネルのどちらでも使用できます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトが含まれる場合、サイトごとに異なるフォルダーを持つことができます。 静的ビューファイルのベース URL を入力する前に、設定範囲を正しいサイトに設定します。 コマースインストール以外のフォルダを指定することもできます。 |
| [!UICONTROL Secure Base URL for User Media Files] | ストア表示 | カタログ画像およびその他のメディアファイルの場所を指すパス。 ファイルは、セキュリティで保護されていないチャネルまたはセキュリティで保護されていないチャネルのどちらでも使用できます。 ベース URL を表すためにプレースホルダーが使用されます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合、それぞれに異なるメディアフォルダーを設定できます。 これにより、各メディアフォルダーを個別にバックアップおよびロールバックできます。 コマースインストール以外のメディアフォルダを指定することもできます。 |
| [!UICONTROL Use Secure URLs on Storefront] | ストア表示 | ドメインにセキュリティ証明書がある場合、SSL 暗号化を使用するかどうかに関わらず、ストアフロントを実行するかを選択できます。 オプション：<br />**`Yes`**— ストア URL はで始まります `https` ページが暗号化された安全なプロトコルで配信されることを示すため。<br />**`No`**  — ストア URL はで始まります `http` をクリックして、ページが安全なプロトコルなしで配信されたことを示します。 |
| [!UICONTROL Use Secure URLs in Admin] | グローバル | ドメインにセキュリティ証明書がある場合、SSL 暗号化を使用するかどうかに関わらず、ストア管理を実行するかを選択できます。 オプション： <br />**`Yes`**— 管理 URL はで始まります `https` ページが暗号化された安全なプロトコルで配信されることを示すため。<br />**`No`**  — 管理 URL はで始まります `http` をクリックして、ページが安全なプロトコルなしで配信されたことを示します。<br /> ストアと管理者の両方でセキュア URL が有効になっている場合、2 つの追加のフィールドが表示され、有効にして設定できます `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | ストア表示 | 有効にした場合、 [`HSTS`][1] は、「中間者」攻撃に対するセキュリティを測定し、「無効な証明書」メッセージがユーザーによって上書きされるのを防ぎます。 オプション： `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | ストア表示 | 有効にすると、セキュアでない (`HTTP`) リクエストをブラウザーからセキュアな (`HTTPS`) プロトコルで使用されます。 オプション： `Yes` / `No` |
| [!UICONTROL Offloader Header] | グローバル | 次の項目を指定します。 `offloader_header` クライアントとロードバランサーの間のプロトコルを識別するためのサーバー設定の値。 ほとんどの Commerce インストールでは、デフォルト値を使用します。 `X-Forwarded-Proto` (XFP) でプロトコルを次のいずれかとして識別します。 `HTTP` または `HTTPS`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Pages]

![Web /デフォルトのページ](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | ストア表示 | ベース URL に関連付けられているランディングページを示します。 コマースコンテンツ管理システム (CMS) からのページを示すために、これはデフォルトで「cms」に設定されています。 また、ブログなど、別の種類のランディングページを使用することもできます。 例えば、ブログがサーバーにインストールされている場合は、 `magento/blog`を使用する場合は、「blog」フォルダーの名前を、ページの選択範囲の相対パスとして入力できます。 |
| [!UICONTROL CMS Home Page] | ストア表示 | ストアのホームページを選択するには、リストから CMS ページを選択します。 デフォルトでは、CMS のホームページには、ストアで使用可能な CMS ページの選択がすべて一覧表示されます。 |
| [!UICONTROL Default No-route URL] | ストア表示 | デフォルトページで `404 Page not Found` エラーが発生しました。 デフォルト値は `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | ストア表示 | 「404（ページが見つかりません）」というエラーが発生した場合に表示する特定の CMS ページを識別します。 デフォルトのページは「404 Not Found」です。 |
| [!UICONTROL CMS No Cookies Page] | ストア表示 | ブラウザーで cookie が有効になっていない場合に表示される特定の CMS ページを識別します。 このページでは、Cookie が使用される理由と、各ブラウザーで Cookie を有効にする方法について説明します。 デフォルトのページは「Cookie を有効にする」です。 |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | ストア表示 | カタログ内のすべての CMS ページにパンくずリストを表示するかどうかを指定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Layouts]

![デフォルトのレイアウト](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | グローバル | を決定します。 [レイアウト](../../content-design/page-layout.md) 製品ページでデフォルトで使用される オプション： <br/>**`No layout updates`**— デフォルトでは、レイアウトの更新は製品ページでは使用できません。<br/>**`Empty`**  — デフォルトでは、は製品ページに空のレイアウトを使用します。 <br/>**`1 column`**— では、デフォルトで、製品ページに単一の列レイアウトが使用されます。<br/>**`2 columns with left bar`**  — デフォルトでは、は 2 列のレイアウトを使用し、製品ページの左側にサイドバーがあります。 <br/>**`2 columns with right bar`**— デフォルトでは、は 2 列のレイアウトを使用し、製品ページの右側にサイドバーがあります。<br/>**`3 columns`**  — では、デフォルトで、製品ページの左右にサイドバーがある 3 列のレイアウトが使用されます。<br/>**`Page -- Full Width`**- （必須） [!DNL Page Builder]) デフォルトでは、は製品ページに対して「ページ — 全幅」レイアウトを使用します。<br/>**`Category - Full Width`** - （必須） [!DNL Page Builder]) では、デフォルトで、製品ページに対して「カテゴリ — 全幅」レイアウトが使用されます。 <br/>**`Product - Full Width`**- （必須） [!DNL Page Builder]) デフォルトでは、は製品ページに対して「製品 — 全幅」レイアウトを使用します。 |
| [!UICONTROL Default Category Layout] | グローバル | を決定します。 [レイアウト](../../content-design/page-layout.md) カテゴリページではデフォルトで使用されます。 オプション： <br/>**`No layout updates`**— デフォルトでは、レイアウトの更新はカテゴリページでは使用できません。<br/>**`Empty`**  — デフォルトでは、はカテゴリページに空のレイアウトを使用します。 <br/>**`1 column`**— デフォルトでは、はカテゴリページに単一列のレイアウトを使用します。<br/>**`2 columns with left bar`**  — デフォルトでは、は 2 列のレイアウトを使用し、左側にカテゴリページ用のサイドバーがあります。 <br/>**`2 columns with right bar`**— デフォルトでは、は 2 列のレイアウトを使用し、カテゴリページの右側にサイドバーがあります。<br/>**`3 columns`**  — デフォルトで、は、カテゴリページの左右にサイドバーがある 3 列のレイアウトを使用します。<br/>**`Page - Full Width`**- （必須） [!DNL Page Builder]) では、デフォルトで、カテゴリページに対して「ページ — 全幅」レイアウトが使用されます。<br/>**`Category - Full Width`** - （必須） [!DNL Page Builder]) では、デフォルトで、カテゴリページに「カテゴリ — 全幅」レイアウトが使用されます。 <br/>**`Product - Full Width`**- （必須） [!DNL Page Builder]) では、デフォルトで、カテゴリページに製品 — 全幅レイアウトが使用されます。 |
| デフォルトのページレイアウト | グローバル | を決定します。 [レイアウト](../../content-design/page-layout.md) CMS ページではデフォルトで使用されます。 オプション： <br/>**`No layout updates`**— デフォルトでは、CMS ページではレイアウトの更新を使用できません。<br/>**`Empty`**  — デフォルトでは、は CMS ページに空のレイアウトを使用します。 <br/>**`1 column`**— はデフォルトで、CMS ページに単一の列レイアウトを使用します。<br/>**`2 columns with left bar`**  — デフォルトでは、は CMS ページ用に左側にサイドバーがある 2 列のレイアウトを使用します。<br/>**`2 columns with right bar`**— デフォルトでは、は CMS ページの右側にサイドバーがある 2 列のレイアウトを使用します。<br/>**`3 columns`**  — はデフォルトで、CMS ページの左右にサイドバーが付いた 3 列のレイアウトを使用します。<br/>**`Page - Full Width`**- （必須） [!UICONTROL Page Builder]) では、デフォルトで、CMS ページに対して「ページ — 全幅」レイアウトが使用されます。<br/>**`Category - Full Width`** - （必須） [!UICONTROL Page Builder]) では、デフォルトで、CMS ページに対して「カテゴリ — 全幅」レイアウトが使用されます。 <br/>**`Product - Full Width`**- （必須） [!DNL Page Builder]) はデフォルトで、CMS ページに対して「製品 — 全幅」レイアウトを使用します。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Cookie Settings]

![Web /デフォルトの Cookie 設定](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | ストア表示 | Cookie が自動的に削除されるまでの期間を指定します。 デフォルト値は 3600 秒（1 時間）です |
| [!UICONTROL Cookie Path] | ストア表示 | コマース Cookie を使用できるサーバー上のフォルダーを指定します。 インストールのどこでも Commerce Cookie を使用できるようにするには、 Cookie のパスを 1 つのスラッシュに設定します。 `/`. この値には、Cookie のパスのみを含めることができ、 **_できません_** には、その他の cookie パラメーターが含まれます。 |
| [!UICONTROL Cookie Domain] | ストア表示 | Commerce Cookie をサブドメインで使用できるかどうかを指定します。 例えば、をサポートします。 `mysubdomain`.domain.com、ドメイン名の先頭にピリオドを付けて入力します（例： ）。 `.domain.com`. この値には、Cookie ドメインのみを含めることができ、 **_できません_** には、その他の cookie パラメーターが含まれます。 |
| [!UICONTROL Use HTTP Only] | ストア表示 | コマース Cookie を安全でないチャネル (http) 上でのみ使用できるか、暗号化されたチャネル (https) 上でも使用できるかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Web サイト | cookie 制限モードが有効かどうかを決定します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Session Validation Settings]

![Web /セッションの検証](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | グローバル | 要求の IP アドレスが一致することを確認します `$_SESSION` データ。 異なる IP アドレスが検出されると、セッションは終了します。 オプション： `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | グローバル | 受信プロキシデータを検証し、リクエストのプロキシアドレスが一致しているかを確認します `$_SESSION` データ。 別のプロキシアドレスが検出されると、セッションは終了します。 オプション： `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | グローバル | 送信プロキシデータを検証し、リクエストの転送先アドレスが一致しているかどうかを確認します  `$_SESSION` データ。 別の転送先アドレスが検出されると、セッションは終了します。 オプション： `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | グローバル | `USER_AGENT` は、Web サイトへのアクセスに使用されるブラウザーまたはデバイスを指します。 ブラウザーの名前とバージョン、およびオペレーティングシステムが一致していることを確認します `$_SESSION` データ。 同じセッション内の要求から別の要求へ、別のユーザーエージェントが検出されると、セッションは終了します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Browser Capabilities Detection]

![Web/ブラウザー機能の検出](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | ストア表示 | ブラウザーで cookie が無効になっている場合、CMS の No Cookies ページに自動的にリダイレクトされます。 オプション： `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | ストア表示 | ブラウザーで JavaScript が無効になっている場合は、次の通知が表示され、JavaScript オプションを有効にするように求められます。 `Yes` / `No` （無効） |
| [!UICONTROL Show Notice if Local Storage is Disabled] | ストア表示 | ローカルキャッシュが無効な場合にメッセージを表示します。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
