---
title: メールテンプレート
description: メールテンプレートの概要と、それらを使用して顧客へのコミュニケーションをサポートし、ブランドを強化する方法について説明します。
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# メールテンプレート

メールテンプレートは、ストアから送信される自動メッセージのレイアウト、コンテンツ、書式を定義します。 各トランザクションメールは、特定のタイプのトランザクションまたはイベントに関連付けられているので、トランザクションメールと呼ばれます。

Commerceには、ストアの操作中に発生する様々なイベントによってトリガーされる一連のレスポンシブメールテンプレートが含まれています。 各テンプレートは画面サイズに合わせて最適化されており、デスクトップだけでなく、タブレットやモバイルデバイスでも表示できます。 顧客アクティビティ、販売、製品アラート、管理者アクション、システムメッセージに関連する様々な準備済みのメールテンプレートがあり、ブランドを反映するために [ カスタマイズ ](email-template-custom.md) できます。

Commerce メールは、HTMLおよびプレーンテキストのメールクライアントでレンダリングできます。 メールのレンダリング方法は、クライアント間で多少異なる場合があります。

## 電子メールロゴの準備

ロゴは、次のいずれかのファイル形式で保存できます。 背景が透明なロゴは、.PNG ファイルまたは。GIF ファイルとして保存できます。

- JPG/JPEG
- GIF
- PNG

ヘッダーテンプレートに指定されたディメンションがあります。 ただし、高解像度デバイスでロゴが適切にレンダリングされるようにするには、アップロードする画像のサイズをこの 3 倍にする必要があります。 通常、元のロゴアートワークはベクトル画像として作成されるので、解像度を損なうことなく拡大することができます。 その後、サポートされているビットマップ画像形式の 1 つに画像を保存できます。

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

ヘッダーの垂直方向のスペースが制限されていることを利用するには、必ず画像を切り抜いて、上部または下部の無駄なスペースを排除します。 画像を編集する場合は、ロゴの縦横比を維持して、高さと幅が均等にサイズ変更されるように注意します。

原則として、画像を元の画像よりも小さくすることはできますが、解像度を損なうことなく大きくすることはできません。 小さな画像を撮影してフォトエディターで拡大すると、画像の解像度が低下します。 例えば、ヘッダーテンプレートでロゴの表示寸法が幅 168 ピクセル、高さ 48 ピクセルの場合、アップロードする画像は幅 504 ピクセル、高さ 144 ピクセルにする必要があります。

| ロゴのDimension | 1 x （画面サイズ） | 3 x （画像サイズ） |
|----------|----|----|
| 幅： | 168 ピクセル | 504 ピクセル |
| 高さ： | 48 ピクセル | 144 ピクセル |

{style="table-layout:auto"}

## メールテンプレートの設定

