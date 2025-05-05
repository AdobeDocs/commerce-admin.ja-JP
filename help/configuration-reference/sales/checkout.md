---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Checkout] ページで設定を確認します。
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![ チェックアウトオプション ](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | ストア表示 | この設定を有効にすると、メール アドレスが既に顧客アカウントに関連付けられている場合に、認証されていないユーザー（ストアフロントおよび API）がクエリを実行できるようになります。 これを使用すると、入力したメールアドレスが既に顧客アカウントに登録されているが、認証されていないユーザーに情報が公開されるコストがかかる場合に、サインインのプロンプトを表示することで、ゲストのチェックアウトワークフローを強化できます。  オプション：`Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | ストア表示 | [1 ページチェックアウト ](../../stores-purchase/checkout-process.md#checkout-options) がデフォルトのチェックアウト形式かどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | ストア表示 | ストアのアカウントについて、ゲストが [ 登録せずにチェックアウト ](../../stores-purchase/checkout-guest.md) を実行できるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | ストア表示 | 購入を行う前に、顧客が販売の [ 利用条件 ](../../stores-purchase/terms-and-conditions.md) に同意する必要があるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Display Billing Address On] | ストア表示 | チェックアウト時の請求先住所の場所を決定します。 オプション：`Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | ストア表示 | チェックアウト時に _注文概要_ に表示できる項目の最大数を決定します。 デフォルトは `10` です。 |
| [!UICONTROL Enable Address Search] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ）お客様が [ アドレス検索 ](../../stores-purchase/checkout-address-search.md) 機能を配送手順、確認および支払い手順に使用できるかどうかを決定します。 これが有効な場合、顧客アドレス数制限を使用して、チェックアウト時にこの機能をアクティブ化するために必要な保存済みアドレス数を設定します。 オプション：`Yes` / `No` |
| 顧客アドレス数の制限 | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) （Adobe Commerceのみ） アドレス検索が有効な場合は、チェックアウト時にこの機能をアクティブ化するために必要な保存済みアドレスの数を特定します。 顧客の保存済みアドレスの数がこの数を超える場合、_配送_ ステップおよび _確認と支払い_ ステップではデフォルトのアドレスのみがレンダリングされます。 お客様は、検索機能を使用して、選択したアドレスを変更できます。 デフォルトは `10` です。 |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![ 買い物かご ](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Web サイト | [ 見積もり価格の有効期間 ](../../stores-purchase/cart-configuration.md#quote-lifetime) を日数で指定します。 |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | ストア表示 | 商品が買い物かごに追加された直後に [ 買い物かごページ ](../../stores-purchase/cart-configuration.md#redirect-to-cart) が表示されるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | ストア表示 | ポケットベルがトリガーされるまでの、買い物かごの中のアイテム数を決定します。 デフォルト値：`20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | ストア表示 | 買い物かごに [ クロスセル品目 ](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) が表示され、顧客に追加の販売オプションを提供するかどうかを示します。 オプション：`Yes` （デフォルト）/`No` |
| [!UICONTROL Grouped Product Image] | ストア表示 | 買い物かご内の [&#128279;](../../stores-purchase/cart-configuration.md#cart-thumbnails) グループ化された商品 [ に表示される ](../../catalog/product-create-grouped.md) サムネール  画像を決定します。 オプション：`Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | ストア表示 | 買い物かご内の設定可能な商品に対して表示される [ サムネール ](../../stores-purchase/cart-configuration.md#cart-thumbnails) 画像を決定します。 オプション：`Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | ストア表示 | 買い物かごからプレビューしたときの見積もりの最大期間（分単位）を決定します。 |
| [!UICONTROL Enable Clear Shopping Cart] | Web サイト | ユーザーが 1 回の操作で買い物かごの中身をクリアできるオプションを買い物かごに表示するかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![ 自分の買い物かごリンク ](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Web サイト | マイ買い物かごリンクの後の括弧内に表示される値を決定します。 オプション：`Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## ミニカート

![ ミニカート ](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | ストア表示 | ヘッダーの買い物かごアイコンをクリックしたときに、ミニ買い物かごが店舗ページに表示されるかどうかを決定します。 ミニカートの表示は、テーマによって異なります。 オプション：`Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | ストア表示 | スクロールバーがトリガーされる前に、ミニ カートに表示できるアイテムの数を決定します。 デフォルト：`5` |
| [!UICONTROL Maximum Number of Items to Display] | ストア表示 | ミニ カートに表示できるアイテムの最大数を決定します。 デフォルト：`10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![ 支払いに失敗したメール ](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/ja/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | ストア表示 | 支払いに失敗したメールを受信する店舗の連絡先を識別します。 既定の受信者：`General Contact` |
| [!UICONTROL Payment Failed Email Sender] | ストア表示 | 支払い失敗メールの送信者として表示される店舗連絡先を識別します。 既定の送信者：`General Contact` |
| [!UICONTROL Payment Failed Template] | ストア表示 | 支払失敗の E メールに使用するテンプレートを識別します。 既定のテンプレート：`Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | ストア表示 | 支払いが失敗したメールのコピーを受け取るユーザーのメールアドレスを指定します。 複数のアドレスはコンマで区切ります。 |
| [!UICONTROL Send Payment Failed Copy Method] | ストア表示 | コピーの送信に使用する電子メールの方法を示します。 オプション：<br />**`Bcc`**– 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、ブラインドコピーを送信します。 BCC 受信者が顧客に表示されない。<br />**`Separate Email`** - コピーを個別のメールとして送信します。 |

{style="table-layout:auto"}
