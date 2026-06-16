---
title: 今すぐ購入
description: インスタント購入について学び、登録した顧客アカウントに迅速なチェックアウトを提供する方法について説明します。
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
TQID: https://experienceleague.adobe.com/sxfhq1vK7ohJBBli3U05dNoOvV2cdHc3j17nwvf3Le4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# 今すぐ購入

_インスタント購入_&#x200B;を使用すると、お客様はアカウントに保存されている情報を使用して、チェックアウトプロセスをスピードアップできます。 有効にすると、要件を満たす顧客の製品ページの「_カートに追加_」ボタンの下に「_即時購入_」ボタンが表示されます。

![即時購入オプションが表示された製品ページ ](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## お客様の要件

- お客様は、アカウントに[ ログイン ](../customers/customer-sign-in.md)しています。

- お客様のアカウントには[ デフォルトの請求先住所と配送先住所](../customers/account-dashboard-address-book.md)があります。

- デフォルトの配送先住所で指定されている国に対して、少なくとも1つの[配送方法](delivery.md)を利用できます。

- お客様のアカウントには、Vaultが有効になっている[ ストアド支払い](../stores-purchase/stored-payment-methods.md)方法があります。

  保存されたクレジットカード情報に安全にアクセスするために、次の支払い方法を使用できます。

   - [Braintree クレジットカード ](braintree.md) （3D セキュアが有効になっている場合、Braintree クレジットカードでは即時の購入はできません）。
   - [PayPalが有効になっているBraintree](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## ストアフロントですばやく購入

1. ストアフロントでは、顧客は購入する商品の商品ページにアクセスします。

1. 必要なオプションを選択し、**[!UICONTROL Instant Purchase]**&#x200B;をクリックします。

   ![即時の購入を確認する確認ダイアログ ](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. **[!UICONTROL Instant Purchase Confirmation]**&#x200B;情報を確認し、**[!UICONTROL OK]**&#x200B;をクリックしてトランザクションを完了します。

   商品ページの上部に、確認メッセージと注文番号が表示されます。

## 今すぐ購入を設定

### 手順1：設定ページを開く

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

### 手順2：支払い方法の保管を設定する

Braintreeでの即時購入またはAdobe CommerceおよびMagento Open Sourceの決済サービスを使用できます。 買い物客が即日購入機能を使用できるようにするには、事前にヴォールティングを有効にする必要があります。

Braintreeまたは決済サービスの決済方法を設定し、ヴォールトを有効にする方法について説明します。

- [Braintree](braintree.md)
- [決済サービスのドキュメント](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### ステップ 3：即時購入を有効にする

1. _[!UICONTROL Sales]_セクションの下の左側のパネルで、**[!UICONTROL Sales]**を選択します。

1. **[!UICONTROL Instant Purchase]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. この変更が特定のストアビューに適用される場合、[設定が適用されるストアビュー](../configuration-reference/scope-change.md#set-the-scope)を選択します。

   プロンプトが表示されたら、**[!UICONTROL OK]**&#x200B;をクリックして続行します。

1. **[!UICONTROL Enabled]**&#x200B;を`Yes`に設定します。

1. ボタンに表示する&#x200B;**[!UICONTROL Button Text]**&#x200B;を入力します。

   ボタンテキストは、ストアビューまたは言語ごとに変更できます。 デフォルトでは、ボタンのテキストは`Instant Purchase`です。

   ![設定 – インスタント購入オプション ](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   これらの各構成設定の詳細については、_構成リファレンスガイド_&#x200B;の[即時購入](../configuration-reference/sales/sales.md#instant-purchase)を参照してください。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

1. キャッシュの更新を求めるメッセージが表示されたら、システムメッセージの「**[!UICONTROL Cache Management]**」をクリックし、指示に従ってキャッシュをフラッシュします。
