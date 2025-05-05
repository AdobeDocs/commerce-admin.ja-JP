---
title: 会社管理者の割り当て
description: 会社ユーザーアカウントを、会社アカウントに指定された会社管理者として割り当てる方法について説明します。
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# 会社管理者の割り当て

会社の管理者は、会社アカウントを最初に作成したときに最初に割り当てられ、管理者からのストア管理者のみが変更できます。

- 各会社に割り当てることができる管理者は 1 人だけです。
- 会社ユーザーは、1 つの会社の管理者になることができます。
- 割り当てられた会社管理者に対する変更は、管理者のストア管理者が行う必要があります。

## 割り当てられた会社管理者の変更

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

   ![ 会社 ](./assets/companies-grid.png){width="700" zoomable="yes"}

1. リストで会社を見つけて、[**[!UICONTROL Edit]**] をクリックします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Company Admin]**」セクションを展開します。

   ![ 会社管理者 ](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 新しい会社管理者の **[!UICONTROL Job Title]** を入力します。

   このアクションを実行すると、フォームがクリアされ、必須 _[!UICONTROL First Name]_&#x200B;および&#x200B;_[!UICONTROL Last Name]_ フィールドがハイライト表示されます。

1. 新しい会社管理者の **[!UICONTROL Email]** アドレスを入力します。

   システムがデータベース内でメールアドレスを見つけられない場合は、会社管理者を置き換えるかどうかを確認するプロンプトが表示されます。

   - 新しい会社管理者のユーザーアカウントが存在しない場合、`Company Admin` タイプのアカウントが作成されます。

   - ユーザーアカウントがシステムに存在する場合は、会社構造内の会社管理者の位置に移動されます。

1. **[!UICONTROL First Name]** と **[!UICONTROL Last Name]**、および新しい会社管理者に適用されるその他の情報を入力します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   元の会社管理者の個人アカウントは、デフォルトのユーザーロールに割り当てられたアクティブなユーザーアカウントとしてシステムに残ります。 これがユーザーアカウントに関連付けられている唯一の会社である場合、アカウントの種類は *[!UICONTROL Company user]* から *[!UICONTROL Individual user]* に変わります。

   システムは、新規管理者と元会社管理者に変更のメール通知を送信します。

