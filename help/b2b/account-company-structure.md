---
title: 会社アカウント構造
description: 会社構造と、ビジネスワークフローおよびポリシーをサポートするために会社管理者が会社構造を定義する方法について説明します。
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# 会社アカウント構造

会社アカウントを設定して、ビジネスの構造を反映させることができます。 最初は、会社の構造には会社の管理者のみが含まれていますが、ユーザーのチームを含めるように拡張できます。 ユーザーは、チームに関連付けたり、会社内の部門や下位部門の階層内で整理したりできます。

![ 部門を有する企業体質 ](./assets/company-structure-diagram.svg){width="500"}

ストアフロント上の会社管理者のアカウントダッシュボードでは、会社構造はツリーで表され、最初は会社管理者のみで構成されています。

![ 会社管理者を置く会社組織 ](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

マーチャントの場合、会社全体の構造が管理画面の _会社_ グリッドと _顧客_ グリッドに反映されます。 会社グリッドには、ステータスに関係なくすべての会社が一覧表示されます。

![ 会社グリッド ](./assets/companies-grid.png){width="700" zoomable="yes"}

次の例は、各会社の最初の会社管理者アカウントを含む [!UICONTROL Customers] グリッドを示しています。

![ 会社管理者アカウントを持つ顧客グリッド ](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

アカウントを作成した後、会社の管理者は、会社の構造を [ チーム ](account-company-structure.md) で定義し、それぞれに [ 会社ユーザー ](account-company-users.md) を設定して [ 役割と権限 ](account-company-roles-permissions.md) を設定できます。

>[!NOTE]
>
>会社ユーザーが追加されると、最初は会社ユーザーが会社管理者の下のルート会社構造に追加されます。 会社管理者が会社内で複数の役割を実行する場合は、役割ごとに異なるメールアドレスを使用して、個別の会社ユーザーアカウントを作成します。

## 会社構造アイコン

| アイコン | 説明 |
| ---- | ----------------- |
| ![ 会社管理者アイコン ](./assets/company-icon-admin.png) | 会社構造内の会社管理者を表します。 |
| ![ チームアイコン ](./assets/company-icon-team.png) | 会社構造内のチームを表します。 |
| ![ ユーザーアイコン ](./assets/company-icon-user.png) | 会社構造内のユーザーを表します。 |
| ![ 移動アイコン ](./assets/company-icon-move.png) | チームを会社構造内の別の位置に移動します。 |
| ![ 拡張アイコン ](./assets/company-icon-expand.png) | 会社構造でチームを展開します。 |
| ![ 折りたたみアイコン ](./assets/company-icon-collapse.png) | 会社構造内のチームを折りたたみます。 |

{style="table-layout:auto"}

## 会社チームの作成

会社のアカウントの構造は、シンプルでフラットな組織か、会社の下位区分や部署ごとに異なるチームを持つ複雑な組織かに関わらず、購買組織を反映する必要があります。

会社が独自のアカウントを管理できるようにストアが [ 設定 ](enable-basic-features.md) されている場合、アカウントの承認後、会社の管理者が最初に完了するタスクの 1 つは、会社構造の設定です。 会社アカウントでは、会社の構造はツリーとして表され、会社の管理者が最上位に表示されます。

![ チームを持つ会社体制 ](./assets/company-structure-teams-diagram.svg){width="450"}

1. 会社の管理者が自分のアカウントにログインします。

1. 左側のパネルで、「**[!UICONTROL Company Structure]**」を選択します。

1. **[!UICONTROL Business Structure]** で **[!UICONTROL Add Team]** をクリックし、次の操作を実行します。

   - **[!UICONTROL Team Title]** および **[!UICONTROL Description]** を入力します。

     チームのタイトルには、チーム、オフィス、会社内の部署など、会社の構造を表すものを使用できます

     ![ チームを追加 ](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - 完了したら、「**[!UICONTROL Save]**」をクリックします。

   - 必要な数のチームを作成します。

1. チームの階層を作成するために、管理者は次の操作を実行します。

   - 親チームを選択し、[**[!UICONTROL Add Team]**] をクリックします。

     ![ 部門を有する企業体質 ](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - **[!UICONTROL Team Title]** および **[!UICONTROL Description]** を入力します。

   - **[!UICONTROL Save]** をクリックします。

1. これらの手順を繰り返して、必要な数のチーム、または必要な数の分割と分割を作成します。

   ![ 組織と事業部を有する企業体質 ](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## チームの移動

会社の管理者は、会社の構造を操作する際に、チームや部門を構造内の他の場所にドラッグできます。

1. 会社管理者が移動するチームを見つけます。

1. チームをクリックして、会社構造内の新しい位置にドラッグします。

## チームの削除

>[!NOTE]
>
>チームを削除する前に、正しいチームが選択されていることを確認することをお勧めします。削除されたチームは復元できません。

1. 会社の管理者が、削除するチームを選択します。

1. **[!UICONTROL Delete Selected]** をクリックします。

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Delete]**」をクリックします。

## チーム構造を展開または折りたたむ

会社の管理者は、会社の構造を操作する際に、ツリーを折りたたんだり展開したりできます。

- **[!UICONTROL Collapse All]** または **[!UICONTROL Expand All]** をクリックします。

- チームを折りたたむには ![ 展開されたアイコン ](../assets/icon-display-collapse.png) をクリックし、チームを展開するには ![ 折りたたまれたアイコン ](../assets/icon-display-expand.png) をクリックします。

## チームへのユーザーの割り当て

チームとユーザーが最初に [ 会社構造 ](account-company-structure.md) に追加されると、それらは会社管理者の下の同じレベルに配置されます。

![ ユーザーとチームを使用した会社構造 ](./assets/company-users-added.png){width="700" zoomable="yes"}

| 制御 | 説明 |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | ビジネス構造ツリーを折りたたむか展開します |
| [!UICONTROL Add User] | 現在のチームの下にユーザーを作成します |
| [!UICONTROL Add Team] | チームを作成します |
| [!UICONTROL Edit Selected / Remove from Structure] | ユーザー情報を編集するか、ビジネス ツリーからユーザーを削除します。 詳しくは、[ 会社ユーザーアカウントの管理 ](account-company-users.md) を参照してください。 |

{style="table-layout:auto"}

1. 左側のパネルでは、会社の管理者が **[!UICONTROL Company Structure]** を選択します。

1. 既存のチームにユーザーを割り当てるには、ユーザーを適切なチームの下にドラッグ（![ 移動アイコン ](../assets/icon-move.png)）します。

   ![ チームの割り当て ](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
