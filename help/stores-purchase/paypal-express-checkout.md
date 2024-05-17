---
title: PayPal Express チェックアウト
description: ストアでオンライン支払いソリューションとして PayPal Express Checkout を設定する方法を説明します。
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3093'
ht-degree: 0%

---

# PayPal Express チェックアウト

PayPal Express Checkout は、顧客がクレジットカードまたは個人の PayPal アカウントのセキュリティから支払う機能を提供することで、売上を高めるのに役立ちます。 チェックアウト時に、お客様は安全な PayPal サイトにリダイレクトされ、支払い情報を完了します。 その後、お客様はストアに戻され、チェックアウトプロセスの残りの部分が完了します。 「エクスプレスチェックアウト」を選択すると、売り上げの増加を報告されている、おなじみの PayPal ボタンがストアに追加されます。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日の時点で、ヨーロッパの銀行は満たされていない支払いを拒否する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件 PayPal Express Checkout がPSD2 に準拠するには、すべての要件が PayPal で処理されるため、何もする必要はありません。

現在 PayPal アカウントをお持ちのお客様は、 _[!UICONTROL Check out with PayPal]_ボタン。 エクスプレスチェックアウトは、スタンドアロンとして、または PayPal オールインワンソリューションの 1 つと共に使用できます。 既にオンラインでクレジットカードを受け入れている場合は、PayPal で支払うことを好む新規顧客を引き付けるための追加オプションとしてエクスプレスチェックアウトを提供できます。

>[!NOTE]
>
>PayPal は、PayPal Express Checkout を通じたデジタル商品の販売のサポートを廃止しており、次のいずれかを使用することをお勧めします [PayPal 支払い標準](paypal-payments-standard.md) または、を含む注文を処理する別の PayPal 支払いゲートウェイ [バーチャル製品](../catalog/product-create-virtual.md).

## 要件

- マーチャント： [ビジネス PayPal アカウント][1]
- 顧客： [個人用 PayPal アカウント][2]

## 高速チェックアウトワークフロー

他の支払い方法とは異なり、PayPal Express Checkout では、お客様は商品ページ、ミニカート、買い物かごから通常のチェックアウトワークフローの最初にチェックアウトできます。

1. **顧客の注文**  – お客様は、 _[!UICONTROL Check out with PayPal]_ボタン。
1. **顧客は PayPal サイトにリダイレクトされる** - トランザクションを完了するために、お客様は PayPal サイトにリダイレクトされます。
1. **顧客が PayPal アカウントにログインする**  – お客様は、PayPal アカウントにログインしてトランザクションを完了する必要があります。 支払いシステムは、PayPal アカウントからの請求情報と配送情報を使用します。
1. **顧客がチェックアウトページに戻る** - ユーザーはストアのチェックアウトページにリダイレクトされて注文を確認します。
1. **顧客の注文**  – お客様が注文し、注文情報が PayPal に送信されます。
1. **PayPal がトランザクションを決済します** - PayPal が注文を受け取り、トランザクションを決済します。

>[!NOTE]
>
>PayPal Express Checkout は、複数の住所を持つ注文をサポートしていません。

## コンテキスト内チェックアウト

PayPal の _コンテキスト内チェックアウト_ オンラインで支払うことをこれまで以上に簡単にします。 お客様は、このシンプルな 1 回または 2 回のクリックでシームレスなチェックアウト中にストアを見失うことはありません。 コンテキスト内チェックアウトは Mac と PC でも同様に機能し、デスクトップコンピューター、タブレット、モバイルデバイスで一貫したエクスペリエンスを提供します。 詳しくは、 [高速チェックアウトでのコンテキスト内チェックアウト][5].

![PayPal コンテキスト内チェックアウトデモ](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal コンテキスト内チェックアウトデモ_][6]

ストアの設定対象 [!DNL PayPal Express Checkout]このオプションを有効にすることができます。

## PayPal アカウントの設定

Commerce Admin で PayPal Express Checkout を設定する前に、PayPal Web サイトでマーチャントアカウントを設定する必要があります。

1. で PayPal の高度なアカウントにログインします。 [manager.paypal.com][3].

1. に移動 **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** さらに、次の設定を行います。

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. クリック **[!UICONTROL Save Changes]**.

