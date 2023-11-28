---
title: 発送ラベルとパッケージの作成
description: 品目を注文でパッケージ化し、発送ラベルを作成する方法を説明します。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# 発送ラベルを作成

発送ラベルを作成するには、まず発送先のアカウントを設定して、ラベルをサポートする必要があります。 次に、プロンプトに従って、パッケージとその内容の説明を入力します。

発送ラベル情報を設定して注文を送信すると、Commerce は発送業者システムに接続し、注文を送信し、発送ラベルと追跡番号を受け取ります。 この出荷の出荷ラベルがシステムに存在する場合は、新しいラベルに置き換えられます。 ただし、既存のトラッキング番号は置き換えられません。 新しいトラッキング番号が既存の番号に追加されます。

## ステップ 1：輸送会社に連絡してください

始める前に、配送先のアカウントがラベルを処理するように設定されていることを確認してください。 一部の通信事業者は、アカウントに送料ラベルを追加するために追加料金を請求する場合があります。

店舗の配送ラベルを有効化するために使用する各配送業者に連絡してください。

各通信事業者が提供する指示に従って、送料ラベルのサポートをアカウントに追加します。

- **FedEx**  — 連絡先 [FedEx Web 統合サービス][1] アカウントのラベル印刷要件を確認するには、以下を実行します。
- **USPS**  — を参照してください。 [Web ツール API ポータル][4] Shipper Support Center で、ラベル印刷の資格情報を設定する方法を確認します。
- **UPS** — 連絡先 [UPS][2] をクリックして、お客様のアカウントが発送ラベルをサポートしていることを確認します。 発送ラベルを生成するには、UPS XML オプションを使用する必要があります。
- **DHL**  — 連絡先 [DHL e コマースソリューション][3] アカウントのラベル印刷要件を確認するには、以下を実行します。

## 手順 2：各通信事業者の設定を更新する

1. 次の項目を確認します。 [ストア情報](../getting-started/store-details.md#store-information) が完了しました。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択し、 **[!UICONTROL Shipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Origin]** セクションと設定 **[!UICONTROL Shipping Origin Address]**.

1. ラベル印刷に対して有効化された各通信事業者アカウントについて、以下の手順に従います。

### UPS 構成

ユナイテッド・パーセル・サービスは、国内外に出荷されます。 ただし、送料ラベルは、米国内からの出荷に対してのみ生成できます。

1. Adobe Analytics の _[!UICONTROL Sales]_セクションの左側のパネルで、「 」を選択します。**[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL UPS]** 」セクションに入力します。

1. UPS の確認 **[!UICONTROL Shipper Number]** が正しい。

   [ 発送担当番号 ] は、次の場合にのみ表示されます。 [!DNL United Parcel Service XML] が有効になっている。

1. クリック **[!UICONTROL Save Config]**.

### USPS 設定

The [!DNL United States Postal Service] は、国内でも国際でも出荷されます。

1. 次で続行： **[!UICONTROL Delivery Methods]** 設定、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL USPS]** 」セクションに入力します。

1. 次を確認します。 **[!UICONTROL Secure Gateway URL]** が正しい。

1. 次を入力します。 **[!UICONTROL Password]** USPS から提供されました。

1. 設定 **[!UICONTROL Size]** から `Large` 次のディメンションの値を入力します。

   - 長さ
   - 幅
   - 高さ
   - ガース

1. クリック **[!UICONTROL Save Config]**.

### FedEx 設定

FedEx は国内外の船です。 米国以外に位置する店舗では、国際出荷用の FedEx ラベルのみを作成できます。

{{beta2-updates}}

1. 次で続行： **[!UICONTROL Delivery Methods]** 設定、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL FedEx]** 」セクションに入力します。

1. 次の FedEx 資格情報が正しいことを確認します。

   - メートル番号
   - キー
   - パスワード

1. クリック **[!UICONTROL Save Config]**.

### DHL 設定

