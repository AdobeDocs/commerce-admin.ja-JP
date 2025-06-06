---
title: 会社アカウントの作成
description: Adobe Commerce Admin での会社アカウントの作成と、ストアフロントでの会社アカウントの作成について説明します。
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 5312aa3f483399ecc4e9491b39f8300d8616e9e5
workflow-type: tm+mt
source-wordcount: '1762'
ht-degree: 0%

---

# 会社アカウントの作成

会社アカウントは、顧客がストアフロントから、または管理者から設定できます。 会社アカウントを作成するリクエストはすべて、アカウントが有効になる前に、ストア管理者の承認が必要です。

ストアフロントから会社アカウントを設定するユーザーには、[ 会社管理者 ](account-company-admin.md) の役割が割り当てられます。 会社アカウントを作成するリクエストが承認されると、会社の管理者はアカウントのパスワードを設定し、アカウントにログインできます。

## 方法 1：顧客がストアフロントからアカウントを作成する

>[!IMPORTANT]
>
>この方法をサポートするには（顧客がストアフロントから会社を登録できるようにします）、[B2B 機能 ](enable-basic-features.md) が有効になっていることを確認します。

1. ストアフロントヘッダーの右上隅で、顧客が「**[!UICONTROL Create an Account]**」をクリックして **[!UICONTROL Create New Company Account]** を選択します。

   ![ 新しい会社アカウントの作成 ](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >訪問者が登録済みユーザーアカウントにログインしている場合は、_[!UICONTROL Customer Profile]_/**[!UICONTROL Company Structure]**/**[!UICONTROL Create a Company Account]**&#x200B;に移動して、会社アカウントを作成できます。

1. _[!UICONTROL Company Information]_&#x200B;のセクションでは、顧客は次の操作を行います。

   - 必須フィールドに入力します。

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - 必要に応じて、残りのフィールドに入力します。

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![ 会社情報 ](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. _[!UICONTROL Legal Address]_&#x200B;セクションの必須フィールドに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![ 住所 ](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. _[!UICONTROL Company Administrator]_&#x200B;セクションでは、は次の操作を実行します。

   - 会社管理者の **[!UICONTROL Email address]** を入力します。

     会社管理者のメールアドレスは、会社のメールアドレスと同じでも、別のメールアドレスでもかまいません。 別のメールアドレスを入力した場合は、会社管理者アカウントに加えて、会社ユーザーアカウントが作成されます。

   - 会社管理者の **[!UICONTROL First Name]** と **[!UICONTROL Last Name]** を入力します。

   - 必要に応じて、次のフィールドに入力します。

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Work Phone Number]**
      - **[!UICONTROL Gender]**

   ![ 会社管理者 ](./assets/company-administrator-account-storefront.png)

1. このストアフロント関数で reCAPTCHA が有効になっている場合、検証を完了します。

1. 情報が完成したら、「**[!UICONTROL Submit]**」を選択します。

   会社のアカウントを作成するリクエストがマーチャントによって承認されると、メール通知が会社の管理者に送信されます。

   ![ ウェルカムメールの例 ](./assets/company-admin-welcome-email.png){width="500"}

   パスワードを設定すると、会社の管理者はアカウントに [ ログイン ](../customers/customer-sign-in.md) できます。

## 方法 2：マーチャントが管理者からアカウントを作成します

管理者から会社を作成するプロセスは、基本的にストアフロントからのプロセスと同じですが、フィールドが追加されます。

![ 管理者から新しい会社を追加する ](./assets/company-add-new.png){width="700" zoomable="yes"}

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. 「**[!UICONTROL Add New Company]**」をクリックして、次の操作を実行します。

   - 次の必須フィールドに入力します。

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - アカウントを運用する準備が整っていない場合は、**[!UICONTROL Status]** を `Pending Approval` に設定します。 （デフォルトで `Active` に設定されています）。

   - 該当する場合は、アカウントを管理する **[!UICONTROL Sales Representative]** の管理者アカウントを選択します。

1. _[!UICONTROL Account Information]_&#x200B;セクションで、次の操作を行います。

   - 必要に応じて、次のフィールドに入力します。

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - **[!UICONTROL Comment]**：必要になる可能性のある顧客に関する追加情報を入力します。

     コメントは、管理者からのみ表示されます。

   ![ 口座情報 ](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. 会社の初回作成時には、_[!UICONTROL Company Hierarchy]_&#x200B;グリッドは展開すると空になります。 会社を保存したら、その会社を会社階層に含めることができます。 [ 会社管理 ](manage-companies.md) を参照してください。

1. 「_[!UICONTROL Legal Address]_」セクションで、次の必須フィールドに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. _[!UICONTROL Company Admin]_&#x200B;セクションで、次の操作を行います。

   - 次の必須フィールドに入力します。

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - 一部のお客様の名前に他よりも多く適用される可能性があり、お客様の裁量で使用できる次のオプションの部分に名前を入力します。

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - 情報が使用可能な場合は、残りのフィールドに入力して、会社管理者について説明します。

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Work Phone Number]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![ 会社管理者 ](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 顧客の与信アクティビティの要約を表示する「_[!UICONTROL Company Credit]_」セクションでは、セクション下部の多数のフィールドに適宜入力します。

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![ 企業信用 ](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. _[!UICONTROL Advanced Settings]_&#x200B;セクションで、次の操作を行います。

   >[!NOTE]
   >
   >顧客グループ割り当てによって、会社とその従業員が使用できる共有カタログが決まります。 デフォルトでは、会社は、設定でデフォルトとして設定されている顧客グループに割り当てられます。

   - 会社とその従業員の **[!UICONTROL Customer Group]** 割り当てを、別の共有カタログまたは標準の顧客グループへのアクセス権を持つグループに変更できます。 グループを変更する前に確認を求められます。

     ![ 顧客グループの変更 ](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - 会社の従業員が自分のアカウントから見積もりを生成できるようにする場合は、**[!UICONTROL Allow Quotes]** を `Yes` に設定します。

   - 会社の従業員が自分のアカウントから発注書を作成して使用できるようにする場合は、**[!UICONTROL Enable Purchase Orders]** を `Yes` に設定します。

   - 会社で使用可能な **[!UICONTROL Applicable Payment Methods]** を変更するには、「**[!UICONTROL Use config settings]**」チェックボックスをオフにして、次のいずれかを選択します。

     | オプション | 説明 |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | （デフォルト） B2B 注文に対して、すべての [ デフォルトとして設定された支払方法 ](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) を有効にします。 |
     | `All Enabled Payment Methods` | 会社コードに関連付けられている顧客コードに対して、すべての [ 有効な支払い方法 ](../configuration-reference/sales/payment-methods.md) を使用できるようにします。 |
     | `Selected Payment Methods` | 会社アカウントに関連付けられた顧客アカウントに使用できる支払い方法を選択できます。 複数の支払い方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各オプションを選択します。 |

     {style="table-layout:auto"}

   - 会社で使用可能な **[!UICONTROL Applicable Shipping Methods]** を変更するには、「**[!UICONTROL Use config settings]**」チェックボックスをオフにして、次のいずれかを選択します。

     | オプション | 説明 |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | （デフォルト） B2B 注文に対して、すべての [ デフォルトとして設定された発送方法 ](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) を有効にします。 |
     | `All Enabled Shipping Methods` | 会社アカウントに関連付けられた顧客アカウントで [&#128279;](../configuration-reference/sales/delivery-methods.md) 有効な配送方法」をすべて使用できるようにします  |
     | `Selected Shipping Methods` | 会社アカウントに関連付けられている顧客アカウントで使用できる発送方法を選択できます。 複数の配送方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各オプションを選択します。 |

     {style="table-layout:auto"}

1. 完了したら、「**[!UICONTROL Save]**」を選択します。

   会社のアカウントを作成するリクエストがマーチャントによって承認されると、メール通知が会社の管理者のメールアドレスに送信されます。

   パスワードを設定すると、会社の管理者はアカウントに [ ログイン ](../customers/customer-sign-in.md) できます。

## ボタンバー

| ボタン | 説明 |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | 変更を保存せずに会社ページに戻ります。 |
| [!UICONTROL Reset] | 変更が保存されていないすべてのフィールドに元の値を復元します。 |
| [!UICONTROL Save] | 会社への変更を保存し、プロファイルを開いたままにします。 |
| [!UICONTROL Save & Close] | 会社への変更を保存し、プロファイルを閉じます。 |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | 会社名は、会社アカウントが最初に作成されたときに入力され、完全な法的名の短縮バージョンにすることができます。 |
| [!UICONTROL Status] | （管理者のみ）会社アカウントの現在の状態を示します。 オプション：<br/>**[!UICONTROL Active]**– 会社アカウントはストア管理者によって承認されています。 会社の管理者と関連するメンバーは、ストアフロントからアカウントにログインして購入することができます。<br/>**[!UICONTROL Pending Approval]** – 会社アカウントを開くリクエストが送信されましたが、ストア管理者によってはまだ承認されていません。 <br/>**[!UICONTROL Rejected]**– 会社のアカウントを開く要求が送信されましたが、ストア管理者によって承認されませんでした。 リクエストの送信に使用された初期ログイン資格情報はブロックされます。<br/>**&#x200B; ブロック &#x200B;**– 会社のメンバーはログインしてカタログにアクセスできますが、購入することはできません。 ストア管理者が、状態の良くない会社アカウントをブロックしている可能性があります。 アカウントのブロックは、ストア管理者がいつでも削除できます。 |
| [!UICONTROL Company Email] | 会社アカウントに関連付けられているメールアドレス。 |
| [!UICONTROL Sales Representative] | （管理者のみ）会社アカウントの主要連絡先である管理者ユーザー。 |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| フィールド | 説明 |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | 会社の正式名称。 |
| [!UICONTROL VAT / TAX ID] | 税金レポートの目的で、一部の管轄区域によって会社に割り当てられた [ 付加価値税 ](../stores-purchase/vat.md) 番号。 ストアフロントに表示される顧客の VAT/TAX ID を設定するには、[ 新しいアカウントオプションの作成 ](../configuration-reference/customers/customer-configuration.md) を参照してください。<br/> **_注意：_** 会社管理者とその他の会社ユーザーは、顧客アカウントに個別の VAT/TAX ID 番号を持っていません。 |
| [!UICONTROL Reseller ID] | 税金レポート目的で会社に割り当てられる転売番号。 |
| [!UICONTROL Comment] | （管理者のみ）会社アカウントに関するこれらのメモは参照用で、管理者にのみ表示されます。 |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| フィールド | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | 会社の ID 番号。 |
| [!UICONTROL Company Name] | 会社の正式名称。 <br/> 編集中の会社行に `current company indicator` が表示されます。 |
| [!UICONTROL Company Email] | 会社アカウントに関連付けられているメールアドレス。 |
| [!UICONTROL Phone Number] | 会社の主要電話番号。 |
| [!UICONTROL Country] | 会社がビジネスを行うための登録が行われている国。 |
| [!UICONTROL State/Province] | 会社が事業を行うために登録されている州または都道府県。 |
| [!UICONTROL City] | 会社が営業を行うための登録が行われている市区町村。 |
| [!UICONTROL Group/Shared Catalog] | （管理者のみ）会社に割り当てられている [ 顧客グループ ](../customers/customer-groups.md) または [ 共有カタログ ](catalog-shared.md) を示します。 |
| [!UICONTROL Company Admin] | 会社の管理者の氏名。 |
| [!UICONTROL Action] | その会社ラインで可能なアクションのリスト。 |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| フィールド | 説明 |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | 会社が事業を行うために登録されている住所。 |
| [!UICONTROL City] | 会社が営業を行うための登録が行われている市区町村。 |
| [!UICONTROL Country] | 会社がビジネスを行うための登録が行われている国。 |
| [!UICONTROL State/Province] | 会社が事業を行うために登録されている州または都道府県。 |
| [!UICONTROL ZIP/Postal Code] | 会社が営業を登録する郵便番号。 |
| [!UICONTROL Phone Number] | 会社の主要電話番号。 |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| フィールド | 説明 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | 会社管理者が属する web サイトを決定します。 |
| [!UICONTROL Job Title] | 会社アカウントを管理する会社管理者の役職。 |
| [!UICONTROL Work Phone Number] | 会社アカウントを管理する会社管理者の電話番号。 |
| [!UICONTROL Email] | 会社の管理者のメールアドレスは、会社のメールアドレスと同じにすることができます。 別のメールアドレスを入力した場合は、会社アカウントに加えて、会社管理者用に個別のアカウントが作成されます。 |
| [!UICONTROL Prefix] | 該当する場合、会社管理者の名前に関連付けられたプレフィックス （`Mr.`、`Ms.`、`Mrs.`、`Dr.` など）。 設定に応じて、入力フィールドはテキストフィールドまたはリストになります。 |
| [!UICONTROL First Name] | 会社の管理者の名。 |
| [!UICONTROL Middle Name/Initial] | 会社の管理者のミドルネームまたはイニシャル。 |
| [!UICONTROL Last Name] | 会社の管理者の姓。 |
| [!UICONTROL Suffix] | 該当する場合、会社の管理者の名前に関連付けられたサフィックス （`Jr.`、`Sr.`、`III.` など）。 設定に応じて、入力フィールドはテキストフィールドまたはリストになります。 |
| [!UICONTROL Gender] | 会社の管理者の性別。 オプション：`Male`/`Female`/`Not Specified` |
| [!UICONTROL Send Welcome Email From] | お知らせメールの送信元のストア表示です。 |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| フィールド | 説明 |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | （管理者のみ）企業クレジットでの購入に対してストアが受け入れる通貨。 |
| [!UICONTROL Credit Limit] | （管理者のみ）会社アカウントに拡張されるクレジット制限。 |
| [!UICONTROL Allow to Exceed Credit Limit] | （管理者のみ）会社がクレジット制限を超える権限を持っているかどうかを示します。 オプション：`Yes` / `No` |
| [!UICONTROL Reason for Change] | （管理者のみ）会社がクレジット制限を超えることを許可または禁止する理由を説明するメモ。 このフィールドは、与信限度額を超える権限が変更された場合にのみ有効になります。 |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| フィールド | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | （管理者のみ）会社に割り当てられている [ 顧客グループ ](../customers/customer-groups.md) または [ 共有カタログ ](catalog-shared.md) を示します。 |
| [!UICONTROL Allow Quotes] | （管理者のみ）会社のメンバーが、会社の代わりに交渉可能な見積もりを準備して送信できるかどうかを決定します。 |
| [!UICONTROL Enable Purchase Orders] | （管理者のみ）会社のメンバーが、会社の代わりに [ 発注書 ](account-dashboard-my-purchase-orders.md) として注文を送信できるかどうかを決定します。 |
| 適用可能な支払い方法 | （管理者のみ）会社の購入に使用できる支払い方法を示します。 オプション：`B2B Payment Methods`/`All Enabled Payment Methods`/`Selected Payment Methods` |
| [!UICONTROL Payment Methods] | （管理者のみ）特定の支払方法が有効化されると有効化されます。 会社のアカウントで複数の支払い方法を使用できるようにするには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各オプションを選択します。 |
| [!UICONTROL Applicable Shipping Methods] | （管理者のみ）会社の購入に使用できる発送方法を示します。 オプション：`B2B Shipping Methods`/`All Enabled Shipping Methods`/`Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | （管理者のみ）特定の発送方法がアクティブ化されると、アクティブになります。 会社のアカウントで複数の支払い方法を使用できるようにするには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各オプションを選択します。 |

{style="table-layout:auto"}
