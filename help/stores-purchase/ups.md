---
title: UPS (United Parcel Service)
description: UPS を店舗の配送業者として設定する方法を説明します。
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# UPS (United Parcel Service)

United Parcel Service (UPS) は、220 以上の国々に対し、陸地と空気による国内および国際的な海運サービスを提供します。

{{ups-api}}

>[!NOTE]
>
>UPS で使用可能 [寸法の重さ](carriers.md#dimensional-weight) 送料を決定する。 ただし、Adobe Commerceは重量ベースの配送コスト計算のみをサポートしています。

## ステップ 1: UPS 配送先アカウントを開く

この発送方法を顧客に提供するには、まず UPS のアカウントを開く必要があります。

## 手順 2：ストアの UPS を有効にする

{{beta2-updates}}

1. 次の日： _管理サイドバー_&#x200B;に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、の下 **[!UICONTROL Sales]**&#x200B;を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL UPS]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enabled for Checkout]** から `Yes`.

1. UPS XML アカウント（デフォルト）の場合は、 **[!UICONTROL UPS Type]** から `United Parcel Service XML` 次の操作を実行します。

   - UPS 資格情報を入力してください： **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (16 桁の UPS アカウント `Access Key`) および **[!UICONTROL Password]**

   - 設定 **[!UICONTROL Mode]** から `Live` 安全な接続を介して UPS 出荷システムにデータを送信する。 （開発モードでは、安全な接続を介してデータを送信しません。）

   - を確認します。 **[!UICONTROL Gateway XML URL]** XML ファイルで要求を送信するために必要な

   - 設定 **[!UICONTROL Origin of the Shipment]** 出荷元の地域に。

   - UPS に特別料金がある場合は、 **[!UICONTROL Enable Negotiated Rates]** から `Yes` 6 桁の数字を入力します。 **[!UICONTROL Shipper Number]** UPS によって割り当てられた。

1. 標準 UPS アカウントの場合は、 **[!UICONTROL UPS Type]** から `United Parcel Service` 次の操作を実行します。

   >[!NOTE]
   >
   >標準の United Parcel Service タイプは、廃止が予定されています。 新しい設定の場合は、デフォルトの  `United Parcel Service XML` タイプ。 生成には XML タイプも必要です [出荷ラベル](shipping-labels.md).

   - 設定 **[!UICONTROL Live Account]** を次のいずれかに変更します。

      - `Yes` - UPS を実稼働モードで実行し、顧客への発送方法として UPS を提供します。
      - `No` - UPS をテストモードで実行します。

   - Adobe Analytics の **[!UICONTROL Gateway URL]** 「 」フィールドに、UPS の送料を計算するために使用する URL を入力します。

     >[!IMPORTANT]
     >
     >UPS は、現在のデフォルト（システム値）で使用されている HTTP のサポートを継続していません。 次をクリア： **[!UICONTROL Use system value]** 」チェックボックスをオンにし、HTTPS を使用する URL を変更します。 例： `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. の場合 **[!UICONTROL Title]**「 」には、チェックアウト時に表示するこの発送オプションの名前を入力します。

   デフォルトでは、このフィールドはに設定されています。 `United Parcel Service`.

   ![UPS を有効にする](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 手順 3：コンテナの説明を入力する

1. 設定 **[!UICONTROL Packages Request Type]** を次のいずれかに変更します。

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. の場合 **[!UICONTROL Container]**、出荷に使用する標準梱包タイプを指定します。

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

1. 設定 **[!UICONTROL Weight Unit]** 製品の重み付けを測定する際に使用するシステムに対して。

   UPS がサポートする重量システムは、国によって異なります。 疑わしい場合は、UPS にどの重み付けシステムを使用する必要があるかを尋ねます。 オプションは次のとおりです。

   - `LBS`
   - `KGS`

1. 設定 **[!UICONTROL Destination Type]** を次のいずれかに変更します。

   - `Residential`  — 出荷のほとんどは消費者向けのビジネスです (B2C)。
   - `Commercial`  — 出荷のほとんどは、ビジネス向けのビジネス (B2B) です。

1. 次を入力します。 **[!UICONTROL Maximum Package Weight]** 運送業者によって許可された。

1. 設定 **[!UICONTROL Pickup Method]** を次のいずれかに変更します。

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 次を入力します。 **[!UICONTROL Minimum Package Weight]** 運送業者によって許可された。

   ![コンテナの説明](./assets/ups2.png){width="600" zoomable="yes"}

## 手順 4：処理料金の設定

手数料はオプションで、UPS の送料に追加される追加料金として表示されます。 手数料を含める場合は、次の手順を実行します。

1. 設定 **[!UICONTROL Calculate Handling Fee]** を次のいずれかのメソッドに追加します。

   - `Fixed`
   - `Percent`

1. 処理費の適用方法を決定するには、 **[!UICONTROL Handling Applied]** を次のいずれかに変更します。

   - `Per Order`
   - `Per Package`

1. 金額を入力 **[!UICONTROL Handling Fee]** 請求される。

   パーセンテージを入力するには、10 進形式を使用します。 例えば、 `0.25` 25%です。

   ![手数料](./assets/ups3.png){width="600" zoomable="yes"}

## 手順 5：許可された方法と適用可能な国を指定する

1. の場合 **[!UICONTROL Allowed Methods]**、顧客が利用できる各 UPS 発送方法を選択します。

   チェックアウト時に UPS の下にメソッドが表示されます。 複数の方法を選択するには、Ctrl キー (PC) または Command キー (Mac) を押しながら各オプションをクリックします。

1. 次を指定する場合、 [送料無料](shipping-free.md) オプションを UPS 経由で、無料配送オプションを設定します。

   - 設定 **[!UICONTROL Free Method]** 無料配送に使用する方法に。 UPS を通じて送料無料を提供したくない場合は、 `None`.

   - UPS での無料配送に適合する最小注文額を要求するには、 **[!UICONTROL Enable Free Shipping Threshold]** から `Enable`. 次に、最小値を **[!UICONTROL Free Shipping Amount Threshold]**.

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキストボックスには既定のメッセージがあらかじめ設定されていますが、UPS が使用できなくなった場合に表示する別のメッセージを入力できます。

   ![許可されるメソッド](./assets/ups4.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この配信方法を使用できます。
   - `Specific Countries`  — このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 この配信方法を使用できる国をリストから選択します。

1. 設定 **[!UICONTROL Show Method if Not Applicable]** を次のいずれかに変更します。

   - `Yes`  — チェックアウト時に使用可能な UPS 出荷方法の一覧が表示されます。これには、出荷に適用されない方法も含まれます。
   - `No`  — 出荷に適用できる UPS 出荷方法のみをリストします。

   ![該当国](./assets/ups5.png){width="600" zoomable="yes"}

1. ストアから行われた UPS 出荷の詳細を含むログファイルを作成するには、 **[!UICONTROL Debug]** から `Yes`.

1. の場合 **[!UICONTROL Sort Order]**、数値を入力して、チェックアウト時に UPS が他の配信方法と共にリストに表示される際の順序を決定します。

   `0` =最初 `1` =秒 `2` = 3 番目、など。

1. クリック **[!UICONTROL Save Config]**.

## 手順 6：発送元の住所の設定

1. 次の項目を確認します。 [ストア情報](../getting-started/store-details.md#store-information) が完了しました。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択し、 **[!UICONTROL Shipping Settings]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) **[!UICONTROL Origin]** をクリックし、発送元の住所を設定します。

   ![販売構成 — 発送元住所オプション](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. クリック **[!UICONTROL Save Config]**.

>[!NOTE]
>
>コマースは、送料を計算する際に、UPS に対して完全な注文価格を宣言しません。 この動作は変更できません。