DHL は、国際配送サービスを提供します。

1. 次で続行： **[!UICONTROL Delivery Methods]** 設定、展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL DHL]** 」セクションに入力します。

1. 次を確認します。 **[!UICONTROL Gateway URL]** が正しい。

1. 次の資格情報が入力されていることを確認します。

   - アクセス ID
   - パスワード
   - アカウント番号

1. クリック **[!UICONTROL Save Config]**.

## 手順 3：発送ラベルの作成

### 方法 1：新しい出荷のラベルを作成します

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の順序を探し、レコードを開きます。

   注文のステータスは、次のいずれかである必要があります `Pending` または `Processing`.

1. 右上隅で、 **[!UICONTROL Ship]**.

1. 配送業者の要件に従って配送先情報を確認します。

1. 右下隅で、 **[!UICONTROL Create Shipping Label]** チェックボックス。

1. クリック **[!UICONTROL Submit Shipment]**.

1. パッケージ内の製品を追加または更新：

   - 注文からパッケージに製品を追加するには、 **[!UICONTROL Add Products]**. The _[!UICONTROL Quantity]_列には、パッケージで使用可能な製品の最大数が表示されます。

   - パッケージに追加する各製品のチェックボックスを選択し、 **[!UICONTROL Quantity]** それぞれの 次に、「 **[!UICONTROL Add Selected Product(s) to Package]**.

   - パッケージを追加するには、 **[!UICONTROL Add Package]**.

   - パッケージを削除するには、 **[!UICONTROL Delete Package]**.

   - オーダーをキャンセルするには、 **[!UICONTROL Cancel]**. 発送ラベルが作成されておらず、 _[!UICONTROL Create Shipping Label]_チェックボックスがオフになっている。

   >[!NOTE]
   >
   >デフォルト以外のパッケージタイプを使用した場合や、署名が必要な場合は、送料が顧客に請求した金額と異なる場合があります。 送料の違いは、あなたの店に反映されません。

1. クリック **[!UICONTROL OK]**.

   Commerce は、配送業者システムに接続し、注文を送信し、各パッケージの配送ラベルと追跡番号を受け取ります。

### 方法 2：既存の出荷のラベルを作成する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッドで注文を探し、発送フォームを開きます。

1. Adobe Analytics の _[!UICONTROL Shipping and Tracking Information]_セクションで、**[!UICONTROL Create Shipping Label]**.

1. 注文した製品を適切なパッケージに配布し、 **[!UICONTROL OK]**.

1. パッケージ情報を確認するには、 **[!UICONTROL Show Packages]**.

## 手順 4：ラベルを印刷する

発送ラベルはPDF形式で生成され、管理者から印刷できます。 各ラベルには、注文番号とパッケージ番号が含まれます。

>[!NOTE]
>
>各パッケージの個々の出荷注文が作成されるので、1 つの出荷に対して複数の出荷ラベルが受け取られる場合があります。

### 方法 1：出荷フォームからラベルを印刷する

1. 次の日： _管理サイドバー_&#x200B;次のいずれかのページに移動し、出荷レコードを探します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**  — グリッド内の順序を検索し、レコードを開きます。 左側のパネルで、を選択します。 **[!UICONTROL Shipments]**. 次に、出荷レコードを開きます。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**  — グリッド内の出荷を検索し、レコードを開きます。

1. PDFファイルをダウンロードするには、 _[!UICONTROL Shipping and Tracking]_フォームのセクションで、**[!UICONTROL Print Shipping Label]**.

   ブラウザーの設定に応じて、発送ラベルをブラウザーファイルから直接表示および印刷できます。PDF

   The _[!UICONTROL Print Shipping Label]_ボタンは、配送業者が出荷のラベルを生成した後にのみ表示されます。 ボタンがない場合は、**[!UICONTROL Create Shipping Label]**. このボタンは、Commerce が通信事業者からラベルを受け取った後に表示されます。

