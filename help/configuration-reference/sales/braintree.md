---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: 次の設定を確認します： [!UICONTROL Braintree] のセクション [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] コマース管理のページ。
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4 移行：**<br/>
>Adobe CommerceとMagento Open Sourceのバージョンが 2.4.0 より前の場合、マーチャントは、 [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) をクリックして、コア統合を置き換えます。 2.4.0 の時点で、拡張機能がコアリリースに含まれるようになりました。
><br/><br/>
>Commerce 2.4 に移行する場合、マーチャントは Marketplace で配布された拡張機能 (`paypal/module-braintree` または `gene/module-braintree`) を更新し、コードのカスタマイズを更新して `PayPal_Braintree` 名前空間の代わりに `Magento_Braintree`. コマース用にバンドルされた拡張機能と、その拡張機能で配布された拡張機能のCommerce Marketplace設定が保持されます。 これらのバージョンの拡張機能で行われた支払いは、通常どおりキャプチャ、無効化または返金されます。
><br/><br/>
>Commerce 2.4.0 にアップグレードし、以前の 2.3.x バージョンで推奨Commerce Marketplace拡張を使用しない場合、マルチアドレス機能はBraintree2.4.0 バージョンでは動作しません。 買い物客が _複数のアドレスへの配信_ の場合、Braintreeの支払い方法は表示されません。 以前は 2.3.x でCommerce Marketplace拡張機能を使用すると、複数のアドレスに関する問題が発生していました。

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![基本Braintree設定](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | デフォルト値： `Credit Card` (BRAINTREE) |
| [!UICONTROL Environment] | ストア表示 | オプション： `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | ストア表示 | 支払が処理される際にBraintreeが実行するアクションを決定します。 オプション： <br/>**`Authorize`**・お客様のクレジット・カードに対する資金は、認可されているが、口座から移管されていない。 ストア管理者で注文が作成されます。 後で販売を取り込み、請求書を作成できます。<br/>**`Intent Sale`** ( 以前 `Authorize and Capture` （以前のリリース） — 顧客のクレジットカードに対する資金はBraintreeが認証および取り込み、注文と請求書がストア管理者に作成されます。 |
| [!UICONTROL Sandbox Merchant ID] | ストア表示 | これは、サンドボックスゲートウェイアカウント全体の一意の識別子です。 別名 _パブリック ID_ または _実稼動 ID_&#x200B;の場合、マーチャント ID は実稼動用ゲートウェイとサンドボックスゲートウェイで異なります。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有の公開識別子です。 サンドボックスBraintreeゲートウェイに関連付けられた各ユーザーは、独自のサンドボックス公開鍵を持ちます。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有のプライベート識別子です。 サンドボックスBraintreeゲートウェイに関連付けられた各ユーザーは、サンドボックス用の独自の秘密鍵を持ちます。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Sandbox`. |
| [!UICONTROL Merchant ID] | ストア表示 | ゲートウェイに存在する複数のマーチャントアカウントを含め、ゲートウェイアカウント全体の一意の識別子です。 別名 _パブリック ID_ または _実稼動 ID_&#x200B;の場合、マーチャント ID は実稼動用ゲートウェイとサンドボックスゲートウェイで異なります。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Production`. |
| [!UICONTROL Public Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有の公開識別子です。 ユーザーゲートウェイに関連付けられている各Braintreeには、独自の公開鍵が割り当てられています。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Production`. |
| [!UICONTROL Private Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有のプライベート識別子です。 ユーザーゲートウェイに関連付けられている各Braintreeには、独自の秘密鍵が割り当てられています。 このフィールドは、 _[!UICONTROL Environment]_フィールドが `Production`. |
| [!UICONTROL Enable Card Payments] | Web サイト | 顧客がBraintreeクレジットカードの支払い方法を支払い方法として使用できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Web サイト | を有効にすると、は顧客の支払い情報を安全に保存できるので、顧客は購入ごとにクレジットカード情報を再入力する必要がありません。 オプション： `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Web サイト | 有効にすると、CVV ルールの設定がBraintree・アカウントで検証されます。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintreeの詳細設定](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Web サイト | 顧客カード情報が保存される Vault を識別する、参照用の説明的なタイトル。 |
| [!UICONTROL Merchant Account ID] | Web サイト | この Web サイトからのBraintreeトランザクションに関連付けるマーチャントアカウント ID。 空白の場合、Braintreeアカウントのデフォルトのマーチャントアカウントが使用されます。 |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Web サイト | 評価の一環としてトランザクションが送信されないようにします。 [!DNL Advanced Fraud Tools] チェック、管理を通じて行われた注文に対して、 `Yes`.<br/>オプション： `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Web サイト | `Advanced Fraud Protection` しきい値を満たしたり超えたりすると、チェックはバイパスされます。 このフィールドを空白にすると、このオプションは無効になります。 |
| [!UICONTROL Debug] | Web サイト | Braintreeシステムとストア間の通信をログファイルに記録するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL CVV Verification] | Web サイト | お客様がクレジットカードの後ろから 3 桁のセキュリティコードを提供する必要があるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Web サイト | すべての支払い方法の買い物かごの行項目を送信します。 オプション： `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Web サイト | Braintreeでの支払いとして受け入れる各クレジットカードを指定します。 長押し `Ctrl` ( または `Command` (Mac) をクリックして、カードの組み合わせを選択します。 オプション： `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にBraintreeが他の支払い方法と共に一覧表示される順序を決定します。 |

## [!UICONTROL Braintree Webhooks Settings]

![BraintreeWebhook 設定](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Web サイト | 詐欺保護、ACH 支払い、現地支払い方法に対するウェブフック機能を有効にする。 オプション： `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Web サイト | この URL を [!UICONTROL Webhook Destination URL]. **この URL は、セキュリティで保護され、公にアクセス可能である必要があります。** |
| [!UICONTROL Fraud Protection Approve Order Status] | Web サイト | 不正保護がBraintreeによって承認されると、選択した注文ステータスがコマース注文に割り当てられます。 このステータスは、ACH 支払い方法が使用される注文のステータスと、その注文が次の条件に移行する際に、更新するために使用されます `SETTLED` Braintree。 |
| [!UICONTROL Fraud Protection Reject Order Status] | Web サイト | 不正保護がBraintreeによって却下されると、選択した注文ステータスがコマース注文に割り当てられます。 このステータスは、ACH 支払い方法が使用される注文のステータスと使用時期を更新するために使用されます `SETTLEMENT` 次に該当 `DECLINED` Braintree。 |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![国固有の設定](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | すべての国からのBraintree処理済みの支払いを受け入れるか、特定の国のみを受け入れるかを決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 該当する場合、Braintreeで処理された支払を受け入れる国を識別します。 |
| [!UICONTROL Country Specific Credit Card Types] | Web サイト | Braintreeが処理した支払いに対して国ごとに受け入れられるクレジットカードを識別します。 レコードは国ごとに保存されます。 オプション： <br/>**`Country`**— 国を選択します。<br/>**`Allowed Card Types`**  — 国から受け入れられた各クレジットカードを、Braintreeを通じて支払いとして選択します。 <br/>**`Add`**— 別の国のクレジットカードを許可する行を追加します。<br/>**`Action`**  — その国で許可されているクレジットカードのレコードを削除します。 |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH スルーBraintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Web サイト | 次の場合に決定 [!DNL ACH Direct Debit] は、Braintreeを通じて支払い方法として含まれます。 オプション： `Yes` / `No` |
| [!UICONTROL Sort Order] | Web サイト | 順序を決定します。 [!DNL ACH Direct Debit] は、チェックアウト時に他の支払い方法と共に表示されます。 |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![AppleペイスルーBraintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Web サイト | Apple Pay が支払い方法としてBraintreeを通じて含まれるかどうかを決定します。 オプション： `Yes` / `No` <br/><br/> ドメインは、 [最初にBraintreeアカウントで検証済み](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | Web サイト | 支払が処理される際にBraintreeが実行するアクションを決定します。 オプション： <br/>**`Authorize`**・お客様のカードの資金は、認可されますが、お客様のアカウントからは移転されません。 ストア管理者で注文が作成されます。 後で販売を取り込み、請求書を作成できます。<br/>**`Intent Sale`**  — 顧客のカードの資金は、Braintreeが承認および取り込み、注文と請求書がストア管理者で作成されます。 **_注意：_** これは `Authorize and Capture` 2.3.x 以前のリリースでは、以下のことがおこなわれます。 |
| [!UICONTROL Merchant Name] | ストア表示 | ApplePay ポップアップで顧客に表示されるラベル。 |
| [!UICONTROL Sort Order] | Web サイト | Apple Pay がチェックアウト時に他の支払い方法と共に表示される順序を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![現地支払い方法](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Web サイト | 「現地支払い方法」が、支払い方法としてBraintreeを通じて含まれるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Title] | Web サイト | チェックアウトの支払い方法セクションに表示されるラベル。 デフォルト値： `Local Payments` |
| [!UICONTROL Allowed Payment Method] | Web サイト | 有効にするローカルの支払い方法を選択します。 オプション： `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` （未サポート） |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に、「現地支払い方法」が他の支払い方法と共に表示される順序を決定します。 |

{style="table-layout:auto"}

>[!NOTE]
>
>バンドルされたBraintree拡張は、 [Braintree開発者向けドキュメント](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). その他の現地支払い方法は、今後のリリースでサポートされる予定です。

## [!UICONTROL GooglePay through Braintree]

![GooglePay スルーBraintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Web サイト | 次の場合に決定 [!DNL Google Pay] 支払いは、支払い方法としてBraintreeを通じて含まれます。 オプション： `Yes` / `No` |
| [!UICONTROL Payment Action] | Web サイト | 支払が処理される際にBraintreeが実行するアクションを決定します。 オプション： <br/>**`Authorize`**・お客様のカードの資金は、認可されますが、お客様のアカウントからは移転されません。 ストア管理者で注文が作成されます。 後で販売を取り込み、請求書を作成できます。<br/>**`Intent Sale`**  — 顧客のカードの資金は、Braintreeが承認および取り込み、注文と請求書がストア管理者で作成されます。 **_注意：_** これは `Authorize and Capture` 2.3.x 以前のリリースでは、以下のことがおこなわれます。 |
| [!UICONTROL Button Color] | Web サイト | の色を決定します。 [!DNL Google Pay] 」ボタンをクリックします。 オプション： `White` / `Black` |
| [!UICONTROL Merchant ID] | ストア表示 | Googleから提供された ID をここに入力する必要があります。 |
| [!UICONTROL Accepted Cards] | Web サイト | 顧客が注文時に使用できるカードのタイプを選択します。 [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | Web サイト | Google Pay がチェックアウト時に他の支払い方法と共に表示される順序を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![ベンモスルーBraintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Web サイト | 次の場合に決定 [!DNL Venmo] は、Braintreeを通じて支払い方法として含まれます。 オプション： `Yes` / `No` |
| [!UICONTROL Payment Action] | Web サイト | 支払が処理される際にBraintreeが実行するアクションを決定します。 オプション： <br/>**`Authorize`**・お客様のカードの資金は、認可されますが、お客様のアカウントからは移転されません。 ストア管理者で注文が作成されます。 後で販売を取り込み、請求書を作成できます。<br/>**`Intent Sale`**  — 顧客のカードの資金は、Braintreeが承認および取り込み、注文と請求書がストア管理者で作成されます。 **_注意：_** これは  _許可してキャプチャ_ 2.3.x 以前のリリースでは、以下のことがおこなわれます。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に Venmo が他の支払い方法と共に一覧表示される順序を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal のBraintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Web サイト | PayPal が支払い方法としてBraintreeを通じて含まれるかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Web サイト | PayPal クレジットがBraintreeを通じて支払い方法として含まれるかどうかを指定します。 オプション： `Yes` / `No`. このフィールドは、 `Enable PayPal through Braintree` が `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Web サイト | PayPal PayLater を支払い方法としてBraintreeを通じて含めるかどうかを指定します。 オプション： `Yes` / `No`. このフィールドは、 `Enable PayPal through Braintree` が `Yes` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に顧客に対するBraintreeを通じて PayPal を識別するラベル。 デフォルト値： `PayPal` |
| [!UICONTROL Vault Enabled] | Web サイト | を有効にすると、は顧客の支払い情報を安全に保管できるので、顧客は購入ごとに PayPal 情報を再入力する必要がありません。 オプション： `Yes` / `No` |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に PayPal が他の支払い方法と共にBraintreeを通じて表示される順序を決定する数値。 |
| [!UICONTROL Override Merchant Name] | ストア表示 | 各店舗ビューのマーチャントを識別するために使用できる別名。 |
| [!UICONTROL Payment Action] | Web サイト | 支払い処理時に PayPal がBraintreeを通じて行うアクションを決定します。 オプション： <br/>**`Authorize`**・お客様のカードの資金は、認可されますが、お客様のアカウントからは移転されません。 ストア管理者で注文が作成されます。 後で販売を取り込み、請求書を作成できます。<br/>**`Authorize and Capture`**  — お客様のカード上の資金は、Braintreeを通じて PayPal によって認証および取得され、お客様のストア管理者で注文と請求書が作成されます。 |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | PayPal によって処理された支払いを、すべての国からのBraintreeを通じて受け入れるか、特定の国のみを受け入れるかを決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 該当する場合、Braintreeで処理された支払を受け入れる国を識別します。 |
| [!UICONTROL Require Customer's Billing Address] | Web サイト | 顧客の請求先住所が注文を送信するのに必要かどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Debug] | Web サイト | Braintreeシステムを介した PayPal とストア間の通信をログファイルに記録するかどうかを指定します。 オプション： `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Web サイト | PayPal ボタンが [ミニカート](../../stores-purchase/cart-configuration.md#mini-cart) また、 [買い物かご](../../stores-purchase/cart.md) ページに貼り付けます。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal のスタイル設定](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Location] | Web サイト | PayPal のボタンとメッセージをストアフロントでレンダリングする場所を決定します。 オプション： `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

このセクションのオプションと設定は、 _[!UICONTROL Location]_フィールドに入力します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Web サイト | ボタンを次の 3 つのタイプのいずれかに設定します。 `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

このセクションのオプションと設定は、 _[!UICONTROL PayPal Button Type]_フィールドに入力します。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Web サイト | 選択した場所での PayPal ボタンの位置を決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Button Label] | Web サイト | PayPal ボタンのラベルを決定します。 オプション： `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Web サイト | PayPal ボタンの色を指定します。 オプション： `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Web サイト | PayPal ボタンの形状を決定します。 オプション： `Pill` / `Rectangle` |
| [!UICONTROL Size] | Web サイト | PayPal ボタンのサイズを決定します。 オプション： `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Web サイト | 選択した場所での PayLater メッセージを有効にします。 オプション： `Yes` / `No`. 有効にすると、使用可能なオファー ([制限適用](https://developer.paypal.com/docs/checkout/pay-later/us/)) をクリックします。 |
| [!UICONTROL Message Layout] | Web サイト | PayLater メッセージのレイアウトを決定します。 オプション： `Text` / `Flex` |
| [!UICONTROL Logo] | Web サイト | PayPal ボタンに使用するロゴの種類を決定します。 オプション： `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Web サイト | PayPal ボタンのロゴの位置を指定します。 オプション： `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Web サイト | PayPal ボタンのテキストカラーを決定します。 オプション： `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

これらのオプションを設定すると、PayPal ボタンと PayLater メッセージのプレビューを確認できます。 設定を適用したり、値をリセットしたりする際に使用できるコントロールがあります。

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Apply] | Web サイト | ボタンと PayLater メッセージの選択したスタイル設定を格納し、現在の位置と現在のボタンの種類に適用します。 |
| [!UICONTROL Apply to All Buttons] | Web サイト | ボタンと PayLater メッセージの値に対して選択したスタイル設定を格納し、すべてのボタンの種類と位置に適用します。 |
| [!UICONTROL Reset to Recommended Defaults] | Web サイト | ボタンと PayLater メッセージの推奨既定値にスタイル設定を返し、すべてのボタンの種類と位置に適用します。 |

{style="table-layout:auto"}

## 3d セキュア検証設定

![3D セキュア検証設定](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Web サイト | 顧客が次のようなプログラムに登録されている場合に、トランザクションが追加の検証プロセスに合格する必要があるかどうかを指定します。 _VISA で検証_. オプション： `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Web サイト | すべてのトランザクションに対して、常に 3D セキュアリクエストにチャレンジします。 オプション： `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Web サイト | 1 回の注文で処理を許可する最大注文額を決定します。 Braintreeは、注文額がこのしきい値を超えた場合に、承認を却下します。 |
| [!UICONTROL Verify for Applicable Countries] | Web サイト | 支払いを検証する必要がある国を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Web サイト | 該当する場合、Braintree別の支払いを検証する必要がある特定の国を識別します。 |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![動的記述子](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Name] | ストア表示 | 名前記述子には 2 つの部分があり、アスタリスク (*) で区切られます。 記述子の最初の部分は会社または DBA を識別し、2 番目の部分は製品を識別します。 例： `company*myproduct`  <br/><br/>記述子の Company 部分と Product 部分の長さは、次の方法で割り当てることができます（22 文字までの長さの組み合わせ）。 <br/>**`Option 1`**— 会社は 3 文字でなければなりません/製品は最大 18 文字までです<br/>**`Option 2`**  — 会社は 7 文字でなければなりません/製品は最大 14 文字にする必要があります <br/>**`Option 3`**— 会社は 12 文字である必要があります/製品は最大 9 文字です |
| [!UICONTROL Phone] | ストア表示 | 電話記述子の長さは 10 ～ 14 文字で、数字、ダッシュ、括弧、ピリオドのみを含めることができます。 例： `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | ストア表示 | URL 記述子はドメイン名を表し、最大 13 文字まで指定できます。 例： `company.com` |

{style="table-layout:auto"}
