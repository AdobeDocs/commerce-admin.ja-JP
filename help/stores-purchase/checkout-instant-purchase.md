---
title: 即時購入
description: 即時購入について、および登録済み顧客アカウントの迅速なチェックアウト方法について説明します。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 即時購入

_即時購入_ を使用すると、顧客は、自分のアカウントに保存された情報を使用して、チェックアウトプロセスを迅速に実行できます。 有効にすると、 _即時購入_ ボタンが _買い物かごに追加_ ボタンをクリックして、要件を満たすお客様向けの製品ページに表示します。

![「即時購入」オプションが表示された製品ページ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 顧客要件

- 顧客が [サインイン済み](../customers/customer-sign-in.md) をアカウントに追加します。

- 顧客アカウントに [デフォルトの請求先住所と配送先住所](../customers/account-dashboard-address-book.md).

- 少なくとも 1 つ [輸送方法](delivery.md) は、デフォルトの配送先住所で指定された国に対して使用できます。

- 顧客アカウントに [貯蓄支払い](../stores-purchase/stored-payment-methods.md) vault が有効なメソッド。

  保存されたクレジットカード情報への安全なアクセスを提供するには、次の支払い方法を使用できます。

   - [Braintreeクレジットカード](braintree.md) (3D セキュアが有効な場合、インスタント購入はBraintreeクレジットカードでは使用できません。)
   - [PayPal を有効にしたBraintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## ストアフロントでの即時購入

1. ストアフロントで、顧客は購入する品目の製品ページに移動します。

1. 必要なオプションとクリックを選択 **[!UICONTROL Instant Purchase]**.

   ![即時購入を確認する確認ダイアログ](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. レビュー **[!UICONTROL Instant Purchase Confirmation]** 情報およびクリック数 **[!UICONTROL OK]** をクリックして、トランザクションを完了します。

   製品ページの上部に確認メッセージと注文番号が表示されます。

## 即時購入の設定

### 手順 1：設定ページを開く

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### 手順 2：支払い方法 Vault を設定する

Adobe CommerceおよびMagento Open Sourceでは、Braintreeまたは支払いサービスで即時購入を使用できます。 買い物客がインスタント購入機能を使用する前に、ヴォールティングを有効にする必要があります。

支払い方法を設定し、Braintreeまたは支払いサービスの保管を有効にする方法を説明します。

- [Braintree](braintree.md)
- [支払いサービスドキュメント](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### 手順 3：即時購入を有効にする

1. 左側のパネルで、 _[!UICONTROL Sales]_セクション、選択&#x200B;**[!UICONTROL Sales]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Instant Purchase]** 」セクションに入力します。

1. この変更が特定のストア表示に対するものである場合、 [ストア表示を選択](../configuration-reference/scope-change.md#set-the-scope) 設定が適用される場所

   プロンプトが表示されたら、「 **[!UICONTROL OK]** をクリックして続行します。

1. 設定 **[!UICONTROL Enabled]** から `Yes`.

1. 次を入力します。 **[!UICONTROL Button Text]** ボタンに表示する

   ボタンのテキストは、ストアの表示ごと（言語）に変更できます。 デフォルトでは、ボタンのテキストは `Instant Purchase`.

   ![設定 — 即時購入オプション](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   これらの各設定について詳しくは、 [即時購入](../configuration-reference/sales/sales.md#instant-purchase) （内） _設定リファレンスガイド_.

1. クリック **[!UICONTROL Save Config]**.

1. キャッシュを更新するように求められたら、 **[!UICONTROL Cache Management]** を選択し、指示に従ってキャッシュをフラッシュします。
