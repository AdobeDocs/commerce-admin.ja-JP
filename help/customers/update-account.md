---
title: 顧客プロファイルの更新
description: 顧客が最後にサインインした日時やアカウントからログアウトした日時、顧客プロファイルの更新など、顧客の行動に関する情報にアクセスします。
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 顧客プロファイルの更新

の左側のパネル _[!UICONTROL Customer Information]_ページには、顧客のアクティビティ、住所、注文統計、最近の注文、買い物かごのコンテンツ、製品レビュー、ニュースレターの購読に関する情報が含まれます。

![顧客プロファイル](assets/cust-profile.png){width="700" zoomable="yes"}

## 顧客アカウントの編集

メソッド 1: **_クイック編集_**

1. 1 列目で、編集する顧客アカウントのチェックボックスを選択します。

1. を設定します。 **[!UICONTROL Actions]** 列を `Edit`.

   >[!INFO]
   >
   >更新可能な各値の値がテキストボックスに表示されます。 選択した顧客レコードの一部の値のみをグリッドから編集できます。

   ![クイック編集](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. 必要に応じて、次の値のいずれかを更新します。

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. クリック **[!UICONTROL Save]**.

方法 2: **_完全な編集_**

1. グリッドで、編集する顧客レコードを見つけます。

1. Adobe Analytics の _アクション_ 列の右端にある「 **[!UICONTROL Edit]**.

1. 会社情報に必要な変更を加えます。

   >[!INFO]
   >
   >詳しくは、 [顧客プロファイルの更新](../customers/update-account.md).

1. 完了したら、「 **[!UICONTROL Save Customer]**.

>[!INFO]
>
>保存前にすべての編集作業を取り消す場合は、 **[!UICONTROL Reset]** をクリックして、最後に保存したバージョンに対するすべての変更を返します。

## 顧客情報

### [!UICONTROL Customer View]

The _顧客ビュー_ 「 」タブには、顧客に関する情報が一覧表示されます。次の情報が含まれます。 **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]**、および **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

The [アカウント情報](../customers/account-dashboard-account-information.md) 「 」タブには、管理者ユーザーが個人情報、電子メール、リモートショッピングサポート、生年月日、Web サイトや会社に顧客を添付できる顧客に関する詳細情報が表示されます。

### [!UICONTROL Addresses]

The [アドレス](../customers/account-dashboard-address-book.md) 「 」タブには、顧客のデフォルトの請求先住所と配送先住所、および頻繁に使用するその他の住所が表示されます。

### [!UICONTROL Orders]

The [購入回数](../stores-purchase/orders.md) グリッドには、現在のすべての顧客注文のリストが含まれます。管理者は、その進行状況をトラッキングできます。

### [!UICONTROL Returns]

{{ee-feature}}

The [戻り値](../stores-purchase/returns.md) 「 」タブには、現在返されている顧客リクエストのリストが表示されます。

### [!UICONTROL Shopping cart]

The [買い物かご](../stores-purchase/cart.md) 「 」タブには、現在買い物かごに入っているが、何らかの理由で購入が完了していなかった製品が表示されます。

### [!UICONTROL Wish List]

A [ウィッシュリスト](../stores-purchase/wishlists.md) 顧客が後で買い物かごに転送できる製品のリストを表示します。

### [!UICONTROL Gift Registry]

{{ee-feature}}

The [ギフトレジストリ](../merchandising-promotions/gift-registry-storefront.md) 「 」セクションには、顧客の現在のギフトレジストリと関連するイベントが一覧表示されます。


### [!UICONTROL Store Credit]

{{ee-feature}}

The [店舗クレジット](../customers/store-credit.md) 「 」タブには、顧客アカウントに復元された金額が表示されます。管理者がこの値を管理できます。

### [!UICONTROL Newsletter]

The [ニュースレター](../merchandising-promotions/newsletters.md) 「 」タブには、現在の顧客に送信されたすべての電子メールが表示されます。

### [!UICONTROL Billing Agreements]

The [請求契約](../stores-purchase/paypal-billing-agreements.md) 「 」タブには、ストアと顧客の間の PayPal の請求契約がすべて表示されます。

### [!UICONTROL Product Reviews]

The [製品レビュー](../catalog/settings-advanced-product-reviews.md) 「 」タブには、この顧客が送信したすべてのレビューが表示されます。

### [!UICONTROL Reward Points]

{{ee-feature}}

The [報酬ポイント](../merchandising-promotions/rewards-loyalty.md) 「 」セクションには、お客様の現在の報酬ポイントの残高が表示されます。 管理者ユーザーがこの値を管理できます。

## ボタンバー

| ボタン | 説明 |
|----------|--------------|
| **[!UICONTROL Back]** | 変更を保存せずに、顧客ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | 商人が顧客としてログインする機能を許可します。 |
| **[!UICONTROL Delete Customer]** | 顧客アカウントを削除します。 |
| **[!UICONTROL Reset]** | 顧客フォームに保存されていない変更を以前の値にリセットします。 |
| **[!UICONTROL Create Order]** | [注文を作成](../stores-purchase/customer-account-create-order.md) 顧客アカウントに関連付けられている |
| **[!UICONTROL Reset Password]** | 顧客のパスワードをリセットします。 |
| **[!UICONTROL Force Sign-In]** | 顧客のパスワードに関連付けられたトークンを消去し、管理者がアカウントにアクセスできるようにします。 |
| **[!UICONTROL Manage Shopping Cart]** | 顧客の買い物かごへのアクセスを提供します。 |
| **[!UICONTROL Save and Continue Edit]** | 変更を保存し、顧客アカウントを開いたままにします。 |
| **[!UICONTROL Save Customer]** | 変更を保存し、顧客アカウントを閉じます。 |

{style="table-layout:auto"}
