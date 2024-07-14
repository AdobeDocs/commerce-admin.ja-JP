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

会社の主要連絡先として割り当てられた [ 営業担当者 ](account-company-manage.md) は、デフォルトで、会社に送信される多くの自動メールメッセージの送信者として設定されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Company Configuration]**」を選択します。

1. 必要に応じて、**[!UICONTROL Store View]** をストア表示に設定して、設定の [ スコープ ](../getting-started/websites-stores-views.md#scope-settings) を定義します。

1. **[!UICONTROL Company Registration]** のセクションを完了します。

   >[!NOTE]
   >
   >フィールドを編集可能にするには、「**[!UICONTROL Use system value]**」チェックボックスをオフにします。

   - **[!UICONTROL Company Registration Email Recipient]** を、新しい会社登録要求を受信したときに通知される [ ストアの連絡先 ](../getting-started/store-details.md#store-email-addresses) に設定します。

   - **[!UICONTROL Send Company Registration Email Copy To]** フィールドに、登録通知のコピーを受信する各個人のメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**[!UICONTROL Send Email Copy Method]** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default Company Registration Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Registration Request` テンプレートが使用されます。

     ![ 顧客設定 – 会社登録 ](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. **[!UICONTROL Customer-Related Emails]** のセクションを完了します。

   デフォルトの代わりに使用する代替電子メールテンプレートを準備している場合は、次のそれぞれに使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![ 顧客設定 – 顧客関連のメール ](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. **[!UICONTROL Company Status Change]** のセクションを完了します。

   - **[!UICONTROL Company Status Change for Email Recipient]** を、会社のステータスが変更されたときに通知される [ ストアの連絡先 ](../getting-started/store-details.md#store-email-addresses) に設定します。

   - 「**[!UICONTROL Send Company Status Change Email Copy To]**」フィールドに、ステータス変更通知のコピーを受信する各個人のメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**[!UICONTROL Send Email Copy Method]** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - 会社のステータスが `Pending Approval` から `Active` に変更されたときに、デフォルトの代わりに使用される準備済みのメールテンプレートがある場合は、そのテンプレートに **[!UICONTROL Default 'Company Status Change to Active 1' Email]** を設定します。 デフォルトでは、`Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが `Rejected` または `Blocked` から `Active` に変更されたときに、デフォルトの代わりに使用される準備済みのメールテンプレートがある場合は、そのテンプレートに **[!UICONTROL Default 'Company Status Change to Active 2' Email]** を設定します。 デフォルトでは、`Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「`Rejected`」に変わったときに、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合は、**[!UICONTROL Default 'Company Status Change to Rejected' Email]** をそのテンプレートに設定します。 デフォルトでは、`Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「`Blocked`」に変わったときに、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合は、**[!UICONTROL Default 'Company Status Change to Blocked' Email]** をそのテンプレートに設定します。 デフォルトでは、`Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「`Pending Approval`」に変わったときに、デフォルトの代わりに使用する準備済みのメールテンプレートがある場合は、**[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** をそのテンプレートに設定します。 デフォルトでは、`Company Status Pending Approval` テンプレートが使用されます。

     ![ 顧客の設定 – 会社ステータスの変更 ](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. **[!UICONTROL Company Credit Emails]** のセクションを完了します。

   - 会社に割り当てられているクレジット限度額に変更があったときに通知される [ ストア連絡先 ](../getting-started/store-details.md#store-email-addresses) に **[!UICONTROL Company Credit Change Email Sender]** を設定します。 デフォルトでは、通知は _営業担当者_ に送信されます。

   - 「**[!UICONTROL Send Company Credit Change Email Copy To]**」フィールドに、与信変更通知のコピーを受信する各担当者の電子メール・アドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**[!UICONTROL Send Email Copy Method]** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、会社管理者に送信される次の各通知に対してテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![ 顧客設定 – 会社クレジットメール ](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
