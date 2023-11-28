---
title: 会社アカウントを承認
description: 管理者で会社アカウントのリクエストを承認する方法について説明します。
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 会社アカウントを承認

ストアフロントから会社の作成に対して受け取った要求のステータスは次のとおりです `Pending Approval` 要求がストア管理者によってレビューされ、承認または拒否されるまで。 会社アカウントのステータスは、次のいずれかに設定できます。

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

また、 [アクションコントロール](account-company-manage.md) をクリックして、複数の会社リクエストを承認します。

![承認待ち](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 保留中の会社アカウントを承認

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   以下を使用すると、 _[!UICONTROL Columns]_グリッドの上のセレクターを使用して、**[!UICONTROL Status]**列。

1. Adobe Analytics の _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Edit]**.

1. 設定 **[!UICONTROL Company Status]** から `Active`.

   ![会社ステータスの設定](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 確認するメッセージが表示されたら、「 **[!UICONTROL Change status]**.

   会社の管理者に、会社がアクティブになったことを知らせる電子メール通知が届きます。

1. 該当する場合は、 **[!UICONTROL Sales Representative]** を特定の管理者ユーザーアカウントに追加します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png)  の **[!UICONTROL Account Information]** セクションの **[!UICONTROL Comment]** フィールドにアカウントに関するメモを入力します。

   コメントはストアフロントには表示されません。

1. 完了したら、「 **[!UICONTROL Save]**.

   会社および会社の管理者に、会社アカウントが承認されたことを確認する電子メールが送信されます。

## 会社ステータス

| ステータス | 説明 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 会社が承認され、会社管理者がストアフロントから管理できます。 |
| [!UICONTROL Pending Approval] | 会社アカウントの作成リクエストがストアフロントから送信されましたが、まだ確認されていません。 |
| [!UICONTROL Rejected] | 会社アカウントの作成リクエストがストア管理者によって拒否されました。 |
| [!UICONTROL Blocked] | 会社の口座はもはや良い状態ではない。 顧客はストアフロントからアカウントにアクセスできますが、購入はできません。 |

{style="table-layout:auto"}
