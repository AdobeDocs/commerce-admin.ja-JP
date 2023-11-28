---
title: PayPal 支払いの詳細
description: PayPal Payments Advanced をオンライン支払いソリューションとしてストアに設定する方法を説明します。
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2155'
ht-degree: 0%

---

# PayPal 支払いの詳細

[PayPal 支払いの詳細][4] は [PCI 準拠](../getting-started/compliance-pci.md) 顧客がサイトを離れることなくデビットまたはクレジットカードで支払うことができるソリューション。 これには組み込みのチェックアウトページが含まれ、シームレスで安全なチェックアウト操作を作成するためにカスタマイズできます。

PayPal アカウントを持たないお客様でも、PayPal セキュアな支払いゲートウェイを通じて購入を行うことができます。 受け入れ可能なカードは、Visa、MasterCard、Switch/Maestro、米国と英国のソロクレジットカードです。 PayPal Express Checkout は、PayPal Payments Advanced に付属しています。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日現在、ヨーロッパの銀行は、満たさない支払いを辞退する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件。 PSD2 に準拠するには、PayPal Payments Advanced をサードパーティのプラグインと統合する必要があります。 詳しくは、 [3-D セキュア（ペイフロー用）](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>PayPal Payments Advanced は、ストアの管理者から作成された注文には使用できません。

## 要件

- [PayPal ビジネスアカウント][1]
- 複数のAdobe CommerceおよびMagento Open Sourceの Web サイトを管理する場合は、Web サイトごとに個別の PayPal マーチャントアカウントが必要です。

## チェックアウトワークフロー

1. **顧客が支払い方法を選択**  — チェックアウト時に、お客様は PayPal Payments Advanced で支払うことを選択します。 [ 発注 ] ボタンの代わりに [ 今すぐ支払 ] ボタンが表示されます。

1. **今すぐ支払う**  — 顧客がクリック/タップした回数 _今すぐ支払う_&#x200B;と入力すると、PayPal がホストするフォームが表示されます。 顧客がカード情報を入力し、カードが検証されます。 成功した場合は、注文確認ページが表示されます。

   **PayPal で支払う**  — フォームには、 _PayPal で支払う_ ボタンをクリックします。PayPal サイトにリダイレクトされ、PayPal Express Checkout で支払いを行うことができます。

1. **トラブルシューティング**  — 何らかの理由でトランザクションが失敗した場合は、エラーメッセージがチェックアウトページに表示され、お客様に再試行するように指示されます。 問題は PayPal で管理されます。

## 注文処理ワークフロー

PayPal の支払いを伴う注文処理の詳細は、通常の PayPal の注文処理と同じです。 注文は、オンラインとオフラインの返金に対して生成された請求と発送、およびクレジットメモです。 ただし、PayPal Payments Advanced で支払われた注文に対しては、複数のオンライン返金は利用できません。

1. **顧客が注文を発行する**  — チェックアウトの最後の段階で、顧客は注文を行うボタンをタップします。

1. **PayPal の応答** - PayPal はリクエストを評価します。 有効であると判断された場合、PayPal はトランザクションを処理します。

1. **コマースは注文ステータスを設定します**  — コマースが PayPal から応答を受け取り、注文ステータスを次のいずれかに設定します。

   - **処理中**  — トランザクションが成功しました。
   - **支払保留中** - PayPal からの応答はありませんでした。
   - **キャンセル**  — 何らかの理由でトランザクションが成功しませんでした
   - **詐欺の疑い**  — トランザクションが一部の [PayPal 不正フィルター](paypal.md#paypal-fraud-management-filters). PayPal から、不正サービスによって確認中のトランザクションに対する応答を受け取ります。

1. **商人が注文を完了する**  — 商人が受注を請求し、出荷します。

## PayPal アカウントを設定する

PayPal Payments Advanced in Commerce を設定する前に、PayPal Web サイトでアカウントを設定する必要があります。

1. にログインします。 [PayPal ビジネスアカウント][2].

1. に移動します。 **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** 次の設定を行います。

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** 設定を指定します。

   >[!NOTE]
   >
   >複数のコマース Web サイトを持っている場合は、それぞれに対して個別の PayPal Payments Advanced アカウントを作成する必要があります。

1. レイアウトを作成するように求められたら、次の操作を行います。

   - ページ上部で、「 **[!UICONTROL Customize]**.

   - 選択 **[!UICONTROL Layout C]**.

   - クリック **[!UICONTROL Save and Publish]**.

1. 別のユーザーを設定する（PayPal で推奨）:

   - にログインします。 [PayPal ビジネスアカウント][2].

   - 別のユーザーを設定するには、指示に従います。

   - **[!UICONTROL Save]** が変更されます。

## コマースでの PayPal 支払いの詳細設定

>[!NOTE]
>
>Express Checkout と、All-In-One または Payment Gateway ソリューションの 2 つの PayPal ソリューションを同時にアクティブにすることができます。 支払い方法を変更すると、以前に使用されていたものは無効になります。

>[!TIP]
>
>クリック **[!UICONTROL Save Config]** いつでも作業内容を保存できます。

### 手順 1：設定の開始

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. コマースインストールに複数の Web サイト、ストア、または表示がある場合は、 **[!UICONTROL Store View]** を、この設定を適用するストア表示に追加します。

1. Adobe Analytics の _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地

   この設定は、設定に表示される PayPal ソリューションの選択を決定します。

   ![商家の国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL PayPal All-in-One Payment Solution]** をクリックします。 **[!UICONTROL Configure]** 対象： **[!UICONTROL Payments Advanced]**.

   ![PayPal 支払いの詳細](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### 手順 2：必要な設定を完了する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Required PayPal Settings]** セクション（必要に応じて）で設定します。

   ![詳細な必須設定 — PayPal 支払い詳細](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. （オプション） **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E メールアドレスでは、大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致している必要があります。

   PayPal アカウントをお持ちでない場合は、 **[!UICONTROL Start accepting payments via PayPal]**.

1. PayPal マーチャントアカウントへのログインに使用する次のいずれかの資格情報を入力します。

   - **[!UICONTROL Partner]** - PayPal パートナー ID。
   - **[!UICONTROL Vendor]** - PayPal ユーザーのログイン名。
   - **[!UICONTROL User]** - PayPal アカウントで設定されている別のユーザーの ID。

1. 次を入力します。 **[!UICONTROL Password]** PayPal アカウントに関連付けられている。

1. テスト取引を実行するには、 **[!UICONTROL Test Mode]** から `Yes`.

   サンドボックスで設定をテストする場合は、次のみを使用します。 [クレジットカード番号][3] PayPal で推奨される情報です。 実稼動に移行する準備が整ったら、設定に戻り、テストモードをに設定します。 `No`.

1. システムがプロキシサーバを使用して PayPal システムへの接続を確立する場合は、 **[!UICONTROL Use Proxy]** から `Yes` 次の操作を実行します。

   - の IP アドレスを入力 **[!UICONTROL Proxy Host]**.

   - ポート番号を入力 **[!UICONTROL Proxy Port]**.

     プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを禁止する場合に使用されます。 この場合、サードパーティサーバーを使用してトラフィックがリレーされます。

1. 設定 **[!UICONTROL Enable this Solution]** から `Yes`.

1. 次の項目を選択します。 [PayPal クレジット](paypal.md#paypal-credit-and-pay-later) を顧客に設定する **[!UICONTROL Enable PayPal Credit]** から `Yes`.

### ステップ 3：広告 PayPal クレジット/広告 PayPal PayLater（オプション）の設定

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能を使用すると、買い物客は購入時に全額を支払う代わりに、隔週の分割払いで注文に対して支払うことができます。 PayPal Credit エクスペリエンスは廃止されました。

設定 **[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに変更します。

- `Yes` - PayPal PayLater を宣伝する
- `No` - PayPal クレジットの宣伝を設定するには

#### PayPal クレジットの宣伝

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advertise PayPal Credit]** 」セクションに入力します。

   ![PayPal クレジットの宣伝](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. アカウント情報を取得するには、 **[!UICONTROL Get Publisher ID from PayPal]** そして指示に従う

1. を入力します。 **[!UICONTROL Publisher ID]**.

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

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

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

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順 4：基本設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Basic Settings - PayPal Payments Advanced]** セクション（必要に応じて）で設定します。

   ![PayPal 支払いの詳細基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. PayPal の支払い詳細をチェックアウト時に識別するには、 **[!UICONTROL Title]**.

   タイトルは、 _デビットまたはクレジットカード_.

1. 複数の支払い方法を提供する場合は、次の項目に数値を入力します： **[!UICONTROL Sort Order]** をクリックして、PayPal Payments Advanced が、チェックアウト時に他の支払い方法と共に表示される場合に表示される順序を決定します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認するが、資金を保留する。 金額は、そのまま取り下げられない _キャプチャ_ 商人が
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

### 手順 5：詳細設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

   ![詳細設定 — PayPal 支払い詳細](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キー (PC) または Command キー (Mac) を押しながら、リスト内の顧客がストアで購入できる国を選択します。

1. 支払いシステムとの通信をログファイルに書き込むには、 **[!UICONTROL Debug Mode]** から `Yes`.

   PayPal Payments Advanced のログファイルは次のとおりです。 `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性を検証するには、次のように設定します。 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. 3 桁の CVV セキュリティ・コードをクレジット・カードの後ろから入力した場合に、 **[!UICONTROL CVV Entry is Editable]** から `Yes`.

1. 顧客に CVV コードの入力を要求するには、 **[!UICONTROL Require CVV Entry]** から `Yes`.

1. 支払の確認を顧客に送信するには、次のように設定します。 **[!UICONTROL Send Email Confirmation]** から `Yes`.

1. トランザクション中に PayPal サーバーと情報を交換する方法を決定するには、 **[!UICONTROL URL method for Cancel URL and Return URL]** を次のいずれかに変更します。

   - `GET` - （デフォルト）プロセスの結果である情報を取得します。
   - `POST`  — フォームに入力されたデータなど、データブロックをデータ処理プロセスに提供します。

   The _URL をキャンセル_ および _戻り先 URL_ は、PayPal サーバー上のチェックアウトプロセスの支払い部分を完了またはキャンセルした後に、顧客が戻るページを参照します。

1. ストアの必要に応じて、次のセクションに入力します。

   - [決済レポート設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### 決済レポート設定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Settlement Report Settings]** 」セクションに入力します。

   ![PayPal 決済レポート設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL SFTP Credentials]**、次の操作を実行します。

   - PayPal のセキュア FTP サーバーに新規登録済みの場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - 運用を開始する前にテストレポートを実行するには、 **[!UICONTROL Sandbox Mode]** から `Yes`.

   - 次を入力します。 **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     デフォルトでは、値は `reports.paypal.com`.

   - 次を入力します。 **[!UICONTROL Custom Path]** レポートが保存される場所。

     デフォルトでは、値は `/ppreports/outgoing`.

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

以下を使用します。 _[!UICONTROL Frontend Experience Settings]_サイトに表示する PayPal ロゴを選択し、PayPal マーチャントページの外観をカスタマイズします。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Frontend Experience Settings]** 」セクションに入力します。

   ![PayPal フロントエンドエクスペリエンス設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

1. を選択します。 **[!UICONTROL PayPal Product Logo]** ストアの PayPal ブロックに表示する

   PayPal ロゴは、4 つのスタイルと 2 つのサイズで使用できます。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal マーチャントページの外観をカスタマイズするには、次の手順を実行します。

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

### ステップ 6:PayPal Express チェックアウトの基本設定を完了する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Basic Settings - PayPal Express Checkout]** 」セクションに入力します。

   ![PayPal Express チェックアウトの基本設定](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルをに設定します。 _PayPal_ 各ストア表示に対して、をお勧めします。

1. 複数の支払い方法を提供する場合は、次の項目に数値を入力します： **[!UICONTROL Sort Order]** PayPal Express Checkout が他の支払い方法と共にリストされた際に表示される順序を決定する。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認し、資金を保留する。 金額は、そのまま取り下げられない _キャプチャ_ 商人が
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. 次の手順で _[!UICONTROL Check out with PayPal]_製品ページのボタンをクリックし、**[!UICONTROL Display on Product Details Page]**から `Yes`.

### ステップ 7：詳細設定 — PayPal Express チェックアウト

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

   ![PayPal Express チェックアウトの詳細設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. PayPal Express チェックアウトを買い物かごとミニカートの両方から利用できるようにするには、 **[!UICONTROL Display on Shopping Cart]** から `Yes`.

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries` |このオプションを選択した後、 _特定の国からの支払いリスト_ が表示されます。 Ctrl キー (PC) または Command キー (Mac) を押しながら、リスト内の各国をクリックします。顧客はストアから買い物をすることができます。

1. 支払いシステムとの通信をログファイルに書き込むには、 **[!UICONTROL Debug Mode]** から `Yes`.

   >[!NOTE]
   >
   >次に従って： [PCI データセキュリティ標準](../getting-started/compliance-pci.md)の場合、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性を検証するには、次のように設定します。 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. 顧客の注文の完全な概要を PayPal サイトの行項目別に表示するには、 **[!UICONTROL Transfer Cart Line Items]** から `Yes`.

1. 顧客が注文確認のためにストアに戻ることなく PayPal サイトからトランザクションを完了できるようにするには、 **[!UICONTROL Skip Order Review Step]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
