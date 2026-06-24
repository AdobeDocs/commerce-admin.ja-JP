---
title: '[!UICONTROL Advanced] > [!UICONTROL Admin]'
description: Commerce管理者の[!UICONTROL Advanced] > [!UICONTROL Admin] ページで設定を確認します。
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
TQID: https://experienceleague.adobe.com/nLIhR9z4VAqGUnR2MqQOav3sHg4tnjObhj36K-P08TE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1273
ht-degree: 0%

---

# 詳細設定/管理者

{{config}}

## [!UICONTROL Admin User Emails]

![管理者ユーザーメール &#x200B;](./assets/admin-admin-user-emails.png)<!-- zoom -->

これらの設定の変更について詳しくは、[&#x200B; パスワードを忘れた場合と電子メールをリセットする](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails)を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | グローバル | 管理者ユーザーがパスワードを忘れたときに送信されるメッセージに使用される電子メールテンプレートを識別します。 既定のテンプレート：`Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | グローバル | _パスワードを忘れた_&#x200B;電子メールの送信者として表示されるストア連絡先を識別します。 既定の送信者：`General Contact`<br/>その他の送信者オプション：`Sales Representative`、`Customer Support`、`Custom Email` |
| [!UICONTROL User Notification Template] | グローバル | 管理者通知のデフォルトとして使用される電子メールテンプレートを決定します。 既定のテンプレート：`User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![&#x200B; スタートアップページ &#x200B;](./assets/admin-startup-page.png)<!-- zoom -->

これらの設定の変更について詳しくは、_スタートアップガイド_&#x200B;の「[&#x200B; スタートアップページの変更](../../getting-started/admin-dashboard.md#change-the-startup-page)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | グローバル | ログイン後に表示される管理者ランディングページを指定します。 |

{style="table-layout:auto"}

### [!UICONTROL Startup Page]個のオプション

| 面グラフ |                                                                                                                                                                                                                                                                                                                                                                           | オプション |
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
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [&#x200B; ダッシュボード &#x200B;](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html?lang=ja) ![Adobe Commerce](../../assets/adobe-logo.svg) |
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
|                                                         | `Support` | [`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- 
Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=ja#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![管理者ベース URL](./assets/admin-admin-base-url.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_ストアおよび購入エクスペリエンスガイド_&#x200B;の「[&#x200B; ベース URL](../../stores-purchase/store-urls.md#configure-the-base-url)の設定」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | グローバル | 管理者へのアクセスにカスタム URLを使用するかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Admin URL] | グローバル | 管理者にアクセスするためのカスタム URLを指定します。 デフォルトでは、管理者URLはベース URLと同じです。<br/>**重要：**&#x200B;管理者URLは同じCommerce インストールにあり、ストアフロントと同じドキュメントルートを持つ必要があります。 |
| [!UICONTROL Use Custom Admin Path] | グローバル | 管理者へのアクセスにカスタムパスを使用するかどうかを指定します。 既定のパスは`admin`です。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Admin Path] | グローバル | デフォルトの管理者パスの名前を、推測しにくい名前に変更します。 カスタムパス名を小文字で入力します。 例：`aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![&#x200B; セキュリティ &#x200B;](./assets/admin-security.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_管理者システムガイド_&#x200B;の「[管理者セキュリティの設定](../../systems/security-admin.md)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | ストアビュー | 管理者ユーザーが異なるデバイスから同じアカウントに同時にログインできるかどうかを指定します。 オプション：<br/>**`Yes`**– 同じ管理者アカウントから複数のアクティブなセッションを許可します。<br/>**`No`** – 管理者アカウントごとに1つのアクティブなセッションのみを許可します。 |
| [!UICONTROL Password Reset Protection Type] | ストアビュー | パスワード リセット要求の管理に使用する方法を指定します。 オプション：<br/>**`By IP and Email`**– 通知から応答を受け取った後、パスワードをオンラインでリセットして、管理者アカウントに関連付けられた電子メールアドレスに送信できます。<br/>**`By IP`** - パスワードは、追加確認なしでオンラインでリセットできます。<br/>**`By Email`**- パスワードは、管理者アカウントに関連付けられた電子メールアドレスに送信される通知に電子メールで応答することによってのみリセットできます。<br/>**`None`** - パスワードは、ストア管理者のみがリセットできます。 |
| [!UICONTROL Recovery Link Expiration Period (hours)] | グローバル | パスワード回復リンクが有効な時間数を指定します。 |
| [!UICONTROL Max Number of Password Reset Requests] | ストアビュー | 1時間に送信できるパスワード要求の最大数を指定します。 |
| [!UICONTROL Min Time Between Password Reset Requests] | ストアビュー | パスワードのリセット要求の最小間隔（分）を指定します。 |
| [!UICONTROL Add Secret Key to URLs] | グローバル | 有効にすると、悪用に対する予防策として、管理者URLに秘密鍵が追加されます。 オプション：`Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | グローバル | ユーザーが入力したログイン資格情報が、保存されている資格情報の大文字と小文字を一致させる必要があるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | グローバル | 管理者セッションの長さを秒単位で指定します。 |
| [!UICONTROL Maximum Login Failures to Lockout Account] | グローバル | 管理者ユーザーがアカウントをロックする前にログインを試行できる回数を指定します。 フィールドが空の場合、最小値は設定されません。 デフォルト値：`6` |
| [!UICONTROL Lockout Time (minutes)] | グローバル | ユーザーが再度ログインを試みる前に、管理者アカウントがロックされる分数を指定します。 デフォルト値：`30` |
| [!UICONTROL Minimum Admin Password Length] | グローバル | 管理者パスワードに必要な最小文字数を指定します。 デフォルト値は7で、最小値は7です。 この設定は、管理者パスワードの変更、管理者インターフェイスとCLIの両方からの新しい管理者ユーザーの作成、および管理者からのパスワードリセット操作に影響します。 |
| [!UICONTROL Password Lifetime (days)] | グローバル | 管理者パスワードが期限切れになるまでの日数を指定します。 フィールドが空の場合、有効期間は設定されません。 デフォルト値：`90` |
| [!UICONTROL Password Change] | グローバル | 管理者ユーザーがパスワードを変更する必要があるかどうかを決定します。 オプション：<br/>**`Forced`**- アカウントの設定後に管理者ユーザーがパスワードを変更する必要があります。<br/>**`Recommended`** – 管理者ユーザーは、アカウントの設定後にパスワードを変更することをお勧めします。 |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![&#x200B; ダッシュボード &#x200B;](./assets/admin-dashboard.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_はじめにガイド_&#x200B;の[管理者ダッシュボード &#x200B;](../../getting-started/admin-dashboard.md)を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | グローバル | ダッシュボードに現在の売上データから生成されたチャートが含まれているかどうかを判断します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![管理者グリッド &#x200B;](./assets/admin-admin-grids.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_カタログ管理ガイド_&#x200B;の「[製品表示の制限](../../catalog/products-list.md#limit-product-display)」を参照してください。

>[!NOTE]
>
>大きなカタログのパフォーマンスを向上させるには、グリッドに表示される商品数を制限することをお勧めします。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | グローバル | グリッドに表示される製品数が&#x200B;_[!UICONTROL Records Limit]_&#x200B;個の値に制限されているかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Records Limit] | グローバル | 商品グリッド内の商品の数の制限を設定します。 デフォルトの最小値は`20000`です。 |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_管理者システムガイド_&#x200B;の[CAPTCHA](../../systems/security-captcha.md)を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | グローバル | 管理者ログインのCAPTCHAを有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Font] | グローバル | CAPTCHAの表示に使用するフォントを指定します。 独自のフォントを追加するには、フォントファイルをCommerce インスタンスと同じディレクトリに置き、宣言を`app/code/Magento/Captcha/etc`のconfig.xml ファイルに追加します。デフォルトのフォント：` LinLibertine` |
| [!UICONTROL Forms] | グローバル | CAPTCHAが使用されるフォームを指定します。 オプション：`Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | グローバル | CAPTCHAがいつ表示されるかを指定します。 オプション：<br/>**`Always`**- ログインするには常にCAPTCHAが必要です。<br/>**`After number of attempts to login`** - [!UICONTROL Number of Unsuccessful Attempts to Login] フィールドを表示します。 許可されるログイン試行回数を入力します。 0 （ゼロ）の値は、「表示モード」を「常に」に設定することと似ています。 このオプションでは、「パスワードを忘れた」および「ユーザーを作成」フォームはカバーされません。 CAPTCHAが有効になっていて表示されるように設定されている場合、常にフォームに含まれます。<br />**注**：失敗したログイン試行回数を追跡するには、1つの電子メールアドレスと1つのIP アドレスからログインするたびにカウントされます。 同じIP アドレスから許可されるログイン試行の最大数は1,000です。 この制限は、CAPTCHAが有効になっている場合にのみ適用されます。 |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | グローバル | アカウントがロックされる前に、ユーザーがログインを試行できる回数を指定します。 失敗したログイン試行回数を追跡するには、1つのIP アドレスから1つの電子メールアドレスの試行回数を追跡します。 同じIP アドレスから許可される最大試行回数は1,000回です。 この制限は、CAPTCHAが有効になっている場合にのみ適用されます。 |
| [!UICONTROL CAPTCHA Timeout (minutes)] | グローバル | 現在のCAPTCHAの有効期間を決定します。 CAPTCHAの有効期限が切れると、ユーザーはページをリロードする必要があります。 |
| [!UICONTROL Number of Symbols] | グローバル | CAPTCHAで使用されるシンボルの数を指定します。 許可される最大値は`8`です。 範囲（例：`5-8`）を指定することもできます。 |
| [!UICONTROL Symbols Used in CAPTCHA] | グローバル | CAPTCHAで使用するシンボルを指定します。 文字（a ～ zおよびA ～ Z）と数字（0 ～ 9）のみを使用できます。 フィールドで提案されたデフォルトのシンボルのセットでは、i、l、1などの類似したシンボルは除外されます。 CAPTCHAでこれらのシンボルを表示すると、ユーザーがCAPTCHAを正しく認識する可能性が低くなります。 |
| [!UICONTROL Case Sensitive] | グローバル | CAPTCHAで使用される文字が大文字と小文字を区別するかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![管理者アクションのログ記録](./assets/admin-actions-logging.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_管理者システムガイド_&#x200B;の「[&#x200B; アクションログアーカイブ &#x200B;](../../systems/action-log-archive.md)」を参照してください。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | グローバル | 選択した各アクションのアクションログを有効にします：<br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Company Credit` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/><br/>`Customer Invitations`<br/>`Design Configuration`<br/>`Gift Registry Type` `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![管理者の使用状況](./assets/admin-usage.png)<!-- zoom -->

これらのオプションの設定について詳しくは、_はじめにガイド_&#x200B;の[使用データ収集](../../getting-started/admin.md#usage-data-collection)を参照してください。

| フィールド | 範囲 | 説明 |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | グローバル | 管理者の使用状況データを収集する権限をAdobeに付与して、_管理者_&#x200B;および関連製品やサービスの使用体験を向上させます。 データ収集を許可すると、_製品内ガイダンス_&#x200B;も有効になります。このガイダンスは、_管理者_&#x200B;にヘルプ、ツールヒント、ウォークスルーのガイド、オンボーディング情報、機能のお知らせなどのインタラクティブなコンテンツを提供するように設計されています。 使用状況データでは、個々の管理者は識別されません。 オプション：<br />**`Yes`**- データ収集を許可し、_製品内ガイダンス_.<br />**`No`**&#x200B;を有効にします - データ収集を許可せず、製品内ガイダンス _を有効にしません。_ |

{style="table-layout:auto"}
