---
title: 買い物客への支援の提供
description: 「顧客としてログイン」機能を使用すると、顧客に表示される内容を確認し、顧客に代わって更新を行うことができます。
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 買い物客への支援の提供

顧客は注文に関するヘルプが必要になる場合があります。 ストア管理者は _顧客としてログイン_ を使用できます。これにより、顧客に対して表示される内容を確認し、更新を行って支援することができます。

ユーザーとしてログインした際に実行されたすべてのアクションは、実際のお客様のアカウントに適用されます。

_管理者_ ユーザーに対して有効になっている場合は、_[!UICONTROL Login as Customer]_&#x200B;のボタンが複数のページに表示されます。

* [顧客編集ページ](../customers/update-account.md)
* [注文ビューページ](../stores-purchase/order-processing.md)
* [「請求書ビュー」ページ](../stores-purchase/invoices.md)
* [「出荷ビュー」ページ](../stores-purchase/shipments.md)
* [「クレジット・メモ表示」ページ](../stores-purchase/credit-memo-create.md)

![&#x200B; 顧客としてログイン &#x200B;](assets/login-as-customer.png){width="600" zoomable="yes"}

## 顧客としてログインを有効にする

_顧客としてログイン_ を有効にするには、Commerce インスタンスでその機能を有効にし、ユーザーロール権限で管理者ユーザーのアクセスを有効にする必要があります。

### 機能の有効化

1. 管理者サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Login as Customer]**」を選択します。

   ![&#x200B; 設定オプション – 顧客としてログイン &#x200B;](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Login as Customer]** を `Yes` に設定します。

1. _（オプション）_ 管理者ユーザーが顧客としてログインした際にページキャッシュを有効にするには、**[!UICONTROL Disable Page Cache for Admin User]** を `No` に設定します。

   >[!WARNING]
   >
   > ページキャッシュを無効にする（`Yes` - デフォルト）と、ユーザーとしてログインした際に、キャッシュされていない新しいデータが確実に取得されます。

1. _（オプション）_ マルチサイトまたはマルチストアの設定があり、管理者ユーザーが顧客としてログインした際にストア表示を選択する場合は、**[!UICONTROL Store View to Log in]** を `Manual Selection` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

### 管理者ユーザーのアクセスを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_権限_/**[!UICONTROL User Roles]** に移動します。

1. リストで役割をクリックします。

1. [!UICONTROL _役割情報_] 左側のパネルで、「**[!UICONTROL Role Resources]**」をクリックします。

1. ページの **[!UICONTROL Role Resources]** を `Custom` に変更します。

   >[!INFO]
   >
   > このオプションを選択すると、リソース階層がページに表示されます。

1. **[!UICONTROL Customers]** の親項目とその下の **[!UICONTROL Login as Customer]** の項目までスクロールします。 次に、役割に対して有効にするリソースを選択します。

   * **[!UICONTROL Allow Login as Customer]** – 管理者ユーザーが _顧客としてログイン_ 機能を使用できるようにします。
   * **[!UICONTROL View Login as Customer Log]** – 管理者ユーザーに _顧客としてログイン_ ログを表示することを許可します。

   ![&#x200B; 役割のリソース – 顧客としてログイン &#x200B;](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 「**[!UICONTROL Save Role]**」をクリックします。

## 管理者から顧客としてログインします

1. _管理者_ サイドバーで、**[!UICONTROL Customers]**/[!UICONTROL _すべての顧客_] に移動します。

1. ユーザーを編集モードで開きます。

1. **[!UICONTROL Customer Information]** パネルで、「**[!UICONTROL Account Information]**」セクションを選択します。

1. **[!UICONTROL Allow remote shopping assistance]** を `Yes` に設定します。

   >[!INFO]
   >
   >管理者は、ストアフロントからの許可なしでユーザーとしてログインできるようになりました。

## リモート ショッピング アシスタンスの顧客アカウント権限

管理者がストアサポートスタッフのアカウントアクセスを有効にするには、お客様は自分のアカウントでこの機能を有効にする必要があります。

1. お客様は **[!UICONTROL Account Information]** のページに移動します。

1. **[!UICONTROL Allow remote shopping assistance]** チェックボックスを選択します。

1. 顧客は「**[!UICONTROL Save]**」をクリックします。

![&#x200B; アカウント情報ページ &#x200B;](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>この権限がない場合、管理者ユーザーはこの顧客としてログインできません。

## 顧客としてログインを使用

>[!INFO]
>
>_顧客としてログイン_ を使用するには、管理者が前述のように設定されていることを確認してください。

_顧客としてログイン_ すると、顧客と同じようにサイトを表示でき、トラブルシューティングを行ったり、顧客に対して他のアクションを実行したりできます。 必要な権限を持つユーザーの役割が割り当てられている場合：

1. 前の節で一覧表示したページで「**[!UICONTROL Login as Customer]**」をクリックできます。
1. 「顧客としてログイン」アクションは、「アクション」レポートで使用できます。

>[!WARNING]
>
>[!UICONTROL _顧客として_] ログイン中に実行されたアクション（製品の追加/削除など）は、実際の顧客の注文に適用されます。 ストアフロントでは、特別な状態を `logged in as customer_name` 示するバナーが表示されます。

## カスタマーログとしてログイン

{{ee-feature}}

Adobe Commerceには、「顧客としてログイン _アクションのログが用意されて_ ます。 管理者ユーザーが機能にアクセスするすべてのセッションが一覧表示されます。 ログに記録されたアクションにアクセスするには、[&#x200B; 管理者アクションレポート &#x200B;](../systems/action-log-report.md) に移動します。

レポート設定 **[!UICONTROL Action Group]** をフィルタリングして、ページの上部にある `Login As Customer` をクリック **[!UICONTROL Search]** きます。

![&#x200B; アクションレポートのフィルタリング &#x200B;](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
