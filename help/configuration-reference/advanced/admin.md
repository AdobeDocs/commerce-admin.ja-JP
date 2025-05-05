---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Commerce Admin の [!UICONTROL Advanced] &gt; [!UICONTROL Admin] ページで設定を確認します。
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 詳細/管理者

{{config}}

## [!UICONTROL Admin User Emails]

![ 管理者ユーザーのメール ](./assets/admin-admin-user-emails.png)<!-- zoom -->

これらの設定の変更について詳しくは、「[ パスワードを忘れた場合やメールをリセット ](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails)」を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | グローバル | 管理者ユーザーがパスワードを忘れた場合に送信されるメッセージに使用されるメールテンプレートを識別します。 既定のテンプレート：`Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | グローバル | _パスワードを忘れた場合_ メールの送信者として表示される店舗連絡先を識別します。 デフォルトの送信者：`General Contact`<br/> その他の送信者オプション：`Sales Representative`、`Customer Support`、`Custom Email` |
| [!UICONTROL User Notification Template] | グローバル | 管理者通知用のデフォルトとして使用されるメールテンプレートを決定します。 既定のテンプレート：`User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![ スタートアップ ページ ](./assets/admin-startup-page.png)<!-- zoom -->

これらの設定の変更の詳細については、「[ スタートアップ ガイド ](../../getting-started/admin-dashboard.md#change-the-startup-page) の _スタートアップ ページの変更_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | グローバル | ログイン後に表示される管理者ランディングページを決定します。 |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] オプション

| 領域 |                                                                                                                                                                                                                                                                                                                                                                           | オプション |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)） <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [ ダッシュボード ](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![ 管理ベース URL](./assets/admin-admin-base-url.png)<!-- zoom -->

これらのオプションの設定について詳しくは、[ ストアと購入エクスペリエンスガイド ](../../stores-purchase/store-urls.md#configure-the-base-url) の _ベース URL の設定_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | グローバル | 管理者へのアクセスにカスタム URL を使用するかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Admin URL] | グローバル | 管理者にアクセスするためのカスタム URL を指定します。 デフォルトでは、管理者 URL はベース URL と同じです。<br/>**重要：** 管理者 URL は、同じCommerce インストール内にあり、ストアフロントと同じドキュメントルートを持つ必要があります。 |
| [!UICONTROL Use Custom Admin Path] | グローバル | 管理者へのアクセスにカスタムパスを使用するかどうかを決定します。 デフォルトパスは `admin` です。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Admin Path] | グローバル | デフォルトの管理者パスの名前を推測しにくい名前に変更します。 カスタムパス名を小文字で入力します。 例：`aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![ セキュリティ ](./assets/admin-security.png)<!-- zoom -->

これらのオプションの設定については、『 [ 管理システムガイド _の ](../../systems/security-admin.md) 管理者セキュリティの設定_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | ストア表示 | 管理者ユーザーが、異なるデバイスから同じアカウントに同時にログインできるかどうかを決定します。 オプション：<br/>**`Yes`**– 同じ管理者アカウントからの複数のアクティブなセッションを許可します。<br/>**`No`** – 管理者アカウントごとに 1 つのアクティブなセッションのみを許可します。 |
| [!UICONTROL Password Reset Protection Type] | ストア表示 | パスワードリセットリクエストの管理に使用する方法を決定します。 オプション：<br/>**`By IP and Email`**– 通知から管理者アカウントに関連付けられたメールアドレスに応答が送信された後、パスワードをオンラインでリセットできます。<br/>**`By IP`** - パスワードは、追加の確認なしにオンラインでリセットできます。 <br/>**`By Email`**- パスワードは、管理者アカウントに関連付けられたメールアドレスに送信される通知にメールで応答する場合にのみリセットできます。<br/>**`None`** - パスワードは、ストア管理者のみがリセットできます。 |
| [!UICONTROL Recovery Link Expiration Period (hours)] | グローバル | パスワード回復リンクの有効期間を決定します。 |
| [!UICONTROL Max Number of Password Reset Requests] | ストア表示 | 1 時間あたりに送信できるパスワード要求の最大数を決定します。 |
| [!UICONTROL Min Time Between Password Reset Requests] | ストア表示 | パスワードリセットリクエストの間隔の最小分数を決定します。 |
| [!UICONTROL Add Secret Key to URLs] | グローバル | 有効にすると、悪用に対する予防策として秘密鍵が Admin URL に追加されます。 オプション：`Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | グローバル | ユーザーが入力したログイン資格情報が、保存されたログイン資格情報の大文字と小文字を一致させる必要があるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | グローバル | 管理者セッションの長さを秒単位で指定します。 |
| [!UICONTROL Maximum Login Failures to Lockout Account] | グローバル | 管理者ユーザーがログインを試みる回数を決定します。この回数を超えると、管理者ユーザーのアカウントはロックされます。 フィールドが空の場合、最小値は設定されません。 デフォルト値：`6` |
| [!UICONTROL Lockout Time (minutes)] | グローバル | ユーザーが再度ログインできるようになるまでの、管理者アカウントがロックされる時間（分）を指定します。 デフォルト値：`30` |
| [!UICONTROL Password Lifetime (days)] | グローバル | 管理者パスワードの有効期限が切れるまでの日数を決定します。 フィールドが空の場合、有効期間は設定されません。 デフォルト値：`90` |
| [!UICONTROL Password Change] | グローバル | 管理者ユーザーが自分のパスワードを変更する必要があるかどうかを決定します。 オプション：<br/>**`Forced`**- アカウントの設定後に管理者ユーザーがパスワードを変更する必要があります。<br/>**`Recommended`** - アカウントの設定後に管理者ユーザーがパスワードを変更することを推奨します。 |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![ ダッシュボード ](./assets/admin-dashboard.png)<!-- zoom -->

これらのオプションの設定の詳細については、「[ はじめる前に _」の_ 管理ダッシュボード ](../../getting-started/admin-dashboard.md) を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | グローバル | 現在の販売データから生成されたグラフがダッシュボードに含まれているかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![ 管理グリッド ](./assets/admin-admin-grids.png)<!-- zoom -->

これらのオプションの設定の詳細については、『 [ カタログ管理ガイド ](../../catalog/products-list.md#limit-product-display) の _製品の表示を制限する_ を参照してください。

>[!NOTE]
>
>大きなカタログのパフォーマンスを向上させるには、グリッドに表示する製品数を制限することをお勧めします。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | グローバル | グリッドに表示される製品の数を _[!UICONTROL Records Limit]_&#x200B;の値に制限するかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Records Limit] | グローバル | 製品グリッド内の製品数の上限を設定します。 デフォルトの最小値は `20000` です。 |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

これらのオプションの設定について詳しくは、『 [ 管理システムガイド _の ](../../systems/security-captcha.md)CAPTCHA_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | グローバル | 管理者ログインの CAPTCHA を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Font] | グローバル | CAPTCHA を表示するために使用するフォントを決定します。 独自のフォントを追加するには、フォントファイルをCommerce インスタンスと同じディレクトリに置き、`app/code/Magento/Captcha/etc` Default font:` LinLibertine` にある config.xml ファイルに宣言を追加します。 |
| [!UICONTROL Forms] | グローバル | CAPTCHA が使用されるフォームを決定します。 オプション：`Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | グローバル | CAPTCHA が表示されるタイミングを決定します。 オプション：<br/>**`Always`**- ログインには常に CAPTCHA が必要です。<br/>**`After number of attempts to login`** - 「[!UICONTROL Number of Unsuccessful Attempts to Login]」フィールドを表示します。 許可されるログイン試行回数を入力します。 値が 0 （ゼロ）の場合は、[ 表示モード ] を [ 常に ] に設定する場合と似ています。 このオプションでは、パスワードを忘れた場合とユーザーを作成フォームには対応しません。 CAPTCHA が有効で表示するように設定されている場合、常にフォームに含まれます。<br />**注意**：失敗したログインの試行回数を追跡するには、1 つのメールアドレスで、1 つの IP アドレスからのログインがカウントされます。 同じ IP アドレスから許可されるログイン試行回数の上限は 1,000 です。 この制限は、CAPTCHA が有効な場合にのみ適用されます。 |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | グローバル | アカウントがロックされるまでのログイン試行回数を指定します。 ログインの失敗回数を追跡するために、システムは 1 つの IP アドレスからの試行を 1 つの IP アドレスから追跡します。 同じ IP アドレスからの最大試行回数は 1,000 です。 この制限は、CAPTCHA が有効になっている場合にのみ適用されます。 |
| [!UICONTROL CAPTCHA Timeout (minutes)] | グローバル | 現在の CAPTCHA の有効期間を決定します。 CAPTCHA の有効期限が切れたら、ユーザーはページをリロードする必要があります。 |
| [!UICONTROL Number of Symbols] | グローバル | CAPTCHA で使用されるシンボルの数を決定します。 許容される最大値は `8` です。 また、範囲（例：`5-8`）を指定することもできます。 |
| [!UICONTROL Symbols Used in CAPTCHA] | グローバル | CAPTCHA で使用されるシンボルを決定します。 文字（a ～ z および A ～ Z）と数字（0 ～ 9）のみを使用できます。 フィールドに表示される記号の既定のセットは、i、l、1 などの類似した記号を除外します。 CAPTCHA にこれらの記号を表示すると、ユーザーが CAPTCHA を正しく認識できる可能性が低くなります。 |
| [!UICONTROL Case Sensitive] | グローバル | CAPTCHA で使用される文字で大文字と小文字を区別するかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![ 管理アクションのログ ](./assets/admin-actions-logging.png)<!-- zoom -->

これらのオプションの設定の詳細については、『 [ 管理システムガイド _の ](../../systems/action-log-archive.md) アクションログアーカイブ_ を参照してください。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | グローバル | 選択した各アクションのアクション ログを有効にします：<br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Admin Usage](./assets/admin-usage.png)<!-- zoom -->

これらのオプションの設定の詳細については、「[ はじめる前に _」の_ 使用状況データの収集 ](../../getting-started/admin.md#usage-data-collection) を参照してください。

| フィールド | 範囲 | 説明 |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | グローバル | _Admin_ および関連する製品とサービスのユーザーエクスペリエンスを向上させるために、管理者の使用状況データを収集するAdobeを付与します。 また、データ収集を許可すると、ヘルプ、ツールヒント、ウォークスルー _オンボーディング情報、機能のお知らせなどのインタラクティブコンテンツを_ 管理者 _に提供するように設計された_ 製品内ガイダンスも有効になります。 使用状況データでは個々の管理者は識別されません。 オプション：<br />**`Yes`**- データ収集を許可し、_製品内ガイダンス_ を有効にします。<br />**`No`** - データ収集を許可せず、（製品内ガイダンス _を有効にしません_。 |

{style="table-layout:auto"}
