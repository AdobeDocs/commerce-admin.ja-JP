---
title: ユーザーの役割
description: ユーザーの役割および関連する権限を作成して、管理機能へのアクセスを管理する方法について説明します。
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# ユーザーの役割

管理者へのアクセスを制限されたユーザーを許可するには、まず、適切なレベルの権限を持つ役割を作成します。 役割を保存したら、新しいユーザーを追加し、制限付きの役割を割り当てて、管理者への制限付きアクセスを許可できます。

![管理者 – ユーザーの役割](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## 役割の定義

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. 右上隅のをクリックします。 **[!UICONTROL Add New Role]**.

1. 役割を定義する手順を実行します。

### 手順 1：役割名の追加

1. 次の下 _[!UICONTROL Role Information]_、説明的なを入力します&#x200B;**[!UICONTROL Role Name]**.

1. 次の下 _[!UICONTROL Current User Identity Verification]_、パスワードを入力します。

   ![システム権限 – 役割情報](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### 手順 2：リソースを割り当てる

>[!IMPORTANT]
>
>リソースを割り当てる際に、特定の役割のアクセスを制限している場合は、権限ツールへのアクセスを無効にしてください。 そうでない場合、ユーザーは自分の権限を変更できます。

1. を設定 **[!UICONTROL Role Scopes]** を次のいずれかに変更します。

   - `All`
   - `Custom`

   に設定されている場合 `Custom` マルチサイトインストールの場合は、web サイトのチェックボックスをオンにして、役割を使用するストアを選択します。

   ![ユーザーの役割リソース – カスタム範囲](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >を使用しているユーザー `Custom` の役割の範囲で、web サイトとカテゴリの作成、カテゴリへの製品の割り当て、製品の編集を行うことができません。 _[!UICONTROL All Store Views]_制限付きストアに割り当てられる場合の範囲。 これらのユーザーは、他の操作も実行できません_ global _アクセス権を持たないスコープに影響するアクション。

1. 次の下 _[!UICONTROL Roles Resources]_、設定&#x200B;**[!UICONTROL Resource Access]**対象： `Custom`.

1. が含まれる **[!UICONTROL Resource]** ツリー構造で、役割がアクセスできる各管理機能のチェックボックスを選択します。

   税金設定へのアクセス権を持つ管理者ロールを作成するには、「売上/税金」および「システム/税金」リソースの両方を選択します。 デフォルトとは異なる地域用に web サイトを設定する場合 [出荷元](../stores-purchase/shipping-settings.md#point-of-origin)。役割のシステム /配送料リソースへのアクセスを許可する必要があります。 配送設定によって、カタログ価格に使用する店舗の税率が決まります。

   ![割り当てられたユーザーの役割リソース](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   使用可能な権限のリストには、バンドルされた拡張機能やインストールされた拡張機能に対する追加のオプションが含まれる場合があります。 各機能の最上位の権限を選択すると、ユーザーに使用可能なすべての権限を割り当てることができます。

   >[!NOTE]
   >
   >管理者ユーザーには次が必要です **[!UICONTROL Sales / Archive]** 役割の範囲に対するを表示する権限 _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_、および _[!UICONTROL Shipments]_順序 [タブ](../stores-purchase/order-processing.md).

1. 完了したら、 **[!UICONTROL Save Role]**.

   役割がグリッドに表示され、ユーザーアカウントに割り当てることができます。

## ユーザーへの役割の割り当て

1. から _[!UICONTROL Roles]_グリッドで、編集モードでレコードを開きます。

1. 次の下 _[!UICONTROL Current User Identity Verification]_：ユーザーアカウントのパスワードを入力します。

1. 左パネルで、を選択します。 **[!UICONTROL Role Users]**.

   この _[!UICONTROL Role Users]_新しい役割を保存した後にのみオプションが表示されます。

   ![役割に割り当てられているユーザーアカウント](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. 特定のユーザーレコードを検索するには、次の手順を実行します。

   - 列の上部にある検索フィルターに値を入力して、キーを押します **Enter**.

   - 完全なリストに戻る準備ができたら、 **[!UICONTROL Reset Filter]**.

1. 役割に割り当てるユーザーのチェックボックスを選択します。

1. クリック **[!UICONTROL Save Role]**.

## 役割の編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. グリッドの上にあるフィルターを使用して役割を見つけ、役割名をクリックします。

1. 必要な変更を加えます。

   役割の設定については、ユーザーの役割を作成する手順を参照してください。

1. プロンプトが表示されたら、パスワードを入力して ID を確認します。

1. 「」をクリックします **[!UICONTROL Save Role]**.

## 役割の削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. グリッドの上にあるフィルターを使用して役割を見つけ、編集モードで開きます。

1. 右上隅のをクリックします。 **[!UICONTROL Delete Role]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## ユーザーの役割のデモ

ユーザーの役割の管理については、次のビデオをご覧ください。

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## 役割リソース

カスタムの役割には、次のリソースへのアクセス権を割り当てることができます。 各リソースに関連付けられている機能について詳しくは、リンクされているページを参照してください。

![Adobe Commerce](../assets/adobe-logo.svg) - Adobe Commerceのみ

![Adobe Commerce B2B](../assets/b2b.svg) - Adobe Commerce B2B でのみ使用可能

| Resource |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)） | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [コンテンツのステージング](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
