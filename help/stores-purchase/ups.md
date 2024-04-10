---
title: UPS （統一宅配便）
description: ストアの配送業者として UPS を設定する方法を説明します。
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# UPS （統一宅配便）

ユナイテッドパーセルサービス（UPS）は、220 カ国以上に陸路および空路で国内外配送サービスを提供しています。

{{ups-api}}

>[!NOTE]
>
>UPS が使用できる機能 [寸法重量](carriers.md#dimensional-weight) 配送料を決定します。 ただし、Adobe Commerceでは、重量ベースの送料の計算のみをサポートしています。

## 手順 1: UPS 出荷アカウントのオープン

この配送方法を顧客に提供するには、まず UPS でアカウントを開設する必要があります。

## 手順 2：ストアに対して UPS を有効にする

1. 日 _管理者サイドバー_&#x200B;に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルの下の **[!UICONTROL Sales]**、を選択 **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL UPS]** セクション。

1. を設定 **[!UICONTROL Enabled for Checkout]** 対象： `Yes`.

1. UPS REST アカウント（デフォルト）の場合、次の手順を実行します。

   - UPS 資格情報を入力します。UPS ClientID をとして入力します。 **[!UICONTROL User ID]**、UPS クライアント秘密鍵を **[!UICONTROL Password]**

   - を設定 **[!UICONTROL Mode]** 対象： `Live` 安全な接続で UPS 出荷システムにデータを送信する。 （開発モードでは、安全な接続を介してデータが送信されません）。

   - を確認 **[!UICONTROL Gateway URL]** これはリクエストの送信に必要です。 テストモードにはサンドボックス URL を、ライブリクエストには実稼動 URL を使用します。

   - を確認 **[!UICONTROL Tracking URL]** トラッキング情報を取得するには、この情報が必要です。 テストモードにはサンドボックス URL を、ライブリクエストには実稼動 URL を使用します。

   - を設定 **[!UICONTROL Origin of the Shipment]** 出荷元のリージョンに移動します。

   - UPS を使用して特別料金を設定する場合は、 **[!UICONTROL Enable Negotiated Rates]** 対象： `Yes` そして 6 桁を入力してください **[!UICONTROL Shipper Number]** ups によってあなたに割り当てられました。

   - を設定 **[!UICONTROL Live Account]** を次のいずれかに変更します。

      - `Yes`  – 実稼動モードで UPS を実行し、顧客に出荷方法として UPS を提供します。
      - `No` - UPS をテスト モードで実行します。

   >[!NOTE]
   >
   >標準の United Parcel Service タイプは廃止される予定です。 新しい設定では、デフォルトのを使用します `United Parcel Service REST` タイプ。 REST タイプも、を生成するために必要です。 [配送ラベル](shipping-labels.md).<br/>
   >2.4.7 リリースの場合 **[!UICONTROL UPS Type]**  は次の理由で削除されました `UPS` および `UPS XML` タイプは廃止予定で、次のようにスケジュールされています `UPS REST` がデフォルトです。 ネイティブのAdobe Commerce統合で使用される United Parcel Service （UPS） API は、現在 OAuth 2.0 セキュリティモデルをサポートしていないので、一時的に廃止されます。

   >[!IMPORTANT]
   >
   >UPS は現在のデフォルト （システム値）で使用されている HTTP のサポートを終了しています。 をクリア **[!UICONTROL Use system value]** チェックボックスをオンにして、HTTPS を使用する URL を変更します。 例： `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. の場合 **[!UICONTROL Title]**&#x200B;で、チェックアウト時に表示する配送オプションの名前を入力します。

   デフォルトでは、このフィールドはに設定されています。 `United Parcel Service`.

   ![UPS を有効にする](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 手順 3：コンテナの説明の完了

1. を設定 **[!UICONTROL Packages Request Type]** を次のいずれかに変更します。

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. の場合 **[!UICONTROL Container]**&#x200B;を選択し、出荷に使用する典型的なパッケージタイプを指定します。

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. を設定 **[!UICONTROL Weight Unit]** を、製品の重量の測定に使用するシステムに追加します。

   UPS がサポートするウェイト システムは国によって異なります。 疑問がある場合は、UPS にどの重量システムを使用する必要があるかを尋ねます。 次のようなオプションがあります。

   - `LBS`
   - `KGS`

1. を設定 **[!UICONTROL Destination Type]** を次のいずれかに変更します。

   - `Residential`  – 出荷のほとんどは B2C （Business to Consumer）です。
   - `Commercial`  – 出荷のほとんどは B2B です。

1. を入力 **[!UICONTROL Maximum Package Weight]** 通信事業者によって許可されています。

1. を設定 **[!UICONTROL Pickup Method]** を次のいずれかに変更します。

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. を入力 **[!UICONTROL Minimum Package Weight]** 通信事業者によって許可されています。

   ![コンテナの説明](./assets/ups2.png){width="600" zoomable="yes"}

## 手順 4：手数料の設定

手数料は任意で、UPS の送料に加算される追加料金として表示されます。 手数料を含める場合は、次の操作を行います。

1. を設定 **[!UICONTROL Calculate Handling Fee]** 次のいずれかの方法を使用します。

   - `Fixed`
   - `Percent`

1. 手数料の適用方法を決定するには、を設定します **[!UICONTROL Handling Applied]** を次のいずれかに変更します。

   - `Per Order`
   - `Per Package`

1. 金額を入力 **[!UICONTROL Handling Fee]** 請求される。

   パーセンテージを入力するには、小数点形式を使用します。 例えば、 `0.25` 25% の場合。

   ![手数料](./assets/ups3.png){width="600" zoomable="yes"}

## 手順 5：許可される方法と適用可能な国を指定

1. の場合 **[!UICONTROL Allowed Methods]**&#x200B;顧客が使用できる各 UPS 配送方法を選択します。

   チェックアウト時に UPS の下にメソッドが表示されます。 複数の方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

1. を指定する場合 [送料無料](shipping-free.md) ups 経由のオプション、送料無料オプションを設定します。

   - を設定 **[!UICONTROL Free Method]** を送料無料に使用する方法に変更します。 UPS 経由で送料無料を提供したくない場合は、次のいずれかを選択します `None`.

   - UPS を使用した無料配送の注文に適合する最小注文金額を要求するには、次のように設定します **[!UICONTROL Enable Free Shipping Threshold]** 対象： `Enable`. 次に、で最小値を入力します **[!UICONTROL Free Shipping Amount Threshold]**.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキスト ボックスには既定のメッセージがあらかじめ設定されていますが、UPS が使用できなくなったときに表示する別のメッセージを入力できます。

   ![許可されるメソッド](./assets/ups4.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたこの配信方法を使用できます。
   - `Specific Countries`  – このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 リストで、この配信方法を使用できる国を選択します。

1. を設定 **[!UICONTROL Show Method if Not Applicable]** を次のいずれかに変更します。

   - `Yes` - チェックアウト時に利用可能なすべての UPS 発送方法を一覧表示します。このリストには、出荷に適用されない方法も含まれます。
   - `No`  – 出荷に適用可能な UPS 出荷方法のみをリストします。

   ![対象国](./assets/ups5.png){width="600" zoomable="yes"}

1. ストアからの UPS 出荷の詳細を記録したログ ファイルを作成するには、次のように設定します **[!UICONTROL Debug]** 対象： `Yes`.

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の配信方法と共にリストされたときに UPS が表示される順序を決定します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.

## 手順 6：発送元住所の設定

1. 次のことを確認します [ストア情報](../getting-started/store-details.md#store-information) が完了しました。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択して、 **[!UICONTROL Shipping Settings]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) **[!UICONTROL Origin]** ページで、発送元住所を設定します。

   ![販売設定 – 発送元住所オプション](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce は、配送料を計算する際に、UPS に対して全注文価格を宣言しません。 この動作は変更できません。
