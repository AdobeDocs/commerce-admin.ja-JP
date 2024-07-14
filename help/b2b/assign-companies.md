---
title: 会社階層の管理
description: 企業階層を構築して、複雑な運用モデルを持つ B2B 組織を管理する方法を説明します
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# [!UICONTROL Company Hierarchy] の管理

[!BADGE 1.5.0 – ベータ版 ]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta プログラム参加者のみ使用可能"}

管理者は、関連会社を指定の親会社（組織の最上位にある会社）に割り当てることで、[!UICONTROL Company Hierarchy] を構築できます。 [!UICONTROL Company Type] が `Company` の場合、その会社は組織の一部ではなく、親会社になるか、既存の親会社に割り当てられる資格があります。

管理者では、会社を編集し、会社を割り当てまたは割り当て解除するための [!UICONTROL Company Hierarchy] 設定を更新することで、会社の割り当てを管理します。

![ 会社階層グリッド ](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>[!UICONTROL Company Hierarchy] グリッドについて詳しくは、「[ 会社階層 ](account-company-create.md#company-hierarchy) フィールドの説明を参照してください。

## 組織への会社の割り当て

1. _管理者_ サイドバーから、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

   ![ 会社グリッド ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] グリッドで、会社の詳細ページを開いて割り当てを作成します。

   - 既存の親会社に追加の会社を割り当てるには、親会社の **[!UICONTROL Edit]** のアクションを選択します。
   - 親会社を作成するには、親会社として指定する会社の **[!UICONTROL Edit]** アクションを選択します。

     既存の親会社または子会社から親会社を作成することはできません。

1. 会社の詳細ページで、「**[!UICONTROL Company Hierarchy]**」を展開します。

   ![ 会社階層グリッド ](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   グリッドには、既存の会社の割り当てが存在する場合、それが表示されます。 親会社は、常に [!UICONTROL Company Hierarchy] グリッドの先頭に配置されます。 `[!UICONTROL Current]` フラグは、編集中の会社を示します。

1. 親組織に会社を追加します。

   - **[!UICONTROL Assign Companies]** を選択して、使用可能な会社のリストから選択します。

   - **このページで [ すべて選択 ]** をクリックするか、1 つ以上の特定の会社品目を選択します。

   - 「**[!UICONTROL Assign Selected Companies]**」を選択します。

   - **[!UICONTROL Assign]** を選択して、会社の割り当てを完了します。

     ![ 組織への会社の割り当て ](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 親会社からの会社の割り当て解除

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

   ![ 会社グリッド ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] グリッドで、「**[!UICONTROL Edit]**」を選択して、親会社の会社の詳細ページを開きます。

1. **[!UICONTROL Company Hierarchy]** を展開すると、割り当てられている会社のリストを表示できます。

1. [!UICONTROL Company Hierarchy] グリッドから、**[!UICONTROL Select]** アクションコントロールを使用して会社の割り当てを解除し、**[!UICONTROL Unassign from parent]** を選択します。

   ![ 親組織からの会社の割り当て解除 ](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. プロンプトが表示されたら、「**[!UICONTROL Unassign]**」を選択して、割り当てられた会社を階層から削除します。
