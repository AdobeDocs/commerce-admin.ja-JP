---
title: 会社のユーザーアカウントを管理
description: 会社のユーザーアカウントと、関連する会社アカウント内でのユーザーアカウントの機能について説明します。
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 会社のユーザーアカウントを管理

会社ユーザーは会社管理者によって割り当てられ、 _[!UICONTROL Customers]_顧客タイプ別のグリッド_[!UICONTROL Company User]_. これらの個人は、通常、ストアのサービスやリソースにアクセスするための様々なレベルの権限を持つ購入者です。

会社の管理者が最初に [会社構造](account-company-structure.md)をクリックし、必要に応じて次のタスクを完了します。

- 会社ユーザーの作成とチームへのユーザーの割り当て

- 役割と権限を定義し、ユーザーを役割に割り当てます

>[!IMPORTANT]
>
>会社ユーザーの追加、編集または削除は、会社管理者のみがおこなうことができます。 ユーザーが会社構造から削除されたので、削除を元に戻すことができません。

## 会社ユーザーの追加

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、を選択します。 **[!UICONTROL Company Users]**.

   ![会社ユーザー](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. クリック数 **[!UICONTROL Add New User]** は次の操作を実行します。

   - 次に入る **[!UICONTROL Job Title]** 新しいユーザーの

   - 適切な **[!UICONTROL User Role]** （役割と権限が定義されている場合）。 それ以外の場合は、後でロールの割り当てに戻ることができます。

     ![新しいユーザーを追加](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - ユーザーの必要に応じて、残りのフィールドに入力します。

      - **[!UICONTROL First Name]** および **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   デフォルトでは、 **[!UICONTROL Status]** アカウントが `Active`.

1. 完了したら、「 」をクリックします **[!UICONTROL Save]**.

1. このプロセスを繰り返して、必要な数の会社ユーザーを作成します。

   新しいユーザーは、会社管理者と共に会社ユーザーリストに表示されます。

最初の注文時に時間を節約するために、会社管理者は各会社ユーザーに対し、デフォルトの会社の請求先住所と配送先住所をユーザーに追加するように促すことができます [アドレス帳](../customers/account-dashboard-address-book.md).

## 会社ユーザーを編集

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、を選択します。 **[!UICONTROL Company Users]**.

1. 更新するユーザーレコードを検索し、「 」をクリックします。 **[!UICONTROL Edit]**.

1. 必要な変更を行います。

1. 完了したら、「 」をクリックします **[!UICONTROL Save]**.

## 会社ユーザーの削除

1. ストアフロントから、会社の管理者が自分のアカウントにサインインします。

1. 左側のパネルで、を選択します。 **[!UICONTROL Company Structure]**.

1. 会社構造内の会社ユーザーを選択します。

1. クリック数 **[!UICONTROL Delete Selected]**.

   ![ユーザーを削除](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 確認を求められたら、「 」をクリックします **[!UICONTROL Delete]**.

管理者に会社のユーザーが表示されるまで、 [顧客](../customers/customers-all.md) グリッド ( ただし、 `Inactive` ステータス。

## フィールドの説明

| フィールド | 説明 |
|--------------|---------------|
| [!UICONTROL Job Title] | 会社ユーザーの役職。 |
| [!UICONTROL User Role] | The [役割](account-company-roles-permissions.md) 会社ユーザーに割り当てられました。 オプション： `Default User` / （その他の役割） |
| [!UICONTROL First Name] | 会社ユーザーの名。 |
| [!UICONTROL Last Name] | 会社ユーザーの姓。 |
| [!UICONTROL Email] | 会社ユーザーの電子メールアドレス。 |
| [!UICONTROL Phone Number] | 会社ユーザーの電話番号。 |
| [!UICONTROL Status] | 会社のユーザーアカウントのステータス。 オプション： `Active` / `Inactive` |

{style="table-layout:auto"}
