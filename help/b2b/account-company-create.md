---
title: 会社アカウントの作成
description: Adobe Commerce Admin とストアフロントでの会社アカウントの作成について説明します。
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 0%

---

# 会社アカウントの作成

会社のアカウントは、顧客がストアフロントから、または管理者から設定できます。 会社アカウントを作成するためのすべてのリクエストは、アカウントがアクティブになる前にストア管理者の承認を受ける必要があります。

ストアフロントから会社アカウントを設定するユーザーに、 [会社管理者](account-company-admin.md). 会社アカウントの作成リクエストが承認されると、会社の管理者はアカウントのパスワードを設定し、アカウントにログインできます。

## 方法 1：顧客がストアフロントからアカウントを作成する

>[!IMPORTANT]
>
>この方法をサポートするには（顧客がストアフロントから会社を登録できるようにする）、 [B2B 機能](enable-basic-features.md) が **[!UICONTROL Allow Company Registration from the Storefront]** が `Yes`.

1. ストアフロントヘッダーの右上隅で、ユーザーが **[!UICONTROL Create an Account]** および選択 **[!UICONTROL Create New Company Account]**.

   ![新しい会社アカウントの作成](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >訪問者が登録済みユーザーアカウントにログインしている場合は、次の場所に移動して会社アカウントを作成できます。 _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**. 会社アカウントの作成時に、顧客のアカウントが主要連絡先として割り当てられます。 それ以外の場合は、パスワードを設定する電子メールを受け取る顧客が作成されます。

1. Adobe Analytics の _[!UICONTROL Company Information]_セクションでは、お客様は次の操作を行います。

   - 次の必須フィールドに入力します。

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - 該当する場合は、残りのフィールドに入力します。

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![会社情報](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. の必須フィールドを完了します。 _[!UICONTROL Legal Address]_」セクションに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![法的住所](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Company Administrator]_セクションでは、次の操作を実行します。

   - 次に入る **[!UICONTROL Email address]** （会社管理者向け）。

     会社管理者の電子メールアドレスは、会社の電子メールアドレスまたは別の電子メールアドレスと同じでもかまいません。 別の電子メールアドレスを入力すると、会社の管理者アカウントに加えて、会社のユーザーアカウントが作成されます。

   - 次に入る **[!UICONTROL First Name]** および **[!UICONTROL Last Name]** 会社管理者の

   - 必要に応じて、次のフィールドに入力します。

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![会社管理者](./assets/company-administrator-account-storefront.png)

1. このストアフロント関数で reCAPTCHA が有効になっている場合、検証を完了します。

1. 情報が完了したら、 **[!UICONTROL Submit]**.

   会社アカウントの作成リクエストがマーチャントによって承認されると、会社管理者に電子メール通知が送信されます。

   ![お知らせメールの例](./assets/company-admin-welcome-email.png){width="500"}

   パスワードを設定すると、会社の管理者は [サインイン](../customers/customer-sign-in.md) をアカウントに追加します。

## 方法 2：マーチャントが管理者からアカウントを作成します

管理者から会社を作成するプロセスは、基本的にストアフロントからのプロセスと同じですが、追加のフィールドがあります。

![管理者からの新しい会社の追加](./assets/company-add-new.png){width="700" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. クリック **[!UICONTROL Add New Company]** 次の操作を実行します。

   - 次の必須フィールドに入力します。

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - アカウントが有効になる準備ができていない場合は、 **[!UICONTROL Status]** から `Pending Approval`. （に設定） `Active` （デフォルト）。

   - 該当する場合は、 **[!UICONTROL Sales Representative]** アカウントを管理するユーザー。

1. Adobe Analytics の _[!UICONTROL Account Information]_セクションで、以下の操作を実行します。

   - 該当する場合は、次のフィールドに入力します。

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - の場合 **[!UICONTROL Comment]**」に、必要になる可能性のある顧客に関する追加情報を入力します。

     コメントは管理者からのみ表示されます。

   ![アカウント情報](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. 最初の会社の作成時に、 _[!UICONTROL Company Hierarchy]_グリッドを展開すると、グリッドは空になります。 会社を保存した後、会社階層に含めることができます。 詳しくは、 [会社管理](manage-companies.md).

1. Adobe Analytics の _[!UICONTROL Legal Address]_セクションで、次の必須フィールドに入力します。

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. Adobe Analytics の _[!UICONTROL Company Admin]_セクションで、以下の操作を実行します。

   - 次の必須フィールドに入力します。

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - 名前の次のオプション部分を入力します。これは、他より多くの顧客名に適用でき、自由に使用できます。

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - 情報が使用可能な場合は、残りのフィールドに会社の管理者を説明します。

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![会社管理者](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Company Credit]_「 」セクション：顧客のクレジット活動の概要を表示し、該当する数のフィールドを「 」セクションの下部に入力します。

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![会社クレジット](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Adobe Analytics の _[!UICONTROL Advanced Settings]_セクションで、以下の操作を実行します。

   >[!NOTE]
   >
   >顧客グループの割り当てによって、会社とその従業員が使用できる共有カタログが決まります。 デフォルトでは、会社は設定のデフォルトとして設定された顧客グループに割り当てられます。

   - 次の項目を変更できます。 **[!UICONTROL Customer Group]** 別の共有カタログまたは標準顧客グループにアクセスできるグループに対する会社とその従業員の割り当て。 グループを変更する前に確認するメッセージが表示されます。

     ![顧客グループの変更](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - 会社の従業員が自分のアカウントから見積もりを生成することを許可する場合は、 **[!UICONTROL Allow Quotes]** から `Yes`.

   - 会社の従業員が自分のアカウントから発注書を作成して使用することを許可する場合は、 **[!UICONTROL Enable Purchase Orders]** から `Yes`.

   - 次の手順で **[!UICONTROL Applicable Payment Methods]** 会社が使用できる場合は、 **[!UICONTROL Use config settings]** チェックボックスをオンにして、次のいずれかを選択します。

     | オプション | 説明 |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | （デフォルト）すべてを有効にします。 [デフォルトとして設定された支払い方法](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) B2B 注文の場合。 |
     | `All Enabled Payment Methods` | すべてを作成 [有効な支払い方法](../configuration-reference/sales/payment-methods.md) 会社アカウントに関連付けられた顧客アカウントに対して使用できます。 |
     | `Selected Payment Methods` | 会社アカウントに関連付けられた顧客アカウントで使用できる支払い方法を選択できます。 複数の支払い方法を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションを選択します。 |

     {style="table-layout:auto"}

   - 次の手順で **[!UICONTROL Applicable Shipping Methods]** 会社が使用できる場合は、 **[!UICONTROL Use config settings]** チェックボックスをオンにして、次のいずれかを選択します。

     | オプション | 説明 |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | （デフォルト）すべてを有効にします。 [出荷方法がデフォルトに設定されました](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) B2B 注文の場合。 |
     | `All Enabled Shipping Methods` | すべてを作成 [有効な発送方法](../configuration-reference/sales/delivery-methods.md) 会社アカウントに関連付けられた顧客アカウントに対して使用できます。 |
     | `Selected Shipping Methods` | 会社アカウントに関連付けられている顧客アカウントで使用できる発送方法を選択できます。 複数の発送方法を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションを選択します。 |

     {style="table-layout:auto"}

1. 完了したら、「 」を選択します。 **[!UICONTROL Save]**.

   会社アカウントの作成リクエストがマーチャントによって承認されると、会社管理者の電子メールアドレスに電子メール通知が送信されます。

   パスワードを設定すると、会社の管理者は [サインイン](../customers/customer-sign-in.md) をアカウントに追加します。

## ボタンバー

| ボタン | 説明 |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | 変更を保存せずに会社ページに戻ります。 |
| [!UICONTROL Reset] | 未保存の変更を含むフィールドに元の値を復元します。 |
| [!UICONTROL Save] | 会社に対する変更を保存し、プロファイルを開いたままにします。 |
| [!UICONTROL Save & Close] | 会社に対する変更を保存し、プロファイルを閉じます。 |

{style="table-layout:auto"}

## フィールドの説明

| フィールド | 説明 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | 会社名は、会社アカウントが最初に作成される際に入力されます。また、完全な正式名称の短縮版を使用できます。 |
| [!UICONTROL Status] | （管理者のみ）会社アカウントの現在の状態を示します。 オプション： <br/>**[!UICONTROL Active]**— 会社アカウントはストア管理者によって承認されています。 会社の管理者や関連メンバーは、ストアフロントからアカウントにログインして、購入をおこなうことができます。<br/>**[!UICONTROL Pending Approval]**  — 会社アカウントを開くためのリクエストが送信されましたが、ストア管理者によってまだ承認されていません。 <br/>**[!UICONTROL Rejected]**— 会社アカウントを開くためのリクエストが送信されましたが、ストア管理者によって承認されていません。 リクエストの送信に使用された初期ログイン資格情報はブロックされます。<br/>**&#x200B;ブロック&#x200B;**：会社のメンバーはカタログにログインしてアクセスできますが、購入することはできません。 ストア管理者は、状況が悪い会社アカウントをブロックする場合があります。 アカウントのブロックは、ストア管理者がいつでも削除できます。 |
| [!UICONTROL Company Email] | 会社アカウントに関連付けられている電子メールアドレス。 |
| [!UICONTROL Sales Representative] | （管理者のみ）会社アカウントの主要連絡先である管理者ユーザー。 |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| フィールド | 説明 |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | 会社の正式名称。 |
| [!UICONTROL VAT / TAX ID] | The [付加価値税](../stores-purchase/vat.md) 税レポートの目的で、一部の管轄区域によって会社に割り当てられた番号。 顧客の VAT/TAX ID をストアフロントに表示するように設定するには、 [新しいアカウントオプションの作成](../configuration-reference/customers/customer-configuration.md). <br/> **_注意：_** 会社管理者や他の会社のユーザーは、顧客アカウントに独自の VAT/TAX ID 番号を持っていません。 |
| [!UICONTROL Reseller ID] | 税レポートの目的で会社に割り当てられる再販売番号。 |
| [!UICONTROL Comment] | （管理者のみ）会社アカウントに関するこれらのメモは参照用で、管理者からのみ表示されます。 |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| フィールド | 説明 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | 会社の ID 番号。 |
| [!UICONTROL Company Name] | 会社のフルネーム。 <br/>A `current company indicator` 編集中の会社行に表示されます。 |
| [!UICONTROL Company Email] | 会社アカウントに関連付けられている電子メールアドレス。 |
| [!UICONTROL Phone Number] | 会社の主な電話番号。 |
| [!UICONTROL Country] | 会社が事業を行う登録を受けている国。 |
| [!UICONTROL State/Province] | 会社が事業を行うために登録されている州または都道府県。 |
| [!UICONTROL City] | 会社が事業を営むために登録されている都市。 |
| [!UICONTROL Group/Shared Catalog] | （管理者のみ） [顧客グループ](../customers/customer-groups.md) または [共有カタログ](catalog-shared.md) それは会社に割り当てられています。 |
| [!UICONTROL Company Admin] | 会社管理者のフルネーム。 |
| [!UICONTROL Action] | その会社行で使用可能なアクションのリスト。 |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| フィールド | 説明 |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | 会社が事業を行うために登録されている住所。 |
| [!UICONTROL City] | 会社が事業を営むために登録されている都市。 |
| [!UICONTROL Country] | 会社が事業を行う登録を受けている国。 |
| [!UICONTROL State/Province] | 会社が事業を行うために登録されている州または都道府県。 |
| [!UICONTROL ZIP/Postal Code] | 会社が事業を行うために登録されている郵便番号。 |
| [!UICONTROL Phone Number] | 会社の主な電話番号。 |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| フィールド | 説明 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | 会社の管理者が属する Web サイトを決定します。 |
| [!UICONTROL Job Title] | 会社アカウントを管理する会社管理者の役職。 |
| [!UICONTROL Email] | 会社の管理者の電子メールアドレスは、会社の電子メールアドレスと同じにすることができます。 別の電子メールアドレスを入力すると、会社アカウントに加えて、会社管理者用に個別の個別アカウントが作成されます。 |
| [!UICONTROL Prefix] | 該当する場合、会社管理者の名前に関連付けられたプレフィックス ( 例： `Mr.`, `Ms.`, `Mrs.`または `Dr.`) をクリックします。 設定に応じて、入力フィールドはテキストフィールドまたはリストになります。 |
| [!UICONTROL First Name] | 会社管理者の名。 |
| [!UICONTROL Middle Name/Initial] | 会社管理者のミドルネームまたはイニシャル。 |
| [!UICONTROL Last Name] | 会社管理者の姓。 |
| [!UICONTROL Suffix] | 該当する場合は、会社管理者の名前に関連付けられたサフィックス ( 例： `Jr.`, `Sr.`または `III.`) をクリックします。 設定に応じて、入力フィールドはテキストフィールドまたはリストになります。 |
| [!UICONTROL Gender] | 会社管理者の性別。 オプション： `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | お知らせメールの送信元となるストア表示です。 |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| フィールド | 説明 |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | （管理者のみ）ストアが会社のクレジットでの購入に対して受け入れる通貨。 |
| [!UICONTROL Credit Limit] | （管理者のみ）会社アカウントに拡張されるクレジット制限。 |
| [!UICONTROL Allow to Exceed Credit Limit] | （管理者のみ）会社がクレジット制限を超える権限を持っているかどうかを示します。 オプション： `Yes` / `No` |
| [!UICONTROL Reason for Change] | （管理者のみ）会社がクレジット制限を超えることを許可または禁止する理由を説明する注記。 このフィールドは、クレジット制限を超える権限が変更された場合にのみ有効です。 |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| フィールド | 説明 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | （管理者のみ） [顧客グループ](../customers/customer-groups.md) または [共有カタログ](catalog-shared.md) それは会社に割り当てられています。 |
| [!UICONTROL Allow Quotes] | （管理者のみ）会社メンバーが会社に代わって有価証券を作成し、提出できるかどうかを決定します。 |
| [!UICONTROL Enable Purchase Orders] | （管理者のみ）会社メンバーが注文を次の形式で送信できるかどうかを決定します。 [発注書](account-dashboard-my-purchase-orders.md) 会社を代表して。 |
| 適用可能な支払い方法 | （管理者のみ）会社の購入に使用できる支払い方法を示します。 オプション： `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | （管理者のみ）特定の支払い方法が有効化されると、有効になります。 会社のアカウントで複数の支払い方法を使用できるようにするには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションを選択します。 |
| [!UICONTROL Applicable Shipping Methods] | （管理者のみ）会社の購入に使用できる発送方法を示します。 オプション： `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | （管理者のみ）特定の発送方法が有効化されると、有効になります。 会社のアカウントで複数の支払い方法を使用できるようにするには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションを選択します。 |

{style="table-layout:auto"}
