---
title: PayPal 支払い標準
description: ストアでオンライン支払いソリューションとして PayPal Payments Standard を設定する方法を説明します。
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2064'
ht-degree: 0%

---

# PayPal 支払い標準

[PayPal 支払い標準][4] オンラインで支払いを受け入れる最も簡単な方法です。 お店にチェックアウトボタンを追加するだけで、クレジットカードと PayPal の両方でお支払いの便利さを顧客に提供できます。

>[!NOTE]
>
>米国外の商人の場合、と呼ばれます _PayPal Website Payments Standard_.

PayPal Payments Standard を使用すると、モバイルデバイスでクレジットカードをスワイプできます。 月額料金はかかりません。eBay を通じて支払いを受けることができます。 サポートされるクレジットカードには、Visa、MasterCard、Discover、American Express が含まれます。 また、お客様は個人の PayPal アカウントから直接支払うことができます。 PayPal Payments Standard は、PayPal のワールドワイドなリファレンスリストのすべての国で利用できます。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日の時点で、ヨーロッパの銀行は満たされていない支払いを拒否する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件 PayPal Payments Standard がPSD2 に準拠するには、すべての要件が PayPal で処理されるので、何もする必要はありません。

## マーチャントの要件

- [PayPal ビジネスアカウント][1]

## チェックアウトワークフロー

顧客の場合、PayPal Payments Standard は、個人の PayPal アカウントのクレジットカード情報が最新の場合、1 つの手順で処理されます。

1. **顧客の注文**  – お客様は、 _Pay Now_ 購入を完了するためのボタン。

1. **PayPal はトランザクションを処理します** - トランザクションを完了するために、お客様は PayPal サイトにリダイレクトされます。

## PayPal 支払い標準の設定

>[!NOTE]
>
>PayPal Payments Standard は、Express Checkout を含む他の PayPal メソッドと同時に使用することはできません。 支払いソリューションを変更すると、以前に使用したソリューションは無効になります。

>[!TIP]
>
>クリック **[!UICONTROL Save Config]** 進行状況を保存する時間を指定できます。

### 手順 1：設定の開始

この設定方法は、既存の PayPal アカウントがあることを前提としています。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. Commerceのインストールに複数の web サイト、ストアまたはビューがある場合は、を設定します **[!UICONTROL Store View]** この設定を適用するストア表示に移動します。

