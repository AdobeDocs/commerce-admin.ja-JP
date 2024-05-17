---
title: B2B 機能の有効化
description: 会社アカウント、デフォルトの支払方法と発送方法、発注書、注文承認など、Adobe Commerce ストアの B2B 機能を有効にする方法について説明します。
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# B2B 機能の有効化

デフォルトでは、すべての B2B 機能は最初は無効になっています。 ストア管理者は、Commerce ストアで必要に応じて、B2B 機能を有効または無効にすることができます。 B2B 設定の完全なリストについては、を参照してください。 [B2B 機能の設定リファレンス](../configuration-reference/general/b2b-features.md).

顧客企業のサポートを有効にすると、追加の B2B 機能が自動的に有効になります。

- [!DNL Shared Catalog]

  では、様々な会社のカスタム価格設定をサポートしており、すべての店舗に対してカテゴリ権限も有効にします。

- [!DNL Enable Shared Catalog direct products price assigning]

  共有カタログに割り当てられた製品のみを価格インデックスに保存することで、サイトのパフォーマンスを向上させます。 この機能を有効にすることは、多くの共有カタログを持つマーチャントにとって、様々な企業のカスタム価格を管理するためのベストプラクティスです。

- [!DNL B2B Quotes]

  売り手と会社の買い手に価格を交渉する機能を提供します。

- [!DNL B2B default payment and shipping methods]

  ストアフロントで B2B 購入者が使用できる支払いと配送オプションの選択を決定します。

これらの機能の設定は、の場合にのみ表示されます [!DNL Enable Company] はに設定されています。 `Yes`.

B2B [!DNL Quick Order] および [!DNL Requisition List] 機能は、個別に有効または無効にできます。

## B2B 機能の設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   マルチサイトインストールの場合は、 **[!UICONTROL Store View]** 設定が適用される web サイトの左上隅にあるコントロール。

1. の下の左パネルで _[!UICONTROL General]_、を選択&#x200B;**[!UICONTROL B2B Features]**:

   ![B2B 設定 – 一般](./assets/b2b-features.png){width="600"}

   - を設定して、顧客が独自の会社アカウントを管理し、追加の B2B 機能のサポートを有効にできるようにします **[!UICONTROL Enable Company]**  対象： `Yes`.

     会社サポートを有効にすると、共有カタログ、B2B 見積もり、B2B 支払い方法、B2B 配送方法が自動的に有効になります。

   - 顧客およびゲストが SKU または製品名に基づいてすばやく注文できるようにするには、次のように設定します **[!UICONTROL Enable Quick Order]** 対象： `Yes`.

   - 顧客が自分のアカウント・ダッシュボードから購買依頼リストを作成および管理できるようにするには、次のように設定します。 **[!UICONTROL Enable Requisition List]** 対象： `Yes`.

     以下の手順でも可能です [リストの最大数の設定](configure-requisition-lists.md) 顧客は、のアカウントにを持つことができます。

1. 完了したら、 **[!UICONTROL Save Config]**.

## デフォルトの B2B 支払および発送方法の設定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Default B2B Payment Methods]** セクション。

