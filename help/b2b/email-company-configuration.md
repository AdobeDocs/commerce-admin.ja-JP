---
title: 会社のメールを設定
description: 会社アカウントのコミュニケーションを送信するために使用されるメールオプションとテンプレートについて説明します。
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 会社のメールオプションを設定

この [営業担当者](account-company-manage.md) 会社のプライマリ連絡先として割り当てられた連絡先は、会社に送信される多数の自動メールメッセージの送信者としてデフォルトで設定されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Company Configuration]**.

1. 必要に応じて、を設定します **[!UICONTROL Store View]** をストア表示に追加して定義します。 [範囲](../getting-started/websites-stores-views.md#scope-settings) ：設定。

1. を完了する **[!UICONTROL Company Registration]** セクション：

   >[!NOTE]
   >
   >をクリア **[!UICONTROL Use system value]** フィールドを編集可能にするチェックボックス。

   - を設定 **[!UICONTROL Company Registration Email Recipient]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) 新しい会社登録要求を受信したときに通知されるユーザー。

   - が含まれる **[!UICONTROL Send Company Registration Email Copy To]** フィールドに、登録通知のコピーを受信する各人のメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、を設定します **[!UICONTROL Default Company Registration Email]** ：テンプレートの名前。 デフォルトでは、 `Company Registration Request` テンプレートが使用されます。

     ![顧客設定 – 会社登録](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. を完了する **[!UICONTROL Customer-Related Emails]** セクション：

   デフォルトの代わりに使用する代替電子メールテンプレートを準備している場合は、次のそれぞれに使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![顧客設定 – 顧客関連のメール](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. を完了する **[!UICONTROL Company Status Change]** セクション：

   - を設定 **[!UICONTROL Company Status Change for Email Recipient]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) 会社の状態が変更されたときに通知されるユーザー。

   - が含まれる **[!UICONTROL Send Company Status Change Email Copy To]** フィールドに、ステータス変更通知のコピーを受信する各個人のメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - 会社のステータスが「」から変更された場合、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合 `Pending Approval` 対象： `Active`、設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** そのテンプレートに。 デフォルトでは、 `Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが「」から変更された場合、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合 `Rejected` または `Blocked` 対象： `Active`、設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** そのテンプレートに。 デフォルトでは、 `Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合 `Rejected`、設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** そのテンプレートに。 デフォルトでは、 `Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合 `Blocked`、設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** そのテンプレートに。 デフォルトでは、 `Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合 `Pending Approval`、設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** そのテンプレートに。 デフォルトでは、 `Company Status Pending Approval` テンプレートが使用されます。

     ![顧客の設定 – 会社ステータスの変更](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. を完了する **[!UICONTROL Company Credit Emails]** セクション：

   - を設定 **[!UICONTROL Company Credit Change Email Sender]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) 会社に割り当てられた与信限度額を変更した際に通知されるユーザー。 デフォルトでは、通知はに送信されます。 _営業担当者_.

   - が含まれる **[!UICONTROL Send Company Credit Change Email Copy To]** フィールドに、与信変更通知のコピーを受信する各担当者の電子メール・アドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、会社管理者に送信される次の各通知に対してテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![顧客設定 – 会社のクレジットメール](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Save Config]**.
