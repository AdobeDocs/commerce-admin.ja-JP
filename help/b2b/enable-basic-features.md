---
title: B2B 機能の有効化
description: 会社アカウント、デフォルトの支払方法と発送方法、発注書、注文承認など、Adobe Commerce ストアの B2B 機能を有効にする方法について説明します。
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '1635'
ht-degree: 0%

---

# B2B 機能の有効化

デフォルトでは、すべての B2B 機能は最初は無効になっています。 ストア管理者は、Commerce ストアで必要に応じて、B2B 機能を有効または無効にすることができます。 B2B 設定の完全なリストについては、[B2B 機能の設定リファレンス ](../configuration-reference/general/b2b-features.md) を参照してください。

顧客企業のサポートを有効にすると、追加の B2B 機能が自動的に有効になります。

- [[!DNL Shared Catalog]](catalog-shared.md)

  では、様々な会社のカスタム価格設定をサポートしており、すべての店舗に対してカテゴリ権限も有効にします。

- [!DNL Enable Shared Catalog direct products price assigning]

  共有カタログに割り当てられた製品のみを価格インデックスに保存することで、サイトのパフォーマンスを向上させます。 この機能を有効にすることは、多くの共有カタログを持つマーチャントにとって、様々な企業のカスタム価格を管理するためのベストプラクティスです。

- [[!DNL B2B Quotes]](quotes.md)

  売り手と会社の買い手に価格を交渉する機能を提供します。

- [!DNL B2B default payment and shipping methods]

  ストアフロントで B2B 購入者が使用できる支払いと配送オプションの選択を決定します。

これらの機能の設定は、[!DNL Enable Company] が `Yes` に設定されている場合にのみ表示されます。

B2B の [[!DNL Quick Order]](quick-order.md) 機能と [[!DNL Requisition List]](requisition-lists.md) 機能は、個別に有効または無効にできます。

## B2B 機能の設定

Adobe Commerce B2B 機能を設定するオプションは、[Adobe Commerce B2B 拡張機能がインストールされているCommerce プロジェクトでのみ使用でき ](install.md) す。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

   マルチサイトインストールを使用している場合は、左上隅の **[!UICONTROL Store View]** コントロールを設定が適用される Web サイトに設定します。

1. _[!UICONTROL General]_&#x200B;の下の左パネルで、「**[!UICONTROL B2B Features]**」を選択します。

   ![B2B 設定 – 一般 ](./assets/b2b-features.png){width="600"}

   - **[!UICONTROL Enable Company]** を `Yes` に設定することで、顧客が独自の会社アカウントを管理し、追加の B2B 機能のサポートを有効にできるようにします。

     会社サポートを有効にすると、共有カタログ、B2B 見積もり、B2B 支払い方法、B2B 配送方法が自動的に有効になります。

     ![B2B の設定 – 会社の機能 ](assets/b2b-additional-features.png){width="600"}

   - 顧客やゲストが SKU や製品名に基づいてすばやく注文できるようにするには、**[!UICONTROL Enable Quick Order]** を `Yes` に設定します。

   - 顧客が自分のアカウント・ダッシュボードから購買依頼リストを作成および管理できるようにするには、**[!UICONTROL Enable Requisition List]** を `Yes` に設定します。

     また、顧客が自分のアカウントに持つことができる [ リストの最大数を設定する ](configure-requisition-lists.md) こともできます。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## デフォルトの B2B 支払および発送方法の設定

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Default B2B Payment Methods]**」セクションを展開します。

