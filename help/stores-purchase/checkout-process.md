---
title: チェックアウトプロセスとオプション
description: Adobe CommerceとMagento Open Sourceのチェックアウトプロセスで、トランザクションの完了に必要な情報を収集し、「チェックアウト」ページでプロセスの各ステップを通じて顧客を導く方法を説明します。
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 0%

---

# チェックアウトプロセスとオプション

チェックアウトプロセスが開始されると、トランザクションは、セキュアで暗号化されたチャネルに移行します。 ブラウザーのアドレスバーに南京錠アイコンが表示され、URL が `http` から `https`.

## プロセス

チェックアウトプロセスの目標は、トランザクションの完了に必要な情報を収集することです。 The _チェックアウト_ ページでは、プロセスの各ステップを通じて顧客を導きます。 アカウントにログインしているお客様は、既に多くの情報がアカウントに含まれているので、すばやくチェックアウトを完了できます。 発注書を使用する会社アカウントに関連付けられた顧客のワークフローは、少し異なります。

### 送料

チェックアウトプロセスの最初のステップは、顧客が配送先住所情報を入力し、配送方法を選択することです。 顧客がアカウントを持っている場合、配送先住所は自動的に入力されますが、必要に応じて変更できます。

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 受信者と送信者の住所の形式は、 [顧客住所属性](../customers/address-attributes.md). 入力検証設定は、配送先住所で使用できる有効な文字を決定します。

ページ上部のプログレスバーは、チェックアウトプロセスの各ステップに従い、それまでに入力された情報が「注文の概要」に表示されます。

