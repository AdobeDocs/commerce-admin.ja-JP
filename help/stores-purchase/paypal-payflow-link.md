---
title: PayPal ペイフローリンク
description: ストアでオンライン支払いソリューションとして PayPal Payflow Link を設定する方法を説明します。
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 0%

---

# PayPal ペイフローリンク

PayPal Payflow Link は、米国およびカナダのマーチャントのみが利用できます。 お客様は PayPal アカウントを持ち、PayPal が管理するフォームにクレジットカード情報を入力する必要はありません。 これらの情報は、Adobe CommerceやMagento Open Source サーバーに保存されません。 Payflow Link は、管理者から作成された注文には使用できません。

オンラインとオフラインの両方の払い戻しでクレジットメモがサポートされています。 ただし、複数のオンライン払い戻しはサポートされていません。

>[!IMPORTANT]
>
>**PSD2 の要件：** <br/>
>2019 年 9 月 14 日（PT）現在、ヨーロッパの銀行は、[PSD2](../getting-started/compliance-payment-services-directive.md) の要件を満たさない支払いを拒否する可能性があります。 PSD2 に準拠するには、PayPal Payflow Link をCommerceと統合する必要があります。 詳しくは、[3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/) を参照してください。

## 要件

- [PayPal ビジネスアカウント ][1] PayPal Payflow Pro ゲートウェイは、PayPal のマーチャントアカウントをマーチャントウェブサイトとリンクし、ゲートウェイとマーチャントアカウントの両方として機能します。

- 複数のCommerce web サイトを管理する場合は、web サイトごとに個別の PayPal マーチャントアカウントが必要です。

## 顧客のワークフロー

1. **お客様がチェックアウトに進む** - チェックアウト中、お客様は PayPal Payflow リンクでの支払いを選択し、クレジットカード情報を入力します。 お客様は個人の PayPal アカウントを持っている必要はありません。
1. **顧客が「Pay Now （今すぐ支払う）」を選択** – 顧客が「Pay Now （今すぐ支払う）」ボタンをタップして注文を送信します。
1. **顧客がクレジットカード情報を入力** - PayPal がホストするフォームにクレジットカード情報を入力します。 お客様が _支払いをキャンセル_ リンクをクリックすると、お客様はチェックアウトの支払い情報ステージに戻り、注文ステータスが _キャンセル_ に変わります。
1. **お客様が注文を送信** - クレジットカード情報は PayPal に直接送信され、Commerce サイトには保持されません。

## 注文ワークフロー

1. **PayPal はリクエストを受信** - PayPal は今すぐ支払うためにお客様からリクエストを受信します。
1. **PayPal は支払い情報を検証します** - PayPal はクレジットカード情報を検証し、適切なステータスを割り当てます。
   - **支払検証済：** 検証済の場合、取引が決済されるまで、最初に注文に _支払保留中_ ステータスが割り当てられます。
   - **処理中** - トランザクションが成功しました。
   - **支払い待ち** - システムが PayPal から応答を受信しませんでした。
   - **キャンセル** - トランザクションが何らかの理由で成功しませんでした。
   - **不正の疑い** - トランザクションが一部の [PayPal 不正フィルター ](paypal.md#paypal-fraud-management-filters) を渡しませんでした。 システムは、PayPal から取引が不正サービスによって審査中であるという応答を受け取ります。
   - **支払いキャンセル：** 顧客が _支払いをキャンセル_ リンクをクリックすると、チェックアウトの支払い情報ステージに戻り、注文ステータスが _キャンセル_ に変更されます。
1. **顧客は確認ページにリダイレクトされます** - トランザクションが正常に完了すると、顧客はストアの注文確認ページにリダイレクトされます。 何らかの理由でトランザクションが失敗した場合は、チェックアウトページにエラーメッセージが表示され、顧客にチェックアウトプロセスを繰り返すように指示されます。 これらの状況は PayPal によって管理されます。
1. **マーチャントが注文を履行** - マーチャントは通常どおり請求書を送信し、注文を出荷します。

## PayPal アカウントの設定

1. [PayPal ビジネスアカウント ][2] にログインします。

1. PayPal Manager を使用して [ ホストされたチェックアウトページ ][4] を次の設定で設定します。

   - 「**[!UICONTROL Security Options]**」で、次の設定を行います。

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - 「**[!UICONTROL Customize]**」を選択し、「**[!UICONTROL Layout C]**」を選択します。

     レイアウト C では、クレジットカードとデビットカードのフィールドのみが表示され、サイトにフレームを組み込んだり、スタンドアロンポップアップとして使用したりできます。 サイズは 490 x 565 ピクセルで固定され、エラーメッセージ用のスペースも追加されます。 一部のシステムでは、この設定によりトランスペアレント リダイレクトの問題が修正されます。

1. 設定が完了したら、「**[!UICONTROL Save and Publish]**」をクリックします。

1. 追加のユーザーを設定する（PayPal が推奨）:

   - メインメニューの 2 行目にある「**[!UICONTROL Manage Users]**」をクリックします。

   - アカウントに別のユーザーを追加するには、「**[!UICONTROL Add User]**」をクリックします。

   - _ユーザーを追加_ フォームの次のセクションの必須フィールドに入力します。

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - 「**[!UICONTROL Update]**」をクリックします。

## PayPal Payflow リンクの設定

>[!TIP]
>
>「**[!UICONTROL Save Config]**」をクリックすると、いつでも進行状況を保存できます。

### 手順 1：設定の開始

この設定方法は、既存の PayPal アカウントがあることを前提としています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Payment Methods]**」を選択します。

