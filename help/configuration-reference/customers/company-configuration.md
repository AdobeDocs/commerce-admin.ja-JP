---
title: '[!UICONTROL Customers] > [!UICONTROL Company Configuration]'
description: Commerce管理者の[!UICONTROL Customers] > [!UICONTROL Company Configuration] ページで設定を確認します。
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2Bのインストールと有効化により、企業固有の機能を使用して購買体験をパーソナライズできます。 Adobe Commerce B2Bは、B2BとB2Cの両方のモデルをサポートする統合ソリューションです。 B2B機能について詳しくは、[Adobe Commerce B2B ユーザーガイド &#x200B;](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ja)を参照してください。

>[!NOTE]
>
>B2B機能のこれらの設定オプションへのアクセスは、[役割リソース &#x200B;](../../systems/permissions-user-roles.md#role-resources)によって制御されます。 これらの役割リソースは、管理者ユーザーに割り当てられたユーザー役割に設定する必要があります。

これらの設定について詳しくは、_Adobe Commerce B2B ユーザーガイド_&#x200B;の「[基本的なB2B機能を有効にする](../../b2b/enable-basic-features.md)」を参照してください。

## [!UICONTROL General]

![一般](./assets/company-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | web サイト | ストアへの訪問者が、会社アカウントまたは個人アカウントの[登録](../../customers/customer-sign-in.md)を選択できるかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![電子メール オプション – 会社登録](./assets/company-email-options-company-registration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | ストアビュー | 企業登録リクエストがストアフロントから送信されたときに通知されるストア連絡先。 オプション：`General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | ストアビュー | 登録通知のコピーを受け取る各人物の電子メールアドレス。 複数のメールアドレスをコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストアビュー | 登録メールのコピーを送信するために使用されるメール方法。 オプション：`Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | ストアビュー | 会社登録通知にデフォルトで使用される電子メールテンプレート。 既定のテンプレート：`Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![顧客関連の電子メール &#x200B;](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | ストアビュー | 営業担当者が会社アカウントに割り当てられたときにデフォルトで使用されるメールテンプレート。 このメールは、営業担当者と会社の管理者に送信されます。 既定のテンプレート：`Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | ストアビュー | 個々の顧客アカウントが会社アカウントに割り当てられるときに、デフォルトで使用されるメールテンプレート。 このメールはお客様にのみ送信されます。 既定のテンプレート：`Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | ストアビュー | 会社の管理者が会社に割り当てられたときに使用される電子メールテンプレート。 このメールは、営業担当者と会社の管理者に送信されます。 既定のテンプレート：`Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | ストアビュー | 会社管理者を務めるユーザーのステータスが「非アクティブ」に変更された場合に、デフォルトで使用されるメールテンプレート。 システムは、変更の通知を新しい会社と以前の会社の管理者に電子メールで送信します。 既定のテンプレート：`Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | ストアビュー | 以前の会社管理者が会社のメンバーになった場合にデフォルトで使用されるメールテンプレート。 このメールは会社のメンバーにのみ送信されます。 既定のテンプレート：`Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | ストアビュー | 顧客のステータスがアクティブになったときにデフォルトで使用される電子メールテンプレート。 このメールはお客様にのみ送信されます。 既定のテンプレート：`Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | ストアビュー | 顧客のステータスが非アクティブになったときにデフォルトで使用される電子メールテンプレート。 このメールはお客様にのみ送信されます。 既定のテンプレート：`Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![会社ステータスの変更](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | ストアビュー | 会社のステータスが変更されるたびに通知されるストア連絡先。 オプション：`General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | ストアビュー | 会社のステータス変更通知のコピーを受け取る各人物の電子メールアドレス。 複数のメールアドレスをコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストアビュー | ステータス変更通知のコピーを送信するために使用されるメール方法。 オプション：`Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | ストアビュー | 会社のステータスが&#x200B;_承認待ち_&#x200B;から&#x200B;_アクティブ_&#x200B;に変更されたときに使用される電子メールテンプレート。 既定のテンプレート：`Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | ストアビュー | 会社のステータスが&#x200B;_拒否_&#x200B;または&#x200B;_ブロック_&#x200B;から&#x200B;_アクティブ_&#x200B;に変更されたときに、デフォルトで使用される電子メールテンプレート。 既定のテンプレート：`Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | ストアビュー | 会社のステータスが&#x200B;_Rejected_&#x200B;に変更されたときにデフォルトで使用される電子メールテンプレート。 既定のテンプレート：`Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | ストアビュー | 会社のステータスが&#x200B;_ブロック済み_&#x200B;に変更されたときにデフォルトで使用される電子メールテンプレート。 既定のテンプレート：`Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | ストアビュー | 会社のステータスが&#x200B;_承認待ち_&#x200B;に変更されたときにデフォルトで使用される電子メールテンプレート。 既定のテンプレート：`Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![会社クレジット &#x200B;](./assets/company-email-options-company-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | ストアビュー | 会社のクレジットに変更があった場合に常に通知される店舗の連絡先。 オプション：`General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | ストアビュー | 会社の信用変更通知のコピーを受け取る各人の電子メールアドレス。 複数のメールアドレスをコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストアビュー | クレジット変更通知のコピーを送信するために使用されるメール方法。 オプション：`Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | ストアビュー | 会社のクレジットが割り当てられるときにデフォルトで使用される電子メールテンプレート。 このメールは会社の管理者に送信されます。 既定のテンプレート：`Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | ストアビュー | 会社のクレジット制限が更新されたときにデフォルトで使用される電子メールテンプレート。 このメールは会社の管理者に送信されます。 既定のテンプレート：`Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | ストアビュー | [払い戻し](../../b2b/credit-company.md#apply-a-payment-to-a-company-account)が会社のクレジットに対して行われた場合に、デフォルトで使用される電子メールテンプレート。 このメールは会社の管理者に送信されます。 既定のテンプレート：`Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | ストアビュー | 注文の金額が会社のクレジットに返金される際に、デフォルトで使用される電子メールテンプレート。 このメールは会社の管理者に送信されます。 既定のテンプレート：`Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | ストアビュー | 注文が会社のクレジットに戻されたときにデフォルトで使用される電子メールテンプレート。 このメールは会社の管理者に送信されます。 既定のテンプレート：`Order Reverted to Company Credit` |

{style="table-layout:auto"}