### 方法 2：複数の注文のラベルを印刷する

1. 次の日： _管理サイドバー_&#x200B;次のいずれかのページに移動し、印刷する注文または出荷を選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]**  — グリッドで、出荷ラベルを印刷する各注文のチェックボックスを選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**  — グリッドで、印刷するラベル付きの各出荷のチェックボックスを選択します。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Print Shipping Labels`.

1. クリック **[!UICONTROL Submit]**.

選択した注文に関連する出荷ごとに、出荷ラベルの完全なセットが印刷されます。

## 必要な通信事業者の設定

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージの種類は通信事業者と方法によって異なります。 各通信事業者のデフォルトのパッケージタイプが最初に選択されます。 USPS では、国内出荷にはパッケージタイプは必要ありません。 |
| [!UICONTROL Customs Value] | （国際出荷のみ）国際出荷の内容の宣言価格又は販売価格。 |
| [!UICONTROL Total Weight] | パッケージに追加されたすべての製品の合計重みが自動的に計算されます。 この値は、手動で変更し、ポンドまたはキログラムで入力することもできます。 |
| [!UICONTROL Length, Width, Height] | （オプション）パッケージのディメンションは、カスタムパッケージに対してのみ使用されます。 測定単位は、インチまたはセンチメートルで指定できます。<br/><br/>**[!UICONTROL Not Required]**：配送業者から店舗に配送の確認が送信されません。<br/><br/>**[!UICONTROL No Signature]**：受信者の署名がない配信確認が、配送業者によってストアに送信されます。<br/><br/>**[!UICONTROL Signature Required]**：配送業者は受信者の署名を取得し、店舗に印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Direct]**: （FedEx のみ）FedEx は配信アドレスの人から署名を取得します。 パッケージに署名できる人がいない場合は、通信事業者は別の時点でパッケージの配信を試みます。<br/><br/>**[!UICONTROL Indirect]**: (FedEx Residential Deliveries Only)FedEx は、配信アドレスで誰か（おそらく隣人か建物の管理者）の署名を取得します。 受信者は、署名された FedEx ドアタグを残して、誰も署名することなく、パッケージを残すことを許可できます。<br/><br/>**[!UICONTROL Contents]**: （USPS のみ）パッケージの次のいずれかの説明を選択します。<br/> — ギフト<br/> — ドキュメント<br/> — 商用サンプル<br/>・返品品<br/> — 商品<br/> — その他&#x200B;<br/><br/>**[!UICONTROL Explanation]**: （USPS のみ）パッケージの内容に関する詳細な説明。<br/><br/>**[!UICONTROL Adult Required]**：配送業者は、成人の受信者の署名を取得し、店舗に印刷されたコピーを提供します。 |

{style="table-layout:auto"}

## パッケージの作成

The _[!UICONTROL Create Packages]_ウィンドウは、発送ラベルの作成を選択すると表示されます。 最初のパッケージの設定は、直ちに開始できます。

### パッケージの設定

>[!NOTE]
>
>デフォルト以外の値を [!UICONTROL Type] または、署名の確認を求める場合、出荷の価格は、お客様に請求した価格と異なる場合があります。

1. 出荷済製品のリストを表示し、パッケージに追加するには、 **[!UICONTROL Add Products]**.

   - 製品と数量を指定します。

     The _[!UICONTROL Qty]_列には、追加できる最大数量が表示されます。 最初のパッケージの場合、番号は出荷される製品の合計数量です。

   - 製品をパッケージに追加するには、 **[!UICONTROL Add Selected Product(s) to Package]**.

1. パッケージを追加するには、 **[!UICONTROL Add Package]**.

   複数のパッケージを追加し、同時に編集できます。

1. パッケージを削除するには、 **[!UICONTROL Delete Package]**.

製品をパッケージに追加した後は、数量を直接編集することはできません。

### 数量を増やす

