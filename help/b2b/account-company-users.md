---
title: 会社ユーザーアカウントの管理
description: 会社ユーザーアカウントと、関連する会社アカウント内でそれらがどう機能するかについて説明します。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 会社ユーザーアカウントの管理

会社ユーザーは会社の管理者によって割り当てられ、顧客タイプ _[!UICONTROL Company User]_によって、_[!UICONTROL Customers]_ グリッドの管理者から表示されます。 これらの個人は、通常、ストアのサービスやリソースにアクセスする権限のレベルが異なる買い手です。

会社の管理者は、まず [ 会社の構造 ](account-company-structure.md) を設定し、必要に応じて次のタスクを実行します。

- 会社ユーザーの作成とチームへのユーザーの割り当て

- 役割と権限を定義し、ユーザーを役割に割り当てます。

>[!IMPORTANT]
>
>会社ユーザーの追加、編集、削除は、会社管理者のみが行うことができます。 ユーザーが会社構造から削除されているため、削除を元に戻すことはできません。

## 会社ユーザーを追加

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、「**[!UICONTROL Company Users]**」を選択します。

   ![ 会社ユーザー ](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. **[!UICONTROL Add New User]** をクリックして、次の操作を実行します。

   - 新しいユーザーの **[!UICONTROL Job Title]** を入力します。

   - 役割と権限が定義されている場合は、適切な **[!UICONTROL User Role]** を選択します。 そうしないと、後で戻って役割を割り当てることができます。

     ![ 新しいユーザーを追加 ](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - ユーザーの必要に応じて、残りのフィールドに入力します。

      - **[!UICONTROL First Name]** と **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   デフォルトでは、アカウントの **[!UICONTROL Status]** は `Active` です。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

1. 必要な数の会社ユーザーを作成するプロセスを繰り返します。

   新しいユーザーが、会社管理者と共に会社ユーザーリストに表示されます。

初回注文時の時間を節約するために、会社の管理者は、各会社のユーザーに、デフォルトの会社の請求と配送先住所を [ アドレス帳 ](../customers/account-dashboard-address-book.md) に追加するようリマインダーできます。

## 会社ユーザーの編集

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、「**[!UICONTROL Company Users]**」を選択します。

1. 更新するユーザーレコードを検索し、**[!UICONTROL Edit]** をクリックします。

1. 必要な変更を行います。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

## 会社ユーザーの削除

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、「**[!UICONTROL Company Structure]**」を選択します。

1. 会社構造内の会社ユーザーを選択します。

1. **[!UICONTROL Delete Selected]** をクリックします。

   ![ ユーザーの削除 ](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Delete]**」をクリックします。

管理者では、会社ユーザーは [ 顧客 ](../customers/customers-all.md) グリッドに引き続き表示されますが、ステータスは `Inactive` です。

## フィールドの説明

| フィールド | 説明 |
|--------------|---------------|
| [!UICONTROL Job Title] | 会社ユーザーの役職。 |
| [!UICONTROL User Role] | 会社ユーザーに割り当てられた [ 役割 ](account-company-roles-permissions.md)。 オプション：`Default User` / （その他の役割） |
| [!UICONTROL First Name] | 会社ユーザーの名。 |
| [!UICONTROL Last Name] | 会社ユーザーの姓。 |
| [!UICONTROL Email] | 会社ユーザーの電子メールアドレス。 |
| [!UICONTROL Phone Number] | 会社ユーザーの電話番号。 |
| [!UICONTROL Status] | 会社ユーザーアカウントのステータス。 オプション：`Active` / `Inactive` |

{style="table-layout:auto"}
