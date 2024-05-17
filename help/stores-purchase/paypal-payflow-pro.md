---
title: PayPal Payflow Pro
description: ストアでオンライン支払いソリューションとして PayPal Payflow Pro を設定する方法を説明します。
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2163'
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro ゲートウェイ（旧称：） _Verisign_&#x200B;は、米国、カナダ、オーストラリアおよびニュージーランドのお客様が利用できます。 他の PayPal の支払い方法とは異なり、加盟店は月額固定料金に加えて、数に関係なく、各取引に対して固定料金を請求されます。

![PayPal でチェックアウト](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日の時点で、ヨーロッパの銀行は満たされていない支払いを拒否する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件 PSD2 に準拠するには、PayPal Payflow Pro をサードパーティのプラグインと統合する必要があります。 詳しくは、 [ペイフロー用の 3-D セキュア](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## 要件

- [PayPal ビジネスアカウント][1] - PayPal Payflow Pro ゲートウェイは、PayPal のマーチャントアカウントをマーチャントウェブサイトとリンクし、ゲートウェイとマーチャントアカウントの両方として機能します。

- 複数のAdobe CommerceおよびMagento Open Source web サイトを管理する場合は、web サイトごとに個別の PayPal マーチャントアカウントが必要です。

## 顧客のワークフロー

1. **顧客がチェックアウトに移動** - チェックアウト時に、お客様は PayPal Payflow Pro での支払いを選択し、クレジットカード情報を入力します。 お客様は PayPal の個人アカウントを持つ必要はありません。 ただし、販売国によっては、お客様は個人の PayPal アカウントを使用して注文の支払いをすることもできます。
1. **顧客が注文を送信**  – 顧客が注文を送信し、注文情報が PayPal に送信されて処理されます。 顧客はサイトのチェックアウトページから移動しません。
1. **PayPal がトランザクションを完了します**  – お支払いは注文時に受け付けられます。 設定で指定された支払処理に応じて、受注または受注と請求書のいずれかが作成されます。

## オンライン注文処理ワークフロー

1. **管理者がオンライン請求書を送信**  – 店舗管理者がオンライン請求書を送信し、その結果、対応するトランザクションと請求書が作成されます。
1. **PayPal がトランザクションを受信します**  – 注文情報は PayPal に送信されます。 トランザクションのレコードと請求書が生成されます。 すべての Payflow Pro Gateway 取引は、 [PayPal マーチャントアカウント][2].

>[!NOTE]
>
>PayPal Payflow Pro では、部分請求および部分払い戻しはサポートされていません。

## PayPal アカウントの設定

1. にログイン [PayPal ビジネスアカウント][2].

1. の設定 [ホストされたチェックアウトページ][4] 次の設定で PayPal Manager を使用します。

   - 次の下 **[!UICONTROL Choose your settings]**、設定 **[!UICONTROL Transaction Process Mode]** 対象： `Live`.

   - 次の下 **[!UICONTROL Display options on payment page]**、設定 **Cancel URL Method** 対象： `POST`.

   - 次の下 **[!UICONTROL Billing Information]**&#x200B;で、カードセキュリティコードを選択します **[!UICONTROL CSC]** 必須フィールドと編集可能フィールドの両方のチェックボックス。

   - 次の下 **[!UICONTROL Payment Confirmation]**、設定 **[!UICONTROL Return URL Method]** 対象： `POST`.

   - 次の下 **[!UICONTROL Security Options]**&#x200B;の場合、次の設定を完了します。

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - を選択 **[!UICONTROL Customize]**&#x200B;を選択してから、 **[!UICONTROL Layout C]**.

     レイアウト C では、クレジットカードとデビットカードのフィールドのみが表示され、サイトにフレームを組み込んだり、スタンドアロンポップアップとして使用したりできます。 サイズは 490 x 565 ピクセルで固定され、エラーメッセージ用のスペースも追加されます。 一部のシステムでは、この設定によりトランスペアレント リダイレクトの問題が修正されます。

1. 設定が完了したら、 **[!UICONTROL Save and Publish]**.

1. PayPal Manager メニューで、 **[!UICONTROL Account Administration]**.

1. 次の下 **[!UICONTROL Manage Security]**&#x200B;を選択し、 **[!UICONTROL Transaction Settings]** 次の手順を実行します。

   - を設定 **[!UICONTROL Allow reference transactions]** 対象： `Yes`.

   - クリック **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >複数のCommerce Web サイトがある場合は、それぞれに個別の PayPal 支払い詳細アカウントを作成する必要があります。

1. 別のユーザーを設定します（PayPal が推奨）。

   - メイン メニューの 2 行目で、をクリックします。 **[!UICONTROL Manage Users]**.

   - 別のユーザーをアカウントに追加するには、 **[!UICONTROL Add User]**. リンクは、ユーザーを管理タイトルのすぐ上にあります。

   - の次のセクションの必須フィールドに入力します _[!UICONTROL Add User]_フォーム：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - クリック **[!UICONTROL Update]**.

1. 必ず PayPal アカウントからログアウトしてください。

## Commerceでの PayPal Payflow Pro の設定

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

1. を展開 **[!UICONTROL PayPal Payment Gateways]** （必要な場合）を選択し、 **[!UICONTROL Configure]** （用） **[!UICONTROL Payflow Pro]**.

   ![設定 – Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### 手順 2：必要な PayPal 設定を完了する

![必須設定 – PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. （任意） **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >メールアドレスでは大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致する必要があります。

1. PayPal マーチャントアカウントへのログインに使用する次の資格情報のいずれかを入力します。

   - **[!UICONTROL Partner]** - PayPal パートナー ID。
   - **[!UICONTROL User]** - PayPal アカウントで設定されている別のユーザーの ID。
   - **[!UICONTROL Vendor]** - PayPal ユーザーログイン名。

1. を入力 **[!UICONTROL Password]** これは PayPal アカウントに関連付けられています。

1. テストトランザクションを実行するには、次を設定します **[!UICONTROL Test Mode]** 対象： `Yes`.

   サンドボックスで設定をテストする場合は、のみを使用します [クレジットカード番号][3] それは PayPal で推奨されています。 実稼動に移行する準備ができたら、設定に戻ってテストモードをに設定します。 `No`.

1. システムがプロキシサーバーを使用して PayPal システムへの接続を確立する場合は、を設定します **[!UICONTROL Use Proxy]** 対象： `Yes` 次の手順を実行します。

   - の IP アドレスを入力 **[!UICONTROL Proxy Host]**.

   - のポート番号を入力します **[!UICONTROL Proxy Port]**.

     プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを防ぐ場合に使用されます。 この場合、サードパーティのサーバーを使用してトラフィックがリレーされます。

1. を設定 **[!UICONTROL Enable this Solution]** 対象： `Yes`.

1. を提供したい場合 [PayPal クレジット](paypal.md#paypal-credit-and-pay-later) 顧客に、次を設定 **[!UICONTROL Enable PayPal Credit]** 対象： `Yes`.

1. 顧客の支払い/クレジットカードの詳細を安全に保存して、顧客が毎回の支払情報を再入力する必要がない場合は、次のように設定します **[!UICONTROL Vault Enabled]** 対象： `Yes`.

### 手順 3：広告 PayPal クレジット/広告 PayPal PayLater の設定（オプション）

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

を設定 **[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに変更します。

- `Yes`  – 広告 PayPal PayLater を設定するには
- `No`  – 広告 PayPal クレジットを設定する

#### PayPal クレジットのアドバタイズ

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advertise PayPal Credit]** セクション。

   ![PayPal クレジットのアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. アカウント情報を取得するには、 **[!UICONTROL Get Publisher ID from PayPal]** 指示に従ってください。

1. を入力 **[!UICONTROL Publisher ID]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Home Page]** セクション。

   ![PayPal クレジット ホーム ページ設定のアドバタイズ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) 残りのセクションと、ホームページ設定に関して前の手順を繰り返します。

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順 4：基本設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Basic Settings - PayPal Payflow Pro]** セクション。

   ![基本設定 – PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**&#x200B;を入力し、チェックアウト時に PayPal Payflow Pro を識別するタイトルを入力します。

   タイトルを使用することをお勧めします _デビットまたはクレジットカード_.

1. 複数の支払方法を提供する場合は、次の番号を入力します **[!UICONTROL Sort Order]** 他の支払い方法でリストされた際に Payflow Pro が表示される順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認し、資金を保留します。 この金額は、マーチャントによって取り込まれるまで引き出されません。
   - `Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. の場合 **[!UICONTROL Credit Card Settings]**&#x200B;で、ストアでのお支払いに使用できるクレジットカードを選択します。

   複数のカードを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、それぞれのカードをクリックします。

   >[!NOTE]
   >
   >American Express は追加契約が必要です。

### 手順 5：詳細設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

   ![詳細設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー（PC）または Command キー（Mac）を押しながら、リスト内で、お客様がストアから購入できる国を選択します。

1. 支払システムとの通信をログ・ファイルに書き込むには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. 顧客に CVV コードの入力を要求するには、次のように設定します **[!UICONTROL Require CVV Entry]** 対象： `Yes`.

1. ストアの必要に応じて、次の節を完了します。

   - [CVV と AVS の設定](#cvv-and-avs-settings)
   - [決済報告書の設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### CVV と AVS の設定

アドレス検証システムが不一致を識別した場合にトランザクションを拒否するタイミングを決定するには、様々なシナリオの処理方法を指定します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CVV and AVS Settings]** セクション。

   ![CVV と AVS の設定 – PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. 一致しない番地の不一致に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL AVS Street Does Not Match]** 対象： `Yes`.

1. 一致しない郵便番号に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL AVS Zip Does Not Match]** 対象： `Yes`.

1. 一致しない国識別子に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL International AVS Indicator Does Not Match]** 対象： `Yes`.

1. 一致しない CVV コードに基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL International Card Security Code Does Not Match]** 対象： `Yes`.

#### 決済報告書の設定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Settlement Report Settings]** セクション。

   ![決済レポート設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

フロントエンドエクスペリエンス設定を使用すると、サイトに表示する PayPal ロゴを選択したり、PayPal マーチャントページの外観をカスタマイズしたりできます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Frontend Experience Settings]** セクション。

   ![フロントエンドエクスペリエンスの設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### 手順 6:PayPal Express チェックアウトの基本設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Basic Settings - PayPal Express Checkout]** セクション。

   ![高速チェックアウトの基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルの設定 _PayPal_ ストアごとに表示することをお勧めします。

1. 複数の支払方法を提供する場合は、次の番号を入力します **[!UICONTROL Sort Order]** 他の支払い方法と共にリストされた際に、PayPal Express チェックアウトが表示される順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認し、資金を保留します。 金額は確定するまで引き出されません _キャプチャ済み_ 商人によって。
   - `Sale`  – 購入金額が承認され、すぐにお客様のアカウントから引き出されます。

1. を表示するには _[!UICONTROL Check out with PayPal]_ボタンを使用して、次を設定します&#x200B;**[!UICONTROL Display on Product Details Page]**対象： `Yes`.

### 手順 7:PayPal Express チェックアウトの詳細設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

   ![高速チェックアウトの詳細設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Display on Shopping Cart]** 対象： `Yes`.

1. を設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  – 店舗の構成で指定されたすべての国の顧客は、この支払い方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. 支払システムとの通信をログ・ファイルに書き込むには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. PayPal サイトの明細項目別の顧客注文の完全な概要を表示するには、次のように設定します **[!UICONTROL Transfer Cart Line Items]** 対象： `Yes`.

1. お客様が注文レビューのためにストアに戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、次のように設定します **[!UICONTROL Skip Order Review Step]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

### 手順 8:Google reCAPTCHA の追加

PayPal Payflow Pro のチェックアウトをより適切に保護するには、Google reCAPTCHA を有効にします。 クリック可能なインターフェイスまたは非表示のチェックを使用して reCAPTCHA を実行して顧客を検証するオプションが含まれています。 目に見えないオプションは、販売コンバージョンを増やし、ストアを保護することをお勧めします。 詳しくは、を参照してください [Google reCAPTCHA](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
