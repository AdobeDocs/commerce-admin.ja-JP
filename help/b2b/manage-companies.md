---
title: 会社管理
description: 複雑な運用モデルを持つ B2B 組織の管理と管理を合理化します。
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

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラム参加者のみ利用可能"}

会社管理は、複雑な組織構造を持つ企業の業務を合理化します。 管理者は、会社を指定された親会社に割り当てることで、B2B 組織を反映する会社階層を構築できます。 この割り当てにより、親会社管理者は組織内の会社を表示および管理できます。

から会社の管理タスクを開始 *[!UICONTROL Companies]* 表示。 管理者から、に移動します。  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B 企業グリッドの管理](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Adobe Analytics の *[!UICONTROL Companies grid]*、 *[!UICONTROL Company Type]* 列は、会社が組織の一部として管理されているか、別の会社として管理されているかを示します。

- `Parent` は、1 つ以上の会社が割り当てられているビジネス組織です。 親会社を別の会社の子として割り当てることはできません。

- `Child` は、組織に割り当てられている会社です。 1 つの会社を 1 つの親会社にのみ割り当てることができます。

- `Company` は、単一の会社を表します。 1 つの会社を親会社にするか、既存の親会社に割り当てることで、1 つの会社を組織に含めることができます。

親会社または子会社を編集する場合は、を展開します。 *[!UICONTROL Company Hierarchy]* をクリックして、組織内のすべての会社を表示します。 A `Current` フラグは編集中の会社を示します。

![B2B 企業階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## 以下を表示して設定します。 [!UICONTROL Company Hierarchy]

最初の会社の作成時に、 [!UICONTROL Company Hierarchy] グリッドが空です。 また、会社が単一の会社の場合は空です。

![B2B 企業階層グリッド](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

親会社の場合、適切な権限を持つ管理者ユーザーは、次のタスクを実行できます。

- 新しい親組織を作成するか、既存の親組織を更新して、会社階層を構築します。
- 会社を追加または削除する既存の組織を管理します。

詳しくは、 [会社階層の管理](assign-companies.md).
