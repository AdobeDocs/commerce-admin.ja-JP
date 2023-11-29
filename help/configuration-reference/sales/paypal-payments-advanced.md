---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Advanced]'
description: 設定を確認するには、 [!UICONTROL PayPal Payments Advanced] のセクション [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] コマース管理のページ。
exl-id: c9159408-fbdf-4146-8292-9952cd5d01fa
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Advanced]

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日現在、ヨーロッパの銀行は、満たさない支払いを辞退する可能性があります [PSD2](../../getting-started/compliance-payment-services-directive.md) 要件。 PSD2 に準拠するには [!DNL PayPal Payments Advanced] は、と統合されている必要があります [!DNL Cardinal Commerce]. 詳しくは、 [3-D セキュア（ペイフロー用）](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![必須設定](./assets/payment-methods-paypal-payments-advanced-required.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Web サイト | （オプション） PayPal マーチャントアカウントに関連付けられている電子メールアドレス。 電子メールアドレスでは大文字と小文字が区別され、アカウント内のアドレスと完全に一致する必要があります。 |
| [!UICONTROL Partner] | Web サイト | PayPal パートナー ID（該当する場合）。 |
| [!UICONTROL Vendor] | Web サイト | PayPal ユーザーのログイン名。 |
| ユーザー | Web サイト | PayPal アカウント上の別のユーザーの ID。 |
| [!UICONTROL Password] | Web サイト | PayPal マーチャントアカウントに関連付けられたパスワード。 |
| [!UICONTROL Test Mode] | Web サイト | 有効にすると、テスト環境で PayPal Payments Advanced が実行されます。 実稼働モードで「運用開始」の準備が整ったら、テストモードをオフにします。 オプション： `Yes` / `No` |
| [!UICONTROL Use Proxy] | Web サイト | プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを禁止している場合に、トラフィックをリダイレクトするために使用できます。 該当する場合は、PayPal サーバーとの接続を確立するために使用されるプロキシサーバーを識別します。 オプション： `Yes` / `No` <br/><br/>有効にした場合は、次のオプションを設定します。 <br/>**`Proxy Host`**— プロキシホストの IP アドレス。<br/>**`Proxy Port`**  — プロキシポートの番号。 |
| [!UICONTROL Enable this Solution] | Web サイト | PayPal Payments Advanced が、お客様が支払い方法として利用できるかどうかを決定します。 |
| [!UICONTROL Enable PayPal Credit] | Web サイト | PayPal クレジットをお客様が支払いオプションとして利用できるかどうかを指定します。 |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![PayPal クレジットの宣伝](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Web サイト | PayPal クレジットアカウントに関連付けられた発行者 ID です。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal から Publisher ID を取得します。 |
| [!UICONTROL Home Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] バナーをホームページに表示します。 オプション： <br/>**`Display`**— 次の条件を満たすかどうかを決定します。[!DNL PayPal Credit] バナーがストアのホームページに表示されます。 オプション： `Yes` / `No`<br/>**`Position`** - [!DNL PayPal Credit] バナーをホームページに表示します。 オプション：ヘッダー（中央）/サイドバー（右） <br/>**`Size`**— サイズを決定します [!DNL PayPal Credit] バナーをホームページに表示します。 オプション： `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] カテゴリページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] 製品ページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Web サイト | の位置とサイズを決定します。 [!DNL PayPal Credit] 買い物かごページのバナー。 オプション： （の場合と同じ） [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![基本設定](./assets/payment-methods-paypal-payments-advanced-basic-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時の支払い方法として PayPal Payments Advanced を識別する名前。 |
| [!UICONTROL Sort Order] | ストア表示 | PayPal Payments Advanced が、チェックアウト時に他の支払い方法と共に表示される場合に、PayPal Payments Advanced が表示される順序を決定する数値です。 |
| [!UICONTROL Payment Action] | Web サイト | 注文が送信されたときに PayPal が実行するアクションを決定します。 オプション： <br/>**`Authorization`**・買い付けを承認するが、資金を保留する。 その金額は、商人によって「取り込まれる」まで引き落とされません。<br/>**`Sale`**  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。 |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![詳細設定](./assets/paypal-advanced-settings2.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Web サイト | 適用可能な国の選択範囲を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Web サイト | 支払が受け入れられた国を識別します。 選択した国の請求先住所を持つ顧客のみが、この支払い方法で購入を行うことができます。 |
| [!UICONTROL Debug Mode] | Web サイト | ストアと支払いシステムの間で送信されたメッセージをログファイルに記録します。 オプション： `Yes` / `No` <br/><br/>**_注意：_**ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | Web サイト | トランザクションが発生する前に、ホスト上のセキュアチャネルが検証されるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Web サイト | CVV を入力した後で、お客様が CVV を編集できるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Web サイト | お客様がクレジットカードの後ろから CVV コードを入力する必要があるかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Web サイト | 顧客が支払いの確認を電子メールで受け取るかどうかを決定します。 オプション： `Yes` / `No` |
| [!UICONTROL URL Method for Cancel URL and Return URL] | Web サイト | トランザクション中に PayPal サーバーと情報を交換するために使用する方法を決定します。 オプション： <br/>**`GET`**— プロセスの結果である情報を取得します。 （これはデフォルトのメソッドです）。<br/>**`POST`**  — フォームに入力されたデータなど、データブロックをデータ処理プロセスに送信します。 |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![決済レポート設定](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Web サイト | PayPal のセキュア FTP サーバにログインするために必要なユーザ名。 |
| [!UICONTROL Password] | Web サイト | PayPal のセキュア FTP サーバにログインするために必要なパスワード。 |
| [!UICONTROL Sandbox Mode] | Web サイト | 有効にすると、実稼動環境で「運用を開始」する前に、テスト環境でレポートが実行されます。 オプション： `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Web サイト | 決済レポートが管理される URL。 デフォルト値： `reports.paypal.com` |
| [!UICONTROL Custom Path] | Web サイト | 決済レポートがサーバー上に保存されるパス。 デフォルト値： `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Web サイト | 有効にすると、決済レポートがスケジュールに従って自動的に取得されます。 オプション： `Yes` / `No` |
| [!UICONTROL Schedule] | グローバル | PayPal によって決済レポートが生成される頻度を決定します。 オプション： `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | グローバル | 決済レポートが生成される時間、分、秒を決定します。 |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![フロントエンドエクスペリエンス設定](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | ストア表示 | ストアに表示される PayPal ロゴを指定します。 2 つのサイズに 4 つの基本的なスタイルがあります。 オプション： `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | ストア表示 | PayPal マーチャントページの外観を決定します。 許可されている値： <br/>**`paypal`**- PayPal ページスタイルを使用します。<br/>**`primary`**  — アカウントプロファイルで「プライマリ」スタイルとして指定したページスタイルを使用します。 <br/>**`your_custom_value`**— アカウントプロファイルで指定されたカスタムの支払いページスタイルを使用します。 |
| [!UICONTROL Header Image URL] | ストア表示 | チェックアウトページの左上隅に表示される画像の URL。 最大サイズは 750 x 90 ピクセルです。 <br/><br/>**_注意：_**PayPal では、画像をセキュアな (https) サーバーに保存することをお勧めします。 そうしないと、顧客のブラウザーが、「ページにセキュリティで保護された項目とセキュリティで保護されていない項目の両方が含まれている」と警告する場合があります。 |
| [!UICONTROL Header Image Background Color] | ストア表示 | 六字 [16 進数の色](https://en.wikipedia.org/wiki/Web_colors) チェックアウトページのヘッダーの背景色のコード。 コードは、大文字と小文字のどちらでも入力できます。 |
| [!UICONTROL Header Image Border Color] | ストア表示 | ヘッダーの周囲の 2 ピクセル境界線に対する 6 文字の 16 進カラーコードです。 |
| [!UICONTROL Page Background Color] | ストア表示 | ヘッダーと支払いフォームの後ろに表示されるチェックアウトページの背景色の 6 文字の 16 進数カラーコードです。 |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express チェックアウトの基本設定](./assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時の PayPal Express Checkout 支払い方法を識別する名前。 |
| [!UICONTROL Sort Order] | ストア表示 | チェックアウト時に他の支払い方法と共にリストされた場合に、PayPal Express Checkout が表示される順序を決定する数値です。 入力 `0` をリストの先頭に追加します。 |
| [!UICONTROL Payment Action] | Web サイト | PayPal が注文を受け取ったときに実行するアクションを決定します。 オプション： <br/>**`Authorization`**・買い付けを承認するが、資金を保留する。 その金額は、商人によって「取り込まれる」まで引き落とされません。<br/>**`Sale`**  — 購入金額は、お客様のアカウントから承認され、直ちに取り下げられます。 <br/>**`Order`**— 定義された期間内に、マーチャントが顧客の購入者アカウントから注文済みの合計金額までを取得できる PayPal との契約を表します。 これは最大 29 日間です。 資金を取り込むには、1 つ以上の請求書をコマース管理者から生成する必要があります。 |
| [!UICONTROL URL Display on Product Details Page] | ストア表示 | 「PayPal でのチェックアウト」ボタンを製品ページに表示するかどうかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![PayPal Express チェックアウトの詳細設定](./assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | ストア表示 | PayPal Express Checkout が買い物かごの支払いオプションとして表示されるかどうかを指定します。 オプション： `Yes` （推奨） / `No` |
| [!UICONTROL Payment Action Applicable From] | Web サイト | 適用可能な国の選択範囲を決定します。 オプション： `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Web サイト | 支払が受け入れられた国を識別します。 選択した国の請求先住所を持つ顧客のみが、この支払い方法で購入を行うことができます。 |
| [!UICONTROL Debug Mode] | Web サイト | ストアと PayPal 支払いシステム間で送信されたメッセージをログファイルに記録します。 オプション： `Yes` / `No` <br/><br/>**_注意：_**ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI データセキュリティ基準に従って、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | Web サイト | ホストセキュリティ証明書の検証を有効にします。 オプション： `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Web サイト | PayPal サイト上の顧客の買い物かごからの行項目の完全な概要を表示します。 オプション： `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Web サイト | 顧客が PayPal サイトからトランザクションを完了できるか、またはストアに戻って注文を送信する前に注文の確認手順を完了する必要があるかを指定します。 オプション： `Yes` / `No` |

{style="table-layout:auto"}
