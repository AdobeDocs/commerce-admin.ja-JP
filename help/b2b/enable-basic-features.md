---
title: B2B 機能を有効にする
description: 会社アカウント、デフォルトの支払い方法と配送方法、発注、注文の承認など、Adobe Commerceストアに対する B2B 機能の有効化について説明します。
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# B2B 機能を有効にする

デフォルトでは、すべての B2B 機能は最初は無効になっています。 ストア管理者は、コマースストアの必要に応じて、B2B 機能を有効または無効にできます。 B2B 構成設定の完全なリストについては、 [B2B 機能設定リファレンス](../configuration-reference/general/b2b-features.md).

顧客企業のサポートを有効にすると、追加の B2B 機能が自動的に有効になります。

- [!DNL Shared Catalog]

  様々な会社のカスタム価格設定をサポートし、すべての店舗のカテゴリ権限も有効にします。

- [!DNL Enable Shared Catalog direct products price assigning]

  価格指数で共有カタログに割り当てられた製品のみを保存することで、サイトのパフォーマンスが向上します。 多くの共有カタログを持つマーチャントが異なる企業のカスタム価格を管理する場合、この機能を有効にすることはベストプラクティスです。

- [!DNL B2B Quotes]

  販売者や企業の購入者に、価格を交渉する機能を与えます。

- [!DNL B2B default payment and shipping methods]

  ストアフロントで B2B 購入者が使用できる支払いおよび配送オプションの選択を決定します。

これらの機能の設定は、 [!DNL Enable Company] が `Yes`.

B2B [!DNL Quick Order] および [!DNL Requisition List] 機能は、個別に有効と無効を切り替えることができます。

## B2B 機能の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   マルチサイトインストールを行っている場合は、 **[!UICONTROL Store View]** コントロールを使用します。

1. の下の左側のパネル _[!UICONTROL General]_を選択します。**[!UICONTROL B2B Features]**:

   ![B2B 設定 — 一般](./assets/b2b-features.png){width="600"}

   - 顧客が自社のアカウントを管理し、 **[!UICONTROL Enable Company]**  から `Yes`.

     企業サポートを有効にすると、「共有カタログ」、「B2B 見積」、「B2B 支払方法」、「B2B 発送方法」が自動的に有効になります。

   - SKU または製品名に基づいて顧客やゲストが迅速に注文を行えるようにするには、 **[!UICONTROL Enable Quick Order]** から `Yes`.

   - 顧客が自分のアカウントダッシュボードから購買依頼リストを作成および管理できるようにするには、次のように設定します。 **[!UICONTROL Enable Requisition List]** から `Yes`.

     また、 [最大リスト数の設定](configure-requisition-lists.md) 顧客は、アカウントにを持つことができます。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## デフォルトの B2B 支払い方法と発送方法を設定する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default B2B Payment Methods]** 」セクションに入力します。

