---
title: 会社アカウントを承認
description: 管理者で会社アカウントリクエストを承認する方法について説明します。
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 0%

---

# 会社アカウントを承認

会社を作成するためにストアフロントから受け取ったリクエストのステータスは、ストア管理者がリクエストを確認し、承認または拒否されるまで`Pending Approval`です。 会社アカウントのステータスは、次のいずれかに設定できます。

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

[ アクション コントロール ](account-company-manage.md)を使用して、複数の会社リクエストを承認することもできます。

![承認待ち](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 会社の保留中のアカウントを承認

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Companies]**&#x200B;に移動します。

   グリッドの上にある&#x200B;_[!UICONTROL Columns]_セレクターを使用して、**[!UICONTROL Status]**列を表示できます。

1. _[!UICONTROL Action]_列で、**[!UICONTROL Edit]**をクリックします。

1. **[!UICONTROL Company Status]**&#x200B;を`Active`に設定します。

   ![会社のステータスを設定](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 確認を求められたら、**[!UICONTROL Change status]**&#x200B;をクリックします。

   会社の管理者は、会社がアクティブになったというメール通知を受け取ります。

1. 該当する場合は、**[!UICONTROL Sales Representative]**&#x200B;を特定の管理者ユーザーアカウントに設定します。

1. **[!UICONTROL Account Information]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL Comment]** フィールドを使用してアカウントに関するメモを入力します。

   コメントはストアフロントからは表示されません。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   会社アカウントが承認されたことを確認するメールが、会社および会社の管理者に送信されます。

## 会社ステータス

| ステータス | 説明 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 会社は承認され、会社の管理者がストアフロントから管理できます。 |
| [!UICONTROL Pending Approval] | 会社アカウントの作成リクエストがストアフロントから送信されましたが、まだレビューされていません。 |
| [!UICONTROL Rejected] | 会社アカウントを作成するリクエストは、ストア管理者によって拒否されました。 |
| [!UICONTROL Blocked] | 会社のアカウントはもはや良い状態ではありません。 顧客はストアフロントからアカウントにアクセスできますが、購入はできません。 |

{style="table-layout:auto"}