![チェックアウトプロセス中の出荷ページ](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### 別の住所に出荷

1. アドレス帳に追加のエントリがある場合、顧客は注文が発送される住所を検索します。

1. アドレスを選択するには、次をクリックします。 **[!UICONTROL Ship Here]**.

#### アドレスを追加

1. の下部に _[!UICONTROL Shipping Address]_セクションで、顧客がクリックする&#x200B;**[!UICONTROL + New Address]**.

1. 次を完了します。 _[!UICONTROL Shipping Address]_フォーム。

   デフォルトでは、顧客の姓と名は最初にフォームに表示されます。

   ![配送先住所フォームには、名前と住所の情報が含まれます](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. 新しい住所をアドレス帳に保存する場合は、フォームの下部にあるチェックボックスを選択します。

1. クリック数 **[!UICONTROL Save Address]**.

   新しい住所が配送先住所として選択されます。

   ![保存した住所は、発送ページで自動的に選択されます](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### 発送方法を選択

1. 次のリスト： [輸送](delivery.md) メソッドの場合、お客様は使用するオプションを選択します。

   ![発送ページに発送方法のオプションが表示されます](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. クリック数 **[!UICONTROL Next]** をクリックして続行します。

### 検討と支払い — 通常の注文

チェックアウトプロセスの 2 番目の手順では、お客様が [支払方法](payments.md)、プロモーションコードを含むクーポンを購入に適用します。 必要に応じて、すべての情報を確認し、編集できます。 有効にした場合、顧客は注文をおこなう前に販売の利用条件に同意する必要があります。

>[!NOTE]
>
>Commerce では複数のクーポンコードを設定できますが、顧客は 1 つのクーポンコードのみを買い物かごに適用できます。 ( [クーポンコード](../merchandising-promotions/price-rules-cart-coupon.md) を参照 )。

![チェックアウト時の確認および支払いページ](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### 検討と支払い — 発注

![Adobe Commerce用 B2B](../assets/b2b.svg) (B2B では、Adobe Commerceでのみ使用可能 )

顧客が、有効になっている会社に関連付けられたとき [発注書](../b2b/purchase-order-flow.md)の場合、すべての注文が発注書として処理されます。 使用可能な支払い方法は、会社のアカウント設定によって決まります。

1. 顧客が支払い方法を選択します。

   を使用する場合、 _アカウントでの支払い_ メソッド、 [!UICONTROL Custom Reference Number] フィールドを使用して、請求書番号を参照できます。

1. 顧客がクリックする **[!UICONTROL Place Purchase Order]**.

   発注が行われます。

会社が [承認ルール](../b2b/account-dashboard-approval-rules.md)に設定した場合、発注書は承認プロセスを実行します。 それ以外の場合は、即座に処理されます。

![発注書の確認と支払い](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### 注文の概要に表示される項目数

管理者ユーザーは、チェックアウト時に注文概要に表示される項目の最大数を変更して、製品数を減らして表示を合理化できます。 デフォルトでは、この値は 10 に設定されています。

![注文の概要に表示される項目数](./assets/order-summary.png){width="700" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Checkout Options]** 」セクションに入力します。

1. の場合 **[!UICONTROL Maximum Number of Items to Display in Order Summary]**」には、表示する項目の最大数を入力します。

1. クリック **[!UICONTROL Save Config]**.

   この更新により、チェックアウト時に表示される注文の概要は、指定された品目数に制限されます。

### 注文の確認

注文の確認は、注文が行われた後に表示されます。 登録ユーザーの場合、このページには、顧客のアカウントへのリンクを含む注文番号と、レシートを生成するリンクが含まれます。 登録されたお客様は、注文の確認と追跡情報を E メールで期待するように求められます。 ゲストは、注文を追跡するためのアカウントを作成することをお勧めします。 登録済みのお客様は、リンクをクリックしてレシートを生成できます。

注文確認ページは、 _成功_ ページに保存され、analytics プログラムでコンバージョンを追跡するために使用されます。

![注文の確認ページに、成功メッセージと注文番号が表示されます](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## チェックアウトオプション

チェックアウトオプションは、レイアウトを含む、チェックアウトページの様々な属性を制御します。 ゲストによるチェックアウトの許可や利用条件契約の実施など、チェックアウトに制約を課すように設定できるオプションがあります。 また、チェックアウトプロセス中に情報の表示を制御するオプションもあります。

![設定 — チェックアウトオプション](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

これらの各設定について詳しくは、 [チェックアウトオプション](../configuration-reference/sales/checkout.md#checkout-options) （内） _設定リファレンスガイド_.

### チェックアウトオプションを変更します。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Checkout]**.
1. 必要に応じて、次のオプションを設定します。
1. クリック **[!UICONTROL Save Config]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Checkout Options]** 」セクションに入力します。

1. 設定が特定のストア表示の場合、 [ストア表示を選択](../configuration-reference/scope-change.md#set-the-scope) 設定が適用される場所

   プロンプトが表示されたら、「 **[!UICONTROL OK]** をクリックして続行します。

1. チェックアウトオプションを設定します。

1. クリック **[!UICONTROL Save Config]**.

### 使用可能なチェックアウトオプション

| フィールド | [範囲](../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | ストア表示 | 次の場合に決定 [1 ページのチェックアウト](checkout-one-page.md) は、デフォルトのチェックアウト形式です。 オプション：はい/いいえ |
| [!UICONTROL Allow Guest Checkout] | ストア表示 | ゲストが通過できるかどうかを指定します [登録せずにチェックアウト](checkout-guest.md) ストアのアカウントに対して。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | ストア表示 | お客様が [利用条件](terms-and-conditions.md) 購入前の販売の情報を含んでいます。 オプション： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | ストア表示 | チェックアウト時の請求先住所の場所を決定します。 オプション： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | ストア表示 | チェックアウト時に注文の概要に表示できる項目の最大数を決定します。 デフォルトはです。 `10`. |
| [!UICONTROL Enable Address Search] | Web サイト | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) 顧客が [アドレス検索](checkout-address-search.md) の機能 _送料_、および _レビューと支払い_ 手順。 この関数が有効な場合は、 _[!UICONTROL Number of Customer Addresses Limit]_：チェックアウト時にこの機能を有効化するために必要な保存済みアドレスの数を設定します。 オプション： `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | Web サイト | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) アドレス検索が **[!UICONTROL Enabled]**&#x200B;では、チェックアウト時にこの機能を有効にするために必要な、保存済みアドレスの数を決定します。 顧客の保存済みアドレスの数がこの数を超える場合、デフォルトのアドレスのみが _送料_ および _レビューと支払い_ 手順。 顧客は、検索機能を使用して、選択した住所を変更できます。 デフォルトは 10 です。 |

{style="table-layout:auto"}