1. B2B 注文のデフォルトの支払方法を設定するには、次のように設定します **[!UICONTROL Applicable Payment Methods]** を次のいずれかに変更します。

   - `All Payment Methods`

   - `Selected Payment Methods`

     特定のオプションの場合は、 **[!UICONTROL Payment Methods]** ctrl キー（PC）または Command キー（Mac）を押しながら各オプションをクリックすることにより、顧客が利用できるようにする場合。

   のリスト [支払い方法](../configuration-reference/sales/payment-methods.md) ストアで現在有効または無効になっているオプションを表示します。 リストには、標準の支払い方法に加えて、次の項目も含まれています。

   - 支払い情報は必要ありません
   - [分割払い](#configure-payment-on-account)
   - 保存済みアカウント
   - 保存されたカード

   ![B2B 設定 – デフォルトの支払方法設定](./assets/b2b-features-default-payment-methods.png){width="600"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Default B2B Shipping Methods]** セクション。

1. B2B 注文のデフォルトの出荷方法を指定するには、次のように設定します **[!UICONTROL Applicable Shipping Methods]** を次のいずれかに変更します。

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     特定のオプションの場合は、 **[!UICONTROL Shipping Methods]** ctrl キー（PC）または Command キー（Mac）を押しながら各オプションをクリックすることにより、顧客が利用できるようにする場合。

     発送方法のリストには、現在の発送方法が表示されます [有効または無効](../configuration-reference/sales/delivery-methods.md).

   ![B2B 設定 – デフォルトの発送方法](./assets/b2b-features-shipping-methods.png){width="600"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## 会社のメールオプションを設定

この [営業担当者](account-company-manage.md#assign-a-sales-representative) 会社のプライマリ連絡先として割り当てられた連絡先は、会社に送信される多数の自動メールメッセージの送信者としてデフォルトで設定されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Company Configuration]**.

1. 必要に応じて、を設定します **[!UICONTROL Store View]** をストア表示に追加して定義します。 [範囲](../getting-started/websites-stores-views.md#scope-settings) ：設定。

1. を完了する **[!UICONTROL Company Registration]** セクション：

   >[!NOTE]
   >
   >をクリア **[!UICONTROL Use system value]** フィールドを編集可能にするチェックボックス。

   - を設定 **[!UICONTROL Company Registration Email Recipient]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) 新しい会社登録要求を受信したときに通知されるユーザー。

   - の場合 **[!UICONTROL Send Company Registration Email Copy To]**&#x200B;に、登録通知のコピーを受け取る各ユーザーのメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、を設定します **[!UICONTROL Default Company Registration Email]** ：テンプレートの名前。 デフォルトでは、 `Company Registration Request` テンプレートが使用されます。

     ![顧客設定 – 会社登録](./assets/company-email-options-company-registration.png){width="600"}

1. を完了する **[!UICONTROL Customer-Related Emails]** セクション：

   デフォルトの代わりに使用する代替電子メールテンプレートを準備している場合は、次のそれぞれに使用するテンプレートを選択します。

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![顧客設定 – 顧客関連のメール](./assets/company-email-options-customer-related-emails.png){width="600"}

1. を完了する **[!UICONTROL Company Status Change]** セクション：

   - の場合 **[!UICONTROL Send Company Status Change Email Copy To]**&#x200B;に、ステータス変更通知のコピーを受け取る各ユーザーのメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - 会社のステータスが次から変更されたときに使用するメールテンプレートを準備している場合： `Pending Approval` 対象： `Active`、設定 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** ：テンプレートの名前。 デフォルトでは、 `Company Status Active 1` テンプレートが使用されます。

   - 会社のステータスが次から変更されたときに使用するメールテンプレートを準備している場合： `Rejected` または `Blocked` 対象： `Active`、設定 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** ：テンプレートの名前。 デフォルトでは、 `Company Status Active 2` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合に使用するメールテンプレートを準備している場合 `Rejected`、設定 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** ：テンプレートの名前。 デフォルトでは、 `Company Status Rejected` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合に使用するメールテンプレートを準備している場合 `Blocked`、設定 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** ：テンプレートの名前。 デフォルトでは、 `Company Status Blocked` テンプレートが使用されます。

   - 会社のステータスが「」に変更された場合に使用するメールテンプレートを準備している場合 `Pending Approval`、設定 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** ：テンプレートの名前。 デフォルトでは、 `Company Status Pending Approval` テンプレートが使用されます。

   ![顧客の設定 – 会社ステータスの変更](./assets/company-email-options-company-status-change.png){width="600"}

1. を完了する **[!UICONTROL Company Credit Emails]** セクション：

   - を設定 **[!UICONTROL Company Credit Change Email Sender]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) 会社に割り当てられた与信限度額を変更した際に通知されるユーザー。 デフォルトでは、通知はに送信されます。 _営業担当者_.

   - の場合 **[!UICONTROL Send Company Credit Change Email Copy To]**&#x200B;に、クレジット変更通知のコピーを受信する各ユーザーのメールアドレスを入力します。 複数のメールアドレスを指定する場合はコンマで区切ります。

   - 通知のコピーの送信方法を決定するには、次のように設定します **Send Email Copy メソッド** を次のいずれかに変更します。

      - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
      - `Separate Email` - コピーを別のメールとして送信します。

   - デフォルトの代わりに使用するメールテンプレートを準備している場合は、会社管理者に送信される次の各通知に対してテンプレートを選択します。

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![顧客設定 – 会社のクレジットメール](./assets/company-email-options-company-credit.png){width="600"}

1. 完了したら、 **[!UICONTROL Save Config]**.

## 注文の承認を設定

注文処理と発注書を追跡する機能により、会社管理者は会社の購入者の行動を制御できます。 注文承認機能は、店舗管理者が発注機能を有効にした場合に使用できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL General]** を選択します **[!UICONTROL B2B Features]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order Approval Configuration]** セクション。

   ![注文の承認設定](./assets/b2b-features-order-approval.png){width="600"}

