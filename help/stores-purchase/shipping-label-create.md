---
title: 出荷ラベルおよびパッケージの作成
description: 注文で品目をパッケージ化する方法と、出荷ラベルを作成する方法について説明します。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1889'
ht-degree: 0%

---

# 配送ラベルの作成

配送ラベルを作成するには、まずラベルをサポートする配送業者アカウントを設定する必要があります。 次に、プロンプトに従って、パッケージとそのコンテンツの説明を入力します。

配送ラベル情報を設定して注文を送信すると、Commerceは配送業者システムに接続し、注文を送信し、配送ラベルとトラッキング番号を受け取ります。 この出荷の出荷ラベルがシステムに存在する場合は、新しい出荷ラベルに置き換えられます。 ただし、既存のトラッキング番号は置換されません。 既存の追跡番号に新しい追跡番号が追加されます。

## 手順 1：配送業者に連絡する

開始する前に、配送アカウントがラベルを処理するように設定されていることを確認します。 一部の配送業者は、アカウントに配送ラベルを追加するために追加料金を請求する場合があります。

店舗の配送ラベルを有効化するために使用する各通信事業者に連絡してください。

各通信事業者の指示に従って、お使いのアカウントに配送ラベルのサポートを追加します。

- **FedEx**  – 連絡先 [FedEx Web Integration Services][1] アカウントのラベル印刷要件について説明します。
- **USPS**  – を参照してください。 [Web ツール API ポータル][4] ラベル印刷資格情報の設定方法については、「荷主サポートセンター」を参照してください。
- **UPS** – 連絡先 [UPS][2] お使いのアカウントが配送ラベルをサポートしていることを確認します。 出荷ラベルを生成するには、UPS XML オプションを使用する必要があります。
- **DHL**  – 連絡先 [DHL e コマースソリューション][3] アカウントのラベル印刷要件について説明します。

## 手順 2：各通信事業者の設定の更新

