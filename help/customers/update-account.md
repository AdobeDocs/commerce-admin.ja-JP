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

の左パネル _[!UICONTROL Customer Information]_このページには、顧客のアクティビティ、住所、注文統計、最近の注文、買い物かごの内容、製品のレビュー、ニュースレターの購読に関する情報が含まれています。

![顧客プロファイル](assets/cust-profile.png){width="700" zoomable="yes"}

## 顧客アカウントの編集

メソッド 1: **_クイック編集_**

1. 最初の列で、編集する顧客アカウントのチェックボックスを選択します。

1. を **[!UICONTROL Actions]** 列を `Edit`.

   >[!INFO]
   >
   >更新できる各値の値がテキストボックスに表示されます。 選択した顧客レコードの一部の値のみをグリッドから編集できます。

   ![クイック編集](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. 必要に応じて、次のいずれかの値を更新します。

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. クリック **[!UICONTROL Save]**.

メソッド 2: **_完全編集_**

1. グリッドで、編集する顧客レコードを見つけます。

1. が含まれる _アクション_ 右端のをクリックします。 **[!UICONTROL Edit]**.

1. 会社情報に対して必要な変更を行います。

   >[!INFO]
   >
   >詳しくは、 [顧客プロファイルの更新](../customers/update-account.md).

1. 完了したら、 **[!UICONTROL Save Customer]**.

>[!INFO]
>
>保存前にすべての編集を元に戻すには、をクリックします **[!UICONTROL Reset]** をクリックし、最後に保存されたバージョンに対するすべての変更を返します。

## 顧客情報

### [!UICONTROL Customer View]

この _顧客ビュー_ タブには、顧客に関する情報（次を含む）が一覧表示されます **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]**、および **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

この [アカウント情報](../customers/account-dashboard-account-information.md) タブには、管理者ユーザーが個人情報、メール、リモートショッピングアシスタンス、生年月日を編集したり、web サイトまたは会社に顧客を添付したりできる、顧客に関する詳細情報が表示されます。

### [!UICONTROL Addresses]

この [アドレス](../customers/account-dashboard-address-book.md) タブには、顧客のデフォルトの請求先住所と配送先住所、およびそれらが頻繁に使用する追加の住所が含まれています。

### [!UICONTROL Orders]

この [注文件数](../stores-purchase/orders.md) グリッドには、現在のすべての顧客の注文のリストが含まれており、管理者は注文の進行状況を追跡できます。

### [!UICONTROL Returns]

{{ee-feature}}

この [戻り値](../stores-purchase/returns.md) タブには、現在の返された顧客リクエストが一覧表示されます。

### [!UICONTROL Shopping cart]

この [ショッピングカート](../stores-purchase/cart.md) tab キーを押すと、買い物かごに現在入っている商品が表示されますが、何らかの理由で購入が完了しませんでした。

### [!UICONTROL Wish List]

A [ウィッシュリスト](../stores-purchase/wishlists.md) 顧客が後で買い物かごに転送できる商品のリストを表示します。

### [!UICONTROL Gift Registry]

{{ee-feature}}

この [ギフト レジストリ](../merchandising-promotions/gift-registry-storefront.md) セクションには、顧客の現在のギフトレジストリと関連するイベントが一覧表示されます。


### [!UICONTROL Store Credit]

{{ee-feature}}

この [ストアクレジット](../customers/store-credit.md) タブには、顧客アカウントに復元された金額が表示されます。管理者はこの値を管理できます。

### [!UICONTROL Newsletter]

この [ニュースレター](../merchandising-promotions/newsletters.md) tab キーを押すと、現在の顧客に送信されたすべてのメールが表示されます。

### [!UICONTROL Billing Agreements]

この [請求契約](../stores-purchase/paypal-billing-agreements.md) タブには、ストアとお客様の間のすべての PayPal 請求契約が一覧表示されます。

### [!UICONTROL Product Reviews]

この [製品レビュー](../catalog/settings-advanced-product-reviews.md) タブには、この顧客が送信したすべてのレビューが表示されます。

### [!UICONTROL Reward Points]

{{ee-feature}}

この [報酬ポイント](../merchandising-promotions/rewards-loyalty.md) セクションには、顧客の現在の報酬ポイント残高が表示されます。 管理者ユーザーはこの値を管理できます。

## ボタンバー

| ボタン | 説明 |
|----------|--------------|
| **[!UICONTROL Back]** | 変更を保存せずに顧客ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | マーチャントが顧客としてログインする機能を許可します。 |
| **[!UICONTROL Delete Customer]** | 顧客アカウントを削除します。 |
| **[!UICONTROL Reset]** | 顧客フォーム内の未保存の変更をすべて以前の値にリセットします。 |
| **[!UICONTROL Create Order]** | [オーダーを作成](../stores-purchase/customer-account-create-order.md) これは顧客アカウントに関連付けられています。 |
| **[!UICONTROL Reset Password]** | 顧客のパスワードをリセットします。 |
| **[!UICONTROL Force Sign-In]** | 顧客のパスワードに関連付けられたトークンをクリアし、管理者にアカウントへのアクセスを提供します。 |
| **[!UICONTROL Manage Shopping Cart]** | 顧客の買い物かごへのアクセスを提供します。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客アカウントを開いたままにします。 |
| **[!UICONTROL Save Customer]** | 変更を保存し、顧客アカウントを閉じます。 |

{style="table-layout:auto"}