1. が含まれる _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地。

   この設定により、設定に表示される PayPal ソリューションの選択が決まります。

   ![商社国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. を展開 **[!UICONTROL PayPal All-in-One Payment Solutions]** をクリックして、 **[!UICONTROL Configure]** （用） **[!UICONTROL Payments Standard]**.

   ![PayPal 支払い標準](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### 手順 2:PayPal アカウントを有効にして接続する

![PayPal 支払い標準設定](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. テストまたは実稼動用にアカウントを接続：

   - テスト（開発）モードの場合は、 **[!UICONTROL Sandbox Credentials]** を入力します [PayPal サンドボックス][3] 資格情報。
   - 実稼動モードの場合は、をクリックします。 **[!UICONTROL Connect with PayPal]** そして、実稼動アカウントの資格情報を入力します。

   接続が検証されたら、続行できます。

1. を設定 **[!UICONTROL Enable this Solution]** 対象： `Yes`.

1. を提供したい場合 [PayPal クレジット](paypal.md#paypal-credit-and-pay-later) 顧客に、次を設定 **[!UICONTROL Enable PayPal Credit]** 対象： `Yes`.

### 手順 3：支払の標準設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Payments Standard]** セクション。

   ![必須の設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. を入力 **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

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

   サンドボックスで設定をテストする場合は、のみを使用します [クレジットカード番号][2] それは PayPal で推奨されています。 実稼動に移行する準備が整ったら、設定に戻り、サンドボックスモードをに設定します。 `No` そして、実稼動 PayPal アカウントに接続します。

1. プロキシサーバーを使用してAdobe CommerceまたはMagento Open Sourceと PayPal 支払いシステムを連携させる場合は、次のように設定します **[!UICONTROL API Uses Proxy]** 対象： `Yes` 次の手順を実行します。

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### 手順 4：広告 PayPal クレジット/広告 PayPal PayLater の設定（オプション）

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

を設定 **[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに変更します。

- `Yes`  – 広告 PayPal PayLater を設定するには
- `No`  – 広告 PayPal クレジットを設定する

#### PayPal クレジットのアドバタイズ

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advertise PayPal Credit]** セクション。

   ![PayPal クレジット ホーム ページ設定のアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 残りのセクションと前の手順を繰り返します。

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### PayPal PayLater のアドバタイズ

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advertise PayPal PayLater]** セクション。

1. を設定 **[!UICONTROL Enable PayPal PayLater]** 対象： `Yes`.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Home Page]** セクション。

   ![PayPal クレジット ホーム ページ設定のアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 残りのセクションと前の手順を繰り返します。

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **チェックアウト支払い手順**
   - **[!UICONTROL Catalog Category Page]**

### 手順 5：基本設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** セクション。

   ![Basic Settings](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルを使用することをお勧めします _PayPal_ すべてのストア表示の場合。

1. 複数の支払方法を提供する場合は、次の番号を入力します **[!UICONTROL Sort Order]** 他の支払い方法と共にリストされた際に PayPal 支払い標準が表示される順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認し、資金を保留します。 この金額は、マーチャントによって取り込まれるまで引き出されません。
   - `Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. を表示するには _[!UICONTROL Check out with PayPal]_ボタンを使用して、次を設定します&#x200B;**[!UICONTROL Display on Product Details Page]**対象： `Yes`.

### 手順 6：詳細設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

   ![詳細設定](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. PayPal Payments Standard をショッピングカートとミニカートの両方から利用できるようにするには、次のように設定します **[!UICONTROL Display on Shopping Cart]** 対象： `Yes`.

1. を設定 **[!UICONTROL Payment from Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、それぞれのオプションをクリックします。

1. 支払システムとの通信をログ・ファイルに記録するには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. SSL 検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. PayPal 支払いページに注文の各行項目の概要を表示するには、次のように設定します **[!UICONTROL Transfer Cart Line Items]** 対象： `Yes`.

   最大 10 件の出荷オプションを要約に含めるには、次のように設定します **[!UICONTROL Transfer Shipping Options]** 対象： `Yes`. （このオプションは、明細項目が転送に設定されている場合にのみ表示されます。）

1. PayPal 受け入れボタンに使用する画像のタイプを決定するには、を設定します **[!UICONTROL Shortcut Buttons Flavor]** を次のいずれかに変更します。

   - `Dynamic` - （推奨） PayPal サーバーから動的に変更できる画像を表示します。
   - `Static`  – 動的に変更できない特定の画像を表示します。

1. PayPal アカウントを持っていないお客様がこの方法で購入できるようにするには、を設定します **[!UICONTROL Enable PayPal Guest Checkout]** 対象： `Yes`.

1. を設定 **[!UICONTROL Require Customer's Billing Address]** を次のいずれかに変更します。

   - `Yes`  – すべての購入に対して、顧客の請求先住所が必要です。
   - `No`  – 購入に対してお客様の請求先住所は必要ありません。
   - `For Virtual Quotes Only`  – 仮想見積もりのみに対して、お客様の請求先住所が必要です。

1. 顧客がにエントリできるようにするには [PayPal 請求契約](paypal-billing-agreements.md) 顧客アカウントに利用可能なアクティブな請求契約がない場合は、ストアでを設定します **[!UICONTROL Billing Agreement Signup]** を次のいずれかに変更します。

   - `Auto`  – お客様は、エクスプレスチェックアウトフロー中に請求契約を締結するか、別の支払い方法を使用できます。
   - `Ask Customer`  – お客様は、エクスプレスチェックアウトワークフロー中に請求契約を締結するかどうかを決定できます。
   - `Never`  – お客様は、エクスプレスチェックアウトワークフロー中に請求契約を締結できません。

   >[!NOTE]
   >
   >マーチャントは、PayPal マーチャントテクニカルサポートにリクエストして、アカウントで請求契約を有効にする必要があります。 この _請求契約のサインアップ_ パラメーターは、PayPal がマーチャントアカウントに対して請求契約が有効であることを確認した後にのみ有効にできます。

1. お客様が注文レビューのためにストアに戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、次のように設定します **[!UICONTROL Skip Order Review Step]** 対象： `Yes`.

### 手順 7：設定を完了して保存する

1. ストアの必要に応じて、次の節を完了します。

   - [PayPal 請求契約設定](#paypal-billing-agreement-settings)
   - [決済報告書の設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

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

   - サイトで高速チェックアウトを使用して運用を開始する前にテストレポートを実行するには、次を設定します **[!UICONTROL Sandbox Mode]** 対象： `Yes`.

   - を入力 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     デフォルト値はです `reports.paypal.com`.

   - を入力 **[!UICONTROL Custom Path]** レポートの保存場所。

     デフォルト値はです `/ppreports/outgoing`.

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

の使用 _[!UICONTROL Frontend Experience Settings]_サイトに表示する PayPal ロゴを選択したり、PayPal のマーチャントページの外観をカスタマイズしたりできます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Frontend Experience Settings]** セクション。

   ![フロントエンドエクスペリエンス設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 「」を選択します **[!UICONTROL PayPal Product Logo]** ストアの PayPal ブロックに表示する。

   PayPal ロゴは、4 つのスタイルと 2 つのサイズで使用できます。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal マーチャントページの外観をカスタマイズするには：

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

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
