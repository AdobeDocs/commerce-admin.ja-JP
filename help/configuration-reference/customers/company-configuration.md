---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Company Configuration]'
description: の設定を確認します。 [!UICONTROL Customers] &gt; [!UICONTROL Company Configuration] コマース管理者のページ。
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2B をインストールして有効化すると、会社固有の機能を使用して購入体験をパーソナライズできます。 Adobe Commerce B2B は、B2B モデルと B2C モデルの両方をサポートする統合ソリューションです。 B2B 機能について詳しくは、 [Adobe Commerce B2B ユーザーガイド](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

>[!NOTE]
>
>B2B 機能に対するこれらの設定オプションへのアクセスは、 [役割リソース](../../systems/permissions-user-roles.md#role-resources). これらのロールリソースは、管理者ユーザーに割り当てられたユーザーロール用に設定される必要があります。

これらの設定の詳細については、を参照してください。 [基本的な B2B 機能の有効化](../../b2b/enable-basic-features.md) が含まれる _Adobe Commerce B2B ユーザーガイド_.

## [!UICONTROL General]

![一般](./assets/company-general.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | Web サイト | ストアへの訪問者が以下を選択できるかどうかを決定します [登録](../../customers/customer-sign-in.md) 会社アカウントまたは個人アカウントの場合。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![メールオプション – 会社登録](./assets/company-email-options-company-registration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | ストア表示 | 会社の登録要求がストアフロントから送信されたときに通知される店舗連絡先。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | ストア表示 | 登録通知のコピーを受け取る各担当者の電子メールアドレス。 複数のメールアドレスを指定する場合はコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | 登録 E メールのコピーを送信するために使用される E メール メソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | ストア表示 | 会社登録通知にデフォルトで使用されるメールテンプレート。 デフォルトのテンプレート： `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![顧客関連のメール](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | ストア表示 | 営業担当者が会社アカウントに割り当てられたときに既定で使用される E メール テンプレート。 このメールは、営業担当者と会社の管理者に送信されます。 デフォルトのテンプレート： `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | ストア表示 | 個々の顧客アカウントが会社アカウントに割り当てられている場合にデフォルトで使用されるメールテンプレート。 このメールは、顧客にのみ送信されます。 デフォルトのテンプレート： `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | ストア表示 | 会社管理者が会社に割り当てられたときに使用される E メール テンプレートです。 このメールは、営業担当者と会社の管理者に送信されます。 デフォルトのテンプレート： `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | ストア表示 | 会社管理者の役割を果たすユーザーのステータスが「非アクティブ」に変更された場合にデフォルトで使用されるメールテンプレート。 システムは、新規管理者と元会社管理者に変更のメール通知を送信します。 デフォルトのテンプレート： `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | ストア表示 | 元の会社管理者が会社メンバーになった際にデフォルトで使用されるメールテンプレート。 メールは会社メンバーにのみ送信されます。 デフォルトのテンプレート： `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | ストア表示 | 顧客のステータスがアクティブになる際にデフォルトで使用されるメールテンプレート。 このメールは、顧客にのみ送信されます。 デフォルトのテンプレート： `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | ストア表示 | 顧客のステータスが非アクティブになった場合にデフォルトで使用されるメールテンプレート。 このメールは、顧客にのみ送信されます。 デフォルトのテンプレート： `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![会社ステータスの変更](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | ストア表示 | 会社のステータスが変更されるたびに通知される店舗連絡先。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | ストア表示 | 会社の状態変更通知のコピーを受信する各担当者の電子メール アドレス。 複数のメールアドレスを指定する場合はコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | 状態変更通知のコピーを送信するために使用される電子メール メソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | ストア表示 | 会社の状態の変更時に使用する E メール テンプレート _承認待ち_ 対象： _アクティブ_. デフォルトのテンプレート： `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | ストア表示 | 会社の状態が次の場所から変更されたときに既定で使用される E メール テンプレート _却下_ または _ブロック_ 対象： _アクティブ_. デフォルトのテンプレート： `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | ストア表示 | 会社の状態が次のように変更されたときにデフォルトで使用される E メール テンプレート _却下_. デフォルトのテンプレート： `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | ストア表示 | 会社の状態が次のように変更されたときにデフォルトで使用される E メール テンプレート _ブロック_. デフォルトのテンプレート： `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | ストア表示 | 会社の状態が次のように変更されたときにデフォルトで使用される E メール テンプレート _承認待ち_. デフォルトのテンプレート： `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![会社クレジット](./assets/company-email-options-company-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | ストア表示 | 会社のクレジットが変更されるたびに通知される店舗担当者。 オプション： `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | ストア表示 | 会社の信用変更通知のコピーを受信する各担当者の電子メール アドレス。 複数のメールアドレスを指定する場合はコンマで区切ります。 |
| [!UICONTROL Send Email Copy Method] | ストア表示 | 与信変更通知のコピーを送信するために使用される電子メール メソッド。 オプション： `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | ストア表示 | 会社のクレジットが割り当てられる際にデフォルトで使用される E メール テンプレート。 このメールは、会社管理者に送信されます。 デフォルトのテンプレート： `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | ストア表示 | 会社の与信限度額が更新された際にデフォルトで使用される E メール テンプレート。 このメールは、会社管理者に送信されます。 デフォルトのテンプレート： `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | ストア表示 | 次の場合にデフォルトで使用されるメールテンプレート [償還](../../b2b/credit-company.md#apply-a-payment-to-a-company-account) 会社のクレジットに対して行われます。 このメールは、会社管理者に送信されます。 デフォルトのテンプレート： `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | ストア表示 | 注文の金額が会社クレジットに払い戻される際にデフォルトで使用されるメールテンプレート。 このメールは、会社管理者に送信されます。 デフォルトのテンプレート： `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | ストア表示 | 注文が会社クレジットに戻された際にデフォルトで使用されるメールテンプレート。 このメールは、会社管理者に送信されます。 デフォルトのテンプレート： `Order Reverted to Company Credit` |

{style="table-layout:auto"}
