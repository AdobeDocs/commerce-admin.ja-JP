---
title: 会社階層の管理
description: 複雑な運用モデルを持つ B2B 組織をサポートするために、企業階層を構築および管理します。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# の管理 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="ベータ版プログラム参加者のみ利用可能"}

管理者は、 [!UICONTROL Company Hierarchy] 関連会社を指定された親会社（組織階層の最上位にある会社）に割り当てることで、

既存の会社に割り当てられていない会社を編集して親会社を作成する [!UICONTROL Company Hierarchy]、および関連会社の割り当て。

![会社階層グリッド](./assets/company-detail-view.png){width="700"}

会社を階層に割り当てた後は、 [!UICONTROL Company type] 列の **会社** 企業を A として識別するグリッド `Parent` または  `Child` 会社名。  次の場合、 [!UICONTROL Company Type] 次に該当 `Company`の場合、会社は会社階層の一部ではなく、親会社になる資格があるか、既存の親会社に割り当てられます。

>[!NOTE]
>
>詳しくは、 [!UICONTROL Company Hierarchy] グリッド、詳しくは、 [会社の階層](account-company-create.md#company-hierarchy) フィールドの説明。

管理者では、会社を編集し、 [!UICONTROL Company Hierarchy] のセクション [!UICONTROL Company] 会社の割り当てまたは割り当て解除を行うページ

## 会社を親会社に割り当て

1. 次の日： _管理者_ サイドバー、次に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![企業グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 「会社」グリッドで、会社の詳細ページを開き、割り当てを作成します。

   - 追加の会社を既存の親会社に割り当てるには、 **[!UICONTROL Edit]** 親会社のアクション。
   - 新しい親会社を作成するには、 **[!UICONTROL Edit]** 親として指定された会社に対するアクション。

     既存の親会社または子会社から新しい親会社を作成することはできません。

   ![新しい会社](./assets/company-update.png){width="700" zoomable="yes"}

1. 会社の詳細ページで、 **[!UICONTROL Company Hierarchy]** ドロップダウンと選択 **[!UICONTROL Assign Companies]**.

   ![新しい会社](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   このビューを展開すると、既存の会社の割り当てが存在する場合は、その割り当てを表示できます。 親会社は常に _[!UICONTROL Company Hierarchy]_グリッド `current company indicator` 編集中の会社ラインに表示されます。

1. 割り当てに使用できる会社がグリッドに表示されます。 割り当てる会社を選択し、「 」を選択します。 **[!UICONTROL Assign Selected Companies]**.

1. 以下が可能です。 **このページのすべてを選択** または 1 つの特定の会社行項目をクリックします。 **[!UICONTROL Assign Selected Companies]**.

   ![新しい会社](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. プロンプトが表示されたら、「 」を選択して会社の割り当てを完了します。 **[!UICONTROL Assign]**.

## 親会社から会社の割り当てを解除

1. 次の日： _管理者_ サイドバー、次に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![企業グリッド](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 会社ページで、親会社の会社の詳細ページを開き、 **[!UICONTROL Edit]** アクション。

   ![新しい会社](./assets/company-update.png){width="700" zoomable="yes"}

1. 割り当てられた会社のリストを表示するには、 **[!UICONTROL Company Hierarchy]** ドロップダウン。

1. 会社階層グリッドから、 **[!UICONTROL Select]** 会社に対するアクションを実行し、次に **[!UICONTROL Unassign from parent]**.

   ![新しい会社](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. 割り当てられた会社を階層から削除するよう求められたら、「 」を選択します。 **[!UICONTROL Unassign]**.
