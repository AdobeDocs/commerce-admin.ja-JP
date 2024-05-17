---
title: 会社アカウントを承認
description: 管理者で会社アカウントのリクエストを承認する方法を説明します。
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 会社アカウントを承認

ストアフロントから受け取った会社設立依頼のステータスは以下のとおりです `Pending Approval` ストア管理者がリクエストを確認し、承認または却下するまで。 会社アカウントのステータスは、次のいずれかに設定される場合があります。

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

を使用することもできます [アクション制御](account-company-manage.md) 複数の会社リクエストを承認する場合。

![承認待ち](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 保留中の会社アカウントを承認

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   を使用できます _[!UICONTROL Columns]_グリッドの上にセレクターを配置して、**[!UICONTROL Status]**列。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Edit]**.

1. を設定 **[!UICONTROL Company Status]** 対象： `Active`.

   ![会社ステータスの設定](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 確認を求められたら、 **[!UICONTROL Change status]**.

   会社の管理者に、会社がアクティブになったというメール通知が届きます。

1. 該当する場合、を設定します **[!UICONTROL Sales Representative]** を特定の管理者ユーザーアカウントに対して実行します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png)  この **[!UICONTROL Account Information]** セクションと使用 **[!UICONTROL Comment]** アカウントに関するメモを入力するフィールド。

   コメントはストアフロントからは表示されません。

1. 完了したら、 **[!UICONTROL Save]**.

   会社アカウントが承認されたことを示す確認メールが会社と会社の管理者に送信されます。

## 会社ステータス

| ステータス | 説明 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 会社は承認され、会社管理者がストアフロントから管理できます。 |
| [!UICONTROL Pending Approval] | 会社アカウントを作成するリクエストがストアフロントから送信されましたが、まだレビューされていません。 |
| [!UICONTROL Rejected] | 会社アカウントを作成するリクエストは、ストア管理者によって拒否されました。 |
| [!UICONTROL Blocked] | 会社の帳簿は調わなくなった。 顧客はストアフロントからアカウントにアクセスできますが、購入することはできません。 |

{style="table-layout:auto"}