この設定により、デフォルトのヘッダーテンプレートに表示されるロゴと、ストアから送信されるトランザクションメールメッセージに使用する任意のカスタム [ ヘッダー ](email-template-custom.md#header-template) および [ フッター ](email-template-custom.md#footer-template) テンプレートが決まります。

![ トランザクションメールデザイン ](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

構成設定の詳細なリストについては、『 [_コンテンツおよびデザインガイド_ の _](../content-design/configuration.md)トランザクションメール_ を参照してください。

## 手順 1. ロゴをアップロード

1. _管理者_ サイドバーで、**[!UICONTROL Content]**/_[!UICONTROL Design]_/**[!UICONTROL Configuration]**に移動します。

1. 設定するストア表示を見つけ、_[!UICONTROL Action]_列の&#x200B;**[!UICONTROL Edit]**をクリックします。

1. 「_[!UICONTROL Other Settings]_」の下の「展開セレクター ![ 「**[!UICONTROL Transactional Emails]**」セクション ](../assets/icon-display-expand.png) を展開します。

1. 準備した **[!UICONTROL Logo Image]** をアップロードするには、「**[!UICONTROL Upload]**」をクリックしてシステムからファイルを選択します。

1. **[!UICONTROL Logo Image Alt]**：代替テキストを入力して画像を識別します。

1. **[!UICONTROL Logo Width]** と **[!UICONTROL Logo Height]** をピクセル単位で入力します。

   各値を、`px` の省略形を除いた数字で入力します。 これらの値は、画像の実際のサイズではなく、ヘッダー内のロゴの表示寸法を参照します。

## 手順 2. ヘッダーテンプレートとフッターテンプレートの選択

自分のストアまたは異なるストアにカスタムのヘッダーおよびフッターテンプレートがある場合は、設定の [ スコープ ](../getting-started/websites-stores-views.md#scope-settings) に従って、それぞれに使用するテンプレートを指定できます。 それ以外の場合は、デフォルトのテンプレートが使用されます。 詳しくは、[ メールテンプレートのカスタマイズ ](email-template-custom.md) を参照してください。

1. すべてのトランザクションメールメッセージに使用する **[!UICONTROL Header Template]** を選択します。

1. すべてのトランザクションメールメッセージに使用する **[!UICONTROL Footer Template]** を選択します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## メールテンプレートリスト

メールテンプレートのリストは、モジュールごとにアルファベット順に整理されます。

### [!DNL Amazon_Payment]

| Template | 設定パス |
|--- |--- |
| `Hard-declined Authorization` | 該当なし |
| `Soft-declined Authorization` | 該当なし |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Template | 設定パス |
|--- |--- |
| `Payment Failed` | **ページ：** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**セクション：** [!UICONTROL Payment Failed Emails]<br/>**フィールド：** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）

| Template | 設定パス |
|--- |--- |
| `Assign Company Admin` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **ページ：** [!UICONTROL Customers] > [ 会社設定 ](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails] <br/>**フィールド：** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | 該当なし |
| `Company Registration Request` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Email Options - Company Registration]<br/>**フィールド：** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Status Change]<br/>**フィールド：** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Status Change]<br/>**フィールド：** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Status Change]<br/>**フィールド：** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Status Change]<br/>**フィールド：** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Status Change]<br/>**フィールド：** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Customer-Related Emails]<br/>**フィールド：** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）

| Template | 設定パス |
|--- |--- |
| `Credit Limit Allocated` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Credit]<br/>**フィールド：** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Credit]<br/>**フィールド：** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Credit]<br/>**フィールド：** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Credit]<br/>**フィールド：** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**セクション：** [!UICONTROL Company Credit]<br/>**フィールド：** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Template | 設定パス |
|--- |--- |
| `Contact Form` | **ページ：** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**セクション：** [!UICONTROL Email Options]<br/>**フィールド：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Template | 設定パス |
|--- |--- |
| `Change Email` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Account Information Options]<br/>**フィールド：** [!UICONTROL Change Email Template] |
| メールとパスワードの変更 | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Account Information Options]<br/>**フィールド：** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Password Options]<br/>**フィールド：** メールを忘れた場合のテンプレート |
| `New Account` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Create New Account Options]<br/>**フィールド：** デフォルトのウェルカムメール |
| `New Account (Magento/luma)` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Create New Account Options]<br/>**フィールド：** デフォルトのウェルカムメール |
| `New Account Confirmation Key` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Create New Account Options]<br/>**フィールド：** 確認リンクメール |
| `New Account Confirmed` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Create New Account Options]<br/>**フィールド：** お知らせメール |
| `New Account Without Password` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Create New Account Options]<br/>**フィールド：** デフォルトのパスワードなしのウェルカムメール |
| `Remind Password` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Password Options]<br/>**フィールド：** Remind Email Template |
| `Reset Password` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Password Options] <br/>**フィールド：** パスワードリセットテンプレート |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `Store Credit Update` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**セクション：** [!UICONTROL Store Credit Options]<br/>**フィールド：** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Template | 設定パス |
|--- |--- |
| `Currency Update Warnings` | **ページ：** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**セクション：** [!UICONTROL Scheduled Import Settings]<br/>**フィールド：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Template | 設定パス |
|--- |--- |
| `Footer` | 該当なし |
| `Footer (Magento/luma)` | 該当なし |
| `Header` | 該当なし |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `Gift Card(s) Purchase` | **ページ：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**セクション：** [!UICONTROL Gift Card Email Settings]<br/>**フィールド：** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Template | 設定パス |
|--- |--- |
| `Gift Card Code/Balance` | **ページ：** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**セクション：** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**フィールド：** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Template | 設定パス |
|--- |--- |
| `New Registry` | **ページ：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**セクション：** [!UICONTROL Owner Notification]<br/>**フィールド：** [!UICONTROL Email Template] |
| `Registry Sharing` | **ページ：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**セクション：** [!UICONTROL Gift Registry Sharing]<br/>**フィールド：** [!UICONTROL Email Template] |
| `Registry Update` | **ページ：** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**セクション：** [!UICONTROL Gift Registry Update]<br/>**フィールド：** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Template | 設定パス |
|--- |--- |
| `Order is Ready for Pickup` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Order Ready For Pickup in Store]<br/>**フィールド：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Order Ready For Pickup in Store]<br/>**フィールド：** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Template | 設定パス |
|--- |--- |
| `Customer Invitation` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**セクション：** [!UICONTROL Email]<br/>**フィールド：** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) （Adobe Commerce B2B でのみ使用可能）

| Template | 設定パス |
|--- |--- |
| `Declined Quote` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Expiration Date Reset] | **ページ：** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Quote]<br/>**フィールド：** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Template | 設定パス |
|--- |--- |
| `Subscription Confirmation` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**セクション：** [!UICONTROL  Subscription Options]<br/>**フィールド：** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**セクション：** [!UICONTROL  Subscription Options]<br/>**フィールド：** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**セクション：** [!UICONTROL  Subscription Options]<br/>**フィールド：** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Template | 設定パス |
|--- |--- |
| `Cron Error Warning` | **ページ：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**セクション：** [!UICONTROL Product Alerts Run Settings]<br/>**フィールド：** [!UICONTROL Error Email Template] |
| `Price Alert` | **ページ：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**セクション：** [!UICONTROL Product Alerts]<br/>**フィールド：** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **ページ：** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**セクション：** [!UICONTROL Product Alerts]<br/>**フィールド：** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Template | 設定パス |
|--- |--- |
| `Approved Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL Purchase Order Approval]<br/>**フィールド：** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `Promotion Notification/Reminder` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**セクション：** [!UICONTROL Automated Email Reminder Rules]<br/>**フィールド：** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `Balance Update` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**セクション：** [!UICONTROL Email Notification Settings]<br/>**フィールド：** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**セクション：** [!UICONTROL Email Notification Settings]<br/>**フィールド：** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `New RMA` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA]<br/>**フィールド：** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA]<br/>**フィールド：** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA Admin Comments]<br/>**フィールド：** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA Admin Comments]<br/>**フィールド：** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA Authorization]<br/>**フィールド：** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL  RMA Authorization]<br/>**フィールド：** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**セクション：** [!UICONTROL RMA Customer Comments]<br/>**フィールド：** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Template | 設定パス |
|--- |--- |
| `Credit Memo Update` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo Contents]<br/>**フィールド：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo Comments]<br/>**フィールド：** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo Comments]<br/>**フィールド：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo Comments]<br/>**フィールド：** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice Comments]<br/>**フィールド：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice Comments]<br/>**フィールド：** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice Comments]<br/>**フィールド：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice Comments]<br/>**フィールド：** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo]<br/>**フィールド：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md） <br/>**セクション：** [!UICONTROL Credit Memo]<br/>**フィールド：** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo]<br/>**フィールド：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Credit Memo]<br/>**フィールド：** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice]<br/>**フィールド：** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice]<br/>**フィールド：** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice]<br/>**フィールド：** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Invoice]<br/>**フィールド：** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order]<br/>**フィールド：** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order]<br/>**フィールド：** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order]<br/>**フィールド：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order]<br/>**フィールド：** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment]<br/>**フィールド：** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment]<br/>**フィールド：** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment]<br/>**フィールド：** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment]<br/>**フィールド：** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order Comments]<br/>**フィールド：** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order Comments]<br/>**フィールド：** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order Comments]<br/>**フィールド：** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Order Comments]<br/>**フィールド：** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment Comments]<br/>**フィールド：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment Comments]<br/>**フィールド：** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment Comments]<br/>**フィールド：** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **ページ：** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**セクション：** [!UICONTROL Shipment Comments]<br/>**フィールド：** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）

| Template | 設定パス |
|--- |--- |
| `Export Failed` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**セクション：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**フィールド：** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**セクション：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**フィールド：** [!UICONTROL Error Email Template] |
| `Import Failed` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**セクション：** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**フィールド：** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Template | 設定パス |
|--- |--- |
| `Send Product Link to Friend` | **ページ：** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**セクション：** [!UICONTROL Email Templates]<br/>**フィールド：** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Template | 設定パス |
|--- |--- |
| `Sitemap Generation Settings` | **ページ：** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**セクション：** [!UICONTROL Generation Settings]<br/>**フィールド：** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Template | 設定パス |
|--- |--- |
| `2FA Configuration Required by User` | 該当なし |
| `2FA Configuration Required for the Application` | 該当なし |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Template | 設定パス |
|--- |--- |
| `Forgot Admin Password` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**セクション：** [!UICONTROL Admin User Emails]<br/>**フィールド：** パスワードを忘れた場合のメールテンプレート |
| `User Notification` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**セクション：** [!UICONTROL Admin User Emails]<br/>**フィールド：** ユーザー通知テンプレート |
| `New User Notification` | **ページ：** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**セクション：** [!UICONTROL Admin User Emails]<br/>**フィールド：** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Template | 設定パス |
|--- |--- |
| `Magento Wish List Sharing` | **ページ：** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**セクション：** [!UICONTROL Share Options]<br/>**フィールド：** [!UICONTROL Email Template] |

{style="table-layout:auto"}
