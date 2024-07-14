---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: Commerce Admin の [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] ページの [!UICONTROL PayPal Express Checkout] セクションで、設定を確認します。
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1702'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日（PT）現在、ヨーロッパの銀行は、[PSD2](../../getting-started/compliance-payment-services-directive.md) の要件を満たさない支払いを拒否する可能性があります。 PayPal Express Checkout がPSD2 に準拠するには、すべての要件が PayPal で処理されるため、何もする必要はありません。

{{config}}

## [!UICONTROL Required PayPal Settings]

![PayPal Express チェックアウトが必要な設定 ](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | Web サイト | 顧客が利用できる支払方法として [!DNL PayPal Express Checkout] を有効化します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | Web サイト | 顧客が利用できる支払い方法として、合理化された PayPal コンテキスト内チェックアウトをアクティブ化します。 オプション：`Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | Web サイト | PayPal クレジットを有効化して、顧客が今すぐ購入しても、後で支払えるようにします。 事前に支払いを受けますが、顧客は支払う時間が長くなります。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Express Checkout]

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Web サイト | PayPal マーチャントアカウントが確立されたときに指定したメールアドレスを指定します。 メールアドレスは大文字と小文字が区別され、PayPal システムのメールアドレスと完全に一致する必要があります。 |
| [!UICONTROL API Authentication Methods] | Web サイト | API 認証に使用する方法を決定します。 オプション：<br/>**`API Signature`**- フォームに _[!UICONTROL API Signature]_フィールドを表示します。<br/>**`API Certificate`**- フォームに「_[!UICONTROL API Certificate]_」フィールドを表示します。 |
| [!UICONTROL API Username] | Web サイト | PayPal マーチャントアカウントに関連付けられている API ユーザー名。 |
| [!UICONTROL API Password] | Web サイト | PayPal マーチャントアカウントに関連付けられた API パスワード。 |
| [!UICONTROL API Signature] | Web サイト | PayPal マーチャントアカウントに関連付けられた API 署名。 |
| [!UICONTROL API Certificate] | Web サイト | 参照して API 証明書をアップロードします。 |
| [!UICONTROL Get Credentials from PayPal] |  | PayPal から API 資格情報を取得します。 |
| [!UICONTROL Sandbox Credentials] |  | PayPal からサンドボックス資格情報を取得します。 |
| [!UICONTROL Sandbox Mode] | Web サイト | テスト環境で PayPal Express チェックアウトを実行するには、サンドボックス API 資格情報を入力し、これを `Yes` に設定します。 オプション：`Yes` / `No` |
| [!UICONTROL API Uses Proxy] | Web サイト | プロキシサーバーを使用してCommerceと PayPal システムを接続する場合は、これを `Yes` に設定します。 オプション：`Yes` / `No` |
| [!UICONTROL Proxy Host] | Web サイト | API がプロキシを使用する場合、プロキシホストの IP アドレスを指定します。 |
| [!UICONTROL Proxy Port] | Web サイト | API がプロキシを使用する場合、プロキシホストが使用するポートを指定します。 |

{style="table-layout:auto"}

### [!UICONTROL Advertise PayPal Credit]

![PayPal クレジットの広告 ](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Web サイト | PayPal クレジットアカウントに関連付けられたパブリッシャー ID。 |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal からパブリッシャー ID を取得します。 |
| [!UICONTROL Home Page] | Web サイト | ホーム ページ上の [!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：<br/>**表示** - ストアのホームページに [!DNL PayPal Credit] のバナーを表示します。 オプション：`Yes` / `No` <br/>**位置** - ホームページ上の [!DNL PayPal Credit] のバナーの位置を決定します。 オプション：ヘッダー（中央）/サイドバー（右） <br/>**サイズ** - ホームページの [!DNL PayPal Credit] のバナーのサイズを決定します。 オプション：`190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Web サイト | カテゴリページ上の [!DNL PayPal Credit] のバナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page] と同じ） |
| [!UICONTROL Catalog Product Page] | Web サイト | 製品ページ上の [!DNL PayPal Credit] バナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page] と同じ） |
| [!UICONTROL Checkout Cart Page] | Web サイト | 買い物かごページの [!DNL PayPal Credit] のバナーの位置とサイズを決定します。 オプション：（[!UICONTROL Home Page] と同じ） |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![ 基本設定 ](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Title] | ストア表示 | チェックアウト時の PayPal Express チェックアウト支払い方法を識別する名前。 |
| [!UICONTROL Sort Order] | ストア表示 | チェックアウト時に他のお支払い方法と一緒に表示される場合に、PayPal Express チェックアウトの順序を決定する数字を指定します。 リストの上部に `0` と入力します。 |
| [!UICONTROL Payment Action] | Web サイト | 注文を受け取った際に PayPal が実行するアクションを決定します。 オプション：<br/>**`Authorization`**– 購入を承認しますが、資金を保留します。 この金額は、マーチャントによって「キャプチャ」されるまで引き出されません。<br/>**`Sale`** – 購入金額は許可され、すぐにお客様のアカウントから引き出されます。 <br/>**`Order`**- PayPal との契約を表します。この契約により、マーチャントは、定義された期間内に顧客のバイヤーアカウントから注文された合計を上限とする 1 つ以上の金額を取得できます。 これは最大 29 日間有効です。 資金を取得するには、Commerce管理者から 1 つ以上の請求書を生成する必要があります。 |
| [!UICONTROL Display on Product Details Page] | ストア表示 | 製品ページに「PayPal でチェックアウト」ボタンを表示するかどうかを決定します。 オプション：`Yes`/`No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![ 詳細設定 ](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | ストア表示 | PayPal Express チェックアウトが買い物かごに支払いオプションとして表示されるかどうかを決定します。 オプション：`Yes` （PayPal 推奨）/`No` |
| [!UICONTROL Payment Action Applicable From] | Web サイト | 適用可能な国選択の範囲を決定します。 オプション：`All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Web サイト | 支払いが受け入れられる各国を識別します。 この支払い方法で購入できるのは、選択した国の請求先住所を持つお客様のみです。 |
| [!UICONTROL Debug Mode] | Web サイト | ストアと支払いシステム間で送信されたメッセージをログ ファイルに記録します。 オプション：`Yes` / `No` <br/><br/>**_注意：_**ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | Web サイト | ホスト セキュリティ証明書の検証を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Web サイト | PayPal サイトの顧客の買い物かごからの明細項目の完全な概要を表示します。 オプション：`Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Web サイト | PayPal サイトに最大 10 の配送オプションが含まれます。 オプション：`Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | ストア表示 | PayPal 受け入れボタンに使用する画像のタイプを決定します。 オプション：<br/>**`Dynamic`**- （推奨） PayPal サーバーから動的に変更できる画像を表示します。<br/>**`Static`** – 動的に変更できない静的画像を表示します。 |
| [!UICONTROL Enable PayPal Guest Checkout] | Web サイト | PayPal アカウントをお持ちでないお客様は、PayPal Express Checkout で購入できます。 オプション：`Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Web サイト | 顧客の請求先住所が必須かどうかを決定します。 オプション：`Yes`/`No`/`For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Web サイト | 顧客がストアと [ 請求契約 ](../../stores-purchase/paypal-billing-agreements.md) を締結できるかどうかを決定します。 オプション：<br/>**`Auto`**– お客様は、エクスプレスチェックアウト中に請求契約にサインアップできます。<br/>**`Ask Customer`** – お客様は請求契約に新規登録するかどうかを尋ねられます。 <br/>**`Never`**– お客様は請求契約に新規登録するオプションを提供されません。 |
| [!UICONTROL Skip Order Review Step] | Web サイト | 顧客が PayPal サイトからトランザクションを完了できるか、またはストアに戻って注文を送信する前に注文レビュー手順を完了する必要があるかを決定します。 オプション：`Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Billing Agreement Settings]

![ 請求契約の設定 ](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Enabled] | Web サイト | 有効化すると、請求契約書がチェックアウト時に支払いオプションとして顧客に表示されます。 オプション：`Yes` / `No` |
| [!UICONTROL Title] | ストア表示 | チェックアウト時に支払いオプションとして表示される PayPal 請求契約オプションのラベル。 |
| [!UICONTROL Sort Order] | ストア表示 | チェックアウト時に他の支払い方法と共に請求契約がリストされる順序を決定します。 |
| [!UICONTROL Payment Action] | Web サイト | PayPal がトランザクションをどのように管理するかを決定します。オプション：<br/>**認証** – 購入を承認しますが、資金を保留します。 この金額は、マーチャントによって「キャプチャ」されるまで引き出されません。 <br/>**セール** – 購入金額は許可され、すぐにお客様のアカウントから引き出されます。 |
| [!UICONTROL Payment Applicable From] | Web サイト | 適用可能な国選択の範囲を決定します。 オプション：許可されているすべての国/特定の国 |
| [!UICONTROL Countries Payment Applicable From] | Web サイト | 支払いが受け入れられる各国を識別します。 この支払い方法で購入できるのは、選択した国の請求先住所を持つお客様のみです。 |
| [!UICONTROL Debug Mode] | Web サイト | 支払システムとの通信をログ ファイルに記録します。 オプション：`Yes` / `No` <br/><br/>**_注意：_**ログファイルはサーバーに保存され、開発者のみがアクセスできます。 PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。 |
| [!UICONTROL Enable SSL Verification] | Web サイト | 暗号化された SSL チャネルでトランザクションが確実に実行されるように、に対して検証手順を有効にします。 オプション：`Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Web サイト | 有効にすると、PayPal 支払いページの買い物かごからの明細項目の概要が表示されます。 オプション：`Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Web サイト | 有効にすると、顧客は、顧客アカウントのダッシュボードから請求契約を開始できます。 |

{style="table-layout:auto"}

### [!UICONTROL Settlement Report Settings]

![ 決算報告書の作成等 ](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Web サイト | PayPal のセキュア FTP サーバーにログインするために必要なユーザー名。 |
| [!UICONTROL Password] | Web サイト | PayPal のセキュア FTP サーバーにログインするために必要なパスワード。 |
| [!UICONTROL Sandbox Mode] | Web サイト | 有効にすると、実稼動環境で「実稼動」になる前に、テスト環境でレポートを実行します。 オプション：`Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Web サイト | 決済レポートを管理する URL。 デフォルト値：`reports.paypal.com` |
| [!UICONTROL Custom Path] | Web サイト | 決済レポートがサーバー上に保存されるパス。 デフォルト値：`/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Web サイト | 有効化すると、スケジュールに従って決済レポートが自動的に取得されます。 オプション：`Yes` / `No` |
| [!UICONTROL Schedule] | Web サイト | PayPal によって決済レポートが生成される頻度を決定します。 オプション：`Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Web サイト | 決済レポートが生成される時間、分、および秒を決定します。 |

