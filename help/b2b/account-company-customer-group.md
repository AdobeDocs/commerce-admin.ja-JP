---
title: 会社への顧客グループの割り当て
description: Adobe Commerce ストアの会社アカウントに顧客グループを割り当てる方法について説明します。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: a5a8da076d6cd91eb6c3e573fec5b3fb9d2d3341
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# 会社への顧客グループの割り当て

顧客グループを会社に割り当てる方法は、基本的に共有カタログを割り当てる方法と同じです。 共有カタログが [設定で有効](enable-basic-features.md)では、共有カタログではなく顧客グループが会社に割り当てられます。

>[!NOTE]
>
> 会社に割り当てることができる顧客グループまたは共有カタログは一度に 1 つだけです。 共有カタログに関連付けられている顧客グループは削除できません。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. グリッドで会社を見つけて、 **[!UICONTROL Edit]** が含まれる _[!UICONTROL Action]_列。

   ![会社の編集](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 会社ページで、下にスクロールして展開します ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

1. 適切な **[!UICONTROL Customer Group]**.

   >[!NOTE]
   >
   >この [!UICONTROL Customer Group] 設定で共有カタログが無効になっている場合でも、リストには既存の共有カタログがすべて含まれます。

   会社に割り当てられている顧客グループを変更すると、すべての会社メンバーのプロファイルが更新されます。

   >[!NOTE]
   >
   >会社グループを変更した後、会社のユーザーはログアウトしてストアフロントにログインして、カタログに新しい価格を表示する必要があります。

   ![顧客グループまたは共有カタログの変更](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   >[!NOTE]
   >
   >顧客グループの割り当てを共有カタログから通常の顧客グループに変更すると、会社メンバーは共有カタログにアクセスできなくなり、ストアフロントからプライマリカタログを使用できるようになります。

1. 確認を求められたら、 **[!UICONTROL Proceed]**.

1. クリック **[!UICONTROL Save]**.
