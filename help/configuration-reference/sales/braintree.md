---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] ページで、「[!UICONTROL Braintree]」セクションの設定を確認します。
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: d22d44b8c93649a60b16569cc502d2e291ce6b22
workflow-type: tm+mt
source-wordcount: '2621'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4 の移行：**<br/>
>Adobe CommerceとMagento Open Sourceが 2.4.0 より前のバージョンの場合、マーチャントは、コア統合の代わりに、公式のBraintree支払い統合拡張機能を ](https://marketplace.magento.com/catalogsearch/result/?q=braintree)0}Commerce Marketplace} からインストールして設定することをお勧めします。 [2.4.0 以降、拡張機能はコアリリースに含まれるようになりました。
><br/><br/>
>Commerce 2.4 に移行する場合、マーケットプレイス（`paypal/module-braintree` または `gene/module-braintree`）で配布されている拡張機能をアンインストールし、`Magento_Braintree` の代わりに `PayPal_Braintree` 名前空間を使用するようにコードをカスタマイズする必要があります。 Commerce用にバンドルされた拡張機能の設定とCommerce Marketplaceで配布された拡張機能は保持されます。 これらのバージョンの拡張機能で行われた支払いは、通常どおりキャプチャ、無効化、または払い戻されます。
><br/><br/>
>Commerce 2.4.0 にアップグレードする場合、以前の 2.3.x バージョンで推奨されるCommerce Marketplace拡張機能を使用しないと、マルチアドレス機能はBraintree 2.4.0 バージョンで動作しません。 買い物客が _複数のアドレスに配信_ を選択すると、Braintreeの支払い方法が表示されません。 2.3.x で以前に推奨したCommerce Marketplace拡張機能には、この複数のアドレスの問題があります。

{{config}}

>[!IMPORTANT]
>
>カードに予想外の料金が発生した場合は、[ サブスクリプションをキャンセル ](https://helpx.adobe.com/manage-account/using/cancel-subscription.html) ページでサポートを受けることができます。

## [!UICONTROL Basic Braintree Settings]

![Braintreeの基本設定 ](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | デフォルト値：`Credit Card` （Braintree） |
| [!UICONTROL Environment] | ストア表示 | オプション：`Sandbox` / `Production` |
| [!UICONTROL Payment Action] | ストア表示 | 支払いが処理されたときにBraintreeが実行するアクションを指定します。 オプション：<br/>**`Authorize`**– 顧客のクレジットカードの資金は許可されていますが、アカウントから転送されません。 注文はストア管理者で作成されます。 後で販売をキャプチャし、請求書を作成できます。<br/>**`Intent Sale`** （以前のリリースで `Authorize and Capture` 用） – 顧客のクレジットカードの資金は、Braintreeによって承認および取得され、ストア管理者に注文と請求書が作成されます。 |
| [!UICONTROL Sandbox Merchant ID] | ストア表示 | これは、サンドボックスゲートウェイアカウント全体の一意の ID です。 _パブリック ID_ または _実稼動 ID_ とも呼ばれ、マーチャント ID は実稼動ゲートウェイとサンドボックスゲートウェイで異なります。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Sandbox`」に設定されている場合に表示されます。 |
| [!UICONTROL Sandbox Public Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有の公開識別子です。 サンドボックス Braintree ゲートウェイに関連付けられた各ユーザーには、独自のサンドボックス公開鍵があります。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Sandbox`」に設定されている場合に表示されます。 |
| [!UICONTROL Sandbox Private Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有のプライベート識別子です。 サンドボックス Braintree ゲートウェイに関連付けられた各ユーザーは、サンドボックス用に独自の秘密鍵を持ちます。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Sandbox`」に設定されている場合に表示されます。 |
| [!UICONTROL Merchant ID] | ストア表示 | これは、ゲートウェイに存在する複数のマーチャントアカウントを含む、ゲートウェイアカウント全体の一意の ID です。 _パブリック ID_ または _実稼動 ID_ とも呼ばれ、マーチャント ID は実稼動ゲートウェイとサンドボックスゲートウェイで異なります。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Production`」に設定されている場合に表示されます。 |
| [!UICONTROL Public Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有の公開識別子です。 Braintree ゲートウェイに関連付けられた各ユーザーは、独自の公開鍵を持ちます。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Production`」に設定されている場合に表示されます。 |
| [!UICONTROL Private Key] | ストア表示 | これは、暗号化されたデータへのアクセスを制限する、ユーザー固有のプライベート識別子です。 Braintree Gateway に関連付けられた各ユーザーには、独自の秘密鍵があります。 このフィールドは、「_[!UICONTROL Environment]_」フィールドが「`Production`」に設定されている場合に表示されます。 |
| [!UICONTROL Enable Card Payments] | Web サイト | Braintreeのクレジットカードによる支払い方法が、お客様の支払い方法として利用可能かどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Web サイト | 有効にすると、は顧客の支払い情報を安全に保存できるので、顧客は購入ごとにクレジットカード情報を再入力する必要はありません。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Web サイト | 有効にすると、Braintree アカウントで設定された CVV ルールに対して検証が行われます。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintreeの詳細設定 ](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Web サイト | 顧客カード情報が保存されている Vault を識別する、参照用の説明的なタイトル。 |
| [!UICONTROL Merchant Account ID] | Web サイト | この web サイトからのBraintree取引に関連付けられるマーチャントアカウント ID。 空白の場合、Braintree アカウントのデフォルトのマーチャントアカウントが使用されます。 |
| [!UICONTROL Enable Checkout Express Payments] | Web サイト | PayPal、PayLater、Apple Pay、Google Pay など、チェックアウトプロセスの開始時に Express Payment オプションを使用して、より迅速にチェックアウトできます。 オプション：`Yes` / `No` |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Web サイト | `Yes` に設定されている場合にのみ、管理者を通じて行われた注文に対して、[!DNL Advanced Fraud Tools] チェックの一部として評価のためにトランザクションが送信されないようにします。<br/> オプション：`Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Web サイト | しきい値に達した場合や、しきい値を超えた場合、`Advanced Fraud Protection` のチェックがバイパスされます。 このフィールドを空白にすると、このオプションが無効になります。 |
| [!UICONTROL Debug] | Web サイト | Braintree システムとストア間のやり取りをログファイルに記録するかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL CVV Verification] | Web サイト | 顧客がクレジット カードの裏面から 3 桁のセキュリティ コードを提供する必要があるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Web サイト | すべての支払い方法の買い物かご品目を送信します。 オプション：`Yes` / `No` |
| [!UICONTROL Credit Card Types] | Web サイト | Braintree経由で支払いとして受け入れる各クレジットカードを指定します。 `Ctrl` キー（またはMacの `Command` キー）を押したままにして、カードの組み合わせを選択します。 オプション：`American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にBraintreeが他のお支払い方法と共にリストする注文を指定します。 |

## [!UICONTROL Braintree Webhooks Settings]

![Braintree Webhook の設定 ](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Web サイト | 詐欺保護、ACH 支払い、ローカル支払い方法、および紛争に対して Webhook 機能を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Web サイト | この URL を [!UICONTROL Webhook Destination URL] としてBraintree アカウントに追加します。 **この URL はセキュリティで保護され、公にアクセス可能である必要があります。** |
| [!UICONTROL Fraud Protection Approve Order Status] | Web サイト | 不正防止がBraintreeによって承認されると、選択された注文ステータスがCommerceの注文に割り当てられます。 このステータスは、ACH 支払い方法が使用されている注文のステータスと、Braintreeでの `SETTLED` 行のタイミングを更新するために使用されます。 |
| [!UICONTROL Fraud Protection Reject Order Status] | Web サイト | Braintreeによって不正防止が拒否されると、選択された注文ステータスがCommerce注文に割り当てられます。 このステータスは、ACH 支払い方法が使用されている注文のステータスと、Braintreeで `SETTLEMENT` が使用さ `DECLINED` ている注文のステータスを更新するために使用されます。 |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![ 国別設定 ](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | Braintreeで処理される支払いをすべての国から受け入れるか、特定の国からのみ受け入れるかを指定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 該当する場合、Braintreeで処理される支払いを受け入れる特定の国を識別します。 |
| [!UICONTROL Country Specific Credit Card Types] | Web サイト | Braintreeで処理される支払いに対して、国ごとに受け入れられるクレジットカードを識別します。 レコードは国ごとに保存されます。 オプション：<br/>**`Country`**– 国を選択します。<br/>**`Allowed Card Types`** - Braintreeを通じて支払いとして国から受け入れる各クレジットカードを選択します。 <br/>**`Add`**– 別の国のクレジットカードを許可する行を追加します。<br/>**`Action`** – 許可されている国のクレジットカードの記録を削除します。 |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH からBraintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Web サイト | Braintreeを通じて支払い方法として [!DNL ACH Direct Debit] を含めるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Vault for ACH Direct Debit] | Web サイト | お客様は、将来の使用のために、使い捨ての ACH 口座引落し支払方法をヴォールティング/保存できます。 支払詳細がヴォールトされると、お客様はデータの再入力や支払情報の再認証を行うことなく、ACH 口座引落し支払方法を使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に他の支払い方法 [!DNL ACH Direct Debit] 一緒にリストされる順序を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Braintree経由のApple Pay](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Web サイト | Braintreeを通じてApple Pay を支払い方法として含めるかどうかを決定します。 オプション：`Yes` / `No` <br/><br/> ドメインを [ 最初にBraintree アカウントで検証 ](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) する必要があります。 |
| [!UICONTROL Enable Vault for ApplePay] | Web サイト | お客様は、今後の使用のためにApple Pay の支払い方法をヴォールティング/保存できます。 支払い情報が保管されると、お客様はデータを再入力したり、支払い情報を再認証したりすることなく、Apple Pay を使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Payment Action] | Web サイト | 支払いが処理されたときにBraintreeが実行するアクションを指定します。 オプション：<br/>**`Authorize`**– 顧客のカードの資金は許可されていますが、顧客のアカウントから転送されません。 注文はストア管理者で作成されます。 後で販売をキャプチャし、請求書を作成できます。<br/>**`Intent Sale`** – 顧客のカードの資金はBraintreeによって承認および取得され、注文と請求書はストア管理で作成されます。 **_メモ：_** これは 2.3.x 以前のリリースで `Authorize and Capture` 行されました。 |
| [!UICONTROL Merchant Name] | ストア表示 | ApplePay ポップアップで顧客に表示されるラベル。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にApple Pay が他の支払い方法と共にリストされる注文を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![ 現地支払の方法 ](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Web サイト | Braintreeを通じて現地の支払方法を支払方法として含めるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | Web サイト | チェックアウト時の支払い方法セクションに表示されるラベル。 デフォルト値：`Local Payments` |
| [!UICONTROL Fallback Button Text] | Web サイト | 顧客を web サイトに戻すフォールバック Braintree ページに表示されるボタンに使用するテキストを入力します。 デフォルト値：`Complete Checkout` |
| [!UICONTROL Redirect on Fail] | Web サイト | ローカルの支払方法トランザクションが取り消された場合、失敗した場合、またはエラーが発生した場合に顧客がリダイレクトされる URL を指定します。 チェックアウト支払いページにする必要があります（例：`https://www.domain.com/checkout#payment`）。 |
| [!UICONTROL Allowed Payment Method] | Web サイト | 有効化するローカルの支払方法を選択します。 オプション：`Bancontact`/`EPS`/`giropay`/`iDeal`/`Klarna Pay Now`/`SOFORT`/`MyBank`/`P24`/`SEPA/ELV Direct Debit` （まだサポートされていません） |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にローカル支払方法が他の支払方法と共に一覧表示される順序を決定します。 |

{style="table-layout:auto"}

>[!NOTE]
>
>バンドルされたBraintree拡張機能は、[Braintree開発者向けドキュメント ](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview) にリストされているすべてのローカル支払い方法をサポートしているわけではありません。 今後のリリースでサポートされる予定の、その他の地域での支払い方法も開発中です。

## [!UICONTROL GooglePay through Braintree]

![Braintreeを使用した GooglePay](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Web サイト | お支払いがBraintree[!DNL Google Pay] 支払い方法として含まれるかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Vault for GooglePay] | Web サイト | お客様は、今後の使用のためにGoogle Pay の支払い方法をヴォールティング/保存できます。 支払い情報が保管されると、お客様はデータを再入力したり、支払い情報を再認証したりすることなく、Google Pay を使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Payment Action] | Web サイト | 支払いが処理されたときにBraintreeが実行するアクションを指定します。 オプション：<br/>**`Authorize`**– 顧客のカードの資金は許可されていますが、顧客のアカウントから転送されません。 注文はストア管理者で作成されます。 後で販売をキャプチャし、請求書を作成できます。<br/>**`Intent Sale`** – 顧客のカードの資金はBraintreeによって承認および取得され、注文と請求書はストア管理で作成されます。 **_メモ：_** これは 2.3.x 以前のリリースで `Authorize and Capture` 行されました。 |
| [!UICONTROL Button Color] | Web サイト | [!DNL Google Pay] ボタンの色を決定します。 オプション：`White` / `Black` |
| [!UICONTROL Merchant ID] | ストア表示 | Googleから提供された ID をここに入力する必要があります。 |
| [!UICONTROL Accepted Cards] | Web サイト | [!DNL Google Pay] を使用して顧客が注文に使用できるカードのタイプを選択します。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にGoogle Pay が他の支払い方法と共にリストされる注文を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo からBraintreeへ ](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Web サイト | Braintreeを通じて支払い方法として [!DNL Venmo] を含めるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable Vault for Venmo] | Web サイト | お客様は、将来の使用のために Venmo 支払い方法をヴォールティング/保存できます。 支払いの詳細が保管されると、お客様はデータを再入力したり、支払い情報を再認証したりすることなく、Venmo 支払い方法を使用できます。 オプション：`Yes` / `No` |
| [!UICONTROL Payment Action] | Web サイト | 支払いが処理されたときにBraintreeが実行するアクションを指定します。 オプション：<br/>**`Authorize`**– 顧客のカードの資金は許可されていますが、顧客のアカウントから転送されません。 注文はストア管理者で作成されます。 後で販売をキャプチャし、請求書を作成できます。<br/>**`Intent Sale`** – 顧客のカードの資金はBraintreeによって承認および取得され、注文と請求書はストア管理で作成されます。 **_メモ：_** これは、2.3.x 以前のリリースでは _承認してキャプチャ_ されていました。 |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時に Venmo が他の支払い方法と共にリストされる順序を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![Braintree経由の PayPal](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Web サイト | PayPal をBraintree経由の支払い方法として含めるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Web サイト | PayPal クレジットをBraintree経由の支払い方法として含めるかどうかを決定します。 オプション：`Yes`/`No`。 このフィールドは、`Enable PayPal through Braintree` を `Yes` に設定すると表示されます |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Web サイト | PayPal PayLater をBraintree経由の支払い方法として含めるかどうかを決定します。 オプション：`Yes`/`No`。 このフィールドは、`Enable PayPal through Braintree` を `Yes` に設定すると表示されます |
| [!UICONTROL Title] | ストア表示 | チェックアウト時にBraintreeを通じてお客様に PayPal を識別するラベル。 デフォルト値：`PayPal` |
| [!UICONTROL Vault Enabled] | Web サイト | 有効にすると、顧客の支払い情報の安全なストレージが提供されるので、顧客は購入ごとに PayPal 情報を再入力する必要がなくなります。 オプション：`Yes` / `No` |
| [!UICONTROL Send Cart Line Items for PayPal] | Web サイト | 明細（注文品目）を PayPal に送信し、明細としてギフトカード、商品用のギフトラッピング、注文用のギフトラッピング、ストクレジット、送料、税金を送信します。 オプション：`Yes` / `No` |
| [!UICONTROL Sort Order] | Web サイト | チェックアウト時にBraintreeを通じて PayPal が他のお支払い方法と一緒にリストされる順序を決定する数値です。 |
| [!UICONTROL Override Merchant Name] | ストア表示 | 各店舗表示の販売者を識別するために使用できる代替名。 |
| [!UICONTROL Payment Action] | Web サイト | 支払い処理時にBraintreeを通じて PayPal が実行するアクションを指定します。 オプション：<br/>**`Authorize`**– 顧客のカードの資金は許可されていますが、顧客のアカウントから転送されません。 注文はストア管理者で作成されます。 後で販売をキャプチャし、請求書を作成できます。<br/>**`Authorize and Capture`** – 顧客のカードの資金は、Braintreeを通じて PayPal によって承認および取得され、注文と請求書はストア管理で作成されます。 |
| [!UICONTROL Payment from Applicable Countries] | Web サイト | PayPal によって処理される支払いを、すべての国からBraintreeを通じて受け入れるか、特定の国からのみ受け入れるかを指定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Web サイト | 該当する場合、Braintreeで処理される支払いを受け入れる特定の国を識別します。 |
| [!UICONTROL Require Customer's Billing Address] | Web サイト | 注文を送信するために顧客の請求先住所が必要かどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Debug] | Web サイト | Braintree システムを通じた PayPal とストア間のやり取りをログファイルに記録するかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Web サイト | PayPal ボタンを [ ミニ カート ](../../stores-purchase/cart-configuration.md#mini-cart) および [ 買い物かご ](../../stores-purchase/cart.md) ページに表示するかどうかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

>[!NOTE]
>
>**[!DNL PayPal Credit]** または **[!DNL PayPal PayLater]** のいずれかを有効にできます。 両方のメソッドを同時に有効にすることはできません。

### [!UICONTROL Styling]

![PayPal スタイル設定 ](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Location] | Web サイト | PayPal ボタンとメッセージがストアフロントでレンダリングされる場所を決定します。 オプション：`Mini-Cart and Cart Page`/`Checkout Page`/`Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

このセクションのオプションと設定は、_[!UICONTROL Location]_フィールドの設定によって異なります。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Web サイト | ボタンを `PayPal Button`/`PayPal Pay Later Button`/`PayPal Credit Button` の 3 つのタイプのいずれかに設定します。 |

**[!UICONTROL PayPal Button]**

このセクションのオプションと設定は、「_[!UICONTROL PayPal Button Type]_」フィールドで選択したボタンタイプによって異なります。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Web サイト | 選択した位置での PayPal ボタンの位置を決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Button Label] | Web サイト | PayPal ボタンのラベルを決定します。 オプション：`Paypal`/`Checkout`/`Buy Now`/`Pay` |
| [!UICONTROL Color] | Web サイト | PayPal ボタンの色を決定します。 オプション：`Blue`/`Black`/`Gold`/`Silver` |
| [!UICONTROL Shape] | Web サイト | PayPal ボタンの形状を決定します。 オプション：`Pill` / `Rectangle` |
| [!UICONTROL Size(Deprecated)] | Web サイト | PayPal ボタンのサイズを決定します。 オプション：`Medium`/`Large`/`Responsive` |

{style="table-layout:auto"}

>[!NOTE]
>
>**[!DNL Size(Deprecated)]** 設定フィールドは非推奨となり、PayPal ボタンのスタイル設定には使用されません。

**[!UICONTROL PayLater Messaging]**

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Web サイト | 選択した場所で PayLater メッセージを有効にします。 オプション：`Yes`/`No`。 有効化すると、利用可能なオファーに関する PayLater メッセージが表示されます（[ 制限あり ](https://developer.paypal.com/docs/checkout/pay-later/us/)）。 |
| [!UICONTROL Message Layout] | Web サイト | PayLater メッセージレイアウトを決定します。 オプション：`Text` / `Flex` |
| [!UICONTROL Logo] | Web サイト | PayPal ボタンに使用するロゴのタイプを決定します。 オプション：`Inline`/`Primary`/`Alternative`/`None` |
| [!UICONTROL Logo Position] | Web サイト | PayPal ボタンのロゴの位置を決定します。 オプション：`Left`/`Right`/`Top` |
| [!UICONTROL Text Color] | Web サイト | PayPal ボタンのテキストカラーを決定します。 オプション：`Black`/`White`/`Monochrome`/`Grayscale` |

{style="table-layout:auto"}

これらのオプションを設定すると、PayPal ボタンと PayLater メッセージのプレビューが表示されます。 設定の適用や値のリセットに使用できるコントロールがあります。

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Apply] | Web サイト | ボタンおよび PayLater メッセージング用に選択したスタイル設定を格納し、現在の場所および現在のボタンタイプに適用します。 |
| [!UICONTROL Apply to All Buttons] | Web サイト | ボタンおよび PayLater メッセージング値に対して選択したスタイル設定を格納し、すべてのボタンタイプおよび場所にそれらの設定を適用します。 |
| [!UICONTROL Reset to Recommended Defaults] | Web サイト | スタイル設定を、ボタンおよび PayLater メッセージに推奨されるデフォルト値に戻し、すべてのボタンタイプおよび場所に適用します。 |

{style="table-layout:auto"}

## 3d セキュア検証設定

![3D セキュア検証設定 ](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Web サイト | 顧客が _VISA による検証_ などのプログラムに登録されている場合、トランザクションが追加の検証プロセスをパスする必要があるかどうかを決定します。 オプション：`Yes` / `No` |
| [!UICONTROL Always request 3DS] | Web サイト | すべてのトランザクションに対して常に 3D Secure リクエストにチャレンジします。 オプション：`Yes` / `No` |
| [!UICONTROL Threshold Amount] | Web サイト | 単一の注文での処理が許可されている最大注文額を決定します。 注文金額がこのしきい値の金額を超えると、Braintreeは認証を拒否します。 |
| [!UICONTROL Verify for Applicable Countries] | Web サイト | 支払いを確認する必要がある国を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Web サイト | 該当する場合、Braintreeによる支払いを検証する必要がある具体的な国を特定します。 |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![ 動的記述子 ](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Name] | ストア表示 | 名前記述子には 2 つの部分があり、アスタリスク（*）で区切られています。 記述子の最初の部分は会社または DBA を示し、2 番目の部分は製品を示します。 例：`company*myproduct` <br/><br/> 記述子の会社と製品の部分の長さは、次のように合計 22 文字まで割り当てることができます。<br/>**`Option 1`**– 会社は 3 文字である必要があります/製品は 18 文字まで可能です<br/>**`Option 2`** – 会社は 7 文字である必要があります/製品は 14 文字まで可能です <br/>**`Option 3`**– 会社は 12 文字である必要があります/製品は 9 文字まで可能です |
| [!UICONTROL Phone] | ストア表示 | Phone 記述子の長さは 10 ～ 14 文字で、数字、ダッシュ、括弧、ピリオドのみを使用できます。 例：`9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | ストア表示 | URL 記述子はドメイン名を表し、最大 13 文字にすることができます。 例：`company.com` |

{style="table-layout:auto"}
