---
title: 会社階層の管理
description: 複雑な運用モデルを持つ B2B 組織をサポートするために、会社階層を作成および管理します。
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Company Hierarchy] の管理

管理者は、関連会社を指定の親会社（組織階層の最上位にある会社）に割り当てることにより、[!UICONTROL Company Hierarchy] を作成できます。

管理者から、[!UICONTROL Company Hierarchy] 設定で個々の会社（`[!UICONTROL Company Type] = Company`）を編集して関連会社を割り当てることにより、親会社を作成します。

![ 会社階層グリッド ](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>[!UICONTROL Company Hierarchy] グリッドについて詳しくは、「[ 会社階層 ](account-company-create.md#company-hierarchy) フィールドの説明を参照してください。

親会社を編集し、*[!UICONTROL Company Hierarchy]* グリッドを使用して会社を追加または削除することで、会社の割り当てを管理します。 *[!UICONTROL Actions]* コントロールを使用して、組織内の会社の [ 詳細設定の構成 ](#change-company-settings) を管理します。

## 親会社への会社の割り当て

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

   ![ 会社グリッド ](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] グリッドから、会社の詳細ページを開いて割り当てを作成します。

   - 既存の親会社に追加の会社を割り当てるには、親会社の **[!UICONTROL Edit]** のアクションを選択します。
   - 親会社を作成するには、親として指定した会社の **[!UICONTROL Edit]** のアクションを選択します。

     既存の親会社または子会社から新しい親会社を作成することはできません。

1. 会社の詳細ページで、「**[!UICONTROL Company Hierarchy]**」を展開し、「**[!UICONTROL Assign Companies]**」を選択します。

   ![ 親会社を作成 ](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. 使用可能な会社のリストから、割り当てる会社を選択し、「**[!UICONTROL Assign Selected Companies]**」を選択します。

   ![ 割り当てる会社を選択 ](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. プロンプトが表示されたら、「**[!UICONTROL Assign]**」を選択して会社の割り当てを完了します。

## 親会社からの会社の割り当て解除

1. 会社ページで、**[!UICONTROL Edit]** のアクションを選択して、親会社の会社の詳細ページを開きます。

   ![ 親会社の詳細ページ ](./assets/company-update.png){width="700" zoomable="yes"}

1. **[!UICONTROL Company Hierarchy]** を展開すると、割り当てられている会社のリストを表示できます。

1. 組織から会社を削除します。

   - 削除する会社の [!UICONTROL Action] 列で、**[!UICONTROL Select]**/**[!UICONTROL Unassign from parent]** を選択します。

     ![ 組織からの会社の削除 ](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - プロンプトが表示されたら、「**[!UICONTROL Unassign]**」を選択して、割り当てられた会社を階層から削除します。

## 組織の会社設定の管理

組織の [ 詳細設定 ](account-company-create.md#advanced-settings) 設定を更新して、すべての子会社に親設定を適用するか、組織内の選択した会社に同じ設定を適用します。

更新プロセス中、初期設定値はデフォルトで、親会社に設定されている現在の値になります。 選択した会社の構成を更新するには、少なくとも 1 つの設定を変更する必要があります。

**複数会社の詳細設定の設定の変更**

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. [!UICONTROL Companies] のグリッドで、**[!UICONTROL Action]** の列から **[!UICONTROL Edit]** を選択して親会社を編集します。

1. 親会社の詳細ページで、「」セクション **[!UICONTROL Company Hierarchy]** 展開して、組織に含まれる会社を表示します。

1. 設定する会社を選択します。

   ![ 会社階層から会社を選択 ](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. グリッドの上にある **[!UICONTROL Actions]** コントロールから、[**[!UICONTROL Change company settings]**] を選択します。

   ![ 会社階層の会社設定の変更 ](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 設定の構成を変更します。

   - [!UICONTROL Change company settings] ページで、変更する設定を見つけます。

   - 「**[!UICONTROL Change]**」チェックボックスをオンにして、設定を有効にします。

   - 必要に応じて値を更新します。

     ![ 複数の会社の会社設定の変更 ](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 設定を更新したら、「**[!UICONTROL Apply Changes]**」を選択します。

1. プロンプトが表示されたら、「**[!UICONTROL Change settings]**」を選択して、選択した会社の設定を更新します。

>[!TIP]
>
>会社行項目を編集して、1 つの会社の詳細設定の構成を管理します。
