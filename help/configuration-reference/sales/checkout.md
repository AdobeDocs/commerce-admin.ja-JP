---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: 次のページで設定を確認します： [!UICONTROL Sales] &gt; [!UICONTROL Checkout] コマース管理のページ。
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

>[!NOTE]
>
>[!BADGE 2.4.6-p1]{type=Informative tooltip="2.4.6-p1 の更新点"}[!BADGE 2.4.7-beta1]{type=Informative tooltip="2.4.7-beta1 の更新点"}[2.4.7-beta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) および [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) のリリースでは、説明する機能のセキュリティが強化されています。 またはこれらのリリースバージョンを使用している場合は、リリースノートを確認してください。

![チェックアウトオプション](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | ストア表示 | 次の場合に決定 [1 ページのチェックアウト](../../stores-purchase/checkout-process.md#checkout-options) は、デフォルトのチェックアウト形式です。 オプション： `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | ストア表示 | ゲストが通過できるかどうかを指定します [登録せずにチェックアウト](../../stores-purchase/checkout-guest.md) ストアのアカウントに対して。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | ストア表示 | お客様が [利用条件](../../stores-purchase/terms-and-conditions.md) 購入前の販売の情報を含んでいます。 オプション： `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | ストア表示 | チェックアウト時の請求先住所の場所を決定します。 オプション： `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | ストア表示 | に表示できる項目の最大数を指定します。 _注文の概要_ チェックアウト時に。 デフォルトはです。 `10`. |
| [!UICONTROL Enable Address Search] | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) 顧客が [アドレス検索](../../stores-purchase/checkout-address-search.md) 送料、およびレビューと支払いの手順に関する機能。 これを有効にした場合、「顧客アドレス数の上限」を使用して、チェックアウト時にこの機能を有効にするために必要な保存済みアドレスの数を設定します。 オプション： `Yes` / `No` |
| 顧客アドレス数の上限 | Web サイト | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerceのみ ) アドレスの検索が有効な場合、は、チェックアウト時にこの機能を有効にするために必要な、保存済みアドレスの数を決定します。 顧客の保存済みアドレスの数がこの数を超える場合、デフォルトのアドレスのみが _送料_ および _レビューと支払い_ 手順。 顧客は、検索機能を使用して、選択した住所を変更できます。 デフォルトはです。 `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![買い物かご](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Web サイト | を決定します。 [引用価格の存続期間](../../stores-purchase/cart-configuration.md#quote-lifetime)、日単位。 |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | ストア表示 | を [買い物かごページが表示されます](../../stores-purchase/cart-configuration.md#redirect-to-cart) 商品が買い物かごに追加された直後。 オプション： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | ストア表示 | ページャーがトリガーされる前の買い物かご内の品目数を決定します。 デフォルト値： `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | ストア表示 | 次のかどうかを示します [クロスセル品目](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) は買い物かごに表示され、顧客に追加の販売オプションを提供します。 オプション： `Yes` （デフォルト） / `No` |
| [!UICONTROL Grouped Product Image] | ストア表示 | を決定します。 [サムネール](../../stores-purchase/cart-configuration.md#cart-thumbnails) 画像が [グループ化された製品](../../catalog/product-create-grouped.md) 買い物かごに入れます。 オプション： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | ストア表示 | を決定します。 [サムネール](../../stores-purchase/cart-configuration.md#cart-thumbnails) 買い物かご内の設定可能な製品に対して表示される画像。 オプション： `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | ストア表示 | 買い物かごからプレビューした見積もりの最大閲覧期間を分単位で指定します。 |
| [!UICONTROL Enable Clear Shopping Cart] | Web サイト | ユーザーが 1 回の操作で買い物かごの内容をクリアするオプションを買い物かごに表示するかどうかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![買い物かごへのリンク](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Web サイト | 「買い物かご」リンクの後に括弧内に表示される値を決定します。 オプション： `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## ミニカート

![ミニカート](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | ストア表示 | ヘッダーの買い物かごアイコンをクリックしたときに、ミニカートがストアページに表示されるかどうかを指定します。 ミニカートの表示は、テーマによって異なります。 オプション： `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | ストア表示 | スクロールバーをトリガーする前にミニカートに表示できる項目数を指定します。 デフォルト： `5` |
| [!UICONTROL Maximum Number of Items to Display] | ストア表示 | ミニカートに表示できる項目の最大数を指定します。 デフォルト： `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![支払いに失敗したメール](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | ストア表示 | 支払いに失敗した電子メールを受け取るストアの連絡先を識別します。 デフォルトの受信者： `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | ストア表示 | 支払いに失敗した E メールのメッセージ送信者として表示されるストアの連絡先を識別します。 デフォルトの送信者： `General Contact` |
| [!UICONTROL Payment Failed Template] | ストア表示 | 支払いに失敗した E メールに使用されるテンプレートを識別します。 デフォルトのテンプレート： `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | ストア表示 | 支払い失敗の電子メールのコピーを受け取る人の電子メールアドレスを指定します。 複数のアドレスを指定する場合は、コンマで区切ります。 |
| [!UICONTROL Send Payment Failed Copy Method] | ストア表示 | コピーの送信に使用する電子メールメソッドを示します。 オプション： <br />**`Bcc`**— 顧客に送信されるのと同じ E メールのヘッダーに受信者を含めて、非表示の提供コピーを送信します。 BCC 受信者は、顧客に対して表示されません。<br />**`Separate Email`**  — コピーを別の E メールとして送信します。 |

{style="table-layout:auto"}
