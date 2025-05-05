---
title: 即時購入
description: インスタント購入の概要と、登録済みの顧客アカウントを迅速にチェックアウトする方法について説明します。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 即時購入

_即時購入_ を使用すると、お客様は、アカウントに保存された情報を使用して、チェックアウトプロセスを迅速に実行できます。 有効にすると、要件を満たすお客様に対して、製品ページの _買い物かごに追加_ ボタンの下に _即時購入_ ボタンが表示されます。

![ 「インスタント購入」オプションが表示された製品ページ ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 顧客要件

- 顧客が自分のアカウントに [ ログイン ](../customers/customer-sign-in.md) している。

- 顧客アカウントには [ デフォルトの請求および配送先住所 ](../customers/account-dashboard-address-book.md) があります。

- デフォルトの配送先住所で指定された国で、少なくとも 1 つの [ 配送方法 ](delivery.md) を使用できます。

- 顧客アカウントには、Vault が有効になっている [ 保存された支払い ](../stores-purchase/stored-payment-methods.md) 方法があります。

  保存されたクレジットカード情報への安全なアクセスを提供するには、次の支払い方法を使用できます。

   - [Braintree クレジット カード ](braintree.md) （3D セキュアが有効な場合、インスタント購入はBraintree クレジット カードで使用できません。）
   - [PayPal が有効なBraintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## ストアフロントでの即時購入

1. ストアフロントでは、お客様は購入する商品の商品ページに移動します。

1. 必要なオプションを選択し、**[!UICONTROL Instant Purchase]** をクリックします。

   ![ インスタント購入を確認するための確認ダイアログ ](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. **[!UICONTROL Instant Purchase Confirmation]** の情報を確認し、**[!UICONTROL OK]** をクリックしてトランザクションを完了します。

   製品ページの上部に確認メッセージと注文番号が表示されます。

## インスタント購入の設定

### 手順 1：設定ページを開く

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

### 手順 2：支払い方法 Vault の設定

Braintreeで即時購入を使用するか、Adobe CommerceとMagento Open Sourceの支払いサービスを使用できます。 買い物客がインスタント購入機能を使用するには、ボルトを有効にする必要があります。

支払方法を設定し、Braintreeまたは支払いサービスの保管を有効にする方法を説明します。

- [Braintree](braintree.md)
- [ 支払いサービスのドキュメント ](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### 手順 3：即時購入を有効にする

1. 「_[!UICONTROL Sales]_」セクションの下にある左パネルで、「**[!UICONTROL Sales]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Instant Purchase]**」セクションを展開します。

1. この変更が特定のストア表示に対するものである場合は、設定が適用される [ ストア表示を選択 ](../configuration-reference/scope-change.md#set-the-scope) します。

   プロンプトが表示されたら、「**[!UICONTROL OK]**」をクリックして続行します。

1. **[!UICONTROL Enabled]** を `Yes` に設定します。

1. ボタンに表示する **[!UICONTROL Button Text]** を入力します。

   ボタンのテキストは、ストア表示または言語ごとに変更できます。 デフォルトでは、ボタンのテキストは `Instant Purchase` です。

   ![ 設定 – 即時購入オプション ](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、『 [ 設定リファレンスガイド _の ](../configuration-reference/sales/sales.md#instant-purchase) 即時購入_ を参照してください。

1. 「**[!UICONTROL Save Config]**」をクリックします。

1. キャッシュを更新するように求められたら、システムメッセージの **[!UICONTROL Cache Management]** をクリックし、指示に従ってキャッシュをフラッシュします。
