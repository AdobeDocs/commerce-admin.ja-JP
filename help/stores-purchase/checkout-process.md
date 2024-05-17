---
title: チェックアウトプロセスとオプション
description: Adobe CommerceとMagento Open Sourceのチェックアウトプロセスが、トランザクションの完了に必要な情報を収集する方法と、「チェックアウト」ページがプロセスの各ステップを通じてお客様を導く方法について説明します。
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 0%

---

# チェックアウトプロセスとオプション

チェックアウトプロセスが開始されると、トランザクションは、暗号化された安全なチャネルに移動します。 ブラウザーのアドレスバーに南京錠の記号が表示され、URL が次の場所から変更されます。 `http` 対象： `https`.

## プロセス

チェックアウトプロセスの目標は、トランザクションの完了に必要な情報を収集することです。 この _チェックアウト_ このページでは、プロセスの各ステップを順を追って説明します。 アカウントにログインしている顧客は、情報の多くが既にアカウントに存在するので、すばやくチェックアウトを完了できます。 発注書を使用する会社アカウントに関連付けられている顧客のワークフローは若干異なります。

### 送料

チェックアウトプロセスの最初の手順は、顧客が配送先住所情報を入力し、配送方法を選択することです。 顧客がアカウントを持っている場合、配送先住所は自動的に入力されますが、必要に応じて変更できます。

