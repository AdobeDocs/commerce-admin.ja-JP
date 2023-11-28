---
title: 会社の電子メールを設定
description: 会社アカウントのコミュニケーションを送信するために使用する電子メールのオプションとテンプレートについて説明します。
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 会社の電子メールオプションを設定する

The [営業担当者](account-company-manage.md) 会社の主要連絡先として割り当てられる電子メールメッセージは、会社に送信される多数の自動電子メールメッセージの送信者としてデフォルトで設定されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Company Configuration]**.

1. 必要に応じて、 **[!UICONTROL Store View]** をストア表示に追加して、 [範囲](../getting-started/websites-stores-views.md#scope-settings) 設定の。

1. 次を完了： **[!UICONTROL Company Registration]** セクション：

   >[!NOTE]
   >
   >次をクリア： **[!UICONTROL Use system value]** チェックボックスをオンにして、フィールドを編集可能にします。

   - 設定 **[!UICONTROL Company Registration Email Recipient]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) 新しい会社登録要求を受け取ったときに通知を受け取るユーザー。

   - Adobe Analytics の **[!UICONTROL Send Company Registration Email Copy To]** 「 」フィールドで、登録通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - デフォルトの代わりに使用する電子メールテンプレートを準備した場合は、 **[!UICONTROL Default Company Registration Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Registration Request` テンプレートが使用されます。

     ![顧客の設定 — 会社の登録](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 次を完了： **[!UICONTROL Customer-Related Emails]** セクション：

   デフォルトの代わりに使用する代替の電子メールテンプレートを準備した場合、次の各項目に使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![顧客設定 — 顧客関連の E メール](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 次を完了： **[!UICONTROL Company Status Change]** セクション：

   - 設定 **[!UICONTROL Company Status Change for Email Recipient]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) 会社のステータスが変更されたときに通知を受け取るユーザー。

   - Adobe Analytics の **[!UICONTROL Send Company Status Change Email Copy To]** 「 」フィールドで、ステータス変更通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - 会社のステータスが次の日から変わった場合にデフォルトの代わりに使用する準備済みの電子メールテンプレートがある場合 `Pending Approval` から `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** をそのテンプレートに追加します。 デフォルトでは、 `Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが次の日から変わった場合にデフォルトの代わりに使用する準備済みの電子メールテンプレートがある場合 `Rejected` または `Blocked` から `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** をそのテンプレートに追加します。 デフォルトでは、 `Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「 `Rejected`，設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** をそのテンプレートに追加します。 デフォルトでは、 `Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「 `Blocked`，設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** をそのテンプレートに追加します。 デフォルトでは、 `Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「 `Pending Approval`，設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** をそのテンプレートに追加します。 デフォルトでは、 `Company Status Pending Approval` テンプレートが使用されます。

     ![顧客の設定 — 会社のステータスの変更](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 次を完了： **[!UICONTROL Company Credit Emails]** セクション：

   - 設定 **[!UICONTROL Company Credit Change Email Sender]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) 会社に割り当てられているクレジット制限に変更が加えられた場合に通知を受け取るユーザー。 デフォルトでは、通知は _セールス担当者_.

   - Adobe Analytics の **[!UICONTROL Send Company Credit Change Email Copy To]** 「 」フィールドで、クレジット変更通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **[!UICONTROL Send Email Copy Method]** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - デフォルトの代わりに使用する電子メールテンプレートを準備した場合は、会社の管理者に送信される次の各通知のテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![顧客の設定 — 会社のクレジットメール](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.
