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

# を管理する [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0 – ベータ版]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラムの参加者のみが使用できます"}

管理者はを作成できます [!UICONTROL Company Hierarchy] 関係会社を指定親会社（組織の最上位の会社）に割り当てる。 次の場合 [!UICONTROL Company Type] 等しい `Company`ただし、その会社は組織に属しておらず、親会社になるか、既存の親会社に割り当てられる資格があります。

管理者では、会社を編集してを更新することにより、会社の割り当てを管理します [!UICONTROL Company Hierarchy] 会社を割り当てる、または割り当てを解除する設定。

![会社階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>について [!UICONTROL Company Hierarchy] グリッド、を参照 [会社階層](account-company-create.md#company-hierarchy) フィールドの説明。

## 組織への会社の割り当て

1. から _Admin_ サイドバー、移動先 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![会社グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. が含まれる [!UICONTROL Companies] グリッドで、会社の詳細ページを開いて割り当てを作成します。

   - 追加の会社を既存の親会社に割り当てるには、 **[!UICONTROL Edit]** 親会社に対するアクション。
   - 親会社を作成するには、 **[!UICONTROL Edit]** 会社が親として指定するアクション。

     既存の親会社または子会社から親会社を作成することはできません。

1. 会社の詳細ページでを展開します **[!UICONTROL Company Hierarchy]**.

   ![会社階層グリッド](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   グリッドには、既存の会社の割り当てが存在する場合、それが表示されます。 親会社は常に [!UICONTROL Company Hierarchy] グリッド。 この `[!UICONTROL Current]` フラグは、編集中の会社を示します。

1. 親組織に会社を追加します。

   - を選択して、利用可能な会社のリストから選択します。 **[!UICONTROL Assign Companies]**.

   - **このページですべてを選択**&#x200B;または、1 つ以上の特定の会社行項目を選択します。

   - を選択 **[!UICONTROL Assign Selected Companies]**.

   - 次を選択して、会社の割り当てを完了します **[!UICONTROL Assign]**.

     ![組織への会社の割り当て](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 親会社からの会社の割り当て解除

1. 日 _Admin_ サイドバー、移動先 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![会社グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. が含まれる [!UICONTROL Companies] グリッドで、次の項目を選択して、親会社の会社の詳細ページを開きます **[!UICONTROL Edit]**.

1. 割り当てられた会社の一覧を表示するには、次の項目を展開します **[!UICONTROL Company Hierarchy]**.

1. から [!UICONTROL Company Hierarchy] グリッド、会社の割り当てを解除するには **[!UICONTROL Select]** 選択するアクション制御 **[!UICONTROL Unassign from parent]**.

   ![親組織からの会社の割り当て解除](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. プロンプトが表示されたら、以下を選択して、割り当てられた会社を階層から削除します。 **[!UICONTROL Unassign]**.