{style="table-layout:auto"}

### [!UICONTROL Frontend Experience Settings]

![ フロントエンドエクスペリエンスの設定 – PayPal マーチャントページのスタイル ](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | ストア表示 | ストアに表示される PayPal ロゴを決定します。 2 つのサイズには 4 つの基本スタイルがあります。 オプション：`No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | ストア表示 | PayPal マーチャントページの外観を決定します。 許可されている値：**`paypal`** - PayPal ページスタイルを使用します。 <br/>**`primary`**- アカウントプロファイルで「プライマリ」スタイルとして識別したページスタイルを使用します。<br/>**`your_custom_value`** - アカウントプロファイルで指定されているカスタム支払いページスタイルを使用します。 |
| [!UICONTROL Header Image URL] | ストア表示 | チェックアウトページの左上隅に表示される画像の URL。 最大サイズは 750 x 90 ピクセルです。 <br/><br/>**_注意：_**PayPal では、画像を安全な（https）サーバーに保存することをお勧めします。 そうしないと、顧客のブラウザーで「ページにセキュアな項目とセキュアでない項目の両方が含まれています」と警告される場合があります。 |
| [!UICONTROL Header Image Background Color] | ストア表示 | チェックアウトページのヘッダーの背景色を 6 文字 [16 進数カラー ](https://en.wikipedia.org/wiki/Web_colors) のコードで表します。 コードは、大文字でも小文字でも入力できます。 |
| [!UICONTROL Header Image Border Color] | ストア表示 | ヘッダーの周囲の 2 ピクセルの境界線の 6 文字 [16 進色 ](https://en.wikipedia.org/wiki/Web_colors) コード。 |
| [!UICONTROL Page Background Color] | ストア表示 | ヘッダーと支払いフォームの後ろに表示される、チェックアウトページの背景色の 6 文字 [16 進数カラー ](https://en.wikipedia.org/wiki/Web_colors) コード。 |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![ フロントエンドエクスペリエンス設定 – スマートボタンのカスタマイズ ](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Customize Button] | ストア表示 | ストアのレイアウトとテーマに合わせて PayPal スマート ボタンをカスタマイズできるかどうかを決定します。 これらの変更は、チェックアウトページ、製品ページ、買い物かごページ、ミニ買い物かごに個別に適用できます。 |
| [!UICONTROL Label] | ストア表示 | PayPal がスマート支払いボタンに表示するテキスト。 オプション：<br/>**`Checkout`**（「PayPal チェックアウト」として表示）<br/>**`Pay`** （「PayPal で支払う」として表示） <br/>**`Buy Now`**（「PayPal で今すぐ購入」として表示）<br/>**`PayPal`** （「PayPal」として表示） <br/>**`Installment`**（「PayPal」として表示）<br/>**`Credit`** （「PayPal クレジット」として表示） |
| [!UICONTROL Layout] | ストア表示 | PayPal スマート ボタンを縦に表示するか横に表示するかを決定します。 オプション：<br/>**`Vertical`**- 「ゲストのチェックアウトを有効にする」が選択されているかどうかに関係なく、購入者は PayPal にログインするか、PayPal アカウントを作成する必要があります。<br/>**`Horizontal`** - 「ゲストのチェックアウトを有効にする」が選択されている場合、は PayPal ポップアップウィンドウに **`Pay with Debit Card or Credit Card`** のボタンを表示します。 それ以外の場合、購入者は PayPal にログインするか、PayPal アカウントを作成する必要があります。 |
| [!UICONTROL Size] | ストア表示 | スマート支払いボタンのサイズを設定します。 オプション：<br/>**`Medium`**～250 ピクセル x 35 ピクセル<br/>**`Large`**～350 ピクセル x 40 ピクセル <br/>**`Responsive`**- （デフォルト）コンテナの幅に調整します。 最小幅は 100 ピクセル、最大幅は 500 ピクセルです。 高さは幅に基づいて動的に調整されます。 |
| [!UICONTROL Shape] | ストア表示 | スマート支払いボタンの形状を設定します。 オプション：`Pill` （デフォルト）/`Rectangle` |
| [!UICONTROL Color] | ストア表示 | スマート支払いボタンの色を設定します。 オプション：`Gold` （デフォルト）/`Blue`/`Silver`/`Black` |

{style="table-layout:auto"}

#### [!UICONTROL Customize Smart Buttons (Features)]

![ フロントエンドエクスペリエンスの設定 – スマートボタンのカスタマイズ（機能） ](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| フィールド | [ 範囲 ](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | ストア表示 | チェックアウトページに表示される他の PayPal 資金調達オプションを決定します。 選択したオプションは、チェックアウトページには表示されません。 選択されていないオプションは、PayPal がストアの通貨と購入者の場所をサポートしている場合にのみ表示されます。 オプション：`PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{style="table-layout:auto"}
