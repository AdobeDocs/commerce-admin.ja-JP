---
title: PayPal ペイメントプロ
description: ストアでオンライン支払いソリューションとして PayPal Payments Pro を設定する方法を説明します。
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2240'
ht-degree: 0%

---

# PayPal ペイメントプロ

[PayPal ペイメントプロ][3] マーチャントアカウントと支払いゲートウェイのすべての利点に加えて、独自の完全にカスタマイズされたチェックアウトエクスペリエンスを作成する機能をもたらします。 PayPal Express Checkout は PayPal Payments Pro で自動的に有効化されるため、1 億 1,000 万人以上のアクティブな PayPal ユーザーを利用できます。

![PayPal Payments Pro がミニカートに表示されます](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日の時点で、ヨーロッパの銀行は満たされていない支払いを拒否する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件 PSD2 に準拠するには、PayPal Payments Pro をサードパーティのプラグインと統合する必要があります。

>[!NOTE]
>
>現在、PayPal Payments Pro は米国、英国、カナダで利用できます。

## 要件

- [PayPal マーチャントアカウント][1] （直接支払が有効化されている場合）

## チェックアウトワークフロー

1. **顧客がチェックアウトに移動**  – 顧客が買い物かごに製品を追加し、クリックやタップをおこなう _チェックアウトに進む_.|
1. **顧客が支払方法を選択します** - チェックアウト時に、顧客はを選択します _PayPal 直接支払い_ オプションを選択し、クレジットカード情報を入力します。
   - PayPal Payments Pro で支払う場合、お客様はチェックアウトプロセス中にサイトに滞在します。
   - PayPal Express Checkout で支払う場合、お客様は取引を完了するために PayPal サイトにリダイレクトされます。

顧客の要求に応じて、店舗管理者は管理者からの注文を作成し、PayPal Payments Pro でトランザクションを処理することもできます。

## 注文処理ワークフロー

1. **注文**  – 注文は、ストアの管理者または PayPal マーチャントアカウントから処理できます。

1. **[!UICONTROL Payment Action]**  – 設定で指定された支払いアクションが注文に適用されます。 次のようなオプションがあります。

   - **を承認する** - Commerceがを使用して注文を作成する _処理_ ステータス。 この場合において、認可を受けるべき金額については、承認保留中とする。
   - **販売** - Commerceによって、受注と請求書の両方が作成されます。
   - **キャプチャ** - PayPal は、注文金額を顧客残高、銀行口座、またはクレジットカードからマーチャントアカウントに転送します。

1. **請求** - PayPal がCommerceに即時支払い通知メッセージを送信した後、請求書がCommerceで作成される。

   PayPal マーチャントアカウントで即時支払い通知が有効になっていることを確認します。

   >[!NOTE]
   >
   >必要に応じて、指定された数量の製品に対して注文の一部を請求できます。 送信された部分請求書ごとに、一意の ID を持つ個別の取得取引が使用可能になり、個別の請求書が生成されます。

   承認のみの支払トランザクションは、注文金額が完全にキャプチャされた後にのみクローズされます。

   注文金額が完全に請求されるまで、オンラインでいつでも注文を無効にできます。

1. **戻り値**  – お客様が購入した商品を返品し、返金を請求する場合、注文金額のキャプチャや請求書の作成と同様に、管理者または PayPal マーチャントアカウントからオンライン返金を作成できます。

## PayPal アカウントの設定

Commerceで PayPal Payments Pro を設定する前に、PayPal Web サイトでマーチャントアカウントを設定する必要があります。

1. にログイン [PayPal ビジネスアカウント](https://manager.paypal.com/).

1. PayPal Manager メニューで、 **[!UICONTROL Service Settings]**.

1. 次の下 **[!UICONTROL Hosted Checkout Pages]**&#x200B;を選択し、 **[!UICONTROL Set Up]**.

1. 次の下 **[!UICONTROL Choose your settings]**、設定 **[!UICONTROL Transaction Process Mode]** 対象： `Live`.

1. 次の下 **[!UICONTROL Display options on payment page]**、設定 **[!UICONTROL Cancel URL Method]** 対象： `POST`.

1. 次の下 **[!UICONTROL Billing Information]**&#x200B;で、カードセキュリティコードを選択します **[!UICONTROL CSC]** 必須フィールドと編集可能フィールドの両方のチェックボックス。

1. 次の下 **[!UICONTROL Payment Confirmation]**、設定 **[!UICONTROL Return URL Method]** 対象： `POST`.

1. 次の下 **[!UICONTROL Security Options]**、以下を設定します。

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. クリック **[!UICONTROL Save Changes]**.

1. が含まれる _PayPal マネージャー_ メニュー、を選択 **[!UICONTROL Service Settings]** との下 _ホストされたチェックアウトページ_、を選択 **[!UICONTROL Customize]**.

1. を選択 **[!UICONTROL Layout C]**.

   レイアウト C では、クレジットカードとデビットカードのフィールドのみが表示され、サイトにフレームを組み込んだり、スタンドアロンポップアップとして使用したりできます。 サイズは 490 x 565 ピクセルで固定され、エラーメッセージ用のスペースも追加されます。 一部のシステムでは、この設定によりトランスペアレント リダイレクトの問題が修正されます。

1. クリック **[!UICONTROL Save and Publish]**.

1. PayPal Manager メニューで、 **[!UICONTROL Account Administration]**. 次の下 **[!UICONTROL Manage Security]**&#x200B;を選択し、 **[!UICONTROL Transaction Settings]**.

1. を設定 **[!UICONTROL Allow reference transactions]** 対象： `Yes`.

1. クリック **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >複数のCommerce Web サイトがある場合は、それぞれに個別の PayPal Payments Pro アカウントを作成する必要があります。

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

## Commerceでの PayPal Payments Pro の設定

>[!NOTE]
>
>2 つの PayPal ソリューションを同時にアクティブにすることができます。 [PayPal Express チェックアウト](paypal-express-checkout.md)、およびいずれかの [オールインワンソリューション](paypal.md#paypal-all-in-one-payment-solutions). 支払いソリューションを変更すると、以前に使用したソリューションが自動的に無効になります。

>[!TIP]
>
>クリック **[!UICONTROL Save Config]** 進行状況を保存する時間を指定できます。

### 手順 1：設定の開始

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Payment Methods]**.

1. Commerceのインストールに複数の web サイト、ストアまたはビューがある場合は、を設定します **[!UICONTROL Store View]** この設定を適用するストア表示に移動します。

1. が含まれる _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地。

   この設定により、設定に表示される PayPal ソリューションの選択が決まります。

   ![商社国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. を展開 **[!UICONTROL PayPal All-in-One Payment Solution]** をクリックして、 **[!UICONTROL Configure]** （用） **[!UICONTROL Payments Pro]**.

   ![PayPal ペイメントプロ](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### 手順 2：必要な PayPal 設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Payments Pro and Express Checkout]** セクション。

   ![PayPal Payments Pro の必須設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. （任意） **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >メールアドレスでは大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致する必要があります。

   PayPal アカウントをお持ちでない場合は、 **[!UICONTROL Start accepting payments via PayPal]**.

1. PayPal マーチャントアカウントへのログインに使用する次の資格情報のいずれかを入力します。

   - **[!UICONTROL Partner]** - PayPal パートナー ID。
   - **[!UICONTROL Vendor]** - PayPal ユーザーログイン名。
   - **[!UICONTROL User]** - PayPal アカウントで設定されている別のユーザーの ID。

1. を入力 **[!UICONTROL Password]** これは PayPal アカウントに関連付けられています。

1. テストトランザクションを実行するには、次を設定します **[!UICONTROL Test Mode]** 対象： `Yes`.

   サンドボックスで設定をテストする場合は、のみを使用します [クレジットカード番号][2] それは PayPal で推奨されています。 実稼動に移行する準備ができたら、設定に戻ってテストモードをに設定します。 `No`.

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順 4：基本設定を完了する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Basic Settings - PayPal Payments Pro]** セクション。

   ![PayPal Payment Pro の基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**&#x200B;を入力し、チェックアウト時に PayPal Payments Pro を識別するタイトルを入力します。

   タイトルを使用することをお勧めします _デビットまたはクレジットカード_.

1. 複数の支払方法を提供する場合は、次の番号を入力します **[!UICONTROL Sort Order]** チェックアウト時に他の支払い方法と一緒にリストされたときに PayPal Payments Pro が表示される順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` =最初、 `1` =秒、 `2` = 3 番目、など）。

1. を設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization`  – 購入を承認しますが、資金を保留します。 金額は確定するまで引き出されません _キャプチャ済み_ 商人によって。
   - `Sale`  – 購入金額が承認され、即座に顧客アカウントから引き出されます。

1. の場合 **[!UICONTROL Credit Card Settings]**&#x200B;で、ストアでのお支払いに使用できるクレジットカードを選択します。

   複数のカードを選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、それぞれのカードをクリックします。

   >[!NOTE]
   >
   >American Express は追加契約が必要です。

### 手順 5：詳細設定の完了

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Advanced Settings]** セクション。

   ![PayPal Payments Pro の詳細設定](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー（PC）または Command キー（Mac）を押しながら、リスト内で、お客様がストアから購入できる国を選択します。

1. 支払システムとの通信をログ・ファイルに書き込むには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. 顧客に CVV コードの入力を要求するには、次のように設定します **[!UICONTROL Require CVV Entry]** 対象： `Yes`.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL CVV and AVS Settings]** セクション。

1. アドレス検証システムが不一致を識別したときにトランザクションを拒否するタイミングを決定するには、次の各シナリオの処理方法を指定します。

   - 一致しない番地の不一致に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL AVS Street Does Not Match]** 対象： `Yes`.

   - 一致しない郵便番号に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL AVS Zip Does Not Match]** 対象： `Yes`.

   - 一致しない国識別子に基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL International AVS Indicator Does Not Match]** 対象： `Yes`.

   - 一致しない CVV コードに基づいてトランザクションを拒否するには、次のように設定します **[!UICONTROL International Card Security Code Does Not Match]** 対象： `Yes`.

   ![PayPal Payments Pro 必須設定 – CVV および AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. ストアの必要に応じて、次の節を完了します。

   - [決済報告書の設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### 決済報告書の設定

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Settlement Report Settings]** セクション。

   ![PayPal 決済レポートの設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL SFTP Credentials]**、次の手順を実行します。

   - PayPal のセキュア FTP サーバーに新規登録している場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - サイトで Payments Pro を使用して運用を開始する前にテストレポートを実行するには、次のように設定します **[!UICONTROL Sandbox Mode]** 対象： `Yes`.

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

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたお支払方法を使用できます。
   - `Specific Countries`  – このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. 支払システムとの通信をログ・ファイルに書き込むには、次のように設定します **[!UICONTROL Debug Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、を設定します **[!UICONTROL Enable SSL Verification]** 対象： `Yes`.

1. PayPal サイトの明細項目別の顧客注文の完全な概要を表示するには、次のように設定します **[!UICONTROL Transfer Cart Line Items]** 対象： `Yes`.

1. お客様が注文レビューのためにストアに戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、次のように設定します **[!UICONTROL Skip Order Review Step]** 対象： `Yes`.

1. 完了したら、 **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
