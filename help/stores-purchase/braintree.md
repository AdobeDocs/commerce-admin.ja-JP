---
title: Braintree
description: ストアでオンライン支払いソリューションとしてBraintreeを設定する方法を説明します。
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintreeは、不正検知と PayPal 統合により、完全にカスタマイズ可能なチェックアウトエクスペリエンスを提供します。 をサポートします [!DNL Apple Pay], [!DNL Google Pay]、ACH、Venmo およびローカル支払い方法。 BraintreeはBraintreeシステムで行われるので、マーチャントの PCI コンプライアンスに関する負担を軽減できます。 Braintree支払いの統合は、次の方法で開発されました。 [ジーンCommerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>以前のバージョンのAdobe CommerceまたはCommerce MarketplaceのBraintree拡張機能がインストールされたMagento Open Sourceから 2.4.x にアップグレードする場合は、を参照してください [2.4 アップグレードノート](#24-upgrade-notes) このページの最後


## 手順 1:Braintree資格情報を取得する

に移動 [Braintree支払い][1] アカウントに新規登録します。

## 手順 2：基本設定を完了する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

   - Commerceのインストールに複数の web サイト、ストア、ビューがある場合は、左上隅にある **[!UICONTROL Store View]** 設定が適用される場所。

   - が含まれる _[!UICONTROL Merchant Location]_セクションで、次のことを確認します&#x200B;**[!UICONTROL Merchant Country]**は、ビジネスの場所に設定されます。

1. 次の下 _[!UICONTROL Recommended Solutions]_、内_[!UICONTROL Braintree Payments] （基準： [ジーンCommerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [リリースノート](https://support.gene.co.uk/support/solutions/articles/35000228529)_セクションで、をクリック&#x200B;**[!UICONTROL Configure]**.

   ![Braintreeの設定](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**&#x200B;を入力し、チェックアウト時に支払いオプションとしてBraintreeを識別するタイトルを入力します。

1. 現在の操作を設定 **[!UICONTROL Environment]** Braintree取引の対象 `Sandbox` または `Production`

   サンドボックスで設定をテストする場合は、のみを使用します [クレジットカード番号][2] Braintreeが推奨します。 Braintreeを使用して実稼動に移行する準備ができたら、次のように設定します **[!UICONTROL Environment]** 対象： `Production`.

   ![基本資格情報設定](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only`  – 購入を承認し、資金を保留します。 金額は、セールが行われるまで、顧客の銀行口座から引き出されません _キャプチャ済み_ 商人による。|
   - `Intent Sale`   – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。 **_注意：_** この値  _認証とキャプチャ_ 2.3.x 以前のリリース。|

1. を入力 **[!UICONTROL Sandbox Merchant ID / Merchant ID]** Braintreeアカウントから。

1. Braintreeアカウントから次の資格情報を入力します。

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >両方のフィールドが別々にあります **（サンドボックスと実稼動）** 環境、およびその他のフィールドは、選択した環境に基づいてレンダリングされます。

1. 設定を保存する前に、 **[!UICONTROL Validate Credentials]** をクリックして認証情報を検証します。

1. を設定 **[!UICONTROL Enable Card Payments]** 対象： `Yes`.

   ![Basic Settings](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   顧客情報を安全に保存する機能が必要なので、顧客が購入するたびに情報を再入力する必要がない場合は、次のように設定します **[!UICONTROL Enable Vault for Card Payments]** 対象： `Yes`.

## 手順 3：詳細設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Braintree Settings]** セクション。

   ![詳細設定](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. の場合 **[!UICONTROL Vault Title]**&#x200B;を入力し、顧客カード情報が保存されている Vault を識別する参照の説明的なタイトルを入力します。

1. を入力 **[!UICONTROL Merchant Account ID]** Braintreeアカウントから。

   使用するマーチャントアカウントを指定しない場合、Braintreeはデフォルトのマーチャントアカウントを使用して取引を処理します。

1. PayPal、PayLater、Apple Pay、Google Pay など、チェックアウトプロセスの開始時に Express Payment オプションを使用して、より迅速にチェックアウトをおこなえるようにします。 **[!UICONTROL Enable Checkout Express Payments]** 対象： `Yes`.

1. 高度な不正ツールのチェックの一環として評価のためにトランザクションが送信されないようにするには、管理者を通じて行われた注文に対して、次のように設定します **[!UICONTROL Skip Fraud Checks on Admin Orders]** 対象： `Yes`.

1. を **[!UICONTROL Bypass Fraud Protection Threshold]** その結果、 `Advanced Fraud Protection` しきい値に達した、またはしきい値を超えた場合、チェックはバイパスされます。

   このフィールドを空白にすると、このオプションが無効になります。

1. ストアとBraintree間のやり取りのログファイルを保存する場合は、次のように設定します。 **[!UICONTROL Debug]** 対象： `Yes`.

1. クレジットカードの裏面から 3 桁のセキュリティコードを提供するよう顧客に要求するには、次のように設定します **[!UICONTROL CVV Verification]** 対象： `Yes`.

   CVV 検証を使用する場合は、で AVS や CVV を必ず有効にします。 _設定/処理_ Braintreeアカウントの「」セクション。

1. すべての支払方法に対してカート品目を送信するには、次のように設定します **[!UICONTROL Send Card Line Items]** 対象： `Yes`.

1. の場合 **[!UICONTROL Credit Card Types]**&#x200B;で、Braintreeを通じて支払いとしてストアで受け入れられる各クレジットカードを選択します。

   複数のカードの種類を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の支払い方法と一緒にリストされたときにBraintreeが表示される順序を決定します。

## 手順 4:BraintreeWebhook を設定する

![Braintree Webhook の設定](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable Webhook]** 対象： `Yes` 詐欺保護、ACH 支払いおよびローカル支払い方法の Webhook 機能を有効にします。

1. URL をにコピー **[!UICONTROL Fraud Protection URL]** フィールドに入力し、Braintreeアカウントに _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >この URL はセキュリティで保護され、公開アクセス可能である必要があります。

1. を **[!UICONTROL Fraud Protection Approve Order Status]** Braintreeが不正防止を承認するタイミングを決定するフィールド。

   選択した注文ステータスがCommerceの注文に割り当てられます。

1. を **[!UICONTROL Fraud Protection Reject Order Status]** Braintreeにより不正防止が拒否された場合に判断するためのフィールド。

   選択した注文ステータスがCommerceの注文に割り当てられます。

## 手順 5：国固有の設定の完了

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー（PC）または Command キー（Mac）を押しながら、リスト内で、お客様がストアから購入できる国を選択します。

   ![国固有の設定](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. を設定するには **[!UICONTROL Country Specific Credit Card Types]**:

   - クリック **[!UICONTROL Add]**.

   - を **[!UICONTROL Country]** およびを選択します **[!UICONTROL Allowed Credit Card Type]**.

   - 繰り返して、各国から受け入れるクレジットカードを識別します。

## 手順 6:Braintreeを使用して ACH を設定する

![Braintreeによる ACH](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. ACH をBraintreeの支払いオプションとして含めるには、次のように設定します **[!UICONTROL Enable ACH Direct Debit]** 対象： `Yes`.

1. お客様は、1 回限りの ACH Direct Debit 支払い方法をヴォールティングし、将来の使用のために保存できます。 ヴォールト後、お客様は、設定されている場合に支払情報を再入力または認証する必要なく、ACH 口座引落しを再利用できます **[!UICONTROL Enable Vault for ACH Direct Debit]** 対象： `Yes`.

1. の場合 **[!UICONTROL Sort Order]**&#x200B;数字を入力して、チェックアウト時に他の支払い方法と一緒に表示されるBraintreeACH 支払い方法の表示順序を指定します。

## 手順 7：を完了する [!UICONTROL Apple Pay] Braintree設定を使用

![Braintree設定を使用した ApplePay](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. 次を含める [!DNL Apple Pay] Braintree付き支払いオプションとして、を設定します **[!UICONTROL Enable ApplePay through Braintree]** 対象： `Yes`.

   必ずしてください [ドメイン名の確認](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) まずBraintreeアカウントから。

1. お客様の情報を安全に保存し、Apple Pay で購入するたびに再入力する必要がない場合は、次のように設定します。 **[!UICONTROL Enable Vault for ApplePay]** 対象： `Yes`.

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only`  – 購入を承認し、資金を保留します。 金額は、セールが行われるまで、顧客の銀行口座から引き出されません _キャプチャ済み_ 商人によって。
   - `Intent Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. の場合 **[!UICONTROL Merchant Name]**&#x200B;に入力します。このテキストは、Apple Pay ダイアログで顧客に表示されるラベルを指定します。

1. の場合 **[!UICONTROL Sort Order]**：以下の条件を満たす順序を決定する番号を入力 [!DNL Apple Pay] 支払いオプションは、チェックアウト時に他の支払いオプションと一緒にリストされたときに表示されます。

## 手順 8：現地の支払方法の設定を完了する

1. Braintree付きの支払いオプションとしてローカル支払方法を含めるには、次のように設定します **[!UICONTROL Enable Local Payment Methods]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、「チェックアウトの支払方法」セクションに表示されるラベルに使用するテキストを入力します（デフォルト値： `Local Payments`）に設定します。

1. の場合 **[!UICONTROL Fallback Button Text]**&#x200B;に、フォールバックBraintreeページに表示され、顧客を web サイトに戻すためのボタンに使用するテキストを入力します（例： `Complete Checkout`）に設定します。

1. の場合 **[!UICONTROL Redirect on Fail]**&#x200B;を入力します。この URL では、ローカル支払方法トランザクションがキャンセル、失敗、またはエラーが発生した場合に顧客をリダイレクトする必要があります。 チェックアウト支払いページにする必要があります（例： `https://www.domain.com/checkout#payment`）に設定します。

1. の場合 **[!UICONTROL Allowed Payment Methods]**&#x200B;を選択し、有効にする現地の支払方法を選択します。

   オプション： `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` （まだサポートされていません）

   ![ローカル支払方法の設定](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >バンドルされたBraintree拡張機能は、にリストされているすべてのローカル支払い方法をサポートしているわけではありません [Braintree開発者向けドキュメント](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). 今後のリリースでサポートされる予定の、その他の地域での支払い方法も開発中です。

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の支払いオプションと一緒にリストされたときにローカルの支払い方法が表示される順序を決定します。

## 手順 9：を完了する [!DNL Google Pay] Braintree設定を使用

![Google ペイ スルーBraintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. 次を含める [!DNL Google Pay] Braintree付き支払いオプションとして、を設定します **[!UICONTROL Enable GooglePay Through Braintree]** 対象： `Yes`.

1. お客様の情報を安全に保存し、Google Pay で購入するたびに再入力する必要がない場合は、次のように設定します。 **[!UICONTROL Enable Vault for GooglePay]** 対象： `Yes`.

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only`  – 購入を承認し、資金を保留します。 金額は、セールが行われるまで、顧客の銀行口座から引き出されません _キャプチャ済み_ 商人によって。
   - `Intent Sale`   – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. を設定 **[!UICONTROL Button Color]** の色を決定するには [!DNL Google Pay] ボタン： `White` または `Black`

1. の場合 **[!UICONTROL Merchant ID]**&#x200B;を入力し、MerchantID を入力します（Googleが提供）。

1. の場合 **[!UICONTROL Accepted Cards]**&#x200B;を使用して、顧客が注文に使用できるカードのタイプを選択します [!DNL Google Pay].

   オプション： `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. の場合 **[!UICONTROL Sort Order]**：以下の条件を満たす順序を決定する番号を入力 [!DNL Google Pay] は、チェックアウト時に他のお支払いオプションと一緒にリストされたときに表示されます。

## 手順 10:Braintreeを使用して Venmo を設定する

1. Venmo をBraintreeの支払いオプションとして含めるには、次のように設定します **[!UICONTROL Enable Venmo through Braintree]** 対象： `Yes`.

1. を設定 **[!UICONTROL Enable Vault for Venmo]** 対象： `Yes` 安全な Vault を使用して顧客の Venmo アカウントを保存できるようにして、顧客が今後のトランザクションで Venmo アカウントに再度ログインする必要がないようにする。

   ![Braintreeによるベンモ](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only`  – 購入を承認し、資金を保留します。 金額は、セールが行われるまで、顧客の銀行口座から引き出されません _キャプチャ済み_ 商人によって。
   - `Intent Sale`   – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の支払いオプションと共にリストされたときに Venmo が表示される順序を決定します。

## 手順 11:Braintreeを使用して PayPal を設定する

![Braintree設定を使用した PayPal](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. PayPal をBraintreeの支払いオプションとして含めるには、次のように設定します **[!UICONTROL Enable PayPal through Braintree]** 対象： `Yes`.

1. Braintreeの支払い方法で PayPal を指定してください：

   >[!NOTE]
   >
   >次のいずれか **[!DNL PayPal Credit]** または **[!DNL PayPal PayLater]** を有効にできます。 両方のメソッドを同時に有効にすることはできません。

   - 次を含める [!DNL PayPal Credit] Braintree付き支払いオプションとして、を設定します **[!UICONTROL Enable PayPal Credit through Braintree]** 対象： `Yes`.

     条件 **Braintreeによる PayPal の有効化** はに設定されています。 `Yes`このフィールドのみが表示されます。

     >[!NOTE]
     >
     >PayPal クレジットは米国および英国でのみ利用できます。 に対して選択した値の場合、PayPal クレジットは無効になります _[!UICONTROL Merchant Country]_フィールドが `US` または `UK`.

   - 次を含める [!DNL PayPal PayLater] Braintree付き支払いオプションとして、を設定します **[!UICONTROL Enable PayPal PayLater through Braintree]** 対象： `Yes`.

     条件 **[!UICONTROL Enable PayPal PayLater through Braintree]** はに設定されています。 `Yes`このフィールドのみが表示されます。

     次のようなオファーに対しては、サイトに PayLater メッセージを表示できます _3 で支払う_&#x200B;お客様は、このオプションを使用して、毎月無利子で 3 回の支払いを行うことができます。 Braintree統合では、この機能を宣伝するために、サイトにメッセージを表示できます。 PayLater オファーを、他のコンテンツ、マーケティングまたはマテリアルでプロモーションすることはできません。

1. の場合 **[!UICONTROL Title]**&#x200B;を入力し、チェックアウト時に PayPal オプションでBraintree支払いを識別するタイトルを入力します。

1. を設定 **[!UICONTROL Vault Enabled]** 対象： `Yes` 安全な保管庫を使用して顧客の PayPal アカウントを保存できるようにする。 ヴォールティングされた PayPal アカウントは、将来のトランザクションに使用でき、顧客のステップ数を減らすことができます。

1. を設定 **[!UICONTROL Send Cart Line Items for PayPal]** 対象： `Yes` 明細（受注品目）を PayPal に送信する際に、明細としてギフトカード、品目のギフトラッピング、注文のギフトラッピング、ストクレジット、出荷、税金を送信します。

1. の場合 **[!UICONTROL Sort Order]**&#x200B;数字を入力して、チェックアウト時に他のお支払い方法と一緒に表示されるBraintreePayPal 支払い方法の表示順序を指定します。

1. で定義されている商社名とは異なる商社名を表示するには [ストアの設定](../getting-started/store-details.md#store-information)に名前を入力します **[!UICONTROL Override Merchant Name]** 必要に応じて表示するフィールド。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only`  – 購入を承認し、資金を保留します。 金額は、セールが行われるまで、顧客の銀行口座から引き出されません _キャプチャ済み_ 商人によって。
   - `Authorize and Capture`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. を設定 **[!UICONTROL Payment from Applicable Countries]** PayPal で処理されるBraintree取引に対して、以下のいずれかに該当すること：

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー（PC）または Command キー（Mac）を押しながら、リスト内で、お客様がストアから購入できる国を選択します。

1. 顧客に請求先住所の指定を要求するには、を設定します **[!UICONTROL Require Customer's Billing Address]** 対象： `Yes`.

   >[!NOTE]
   >
   >この機能は、PayPal テクニカルサポートがお使いのアカウントで有効にする必要があります。

1. Braintreeを使用してストアと PayPal 間のインタラクションのログファイルを保存するには、次のように設定します **[!UICONTROL Debug]** 対象： `Yes`.

1. ミニカートと買い物かごページの両方に PayPal ボタンを表示するには、次のように設定します **[!UICONTROL Display on Shopping Cart]** 対象： `Yes`.

## 手順 12：スタイル設定を指定する

1. の場合 **[!UICONTROL Location]**&#x200B;で、PayPal ボタンとメッセージのレンダリング先を選択します。 `Mini-Cart and Cart Page`, `Checkout Page`、または `Product Page`

   ![PayPal スタイル設定](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

このセクションのオプションと設定は、の設定によって異なります _[!UICONTROL Location]_フィールド。

1. を設定 **[!UICONTROL PayPal Button Type]** 次の 3 種類のボタンのいずれかに割り当てます。 `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

このセクションのオプションと設定は、 _[!UICONTROL PayPal Button Type]_フィールド。

1. 選択した場所のストアフロントに PayPal ボタンを表示するには、を設定します **[!UICONTROL Show PayPal Button]** 対象： `Yes`.

1. の場合 **[!UICONTROL Button Label]**&#x200B;を選択し、「PayPal」ボタンラベルを選択します。 `Paypal`, `Checkout`, `Buynow`、または `Pay`

1. の場合 **[!UICONTROL Color]**&#x200B;で、PayPal ボタンの色を選択します。 `Blue`, `Black`, `Gold`、または `Silver`

1. の場合 **[!UICONTROL Shape]**&#x200B;の場合は、[PayPal ボタン ] 図形を選択します。 `Pill` または `Rectangle`

1. の場合 **[!UICONTROL Size (Deprecated)]**&#x200B;を選択し、PayPal ボタンのサイズを選択します。 `Medium`, `Large`、または `Responsive`

>[!NOTE]
>
>この **[!DNL Size(Deprecated)]** 設定フィールドは非推奨で、PayPal ボタンのスタイル設定には使用されていません。

**[!UICONTROL PayLater Messaging]**

1. 表示対象 [!DNL PayLater] 選択した場所のストアフロントでのメッセージ、を設定 **[!UICONTROL Show PayLater Messaging]** 対象： `Yes`.

   このメッセージには、次の項目が表示されます [!DNL PayLater] 使用可能なオファーのメッセージング （[制限が適用されます](https://developer.paypal.com/docs/checkout/pay-later/us/)）に設定します。

1. の場合 **[!UICONTROL Message Layout]**&#x200B;を選択し、 [!DNL PayLater] メッセージのレイアウト： `Text` または `Flex`

1. の場合 **[!UICONTROL Logo]**&#x200B;で、PayPal ロゴのタイプを選択します。 `Inline`, `Primary`, `Alternative`、または `None`

1. の場合 **[!UICONTROL Logo Position]**&#x200B;を選択し、PayPal ロゴの位置を選択します。 `Left`, `Right`、または `Top`

1. の場合 **[!UICONTROL Text Color]**&#x200B;を選択し、 [!DNL PayLater] メッセージのテキストの色： `Black`, `White`, `Monochrome`、または `Grayscale`

これらのオプションを設定すると、PayPal ボタンと PayLater メッセージのプレビューが表示されます。 設定の適用や値のリセットに使用できるコントロールがあります。

- ボタンおよび PayLater メッセージング用に選択したスタイル設定を保存し、現在の場所および現在のボタン タイプに適用するには、をクリックします。 **[!UICONTROL Apply]**.

- ボタンおよび PayLater メッセージング値に対して選択したスタイル設定を保存し、それらをボタンのすべてのタイプと場所に適用するには、 **[!UICONTROL Apply to All Buttons]**.

- スタイル設定をボタンと PayLater メッセージに推奨されるデフォルト値に戻し、すべてのボタンタイプと場所に適用するには、 **[!UICONTROL Reset to Recommended Defaults]**.

## 手順 13: 3D 検証設定の完了

1. 検証プログラムに登録されているクレジットカードを使用している顧客に対して、検証手順を追加する場合（例：） _VISA で確認_）、設定 **[!UICONTROL 3D Secure Verification]** 対象： `Yes`.

   プロセス中に、検証用に送信されたトランザクション金額と、認証用に送信された金額がチェックされます。

2. すべてのトランザクションに対して常に 3D セキュア要求にチャレンジするには、次のように設定します **[!UICONTROL Always request 3DS]** 対象： `Yes`.

3. の場合 **[!UICONTROL Threshold Amount]**&#x200B;を入力し、3D 検証のトリガーに必要な最小注文額を入力します。

4. を設定 **[!UICONTROL Verify for Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Verify for Specific Countries]_リストが表示されます。 Ctrl キー（PC）または Command キー（Mac）を押しながら、リスト内で、お客様がストアから購入できる国を選択します。

   ![3D 検証設定](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## 手順 14:Braintree動的記述子の設定

次の記述子は、顧客のクレジットカード明細書の購入を識別するために使用されます。 各購入に関連付けられている会社を明確に識別することで、チャージバックの数を減らすことができます。 動的記述子がアカウントで有効になっていない場合は、Braintreeサポートにお問い合わせください。

![動的記述子](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. の動的記述子を入力 **[!UICONTROL Name]**, **[!UICONTROL Phone]**、および **[!UICONTROL URL]** 次のガイドラインに従います。

   - **[!UICONTROL Name]**  – 名前記述子にはアスタリスク（*）で区切られた 2 つの部分があります。 例：

     `company*myproduct`

     記述子の最初の部分は会社または DBA を示し、2 番目の部分は製品を示します。 の長さ `company` および `product` 記述子の一部は、以下の方法で、合計 22 文字まで割り当てることができます。

     **_名前記述子に含まれる文字_**

     _オプション 1:_ `Company` 3 文字にする必要があります。 `Product` 最大 18 文字まで指定できます

     _オプション 2:_ `Company` 7 文字にする必要があります。 `Product` 最大 14 文字まで指定できます

     _オプション 3_: `Company` 12 文字にする必要があります。 `Product` 最大 9 文字まで指定できます

   - **[!UICONTROL Phone]**  – 電話記述子の長さは 10 ～ 14 文字で、数字、ダッシュ、括弧、ピリオドのみを含めることができます。 例：

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - URL 記述子はドメイン名を表し、最大 13 文字にすることができます。 例：

     `company.com`

1. Braintreeの設定が完了したら、 **[!UICONTROL Save Config]**.

## 2.4 アップグレードノート

Adobe CommerceおよびMagento Open Source 2.4.0 以降、Braintree拡張機能はリリースに含まれています。 Marketplace のBraintree拡張機能がインストールされている 2.4.0 以前のバージョンから Commerce 2.4.x に移行する場合は、拡張機能をアンインストールする必要があります（`paypal/module-braintree` または `gene/module-braintree`）を選択し、コードのカスタマイズを更新して、 `PayPal_Braintree` の代わりにの名前空間 `Magento_Braintree`. Commerce Braintreeの主要な支払いバンドル拡張機能および拡張機能で配布されたCommerce Marketplaceが保持され、以前のバージョンで行われた支払いは、通常どおりキャプチャ、無効化または払い戻しできます。

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
