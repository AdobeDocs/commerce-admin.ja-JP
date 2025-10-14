---
title: 会社への顧客グループの割り当て
description: Adobe Commerce ストアの会社アカウントに顧客グループを割り当てる方法について説明します。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
source-git-commit: 581d2cf82880552432471171b69a1a597da54c30
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 会社への顧客グループの割り当て

顧客グループを会社に割り当てる方法は、基本的に共有カタログを割り当てる方法と同じです。 共有カタログが [&#x200B; 設定で有効 &#x200B;](enable-basic-features.md) になっていない場合は、共有カタログではなく顧客グループが会社に割り当てられます。

- 会社に割り当てることができる顧客グループまたは共有カタログは一度に 1 つだけです。 共有カタログに関連付けられている顧客グループは削除できません。
- 会社に割り当てられている顧客グループを変更すると、すべての会社メンバーのプロファイルが更新されます。
- 顧客グループの割り当てを共有カタログから通常の顧客グループに変更すると、会社メンバーは共有カタログにアクセスできなくなり、ストアフロントからプライマリカタログを使用できるようになります。
- 会社グループを変更した後、会社のユーザーはログアウトしてストアフロントにログインして、カタログに新しい価格を表示する必要があります。

## 顧客グループの変更

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. グリッドで会社を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

   ![&#x200B; 会社の編集 &#x200B;](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 会社ページで、下にスクロールして「**[!UICONTROL Advanced Settings]**」セクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開します。

1. 適切な **[!UICONTROL Customer Group]** を設定します。

   設定で共有カタログが無効になっている場合でも、[!UICONTROL Customer Group] リストには既存のすべての共有カタログが表示されます。

   ![&#x200B; 顧客グループまたは共有カタログの変更 &#x200B;](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. 確認を求めるメッセージが表示されたら、「**[!UICONTROL Proceed]**」をクリックします。

1. 「**[!UICONTROL Save]**」をクリックします。