1. B2B 注文のデフォルトの支払い方法を設定するには、 **[!UICONTROL Applicable Payment Methods]** を次のいずれかに変更します。

   - `All Payment Methods`

   - `Selected Payment Methods`

     特定のオプションの場合、 **[!UICONTROL Payment Methods]** Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックすると、顧客が利用できるようになります。

   次のリスト： [支払い方法](../configuration-reference/sales/payment-methods.md) は、ストアで現在有効または無効になっているオプションを示します。 標準の支払い方法に加え、リストには次のものも含まれます。

   - 支払い情報は不要です
   - [アカウントでの支払い](#configure-payment-on-account)
   - 保存済みアカウント
   - 保存済みカード

   ![B2B 構成 — デフォルトの支払い方法設定](./assets/b2b-features-default-payment-methods.png){width="600"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default B2B Shipping Methods]** 」セクションに入力します。

1. B2B 注文のデフォルトの発送方法を指定するには、 **[!UICONTROL Applicable Shipping Methods]** を次のいずれかに変更します。

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     特定のオプションの場合、 **[!UICONTROL Shipping Methods]** Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックすると、顧客が利用できるようになります。

     配送方法のリストには、現在の配送方法が表示されます [有効/無効](../configuration-reference/sales/delivery-methods.md).

   ![B2B 設定 — デフォルトの発送方法](./assets/b2b-features-shipping-methods.png){width="600"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 会社の電子メールオプションを設定する

The [営業担当者](account-company-manage.md#assign-a-sales-representative) 会社の主要連絡先として割り当てられる電子メールメッセージは、会社に送信される多数の自動電子メールメッセージの送信者としてデフォルトで設定されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Company Configuration]**.

1. 必要に応じて、 **[!UICONTROL Store View]** をストア表示に追加して、 [範囲](../getting-started/websites-stores-views.md#scope-settings) 設定の。

1. 次を完了： **[!UICONTROL Company Registration]** セクション：

   >[!NOTE]
   >
   >次をクリア： **[!UICONTROL Use system value]** チェックボックスをオンにして、フィールドを編集可能にします。

   - 設定 **[!UICONTROL Company Registration Email Recipient]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) 新しい会社登録要求を受け取ったときに通知を受け取るユーザー。

   - の場合 **[!UICONTROL Send Company Registration Email Copy To]**「 」に、登録通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - デフォルトの代わりに使用する電子メールテンプレートを準備した場合は、 **[!UICONTROL Default Company Registration Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Registration Request` テンプレートが使用されます。

     ![顧客の設定 — 会社の登録](./assets/company-email-options-company-registration.png){width="600"}

1. 次を完了： **[!UICONTROL Customer-Related Emails]** セクション：

   デフォルトの代わりに使用する代替の電子メールテンプレートを準備した場合、次の各項目に使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![顧客設定 — 顧客関連の E メール](./assets/company-email-options-customer-related-emails.png){width="600"}

1. 次を完了： **[!UICONTROL Company Status Change]** セクション：

   - の場合 **[!UICONTROL Send Company Status Change Email Copy To]**「 」で、ステータス変更通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - 会社のステータスが次の条件から変わったときに使用する電子メールテンプレートを準備している場合 `Pending Approval` から `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが次の条件から変わったときに使用する電子メールテンプレートを準備している場合 `Rejected` または `Blocked` から `Active`，設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「 `Rejected`，設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「 `Blocked`，設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「 `Pending Approval`，設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** をテンプレートの名前に追加します。 デフォルトでは、 `Company Status Pending Approval` テンプレートが使用されます。

   ![顧客の設定 — 会社のステータスの変更](./assets/company-email-options-company-status-change.png){width="600"}

1. 次を完了： **[!UICONTROL Company Credit Emails]** セクション：

   - 設定 **[!UICONTROL Company Credit Change Email Sender]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses) 会社に割り当てられているクレジット制限に変更が加えられた場合に通知を受け取るユーザー。 デフォルトでは、通知は _セールス担当者_.

   - の場合 **[!UICONTROL Send Company Credit Change Email Copy To]**「 」に、クレジット変更通知のコピーを受け取る各人の電子メールアドレスを入力します。 複数の電子メールアドレスはコンマで区切ります。

   - 通知のコピーを送信する方法を決定するには、 **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
      - `Separate Email`  — コピーを別の E メールとして送信します。

   - デフォルトの代わりに使用する電子メールテンプレートを準備した場合は、会社の管理者に送信される次の各通知のテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![顧客の設定 — 会社のクレジットメール](./assets/company-email-options-company-credit.png){width="600"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## オーダーの承認を設定

注文処理と発注を追跡する機能により、会社管理者は会社の購入者のアクションを制御できます。 注文の承認機能は、店舗管理者が発注書機能を有効にしている場合に使用できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL General]** を選択します。 **[!UICONTROL B2B Features]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order Approval Configuration]** 」セクションに入力します。

   ![注文の承認設定](./assets/b2b-features-order-approval.png){width="600"}

1. 会社が独自の発注書を作成できるようにするには、 **[!UICONTROL Enable Purchase Orders]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

   発注書機能は、Web サイトレベルで有効になります。 会社に対してこのタイプの注文を有効にするには、各 [会社プロファイル](account-company-manage.md).

## 発注書の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. リスト内の会社を検索し、 **[!UICONTROL Edit]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable Purchase Orders]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save]**.

有効化後、 **[!UICONTROL Approval Rules]** セクションがストアフロントに表示されます。 [アカウントダッシュボード](../customers/account-dashboard.md) （会社管理者用）

>[!NOTE]
>
>ストアフロントでの発注書アクセス権は、会社管理者が [会社のユーザーロールの権限](account-company-roles-permissions.md).

## アカウントでの支払いの設定

「アカウントでの支払い」は、企業がプロファイルで指定されているクレジット制限まで購入できるオフラインの支払い方法です。 アカウントでの支払いは、グローバルに、または会社ごとに有効にでき、有効な場合にのみチェックアウト時に表示されます。 条件 _アカウントでの支払い_ が支払い方法として使用される場合、注文の先頭に、アカウントのステータスを示すメッセージが表示されます。 特定の会社に対してこの支払い方法を設定するには、 [会社アカウントの管理](account-company-manage.md).

>[!NOTE]
>
>アカウントでの支払いは、次の条件を持つ注文ではサポートされていません： [複数の配送先住所](../stores-purchase/shipping-settings.md#multiple-addresses) およびは、これらの注文の支払いオプションには表示されません。

ストアの「アカウントでの支払い」を有効にするには、次の手順に従います。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Payment on Account]** 」セクションに入力します。

   ![アカウントでの支払い](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスを使用して、これらの設定を変更できます。

1. アカウントでの支払いを許可するには、 **[!UICONTROL Enabled]** から `Yes`.

1. を入力します。 **[!UICONTROL Title]** を使用して、チェックアウト時に支払い方法を識別するか、 `Payment on Account` デフォルトのタイトル。

1. 注文が通常承認を待つ場合は、デフォルトを受け入れます **[!UICONTROL New Order Status]** as `Pending` 承認されるまで

   必要に応じて、 `Processing` または `Suspected Fraud` この支払い方法での新規注文のステータス。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** をこの支払い方法に適合するために必要な注文金額に設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間にあるか、または完全に一致する場合に認定されます。

1. を入力します。 **[!UICONTROL Sort Order]** チェックアウト時に表示される支払い方法のリストで、この項目の位置を設定する数。

   値は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 完了したら、「 **[!UICONTROL Save Config]**.
