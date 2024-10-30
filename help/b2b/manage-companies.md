---
title: 会社管理
description: 複雑な運用モデルにより、B2B 組織の管理を合理化します。
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 会社管理

会社経営は、複雑な組織構造を持つ企業の業務を合理化します。 管理者ユーザーは、会社を指定された親会社に割り当てることにより、B2B 組織をミラーリングする会社階層を作成できます。 この割り当てを使用すると、親会社管理者は組織内の会社を表示および管理できます。

*[!UICONTROL Companies]* ビューから会社管理タスクを開始します。 管理者で、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

![B2B 会社グリッドの管理 ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Company Type]* の列は、会社が組織の一部として管理されているか、別の会社として管理されているかを示します。

- `Parent` は、1 つ以上の会社が割り当てられているビジネス組織です。 親会社を他の会社の子として割り当てることはできません。

- `Child` は、組織に割り当てられている会社です。 会社は、1 つの親会社にのみ割り当てることができます。

- `Company` は単一の会社を表します。 1 つの会社を組織の一部にするには、その会社を親会社にするか、既存の親会社に割り当てます。

親または子会社を編集する際に、*[!UICONTROL Company Hierarchy]* を展開すると、組織内のすべての会社が表示されます。 `Current` フラグは、編集中の会社を示します。

![B2B 会社階層グリッド ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## [!UICONTROL Company Hierarchy] の表示と設定

会社の初回作成時には、*[!UICONTROL Company Hierarchy]* グリッドは空です。 会社が 1 つの会社の場合も空です。

![B2B 会社階層グリッド ](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

会社が組織の親会社であり、組織内の他の会社の会社アカウントが既にAdobe Commerceに設定されている場合、適切な権限を持つ管理者ユーザーは、会社を割り当て、*[!UICONTROL Company Hierarchy]* Grid を使用して他の会社管理タスクを実行できます。

- 親会社に関連付けられているすべての会社を表示します。
- 親会社の詳細ページから、その組織に他の会社を割り当てます。
- *[!UICONTROL Unassign from parent]* アクションを使用して、組織から会社を削除します。
- *[!UICONTROL Advanced Settings]* 設定を更新して、同じ設定を複数の会社に適用します。

手順について詳しくは、「[ 会社階層の管理 ](manage-company-hierarchy.md)」を参照してください。

