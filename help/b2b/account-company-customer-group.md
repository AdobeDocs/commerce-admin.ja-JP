---
title: 顧客グループの会社への割り当て
description: Adobe Commerce ストアの会社アカウントに顧客グループを割り当てる方法について説明します。
exl-id: fba3c17e-95df-4e9e-84b8-67409c6da72d
feature: B2B, Companies, Configuration, Customers
role: Admin, User
TQID: https://experienceleague.adobe.com/O03eRkYyE78HIHjmwYRXqfOR2A7k1KFL11AspJGCi-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 236
ht-degree: 0%

---

# 顧客グループの会社への割り当て

顧客グループを企業に割り当てることは、基本的に共有カタログを割り当てることと同じです。 共有カタログが設定[&#128279;](enable-basic-features.md)で有効になっていない場合、共有カタログではなく顧客グループが会社に割り当てられます。

- 一度に会社に割り当てることができる顧客グループまたは共有カタログは1つだけです。 共有カタログに関連付けられている顧客グループは削除できません。
- 会社に割り当てられた顧客グループを変更すると、会社のすべてのメンバーのプロファイルが更新されます。
- 顧客グループの割り当てが共有カタログから通常の顧客グループに変更されると、会社のメンバーは共有カタログにアクセスできなくなり、プライマリカタログはストアフロントから利用できるようになります。
- 会社グループを変更した後、会社ユーザーはログアウトしてストアフロントにログインし、カタログに新しい価格を表示する必要があります。

## 顧客グループの変更

1. _管理者_ サイドバーで、**[!UICONTROL Customers]** > **[!UICONTROL Companies]**&#x200B;に移動します。

1. グリッドで会社を見つけ、_[!UICONTROL Action]_&#x200B;列の&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

   ![会社を編集](./assets/companies-grid-edit.png){width="700" zoomable="yes"}

1. 会社ページで、下にスクロールして![拡張セレクター](../assets/icon-display-expand.png)、**[!UICONTROL Advanced Settings]** セクションを展開します。

1. 適切な&#x200B;**[!UICONTROL Customer Group]**&#x200B;を設定します。

   [!UICONTROL Customer Group] リストには、設定で共有カタログが無効になっている場合でも、既存のすべての共有カタログが含まれます。

   ![顧客グループまたは共有カタログの変更](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

1. 確認を求められたら、**[!UICONTROL Proceed]**&#x200B;をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。
