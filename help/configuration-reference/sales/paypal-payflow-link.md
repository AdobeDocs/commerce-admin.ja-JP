---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]'
description: Commerce管理者の[!UICONTROL Sales] > [!UICONTROL Payment Methods] ページの[!UICONTROL PayPal Payflow Link] セクションの設定を確認します。
exl-id: 5ea30b22-e251-4d93-be2c-d34138ef2f7d
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]

>[!IMPORTANT]
>
>**PSD2の要件：** <br/>
>2019年9月14日現在、ヨーロッパの銀行は[PSD2](../../getting-started/compliance-payment-services-directive.md)の要件を満たさない支払いを拒否する可能性があります。 PSD2に準拠するには、[!DNL PayPal Payflow Link]を[!DNL Cardinal Commerce]と統合する必要があります。 詳しくは、「[3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/)」を参照してください。

{{config}}

## [!UICONTROL Required Settings]

![必要な設定](./assets/paypal-payflow-link-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | web サイト | （オプション） PayPal加盟店アカウントに関連付けられているメールアドレス。 メールアドレスでは大文字と小文字が区別されるため、アカウント内のアドレスと完全に一致する必要があります。 |
| [!UICONTROL Partner] | web サイト | PayPal パートナーID （該当する場合）。 |
| [!UICONTROL Vendor] | web サイト | PayPal ユーザーログイン名。 |
| ユーザー | web サイト | PayPal アカウントの追加ユーザーのID。 ネットワークに他のユーザーがいない場合は、ベンダーまたは加盟店IDを入力します。 |
| [!UICONTROL Password] | web サイト | PayPal加盟店アカウントに関連付けられているパスワード。 |
| [!UICONTROL Test Mode] | web サイト | 有効にすると、テスト環境でPayPal Payflow Proを実行します。 実稼動モードで「本番稼動」する準備ができたら、テストモードをオフにします。 オプション：`Yes` / `No` |
| [!UICONTROL Use Proxy] | web サイト | プロキシは、サーバーファイアウォールがPayPal サーバーへの直接アクセスを妨げる場合に、トラフィックをリダイレクトするために使用できます。 該当する場合は、PayPal サーバーとの接続を確立するために使用されるプロキシサーバーを識別します。 オプション：`Yes` / `No` <br/><br/>有効な場合、プロキシオプションを設定します：<br/>**`Proxy Host`**- プロキシホストのIP アドレス。<br/>**`Proxy Port`** - プロキシ ポートの番号。 |
| [!UICONTROL Enable Payflow Link] | web サイト | PayPal Payflow Linkがお客様の支払い方法として利用可能かどうかを判断します。 |
| [!UICONTROL Enable Express Checkout] | web サイト | PayPal Express Checkoutがお客様の支払い方法として利用可能かどうかを判断します。 |
| [!UICONTROL Enable PayPal Credit] | web サイト | PayPal クレジットがお客様の支払いオプションとして利用可能かどうかを決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![PayPal クレジットの広告](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | web サイト | PayPal クレジット アカウントに関連付けられている発行者ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPalからパブリッシャーIDを取得します。 |
| [!UICONTROL Home Page] | web サイト | ホームページ上の[!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：<br/>**`Display`**- ストアのホームページに[!DNL PayPal Credit] バナーが表示されるかどうかを指定します。 オプション：`Yes` / `No`<br/>**`Position`** - ホームページ上の[!DNL PayPal Credit] バナーの位置を決定します。 オプション：ヘッダー（中央） / サイドバー（右） <br/>**`Size`**- ホームページの[!DNL PayPal Credit] バナーのサイズを決定します。 オプション：`190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | web サイト | カテゴリーページ上の[!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page]と同じ） |
| [!UICONTROL Catalog Product Page] | web サイト | 商品ページ上の[!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page]と同じ） |
| [!UICONTROL Checkout Cart Page] | web サイト | 買い物かごページの[!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page]と同じ） |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings]

![基本設定](./assets/payment-methods-paypal-payflow-link-basic-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストアビュー | チェックアウト時の支払い方法としてPayPal Payflow Linkを識別する名前。 |
| [!UICONTROL Sort Order] | ストアビュー | チェックアウト時に他の支払い方法と共に表示されるPayPal Payflow Linkの表示順序を決定する番号。 |
| [!UICONTROL Payment Action] | web サイト | 注文の送信時にPayPalが実行するアクションを指定します。 オプション：<br/>**`Authorization`**– 購入を承認しますが、ファンドを保留します。 金額は、加盟店が「獲得」するまで引き落とされません。<br/>**`Sale`** – 購入金額が承認され、お客様のアカウントから直ちに引き落とされます。 |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

![詳細設定](./assets/payment-methods-paypal-payflow-link-advanced-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | web サイト | 該当する国の選択範囲を指定します。 オプション：すべての許可された国/特定の国 |
| [!UICONTROL Countries Payment Applicable From] | web サイト | 支払いが受け入れられる各国を示します。 この支払い方法で購入できるのは、選択した国の請求先住所を持つ顧客のみです。 |
| [!UICONTROL Debug Mode] | web サイト | ストアと支払いシステムの間で送信されたメッセージをログファイルに記録します。 オプション：`Yes` / `No` <br/><br/>**_Note:_** ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従い、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | web サイト | トランザクションが発生する前に、ホスト上のセキュアチャネルが検証されるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | web サイト | 顧客がCVVを入力した後で編集できるかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL Require CVV Entry] | web サイト | 顧客がクレジットカードの裏面からCVV コードを入力する必要があるかどうかを判断します。 オプション：`Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | web サイト | お客様が支払いの確認メールを受信するかどうかを指定します。 オプション：`Yes` / `No` |
| [!UICONTROL URL Method for Cancel  URL and Return URL] | web サイト | トランザクション中にPayPal サーバーと情報を交換するために使用される方法を指定します。 オプション：<br/>**`GET`**- プロセスの結果である情報を取得します。 （これは既定の方法です。）<br/>**`POST`** - フォームに入力されたデータなどのデータ ブロックをデータ処理プロセスに送信します。 |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![決済レポート設定](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | web サイト | PayPalのセキュア FTP サーバーにログインするために必要なユーザー名。 |
| [!UICONTROL Password] | web サイト | PayPalのセキュア FTP サーバーにログインするために必要なパスワード。 |
| [!UICONTROL Sandbox Mode] | web サイト | 有効にすると、実稼動環境で「本番稼動中」になる前に、テスト環境でレポートを実行します。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | web サイト | 決済レポートが管理されるURL。 デフォルト値：`reports.paypal.com` |
| [!UICONTROL Custom Path] | web サイト | 決済レポートがサーバーに保存されるパス。 デフォルト値：`/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | web サイト | 有効にすると、スケジュール時に決済レポートが自動的に取得されます。 オプション：`Yes` / `No` |
| [!UICONTROL Schedule] | グローバル | PayPalが決済レポートを生成する頻度を指定します。 オプション：`Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | グローバル | 決済レポートが生成される時間、分、秒を指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![ フロントエンドエクスペリエンス設定](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | ストアビュー | ストアに表示されるPayPal ロゴを決定します。 2つのサイズに4つの基本スタイルがあります。 オプション：`No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| PayPal加盟店ページのスタイル |  |  |
| [!UICONTROL Page Style] | ストアビュー | PayPal マーチャントページの外観を決定します。 許可される値：<br/>**`paypal`**- PayPal ページスタイルを使用します。<br/>**`primary`** - アカウントプロファイルで「プライマリ」スタイルとして識別したページスタイルを使用します。<br/>**`your_custom_value`**- アカウントプロファイルで指定されたカスタム支払いページスタイルを使用します。 |
| [!UICONTROL Header Image URL] | ストアビュー | チェックアウトページの左上隅に表示される画像のURL。 最大サイズは750 x 90 ピクセルです。 <br/><br/>**_Note:_** PayPalでは、画像を安全な（https）サーバーに保存することをお勧めします。 それ以外の場合、お客様のブラウザーは「ページに安全な項目と安全でない項目の両方が含まれています」と警告する場合があります。 |
| [!UICONTROL Header Image Background Color] | ストアビュー | チェックアウトページのヘッダーの背景色の6文字の[16進数カラー](https://en.wikipedia.org/wiki/Web_colors) コード。 コードは、大文字と小文字のどちらでも入力できます。 |
| [!UICONTROL Header Image Border Color] | ストアビュー | ヘッダーの周囲の2 ピクセル境界の6文字の16進数カラーコード。 |
| [!UICONTROL Page Background Color] | ストアビュー | ヘッダーと支払いフォームの背後に表示されるチェックアウトページの背景色の6文字の16進数カラーコード。 |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express チェックアウトの基本設定](./assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストアビュー | チェックアウト時のPayPal Express チェックアウト支払い方法を識別する名前。 |
| [!UICONTROL Sort Order] | ストアビュー | チェックアウト時に他の支払い方法と一緒に表示されるPayPal Express Checkoutの表示順序を決定する番号。 リストの先頭に`0`と入力します。 |
| [!UICONTROL Payment Action] | web サイト | PayPalが注文を受け取ったときに実行されるアクションを決定します。 オプション：<br/>**`Authorization`**– 購入を承認しますが、ファンドを保留します。 金額は、加盟店が「獲得」するまで引き落とされません。<br/>**`Sale`** – 購入金額が承認され、お客様のアカウントから直ちに引き落とされます。<br/>**`Order`**– 定義された期間内に、加盟店が顧客の購入者アカウントから注文された合計までの1つ以上の金額を取得できるようにするPayPalとの契約を表します。 最大29日間です。 資金を取得するには、Commerce管理者から1つ以上の請求書を生成する必要があります。 |
| [!UICONTROL URL Display on Product Details Page] | ストアビュー | 「PayPalでのチェックアウト」ボタンが製品ページに表示されるかどうかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings - PayPal Express Checkout]

![詳細設定](./assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | ストアビュー | PayPal Express Checkoutをショッピングカートに支払いオプションとして表示するかどうかを指定します。 オプション：はい（推奨）/いいえ |
| [!UICONTROL Payment Action Applicable From] | web サイト | 該当する国の選択範囲を指定します。 オプション：すべての許可された国/特定の国 |
| [!UICONTROL Countries Payment Applicable From] | web サイト | 支払いが受け入れられる各国を示します。 この支払い方法で購入できるのは、選択した国の請求先住所を持つ顧客のみです。 |
| [!UICONTROL Debug Mode] | web サイト | ストアとPayPal支払いシステムの間で送信されたメッセージをログファイルに記録します。 オプション：`Yes` / `No` <br/><br/>**_Note:_** ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従い、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | web サイト | ホストのセキュリティ証明書の検証を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | web サイト | PayPal サイトで顧客のショッピングカートから行アイテムの完全な概要を表示します。 オプション：`Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | web サイト | お客様がPayPal サイトからトランザクションを完了できるか、または店舗に戻って注文を送信する前に注文レビュー手順を完了する必要があるかを指定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}
