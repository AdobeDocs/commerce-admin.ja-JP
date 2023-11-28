---
title: PayPal Express チェックアウト
description: PayPal Express Checkout をオンライン支払いソリューションとしてストアに設定する方法を説明します。
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3113'
ht-degree: 0%

---

# PayPal Express チェックアウト

PayPal Express Checkout は、お客様にクレジットカードで支払う機能を提供すること、または個人の PayPal アカウントのセキュリティから支払う機能を提供することで、売上を増やすのに役立ちます。 チェックアウト時に、顧客はセキュアな PayPal サイトにリダイレクトされ、支払い情報を完了します。 その後、顧客がストアに戻り、残りのチェックアウトプロセスを完了します。 「速達チェックアウト」を選択すると、おなじみの PayPal ボタンがストアに追加され、売上を増やすように報告されています。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日現在、ヨーロッパの銀行は、満たさない支払いを辞退する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件。 PayPal Express Checkout がPSD2 に準拠するために必要なアクションはありません。すべての要件は PayPal で処理されます。

現在の PayPal アカウントを持つお客様は、 _[!UICONTROL Check out with PayPal]_」ボタンをクリックします。 速達チェックアウトは、スタンドアロンとして、または PayPal のオールインワンソリューションの 1 つと共に使用できます。 既にオンラインでクレジットカードを受け入れている場合は、PayPal で支払いを希望する新規顧客を引き付けるための追加のオプションとして、速達チェックアウトを提供することができます。

>[!NOTE]
>
>PayPal は、PayPal Express Checkout を通じたデジタル商品販売のサポートを廃止し、次のいずれかを使用することをお勧めします。 [PayPal 支払い標準](paypal-payments-standard.md) または他の PayPal 支払いゲートウェイを使用して、 [仮想製品](../catalog/product-create-virtual.md).

## 要件

- マーチャント： [Business PayPal アカウント][1]
- 顧客： [個人の PayPal アカウント][2]

## 高速チェックアウトワークフロー

他の支払い方法とは異なり、PayPal Express Checkout では、お客様は通常のチェックアウトワークフローの最初に、製品ページ、ミニカート、買い物かごからチェックアウトできます。

1. **顧客が注文を発行する**  — 顧客が _[!UICONTROL Check out with PayPal]_」ボタンをクリックします。
1. **お客様が PayPal サイトにリダイレクトされる**  — 顧客は PayPal サイトにリダイレクトされ、トランザクションを完了します。
1. **顧客が PayPal アカウントにログインする**  — 顧客が PayPal アカウントにログインして、トランザクションを完了する必要があります。 支払いシステムは、PayPal アカウントからの請求と配送先情報を使用します。
1. **顧客がチェックアウトページに戻る**  — 顧客は、注文を確認するために、ストアのチェックアウトページにリダイレクトされます。
1. **顧客が注文を発行する**  — 顧客が注文を行い、注文情報が PayPal に送信されます。
1. **PayPal がトランザクションを解決します** - PayPal が注文を受け取り、トランザクションを解決します。

>[!NOTE]
>
>PayPal Express Checkout は、複数のアドレスを持つ注文をサポートしていません。

## コンテキスト内チェックアウト

PayPal の _コンテキスト内チェックアウト_ を使用すると、オンラインでの支払いがこれまで以上に簡単になります。 シンプルなワンクリックまたは 2 クリックでシームレスにチェックアウトできるので、顧客は店舗を見失うことはありません。 コンテキスト内チェックアウトは、Mac と PC でも同様に機能し、デスクトップコンピューター、タブレット、モバイルデバイスでも一貫したエクスペリエンスを提供します。 詳しくは、 [高速チェックアウトでのコンテキスト内チェックアウト][5].

![PayPal のコンテキスト内チェックアウトデモ](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal のコンテキスト内チェックアウトデモ_][6]

ストアを [!DNL PayPal Express Checkout]を使用する場合は、このオプションを有効にできます。

## PayPal アカウントを設定する

コマース管理で PayPal Express Checkout を設定する前に、PayPal Web サイトでマーチャントアカウントを設定する必要があります。

1. PayPal Advanced アカウントにログインする場所： [manager.paypal.com][3].

1. に移動します。 **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** 次の設定を行います。

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. クリック **[!UICONTROL Save Changes]**.

