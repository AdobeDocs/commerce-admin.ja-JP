---
title: Braintree
description: 店舗でBraintreeをオンライン支払いソリューションとして設定する方法を説明します。
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: dba610f53893a8698d2c52fe92fd0266f1cfa0cb
workflow-type: tm+mt
source-wordcount: '2380'
ht-degree: 0%

---

# Braintree

Braintreeは、詐欺検出と PayPal 統合により、完全にカスタマイズ可能なチェックアウトエクスペリエンスを提供します。 対応 [!DNL Apple Pay], [!DNL Google Pay]、ACH、Venmo、および現地の支払い方法。 Braintreeは、取引がBraintree・システム上で行われるため、マーチャントの PCI コンプライアンスの負担を軽減します。 Braintree支払統合は、 [GENE コマース](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>以前のバージョンのAdobe Commerceから 2.4.x にアップグレードする場合、またはCommerce MarketplaceからBraintree拡張機能がインストールされたMagento Open Sourceの場合は、 [2.4 アップグレードに関する注意](#24-upgrade-notes) をクリックします。

{{beta2-updates}}

## 手順 1:Braintreeの資格情報を取得する

に移動します。 [Braintree支払][1] アカウントに新規登録します。

## 手順 2：基本設定の完了

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

   - コマースインストールに複数の Web サイト、ストア、表示がある場合は、左上隅で **[!UICONTROL Store View]** 設定が適用される場所

   - Adobe Analytics の _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**は、ビジネスの場所に設定されます。

1. の下 _[!UICONTROL Recommended Solutions]_、_[!UICONTROL Braintree Payments (by GENE Commerce v4.5.0)]_ セクションで、 **[!UICONTROL Configure]**.

   ![設定Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にBraintreeを支払いオプションとして識別するタイトルを入力します。

1. 現在の動作を設定 **[!UICONTROL Environment]** Braintree取引先： `Sandbox` または `Production`

   サンドボックスで設定をテストする場合は、次のみを使用します。 [クレジットカード番号][2] Braintreeが推奨 Braintreeを使用して実稼動環境に移行する準備が整ったら、次の手順に従って、 **[!UICONTROL Environment]** から `Production`.

   ![基本的な資格情報設定](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only` ・買い付けを承認し、資金を保留する。 金額は、販売が完了するまで、顧客の銀行口座から引き出されません _キャプチャ_ 商人によって。|
   - `Intent Sale`   — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。 **_注意：_** この値は次のとおりです。  _許可してキャプチャ_ 2.3.x 以前のリリースでの更新と更新。|

1. 次を入力します。 **[!UICONTROL Sandbox Merchant ID / Merchant ID]** をBraintreeアカウントから。

1. Braintreeアカウントから次の資格情報を入力します。

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >両方に別々のフィールドがあります **（サンドボックスと実稼動）** 環境とその他のフィールドは、選択した環境に基づいてレンダリングされます。

1. 設定を保存する前に、 **[!UICONTROL Validate Credentials]** 認証情報を検証する場合。

1. 設定 **[!UICONTROL Enable Card Payments]** から `Yes`.

   ![基本設定](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   顧客情報を安全に保存したい場合、顧客は購入するたびに情報を再入力する必要がない場合は、 **[!UICONTROL Enable Vault for Card Payments]** から `Yes`.

## 手順 3：詳細設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Braintree Settings]** 」セクションに入力します。

   ![詳細設定](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. の場合 **[!UICONTROL Vault Title]**&#x200B;をクリックし、顧客カード情報が保存される Vault を識別する参照用の説明的なタイトルを入力します。

1. 次を入力します。 **[!UICONTROL Merchant Account ID]** をBraintreeアカウントから。

   使用するマーチャントアカウントを指定しない場合、Braintreeはデフォルトのマーチャントアカウントを使用してトランザクションを処理します。

1. 高度な不正ツールのチェックの一環としてトランザクションが評価用に送信されないようにするには、管理者を通じて行われた注文に対して、 **[!UICONTROL Skip Fraud Checks on Admin Orders]** から `Yes`.

1. を設定します。 **[!UICONTROL Bypass Fraud Protection Threshold]** そのため `Advanced Fraud Protection` しきい値に達したり、しきい値を超えたりした場合は、チェックがバイパスされます。

   このフィールドを空白にすると、このオプションは無効になります。

1. ストアとBraintreeの間のやり取りのログファイルを保存する場合は、 **[!UICONTROL Debug]** から `Yes`.

1. お客様にクレジットカードの後ろから 3 桁のセキュリティコードを提供するよう求めるには、 **[!UICONTROL CVV Verification]** から `Yes`.

   CVV 検証を使用する場合は、AVS や CVV を _設定/処理中_ Braintreeアカウントの

1. すべての支払い方法に対して買い物かごの品目を送信するには、 **[!UICONTROL Send Card Line Items]** から `Yes`.

1. の場合 **[!UICONTROL Credit Card Types]**「 」で、店舗で受け入れられる各クレジットカードを「Braintree」を通じた支払い」として選択します。

   複数のカードタイプを選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. の場合 **[!UICONTROL Sort Order]**&#x200B;をクリックし、チェックアウト時に他の支払い方法と共にリストに表示されるBraintreeの順序を決定する数値を入力します。

## 手順 4:Braintreeの Webhook 設定の完了

![BraintreeWebhook 設定](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Webhook]** から `Yes` 不正保護、ACH 支払い、および現地支払い方法に関するウェブフック機能を有効にする。

1. URL を **[!UICONTROL Fraud Protection URL]** フィールドに入力し、Braintreeアカウントに _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >この URL は、セキュリティで保護され、公にアクセス可能である必要があります。

1. を設定します。 **[!UICONTROL Fraud Protection Approve Order Status]** フィールドを使用して、Braintreeが不正保護を承認するタイミングを決定します。

   選択した注文ステータスがコマース注文に割り当てられます。

1. を設定します。 **[!UICONTROL Fraud Protection Reject Order Status]** 不正保護がBraintreeによって拒否されたタイミングを決定するフィールド。

   選択した注文ステータスがコマース注文に割り当てられます。

## 手順 5：国固有の設定を完了する

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー (PC) または Command キー (Mac) を押しながら、リスト内の顧客がストアで購入できる国を選択します。

   ![国固有の設定](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. 次の手順でを設定します。 **[!UICONTROL Country Specific Credit Card Types]**:

   - クリック **[!UICONTROL Add]**.

   - を設定します。 **[!UICONTROL Country]** を選択し、 **[!UICONTROL Allowed Credit Card Type]**.

   - 繰り返して、各国から受け入れられたクレジットカードを特定します。

## 手順 6:Braintree設定を使用して ACH を完了する

![ACH スルーBraintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. ACH を支払オプションとして「Braintree」に含めるには、 **[!UICONTROL Enable ACH Direct Debit]** から `Yes`.

1. の場合 **[!UICONTROL Sort Order]**「 」に数値を入力して、チェックアウト時に他の支払オプションと共にリストされた場合に「ACH 支払Braintree」オプションが表示される順序を決定します。

## 手順 7: [!UICONTROL Apple Pay] Braintree設定

![Braintree設定で ApplePay](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. 含める [!DNL Apple Pay] をBraintreeの支払オプションとして設定 **[!UICONTROL Enable ApplePay through Braintree]** から `Yes`.

   必ず [ドメイン名を確認してください](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) 最初にBraintreeアカウントで。

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only` ・買い付けを承認し、資金を保留する。 金額は、販売が完了するまで、顧客の銀行口座から引き出されません _キャプチャ_ 商人が
   - `Intent Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. の場合 **[!UICONTROL Merchant Name]**&#x200B;の場合は、Apple Pay ダイアログで顧客に表示するラベルを指定するテキストを入力します。

1. の場合 **[!UICONTROL Sort Order]**、番号を入力して、 [!DNL Apple Pay] 「支払い」オプションは、チェックアウト時に他の支払いオプションと共に表示される場合に表示されます。

## 手順 8：現地支払い方法の設定を完了します

1. 現地支払い方法を支払オプションとしてBraintreeと共に含めるには、 **[!UICONTROL Enable Local Payment Methods]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、「チェックアウトの支払い方法」セクションに表示されるラベルに使用するテキストを入力します ( デフォルト値： `Local Payments`) をクリックします。

1. の場合 **[!UICONTROL Allowed Payment Methods]**、有効にするローカルの支払い方法を選択します。

   オプション： `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` （未サポート）

   ![ローカル支払い方法の設定](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >バンドルされたBraintree拡張は、 [Braintree開発者向けドキュメント](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). その他の現地支払い方法は、今後のリリースでサポートされる予定です。

1. の場合 **[!UICONTROL Sort Order]**「 」に数値を入力して、チェックアウト時に他の支払オプションと共にリストされた場合に、現地の支払い方法が表示される順序を決定します。

## 手順 9: [!DNL Google Pay] Braintree設定

![GoogleペイスルーBraintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. 含める [!DNL Google Pay] をBraintreeの支払オプションとして設定 **[!UICONTROL Enable GooglePay Through Braintree]** から `Yes`.

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only` ・買い付けを承認し、資金を保留する。 金額は、販売が完了するまで、顧客の銀行口座から引き出されません _キャプチャ_ 商人が
   - `Intent Sale`   — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. 設定 **[!UICONTROL Button Color]** 色を決めるには [!DNL Google Pay] ボタン： `White` または `Black`

1. の場合 **[!UICONTROL Merchant ID]**&#x200B;に、MerchantID(Googleから提供される ) を入力します。

1. の場合 **[!UICONTROL Accepted Cards]**&#x200B;を使用して、顧客が [!DNL Google Pay].

   オプション： `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. の場合 **[!UICONTROL Sort Order]**、番号を入力して、 [!DNL Google Pay] は、チェックアウト時に他の支払いオプションと共に表示される場合に表示されます。

## 手順 10:Venmo の設定からBraintreeを完了する

1. Venmo を支払オプションとしてBraintree付きで含めるには、 **[!UICONTROL Enable Venmo through Braintree]** から `Yes`.

   ![ベンモスルーBraintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only` ・買い付けを承認し、資金を保留する。 金額は、販売が完了するまで、顧客の銀行口座から引き出されません _キャプチャ_ 商人が
   - `Intent Sale`   — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. の場合 **[!UICONTROL Sort Order]**、数値を入力して、チェックアウト時に Venmo が他の支払オプションと共にリストに表示される際の順序を決定します。

## ステップ 11:Braintree設定を通じて PayPal を完成させる

![PayPal のBraintree設定](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. PayPal を支払いオプションとしてBraintreeに含めるには、 **[!UICONTROL Enable PayPal through Braintree]** から `Yes`.

1. Braintree支払い方法で PayPal を指定：

   >[!NOTE]
   >
   >次のいずれか **[!DNL PayPal Credit]** または **[!DNL PayPal PayLater]** を有効にできます。 両方のメソッドを同時に有効にすることはできません。

   - 含める [!DNL PayPal Credit] をBraintreeの支払オプションとして設定 **[!UICONTROL Enable PayPal Credit through Braintree]** から `Yes`.

     条件 **PayPal を有効にするBraintree** が `Yes`の場合は、このフィールドのみが表示されます。

     >[!NOTE]
     >
     >PayPal Credit は、米国および英国でのみ利用できます。 PayPal クレジットは、 _[!UICONTROL Merchant Country]_フィールドが次の値ではありません `US` または `UK`.

   - 含める [!DNL PayPal PayLater] をBraintreeの支払オプションとして設定 **[!UICONTROL Enable PayPal PayLater through Braintree]** から `Yes`.

     条件 **[!UICONTROL Enable PayPal PayLater through Braintree]** が `Yes`の場合は、このフィールドのみが表示されます。

     サイトに PayLater のメッセージを表示して、次のようなオファーを表示できます。 _3 で支払う_：顧客が月 3 回の無利子支払いをおこなえるようにします。 Braintreeの統合により、サイトにメッセージを表示して、この機能をプロモーションできます。 他のコンテンツ、マーケティング、マテリアルを使用して PayLater オファーをプロモーションすることはできません。

1. の場合 **[!UICONTROL Title]**、チェックアウト時に PayPal によるBraintreeの支払いを識別するタイトルを入力します。

1. 設定 **[!UICONTROL Vault Title]** から `Yes` 顧客のクレジットカード情報を保存するための安全な vault の使用を可能にする。

1. の場合 **[!UICONTROL Sort Order]**&#x200B;をクリックし、チェックアウト時に他の支払いオプションと共にリストされた場合に PayPal のBraintreeオプションが表示される順序を指定する数値を入力します。

1. マーチャント名を、 [ストア設定](../getting-started/store-details.md#store-information)」で、「 **[!UICONTROL Override Merchant Name]** フィールドに値を入力します。

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorize Only` ・買い付けを承認し、資金を保留する。 金額は、販売が完了するまで、顧客の銀行口座から引き出されません _キャプチャ_ 商人が
   - `Authorize and Capture`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. 設定 **[!UICONTROL Payment from Applicable Countries]** を PayPal で処理されるBraintreeトランザクションに対して、次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー (PC) または Command キー (Mac) を押しながら、リスト内の顧客がストアで購入できる国を選択します。

1. 顧客に請求先住所の入力を求めるには、 **[!UICONTROL Require Customer's Billing Address]** から `Yes`.

   >[!NOTE]
   >
   >この機能は、PayPal テクニカルサポートがお客様のアカウントに対して有効にする必要があります。

1. ストアと PayPal 間のやり取りのログファイルをBraintreeで保存するには、 **[!UICONTROL Debug]** から `Yes`.

1. PayPal ボタンをミニカートと買い物かごページの両方に表示するには、 **[!UICONTROL Display on Shopping Cart]** から `Yes`.

## 手順 12：スタイル設定を設定する

1. の場合 **[!UICONTROL Location]**、PayPal のボタンとメッセージをレンダリングする場所を選択します。 `Mini-Cart and Cart Page`, `Checkout Page`または `Product Page`

   ![PayPal のスタイル設定](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

このセクションのオプションと設定は、 _[!UICONTROL Location]_フィールドに入力します。

1. 設定 **[!UICONTROL PayPal Button Type]** を次の 3 種類のボタンのいずれかに設定します。 `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

このセクションのオプションと設定は、 _[!UICONTROL PayPal Button Type]_フィールドに入力します。

1. 選択した場所のストアフロントに PayPal ボタンを表示するには、 **[!UICONTROL Show PayPal Button]** から `Yes`.

1. の場合 **[!UICONTROL Button Label]**、 PayPal ボタンのラベルを選択します。 `Paypal`, `Checkout`, `Buynow`または `Pay`

1. の場合 **[!UICONTROL Color]**、 PayPal ボタンの色を選択します。 `Blue`, `Black`, `Gold`または `Silver`

1. の場合 **[!UICONTROL Shape]**、 PayPal ボタンのシェイプを選択します。 `Pill` または `Rectangle`

1. の場合 **[!UICONTROL Size]**、 PayPal ボタンのサイズを選択します。 `Medium`, `Large`または `Responsive`

**[!UICONTROL PayLater Messaging]**

1. 表示する [!DNL PayLater] 選択した場所のストアフロントでのメッセージングに、 **[!UICONTROL Show PayLater Messaging]** から `Yes`.

   このメッセージには、 [!DNL PayLater] 利用可能なオファーのメッセージ ([制限適用](https://developer.paypal.com/docs/checkout/pay-later/us/)) をクリックします。

1. の場合 **[!UICONTROL Message Layout]**&#x200B;を選択し、 [!DNL PayLater] メッセージのレイアウト： `Text` または `Flex`

1. の場合 **[!UICONTROL Logo]**、 PayPal のロゴタイプを選択します。 `Inline`, `Primary`, `Alternative`または `None`

1. の場合 **[!UICONTROL Logo Position]**、PayPal のロゴの位置を選択します。 `Left`, `Right`または `Top`

1. の場合 **[!UICONTROL Text Color]**&#x200B;を選択し、 [!DNL PayLater] メッセージテキストの色： `Black`, `White`, `Monochrome`または `Grayscale`

これらのオプションを設定すると、PayPal ボタンと PayLater メッセージのプレビューを確認できます。 設定を適用したり、値をリセットしたりする際に使用できるコントロールがあります。

- ボタンと PayLater メッセージの選択したスタイル設定を保存し、現在の位置と現在のボタンの種類に適用するには、 **[!UICONTROL Apply]**.

- ボタンと PayLater メッセージング値のスタイル設定を保存し、すべてのボタンの種類と場所に適用するには、 **[!UICONTROL Apply to All Buttons]**.

- スタイル設定をボタンと PayLater メッセージの推奨既定値に戻し、すべてのボタンの種類と位置に適用するには、 **[!UICONTROL Reset to Recommended Defaults]**.

## 手順 13: 3D 検証設定を完了する

1. 検証プログラムに登録されているクレジットカードを使用する顧客に検証ステップを追加する場合 ( 例： _VISA で検証_)，設定 **[!UICONTROL 3D Secure Verification]** から `Yes`.

   プロセス中に、検証用に送信されたトランザクション金額と、承認用に送信された金額が照合されます。

2. すべてのトランザクションに対して常に 3D セキュア要求に対してチャレンジするには、 **[!UICONTROL Always request 3DS]** から `Yes`.

3. の場合 **[!UICONTROL Threshold Amount]**、3D 検証のトリガーに必要な最小注文額を入力します。

4. 設定 **[!UICONTROL Verify for Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Verify for Specific Countries]_リストが表示されます。 Ctrl キー (PC) または Command キー (Mac) を押しながら、リスト内の顧客がストアで購入できる国を選択します。

   ![3D 検証設定](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## 手順 14：動的記述子のBraintree

次の記述子は、顧客のクレジットカード明細書での購入を識別するために使用されます。 各購入に関連する会社を明確に識別することで、チャージバックの数を減らすことができます。 お使いのアカウントで動的記述子が有効になっていない場合は、Braintreeサポートにお問い合わせください。

![動的記述子](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. の動的記述子を入力 **[!UICONTROL Name]**, **[!UICONTROL Phone]**、および **[!UICONTROL URL]** 次のガイドラインに従います。

   - **[!UICONTROL Name]**  — 名前記述子には 2 つの部分があり、アスタリスク (*) で区切られます。 例：

     `company*myproduct`

     記述子の最初の部分は会社または DBA を識別し、2 番目の部分は製品を識別します。 の長さ `company` および `product` 記述子の一部は、次の方法で割り当てることができます（22 文字までの長さの組み合わせ）。

     **_名前記述子の文字_**

     _オプション 1:_ `Company` は、3 文字である必要があります。 `Product` は 18 文字までです

     _オプション 2:_ `Company` は 7 文字でなければなりません。 `Product` は最大 14 文字です

     _オプション 3_: `Company` は、12 文字である必要があります。 `Product` は最大 9 文字までです

   - **[!UICONTROL Phone]**  — 電話記述子の長さは 10 ～ 14 文字で、数字、ダッシュ、括弧、ピリオドのみを含めることができます。 例：

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - URL 記述子はドメイン名を表し、最大 13 文字まで設定できます。 例：

     `company.com`

1. Braintreeの設定が完了したら、 **[!UICONTROL Save Config]**.

## 2.4 アップグレードに関する注意

2.3 から Commerce 2.4 にアップグレードする前に、マーチャントは、コアコマースBraintreeの統合を、 [Commerce Marketplace](https://commercemarketplace.adobe.com/catalogsearch/result/?q=braintree). Adobe CommerceとMagento Open Source2.4.0 以降、Braintree拡張機能がリリースに含まれます。

Marketplace 拡張機能がインストールされている 2.4.0 より前のバージョンから Commerce 2.4.x に移行する場合は、そのBraintree機能 (`paypal/module-braintree` または `gene/module-braintree`) を更新し、コードのカスタマイズを更新して `PayPal_Braintree` 名前空間の代わりに `Magento_Braintree`. コアコマースBraintree支払のバンドルされた拡張とCommerce Marketplaceで配布された拡張の構成設定が保持され、以前のバージョンに置かれた支払いは、通常どおりキャプチャ、無効化、返金できます。

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
