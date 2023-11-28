---
title: PayPal ペイフローリンク
description: PayPal Payflow Link をお客様のストアでオンライン支払いソリューションとして設定する方法を説明します。
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# PayPal ペイフローリンク

PayPal Payflow リンクは、米国およびカナダの商人に対してのみ利用できます。 お客様は、個人の PayPal アカウントを持っている必要はありません。また、PayPal がホストするフォームにクレジットカード情報を入力する必要もありません。 情報は、Adobe CommerceまたはMagento Open Sourceサーバーには保存されません。 ペイフローリンクは、管理者から作成された注文には使用できません。

クレジットメモは、オンラインとオフラインの両方の払い戻しに対してサポートされています。 ただし、複数のオンライン返金はサポートされていません。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日現在、ヨーロッパの銀行は、満たさない支払いを辞退する可能性があります [PSD2](../getting-started/compliance-payment-services-directive.md) 要件。 PSD2 に準拠するには、PayPal Payflow Link を Cardinal Commerce と統合する必要があります。 詳しくは、 [3-D セキュア（ペイフロー用）](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## 要件

- [PayPal ビジネスアカウント][1] PayPal Payflow Pro ゲートウェイは、PayPal のマーチャントアカウントとマーチャントウェブサイトとをリンクし、ゲートウェイとマーチャントアカウントの両方の役割を果たします。

- 複数のコマース Web サイトを管理する場合は、Web サイトごとに個別の PayPal マーチャントアカウントが必要です。

## 顧客ワークフロー

1. **顧客がチェックアウトに移動**  — チェックアウト時に、顧客は PayPal Payflow リンクを使用して支払いを選択し、クレジットカード情報を入力します。 お客様は、個人の PayPal アカウントを持つ必要はありません。
1. **お客様が今すぐ支払う**  — 顧客が「Pay Now」ボタンをタップして注文を送信します。
1. **顧客がクレジットカード情報を入力**  — 顧客が、PayPal がホストするフォームにクレジットカード情報を入力します。 顧客が _支払いのキャンセル_ リンクをクリックすると、顧客はチェックアウトの支払情報ステージに戻り、注文ステータスは次のように変わります。 _キャンセル_.
1. **顧客が注文を送信**  — クレジットカード情報は PayPal に直接送信され、コマースサイトのどこにも保持されません。

## 注文ワークフロー

1. **PayPal がリクエストを受信** - PayPal は、お客様から Pay Now へのリクエストを受け取ります。
1. **PayPal が支払情報を検証します** - PayPal は、クレジットカード情報を検証し、適切なステータスを割り当てます。
   - **支払い確認済み：** 検証された場合、 _支払保留中_ ステータスは、トランザクションが決済されるまで、最初に注文に割り当てられます。
   - **処理中**  — トランザクションが成功しました。
   - **支払保留中** - PayPal からの応答がシステムに送信されなかった。
   - **キャンセル**  — 何らかの理由でトランザクションが成功しなかった。
   - **詐欺の疑い**  — トランザクションが一部の [PayPal 不正フィルター](paypal.md#paypal-fraud-management-filters). PayPal から、不正サービスによって確認中のトランザクションに対する応答を受け取ります。
   - **支払いのキャンセル：** 顧客が _支払いのキャンセル_ リンクをクリックすると、顧客はチェックアウトの支払情報ステージに戻り、注文ステータスは次のように変わります。 _キャンセル_.
1. **顧客が確認ページにリダイレクトされる**   — トランザクションが正常に完了すると、顧客はストアの注文確認ページにリダイレクトされます。 何らかの理由でトランザクションが失敗した場合は、エラーメッセージがチェックアウトページに表示され、顧客はチェックアウトプロセスを繰り返すように指示されます。 これらの状況は PayPal で管理されます。
1. **商人が注文を完了する** ・商人が通常どおりに請求書を発行し、発注を出荷します。

## PayPal アカウントを設定する

1. にログインします。 [PayPal ビジネスアカウント][2].

1. を設定します。 [ホストされるチェックアウトページ][4] 以下の設定で PayPal Manager を使用します。

   - の下 **[!UICONTROL Security Options]**、次の設定を実行します。

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - 選択 **[!UICONTROL Customize]**&#x200B;を選択し、次を選択します。 **[!UICONTROL Layout C]**.

     レイアウト C はクレジットカードとデビットカードのフィールドのみを表示し、サイト上に枠付けしたり、スタンドアロンのポップアップとして使用したりできます。 サイズは 490 x 565 ピクセルで固定され、エラーメッセージ用の余分なスペースがあります。 一部のシステムでは、この設定により、透過的なリダイレクトの問題が修正されます。

1. 設定が完了したら、 **[!UICONTROL Save and Publish]**.

1. 追加のユーザーを設定します（PayPal で推奨）。

   - メインメニューの 2 行目で、 **[!UICONTROL Manage Users]**.

   - 別のユーザーをアカウントに追加するには、 **[!UICONTROL Add User]**.

   - 次のセクションの必須フィールドに入力します。 _ユーザーを追加_ フォーム：

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - クリック **[!UICONTROL Update]**.

## PayPal ペイフローリンクの設定

>[!TIP]
>
>クリック **[!UICONTROL Save Config]** いつでも作業内容を保存できます。

### 手順 1：設定の開始

この設定方法は、既存の PayPal アカウントを持っていることを前提としています。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Payment Methods]**.

1. コマースインストールに複数の Web サイト、ストア、または表示がある場合は、 **[!UICONTROL Store View]** を、この設定を適用するストア表示に追加します。

1. Adobe Analytics の _[!UICONTROL Merchant Location]_セクションで、**[!UICONTROL Merchant Country]**ビジネスの所在地

   この設定は、設定に表示される PayPal ソリューションの選択を決定します。

   ![商家の国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 展開 **[!UICONTROL PayPal Payment Gateways]** （必要に応じて）をクリックし、 **[!UICONTROL Configure]** 対象： **[!UICONTROL Payflow Link]**.

   ![ペイフローリンク — 設定](./assets/payflow-link.png){width="600" zoomable="yes"}

### 手順 2：必要な PayPal 設定を完了する

![PayPal 設定が必要 — PayPal Payflow リンク](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. （オプション） **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >E メールアドレスでは、大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致している必要があります。

1. PayPal マーチャントアカウントへのログインに使用する次のいずれかの資格情報を入力します。

   - **[!UICONTROL Partner]** - PayPal パートナー ID。
   - **[!UICONTROL User]** - PayPal アカウントで設定されている別のユーザーの ID。
   - **[!UICONTROL Vendor]** - PayPal ユーザーのログイン名。

1. 次を入力します。 **[!UICONTROL Password]** PayPal アカウントに関連付けられている。

1. テスト取引を実行するには、 **[!UICONTROL Test Mode]** から `Yes`.

   サンドボックスで設定をテストする場合は、次のみを使用します。 [クレジットカード番号][3] PayPal で推奨される情報です。 実稼動に移行する準備が整ったら、設定に戻り、テストモードをに設定します。 `No`.

1. システムがプロキシサーバを使用して PayPal システムへの接続を確立する場合は、 **[!UICONTROL Test Mode]** から `Yes` 次の操作を実行します。

   - の IP アドレスを入力 **[!UICONTROL Proxy Host]**.

   - ポート番号を入力 **[!UICONTROL Proxy Port]**.

     プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを禁止する場合に使用されます。 その場合、トラフィックの中継にサードパーティサーバーが使用されます。

1. 設定 **[!UICONTROL Enable Payflow Link]** から `Yes`.

1. を有効にする場合 [PayPal Express チェックアウト](paypal-express-checkout.md) 顧客のオプション、設定 **[!UICONTROL Enable Express Checkout]** から `Yes`.

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

   ![広告 PayPal クレジットホームページ設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 残りのセクションで、ホームページの設定に関して前の手順を繰り返します。

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### 広告 PayPal PayLater

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advertise PayPal PayLater]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enable PayPal PayLater]** から `Yes`.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Home Page]** 」セクションに入力します。

   ![広告 PayPal クレジットホームページ設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) 残りのセクションと、前の手順を繰り返します。

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順 4：基本設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Basic Settings - PayPal Payflow Link]** 」セクションに入力します。

   ![基本設定 — PayPal Payflow リンク](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時に PayPal Payflow リンクを識別するタイトルを入力します。

   タイトルは、 _デビットまたはクレジットカード_.

1. 複数の支払い方法を提供する場合は、次の項目に数値を入力します： **[!UICONTROL Sort Order]** 他の支払方法とともにリストされた場合に、Payflow リンクが表示される順序を決定します。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認し、資金を保留する。 金額は、商人が取り込むまで引き落とされません。
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

### 手順 5：詳細設定の完了

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

   ![詳細設定 — PayPal ペイフローリンク](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 Ctrl キーを押しながら、リスト内の各国を選択します。この国では、顧客がストアで買い物をすることができます。

1. 支払いシステムとの通信をログファイルに書き込むには、 **[!UICONTROL Debug Mode]** から `Yes`.

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性を検証するには、次のように設定します。 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. 3 桁の CVV セキュリティ・コードをクレジット・カードの後ろから入力した場合は、 **[!UICONTROL CVV Entry is Editable]** から `Yes`.

1. 顧客に CVV コードの入力を要求するには、 **[!UICONTROL Require CVV Entry]** から `Yes`.

1. 支払の確認を顧客に送信するには、次のように設定します。 **[!UICONTROL Send Email Confirmation]** から `Yes`.

1. トランザクション中に PayPal サーバーと情報を交換する方法を決定するには、 **[!UICONTROL URL method for Cancel URL and Return URL]** を次のいずれかに変更します。

   - `GET`  — プロセスの結果である情報を取得します（デフォルトのメソッド）。
   - `POST`  — フォームに入力されたデータなど、データブロックをデータ処理プロセスに提供します。

   The _URL をキャンセル_ および _戻り先 URL_ PayPal サーバー上のチェックアウトプロセスの支払い部分を完了またはキャンセルした後に、顧客が戻ってくるページを参照します。

1. ストアの必要に応じて、次のセクションに入力します。

   - [決済レポート設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### 決済レポート設定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Settlement Report Settings]** 」セクションに入力します。

   ![決済レポート設定 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL SFTP Credentials]**、次の操作を実行します。

   - PayPal セキュア FTP サーバーに新規登録している場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - サイト上で高速チェックアウトを使用して運用を開始する前にテストレポートを実行するには、 **[!UICONTROL Sandbox Mode]** から `Yes`.

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

   ![フロントエンドエクスペリエンス設定 — PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### ステップ 6: PayPal Express Checkout の基本設定を完了する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Basic Settings - PayPal Express Checkout]** 」セクションに入力します。

   ![基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. の場合 **[!UICONTROL Title]**、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   タイトルをに設定します。 _PayPal_ 各ストア表示に対して、をお勧めします。

1. 複数の支払い方法を提供する場合は、次の項目に数値を入力します： **[!UICONTROL Sort Order]** PayPal Express Checkout が他の支払い方法と共にリストされた際に表示される順序を決定する。

   この数は他の支払い方法に対する相対値です。 (`0` =最初 `1` =秒 `2` = 3 番目、など )

1. 設定 **[!UICONTROL Payment Action]** を次のいずれかに変更します。

   - `Authorization` ・買い付けを承認し、資金を保留する。 金額は、そのまま取り下げられない _キャプチャ_ 商人が
   - `Sale`  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。

1. 次の手順で _[!UICONTROL Check out with PayPal]_製品ページのボタンをクリックし、**[!UICONTROL Display on Product Details Page]**から `Yes`.

### ステップ 7: PayPal Express チェックアウトの詳細設定を完了する

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Advanced Settings]** 」セクションに入力します。

   ![詳細設定](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Display on Shopping Cart]** から `Yes`.

1. 設定 **[!UICONTROL Payment Applicable From]** を次のいずれかに変更します。

   - `All Allowed Countries`  — ストア設定で指定されたすべての国のお客様は、この支払い方法を使用できます。
   - `Specific Countries`  — このオプションを選択した後、 _[!UICONTROL Payment from Specific Countries]_リストが表示されます。 複数の国を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各項目をクリックします。

1. 支払いシステムとの通信をログファイルに書き込むには、 **[!UICONTROL Debug Mode]** から `Yes`.

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性を検証するには、次のように設定します。 **[!UICONTROL Enable SSL Verification]** から `Yes`.

1. PayPal サイトから顧客の注文の完全な概要を行項目別に表示するには、 **[!UICONTROL Transfer Cart Line Items]** から `Yes`.

1. 顧客が注文確認のためにストアに戻ることなく PayPal サイトからトランザクションを完了できるようにするには、 **[!UICONTROL Skip Order Review Step]** から `Yes`.

1. 完了したら、「 **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