1. 別のユーザーを設定する（PayPal で推奨）:

   - に移動します。 [manager.paypal.com][3] お使いのアカウントにログインします。

   - 別のユーザーを設定するには、指示に従います。

   - クリック **[!UICONTROL Update]**.

## コマースでの PayPal Express チェックアウトの設定

PayPal Express Checkout と、All-in-one ソリューションの 2 つの PayPal ソリューションを同時にアクティブにすることができます。 別のソリューションを有効にした場合、以前に使用したソリューションは自動的に無効化されます。

>[!NOTE]
>
>クリック **[!UICONTROL Save Config]** いつでも作業内容を保存できます。

### 手順 1：設定の開始

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. インストールに複数の Web サイト、ストア、または表示がある場合は、 **[!UICONTROL Store View]** を、この設定を適用するストア表示に追加します。

1. Adobe Analytics の _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地

   この設定は、設定に表示される PayPal ソリューションの選択を決定します。

   ![商家の国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. の下 _[!UICONTROL Recommended Solutions]_をクリックし、**[!UICONTROL Configure]**対象：**[!UICONTROL PayPal Express Checkout]**.

   ![PayPal Express チェックアウトの設定](./assets/paypal-express-checkout.png){width="600"}

### 手順 2:PayPal アカウントを有効にして接続する

1. 必要に応じて、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Required PayPal Settings]** 」セクションに入力します。

   ![PayPal アカウントに接続する](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. テストまたは実稼動用のアカウントに接続します。

   - テスト（開発）モードの場合は、 **[!UICONTROL Sandbox Credentials]** を入力し、 [PayPal サンドボックス][7] 認証情報。
   - 実稼動モードの場合は、 **[!UICONTROL Connect with PayPal]** 実稼動アカウントの資格情報を入力します。

   接続が検証されたら、続行できます。

1. 設定 **[!UICONTROL Enable this Solution]** から `Yes`.

1. 有効にするには [PayPal コンテキスト内チェックアウト](#in-context-checkout):

   - 設定 **[!UICONTROL Enable In-Context Checkout Experience]** から `Yes`.

   - PayPal を入力 **[!UICONTROL Merchant Account ID]**.

     Merchant アカウント ID は PayPal ビジネスアカウントプロファイルにあります。

>[!NOTE]
>
>[PayPal クレジット](paypal.md#paypal-credit-and-pay-later) は、この支払いオプションに対してデフォルトで有効になっています。

### 手順 3：必要な PayPal 設定を完了する

1. 必要に応じて、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Express Checkout]** 」セクションに入力します。

   ![PayPal Express チェックアウトに必要な設定](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. （オプション） **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E メールアドレスでは、大文字と小文字が区別されます。 支払いを受け取るには、入力した電子メールアドレスが PayPal マーチャントアカウントで指定された電子メールアドレスと一致している必要があります。

   PayPal アカウントをお持ちでない場合は、 **[!UICONTROL Start accepting payments via PayPal]**.

1. 設定 **[!UICONTROL API Authentication Methods]** を次のいずれかに変更します。

   - `API Signature`  — この PayPal 認証方式は、実装が最も簡単で、ユーザ名、パスワード、およびアカウントを識別する一意の文字列と数字列に基づいています。 API 署名の資格情報は期限切れにはなりません。
   - `API Certificate`  — この PayPal 認証方法は、ユーザー名、パスワード、ダウンロード可能な証明書に基づいて、より安全になります。 API 資格情報は 3 年後に期限切れになり、更新する必要があります。

   必要に応じて、以下の手順を実行します。

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Sandbox アカウントの資格情報を使用している場合は、 **[!UICONTROL Sandbox Mode]** から `Yes`.

   サンドボックスで設定をテストする場合は、次のみを使用します。 [クレジットカード番号][4] PayPal で推奨される情報です。 実稼動に移行する準備が整ったら、設定に戻り、サンドボックスモードをに設定します。 `No` お使いの実稼動 PayPal アカウントに接続します。

1. システムがプロキシサーバーを使用して Commerce と PayPal 支払いシステム間の接続を確立する場合は、 **[!UICONTROL API Uses Proxy]** から `Yes` 次の手順を実行します。

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

この一連の手順の最後に、必要な PayPal 設定が完了します。 「基本設定」と「詳細設定」を続行するか、「 **[!UICONTROL Save Config]** 後で設定を調整する

### ステップ 4：広告 PayPal クレジット/広告 PayPal PayLater（オプション）の設定

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能を使用すると、買い物客は購入時に全額を支払う代わりに、隔週の分割払いで注文に対して支払うことができます。 PayPal Credit エクスペリエンスは廃止されました。

設定 **[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに変更します。

- `Yes` - PayPal PayLater を宣伝する
- `No` - PayPal クレジットの宣伝を設定するには

>[!NOTE]
>
>The **[!UICONTROL Enable PayPal PayLater Experience]** を設定しても無効になりません [!DNL PayPal PayLater] 機能と削除しない **_[!UICONTROL PayPal PayLater]_** ボタンをストアフロントからクリックします。 両方を無効にするには **_[!UICONTROL PayPal PayLater]_** および **_[!UICONTROL PayPal Credit]_** ストアフロントのボタンをクリックし、 `PayPal Credit` の値 **[!UICONTROL Disable Funding Options]** 設定 ([!UICONTROL Advanced Settings] under [!UICONTROL Frontend Experience Settings]) をクリックします。

#### PayPal クレジットの宣伝

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advertise PayPal Credit]** 」セクションに入力します。

1. アカウント情報を取得するには、 **[!UICONTROL Get Publisher ID from PayPal]** そして指示に従う

1. を入力します。 **[!UICONTROL Publisher ID]**.

   ![PayPal クレジットの宣伝](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Home Page]** 」セクションに入力します。

1. ページにバナーを配置するには、 **[!UICONTROL Display]** から `Yes`.

1. 設定 **[!UICONTROL Position]** を次のいずれかに変更します。

   - `Header (center)`
   - `Sidebar (right)`

1. 設定 **[!UICONTROL Size]** を次のいずれかに変更します。

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![広告 PayPal クレジットホームページ設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 残りのセクションと、前の手順を繰り返します。

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### 広告 PayPal PayLater

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advertise PayPal PayLater]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable PayPal PayLater]** から `Yes`.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Home Page]** 」セクションに入力します。

1. ページにバナーを配置するには、 **[!UICONTROL Display]** から `Yes`.

1. 設定 **[!UICONTROL Position]** を次のいずれかに変更します。

   - `Header (center)`
   - `Sidebar`

1. 設定 **[!UICONTROL Style Layout]** を次のいずれかに変更します。

   - `Text`
   - `Flex`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** 唯一、設定 **[!UICONTROL Logo Type]** を次のいずれかに変更します。

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** 唯一、設定 **[!UICONTROL Logo Position]** を次のいずれかに変更します。

   - `Left`
   - `Right`
   - `Top`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** 唯一、設定 **[!UICONTROL Text Color]** を次のいずれかに変更します。

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** 唯一、設定 **[!UICONTROL Text Size]** を次のいずれかに変更します。

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 唯一、設定 **[!UICONTROL Ratio]** を次のいずれかに変更します。

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 唯一、設定 **[!UICONTROL Color]** を次のいずれかに変更します。

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![広告 PayPal クレジットホームページ設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 残りのセクションと、前の手順を繰り返します。

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 手順 5：基本設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Basic Settings - PayPal Express Checkout]** 」セクションに入力します。

   ![基本設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルは、 _PayPal_ （すべてのストア表示）

1. 複数の支払い方法を提供する場合は、次の項目に数値を入力します： **[!UICONTROL Sort Order]** PayPal Express Checkout が他の支払い方法と共にリストされた際に表示される順序を決定する。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認し、資金を保留する。 金額は、そのまま取り下げられない _キャプチャ_ 商人が
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。
   - `Order`  — 注文金額は、PayPal の顧客残高、銀行口座、クレジットカードには記載されていないか、認定されていません。 注文の支払いアクションは、PayPal の支払いシステムと商人との間の契約を表します。 これにより、マーチャントは、顧客の購入者アカウントから注文済みの合計に至る 1 つ以上の金額を、最大 29 日間にわたって取り込むことができます。 マーチャントは、注文後、次の 29 日間の間、いつでもそれらを取り込むことができます。 注文額のキャプチャは、1 つ以上の請求書を作成して、コマース管理者からのみ実行できます。

1. 次の手順で _[!UICONTROL Check out with PayPal]_製品ページのボタンをクリックし、**[!UICONTROL Display on Product Details Page]**から `Yes`.

1. 支払処理が `Order`、以下を完了します。

   - **[!UICONTROL Authorization Honor Period (days)]**  — プライマリ認証が有効である期間を決定します。 値は、PayPal マーチャントアカウントの対応する値と等しい必要があります。 PayPal マーチャントアカウントのデフォルト値は次のとおりです。 `3`. この数を増やすには、PayPal に連絡する必要があります。 承認は、米国太平洋時間の最終日午後 11 時 49 分に無効になります。

   - **[!UICONTROL Order Valid Period (days)]**  — 注文が有効である期間を決定します。 注文が無効になると、その注文に対する請求書を作成できなくなります。 PayPal マーチャントアカウントの注文有効期間の値と等しい値を指定します。 PayPal マーチャントアカウントのデフォルト値は次のとおりです。 `29`. この番号を変更するには、PayPal に連絡する必要があります。

   - **[!UICONTROL Number of Child Authorizations]** - 1 件の注文に対する認証の最大数を指定します。この数により、注文に対して作成できるオンラインの一部請求書の最大数が決まります。 この値は、PayPal マーチャントアカウントの対応する設定と等しくする必要があります。 PayPal アカウントでの子認証のデフォルト数は次のとおりです。 `1`. この数を増やすには、PayPal に連絡する必要があります。

### 手順 6：詳細設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

   ![詳細設定 — PayPal Express チェックアウト](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display on Shopping Cart]** から `Yes`.

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — ストア設定で指定されたすべての国のお客様は、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各項目をクリックします。

1. 支払いシステムとの通信をログファイルに書き込むには、 **[!UICONTROL Debug Mode]** から `Yes`.

   PayPal Payments Advanced のログファイルは次のとおりです。 `_payflow_advanced.log`.

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性を検証するには、次のように設定します。 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. PayPal サイトから顧客の注文の完全な概要を行項目別に表示するには、 **[!UICONTROL Transfer Cart Line Items]** から `Yes`.

1. 概要に最大 10 個の送料オプションを含めるには、 **[!UICONTROL Transfer Shipping Options]** から `Yes`. （このオプションは、行項目が転送に設定されている場合にのみ表示されます）。

1. PayPal の許可ボタンに使用する画像の種類を決定するには、 **[!UICONTROL Shortcut Buttons Flavor]** を次のいずれかに変更します。

   - `Dynamic` - （推奨） PayPal サーバーから動的に変更できる画像を表示します。
   - `Static`  — 動的に変更できない特定の画像を表示します。

1. PayPal アカウントを持たない顧客がこの方法で購入を許可するには、 **[!UICONTROL Enable PayPal Guest Checkout]** から `Yes`.

1. 設定 **[!UICONTROL Require Customer's Billing Address]** を次のいずれかに変更します。

   - `Yes`  — すべての購入について、顧客の請求先住所が必要です。
   - `No`  — 購入時に顧客の請求先住所は不要です。
   - `For Virtual Quotes Only`  — 仮想見積もりの場合のみ、顧客の請求先住所が必要です。

   >[!NOTE]
   >
   >この機能は、PayPal テクニカルサポートを通じてマーチャントアカウントに対して有効にする必要があります。

1. （オプション） **[!UICONTROL Billing Agreement Signup]** 顧客に署名を許可する [請求契約](paypal-billing-agreements.md) 顧客アカウントで有効な請求契約が利用できない場合は、PayPal 支払いシステムのストアに次の情報を入力します。

   - `Auto`  — 顧客は、速達チェックアウト・フローで請求契約に署名するか、別の支払い方法を使用できます。
   - `Ask Customer`  — お客様は、速達チェックアウトフローで請求契約に署名するかどうかを決定できます。
   - `Never`  — お客様は、速達チェックアウト・フローで請求契約に署名できません。

   >[!NOTE]
   >
   >商人は尋ねるべし [PayPal Merchant テクニカルサポート](https://developer.paypal.com/support/) ：アカウントで請求契約を有効にします。 The _請求契約のサインアップ_ パラメーターは、PayPal がマーチャントアカウントに対して請求契約が有効になっていることを確認した後にのみ有効になります。

1. 顧客が注文確認のためにストアに戻ることなく PayPal サイトからトランザクションを完了できるようにするには、 **[!UICONTROL Skip Order Review Step]** から `Yes`.

1. ストアの必要に応じて、次の追加のセクションに入力します。

   - [PayPall 請求契約設定](#paypal-billing-agreement-settings)
   - [決済レポート設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)
   - [スマートボタンのカスタマイズ](#customize-smart-buttons)
   - [機能](#features)

1. 完了したら、「 **[!UICONTROL Save Config]**.

#### PayPal 請求契約設定

A [請求契約](paypal-billing-agreements.md) は、複数の注文での使用を PayPal によって承認された、マーチャントと顧客の間の営業契約です。 チェックアウトプロセスでは、「請求契約の支払い」オプションは、会社との請求契約を既に入力している顧客に対してのみ表示されます。 PayPal が契約を承認すると、支払いシステムは、契約に関連付けられた各注文を識別する一意の参照 ID を発行します。 発注と同様に、顧客が会社で設定できる請求契約の数に制限はありません。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL PayPal Billing Agreement Settings]** 」セクションに入力します。

   ![請求契約設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enabled]** から `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;をクリックし、チェックアウト時に PayPal の請求契約方法を識別するタイトルを入力します。

1. 複数の支払い方法を提供する場合は、 **[!UICONTROL Sort Order]** フィールドを使用して、チェックアウト時に他の支払い方法と共にリストされた場合に請求基本契約が表示される順序を決定します。

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認し、資金を保留する。 その金額は、商人によって「取り込まれる」まで引き落とされません。
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — ストア設定で指定されたすべての国のお客様は、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各国をクリックします。

1. 支払いシステムとの通信をログファイルに記録するには、 **[!UICONTROL Debug Mode]** から `Yes`.

   >[!NOTE]
   >
   >ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。

1. SSL 検証を有効にするには、 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. 顧客の注文の各行項目の要約を PayPal の支払いページに表示するには、 **[!UICONTROL Transfer Cart Line Items]** から `Yes`.

1. 顧客が顧客アカウントのダッシュボードから請求契約を開始できるようにするには、 **[!UICONTROL Allow in Billing Agreement Wizard]** から `Yes`.

#### 決済レポート設定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Settlement Report Settings]** 」セクションに入力します。

   ![決済レポート設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL SFTP Credentials]**、次の操作を実行します。

   - PayPal セキュア FTP サーバーに新規登録している場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - 次の前にテストレポートを実行するには _運行中_ お客様のサイトの「Express Checkout」で、 **[!UICONTROL Sandbox Mode]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     デフォルトでは、値は次のとおりです。 `reports.paypal.com`

   - 次を入力します。 **[!UICONTROL Custom Path]** レポートが保存される場所。

     デフォルトでは、値は次のとおりです。 `/ppreports/outgoing`

1. スケジュールに従ってレポートを生成するには、 **[!UICONTROL Scheduled Fetching]** 設定：

   - 設定 **[!UICONTROL Enable Automatic Fetching]** から `Yes`.

   - 設定 **[!UICONTROL Schedule]** を次のいずれかに変更します。

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal は各レポートを 45 日間保持します。

   - 設定 **[!UICONTROL Time of Day]** を、時間、分および秒（秒）に設定します。

#### フロントエンドエクスペリエンス設定

Frontend Experience Settings を使用して、サイトに表示する PayPal ロゴを選択し、PayPal マーチャントページの外観をカスタマイズします。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Frontend Experience Settings]** 」セクションに入力します。

   ![フロントエンドエクスペリエンス設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL PayPal Product Logo]** ストアの PayPal ブロックに表示する

   PayPal ロゴは、4 つのスタイルと 2 つのサイズで使用できます。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal のマーチャントページの外観をカスタマイズするには、次の手順を実行します。

   - 名前を入力 **[!UICONTROL Page Style]** PayPal のマーチャントページに適用する

      - `paypal` - PayPal ページスタイルを使用します。
      - `primary` - _プライマリ_ スタイルを設定します。
      - `your_custom_value`  — アカウントプロファイルで指定されたカスタムの支払いページスタイルを使用します。

   - の場合 **[!UICONTROL Header Image URL]**」で、支払いページの左上隅に表示する画像の URL を入力します。 最大ファイルサイズは、幅 750 ピクセル、高さ 90 ピクセルです。

     >[!NOTE]
     >
     >PayPal では、画像を安全な (https) サーバーに配置することをお勧めします。 そうしないと、ブラウザーは、 _ページにセキュリティで保護された項目とセキュリティで保護されていない項目の両方が含まれています_.

   - ページの色を設定するには、6 文字の 16 進コード ( `#` 記号。次の各項目に対して使用します。

      - **[!UICONTROL Header Background Color]**  — チェックアウトページヘッダーの背景色。
      - **[!UICONTROL Header Border Color]**  — ヘッダーの周囲の 2 ピクセルの境界線のカラー。
      - **[!UICONTROL Page Background Color]**  — チェックアウトページ、ヘッダーおよび支払いフォームの周囲の背景色。

#### スマートボタンのカスタマイズ

The _スマート支払いボタン_ 機能を使用すると、PayPal ボタンをカスタマイズできます。このボタンは、「チェックアウト」、「製品の詳細」、「買い物かご」および「ミニ買い物かご」の各ページに表示できます。 PayPal の社内調査では、デフォルトのオプションが非常に認識可能で、購入率が高くなる可能性がありますが、そのデフォルトはストアのスタイルと一致しない場合があります。 以下を選択できます。

- PayPal ボタンのサイズ、色、形状
- PayPal ボタンに表示されるテキスト
- 複数のボタンが表示されている場合のレイアウト（水平または垂直）

ボタンをカスタマイズするには、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) 次の各セクションと設定を調整します。

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![チェックアウトページの設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_各ページタイプのボタンの表示を設定するには：_**

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 「 」セクションに表示されます。

1. 設定 **[!UICONTROL Customize Button]** から `Yes`.

1. PayPal がスマート支払いボタンに表示するテキストを設定するには、 **[!UICONTROL Label]** を次のいずれかに変更します。

   - `Checkout` - PayPal チェックアウト
   - `Pay` - PayPal チェックアウト
   - `Buy Now` - PayPal で今すぐ購入
   - `PayPal` - PayPal
   - `Installment`  - PayPal
   - `Credit` - PayPal クレジット

1. 設定 **[!UICONTROL Layout]** を次のいずれかに変更します。

   - `Vertical` - （デフォルト） PayPal のスマートボタンを垂直に表示します。 購入者は、PayPal にログインするか、PayPal アカウントを作成する必要があります。 **[!UICONTROL Enable Guest Checkout]** が選択されている。
   - `Horizontal` - PayPal のスマートボタンを水平に表示します。 条件 **[!UICONTROL Enable Guest Checkout]** が選択されている場合、 **[!UICONTROL Pay with Debit Card or Credit Card]** ボタンが PayPal ポップアップウィンドウに表示されます。 それ以外の場合、購入者は PayPal にログインするか、PayPal アカウントを作成する必要があります。

1. 設定 **[!UICONTROL Size]** を次のいずれかに変更します。

   - `Medium` - 250 ピクセル x 35 ピクセル。
   - `Large` - 350 ピクセル x 40 ピクセル。
   - `Responsive` - （デフォルト）コンテナの幅に合わせて調整します。 最小幅は 100 ピクセル、最大幅は 500 ピクセルです。 高さは、幅に基づいて動的に調整されます。

1. 設定 **[!UICONTROL Shape]** を次のいずれかに変更します。

   - `Pill` - （デフォルト）ボタンは丸薬のような形をしています（中央が長く、端が湾曲しています）。
   - `Rectangle`  — 長方形の四角形で、曲線を含まない四角形。

1. 設定 **[!UICONTROL Color]** を次のいずれかに変更します。

   - `Gold` （デフォルト）
   - `Blue`
   - `Silver`
   - `Black`

#### 機能

機能設定を使用すると、この PayPal ソリューションに関連する特定の機能を無効にできます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Features]** 」セクションに入力します。

   ![チェックアウトページの設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. を設定します。 **[!UICONTROL Disable Funding Options]** 他の PayPal 資金オプションを _チェックアウト_ ページに貼り付けます。

   選択したオプションは、 _チェックアウト_ ページに貼り付けます。 未選択のオプションは、PayPal が店舗通貨と購入者の場所をサポートする場合にのみ表示されます。 オプションは次のとおりです。

   - PayPal クレジット
   - ベンモ
   - PayPal ゲストチェックアウトクレジットカードアイコン
   - Elektronisches Lastschriftverfahren — ドイツ ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
