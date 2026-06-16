---
title: PayPal Payflow Pro
description: PayPal Payflow Proをオンライン決済ソリューションとしてストアに設定する方法を説明します。
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/Ihjp0mA-r63ONIWgCpZFxi4rdt9cVowqPX1VyD4SRaQ
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 2264
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro ゲートウェイ（旧&#x200B;_Verisign_）は、米国、カナダ、オーストラリア、ニュージーランドのお客様が利用できます。 他のPayPalの支払い方法とは異なり、加盟店は、月額固定手数料に加えて、取引数に関係なく各取引に対して固定手数料が請求されます。

![PayPalでのチェックアウト &#x200B;](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2の要件：** <br/>
>2019年9月14日の時点で、ヨーロッパの銀行は[PSD2](../getting-started/compliance-payment-services-directive.md)の要件を満たさない支払いを拒否する可能性があります。PSD2に準拠するには、PayPal Payflow Proをサードパーティ製プラグインと統合する必要があります。詳しくは、「[3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/)」を参照してください。

## 要件定義

- [PayPal Business Account](https://www.paypal.com/webapps/mpp/how-to-sell-online) - PayPal Payflow Pro ゲートウェイは、PayPalの加盟店アカウントを加盟店web サイトにリンクし、ゲートウェイと加盟店アカウントの両方として機能します。

- 複数のAdobe CommerceおよびMagento Open Source web サイトを管理する場合は、各web サイトに対して個別のPayPal マーチャント アカウントが必要です。

## 顧客ワークフロー

1. **お客様はチェックアウトに行きます** - チェックアウト中、お客様はPayPal Payflow Proでの支払いを選択し、クレジットカード情報を入力します。 お客様は、個人のPayPal アカウントを持つ必要はありません。 ただし、加盟店の国によっては、顧客は個人のPayPal アカウントを使用して注文の支払いをおこなうことができます。
1. **お客様が注文を送信** – お客様が注文を送信すると、注文情報がPayPalに送信され、処理されます。 顧客がサイトのチェックアウトページを離れることはありません。
1. **PayPalは取引を完了します** – 注文が行われた時点で支払いが受け付けられます。 設定で指定した支払いアクションに応じて、販売注文または販売注文と請求書が作成されます。

## オンライン注文処理ワークフロー

1. **管理者がオンライン請求書を送信します** - ストア管理者がオンライン請求書を送信すると、対応するトランザクションと請求書が作成されます。
1. **PayPalはトランザクションを受信します** – 注文情報はPayPalに送信されます。 トランザクションと請求書のレコードが生成されます。 [PayPal マーチャント アカウント &#x200B;](https://manager.paypal.com/)のすべてのPayflow Pro Gateway トランザクションを表示できます。

>[!NOTE]
>
>PayPal Payflow Proでは、請求書の一部および返金はサポートされていません。

## PayPal アカウントの設定

1. [PayPal法人向けアカウント &#x200B;](https://manager.paypal.com/)にログインします。

1. PayPal Managerを使用して、次の設定で[&#x200B; ホスト型チェックアウトページ &#x200B;](https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager)を設定します。

   - **[!UICONTROL Choose your settings]**&#x200B;で、**[!UICONTROL Transaction Process Mode]**&#x200B;を`Live`に設定します。

   - **[!UICONTROL Display options on payment page]**&#x200B;で、**URLの解約メソッド**&#x200B;を`POST`に設定します。

   - **[!UICONTROL Billing Information]**&#x200B;で、必須フィールドと編集可能フィールドの両方に対して、カードセキュリティコード **[!UICONTROL CSC]**&#x200B;のチェックボックスを選択します。

   - **[!UICONTROL Payment Confirmation]**&#x200B;で、**[!UICONTROL Return URL Method]**&#x200B;を`POST`に設定します。

   - **[!UICONTROL Security Options]**&#x200B;で、次の設定を完了します。

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - **[!UICONTROL Customize]**&#x200B;を選択し、**[!UICONTROL Layout C]**&#x200B;を選択します。

     レイアウト Cにはクレジットカードとデビットカードのフィールドのみが表示され、サイトにフレーム化するか、スタンドアロンのポップアップとして使用できます。 サイズは490 x 565 ピクセルに固定され、エラーメッセージ用の余分なスペースが追加されています。 一部のシステムでは、この設定によって透過的なリダイレクトに関する問題が修正されます。

1. 設定が完了したら、**[!UICONTROL Save and Publish]**&#x200B;をクリックします。

1. PayPal Manager メニューで、**[!UICONTROL Account Administration]**&#x200B;を選択します。

1. **[!UICONTROL Manage Security]**&#x200B;で「**[!UICONTROL Transaction Settings]**」をクリックし、次の操作を行います。

   - **[!UICONTROL Allow reference transactions]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Confirm]**&#x200B;をクリックします。

     >[!NOTE]
     >
     >複数のCommerce Web サイトがある場合は、それぞれに個別のPayPal Payments Advanced アカウントを作成する必要があります。

1. 別のユーザーを設定する（PayPalで推奨）:

   - メインメニューの2行目で、**[!UICONTROL Manage Users]**&#x200B;をクリックします。

   - アカウントに別のユーザーを追加するには、**[!UICONTROL Add User]**&#x200B;をクリックします。 リンクは、「ユーザーを管理」タイトルのすぐ上にあります。

   - _[!UICONTROL Add User]_&#x200B;フォームの次のセクションで、必須フィールドに入力します。

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - **[!UICONTROL Update]**&#x200B;をクリックします。

1. 必ずPayPal アカウントからログアウトしてください。

## CommerceでのPayPal Payflow Proの設定

>[!TIP]
>
>いつでも&#x200B;**[!UICONTROL Save Config]**&#x200B;をクリックして、進行状況を保存します。

### 手順1：設定を開始する

この設定方法は、既存のPayPal アカウントを持っていることを前提としています。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Payment Methods]**&#x200B;を選択します。

1. Commerce インストールに複数のweb サイト、ストア、またはビューがある場合は、この設定を適用するストアビューに&#x200B;**[!UICONTROL Store View]**&#x200B;を設定します。

1. 「_[!UICONTROL Merchant Location]_」セクションで、ビジネスが存在する&#x200B;**[!UICONTROL Merchant Country]**&#x200B;を選択します。

   この設定は、設定に表示されるPayPal ソリューションの選択を決定します。

   ![&#x200B; マーチャント国](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. **[!UICONTROL PayPal Payment Gateways]** （必要な場合）を展開し、**[!UICONTROL Payflow Pro]**&#x200B;の&#x200B;**[!UICONTROL Configure]**&#x200B;をクリックします。

   ![設定 – Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### ステップ 2：必要なPayPal設定を完了する

![必要な設定 – PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. （オプション）を入力します。**[!UICONTROL Email Associated with your PayPal Merchant Account]**

   >[!IMPORTANT]
   >
   >メールアドレスでは、大文字と小文字が区別されます。 支払いを受け取るには、メールアドレスがPayPal加盟店アカウントで指定されたメールアドレスと一致している必要があります。

1. PayPal加盟店アカウントへのログインに使用する次のいずれかの資格情報を入力します。

   - **[!UICONTROL Partner]** - PayPal パートナーID。
   - **[!UICONTROL User]** - アカウントに1人以上のユーザーを設定する場合、この値はトランザクションの処理を許可されたユーザーのIDです。 ただし、追加のユーザーを設定していない場合、**[!UICONTROL USER]**&#x200B;の値は&#x200B;**[!UICONTROL Vendor]**&#x200B;と同じです。
   - **[!UICONTROL Vendor]** - アカウントに登録したときに作成されたマーチャントのログイン ID。

1. PayPal アカウントに関連付けられている&#x200B;**[!UICONTROL Password]**&#x200B;を入力します。

1. テスト トランザクションを実行するには、**[!UICONTROL Test Mode]**&#x200B;を`Yes`に設定します。

   サンドボックスで設定をテストする場合は、PayPalが推奨する[&#x200B; クレジットカード番号](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm)のみを使用します。 実稼動環境に移行する準備ができたら、設定に戻り、テストモードを`No`に設定します。

1. システムでプロキシサーバーを使用してPayPal システムへの接続を確立する場合は、**[!UICONTROL Use Proxy]**&#x200B;を`Yes`に設定し、次の操作を行います。

   - **[!UICONTROL Proxy Host]**&#x200B;のIP アドレスを入力してください。

   - **[!UICONTROL Proxy Port]**&#x200B;のポート番号を入力してください。

     プロキシは、サーバーファイアウォールがPayPal サーバーへの直接アクセスを禁止している場合に使用されます。 この場合、トラフィックを中継するためにサードパーティサーバーが使用されます。

1. **[!UICONTROL Enable this Solution]**&#x200B;を`Yes`に設定します。

1. [PayPal クレジット &#x200B;](paypal.md#paypal-credit-and-pay-later)を顧客に提供する場合は、**[!UICONTROL Enable PayPal Credit]**&#x200B;を`Yes`に設定します。

1. 顧客の支払い/クレジットカードの詳細を安全に保存する場合、顧客が毎回支払い情報を再入力する必要がないように、**[!UICONTROL Vault Enabled]**&#x200B;を`Yes`に設定します。

>[!NOTE]
>
>PayPal PayFlow Pro トランザクション ID （PNREF）は、12か月間の固定期間のリファレンストランザクションで使用できるようになりました。 有効期限が切れると、保存されたカードは表示されなくなり、再度追加する必要があります。

### ステップ 3:Advertising PayPal Credit / Advertising PayPal PayLaterの設定（オプション）

2.4.3 リリース以降、PayPal PayLaterは、PayPalを含むデプロイメントでサポートされています。 この機能により、買い物客は購入時に全額を支払うのではなく、隔週の分割で注文の支払いを行うことができます。 PayPal Credit エクスペリエンスは非推奨（廃止予定）です。

**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;を次のいずれかに設定します：

- `Yes` - Advertising PayPal PayLaterを設定するには
- `No` - Advertising PayPal クレジットを設定するには

#### Advertising PayPal Credit

1. **[!UICONTROL Advertise PayPal Credit]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![PayPal クレジットの広告](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. アカウント情報を取得するには、**[!UICONTROL Get Publisher ID from PayPal]**&#x200B;をクリックし、指示に従います。

1. **[!UICONTROL Publisher ID]**&#x200B;を入力します。

1. **[!UICONTROL Home Page]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![PayPal クレジットのホームページ設定の広告](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. ページにバナーを配置するには、**[!UICONTROL Display]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Position]**&#x200B;を次のいずれかに設定します：

   - `Header (center)`
   - `Sidebar (right)`

1. **[!UICONTROL Size]**&#x200B;を次のいずれかに設定します：

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. 残りのセクションを![拡張セレクター](../assets/icon-display-expand.png)展開し、ホームページ設定の前の手順を繰り返します。

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### PayPal PayLaterの広告

1. **[!UICONTROL Advertise PayPal PayLater]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Enable PayPal PayLater]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Home Page]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![PayPal クレジットのホームページ設定の広告](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. ページにバナーを配置するには、**[!UICONTROL Display]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Position]**&#x200B;を次のいずれかに設定します：

   - `Header (center)`
   - `Sidebar`

1. **[!UICONTROL Style Layout]**&#x200B;を次のいずれかに設定します：

   - `Text`
   - `Flex`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;のみの場合は、**[!UICONTROL Logo Type]**&#x200B;を次のいずれかに設定します。

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;のみの場合は、**[!UICONTROL Logo Position]**&#x200B;を次のいずれかに設定します。

   - `Left`
   - `Right`
   - `Top`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;のみの場合は、**[!UICONTROL Text Color]**&#x200B;を次のいずれかに設定します。

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;のみの場合は、**[!UICONTROL Text Size]**&#x200B;を次のいずれかに設定します。

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]**&#x200B;のみの場合は、**[!UICONTROL Ratio]**&#x200B;を次のいずれかに設定します。

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]**&#x200B;のみの場合は、**[!UICONTROL Color]**&#x200B;を次のいずれかに設定します。

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. 残りのセクションを![拡張セレクター](../assets/icon-display-expand.png)展開し、前の手順を繰り返します。

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### 手順4：基本設定を完了する

1. **[!UICONTROL Basic Settings - PayPal Payflow Pro]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![基本設定 – PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. 「**[!UICONTROL Title]**」に、チェックアウト時にPayPal Payflow Proを識別するタイトルを入力します。

   「_デビットカードまたはクレジットカード_」というタイトルを使用することをお勧めします。

1. 複数の支払い方法を提供している場合は、**[!UICONTROL Sort Order]**&#x200B;の数値を入力して、他の支払い方法と共に表示されるときにPayflow Proが表示される順序を決定します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. **[!UICONTROL Payment Action]**&#x200B;を次のいずれかに設定します：

   - `Authorization` – 購入を承認し、資金を保留します。 金額は、加盟店が獲得するまで引き落とされません。
   - `Sale` – 購入金額が承認され、お客様のアカウントから直ちに引き落とされます。

1. **[!UICONTROL Credit Card Settings]**&#x200B;の場合、ストアでの支払いに使用できるクレジットカードを選択します。

   複数のカードを選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら、それぞれのカードをクリックします。

   >[!NOTE]
   >
   >American Expressには追加契約が必要です。

### 手順5：詳細設定を完了する

1. **[!UICONTROL Advanced Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![詳細設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Payment Applicable From]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての[国](../getting-started/store-details.md#country-options)のお客様は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 Ctrl キー（PC）またはCommand キー（Mac）を押しながら、お客様が店舗で購入できる国をリストから選択します。

1. 支払いシステムとの通信をログファイルに書き込むには、**[!UICONTROL Debug Mode]**&#x200B;を`Yes`に設定します。

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの真正性検証を有効にするには、**[!UICONTROL Enable SSL Verification]**&#x200B;を`Yes`に設定します。

1. 顧客にCVV コードの入力を求めるには、**[!UICONTROL Require CVV Entry]**&#x200B;を`Yes`に設定します。

1. ストアの必要に応じて、次のセクションを完了します。

   - [CVVとAVSの設定](#cvv-and-avs-settings)
   - [決済レポート設定](#settlement-report-settings)
   - [フロントエンドエクスペリエンス設定](#frontend-experience-settings)

#### CVVとAVSの設定

Address Verification Systemが不一致を識別したときにトランザクションを拒否するタイミングを決定するには、様々なシナリオの処理方法を指定します。

1. **[!UICONTROL CVV and AVS Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![CVVおよびAVS設定 – PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. 不一致のストリートミスマッチに基づいてトランザクションを拒否するには、**[!UICONTROL AVS Street Does Not Match]**&#x200B;を`Yes`に設定します。

1. 一致しない郵便番号に基づいてトランザクションを拒否するには、**[!UICONTROL AVS Zip Does Not Match]**&#x200B;を`Yes`に設定します。

1. 一致しない国IDに基づいてトランザクションを拒否するには、**[!UICONTROL International AVS Indicator Does Not Match]**&#x200B;を`Yes`に設定します。

1. 一致しないCVV コードに基づいてトランザクションを拒否するには、**[!UICONTROL International Card Security Code Does Not Match]**&#x200B;を`Yes`に設定します。

#### 決済レポート設定

1. **[!UICONTROL Settlement Report Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![決済レポート設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL SFTP Credentials]**&#x200B;に対して、次の操作を行います。

   - PayPal Secure FTP Serverにサインアップしている場合は、次のSFTP ログイン資格情報を入力します。

      - ログイン
      - パスワード

   - サイトでExpress Checkoutを使用して本番稼働前にテストレポートを実行するには、**[!UICONTROL Sandbox Mode]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Custom Endpoint Hostname or IP Address]**&#x200B;を入力します。

     デフォルトでは、値は`reports.paypal.com`です。

   - レポートを保存する&#x200B;**[!UICONTROL Custom Path]**&#x200B;を入力します。

     デフォルトでは、値は`/ppreports/outgoing`です。

1. スケジュールに従ってレポートを生成するには、**[!UICONTROL Scheduled Fetching]**&#x200B;設定を完了します。

   - **[!UICONTROL Enable Automatic Fetching]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Schedule]**&#x200B;を次のいずれかに設定します：

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPalは、各レポートを45日間保持します。

   - レポートを生成する場合は、**[!UICONTROL Time of Day]**&#x200B;を時間、分、秒に設定します。

#### フロントエンドエクスペリエンス設定

フロントエンドエクスペリエンス設定を使用して、サイトに表示するPayPal ロゴを選択し、PayPal マーチャントページの外観をカスタマイズします。

1. **[!UICONTROL Frontend Experience Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![&#x200B; フロントエンドエクスペリエンス設定 – PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. ストアのPayPal ブロックに表示する&#x200B;**[!UICONTROL PayPal Product Logo]**&#x200B;を選択します。

   PayPalのロゴには4つのスタイルと2つのサイズがあります。

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal マーチャントページの外観をカスタマイズするには：

   - PayPal マーチャント ページに適用する&#x200B;**[!UICONTROL Page Style]**&#x200B;の名前を入力します。

      - `paypal` - PayPal ページスタイルを使用します。
      - `primary` - アカウントプロファイルで&#x200B;_primary_ スタイルとして識別したページスタイルを使用します。
      - `your_custom_value` - アカウント プロファイルで指定されたカスタム支払いページ スタイルを使用します。

   - **[!UICONTROL Header Image URL]**&#x200B;に、支払いページの左上隅に表示する画像のURLを入力します。 最大ファイルサイズは、幅750 ピクセル、高さ90 ピクセルです。

     >[!NOTE]
     >
     >PayPalでは、画像が安全な（https）サーバー上にあることをお勧めします。 それ以外の場合、ブラウザーは、_ページにセキュアな項目とセキュアでない項目の両方が含まれていることを警告する場合があります_。

   - ページの色を設定するには、次のそれぞれに`#`記号なしで6文字の16進数コードを入力します。

      - **[!UICONTROL Header Background Color]** - チェックアウト ページ ヘッダーの背景色。
      - **[!UICONTROL Header Border Color]** - ヘッダーの周囲の2 ピクセル境界の色。
      - **[!UICONTROL Page Background Color]** - チェックアウトページと、ヘッダーと支払いフォームの周囲の背景色。

### ステップ 6:PayPal Express Checkoutの基本設定を完了する

1. **[!UICONTROL Basic Settings - PayPal Express Checkout]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![Express チェックアウト基本設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Title]**&#x200B;に、チェックアウト時にこの支払い方法を識別するタイトルを入力します。

   各ストアビューのタイトルを&#x200B;_PayPal_&#x200B;に設定することをお勧めします。

1. 複数の支払い方法を提供している場合は、**[!UICONTROL Sort Order]**&#x200B;の数値を入力して、他の支払い方法と一緒に表示されるPayPal Express Checkoutの順序を決定します。

   この数字は他の支払い方法に関連しています。 （`0` = first, `1` = second, `2` = thirdなど）

1. **[!UICONTROL Payment Action]**&#x200B;を次のいずれかに設定します：

   - `Authorization` – 購入を承認し、資金を保留します。 金額は、加盟店が&#x200B;_獲得_&#x200B;するまで引き落とされません。
   - `Sale` – 購入金額が承認され、お客様のアカウントから直ちに引き落とされます。

1. 製品ページに&#x200B;_[!UICONTROL Check out with PayPal]_&#x200B;ボタンを表示するには、**[!UICONTROL Display on Product Details Page]**&#x200B;を`Yes`に設定します。

### 手順7:PayPal Express Checkoutの詳細設定を完了する

1. **[!UICONTROL Advanced Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![Express チェックアウトの詳細設定](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display on Shopping Cart]**&#x200B;を`Yes`に設定します。

1. **[!UICONTROL Payment Applicable From]**&#x200B;を次のいずれかに設定します：

   - `All Allowed Countries` - ストア設定で指定されたすべての国のお客様は、この支払い方法を使用できます。
   - `Specific Countries` – このオプションを選択すると、_[!UICONTROL Payment from Specific Countries]_&#x200B;リストが表示されます。 複数の国を選択するには、Ctrl キー（PC）またはCommand キー（Mac）を押しながら各項目をクリックします。

1. 支払いシステムとの通信をログファイルに書き込むには、**[!UICONTROL Debug Mode]**&#x200B;を`Yes`に設定します。

   >[!NOTE]
   >
   >PCI データセキュリティ基準に従い、クレジットカード情報はログファイルに記録されません。

1. ホストの真正性検証を有効にするには、**[!UICONTROL Enable SSL Verification]**&#x200B;を`Yes`に設定します。

1. PayPal サイトからの顧客注文の完全な概要を行項目ごとに表示するには、**[!UICONTROL Transfer Cart Line Items]**&#x200B;を`Yes`に設定します。

1. 注文レビューのために店舗に戻ることなく、PayPal サイトからトランザクションを完了できるようにするには、**[!UICONTROL Skip Order Review Step]**&#x200B;を`Yes`に設定します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

### 手順8:Google reCAPTCHAの追加

PayPal Payflow Pro チェックアウトをより適切に保護するには、Google reCAPTCHAを有効にします。 クリック可能なインターフェイスまたは非表示のチェックを使用してreCAPTCHAを実行し、顧客を検証するオプションが含まれています。 目に見えないオプションは、販売のコンバージョンを増やし、ストアを保護することをお勧めします。 詳しくは、[Google reCAPTCHA](../systems/security-google-recaptcha.md)を参照してください。
