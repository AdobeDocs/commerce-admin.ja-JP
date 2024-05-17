---
title: 即時購入
description: インスタント購入の概要と、登録済みの顧客アカウントを迅速にチェックアウトする方法について説明します。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 即時購入

_即時購入_ を使用すると、お客様は、アカウントに保存された情報を使用して、チェックアウトプロセスを迅速に実行できます。 有効にすると、 _即時購入_ ボタンがの下に表示されます _カートに追加_ 要件を満たすお客様向けの製品ページのボタン。

![「インスタント購入」オプションが表示された製品ページ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 顧客要件

- 顧客 [ログイン済み](../customers/customer-sign-in.md) をユーザーに報告します。

- 顧客アカウントに [既定の請求先住所と送付先住所](../customers/account-dashboard-address-book.md).

- 少なくとも 1 つ [発送方法](delivery.md) は、デフォルトの配送先住所で指定された国で使用できます。

- 顧客アカウントに [保管済みの支払い](../stores-purchase/stored-payment-methods.md) vault が有効になっているメソッド。

  保存されたクレジットカード情報への安全なアクセスを提供するには、次の支払い方法を使用できます。

   - [Braintreeクレジットカード](braintree.md) （3D セキュアが有効化されている場合、Braintreeクレジットカードでは即時購入を利用できません。
   - [PayPal が有効なBraintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## ストアフロントでの即時購入

1. ストアフロントでは、お客様は購入する商品の商品ページに移動します。

1. 必要なオプションとクリックを選択します **[!UICONTROL Instant Purchase]**.

   ![インスタント購入を確認するための確認ダイアログ](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. をレビュー **[!UICONTROL Instant Purchase Confirmation]** 情報とクリック数 **[!UICONTROL OK]** をクリックしてトランザクションを完了します。

   製品ページの上部に確認メッセージと注文番号が表示されます。

## インスタント購入の設定

### 手順 1：設定ページを開く

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### 手順 2：支払い方法 Vault の設定

Adobe CommerceとMagento Open SourceのBraintreeまたは支払いサービスで即時購入を使用できます。 買い物客がインスタント購入機能を使用するには、ボルトを有効にする必要があります。

支払い方法を設定し、Braintreeまたは支払いサービスのヴォールティングを有効にする方法を説明します。

- [Braintree](braintree.md)
- [支払いサービスのドキュメント](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### 手順 3：即時購入を有効にする

1. 左パネルのの下にある _[!UICONTROL Sales]_セクションで選択&#x200B;**[!UICONTROL Sales]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Instant Purchase]** セクション。

1. この変更が特定のストア表示に対するものである場合、 [ストア表示の選択](../configuration-reference/scope-change.md#set-the-scope) 設定が適用される場所。

   プロンプトが表示されたら、 **[!UICONTROL OK]** 続行します。

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

1. を入力 **[!UICONTROL Button Text]** ボタンに表示する。

   ボタンのテキストは、ストア表示または言語ごとに変更できます。 デフォルトでは、ボタンのテキストはです `Instant Purchase`.

   ![設定 – 即時購入オプション](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、を参照してください。 [即時購入](../configuration-reference/sales/sales.md#instant-purchase) が含まれる _設定リファレンスガイド_.

1. クリック **[!UICONTROL Save Config]**.

1. キャッシュの更新を求めるメッセージが表示されたら、 **[!UICONTROL Cache Management]** システムメッセージで、指示に従ってキャッシュをフラッシュします。
