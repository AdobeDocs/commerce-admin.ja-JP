---
title: 会社管理者の割り当て
description: 会社アカウントの指定会社管理者として会社ユーザーアカウントを割り当てる方法を説明します。
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 0%

---

# 会社管理者の割り当て

会社の管理者は、会社アカウントが最初に作成されたときに最初に割り当てられ、管理者のストア管理者のみが変更できます。

- 各会社に割り当てられた管理者は1人だけです。
- 会社ユーザーは、1つの会社の管理者にすることができます。
- 割り当てられた会社の管理者への変更は、管理者からストア管理者が完了する必要があります。

## 割り当てられた会社の管理者を変更

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Companies]**&#x200B;に移動します。

   ![企業](./assets/companies-grid.png){width="700" zoomable="yes"}

1. リスト内の会社を検索し、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Company Admin]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![会社管理者](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 新しい会社の管理者の&#x200B;**[!UICONTROL Job Title]**&#x200B;を入力します。

   このアクションにより、フォームがクリアされ、必須フィールド _[!UICONTROL First Name]_&#x200B;と_[!UICONTROL Last Name]_ フィールドが強調表示されます。

1. 新しい会社管理者の&#x200B;**[!UICONTROL Email]** アドレスを入力してください。

   データベースにメールアドレスが見つからない場合は、会社の管理者を置き換えるかどうかを確認するメッセージが表示されます。

   - 新しい会社管理者のユーザーアカウントが存在しない場合、システムは`Company Admin` タイプのアカウントを作成します。

   - ユーザーアカウントがシステム内に存在する場合は、会社構造の会社管理者の位置に移動します。

1. **[!UICONTROL First Name]**&#x200B;と&#x200B;**[!UICONTROL Last Name]**&#x200B;を入力し、新しい会社管理者に該当するその他の情報を入力します。

1. 完了したら、**[!UICONTROL Save]**&#x200B;をクリックします。

   以前の会社管理者の個々のアカウントは、デフォルトのユーザー役割に割り当てられたアクティブユーザーアカウントとしてシステム内に残ります。 この会社がユーザーアカウントに関連付けられている唯一の会社である場合、アカウントの種類は&#x200B;*[!UICONTROL Company user]*&#x200B;から&#x200B;*[!UICONTROL Individual user]*&#x200B;に変更されます。

   システムは、変更の通知を新しい会社と以前の会社の管理者に電子メールで送信します。

