---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Company Configuration]'
description: 次のページで設定を確認します： [!UICONTROL Customers] &gt; [!UICONTROL Company Configuration] コマース管理のページ。
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce向け B2B のインストールと有効化により、企業固有の機能で購入エクスペリエンスをパーソナライズできます。 Adobe Commerce用 B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能の詳細については、 [B2B for Adobe Commerceユーザーガイド](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

>[!NOTE]
>
>B2B 機能のこれらの設定オプションへのアクセスは、 [役割リソース](../../systems/permissions-user-roles.md#role-resources). これらの役割リソースは、管理者ユーザーに割り当てられたユーザーロールに対して設定する必要があります。

これらの設定について詳しくは、 [基本 B2B 機能の有効化](../../b2b/enable-basic-features.md) （内） _B2B for Adobe Commerceユーザーガイド_.

## [!UICONTROL General]

![一般](./assets/company-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | Web サイト | ストアの訪問者が [登録者](../../customers/customer-sign-in.md) 会社アカウントまたは個々のアカウントの場合。 オプション： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Email Options - Company Registration]

![メールオプション — 会社の登録](./assets/company-email-options-company-registration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | ストア表示 | ストアフロントから会社登録要求が送信されたときに通知されるストアの連絡先。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | ストア表示 | 登録通知のコピーを受け取る各人の電子メールアドレス。 複数の電子メールアドレスはコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | 登録電子メールのコピーを送信するために使用される電子メールメソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | ストア表示 | 会社登録通知にデフォルトで使用される電子メールテンプレート。 デフォルトのテンプレート： `Company Registration Request` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Customer-Related Emails]

![顧客関連メール](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | ストア表示 | セールス担当者が会社のアカウントに割り当てられる際にデフォルトで使用される電子メールテンプレート。 この電子メールは、セールス担当者および会社の管理者に送信されます。 デフォルトのテンプレート： `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | ストア表示 | 個々の顧客アカウントが会社アカウントに割り当てられる際にデフォルトで使用される電子メールテンプレート。 この E メールは顧客にのみ送信されます。 デフォルトのテンプレート： `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | ストア表示 | 会社の管理者が会社に割り当てられる際に使用される電子メールテンプレート。 この電子メールは、セールス担当者および会社の管理者に送信されます。 デフォルトのテンプレート： `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | ストア表示 | 会社管理者の役割を果たす人のステータスが「非アクティブ」に変わった場合にデフォルトで使用される電子メールテンプレートです。 システムは、変更の電子メール通知を新しい会社と以前の会社の管理者に送信します。 デフォルトのテンプレート： `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | ストア表示 | 以前の会社管理者が会社メンバーになったときにデフォルトで使用される電子メールテンプレートです。 電子メールは会社のメンバーにのみ送信されます。 デフォルトのテンプレート： `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | ストア表示 | 顧客のステータスがアクティブになったときにデフォルトで使用される電子メールテンプレート。 この E メールは顧客にのみ送信されます。 デフォルトのテンプレート： `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | ストア表示 | 顧客のステータスが非アクティブになったときにデフォルトで使用される電子メールテンプレート。 この E メールは顧客にのみ送信されます。 デフォルトのテンプレート： `Customer Status Inactive` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Company Status Change]

![会社ステータスの変更](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | ストア表示 | 会社のステータスが変更されたときに通知される店舗の連絡先。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | ストア表示 | 会社ステータス変更通知のコピーを受け取る各人の電子メールアドレス。 複数の電子メールアドレスはコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | ステータス変更通知のコピーを送信するために使用する電子メールメソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | ストア表示 | 会社のステータスが _承認待ち_ から _アクティブ_. デフォルトのテンプレート： `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | ストア表示 | 会社のステータスが次の日から変わったときにデフォルトで使用される電子メールテンプレート _却下_ または _ブロック_ から _アクティブ_. デフォルトのテンプレート： `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | ストア表示 | 会社のステータスが「 _却下_. デフォルトのテンプレート： `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | ストア表示 | 会社のステータスが「 _ブロック_. デフォルトのテンプレート： `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | ストア表示 | 会社のステータスが「 _承認待ち_. デフォルトのテンプレート： `Company Status Pending Approval` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Company Credit]

![会社クレジット](./assets/company-email-options-company-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | ストア表示 | 会社のクレジットに変更が生じたときに通知されるストアの連絡先。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | ストア表示 | 会社の信用変更通知のコピーを受け取る各人の電子メールアドレス。 複数の電子メールアドレスはコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | クレジット変更通知のコピーを送信するために使用する電子メールメソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | ストア表示 | 会社のクレジットが割り当てられる際にデフォルトで使用される電子メールテンプレート。 この電子メールは会社の管理者に送信されます。 デフォルトのテンプレート： `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | ストア表示 | 会社のクレジット制限が更新されたときにデフォルトで使用される電子メールテンプレート。 この電子メールは会社の管理者に送信されます。 デフォルトのテンプレート： `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | ストア表示 | デフォルトで、 [償還](../../b2b/credit-company.md#apply-a-payment-to-a-company-account) 会社の信用を得る この電子メールは会社の管理者に送信されます。 デフォルトのテンプレート： `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | ストア表示 | 注文額が会社のクレジットに返金される際にデフォルトで使用される電子メールテンプレート。 この電子メールは会社の管理者に送信されます。 デフォルトのテンプレート： `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | ストア表示 | 注文が会社のクレジットに戻されたときにデフォルトで使用される電子メールテンプレート。 この電子メールは会社の管理者に送信されます。 デフォルトのテンプレート： `Order Reverted to Company Credit` |

{:style=&quot;table-layout:auto&quot;}