1. クリック **[!UICONTROL Add Selection]**.

1. 追加の数量を入力します。

   この番号は、パッケージ内の製品の前の数量に追加されます。

### 数量を減らす

1. パッケージから製品を削除します。

1. クリック **[!UICONTROL Add Selection]**.

1. 小さい新しい値を入力します。

### 発送ラベルを生成

すべての製品を配布した後、使用するパッケージの合計数は、リストの最後のパッケージの数と同じになります。 The _OK_ のボタンは、出荷されたすべての項目がパッケージに配布され、必要な情報がすべて完了するまで無効になります。

ラベルを生成するには、 **[!UICONTROL OK]**.

次をクリックできます。 **[!UICONTROL Cancel]** をクリックして、必要に応じてプロセスを停止します。 パッケージは保存されず、発送ラベルの処理がキャンセルされます。

### フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージのタイプを指定します。 定義済みの値の 1 つを選択します。 使用可能なパッケージの種類は、配送業者ごとに異なります。 「パッケージの作成」ポップアップウィンドウが開くと、配送業者のデフォルトのパッケージが「タイプ」フィールドに表示されます。 輸送業者が設計していないパッケージを選択する場合は、パッケージの寸法を入力する必要があります。 DHL、FedEx、UPS 出荷用に作成された出荷ラベルの場合、「商品のタイプ」フィールドはに設定されます。 `Merchandise`. USPS の場合、フィールドには _内容_ フィールド _[!UICONTROL Create Packages]_ウィンドウ |
| [!UICONTROL Total Weight] | パッケージの合計重み。 「 」フィールドには、パッケージ内の製品の総重みが事前に設定されます。 単位は、ポンドまたはキログラムに設定できます。 |
| [!UICONTROL Length] | パッケージの長さ、整数、および浮動小数点数。 カスタムパッケージタイプを使用すると、「 」フィールドが有効になります。 単位は、インチまたはセンチに設定できます。 |
| [!UICONTROL Width] | パッケージの幅、整数、および浮動小数点数です。 カスタムパッケージタイプを使用すると、「 」フィールドが有効になります。 測定単位は、「高さ」フィールドの横にあるドロップダウンメニューを使用して指定できます。インチからセンチの間で選択します。 |
| [!UICONTROL Height] | パッケージの高さ、整数、および浮動小数点数です。 カスタムパッケージタイプを使用すると、「 」フィールドが有効になります。 測定単位は、「高さ」フィールドの横にあるドロップダウンメニューを使用して指定できます。インチからセンチの間で選択します。 |
| [!UICONTROL Signature] | 配信の確認を定義します。 オプション：<br/><br/>**[!UICONTROL Not Required]**：配信確認レターは送信されません。<br/><br/>**[!UICONTROL No Signature]**：受信者の署名のない配信確認書が送信されます。<br/><br/>**[!UICONTROL Signature Required]**：配送業者が受信者の署名を取得し、その印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Adult Required]**：配送業者は、成人の受信者の署名を取得し、その印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Direct (FedEx only)]**:FedEx は配信アドレスの担当者から署名を取得し、パッケージに署名できるユーザーがいない場合は配信を再試行します。<br/><br/>**[!UICONTROL Indirect (FedEx only)]**:FedEx は、次の 3 つの方法のいずれかで署名を取得します。<br/>(1) 配送先の誰かから <br/>(2) 隣人、建物管理人その他の住所の者からの，又は <br/>(3) 受信者は、誰も存在しないで、パッケージのリリースを承認する署名済みの FedEx ドアタグを残すことができます。 住宅向けの配信にのみ使用できます。 出荷方法によっては、オプションが少し異なる場合があります。 最新の情報については、配送業者のリソースを参照してください。 |
| [!UICONTROL Contents] | （USPS 出荷のみ可能）パッケージの内容の説明。 オプション： `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （USPS 出荷のみ）パッケージの内容に関する詳細な説明。 |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
