---
title: 顧客プロファイルの更新
description: 顧客が最後にアカウントにログインした日時やアカウントからログアウトした日時など、顧客アクティビティに関する情報にアクセスして、顧客プロファイルを更新します。
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# 顧客プロファイルの更新

_[!UICONTROL Customer Information]_&#x200B;ページの左側のパネルには、顧客のアクティビティ、住所、注文統計、最近の注文、買い物かごの内容、製品のレビュー、ニュースレターの購読に関する情報が含まれています。

![ 顧客プロファイル ](assets/cust-profile.png){width="700" zoomable="yes"}

## 顧客アカウントの編集

方法 1:**_クイック編集_**

1. 最初の列で、編集する顧客アカウントのチェックボックスを選択します。

1. **[!UICONTROL Actions]** 列を `Edit` に設定します。

   >[!INFO]
   >
   >更新できる各値の値がテキストボックスに表示されます。 選択した顧客レコードの一部の値のみをグリッドから編集できます。

   ![ クイック編集 ](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. 必要に応じて、次のいずれかの値を更新します。

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. 「**[!UICONTROL Save]**」をクリックします。

方法 2:**_完全編集_**

1. グリッドで、編集する顧客レコードを見つけます。

1. 右端の _アクション_ 列で、「**[!UICONTROL Edit]**」をクリックします。

1. 会社情報に対して必要な変更を行います。

   >[!INFO]
   >
   >詳しくは、[ 顧客プロファイルの更新 ](../customers/update-account.md) を参照してください。

1. 完了したら、「**[!UICONTROL Save Customer]**」をクリックします。

>[!INFO]
>
>保存前にすべての編集を元に戻す場合は、上部のボタンバーの **[!UICONTROL Reset]** をクリックして、最後に保存したバージョンにすべての変更を戻します。

## 顧客情報

### [!UICONTROL Customer View]

_顧客表示_ タブには、**[!UICONTROL Personal Information]**、**[!UICONTROL Reward Points Balance]**、**[!UICONTROL Store Credit Balance]** など、顧客に関する情報が一覧表示されます。

### [!UICONTROL Account Information]

「[ アカウント情報 ](../customers/account-dashboard-account-information.md)」タブには、管理者ユーザーが個人情報、メール、リモートショッピングアシスタンス、生年月日を編集したり、web サイトや会社に顧客を添付したりできる、顧客に関する詳細情報が表示されます。

### [!UICONTROL Addresses]

[ アドレス ](../customers/account-dashboard-address-book.md) タブには、顧客のデフォルトの請求先住所と配送先住所、およびそれらが頻繁に使用する追加の住所が含まれています。

### [!UICONTROL Orders]

[ 注文 ](../stores-purchase/orders.md) グリッドには、現在のすべての顧客の注文のリストが含まれており、管理者は注文の進行状況を追跡できます。

### [!UICONTROL Returns]

{{ee-feature}}

「[Returns](../stores-purchase/returns.md)」タブには、現在の返された顧客リクエストがリストされます。

### [!UICONTROL Shopping cart]

「[ 買い物かご ](../stores-purchase/cart.md)」タブには、現在カートに入っているが何らかの理由で購入が完了しなかった製品が表示されます。

### [!UICONTROL Wish List]

[ ウィッシュリスト ](../stores-purchase/wishlists.md) には、顧客が後で買い物かごに転送できる製品のリストが表示されます。

### [!UICONTROL Gift Registry]

{{ee-feature}}

[ ギフトレジストリ ](../merchandising-promotions/gift-registry-storefront.md) セクションには、顧客の現在のギフトレジストリと関連するイベントが一覧表示されます。


### [!UICONTROL Store Credit]

{{ee-feature}}

[ ストアクレジット ](../customers/store-credit.md) タブには、顧客アカウントに復元された金額が表示されます。管理者はこの値を管理できます。

### [!UICONTROL Newsletter]

「[ ニュースレター ](../merchandising-promotions/newsletters.md)」タブには、現在の顧客に送信されたすべてのメールが表示されます。

### [!UICONTROL Billing Agreements]

[ 請求契約 ](../stores-purchase/paypal-billing-agreements.md) タブには、ストアとお客様の間のすべての PayPal 請求契約が一覧表示されます。

### [!UICONTROL Product Reviews]

[ 製品レビュー ](../catalog/settings-advanced-product-reviews.md) タブには、この顧客が送信したすべてのレビューが表示されます。

### [!UICONTROL Reward Points]

{{ee-feature}}

[ 報酬ポイント ](../merchandising-promotions/rewards-loyalty.md) セクションには、顧客の現在の報酬ポイント残高が表示されます。 管理者ユーザーはこの値を管理できます。

## ボタンバー

| ボタン | 説明 |
|----------|--------------|
| **[!UICONTROL Back]** | 変更を保存せずに顧客ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | マーチャントが顧客としてログインする機能を許可します。 |
| **[!UICONTROL Delete Customer]** | 顧客アカウントを削除します。 |
| **[!UICONTROL Reset]** | 顧客フォーム内の未保存の変更をすべて以前の値にリセットします。 |
| **[!UICONTROL Create Order]** | 顧客 ID に関連付けられた [ 注文を作成します ](../stores-purchase/customer-account-create-order.md)。 |
| **[!UICONTROL Reset Password]** | 顧客のパスワードをリセットします。 |
| **[!UICONTROL Force Sign-In]** | 顧客のパスワードに関連付けられたトークンをクリアし、管理者にアカウントへのアクセスを提供します。 |
| **[!UICONTROL Manage Shopping Cart]** | 顧客の買い物かごへのアクセスを提供します。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客アカウントを開いたままにします。 |
| **[!UICONTROL Save Customer]** | 変更を保存し、顧客アカウントを閉じます。 |

{style="table-layout:auto"}