1. Commerceのインストールに複数の web サイト、ストアまたはビューがある場合は、この設定を適用するストアビューに **[!UICONTROL Store View]** を設定します。

1. 「_[!UICONTROL Merchant Location]_」セクションで、ビジネスが所在する&#x200B;**[!UICONTROL Merchant Country]**&#x200B;を選択します。

   この設定により、設定に表示される PayPal ソリューションの選択が決まります。

   ![ 商国 ](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 必要に応じて「**[!UICONTROL PayPal Payment Gateways]**」を展開し、「**[!UICONTROL Configure]**」をクリックして **[!UICONTROL Payflow Link]** を表示します。

   ![ ペイフローリンク – 設定 ](./assets/payflow-link.png){width="600" zoomable="yes"}

### 手順 2：必要な PayPal 設定を完了する

![ 必須 PayPal 設定 – PayPal Payflow Link](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. （任意） **[!UICONTROL Email Associated with your PayPal Merchant Account]** を入力します。

   >[!IMPORTANT]
   >
   >メールアドレスでは大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスが PayPal マーチャントアカウントで指定されたメールアドレスと一致する必要があります。

1. PayPal マーチャントアカウントへのログインに使用する次の資格情報のいずれかを入力します。

   - **[!UICONTROL Partner]** - PayPal パートナー ID。
   - **[!UICONTROL User]** - PayPal アカウントで設定されている別のユーザーの ID。
   - **[!UICONTROL Vendor]** - PayPal ユーザーのログイン名。

1. PayPal アカウントに関連付けられている **[!UICONTROL Password]** を入力します。

1. テストトランザクションを実行するには、**[!UICONTROL Test Mode]** を `Yes` に設定します。

   サンドボックスで設定をテストする場合は、PayPal が推奨する [ クレジットカード番号 ][3] のみを使用します。 実稼動に移行する準備が整ったら、設定に戻って「テストモード」を `No` に設定します。

1. システムがプロキシサーバーを使用して PayPal システムへの接続を確立する場合は、**[!UICONTROL Test Mode]** を `Yes` に設定し、次の手順を実行します。

   - **[!UICONTROL Proxy Host]** の IP アドレスを入力します。

   - **[!UICONTROL Proxy Port]** のポート番号を入力します。

     プロキシは、サーバーファイアウォールが PayPal サーバーへの直接アクセスを防ぐ場合に使用されます。 この場合、サードパーティのサーバーを使用してトラフィックがリレーされます。

1. **[!UICONTROL Enable Payflow Link]** を `Yes` に設定します。

1. 顧客に対して [PayPal エクスプレスチェックアウト ](paypal-express-checkout.md) オプションを有効にする場合は、**[!UICONTROL Enable Express Checkout]** を `Yes` に設定します。

1. 顧客に [PayPal クレジット ](paypal.md#paypal-credit-and-pay-later) を提供する場合は、**[!UICONTROL Enable PayPal Credit]** を `Yes` に設定します。

### 手順 3：広告 PayPal クレジット/広告 PayPal PayLater の設定（オプション）

2.4.3 リリース以降、PayPal PayLater は PayPal を含むデプロイメントでサポートされます。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割払いで注文の支払いを行うことができます。 PayPal クレジットエクスペリエンスは非推奨（廃止予定）となりました。

**[!UICONTROL Enable PayPal PayLater Experience]** を次のいずれかに設定します。

- `Yes` - PayPal PayLater をアドバタイズを設定するには
- `No` – 広告 PayPal クレジットを設定する

#### PayPal クレジットのアドバタイズ

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Advertise PayPal Credit]**」セクションを展開します。

   ![PayPal クレジットの広告 ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. アカウント情報を取得するには、**[!UICONTROL Get Publisher ID from PayPal]** をクリックし、指示に従ってください。

1. **[!UICONTROL Publisher ID]** を入力します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Home Page]**」セクションを展開します。

   ![PayPal クレジット ホーム ページ設定のアドバタイズ ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. ページにバナーを配置するには、「**[!UICONTROL Display]**」を「`Yes`」に設定します。

1. **[!UICONTROL Position]** を次のいずれかに設定します。

   - `Header (center)`
   - `Sidebar (right)`

1. **[!UICONTROL Size]** を次のいずれかに設定します。

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. ![ 展開セレクター ](../assets/icon-display-expand.png) 残りのセクションを展開し、ホームページ設定について前の手順を繰り返します。

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### PayPal PayLater のアドバタイズ

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Advertise PayPal PayLater]**」セクションを展開します。

1. **[!UICONTROL Enable PayPal PayLater]** を `Yes` に設定します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Home Page]**」セクションを展開します。

   ![PayPal クレジット ホーム ページ設定のアドバタイズ ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. ページにバナーを配置するには、「**[!UICONTROL Display]**」を「`Yes`」に設定します。

1. **[!UICONTROL Position]** を次のいずれかに設定します。

   - `Header (center)`
   - `Sidebar`

1. **[!UICONTROL Style Layout]** を次のいずれかに設定します。

   - `Text`
   - `Flex`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]** の場合のみ、**[!UICONTROL Logo Type]** を次のいずれかに設定します。

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]** の場合のみ、**[!UICONTROL Logo Position]** を次のいずれかに設定します。

   - `Left`
   - `Right`
   - `Top`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]** の場合のみ、**[!UICONTROL Text Color]** を次のいずれかに設定します。

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]** の場合のみ、**[!UICONTROL Text Size]** を次のいずれかに設定します。

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]** の場合のみ、**[!UICONTROL Ratio]** を次のいずれかに設定します。

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]** の場合のみ、**[!UICONTROL Color]** を次のいずれかに設定します。

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. ![ 展開セレクター ](../assets/icon-display-expand.png) 残りのセクションを展開し、前の手順を繰り返します。

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順 4：基本設定を完了する

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Basic Settings - PayPal Payflow Link]**」セクションを展開します。

   ![ 基本設定 – PayPal ペイフローリンク ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Title]** しくは、チェックアウト時に PayPal ペイフローリンクを識別するタイトルを入力します。

   タイトル _デビットまたはクレジットカード_ を使用することをお勧めします。

