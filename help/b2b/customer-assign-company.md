---
title: 会社アカウントへの顧客の追加
description: 既存の顧客を会社アカウントに追加する方法について説明します。
exl-id: ee2f9c27-37d6-4997-8285-1c4c84f8d04c
feature: B2B, Companies, Customers
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 会社アカウントへの顧客の追加

設定で有効にすると、会社の管理者がユーザーを会社に追加します。 ただし、顧客プロファイルの会社割り当ては、管理者から作成または変更することもできます。

>[!NOTE]
>
>個人が既にストアに個人用アカウントを持っていて、後で会社に就職する場合は、その個人の個人用アカウントを会社に割り当てないでください。 代わりに、会社のメールアドレスを持つユーザーの会社ユーザーアカウントを作成します。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. グリッドで顧客を見つけて、 **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

1. 左パネルで、を選択します。 **[!UICONTROL Account Information]**.

1. クリック **[!UICONTROL Associate to Company]** 会社名の最初の数文字を入力します。

   システムによって、可能なすべての一致のリストが生成されます。

   ![会社に関連付け](./assets/company-assign-customer-account.png){width="600"}

1. リストで、顧客を割り当てる会社を選択し、 **[!UICONTROL Done]**.

1. お客様が以前に別の会社に割り当てられている場合は、 **[!UICONTROL Confirm]**.

   顧客が顧客グループに再割り当てされている [共有カタログ](catalog-shared.md)）を追加し、これに追加しました [会社構造](account-company-structure.md).

1. 完了したら、 **[!UICONTROL Save Customer]**.

   で次の列が更新されます。 [顧客](../customers/customers-all.md) グリッド：

   - この _[!UICONTROL Group]_列が、会社に割り当てられている顧客グループ（または共有カタログ）の名前に変わります。
   - この _[!UICONTROL Company]_列には、顧客プロファイルが関連付けられるようになった会社の名前が表示されます。
