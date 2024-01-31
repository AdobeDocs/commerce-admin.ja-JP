---
title: 会社階層の管理
description: 企業階層を構築し、複雑な運用モデルを持つ B2B 組織を管理する方法を学ぶ
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

# の管理 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラム参加者のみ利用可能"}

管理者は、 [!UICONTROL Company Hierarchy] 関連会社を指定した親会社（組織のトップにある会社）に割り当てます。 次の場合、 [!UICONTROL Company Type] 次に該当 `Company`の場合、会社は組織に属しておらず、親会社になる資格があるか、既存の親会社に割り当てられる資格があります。

管理者では、会社を編集し、 [!UICONTROL Company Hierarchy] 会社の割り当てまたは割り当て解除を行うための設定

![会社階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>詳しくは、 [!UICONTROL Company Hierarchy] グリッド、詳しくは、 [会社の階層](account-company-create.md#company-hierarchy) フィールドの説明。

## 会社を組織に割り当てる

1. 次から： _管理者_ サイドバー、次に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![企業グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Adobe Analytics の [!UICONTROL Companies] グリッドで、会社の詳細ページを開き、割り当てを作成します。

   - 追加の会社を既存の親会社に割り当てるには、 **[!UICONTROL Edit]** 親会社のアクション。
   - 親会社を作成するには、 **[!UICONTROL Edit]** 親として指定する会社のアクション。

     既存の親会社または子会社から親会社を作成することはできません。

1. 会社の詳細ページで、を展開します。 **[!UICONTROL Company Hierarchy]**.

   ![会社階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   グリッドには、既存の会社の割り当てが存在する場合は、それが表示されます。 親会社は常に [!UICONTROL Company Hierarchy] グリッド。 The `[!UICONTROL Current]` フラグは編集中の会社を示します。

1. 親組織に会社を追加します。

   - 利用可能な会社のリストから選択し、 **[!UICONTROL Assign Companies]**.

   - **このページのすべてを選択**&#x200B;または 1 つ以上の特定の会社行項目を選択します。

   - 選択 **[!UICONTROL Assign Selected Companies]**.

   - 「 」を選択して会社の割り当てを完了します **[!UICONTROL Assign]**.

     ![会社を組織に割り当て](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 親会社から会社の割り当てを解除

1. 次の日： _管理者_ サイドバー、次に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![企業グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Adobe Analytics の [!UICONTROL Companies] グリッドで、親会社の会社の詳細ページを開き、「 **[!UICONTROL Edit]**.

1. 展開して割り当てられた会社のリストを表示 **[!UICONTROL Company Hierarchy]**.

1. 次から： [!UICONTROL Company Hierarchy] グリッド、 **[!UICONTROL Select]** 選択するアクションコントロール **[!UICONTROL Unassign from parent]**.

   ![親組織から会社の割り当てを解除](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. 割り当てられた会社を階層から削除するよう求められたら、「 」を選択します。 **[!UICONTROL Unassign]**.