![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）受信者と送信者の住所の書式は、のプロパティによって決定されます [顧客の住所属性](../customers/address-attributes.md). 入力検証設定は、配送先住所で使用できる有効な文字を決定します。

ページの上部にあるプログレスバーはチェックアウトプロセスの各ステップに従い、注文概要には入力した情報が表示されます。

![チェックアウトプロセス中の送料ページ](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### 別の住所に配送

1. アドレス帳に追加のエントリがある場合、顧客は注文が出荷される住所を見つけます。

1. アドレスを選択するには、をクリックします **[!UICONTROL Ship Here]**.

#### アドレスを追加

1. の下部 _[!UICONTROL Shipping Address]_セクション、顧客のクリック数&#x200B;**[!UICONTROL + New Address]**.

1. 完了： _[!UICONTROL Shipping Address]_フォーム。

   デフォルトでは、顧客の姓と名が最初にフォームに表示されます。

   ![発送先住所フォームには、名前と住所の情報が含まれます](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. アドレス帳に新しい住所を保存するには、フォームの下部にあるチェックボックスを選択します。

1. クリック数 **[!UICONTROL Save Address]**.

   新しい住所が配送先住所として選択されました。

   ![保存された住所は、「発送先」ページで自動的に選択されます](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### 配送方法を選択

1. のリスト内 [送料](delivery.md) 方法。顧客が使用するオプションを選択します。

   ![「出荷」ページには、出荷方法オプションが表示されます](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. クリック数 **[!UICONTROL Next]** 続行します。

### レビューと支払い – 通常の注文

チェックアウトプロセスの 2 番目の手順では、顧客は以下を選択します。 [支払い方法](payments.md)を入力し、プロモーションコードを含むクーポンを購入に適用します。 すべての情報は、必要に応じて確認および編集できます。 有効にした場合、お客様は注文する前に販売条件に同意する必要があります。

>[!NOTE]
>
>Commerceでは複数のクーポンコードを設定できますが、お客様は 1 つのクーポンコードのみを買い物かごに適用できます。 （ [クーポンコード](../merchandising-promotions/price-rules-cart-coupon.md) を参照してください）。

![チェックアウト時の確認と支払いページ](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### レビューと支払 – 発注

![Adobe Commerceの B2B](../assets/b2b.svg) （B2B でAdobe Commerceでのみ使用可能）

を有効にしている会社に顧客が関連付けられている場合 [発注書](../b2b/purchase-order-flow.md)すべての注文は発注書として処理されます。 利用可能な支払い方法は、会社アカウントの設定によって決まります。

1. 顧客が支払い方法を選択します。

   使用する場合 _分割払い_ メソッド、 [!UICONTROL Custom Reference Number] フィールドを使用して、請求書番号を参照できます。

1. 顧客のクリック数 **[!UICONTROL Place Purchase Order]**.

   発注が行われます。

会社が次のように設定している場合 [承認ルール](../b2b/account-dashboard-approval-rules.md)を選択すると、発注書は承認プロセスを実行します。 それ以外の場合は、直ちに処理されます。

![発注書の確認と支払](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### 注文概要に表示される項目数

管理者ユーザーは、チェックアウト時に注文概要に表示される最大項目数を変更して、より少ない製品で表示を効率化できます。 デフォルトでは、この値は 10 に設定されています。

![注文概要に表示される項目数](./assets/order-summary.png){width="700" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Checkout]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Checkout Options]** セクション。

1. の場合 **[!UICONTROL Maximum Number of Items to Display in Order Summary]**&#x200B;を選択し、表示する項目の最大数を入力します。

1. クリック **[!UICONTROL Save Config]**.

   この更新により、チェックアウト時に表示される注文概要は、指定した数量の項目に限定されます。

### 注文確認

注文後、注文確認が表示されます。 登録済みのお客様の場合、ページには、注文番号と、お客様のアカウントへのリンク、およびレシートを生成するためのリンクが含まれます。 登録されたお客様は、メールで注文確認と追跡情報を期待するように言われます。 注文を追跡するためのアカウントを作成することをお勧めします。 登録済みのお客様は、リンクをクリックして領収書を生成できます。

注文確認ページは、とも呼ばれます _成功_ ページに移動します。analytics プログラムでコンバージョンを追跡するために使用されます。

![Order Confirmation ページには、成功メッセージとオーダー番号が表示されます](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## チェックアウトオプション

チェックアウトオプションは、レイアウトなど、チェックアウトページの様々な属性を制御します。 ゲストのチェックアウトを許可したり、利用条件に関する契約を適用するなど、チェックアウトに制約を設定できるオプションがあります。 チェックアウトプロセス中の情報の表示を制御するオプションもあります。

![設定 – チェックアウトオプション](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

これらの各設定について詳しくは、を参照してください。 [チェックアウトオプション](../configuration-reference/sales/checkout.md#checkout-options) が含まれる _設定リファレンスガイド_.

### チェックアウトオプションの変更

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Checkout]**.
1. 必要に応じて、次のいずれかのオプションを設定します。
1. クリック **[!UICONTROL Save Config]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Checkout Options]** セクション。

1. 設定が特定のストア表示の場合、 [ストア表示の選択](../configuration-reference/scope-change.md#set-the-scope) 設定が適用される場所。

   プロンプトが表示されたら、 **[!UICONTROL OK]** 続行します。

1. チェックアウトオプションを設定します。

1. クリック **[!UICONTROL Save Config]**.

### 使用可能なチェックアウトオプション

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | ストア表示 | 次のかどうかを判断します [1 ページチェックアウト](checkout-one-page.md) はデフォルトのチェックアウト形式です。 オプション：はい/いいえ |
| [!UICONTROL Allow Guest Checkout] | ストア表示 | ゲストが経由できるかどうかを決定します [登録せずにチェックアウト](checkout-guest.md) ストアのアカウントの場合。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | ストア表示 | お客様がに同意する必要があるかどうかを判断します [利用条件](terms-and-conditions.md) 購入する前の販売の。 オプション： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | ストア表示 | チェックアウト時の請求先住所の場所を決定します。 オプション： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | ストア表示 | チェックアウト時に注文概要に表示できる項目の最大数を決定します。 デフォルトはです `10`. |
| [!UICONTROL Enable Address Search] | Web サイト | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）お客様がを使用できるかどうかを決定します。 [アドレス検索](checkout-address-search.md) 機能： _送料_、および _レビューと支払い_ 手順。 この関数を有効にする場合は、 _[!UICONTROL Number of Customer Addresses Limit]_チェックアウト時にこの機能をアクティブ化するために必要な、保存済みアドレスの数を設定します。 オプション： `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | Web サイト | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）アドレス検索が **[!UICONTROL Enabled]**&#x200B;は、チェックアウト時にこの機能をアクティブ化するために必要な保存済みアドレスの数を決定します。 顧客の保存済みアドレスの数がこの数を満たしているか、この数を超える場合、デフォルトのアドレスのみが _送料_ および _レビューと支払い_ 手順。 お客様は、検索機能を使用して、選択したアドレスを変更できます。 デフォルトは 10 です。 |

{style="table-layout:auto"}