1. 別のユーザーを設定します（PayPal が推奨）。

   - に移動 [manager.paypal.com][3] そして、あなたのアカウントにログインしてください。

   - 別のユーザーを設定するには、手順に従います。

   - クリック **[!UICONTROL Update]**.

## Commerceでの PayPal Express チェックアウトの設定

PayPal Express Checkout とオールインワンソリューションの 2 つの PayPal ソリューションを同時にアクティブにすることができます。 別のソリューションを有効にすると、以前に使用したソリューションが自動的に非アクティブになります。

>[!NOTE]
>
>クリック **[!UICONTROL Save Config]** 進行状況を保存する時間を指定できます。

### 手順 1：設定の開始

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. インストールに複数の web サイト、ストア、ビューがある場合は、を設定します **[!UICONTROL Store View]** この設定を適用するストア表示に移動します。

1. が含まれる _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地。

   この設定により、設定に表示される PayPal ソリューションの選択が決まります。

   ![商社国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 次の下 _[!UICONTROL Recommended Solutions]_を選択し、**[!UICONTROL Configure]**（用）**[!UICONTROL PayPal Express Checkout]**.

   ![PayPal Express チェックアウトの設定](./assets/paypal-express-checkout.png){width="600"}

### 手順 2:PayPal アカウントを有効にして接続する

1. 必要に応じて、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Required PayPal Settings]** セクション。

   ![PayPal アカウントを接続](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. テストまたは実稼動用にアカウントを接続：

   - テスト（開発）モードの場合は、 **[!UICONTROL Sandbox Credentials]** を入力します [PayPal サンドボックス][7] 資格情報。
   - 実稼動モードの場合は、をクリックします。 **[!UICONTROL Connect with PayPal]** そして、実稼動アカウントの資格情報を入力します。

   接続が検証されたら、続行できます。

1. を設定 **[!UICONTROL Enable this Solution]** 対象： `Yes`.

1. を有効にする [PayPal コンテキスト内チェックアウト](#in-context-checkout):

   - を設定 **[!UICONTROL Enable In-Context Checkout Experience]** 対象： `Yes`.

   - PayPal を入力 **[!UICONTROL Merchant Account ID]**.

     マーチャントアカウント ID は、PayPal ビジネスアカウントプロファイルに記載されています。

>[!NOTE]
>
>[PayPal クレジット](paypal.md#paypal-credit-and-pay-later) この支払いオプションに対してデフォルトで有効になっています。

### 手順 3：必要な PayPal 設定を完了する

1. 必要に応じて、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Express Checkout]** セクション。

   ![PayPal Express チェックアウト必須設定](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. （任意） **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >メールアドレスでは大文字と小文字が区別されます。 支払いを受け取るには、入力するメールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致する必要があります。

   PayPal アカウントをお持ちでない場合は、 **[!UICONTROL Start accepting payments via PayPal]**.

1. を設定 **[!UICONTROL API Authentication Methods]** を次のいずれかに変更します。

   - `API Signature`  – この PayPal 認証方法は実装が最も簡単で、ユーザー名、パスワード、およびアカウントを識別する一意の文字列と数字に基づいています。 API 署名資格情報の有効期限はありません。
   - `API Certificate`  – この PayPal 認証方法はより安全で、ユーザー名、パスワード、ダウンロード可能な証明書に基づいています。 API 資格情報は 3 年後に期限切れになり、更新する必要があります。

   必要に応じて、次の手順を実行します。

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. サンドボックスアカウントの資格情報を使用している場合は、次のように設定します **[!UICONTROL Sandbox Mode]** 対象： `Yes`.

   サンドボックスで設定をテストする場合は、のみを使用します [クレジットカード番号][4] それは PayPal で推奨されています。 実稼動に移行する準備が整ったら、設定に戻り、サンドボックスモードをに設定します。 `No` そして、実稼動 PayPal アカウントに接続します。

1. お使いのシステムがプロキシサーバーを使用してCommerceと PayPal 支払いシステムの間で接続を確立する場合は、を設定します **[!UICONTROL API Uses Proxy]** 対象： `Yes` 次の手順を実行します。

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

この一連の手順の最後に、必要な PayPal 設定が完了します。 「基本設定」と「詳細設定」を選択して続行するか、 **[!UICONTROL Save Config]** 設定を調整するために後で戻る

### 手順 4：広告 PayPal クレジット/広告 PayPal PayLater の設定（オプション）

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

を設定 **[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに変更します。

- `Yes`  – 広告 PayPal PayLater を設定するには
- `No`  – 広告 PayPal クレジットを設定する

>[!NOTE]
>
>この **[!UICONTROL Enable PayPal PayLater Experience]** を設定しても、 [!DNL PayPal PayLater] 機能するが削除されない **_[!UICONTROL PayPal PayLater]_** ストアフロントのボタン。 両方を無効にするには **_[!UICONTROL PayPal PayLater]_** および **_[!UICONTROL PayPal Credit]_** ストアフロントのボタンで、 `PayPal Credit` の値 **[!UICONTROL Disable Funding Options]** 設定（[!UICONTROL Advanced Settings] 未満 [!UICONTROL Frontend Experience Settings]）に設定します。

#### PayPal クレジットのアドバタイズ

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advertise PayPal Credit]** セクション。

1. アカウント情報を取得するには、 **[!UICONTROL Get Publisher ID from PayPal]** 指示に従ってください。

1. を入力 **[!UICONTROL Publisher ID]**.

   ![PayPal クレジットのアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Home Page]** セクション。

1. ページにバナーを配置するには、を設定します **[!UICONTROL Display]** 対象： `Yes`.

1. を設定 **[!UICONTROL Position]** を次のいずれかに変更します。

   - `Header (center)`
   - `Sidebar (right)`

1. を設定 **[!UICONTROL Size]** を次のいずれかに変更します。

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![PayPal クレジット ホーム ページ設定のアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 残りのセクションと前の手順を繰り返します。

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### PayPal PayLater のアドバタイズ

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advertise PayPal PayLater]** セクション。

1. を設定 **[!UICONTROL Enable PayPal PayLater]** 対象： `Yes`.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Home Page]** セクション。

1. ページにバナーを配置するには、を設定します **[!UICONTROL Display]** 対象： `Yes`.

1. を設定 **[!UICONTROL Position]** を次のいずれかに変更します。

   - `Header (center)`
   - `Sidebar`

1. を設定 **[!UICONTROL Style Layout]** を次のいずれかに変更します。

   - `Text`
   - `Flex`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** のみ、設定 **[!UICONTROL Logo Type]** を次のいずれかに変更します。

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** のみ、設定 **[!UICONTROL Logo Position]** を次のいずれかに変更します。

   - `Left`
   - `Right`
   - `Top`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** のみ、設定 **[!UICONTROL Text Color]** を次のいずれかに変更します。

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Text]** のみ、設定 **[!UICONTROL Text Size]** を次のいずれかに変更します。

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Flex]** のみ、設定 **[!UICONTROL Ratio]** を次のいずれかに変更します。

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. の場合 [!UICONTROL Style Layout] **[!UICONTROL Flex]** のみ、設定 **[!UICONTROL Color]** を次のいずれかに変更します。

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![PayPal クレジット ホーム ページ設定のアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 残りのセクションと前の手順を繰り返します。

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 手順 5：基本設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Basic Settings - PayPal Express Checkout]** セクション。

   ![Basic Settings](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルを使用することをお勧めします _PayPal_ すべてのストア表示の場合。

1. 複数の支払方法を提供する場合は、次の番号を入力します **[!UICONTROL Sort Order]** 他の支払い方法と共にリストされた際に、PayPal Express チェックアウトが表示される順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認し、資金を保留します。 金額は確定するまで引き出されません _キャプチャ済み_ 商人によって。
   - `Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。
   - `Order`  – 注文金額は、PayPal の顧客残高、銀行口座、クレジットカードでキャプチャまたは承認されていません。 注文支払いアクションは、PayPal 支払いシステムとマーチャントの間の契約を表します。 これにより、マーチャントは、最大 29 日間にわたって、顧客の買い手口座から注文された合計までの 1 つ以上の金額をキャプチャできます。 資金が注文された後、マーチャントは次の 29 日間の間にいつでも資金を取り込むことができます。 注文金額のキャプチャは、1 つ以上の請求書を作成することにより、Commerce管理者からのみ実行できます。

1. を表示するには _[!UICONTROL Check out with PayPal]_ボタンを使用して、次を設定します&#x200B;**[!UICONTROL Display on Product Details Page]**対象： `Yes`.

1. 支払アクションが次のように設定されている場合 `Order`、次の手順を完了します

   - **[!UICONTROL Authorization Honor Period (days)]** - プライマリ認証が有効なままである期間を決定します。 値は、PayPal マーチャントアカウントの対応する値と等しくなければなりません。 PayPal マーチャントアカウントのデフォルト値はです `3`. この数を増やすには、PayPal に連絡する必要があります。 この承認は、米国太平洋標準時（PT）の最終日の午後 11 時 49 分に無効になります。

   - **[!UICONTROL Order Valid Period (days)]**  – 注文が有効である期間を決定します。 注文が無効になると、請求書を作成できなくなります。 PayPal マーチャントアカウントの「注文有効期間」の値と等しい値を指定します。 PayPal マーチャントアカウントのデフォルト値はです `29`. この番号を変更するには、PayPal に連絡する必要があります。

   - **[!UICONTROL Number of Child Authorizations]**  – 単一の受注に対する承認の最大数を指定します。これにより、受注に対して作成できるオンライン部分請求書の最大数が決まります。 この値は、PayPal マーチャントアカウントの対応する設定と等しい必要があります。 PayPal アカウントの子認証のデフォルト数は次のとおりです。 `1`. この数を増やすには、PayPal に連絡する必要があります。

### 手順 6：詳細設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

   ![詳細設定 – PayPal Express チェックアウト](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Display on Shopping Cart]** 対象： `Yes`.

1. を設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  – 店舗の構成で指定されたすべての国の顧客は、この支払い方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. 支払システムとの通信をログ・ファイルに書き込むには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   PayPal Payments Advanced のログファイルはです。 `_payflow_advanced.log`.

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. PayPal サイトの明細項目別の顧客注文の完全な概要を表示するには、次のように設定します **[!UICONTROL Transfer Cart Line Items]** 対象： `Yes`.

1. 最大 10 件の出荷オプションを要約に含めるには、次のように設定します **[!UICONTROL Transfer Shipping Options]** 対象： `Yes`. （このオプションは、明細項目が転送に設定されている場合にのみ表示されます。）

1. PayPal 受け入れボタンに使用する画像のタイプを決定するには、を設定します **[!UICONTROL Shortcut Buttons Flavor]** を次のいずれかに変更します。

   - `Dynamic` - （推奨） PayPal サーバーから動的に変更できる画像を表示します。
   - `Static`  – 動的に変更できない特定の画像を表示します。

1. PayPal アカウントを持たない顧客がこの方法で購入できるようにするには、次のように設定します **[!UICONTROL Enable PayPal Guest Checkout]** 対象： `Yes`.

1. を設定 **[!UICONTROL Require Customer's Billing Address]** を次のいずれかに変更します。

   - `Yes`  – すべての購入に対して、顧客の請求先住所が必要です。
   - `No`  – 購入に際して、顧客の請求先住所は必要ありません。
   - `For Virtual Quotes Only`  – 仮想見積もりのみに対して、顧客の請求先住所が必要です。

   >[!NOTE]
   >
   >この機能は、PayPal テクニカルサポートを通じてマーチャントアカウントで有効にする必要があります。

1. （オプション）を設定します **[!UICONTROL Billing Agreement Signup]** 顧客がに署名できるようにする [請求契約](paypal-billing-agreements.md) 顧客アカウントに有効な請求契約がない場合、PayPal 支払いシステムのストアで以下を行います。

   - `Auto`  – お客様は、エクスプレスチェックアウトフロー中に請求契約に署名するか、別の支払い方法を使用できます。
   - `Ask Customer`  – お客様は、エクスプレスチェックアウトフロー中に請求契約に署名するかどうかを決定できます。
   - `Never`  – お客様は、エクスプレスチェックアウトフロー中に請求契約に署名できません。

   >[!NOTE]
   >
   >商人は尋ねなければならない [PayPal マーチャントテクニカルサポート](https://developer.paypal.com/support/) をクリックして、アカウントで請求契約を有効にします。 この _請求契約のサインアップ_ パラメーターは、PayPal がマーチャントアカウントに対して請求契約が有効であることを確認した後にのみ有効になります。

1. お客様が注文レビューのためにストアに戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、次のように設定します **[!UICONTROL Skip Order Review Step]** 対象： `Yes`.

1. ストアの必要に応じて、次の追加セクションを完了します。

   - [PayPall 請求契約の設定](#paypal-billing-agreement-settings)
   - [決済報告書の設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)
   - [スマートボタンのカスタマイズ](#customize-smart-buttons)
   - [機能](#features)

1. 完了したら、 **[!UICONTROL Save Config]**.

#### PayPal 請求契約設定

A [請求契約](paypal-billing-agreements.md) は、PayPal によって複数の注文での使用が許可されている、マーチャントと顧客の間の販売契約です。 チェックアウトプロセス中に、請求契約の支払いオプションは、会社と請求契約を既に入力している顧客にのみ表示されます。 PayPal が契約を承認すると、支払いシステムは、契約に関連付けられている各注文を識別するための一意の参照 ID を発行します。 発注書と同様に、顧客が会社で設定できる請求契約の数に制限はありません。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL PayPal Billing Agreement Settings]** セクション。

   ![請求契約の設定](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enabled]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時の PayPal 請求契約メソッドを識別するタイトルを入力します。

1. 複数の支払い方法を提供する場合は、 **[!UICONTROL Sort Order]** チェックアウト時に他の支払い方法と共に表示される請求契約の表示順序を決定するフィールド。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認し、資金を保留します。 この金額は、マーチャントによって「キャプチャ」されるまで引き出されません。
   - `Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. を設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  – 店舗の構成で指定されたすべての国の顧客は、この支払い方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれの国をクリックします。

1. 支払システムとの通信をログ・ファイルに記録するには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. SSL 検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. PayPal 支払いページで顧客の注文の各行項目の概要を表示するには、次のように設定します **[!UICONTROL Transfer Cart Line Items]** 対象： `Yes`.

1. 顧客が顧客アカウントのダッシュボードから請求契約を開始できるようにするには、次のように設定します **[!UICONTROL Allow in Billing Agreement Wizard]** 対象： `Yes`.

#### 決済報告書の設定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Settlement Report Settings]** セクション。

   ![決済報告書の設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL SFTP Credentials]**、次の手順を実行します。

   - PayPal セキュア FTP サーバーに新規登録している場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - 前にテストレポートを実行するには _運用開始_ サイトの高速チェックアウトを使用して、を設定します **[!UICONTROL Sandbox Mode]** 対象： `Yes`.

   - を入力 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     デフォルト値はです。 `reports.paypal.com`

   - を入力 **[!UICONTROL Custom Path]** レポートの保存場所。

     デフォルト値はです。 `/ppreports/outgoing`

1. スケジュールに従ってレポートを生成するには、を実行します **[!UICONTROL Scheduled Fetching]** 設定：

   - を設定 **[!UICONTROL Enable Automatic Fetching]** 対象： `Yes`.

   - を設定 **[!UICONTROL Schedule]** を次のいずれかに変更します。

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal は各レポートを 45 日間保持します。

   - を設定 **[!UICONTROL Time of Day]** レポートを生成する時、分、秒。

#### フロントエンドエクスペリエンス設定

フロントエンドエクスペリエンス設定を使用すると、サイトに表示する PayPal ロゴを選択したり、PayPal マーチャントページの外観をカスタマイズしたりできます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Frontend Experience Settings]** セクション。

   ![フロントエンドエクスペリエンス設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 「」を選択します **[!UICONTROL PayPal Product Logo]** ストアの PayPal ブロックに表示する。

   PayPal ロゴは、4 つのスタイルと 2 つのサイズで使用できます。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal マーチャントページの外観をカスタマイズするには、次の手順を実行します。

   - の名前を入力 **[!UICONTROL Page Style]** paypal マーチャントページに適用する手順は次のとおりです。

      - `paypal` - PayPal ページスタイルを使用します。
      - `primary`  – として識別したページスタイルを使用します _プライマリ_ アカウントプロファイルのスタイル。
      - `your_custom_value` - アカウントプロファイルで指定されているカスタム支払いページスタイルを使用します。

   - の場合 **[!UICONTROL Header Image URL]**、支払いページの左上隅に表示する画像の URL を入力します。 最大ファイルサイズは、幅 750 ピクセル、高さ 90 ピクセルです。

     >[!NOTE]
     >
     >PayPal では、画像をセキュアな（https）サーバーに配置することをお勧めします。 そうでない場合、ブラウザーは次の警告を表示する場合があります _ページには、セキュリティで保護された項目と保護されていない項目の両方が含まれています_.

   - ページのカラーを設定するには、6 文字の 16 進コードを `#` 記号。次の各項目について説明します。

      - **[!UICONTROL Header Background Color]** - チェックアウトページヘッダーの背景色
      - **[!UICONTROL Header Border Color]** - ヘッダーの周囲の 2 ピクセルの境界線の色。
      - **[!UICONTROL Page Background Color]** - チェックアウトページ、およびヘッダーと支払いフォーム周辺の背景色

#### スマートボタンのカスタマイズ

この _スマート支払いボタン_ paypal ボタンをカスタマイズできます。このボタンは、「チェックアウト」、「製品詳細」、「買い物かご」、「ミニ買い物かご」の各ページに表示できます。 PayPal の内部調査では、デフォルトのオプションは非常に認識可能であり、購入率の増加につながる可能性があることを示唆していますが、デフォルトはストアのスタイル設定と一致しない可能性があります。 以下から選択できます。

- PayPal ボタンのサイズ、色、形状
- PayPal ボタンに表示するテキスト
- 複数のボタンが表示されている場合のレイアウト（水平または垂直）

ボタンをカスタマイズするには、を展開します ![展開セレクター](../assets/icon-display-expand.png) 以下の各セクションを参照し、設定を調整します。

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![チェックアウトページの設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_各ページタイプのボタンの表示を設定するには：_**

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) セクション。

1. を設定 **[!UICONTROL Customize Button]** 対象： `Yes`.

1. PayPal がスマート支払いボタンに表示するテキストを設定するには、次のように設定します **[!UICONTROL Label]** を次のいずれかに変更します。

   - `Checkout` - PayPal チェックアウト
   - `Pay` - PayPal チェックアウト
   - `Buy Now` - PayPal で今すぐ購入
   - `PayPal` - PayPal
   - `Installment`  - PayPal
   - `Credit` - PayPal クレジット

1. を設定 **[!UICONTROL Layout]** を次のいずれかに変更します。

   - `Vertical` - （デフォルト） PayPal スマートボタンを垂直方向に表示します。 購入者は、PayPal にログインするか、PayPal アカウントを作成する必要があります。 **[!UICONTROL Enable Guest Checkout]** が選択されました。
   - `Horizontal` - PayPal スマートボタンを水平方向に表示します。 条件 **[!UICONTROL Enable Guest Checkout]** が選択されている場合、 **[!UICONTROL Pay with Debit Card or Credit Card]** ボタンが PayPal ポップアップウィンドウに表示されます。 それ以外の場合、購入者は PayPal にログインするか、PayPal アカウントを作成する必要があります。

1. を設定 **[!UICONTROL Size]** を次のいずれかに変更します。

   - `Medium` - 250 ピクセル x 35 ピクセル。
   - `Large` - 350 ピクセル x 40 ピクセル。
   - `Responsive` - （デフォルト）コンテナの幅に合わせて調整します。 最小幅は 100 ピクセル、最大幅は 500 ピクセルです。 高さは幅に基づいて動的に調整されます。

1. を設定 **[!UICONTROL Shape]** を次のいずれかに変更します。

   - `Pill` - （既定値） ボタンはピルのような形をしています（中央は長く、端はカーブしています）。
   - `Rectangle`  – 四角形のシェイプ（曲線なし）。

1. を設定 **[!UICONTROL Color]** を次のいずれかに変更します。

   - `Gold` （デフォルト）
   - `Blue`
   - `Silver`
   - `Black`

#### 機能

機能設定を使用すると、この PayPal ソリューションに関連する特定の機能を無効にすることができます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Features]** セクション。

   ![チェックアウトページの設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. を **[!UICONTROL Disable Funding Options]** に表示される他の PayPal 資金調達オプションを決定するには _チェックアウト_ ページ。

   選択したオプションがに表示されません _チェックアウト_ ページ。 選択されていないオプションは、PayPal がストア通貨と購入者の場所をサポートしている場合にのみ表示されます。 次のようなオプションがあります。

   - PayPal クレジット
   - ベンモ
   - PayPal ゲスト チェックアウト クレジット カード アイコン
   - Elektronisches Lastschriftverfahren - ドイツ語 ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