1. 会社が独自の発注書を作成できるようにするには、次のように設定します **[!UICONTROL Enable Purchase Orders]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

   発注機能は web サイトレベルで有効になります。 会社に対してこのタイプの注文を有効にするには、それぞれに適切な設定で同じ操作を行います [会社概要](account-company-manage.md).

## 発注書の構成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. リストで会社を見つけて、 **[!UICONTROL Edit]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

1. を設定 **[!UICONTROL Enable Purchase Orders]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save]**.

アクティブ化後、 **[!UICONTROL Approval Rules]** セクションはストアフロントに表示されます [Account Dashboard](../customers/account-dashboard.md) 会社の管理者の場合。

>[!NOTE]
>
>ストアフロントの発注書へのアクセスは、次に基づいて、会社の管理者から許可される必要があります [会社ユーザーの役割の権限](account-company-roles-permissions.md).

## 分割払いの構成

アカウント内支払いは、企業がプロファイルで指定されたクレジット制限を超えない範囲で購入できるオフラインの支払い方法です。 アカウントでの支払いは、グローバルに、または会社ごとに有効化できます。有効化されている場合にのみ、チェックアウト時に表示されます。 条件 _分割払い_ を支払方法として使用すると、注文の上部に、アカウントのステータスを示すメッセージが表示されます。 特定の会社に対してこの支払い方法を設定するには、次を参照してください。 [会社アカウントの管理](account-company-manage.md).

>[!NOTE]
>
>での注文については、分割払いはサポートされていません。 [複数の配送先住所](../stores-purchase/shipping-settings.md#multiple-addresses) およびは、これらの注文の支払いオプションの中には表示されません。

ストアでアカウント内支払いを有効にするには：

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Payment on Account]** セクション。

   ![分割払い](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** これらの設定を変更するチェックボックス。

1. 分割払いを許可するには、次のように設定します **[!UICONTROL Enabled]** 対象： `Yes`.

1. を入力 **[!UICONTROL Title]** チェックアウト時に支払い方法を識別します。または、 `Payment on Account` デフォルトのタイトル。

1. 注文が通常、承認を待つ場合は、デフォルトのを使用します **[!UICONTROL New Order Status]** as `Pending` 承認されるまで。

   必要に応じて、を使用できます `Processing` または `Suspected Fraud` この支払い方法を使用する新しい注文のステータス。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. を設定 **[!UICONTROL Minimum Order Total]** および **[!UICONTROL Maximum Order Total]** ご注文の金額は、この支払い方法の対象として必要です。

   >[!NOTE]
   >
   >注文は、合計が最小値と最大値の間に収まる、または完全に一致する場合に該当します。

1. を入力 **[!UICONTROL Sort Order]** チェックアウト時に表示される支払い方法の一覧で、この項目の位置を設定する数値です。

   この値は、他の支払い方法を基準にしています。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. 完了したら、 **[!UICONTROL Save Config]**.
