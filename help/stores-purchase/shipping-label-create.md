---
title: 配送ラベルとパッケージの作成
description: 注文で商品をパッケージ化し、配送ラベルを作成する方法を説明します。
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: ca9114db6ab79e7edee6d9be4ce0c8f79b8c793d
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 0%

---

# 配送ラベルの作成

配送ラベルを作成するには、最初にラベルをサポートするように配送業者アカウントを設定する必要があります。 次に、プロンプトに従って、パッケージとその内容の説明を入力します。

配送ラベル情報を設定して注文を送信すると、Commerceは配送業者システムに接続して注文を送信し、配送ラベルと追跡番号を受け取ります。 この出荷用の出荷ラベルがシステムに存在する場合は、新しいラベルに置き換えられます。 ただし、既存のトラッキング番号は置き換えられません。 新しい追跡番号が既存の追跡番号に追加されます。

## ステップ 1：配送業者に連絡する

始める前に、輸送口座がラベルを処理するように設定されていることを確認してください。 一部の配送業者は、送料を追加料金で請求して送料ラベルをアカウントに追加する場合があります。

ストアの配送ラベルを有効にするために使用する各キャリアにお問い合わせください。

各キャリアの指示に従って、お客様のアカウントに配送ラベルのサポートを追加してください。

- **FedEx** - アカウントのラベル印刷要件について詳しくは、[FedEx Web Integration Services](https://www.fedex.com/en-us/api/get-support.html)にお問い合わせください。
- **USPS** - ラベル印刷資格情報の設定方法については、[USPS ポータル ](https://developers.usps.com/)を参照してください。
- **UPS**- [UPS](https://www.ups.com/us/en/support/contact-us.page)に連絡して、お客様のアカウントが配送ラベルをサポートしていることを確認してください。 配送ラベルを生成するには、UPS XML オプションを使用する必要があります。
- **DHL** - アカウントのラベル印刷要件について詳しくは、[DHL e コマースソリューション ](https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html)にお問い合わせください。

## 手順2：各キャリアの設定を更新する

1. [ ストア情報](../getting-started/store-details.md#store-information)が完了していることを確認してください。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Shipping Settings]**&#x200B;を選択します。

1. **[!UICONTROL Origin]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL Shipping Origin Address]**&#x200B;を設定します。

1. ラベル印刷用にアクティベートされている各キャリアアカウントについて、次の手順に従います。

### UPS設定

United Parcel Serviceは国内外の両方で出荷しています。 ただし、配送ラベルは、米国内から発送された配送に対してのみ生成できます。

1. 左側のパネルの「_[!UICONTROL Sales]_」セクションで、**[!UICONTROL Delivery Methods]**を選択します。

1. **[!UICONTROL UPS]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. UPS **[!UICONTROL Shipper Number]**&#x200B;が正しいことを確認してください。

   お客様の配送人番号は、[!DNL United Parcel Service XML]が有効になっている場合にのみ表示されます。

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

### USPS設定

[!DNL United States Postal Service]は国内外の両方に出荷されます。

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. **[!UICONTROL Delivery Methods]**&#x200B;設定を続行して、**[!UICONTROL USPS]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL USPS Type]**&#x200B;を`USPS Rest APIs`または`USPS Web Tools API`として選択します。

   >[!NOTE]
   >
   >USPSはUSPS Web Tools APIをサポートしなくなりました。

1. **[!UICONTROL Secure Gateway URL]**&#x200B;が正しいことを確認します。

1. 選択した&#x200B;**[!UICONTROL USPS Type]**&#x200B;に基づいて、次の設定が完了していることを確認します。

   USPS REST APIを使用している場合：
   - Consumer Key
   - Consumer Secret
   - 価格オプション
   - アカウントタイプ
   - アカウント番号
   - 顧客登録ID （CRID）
   - メーラー識別子（MID）
   - マニフェスト MID
   - AES/ITN

   USPS Web Tools APIを使用している場合：
   - ユーザーId
   - パスワード

1. **[!UICONTROL Size]**&#x200B;を`Large`に設定し、次のディメンションの値を入力します。

   - 長さ
   - 幅
   - 高さ
   - Girth

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

### FedEx設定

FedExは国内外でサービスを提供。 米国外の店舗では、国際配送にのみFedEx ラベルを作成できます。

1. **[!UICONTROL Delivery Methods]**&#x200B;設定を続行して、**[!UICONTROL FedEx]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. 次のFedEx資格情報が正しいことを確認します。

   - メーター番号
   - キー
   - パスワード

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

### DHL設定

DHLは国際配送サービスを提供しています。

1. **[!UICONTROL Delivery Methods]**&#x200B;設定を続行して、**[!UICONTROL DHL]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL DHL Type]**&#x200B;を`DHL REST`または`DHL XML`として選択します。

1. **[!UICONTROL DHL Type]**&#x200B;の選択に基づいて、次の資格情報が完了していることを確認します。

   - アクセス ID
   - パスワード
   - アカウント番号
   - API キー
   - API シークレット

1. **[!UICONTROL Save Config]**&#x200B;をクリックします。

## ステップ 3：配送ラベルの作成

### 方法1：新しい出荷用のラベルを作成する

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;に移動します。

1. グリッドで注文を検索し、レコードを開きます。

   注文のステータスは`Pending`または`Processing`である必要があります。

1. 右上隅の「**[!UICONTROL Ship]**」をクリックします。

1. 配送業者の要件に従って配送情報を確認します。

1. 右下隅の「**[!UICONTROL Create Shipping Label]**」チェックボックスを選択します。

1. **[!UICONTROL Submit Shipment]**&#x200B;をクリックします。

1. パッケージ内の製品の追加または更新：

   - 注文からパッケージに製品を追加するには、**[!UICONTROL Add Products]**&#x200B;をクリックします。 _[!UICONTROL Quantity]_列には、パッケージで使用可能な製品の最大数が表示されます。

   - パッケージに追加する各製品のチェックボックスを選択し、それぞれの&#x200B;**[!UICONTROL Quantity]**&#x200B;を入力します。 次に、**[!UICONTROL Add Selected Product(s) to Package]**&#x200B;をクリックします。

   - パッケージを追加するには、**[!UICONTROL Add Package]**&#x200B;をクリックします。

   - パッケージを削除するには、**[!UICONTROL Delete Package]**&#x200B;をクリックします。

   - 注文をキャンセルするには、**[!UICONTROL Cancel]**&#x200B;をクリックします。 配送ラベルが作成されず、_[!UICONTROL Create Shipping Label]_チェックボックスがオフになります。

   >[!NOTE]
   >
   >デフォルト以外のパッケージタイプを使用する場合、または署名が必要な場合、送料はお客様が請求したものとは異なる場合があります。 送料の違いは店舗には反映されません。

1. **[!UICONTROL OK]**&#x200B;をクリックします。

   Commerceは、配送会社システムに接続して注文を送信し、各パッケージの配送ラベルと追跡番号を受け取ります。

### 方法2：既存の出荷のラベルを作成する

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**に移動します。

1. グリッドで注文を見つけて、配送フォームを開きます。

1. _[!UICONTROL Shipping and Tracking Information]_セクションで、**[!UICONTROL Create Shipping Label]**をクリックします。

1. 注文した製品を適切なパッケージに配布し、**[!UICONTROL OK]**&#x200B;をクリックします。

1. パッケージ情報を確認するには、**[!UICONTROL Show Packages]**&#x200B;をクリックします。

## 手順4：ラベルの印刷

配送ラベルはPDF形式で生成され、管理者から印刷できます。 各ラベルには、注文番号とパッケージ番号が含まれています。

>[!NOTE]
>
>各パッケージに対して個別の出荷注文が作成されるため、1回の出荷に対して複数の配送ラベルが届く場合があります。

### 方法1：出荷フォームからラベルを印刷する

1. _管理者サイドバー_&#x200B;で、次のいずれかのページに移動し、出荷記録を探します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - グリッド内の注文を検索し、レコードを開きます。 左側のパネルで、**[!UICONTROL Shipments]**&#x200B;を選択します。 次に、出荷レコードを開きます。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - グリッドで出荷を検索し、レコードを開きます。

1. PDF ファイルをダウンロードするには、フォームの&#x200B;_[!UICONTROL Shipping and Tracking]_セクションに移動し、**[!UICONTROL Print Shipping Label]**をクリックします。

   ブラウザーの設定に応じて、PDF ファイルから直接出荷ラベルを表示および印刷できます。

   _[!UICONTROL Print Shipping Label]_ボタンは、配送業者が出荷のラベルを生成した後にのみ表示されます。 ボタンが見つからない場合は、**[!UICONTROL Create Shipping Label]**をクリックします。 このボタンは、Commerceが通信事業者からラベルを受け取った後に表示されます。

### 方法2：複数注文のラベルを印刷する

1. _管理者サイドバー_&#x200B;で、次のいずれかのページに移動し、印刷する注文または出荷を選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - グリッドで、印刷する出荷ラベルが含まれている各注文のチェックボックスを選択します。

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - グリッドで、印刷するラベルを含む各出荷のチェックボックスを選択します。

1. **[!UICONTROL Actions]** コントロールを`Print Shipping Labels`に設定します。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

選択した注文に関連する各出荷に対して、出荷ラベルの完全なセットが印刷されます。

## 必要なキャリア設定

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージタイプは、キャリアと方法によって異なります。 各キャリアのデフォルトパッケージタイプは、最初に選択されます。 USPSは、国内配送にパッケージタイプを必要としません。 |
| [!UICONTROL Customs Value] | （国際配送のみ）国際配送の内容の宣言価値または販売価格。 |
| [!UICONTROL Total Weight] | パッケージに追加されたすべての製品の合計重量は、自動的に計算されます。 値は手動で変更し、ポンドまたはキログラムとして入力することもできます。 |
| [!UICONTROL Length, Width, Height] | （オプション）パッケージディメンションは、カスタムパッケージにのみ使用されます。 単位はインチまたはセンチメートルで指定できます。<br/><br/>**[!UICONTROL Not Required]**：配送業者が店舗に配達確認を送信しません。<br/><br/>**[!UICONTROL No Signature]**：受信者の署名がない配達確認は、配送業者が店舗に送信します。<br/><br/>**[!UICONTROL Signature Required]**：配送業者は受信者の署名を取得し、印刷されたコピーを店舗に提供します。<br/><br/>**[!UICONTROL Direct]**: （FedExのみ） FedExは配送先住所で誰かから署名を取得します。 パッケージに署名できる人がいない場合、通信事業者は別の時間にパッケージを配信しようとします。<br/><br/>**[!UICONTROL Indirect]**: （FedEx Residential Deliveries Only） FedExは、配信アドレスで誰か（おそらくネイバーまたはビルマネージャー）の署名を取得します。 受信者は、署名済みのFedExのドアタグを残して、誰も署名せずにパッケージを残すことを許可できます。<br/><br/>**[!UICONTROL Contents]**: （USPSのみ）パッケージの次のいずれかの説明を選択します。<br/>- ギフト <br/> – 文書<br/> – 商用サンプル <br/> – 返品品<br/> – 商品<br/> – その他&#x200B;<br/><br/>**[!UICONTROL Explanation]**: （USPSのみ） パッケージ内容の詳細な説明。<br/><br/>**[!UICONTROL Adult Required]**：配送業者は成人受信者の署名を取得し、印刷コピーを店に提示します。 |

{style="table-layout:auto"}

## パッケージの作成

配送ラベルの作成を選択すると、_[!UICONTROL Create Packages]_ウィンドウが表示されます。 最初のパッケージの設定をすぐに開始できます。

### パッケージの設定

>[!NOTE]
>
>[!UICONTROL Type]のデフォルト以外の値を選択するか、署名の確認を要求することを選択した場合、出荷価格は顧客に請求した価格と異なる場合があります。

1. 発送済み製品のリストを表示してパッケージに追加するには、**[!UICONTROL Add Products]**&#x200B;をクリックします。

   - 商品と数量を指定します。

     _[!UICONTROL Qty]_列には、追加可能な最大数量が表示されます。 最初のパッケージの場合、番号は出荷される製品の合計数量です。

   - 製品をパッケージに追加するには、**[!UICONTROL Add Selected Product(s) to Package]**&#x200B;をクリックします。

1. パッケージを追加するには、**[!UICONTROL Add Package]**&#x200B;をクリックします。

   複数のパッケージを追加し、同時に編集できます。

1. パッケージを削除するには、**[!UICONTROL Delete Package]**&#x200B;をクリックします。

製品がパッケージに追加された後、数量を直接編集することはできません。

### 量を増やす

1. **[!UICONTROL Add Selection]**&#x200B;をクリックします。

1. 追加数量を入力します。

   番号は、パッケージ内の製品の前の数量に追加されます。

### 数量を減らす

1. パッケージから製品を削除します。

1. **[!UICONTROL Add Selection]**&#x200B;をクリックします。

1. 新しい小さい値を入力します。

### 配送ラベルの生成

すべての製品を配布した後、使用するパッケージの合計数は、リスト内の最後のパッケージの数に等しくなります。 すべての出荷済みアイテムがパッケージに配布され、すべての必要な情報が完了するまで、_OK_ ボタンは無効になります。

ラベルを生成するには、**[!UICONTROL OK]**&#x200B;をクリックします。

必要に応じて、**[!UICONTROL Cancel]**&#x200B;をクリックしてプロセスを停止できます。 パッケージは保存されず、配送ラベルプロセスはキャンセルされます。

### フィールドの説明

| フィールド | 説明 |
|--- |--- |
| [!UICONTROL Type] | パッケージのタイプを指定します。 定義済みの値のいずれかを選択します。 利用可能なパッケージタイプは、配送業者ごとに異なります。 「パッケージを作成」ポップアップウィンドウが開くと、配送業者のデフォルトパッケージが「タイプ」フィールドに表示されます。 配送業者が設計していないパッケージを選択した場合は、パッケージの寸法を入力する必要があります。 DHL、FedEx、およびUPS出荷用に作成された配送ラベルの場合、「商品の種類」フィールドは`Merchandise`に設定されます。 USPSの場合、フィールドには&#x200B;_[!UICONTROL Create Packages]_ウィンドウの_ Contents _フィールドの値が反映されます。 |
| [!UICONTROL Total Weight] | パッケージの合計重量。 このフィールドには、パッケージ内の製品の合計重量が事前に入力されます。 測定単位は、ポンドまたはキログラムのいずれかに設定できます。 |
| [!UICONTROL Length] | パッケージの長さ、整数、浮動小数点数。 カスタムパッケージタイプを使用する場合、このフィールドは有効になります。 測定単位は、インチまたはセンチメートルのいずれかに設定できます。 |
| [!UICONTROL Width] | パッケージの幅、整数、および浮動小数点数。 カスタムパッケージタイプを使用する場合、このフィールドは有効になります。 測定単位は、高さフィールドの横にあるドロップダウンメニューを使用して指定できます。インチとセンチメートルの間で選択します。 |
| [!UICONTROL Height] | パッケージの高さ、整数、浮動小数点数。 カスタムパッケージタイプを使用する場合、このフィールドは有効になります。 測定単位は、高さフィールドの横にあるドロップダウンメニューを使用して指定できます。インチとセンチメートルの間で選択します。 |
| [!UICONTROL Signature] | 配達確認を定義します。 オプション：<br/><br/>**[!UICONTROL Not Required]**：配達確認レターは送信されません。<br/><br/>**[!UICONTROL No Signature]**：受信者の署名のない配達確認レターが送信されます。<br/><br/>**[!UICONTROL Signature Required]**：配送業者は受信者の署名を取得し、印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Adult Required]**：配送業者は成人受信者の署名を取得し、印刷されたコピーを提供します。<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedExは配達先住所で署名を取得し、パッケージに署名できる人人人がいない場合再試行します。<br/><br/>**[!UICONTROL Indirect (FedEx only)]** （1） <br/> （2）がネイバー、ビルマネージャー、またはアドレスの他の人から送信された場合、または<br/> （3）受信者は、誰も出席せずにパッケージのリリースを許可する署名済みのFedEx Door Tagを残すことができます。 <br/>住宅配達のみのご利用となります。 オプションは、配送方法によって少し異なる場合があります。 最新の情報については、配送業者のリソースを参照してください。 |
| [!UICONTROL Contents] | （USPS発送のみ可能）パッケージ内容の説明。 オプション：`Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | （USPS出荷のみ）パッケージ内容の詳細な説明。 |

{style="table-layout:auto"}


<!-- Last updated from includes: 2026-05-12 15:47:19 -->
