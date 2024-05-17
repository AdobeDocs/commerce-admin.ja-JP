---
title: 会社管理
description: 複雑な運用モデルにより、B2B 組織の管理を合理化します。
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 会社管理

[!BADGE 1.5.0 – ベータ版]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラムの参加者のみが使用できます"}

会社経営は、複雑な組織構造を持つ企業の業務を合理化します。 管理者ユーザーは、会社を指定された親会社に割り当てることにより、B2B 組織をミラーリングする会社階層を作成できます。 この割り当てを使用すると、親会社管理者は組織内の会社を表示および管理できます。

からの会社管理タスクの開始 *[!UICONTROL Companies]* 表示。 管理者から、に移動します。  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B 会社管理グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

が含まれる *[!UICONTROL Companies grid]*, *[!UICONTROL Company Type]* 列は、会社が組織の一部として管理されているか、別の会社として管理されているかを示します。

- `Parent` は、1 つ以上の会社が割り当てられているビジネス組織です。 親会社を他の会社の子として割り当てることはできません。

- `Child` は、組織に割り当てられている会社です。 会社は、1 つの親会社にのみ割り当てることができます。

- `Company` 単一の会社を表します。 1 つの会社を組織の一部にするには、その会社を親会社にするか、既存の親会社に割り当てます。

親会社または子会社を編集する場合は、を展開します *[!UICONTROL Company Hierarchy]* 組織内のすべての会社を表示します。 A `Current` フラグは、編集中の会社を示します。

![B2B 会社階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## を表示および設定する [!UICONTROL Company Hierarchy]

会社の初回作成時、 [!UICONTROL Company Hierarchy] グリッドが空です。 会社が 1 つの会社の場合も空です。

![B2B 会社階層グリッド](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

親会社の場合、適切な権限を持つ管理者ユーザーは次のタスクを実行できます。

- 新しい親組織を作成するか、既存の親組織を更新して、会社階層を構築します。
- 既存の組織を管理して会社を追加または削除します。

詳しくは、を参照してください [会社階層の管理](assign-companies.md).
