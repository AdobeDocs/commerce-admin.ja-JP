---
title: 会社管理者の割り当て
description: 会社ユーザーアカウントを、会社アカウントに指定された会社管理者として割り当てる方法について説明します。
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# 会社管理者の割り当て

会社の管理者は、会社アカウントを最初に作成したときに最初に割り当てられ、管理者からのストア管理者のみが変更できます。

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. リストで会社を見つけて、「**[!UICONTROL Edit]**」をクリックします。

   ![ 会社 ](./assets/companies-grid.png){width="700" zoomable="yes"}

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Company Admin]**」セクションを展開します。

   ![ 会社管理者 ](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 新しい会社の管理者の **[!UICONTROL Job Title]** を入力し、[**[!UICONTROL Proceed]**] をクリックして続行します。

   このアクションを実行すると、フォームがクリアされ、必須 _[!UICONTROL First Name]_および_[!UICONTROL Last Name]_ フィールドがハイライト表示されます。

1. 新しい会社管理者の **[!UICONTROL Email]** アドレスを入力します。

   システムがデータベース内でメールアドレスを見つけられない場合は、会社管理者を置き換えるかどうかを確認するプロンプトが表示されます。

   - 新しい会社管理者のユーザーアカウントが存在しない場合、`Company Admin` タイプのアカウントが作成されます。

   - ユーザーアカウントがシステムに存在する場合は、会社構造内の会社管理者の位置に移動されます。

1. **[!UICONTROL First Name]** と **[!UICONTROL Last Name]**、および新しい会社管理者に適用されるその他の情報を入力します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

   元の会社管理者の個人アカウントは、デフォルトのユーザーロールに割り当てられた、会社構造内のアクティブな個人ユーザーアカウントとしてシステムに残ります。

   システムは、新規管理者と元会社管理者に変更のメール通知を送信します。