1. 複数の支払方法を提供する場合は、**[!UICONTROL Sort Order]** の番号を入力して、他の支払方法とともにリストされた場合に表示される Payflow Link の順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. **[!UICONTROL Payment Action]** を次のいずれかに設定します。

   - `Authorization` – 購入を承認し、資金を保留します。 この金額は、マーチャントによって取り込まれるまで引き出されません。
   - `Sale` – 購入金額は許可され、すぐにお客様のアカウントから引き出されます。

### 手順 5：詳細設定の完了

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Advanced Settings]**」セクションを展開します。

   ![ 詳細設定 – PayPal ペイフローリンク ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Payment Applicable From]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての [ 国 ](../getting-started/store-details.md#country-options) のお客様がこの支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;のリストが表示されます。 Ctrl キーを押しながら、顧客がストアから購入できるリストの各国を選択します。

1. 支払いシステムとの通信をログファイルに書き込むには、**[!UICONTROL Debug Mode]** を `Yes` に設定します。

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、**[!UICONTROL Enable SSL Verification]** を `Yes` に設定します。

1. クレジットカードの裏面から 3 桁の CVV セキュリティコードの入力を修正できるようにする場合は、**[!UICONTROL CVV Entry is Editable]** を `Yes` に設定します。

1. 顧客に CVV コードの入力を要求するには、**[!UICONTROL Require CVV Entry]** を `Yes` に設定します。

1. 顧客に支払の確認を送信するには、**[!UICONTROL Send Email Confirmation]** を `Yes` に設定します。

1. トランザクション中に PayPal サーバーと情報を交換するために使用する方法を決定するには、**[!UICONTROL URL method for Cancel URL and Return URL]** を次のいずれかに設定します。

   - `GET` - プロセスの結果である情報を取得します（デフォルトメソッド）。
   - `POST` - フォームに入力されたデータなどのデータブロックをデータ処理プロセスに提供します。

   _キャンセル URL_ と _返品 URL_ は、PayPal サーバーのチェックアウトプロセスの支払い部分を完了またはキャンセルした後に顧客が戻ってくるページを参照します

1. ストアの必要に応じて、次の節を完了します。

   - [決済報告書の設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### 決済報告書の設定

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Settlement Report Settings]**」セクションを展開します。

   ![ 決済報告書の設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL SFTP Credentials]** の場合は、次の手順を実行します。

   - PayPal セキュア FTP サーバーに新規登録している場合は、次の SFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - サイトで高速チェックアウトを使用して運用を開始する前にテストレポートを実行するには、**[!UICONTROL Sandbox Mode]** を `Yes` に設定します。

   - **[!UICONTROL Custom Endpoint Hostname or IP Address]** を入力します。

     デフォルト値は `reports.paypal.com` です。

   - レポートを保存する **[!UICONTROL Custom Path]** を入力します。

     デフォルト値は `/ppreports/outgoing` です。

1. スケジュールに従ってレポートを生成するには、**[!UICONTROL Scheduled Fetching]** の設定を完了します。

   - **[!UICONTROL Enable Automatic Fetching]** を `Yes` に設定します。

   - **[!UICONTROL Schedule]** を次のいずれかに設定します。

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal は各レポートを 45 日間保持します。

   - レポートを生成する時、分、秒に **[!UICONTROL Time of Day]** を設定します。

#### フロントエンドエクスペリエンス設定

_[!UICONTROL Frontend Experience Settings]_&#x200B;を使用して、サイトに表示する PayPal ロゴを選択したり、PayPal マーチャントページの外観をカスタマイズしたりします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Frontend Experience Settings]**」セクションを展開します。

   ![ フロントエンドエクスペリエンスの設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. ストアの PayPal ブロックに表示する **[!UICONTROL PayPal Product Logo]** を選択します。

   PayPal ロゴは、4 つのスタイルと 2 つのサイズで使用できます。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal マーチャントページの外観をカスタマイズするには：

   - PayPal マーチャントページに適用する **[!UICONTROL Page Style]** ージの名前を入力します。

      - `paypal` - PayPal ページスタイルを使用します。
      - `primary` - アカウントプロファイルで _プライマリ_ スタイルとして識別したページスタイルを使用します。
      - `your_custom_value` - アカウントプロファイルで指定されているカスタム支払いページスタイルを使用します。

   - **[!UICONTROL Header Image URL]**：支払いページの左上隅に表示する画像の URL を入力します。 最大ファイルサイズは、幅 750 ピクセル、高さ 90 ピクセルです。

     >[!NOTE]
     >
     >PayPal では、画像をセキュアな（https）サーバーに配置することをお勧めします。 そうしないと、ブラウザーは _ページにセキュアな項目とセキュアでない項目の両方が含まれている_ と警告する場合があります。

   - ページの色を設定するには、次の各項目に対して、6 文字の 16 進コードを `#` 記号なしで入力します。

      - **[!UICONTROL Header Background Color]** - チェックアウトページヘッダーの背景色
      - **[!UICONTROL Header Border Color]** - ヘッダーの周囲の 2 ピクセルの境界線の色。
      - **[!UICONTROL Page Background Color]** - チェックアウトページ、およびヘッダーと支払いフォーム周辺の背景色

### 手順 6:PayPal Express チェックアウトの基本設定を完了する

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Basic Settings - PayPal Express Checkout]**」セクションを展開します。

   ![ 基本設定 ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Title]** の場合は、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   ストア表示ごとにタイトルを _PayPal_ に設定することをお勧めします。

1. 複数の支払い方法を提供する場合は、**[!UICONTROL Sort Order]** の番号を入力して、他の支払い方法と共に表示される PayPal Express Checkout の表示順序を決定します。

   この番号は、他の支払い方法と相対的です。 （`0` = 1 番目、`1` = 2 番目、`2` = 3 番目など）。

1. **[!UICONTROL Payment Action]** を次のいずれかに設定します。

   - `Authorization` – 購入を承認し、資金を保留します。 この金額は、マーチャントによって _キャプチャ_ されるまで引き出されません。
   - `Sale` – 購入金額は許可され、すぐにお客様のアカウントから引き出されます。

1. 製品ページに「_[!UICONTROL Check out with PayPal]_」ボタンを表示するには、「**[!UICONTROL Display on Product Details Page]**」を「`Yes`」に設定します。

### 手順 7:PayPal Express チェックアウトの詳細設定を完了する

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Advanced Settings]**」セクションを展開します。

   ![ 詳細設定 ](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display on Shopping Cart]** を `Yes` に設定します。

1. **[!UICONTROL Payment Applicable From]** を次のいずれかに設定します。

   - `All Allowed Countries` - ストア設定で指定されたすべての国の顧客は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;のリストが表示されます。 複数の国を選択するには、Ctrl キー（PC）または Command キー（Mac）を押しながら、各項目をクリックします。

1. 支払いシステムとの通信をログファイルに書き込むには、**[!UICONTROL Debug Mode]** を `Yes` に設定します。

   >[!NOTE]
   >
   >PCI Data Security Standards に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの信頼性の検証を有効にするには、**[!UICONTROL Enable SSL Verification]** を `Yes` に設定します。

1. PayPal サイトの品目別の顧客オーダーの完全な概要を表示するには、**[!UICONTROL Transfer Cart Line Items]** を `Yes` に設定します。

1. お客様が注文レビューのためにストアに戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、**[!UICONTROL Skip Order Review Step]** を `Yes` に設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