1. 次のことを確認します [ストア情報](../getting-started/store-details.md#store-information) が完了しました。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択して、 **[!UICONTROL Shipping Settings]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Origin]** セクション化と設定 **[!UICONTROL Shipping Origin Address]**.

1. ラベル印刷用に有効にする通信事業者アカウントごとに、以下の手順に従います。

### UPS の構成

United Parcel Service は、国内および海外の両方で出荷されます。 ただし、配送ラベルを生成できるのは、米国内の配送に対してのみです。

1. が含まれる _[!UICONTROL Sales]_左側のパネルの「」セクションで、**[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL UPS]** セクション。

1. UPS の確認 **[!UICONTROL Shipper Number]** は正しいです。

   荷主番号は、次の場合にのみ表示されます [!DNL United Parcel Service XML] が有効になっています。

1. クリック **[!UICONTROL Save Config]**.

### USPS の構成

この [!DNL United States Postal Service] 国内外を問わず出荷しています。

1. 継続#セツゾク# **[!UICONTROL Delivery Methods]** 設定、展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL USPS]** セクション。

1. を確認します **[!UICONTROL Secure Gateway URL]** は正しいです。

1. を入力 **[!UICONTROL Password]** usps からお客様に提供

1. を設定 **[!UICONTROL Size]** 対象： `Large` さらに、次のディメンションの値を入力します。

   - 長さ
   - 幅
   - 高さ
   - 周囲

1. クリック **[!UICONTROL Save Config]**.

### FedEx 設定

国内外の FedEx 船。 米国以外の店舗では、国際配送にのみ FedEx ラベルを作成できます。

1. 継続#セツゾク# **[!UICONTROL Delivery Methods]** 設定、展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL FedEx]** セクション。

1. 次の FedEx 認証情報が正しいことを確認します。

   - メートル番号
   - キー
   - パスワード

1. クリック **[!UICONTROL Save Config]**.

### DHL 設定

DHL は国際配送サービスを提供しています。

1. 継続#セツゾク# **[!UICONTROL Delivery Methods]** 設定、展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL DHL]** セクション。

1. を確認します **[!UICONTROL Gateway URL]** は正しいです。

1. 次の資格情報が完全であることを確認します。

   - アクセス ID
   - パスワード
   - アカウント番号

1. クリック **[!UICONTROL Save Config]**.

## 手順 3：配送ラベルの作成

### 方法 1：新規出荷のラベルの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を検索し、レコードを開きます。

   注文のステータスは次のいずれかである必要があります `Pending` または `Processing`.

1. 右上隅のをクリックします。 **[!UICONTROL Ship]**.

1. 配送業者の要件に従って配送情報を確認します。

1. 右下隅にあるを選択します **[!UICONTROL Create Shipping Label]** チェックボックス。

1. クリック **[!UICONTROL Submit Shipment]**.

1. パッケージ内の製品を追加または更新：

   - 注文からパッケージに製品を追加するには、 **[!UICONTROL Add Products]**. この _[!UICONTROL Quantity]_列には、パッケージで使用できる製品の最大数が表示されます。

   - パッケージに追加する各製品のチェックボックスを選択し、 **[!UICONTROL Quantity]** 各。 次に、 **[!UICONTROL Add Selected Product(s) to Package]**.

   - パッケージを追加するには、をクリックします **[!UICONTROL Add Package]**.

   - パッケージを削除するには、をクリックします **[!UICONTROL Delete Package]**.

   - 注文をキャンセルするには、をクリックします **[!UICONTROL Cancel]**. 出荷ラベルが作成されず、 _[!UICONTROL Create Shipping Label]_チェックボックスがオフになっています。

   >[!NOTE]
   >
   >デフォルト以外のパッケージタイプを使用する場合や、署名が必要な場合、送料はお客様が請求した金額と異なる場合があります。 送料の違いはストアには反映されません。

1. クリック **[!UICONTROL OK]**.

   Commerceは配送業者システムに接続し、注文を送信し、各パッケージの配送ラベルとトラッキング番号を受け取ります。

### 方法 2：既存の出荷のラベルの作成

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッドで注文を見つけて、配送フォームを開きます。

1. が含まれる _[!UICONTROL Shipping and Tracking Information]_セクションで、をクリック&#x200B;**[!UICONTROL Create Shipping Label]**.

1. 注文した製品を適切なパッケージに配布し、 **[!UICONTROL OK]**.

1. パッケージ情報を確認するには、をクリックします **[!UICONTROL Show Packages]**.

## 手順 4：ラベルを印刷する

配送ラベルはPDF形式で生成され、管理者が印刷できます。 各ラベルには、注文番号とパッケージ番号が含まれます。

>[!NOTE]
>
>1 つのパッケージに対して個別の出荷注文が作成されるため、1 つの出荷に対して複数の出荷ラベルが受け取られる場合があります。

### 方法 1：出荷フォームからのラベルの印刷

1. 日 _管理者サイドバー_&#x200B;以下のいずれかのページに移動して、出荷レコードを見つけます。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - グリッド内の順序を見つけて、レコードを開きます。 左パネルで、を選択します。 **[!UICONTROL Shipments]**. 次に、出荷レコードを開きます。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**  – 出荷をグリッドで検索し、レコードを開きます。

1. PDFファイルをダウンロードするには、 _[!UICONTROL Shipping and Tracking]_フォームのセクションで、**[!UICONTROL Print Shipping Label]**.

   お使いのブラウザの設定に応じて、PDFファイルから直接ラベルを表示して印刷することができます。

   この _[!UICONTROL Print Shipping Label]_ボタンは、運送業者が出荷のラベルを生成した後にのみ表示されます。 ボタンがない場合は、**[!UICONTROL Create Shipping Label]**. このボタンは、Commerceが通信事業者からラベルを受け取った後に表示されます。

### 方法 2：複数注文のラベルを印刷する

1. 日 _管理者サイドバー_&#x200B;以下のいずれかのページに移動し、印刷する注文または出荷を選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - グリッドで、出荷ラベルを印刷する各注文のチェックボックスを選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - グリッドで、ラベルを印刷する各出荷のチェックボックスを選択します。

1. を **[!UICONTROL Actions]** コントロール先 `Print Shipping Labels`.

1. クリック **[!UICONTROL Submit]**.

選択した注文に関連する出荷ごとに、出荷ラベルの完全なセットが印刷されます。

## 必須の通信事業者設定

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージタイプは、キャリアと方法によって異なります。 各通信事業者のデフォルトのパッケージタイプは、最初に選択されます。 USPS は国内出荷用のパッケージタイプを必要としません。 |
| [!UICONTROL Customs Value] | （国際配送の場合のみ）国際配送のコンテンツの宣言値または販売価格。 |
| [!UICONTROL Total Weight] | パッケージに追加されたすべての製品の合計重量は自動的に計算されます。 値を手動で変更して、ポンドまたはキログラムとして入力することもできます。 |
| [!UICONTROL Length, Width, Height] | （オプション）パッケージディメンションは、カスタムパッケージにのみ使用されます。 計測単位はインチまたはセンチメートルで指定できます。<br/><br/>**[!UICONTROL Not Required]**：配送の確認が配送業者によってストアに送信されません。<br/><br/>**[!UICONTROL No Signature]**：受信者の署名のない配信確認は、配送業者によってストアに送信されます。<br/><br/>**[!UICONTROL Signature Required]**：配送業者が受信者の署名を取得し、印刷されたコピーをストアに提供します。<br/><br/>**[!UICONTROL Direct]**: （FedEx のみ） FedEx は、配信アドレスのユーザーから署名を取得します。 パッケージに署名できる人がいない場合、通信事業者は別の時点でパッケージの配信を試みます。<br/><br/>**[!UICONTROL Indirect]**: （FedEx 住宅用配信のみ） FedEx は、配信アドレスの誰か（おそらく隣人またはビル管理者）の署名を取得します。 受信者は、署名済みの FedEx ドアタグを残して、誰も署名せずにパッケージを残すことを許可できます。<br/><br/>**[!UICONTROL Contents]**:（USPS のみ）パッケージの説明として、以下のいずれかを選択します。<br/>- ギフト<br/>- ドキュメント<br/> – 商用サンプル<br/>・返品返品<br/>・商品<br/> – その他&#x200B;<br/><br/>**[!UICONTROL Explanation]**:（USPS のみ）パッケージコンテンツの詳細な説明。<br/><br/>**[!UICONTROL Adult Required]**：配送業者が成人受信者の署名を取得し、印刷されたコピーを店舗に提供します。 |

{style="table-layout:auto"}

## パッケージの作成

この _[!UICONTROL Create Packages]_ウィンドウが表示されるのは、出荷ラベルの作成を選択した場合です。 最初のパッケージの設定をすぐに開始できます。

### パッケージの設定

>[!NOTE]
>
>にデフォルト以外の値を選択した場合、 [!UICONTROL Type] または、署名確認を要求することを選択すると、出荷の価格は、お客様に請求したものとは異なる場合があります。

1. 出荷済み製品の一覧を表示してパッケージに追加するには、 **[!UICONTROL Add Products]**.

   - 製品と数量を指定します。

     この _[!UICONTROL Qty]_列には、追加できる最大数量が表示されます。 1 つ目のパッケージの場合、この数値は出荷される製品の合計数量です。

   - 製品をパッケージに追加するには、 **[!UICONTROL Add Selected Product(s) to Package]**.

1. パッケージを追加するには、をクリックします **[!UICONTROL Add Package]**.

   複数のパッケージを追加し、同時に編集できます。

1. パッケージを削除するには、をクリックします **[!UICONTROL Delete Package]**.

製品をパッケージに追加した後で、数量を直接編集することはできません。

### 数量を増やす

1. クリック **[!UICONTROL Add Selection]**.

1. 追加数量を入力します。

   この番号は、パッケージ内の以前の製品数量に追加されます。

### 数量を減らす

1. パッケージから製品を削除します。

1. クリック **[!UICONTROL Add Selection]**.

1. 新しい小さい値を入力します。

### 出荷ラベルの生成

すべての製品を配布すると、使用するパッケージの合計数は、リスト内の最後のパッケージの数と等しくなります。 この _OK_ ボタンは、すべての出荷品目がパッケージに配布され、必要な情報がすべて完了するまで無効になります。

ラベルを生成するには、をクリックします **[!UICONTROL OK]**.

次のいずれかをクリックできます。 **[!UICONTROL Cancel]** 必要に応じて、プロセスを停止します。 パッケージは保存されず、出荷ラベル処理がキャンセルされます。

### フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージのタイプを指定します。 定義済みの値の 1 つを選択します。 使用可能なパッケージタイプは、配送業者ごとに異なります。 パッケージを作成ポップアップウィンドウが開くと、配送業者のデフォルトのパッケージが「タイプ」フィールドに表示されます。 配送業者によって設計されていないパッケージを選択する場合は、パッケージのサイズを入力する必要があります。 DHL、FedEx および UPS 出荷用に作成された出荷ラベルの場合、「商品タイプ」フィールドは次のように設定されます `Merchandise`. USPS の場合、このフィールドには、 _目次_ のフィールド _[!UICONTROL Create Packages]_ウィンドウ。 |
| [!UICONTROL Total Weight] | パッケージの合計重量。 このフィールドには、パッケージ内の製品の合計重量が事前に入力されています。 測定単位は、ポンドまたはキログラムに設定できます。 |
| [!UICONTROL Length] | パッケージの長さ、整数および浮動小数点数。 カスタムパッケージタイプを使用すると、このフィールドが有効になります。 単位はインチまたはセンチメートルに設定できます。 |
| [!UICONTROL Width] | パッケージの幅、整数、浮動小数点数。 カスタムパッケージタイプを使用すると、このフィールドが有効になります。 計測単位は、[ 高さ ] フィールドの隣にあるドロップダウン メニューを使用して指定できます。インチとセンチメートルの間で選択します。 |
| [!UICONTROL Height] | パッケージの高さ、整数および浮動小数点数。 カスタムパッケージタイプを使用すると、このフィールドが有効になります。 計測単位は、[ 高さ ] フィールドの隣にあるドロップダウン メニューを使用して指定できます。インチとセンチメートルの間で選択します。 |
| [!UICONTROL Signature] | 配信の確認を定義します。 オプション：<br/><br/>**[!UICONTROL Not Required]**：配信確認のレターが送信されません。<br/><br/>**[!UICONTROL No Signature]**：受信者に署名されていない配信確認書が送信されます。<br/><br/>**[!UICONTROL Signature Required]**：配送業者が受信者の署名を取得し、印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Adult Required]**：配送業者が成人受信者の署名を取得し、印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Direct (FedEx only)]**:FedEx は、配信アドレスに到達したユーザーから署名を取得し、パッケージに署名できるユーザーがいない場合は配信を再試行します。<br/><br/>**[!UICONTROL Indirect (FedEx only)]**:FedEx は、次の 3 つの方法のいずれかで署名を取得します。<br/>（1）引き渡し先住所の誰かから； <br/>（2）隣人、建物の管理者その他の住所の者から、または <br/>（3）受取人は、パッケージのリリースを承認する署名済み FedEx ドアタグを誰も出席せずに残すことができます。 居住地での配信にのみ使用できます。 オプションは、配送方法によって若干異なる場合があります。 最新の情報については、配送業者のリソースを参照してください。 |
| [!UICONTROL Contents] | （USPS 出荷の場合のみ使用可能）パッケージコンテンツの説明。 オプション： `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （USPS 出荷のみ）パッケージコンテンツの詳細な説明。 |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
