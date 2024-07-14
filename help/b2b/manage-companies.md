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

[!BADGE 1.5.0 – ベータ版 ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta プログラム参加者のみ使用可能"}

会社経営は、複雑な組織構造を持つ企業の業務を合理化します。 管理者ユーザーは、会社を指定された親会社に割り当てることにより、B2B 組織をミラーリングする会社階層を作成できます。 この割り当てを使用すると、親会社管理者は組織内の会社を表示および管理できます。

*[!UICONTROL Companies]* ビューから会社管理タスクを開始します。 管理者で、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

![B2B 会社グリッドの管理 ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Companies grid]* の *[!UICONTROL Company Type]* の列は、会社が組織の一部として管理されているか、別の会社として管理されているかを示します。

- `Parent` は、1 つ以上の会社が割り当てられているビジネス組織です。 親会社を他の会社の子として割り当てることはできません。

- `Child` は、組織に割り当てられている会社です。 会社は、1 つの親会社にのみ割り当てることができます。

- `Company` は単一の会社を表します。 1 つの会社を組織の一部にするには、その会社を親会社にするか、既存の親会社に割り当てます。

親または子会社を編集する際に、*[!UICONTROL Company Hierarchy]* を展開すると、組織内のすべての会社が表示されます。 `Current` フラグは、編集中の会社を示します。

![B2B 会社階層グリッド ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## [!UICONTROL Company Hierarchy] の表示と設定

会社の初回作成時には、[!UICONTROL Company Hierarchy] グリッドは空です。 会社が 1 つの会社の場合も空です。

![B2B 会社階層グリッド ](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

親会社の場合、適切な権限を持つ管理者ユーザーは次のタスクを実行できます。

- 新しい親組織を作成するか、既存の親組織を更新して、会社階層を構築します。
- 既存の組織を管理して会社を追加または削除します。

詳しくは、[ 会社階層の管理 ](assign-companies.md) を参照してください。
