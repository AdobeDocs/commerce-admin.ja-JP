---
title: '[!UICONTROL General] > [!UICONTROL Web]'
description: Commerce管理者の[!UICONTROL General] > [!UICONTROL Web] ページで設定を確認します。
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
TQID: https://experienceleague.adobe.com/31ifTtUvNwjEouPwT5N2cQyr6CUrEblmMULOolo6Amw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1809
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web >一般オプション ](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | 範囲 | 説明 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | グローバル | Web サーバーの書き換えが有効になっている場合は、現在のビューのストアコードをURLに挿入します。 オプション：`Yes` / `No`。 <br />このフィールドが`Yes`に設定されている場合、URLの書き換えが正しくマッピングされ、すべてのページが正常に開くように、ブラウザーのURLにストアコードを含める必要があります。 これにより、_404 ページが見つかりません_ エラーを回避できます。 |
| [!UICONTROL Auto-redirect to Base URL] | ストアビュー | （シングルストア設定の場合）サイトに壊れたリンクがある場合、トラフィックは「404 Page Not Found」メッセージを含むページではなく、ベース URLにリダイレクトされます。 オプション：` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Important:_** マルチストア設定のベース URLに自動リダイレクトを使用しないでください。 |
| [!UICONTROL Catalog media URL format] | グローバル | 製品とカテゴリに割り当てられた[URL形式](../../catalog/catalog-urls.md)を定義します。 オプション：画像ごとの一意のハッシュ バリアント（レガシーモード）は、変換されたファイル名を一意のハッシュ値として定義します。 クエリパラメーターに基づく画像最適化は、クエリパラメーターに応じて[画像最適化](../../content-design/media-gallery-image-optimization.md) プロセスを定義します。 |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web >検索エンジン最適化](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | ストアビュー | PHP ベースのシステムでは、通常、ルートフォルダーに`index.php`という名前のファイルが含まれています。 デフォルトでは、ファイル名はルートフォルダー名のすぐ後のURLに表示されます。 これが有効になっている場合、システムはURLから`index.php`を省略します。 このユーザビリティのベストプラクティスは、各URLをより簡潔にし、パフォーマンスやサイトランクに影響を与えません。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > ベース URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Base URL] | ストアビュー | 暗号化（SSL）チャネルを介して実行されていないCommerce ルートフォルダーの完全なアドレス。 URLはスラッシュで終わる必要があります。 |
| [!UICONTROL Base Link URL] | ストアビュー | ベース URLのプレースホルダーとして使用されるマークアップタグ。 |
| [!UICONTROL Base URL for Static View Files] | ストアビュー | Css、フォント、画像、JavaScriptなど、テーマで使用される静的ファイルの場所を指すパス。 プレースホルダーは、ベース URLを表すために使用されます。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合は、サイトごとに異なるフォルダーを設定できます。 静的ビューファイルのベース URLを入力する前に、設定範囲を正しいサイトに設定します。 Commerce インストール以外の場所にフォルダーを指定することもできます。 |
| [!UICONTROL Base URL for User Media Files] | ストアビュー | カタログ画像やその他のメディアファイルの場所を指すパス。 プレースホルダーは、ベース URLを表すために使用されます。 Commerceのインストールに同じフォルダー構造を持つ複数のサイトがある場合は、それぞれに異なるメディアフォルダーを設定できます。 これにより、各メディアフォルダーを個別にバックアップおよびロールバックできます。 Commerce インストール以外の場所にメディアフォルダーを指定することもできます。 |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > ベース URL （セキュア） ](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | ストアビュー | 暗号化されたセキュア（SSL/TLS）プロトコルで配信されるCommerce ルートフォルダーの完全なアドレス。 URLはスラッシュで終わる必要があります。 |
| [!UICONTROL Secure Base Link URL] | ストアビュー | 安全なチャネル上で実行されるベース URLのプレースホルダーとして使用されるマークアップタグ。 |
| [!UICONTROL Secure Base URL for Static View Files] | ストアビュー | CSS、フォント、画像、JavaScriptなど、テーマで使用される静的ファイルの場所を指すマークアップタグ。 ファイルは、安全でないチャネルまたは安全なチャネルのどちらかに存在する可能性があります。 Commerce インストールに同じフォルダー構造を持つ複数のサイトがある場合は、サイトごとに異なるフォルダーを設定できます。 静的ビューファイルのベース URLを入力する前に、設定範囲を正しいサイトに設定します。 Commerce インストール以外の場所にフォルダーを指定することもできます。 |
| [!UICONTROL Secure Base URL for User Media Files] | ストアビュー | カタログ画像やその他のメディアファイルの場所を指すパス。 ファイルは、安全でないチャネルまたは安全なチャネルのどちらかに存在する可能性があります。 プレースホルダーは、ベース URLを表すために使用されます。 Commerceのインストールに同じフォルダー構造を持つ複数のサイトがある場合は、それぞれに異なるメディアフォルダーを設定できます。 これにより、各メディアフォルダーを個別にバックアップおよびロールバックできます。 Commerce インストール以外の場所にメディアフォルダーを指定することもできます。 |
| [!UICONTROL Use Secure URLs on Storefront] | ストアビュー | ドメインにセキュリティ証明書がある場合は、SSL暗号化の有無に関わらず、ストアフロントを実行することを選択できます。 オプション：<br />**`Yes`**- ストア URLは`https`で始まり、ページが暗号化された安全なプロトコルで配信されていることを示します。<br />**`No`** - ストア URLは`http`で始まり、ページが安全なプロトコルなしで配信されていることを示します。 |
| [!UICONTROL Use Secure URLs in Admin] | グローバル | ドメインにセキュリティ証明書がある場合は、SSL暗号化の有無にかかわらず、ストア管理者を実行することを選択できます。 オプション：<br />**`Yes`**– 管理者URLは`https`で始まり、ページが暗号化された安全なプロトコルで配信されていることを示します。<br />**`No`**  – 管理者URLは`http`で始まり、ページが安全なプロトコルなしで配信されていることを示します。<br /> ストアと管理者の両方でセキュア URLが有効になっている場合、2つの追加フィールドが`HSTS`を有効にして設定するように表示されます。 |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | ストアビュー | 有効にすると、[`HSTS`](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html)は「中にいる男性」攻撃に対するセキュリティ対策を提供し、ユーザーが「無効な証明書」メッセージを上書きするのを防ぎます。 オプション：`Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | ストアビュー | 有効にすると、ブラウザーから受信した安全でない（`HTTP`）要求を安全な（`HTTPS`） プロトコルに変換します。 オプション：`Yes` / `No` |
| [!UICONTROL Offloader Header] | グローバル | クライアントとロードバランサー間のプロトコルを識別するために、サーバー設定の`offloader_header`値を指定します。 ほとんどのCommerceのインストールでは、デフォルト値である`X-Forwarded-Proto` （XFP）を使用して、プロトコルを`HTTP`または`HTTPS`として識別します。 |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > デフォルトページ ](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | ストアビュー | ベース URLに関連付けられているランディングページを示します。 これは、Commerce Content Management System （CMS）のページを示すために、デフォルトで「cms」に設定されています。 また、ブログなど、別の種類のランディングページを使用することもできます。 例えば、ブログが`magento/blog`のサーバーにインストールされている場合、「ブログ」フォルダーの名前をページの選択に対する相対パスとして入力できます。 |
| [!UICONTROL CMS Home Page] | ストアビュー | ストアのホームページを選択するには、リストからCMSページを選択します。 デフォルトでは、CMS ホームページには、ストアで使用可能なCMS ページの選択全体が一覧表示されます。 |
| [!UICONTROL Default No-route URL] | ストアビュー | `404 Page not Found` エラーが発生したときに表示する既定のページのURLが含まれます。 デフォルト値は`cms/noroute/index`です。 |
| [!UICONTROL CMS No Route Page] | ストアビュー | 404 Page Not Found エラーが発生した場合に表示する特定のCMS ページを指定します。 デフォルトのページは「404 Not Found」です。 |
| [!UICONTROL CMS No Cookies Page] | ストアビュー | ブラウザーでCookieが有効になっていないときに表示される特定のCMS ページを識別します。 このページでは、Cookieが使用される理由と、各ブラウザーでそれらを有効にする方法について説明します。 デフォルトのページはEnable Cookiesです。 |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | ストアビュー | カタログ内のすべてのCMS ページにパンくずリストが表示されるかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![ デフォルトレイアウト ](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/design/layout/page-layout) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | グローバル | 製品ページにデフォルトで使用される[layout](../../content-design/page-layout.md)を決定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、製品ページのレイアウト更新は利用できません。<br/>**`Empty`** - デフォルトでは、商品ページに空白レイアウトが使用されます。<br/>**`1 column`**- デフォルトでは、製品ページに単一の列レイアウトが使用されます。<br/>**`2 columns with left bar`** - デフォルトでは、製品ページの左側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`2 columns with right bar`**- デフォルトでは、製品ページの右側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`3 columns`** - デフォルトでは、製品ページの左側と右側にサイドバーを持つ3列レイアウトが使用されます。<br/>**`Page -- Full Width`**- （必要なのは[!DNL Page Builder]）デフォルトでは、製品ページにページ – 全幅レイアウトを使用します。<br/>**`Category - Full Width`** - （[!DNL Page Builder]が必要）デフォルトでは、商品ページにカテゴリ – 全幅レイアウトが使用されます。<br/>**`Product - Full Width`**- （[!DNL Page Builder]が必要）デフォルトでは、製品ページに製品 – 全幅レイアウトが使用されます。 |
| [!UICONTROL Default Category Layout] | グローバル | カテゴリーページにデフォルトで使用される[layout](../../content-design/page-layout.md)を決定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、カテゴリーページのレイアウト更新は使用できません。<br/>**`Empty`** - デフォルトでは、カテゴリーページに空白レイアウトが使用されます。<br/>**`1 column`**- デフォルトでは、カテゴリーページに単一の列レイアウトが使用されます。<br/>**`2 columns with left bar`** - デフォルトでは、カテゴリーページの左側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`2 columns with right bar`**- デフォルトでは、カテゴリーページの右側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`3 columns`** - デフォルトでは、カテゴリーページに左と右にサイドバーを含む3列レイアウトが使用されます。<br/>**`Page - Full Width`**- （必要なのは[!DNL Page Builder]）デフォルトでは、カテゴリーページにページ – 全幅レイアウトを使用します。<br/>**`Category - Full Width`** - （[!DNL Page Builder]が必要）デフォルトでは、カテゴリーページにカテゴリ – 全幅レイアウトが使用されます。<br/>**`Product - Full Width`**- （[!DNL Page Builder]が必要）デフォルトでは、カテゴリーページにProduct - Full Width レイアウトが使用されます。 |
| デフォルトページレイアウト | グローバル | CMS ページにデフォルトで使用される[layout](../../content-design/page-layout.md)を指定します。 オプション：<br/>**`No layout updates`**- デフォルトでは、CMS ページのレイアウト更新は使用できません。<br/>**`Empty`** - デフォルトでは、CMS ページに空白レイアウトが使用されます。<br/>**`1 column`**- デフォルトでは、CMS ページに1列レイアウトが使用されます。<br/>**`2 columns with left bar`** - デフォルトでは、CMS ページの左側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`2 columns with right bar`**- デフォルトでは、CMS ページの右側にサイドバーが表示された2列レイアウトが使用されます。<br/>**`3 columns`** - デフォルトでは、CMS ページの左側と右側にサイドバーを持つ3列レイアウトが使用されます。<br/>**`Page - Full Width`**- （必要なのは[!UICONTROL Page Builder]）デフォルトでは、CMS ページのページ – 全幅レイアウトが使用されます。<br/>**`Category - Full Width`** - （[!UICONTROL Page Builder]が必要）デフォルトでは、CMS ページにカテゴリ – 全幅レイアウトが使用されます。<br/>**`Product - Full Width`**- （[!DNL Page Builder]が必要）デフォルトでは、CMS ページにProduct - Full Width レイアウトが使用されます。 |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > デフォルトのCookie設定](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | ストアビュー | Cookieが自動的に削除されるまでの時間を指定します。 デフォルト値は3600秒（1時間）です |
| [!UICONTROL Cookie Path] | ストアビュー | Commerce Cookieを使用できるサーバー上のフォルダーを指定します。 インストール中の任意の場所でCommerce Cookieを使用できるようにするには、Cookie パスを1つのスラッシュ `/`に設定します。 この値にはcookie パスのみを含めることができ、**_には他のcookie パラメーターを含めることはできません。_** |
| [!UICONTROL Cookie Domain] | ストアビュー | サブドメインでCommerce Cookieを使用できるかどうかを指定します。 例えば、`mysubdomain`.domain.comをサポートするには、`.domain.com`のように、先頭にピリオドが付いたドメイン名を入力します。 この値にはcookie ドメインのみを含めることができ、**_には他のcookie パラメーターを含めることはできません。_** |
| [!UICONTROL Use HTTP Only] | ストアビュー | Commerce Cookieを安全でないチャネル（http）でのみ使用できるか、暗号化されたチャネル（https）でも使用できるかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | web サイト | Cookie制限モードが有効かどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > セッション検証](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | グローバル | リクエストのIP アドレスが`$_SESSION` データと一致することを確認します。 セッションは、別のIP アドレスが検出された場合に終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | グローバル | 受信プロキシデータを検証し、リクエストのプロキシアドレスが`$_SESSION` データと一致することを確認します。 セッションは、別のプロキシアドレスが検出された場合に終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | グローバル | 送信プロキシデータを検証し、リクエストの転送済みアドレスが`$_SESSION` データと一致することを確認します。 セッションは、別の転送用アドレスが検出された場合に終了します。 オプション：`Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | グローバル | `USER_AGENT`は、Web サイトへのアクセスに使用されるブラウザーまたはデバイスを指します。 ブラウザーの名前とバージョン、およびオペレーティングシステムが`$_SESSION` データと一致することを確認します。 セッションは、同じセッション内のリクエストから別のリクエストに異なるユーザーエージェントが検出された場合に終了します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > ブラウザー機能の検出](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | ストアビュー | ブラウザーでCookieが無効になっている場合、CMSのCookieなしページに自動的にリダイレクトされます。 オプション：`Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | ストアビュー | ブラウザーでJavaScriptが無効になっている場合は、JavaScript オプションを有効にするよう求める通知が表示されます：`Yes` / `No` （無効） |
| [!UICONTROL Show Notice if Local Storage is Disabled] | ストアビュー | ローカルキャッシュが無効になっている場合は、メッセージを表示します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}
