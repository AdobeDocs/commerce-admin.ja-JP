---
title: FedEx
description: FedEx をお店の配送業者として設定する方法を学びます。
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# FedEx

FedEx は、世界最大の海運サービス会社の 1 つで、航空、貨物、陸上の輸送サービスにいくつかの優先順位を提供しています。

![チェックアウト時の FedEx 送料オプション](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx は [寸法の重さ](carriers.md#dimensional-weight) 送料を決定する。 ただし、Adobe CommerceとMagento Open Sourceは重量ベースの配送コストの計算のみをサポートします。

## ステップ 1:FedEx Web Services Production に登録

A [FedEx マーチャントアカウント][1] FedEx Web Services Production Access の登録が必要です。 FedEx アカウントを作成した後、実稼動アカウントの情報ページを読み、 _実稼動キーを取得_ ページ下部のリンクを使用して登録し、キーを取得します。

>[!NOTE]
>
>必ず認証キーをコピーするか、書き留めてください。 コマース配送設定で FedEx を設定する必要があります。

## 手順 2：ストアの FedEx を有効にする

{{beta2-updates}}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Delivery Methods]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL FedEx]** 」セクションに入力します。

1. 設定 **[!UICONTROL Enabled for Checkout]** から `Yes`.

1. の場合 **[!UICONTROL Title]**、チェックアウト時に FedEx 発送方法を識別するタイトルを入力します。

1. FedEx アカウントから次の情報を入力します。

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. FedEx サンドボックスを設定済みで、テスト環境で作業する場合は、 **[!UICONTROL Sandbox Mode]** から `Yes`.

   >[!NOTE]
   >
   >サンドボックスモードを必ずにに設定してください。 `No` 顧客に配送方法として FedEx を提供する準備が整ったら。

   ![FedEx アカウント設定](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 手順 3：パッケージの説明と取り扱い料金

1. を選択します。 **[!UICONTROL Packages Request Type]** オーダーを複数の出荷に分割する場合の、好みを最もよく説明するオプションを次に示します。

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. 次のタイプを選択： **[!UICONTROL Packaging]** 通常は、お客様のストアから製品を出荷する際に使用します。

1. 設定 **[!UICONTROL Dropoff]** を、配信に使用するピックアップ方法に追加します。

   - `Regular Pickup` ・出荷量が多い場合は、定期的な受け付けのために FedEx との取り決めを行うのがコスト・パフォーマンスに優れています。

   - `Request Courier` - FedEx の宅配便に電話して、出荷を受け取るよう依頼する必要があります。

   - `Drop Box`  — 近くの FedEx ドロップオフボックスで出荷を返却する必要があります。

   - `Business Service Center`  — 現地の FedEx ビジネス・サービス・センターで出荷を中止する必要があります。

   - `Station`  — 現地の FedEx 駅で出荷を中止する必要があります。

1. 設定 **[!UICONTROL Weight Unit]** をロケールで使用される測定単位に追加します。

   - `Pounds`
   - `Kilograms`

1. 次を入力します。 **[!UICONTROL Maximum Package Weight]** FedEx の出荷が許可されました。

   デフォルトの FedEx の最大重量は 150 ポンドです。 詳しくは、配送先にお問い合わせください。 FedEx と特別な取り決めを行っていない限り、デフォルト値をお勧めします。 詳しくは、 [寸法の重み付け](carriers.md#dimensional-weight) を参照してください。

   ![FedEx パッケージ設定](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 必要に応じて、取り扱い料金オプションを設定します。

   処理費はオプションで、チェックアウト時には表示されません。 手数料を含める場合は、次の手順を実行します。

   - 設定 **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - の場合 **[!UICONTROL Handling Applied]**&#x200B;では、次のいずれかの方法を使用して料金を管理します。

      - `Per Order`
      - `Per Package`

   - 次を入力します。 **[!UICONTROL Handling Fee]** 次のいずれかとして `fixed` 量または `percentage`（計算方法に応じて）。

1. 設定 **[!UICONTROL Residential Delivery]** を次のいずれかに変更します。

   - `Yes` - B2C 住宅配送の場合。
   - `No` - B2B 住宅配送の場合。

   ![FedEx 取り扱い料金設定](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 手順 4：許可された方法と適用可能な国

1. 設定 **[!UICONTROL Allowed Methods]** を、提供する各出荷方法に追加します。

   方法を選択する際は、FedEx アカウント、出荷の頻度とサイズ、および国際出荷を許可する場合を考慮します。 次のようなメソッドを必要な数だけ、またはいくつでも提供できます。

   - ヨーロッパ優先
   - 配送日オプション： 1 日の運送、2 日の運送、2 日の午前 2 日の午前 2 日、3 日の運送
   - 国内オプション — 速達節約、地上、最初、一晩、宅配、標準一晩
   - 国際オプション — 国際経済，国際経済貨物，国際最初，国際地，国際，国際，優先度（国際）
   - 優先オプション — 運賃、優先夜間
   - スマート投稿 — スマート投稿メソッドを提供している場合 ( **ハブ ID**)
   - 貨物オプション — 運賃、国際運賃

1. 次を指定する場合、 [送料無料](shipping-free.md) オプションを FedEx を通じて、無料配送オプションを設定します。

   - 設定 **[!UICONTROL Free Method]** 無料配送に使用する方法に。 FedEx を通じて送料無料を提供したくない場合は、 `None`.

   - FedEx での無料配送の注文に適合する最小注文額を要求するには、 **[!UICONTROL Enable Free Shipping Threshold]** から `Enable`. 次に、最小値を **[!UICONTROL Free Shipping Amount Threshold]**.

   この設定は、標準の無料配送方法の設定に似ていますが、チェックアウト時に FedEx セクションに表示されるので、顧客は注文に使用される方法を把握します。

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキストボックスにはデフォルトのメッセージがあらかじめ設定されていますが、FedEx が利用できなくなった場合に表示する別のメッセージを入力できます。

   ![FedEx で許可された配信メソッド](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  — すべてのお客様から [国](../getting-started/store-details.md#country-options) ストア設定で指定された場合、この配信方法を使用できます。

   - `Specific Countries`  — このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 この配信方法を使用できる国をリストから選択します。

1. ストアと FedEx システム間のすべての通信のログを保持する場合は、 **[!UICONTROL Debug]** から `Yes`.

1. 設定 **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes`  — 顧客に対する FedEx の配送方法を、在庫状況に関係なくすべて表示します。
   - `No`  — 注文に適用される FedEx 発送方法のみを表示します。

1. の場合 **[!UICONTROL Sort Order]**、数値を入力して、チェックアウト時に FedEx が他の配信方法と共にリストに表示される際の順序を決定します。

   `0` =最初 `1` =秒 `2` = 3 番目、など。

1. クリック **[!UICONTROL Save Config]**.

   ![FedEx 適用国](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>コマースは、配送料を計算する際に常に FedEx に対して完全な注文価格を宣言します。 この動作は変更できません。

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
