---
title: 会社ユーザーアカウントの管理
description: 会社ユーザーアカウントと、関連する会社アカウント内でそれらがどう機能するかについて説明します。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# 会社ユーザーアカウントの管理

ストアフロントでは、会社ユーザーは会社の管理者によって割り当てられ、_[!UICONTROL Company Users]_&#x200B;ページに表示されます。 これらの個人は、通常、ストアのサービスやリソースにアクセスする権限のレベルが異なる買い手です。

会社の管理者は、まず [ 会社の構造 ](account-company-structure.md) を設定し、必要に応じて次のタスクを実行します。

- 会社ユーザーの作成とチームへのユーザーの割り当て

- 役割と権限を定義し、ユーザーを役割に割り当てます。

会社ユーザーは、会社管理者のみが追加、編集、非アクティブ化または削除できます。

- ユーザーが削除されると、アカウントのステータスが *非アクティブ* に変わり、顧客は会社にログインできなくなります。 管理者は、引き続きユーザーに関連付けられたすべてのコンテンツにアクセスできます。 アカウント管理者は、[!UICONTROL Company Users] のページからアカウントのステータスを *[!UICONTROL Active]* に変更することで、アクセスを復元できます。

- ユーザーアカウントを削除すると、アカウントおよび関連するコンテンツがストアフロントから削除されます。 このアクションは元に戻すことができません。

## 会社ユーザーを追加

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、「**[!UICONTROL Company Users]**」を選択します。

   ![ 会社ユーザー ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. **[!UICONTROL Add New User]** をクリックして、次の操作を実行します。

   - 新しいユーザーの **[!UICONTROL Job Title]** を入力します。

   - 役割と権限が定義されている場合は、適切な **[!UICONTROL User Role]** を選択します。 そうしないと、後で戻って役割を割り当てることができます。

     ![ 新しいユーザーを追加 ](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - 残りのフィールドにユーザー情報を追加します。
      - **[!UICONTROL First Name]** と **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   デフォルトでは、アカウントの **[!UICONTROL Status]** は `Active` です。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. 必要な数の会社ユーザーを作成するプロセスを繰り返します。

   新しいユーザーが、会社管理者と共に会社ユーザーリストに表示されます。

初回注文時の時間を節約するために、会社の管理者は、各会社のユーザーに、デフォルトの会社の請求と配送先住所を [ アドレス帳 ](../customers/account-dashboard-address-book.md) に追加するようリマインダーできます。

## [!UICONTROL Company structure] からのユーザーの削除

会社管理者は、[!UICONTROL Company Structure] ーザーからユーザーを削除できます。

アカウントを削除すると、ユーザーアカウントのステータスが *非アクティブ* に変わり、ユーザーはストアフロントにログインできなくなります。
管理者は、会社ユーザーページからユーザーアカウント情報を編集して、アカウントを再アクティブ化できます。

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、「**[!UICONTROL Company Structure]**」を選択します。

1. 会社構造内の会社ユーザーを選択します。

1. **[!UICONTROL Remove from Structure]** をクリックします。

   ![ ユーザーの削除 ](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Remove]**」をクリックします。

   管理者では、会社ユーザーは [ 顧客 ](../customers/customers-all.md) グリッドに引き続き表示されますが、ステータスは `Inactive` です。

## 会社ユーザーアカウントの表示と管理

会社管理者は、[!UICONTROL Company Users] のページのフィルターの表示を使用して、会社のユーザーアカウントを表示および管理できます。

![ 会社ユーザー ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- **[!UICONTROL Show Inactive Users]** を選択して、非アクティブなユーザーのみを表示します。
- **[!UICONTROL Show Active Users]** を選択して、アクティブなユーザーのみを表示します。
- **[!UICONTROL Show All Users]** を選択して、すべてのユーザーを表示します。

会社管理者は、行項目 *[!UICONTROL Actions]* を使用して個々のアカウントを管理し、アカウント情報の編集、アカウントのステータスの管理、アカウントの削除を行うことができます。

### 会社ユーザーアカウント情報の編集

会社管理者は、ユーザーアカウントプロファイル情報を更新し、アカウントステータスを変更できます。

1. [!UICONTROL Company Users] ページで、更新するユーザーアカウントを見つけます。 「**[!UICONTROL Edit]**」をクリックします。

1. アカウントのステータスの変更など、ユーザーアカウント情報に対して必要な変更を行います。

1. 「」をクリックして変更を適用 **[!UICONTROL Save]** ます。

>[!NOTE]
>
>会社のユーザーアカウントを編集した際に、プロファイルに役職や勤務先電話番号などの必須のアカウント情報が欠落していることがわかった場合は、そのアカウントがCommerce サイト管理者によって追加されたことを示します。 これらのアカウントは、ストアフロントから編集できません。 情報を更新したり、アカウントの状態を変更したりするには、サイト管理者に問い合わせてください。

### アクティブなアカウントの非アクティブ化または削除

1. [!UICONTROL Company Users] ページで、更新するユーザーアカウントを見つけます。 「**[!UICONTROL Manage]**」をクリックします。

   ![ 会社ユーザーページからのユーザーの管理 ](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. プロンプトが表示されたら、必要に応じてユーザーアカウントを無効にするか削除します。

>[!IMPORTANT]
>
>会社ユーザーアカウントを削除すると、アカウントと関連するすべてのコンテンツがシステムから削除されます。 このアクションは元に戻すことができません。

## 会社ユーザーアカウントのプロファイルフィールドの説明

| フィールド | 説明 |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | 会社ユーザーの役職。 |
| [!UICONTROL User Role] | 会社ユーザーに割り当てられた [ 役割 ](account-company-roles-permissions.md)。 オプション：`Default User` / （その他の役割） |
| [!UICONTROL First Name] | 会社ユーザーの名。 |
| [!UICONTROL Last Name] | 会社ユーザーの姓。 |
| [!UICONTROL Email] | 会社ユーザーの電子メールアドレス。 |
| [!UICONTROL Work Phone Number] | 会社ユーザーの仕事用電話番号。 |
| [!UICONTROL Status] | 会社ユーザーアカウントのステータス。 オプション：`Active` / `Inactive` |

{style="table-layout:auto"}