1. B2B 注文のデフォルトの支払い方法を設定するには、**[!UICONTROL Applicable Payment Methods]** を次のいずれかに設定します。

   - `All Payment Methods`

   - `Selected Payment Methods`

     Ctrl キー（PC）または Command キー（Mac）を押しながら各オプションをクリックして、顧客が使用できる **[!UICONTROL Payment Methods]** を選択します。

   [ 支払い方法 ](../configuration-reference/sales/payment-methods.md) のリストには、ストアで現在有効または無効になっているオプションが表示されます。 リストには、標準の支払い方法に加えて、次の項目も含まれています。

   - 支払い情報は必要ありません
   - [分割払い](#configure-payment-on-account)
   - 保存済みアカウント
   - 保存されたカード

   ![B2B 設定 – デフォルトの支払方法設定 ](./assets/b2b-features-default-payment-methods.png){width="600"}

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Default B2B Shipping Methods]**」セクションを展開します。

1. B2B 注文のデフォルトの出荷方法を指定するには、**[!UICONTROL Applicable Shipping Methods]** を次のいずれかに設定します。

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Ctrl キー（PC）または Command キー（Mac）を押しながら各オプションをクリックして、顧客が使用できる **[!UICONTROL Shipping Methods]** を選択します。

     発送方法のリストには、現在 [ 有効または無効 ](../configuration-reference/sales/delivery-methods.md) が表示されます。

   ![B2B 設定 – デフォルトの発送方法 ](./assets/b2b-features-shipping-methods.png){width="600"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 会社のメールオプションを設定

会社の主要連絡先として割り当てられた [ 営業担当者 ](account-company-manage.md#assign-a-sales-representative) は、デフォルトで、会社に送信される多くの自動メールメッセージの送信者として設定されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Company Configuration]**」を選択します。

1. 必要に応じて、**[!UICONTROL Store View]** をストア表示に設定して、設定の [ スコープ ](../getting-started/websites-stores-views.md#scope-settings) を定義します。

1. **[!UICONTROL Company Registration]** のセクションを完了します。

   >[!NOTE]
   >
   >フィールドを編集可能にするには、「**[!UICONTROL Use system value]**」チェックボックスをオフにします。

   - **[!UICONTROL Company Registration Email Recipient]** を、新しい会社登録要求を受信したときに通知される [ ストアの連絡先 ](../getting-started/store-details.md#store-email-addresses) に設定します。

   - **[!UICONTROL Send Company Registration Email Copy To]**：登録通知のコピーを受け取る各ユーザーのメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**Send Email Copy Method** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default Company Registration Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Registration Request` テンプレートが使用されます。

     ![ 顧客設定 – 会社登録 ](./assets/company-email-options-company-registration.png){width="600"}

1. **[!UICONTROL Customer-Related Emails]** のセクションを完了します。

   デフォルトの代わりに使用する代替電子メールテンプレートを準備している場合は、次のそれぞれに使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![ 顧客設定 – 顧客関連のメール ](./assets/company-email-options-customer-related-emails.png){width="600"}

1. **[!UICONTROL Company Status Change]** のセクションを完了します。

   - **[!UICONTROL Send Company Status Change Email Copy To]**: ステータス変更通知のコピーを受信する各担当者の電子メール・アドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**Send Email Copy Method** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - 会社のステータスが `Pending Approval` から `Active` に変更されたときに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default 'Company Status Change to Active 1' Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが「`Rejected`」または「`Blocked`」から「`Active`」に変更されたときに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default 'Company Status Change to Active 2' Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「`Rejected`」に変わるときに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default 'Company Status Change to Rejected' Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「`Blocked`」に変わるときに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default 'Company Status Change to Blocked' Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「`Pending Approval`」に変わるときに使用するメールテンプレートを準備した場合は、**[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** をテンプレートの名前に設定します。 デフォルトでは、`Company Status Pending Approval` テンプレートが使用されます。

   ![ 顧客の設定 – 会社ステータスの変更 ](./assets/company-email-options-company-status-change.png){width="600"}

1. **[!UICONTROL Company Credit Emails]** のセクションを完了します。

   - 会社に割り当てられているクレジット限度額に変更があったときに通知される [ ストア連絡先 ](../getting-started/store-details.md#store-email-addresses) に **[!UICONTROL Company Credit Change Email Sender]** を設定します。 デフォルトでは、通知は _営業担当者_ に送信されます。

   - **[!UICONTROL Send Company Credit Change Email Copy To]**：与信変更通知のコピーを受信する各担当者の電子メール・アドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、**Send Email Copy Method** を次のいずれかに設定します。

      - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを個別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、会社管理者に送信される次の各通知に対してテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![ 顧客設定 – 会社クレジットメール ](./assets/company-email-options-company-credit.png){width="600"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 注文の承認を設定

注文処理と発注書を追跡する機能により、会社管理者は会社の購入者の行動を制御できます。 注文承認機能は、店舗管理者が発注機能を有効にした場合に使用できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL General]**」を展開し、「**[!UICONTROL B2B Features]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Order Approval Configuration]**」セクションを展開します。

   ![ 注文承認の設定 ](./assets/b2b-features-order-approval.png){width="600"}

1. 会社が独自の発注書を作成できるようにするには、**[!UICONTROL Enable Purchase Orders]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   発注機能は web サイトレベルで有効になります。 会社に対してこのタイプの注文を有効にするには、各 [ 会社プロファイル ](account-company-manage.md) の適切な設定で同じ操作を行います。

## 発注書の構成

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/**[!UICONTROL Companies]** に移動します。

1. リストで会社を見つけて、「**[!UICONTROL Edit]**」をクリックします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Advanced Settings]**」セクションを展開します。

1. **[!UICONTROL Enable Purchase Orders]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save]**」をクリックします。

アクティブ化後、会社管理者の場合、ストアフロント [ アカウントダッシュボード ](../customers/account-dashboard.md) に「**[!UICONTROL Approval Rules]**」セクションが表示されます。

>[!NOTE]
>
>ストアフロントの発注書へのアクセスは、[ 会社のユーザーロールの権限 ](account-company-roles-permissions.md) に基づいて、会社の管理者から許可される必要があります。

## 分割払いの構成

アカウント内支払いは、企業がプロファイルで指定されたクレジット制限を超えない範囲で購入できるオフラインの支払い方法です。 アカウントでの支払いは、グローバルに、または会社ごとに有効化できます。有効化されている場合にのみ、チェックアウト時に表示されます。 支払い方法として _アカウントでの支払い_ が使用されている場合、注文の上部にアカウントのステータスを示すメッセージが表示されます。 特定の会社に対してこの支払い方法を設定するには、[ 会社アカウントの管理 ](account-company-manage.md) を参照してください。

>[!NOTE]
>
>アカウントでのお支払いは、[ 複数の配送先住所 ](../stores-purchase/shipping-settings.md#multiple-addresses) を含む注文ではサポートされておらず、これらの注文の支払いオプションには表示されません。

ストアでアカウント内支払いを有効にするには：

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Payment on Account]**」セクションを展開します。

   ![ 分割払 ](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >必要に応じて、まず「**[!UICONTROL Use system value]**」チェックボックスの選択を解除して、これらの設定を変更します。

1. 分割払いを許可するには、**[!UICONTROL Enabled]** を `Yes` に設定します。

1. チェックアウト時に支払い方法を識別する **[!UICONTROL Title]** を入力するか、`Payment on Account` のデフォルトのタイトルをそのまま使用します。

1. 注文が通常、承認を待つ場合は、承認されるまでデフォルト **[!UICONTROL New Order Status]** を `Pending` として受け入れます。

   必要に応じて、この支払い方法を使用して新しい注文の `Processing` または `Suspected Fraud` のステータスを使用できます。

1. **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. この支払い方法の対象として必要な注文金額に **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** を設定します。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. チェックアウト時に表示される支払い方法の一覧のこの項目の位置を設定する **[!UICONTROL Sort Order]** 番号を入力します。

   この値は、他の支払い方法を基準にしています。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
