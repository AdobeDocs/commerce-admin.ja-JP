---
title: FedEx
description: ストアの配送業者として FedEx を設定する方法を説明します。
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

FedEx 社は、航空便、貨物、陸上輸送サービスを複数の優先課題で提供する世界最大級の輸送サービス企業です。

![チェックアウト時の FedEx 配送オプション](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx が使用できる [寸法重量](carriers.md#dimensional-weight) 配送料を決定します。 ただし、Adobe CommerceとMagento Open Sourceでは、重量ベースの送料の計算のみをサポートしています。

## 手順 1:FedEx Web サービスの本番環境への登録

A [FedEx マーチャントアカウント][1] また、FedEx Web サービスの本番アクセスの登録が必要です。 FedEx アカウントを作成したら、実稼働アカウントの情報ページを読み、 _実稼動キーの取得_ ページの下部にある、登録してキーを取得するためのリンク。

>[!NOTE]
>
>認証キーを必ずコピーまたは書き留めてください。 コマースの配送設定で FedEx を設定する必要があります。

## 手順 2：ストアに対して FedEx を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL FedEx]** セクション。

1. を設定 **[!UICONTROL Enabled for Checkout]** 対象： `Yes`.

1. の場合 **[!UICONTROL Title]**&#x200B;を入力し、チェックアウト時の FedEx 配送方法を識別するタイトルを入力します。

1. FedEx アカウントから以下の情報を入力します。

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. FedEx サンドボックスを設定して、テスト環境で作業する場合は、を設定します **[!UICONTROL Sandbox Mode]** 対象： `Yes`.

   >[!NOTE]
   >
   >サンドボックスモードをに忘れずに設定してください `No` お客様に FedEx を配送方法として提供する準備ができたら。

   ![FedEx アカウント設定](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 手順 3：パッケージの説明と手数料

1. を設定 **[!UICONTROL Pickup Type]** 出荷に使用される集荷方法。

   - `DropOff at Fedex Location` - （デフォルト）ローカルの FedEx ステーションで出荷をドロップ・オフすることを示します。
   - `Contact Fedex to Schedule` - FedEx に連絡して集荷を依頼することを示します。
   - `Use Scheduled Pickup`  – 出荷が通常のスケジュールされた集荷の一部として集荷されることを示します。
   - `On Call` - FedEx を呼び出してピックアップがスケジュールされていることを示します。
   - `Package Return Program`  – 出荷が FedEx Ground Package Returns プログラムによって受け取られることを示します。
   - `Regular Stop`  – 出荷が通常の集荷スケジュールで集荷されることを示します。
   - `Tag`  – 出荷集荷が Express タグまたは Ground コール タグの集荷要求に固有であることを示します。 これは、返品配送ラベルにのみ適用されます。

1. の場合 **[!UICONTROL Packages Request Type]**&#x200B;で、1 つの受注を複数の出荷に分割する場合に、作業環境を最もよく表す要求タイプを選択します。

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. の場合 **[!UICONTROL Packaging]**&#x200B;を選択します。通常、商品をストアから出荷するために使用する FedEx パッケージのタイプを選択します。

1. を設定 **[!UICONTROL Weight Unit]** をロケールで使用される測定単位に変換します。

   - `Pounds`
   - `Kilograms`

1. を入力 **[!UICONTROL Maximum Package Weight]** fedex の出荷で許可されます。

   デフォルトの FedEx の最大重量は 150 ポンドです。 詳しくは、配送業者にお問い合わせください。 FedEx で特別な取り決めを行っていない限り、デフォルト値をお勧めします。 参照： [ディメンションの重み付け](carriers.md#dimensional-weight) を参照してください。

   ![FedEx パッケージ設定](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 要件に応じて手数料オプションを設定します。

   手数料はオプションで、チェックアウト時には表示されません。 手数料を含める場合は、次の操作を行います。

   - を設定 **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - の場合 **[!UICONTROL Handling Applied]**&#x200B;の場合は、手数料を管理するために、次のいずれかの方法を選択します。

      - `Per Order`
      - `Per Package`

   - を入力 **[!UICONTROL Handling Fee]** 次のいずれかの場合： `fixed` 金額若しくは `percentage`計算方法によって異なります。

1. を設定 **[!UICONTROL Residential Delivery]** を B2C 販売か B2B 販売かに応じて、次のいずれかに変更します。

   - `Yes` - B2C レジデンシャル配信用。
   - `No` - B2B レジデンシャル配信用。

   ![FedEx 処理手数料設定](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 手順 4：許可される方法と適用国

1. を設定 **[!UICONTROL Allowed Methods]** ご希望の出荷方法ごとに異なります。

   方法を選択する際は、FedEx アカウント、発送の頻度とサイズ、および国際発送を許可している場合を考慮してください。 次のようなメソッドをいくつでも好きなだけ提供できます。

   - ヨーロッパの最優先事項
   - 搬送日オプション：1 日運送費、2 日運送費、2 日、午前 2 日、運送費 3 日
   - 国内のオプション – エクスプレス セーバー、グラウンド、ファースト、オーバーナイト、宅配、スタンダード オーバーナイト
   - 国際オプション – 国際経済，Intl Economy Freight, International First, International Ground, International, Priority Intl
   - 優先オプション – 運賃、一晩での優先
   - Smart Post メソッドを提供する Smart Post-If （ **ハブ ID**）
   - 運送費 – 運送費、全国運送費

1. を指定する場合 [送料無料](shipping-free.md) オプション FedEx を使用して、送料無料オプションを設定します。

   - を設定 **[!UICONTROL Free Method]** を送料無料に使用する方法に変更します。 FedEx を通じて送料無料を提供したくない場合は、次のいずれかを選択します `None`.

   - FedEx を使用して送料無料の注文を確定する最小注文金額を要求するには、次のように設定します **[!UICONTROL Enable Free Shipping Threshold]** 対象： `Enable`. 次に、で最小値を入力します **[!UICONTROL Free Shipping Amount Threshold]**.

   この設定は、標準の送料無料の方法の設定と似ていますが、チェックアウト時に FedEx セクションに表示されるので、お客様はどの方法が注文に使用されているかを把握できます。

1. 必要に応じて、 **[!UICONTROL Displayed Error Message]**.

   このテキスト ボックスには既定のメッセージがあらかじめ設定されていますが、FedEx が使用できなくなったときに表示する別のメッセージを入力できます。

   ![FedEx で許可されている配信方法](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries`  – すべてのお客様 [国](../getting-started/store-details.md#country-options) ストア設定で指定されたこの配信方法を使用できます。

   - `Specific Countries`  – このオプションを選択すると、 _特定の国に出荷_ リストが表示されます。 リストで、この配信方法を使用できる国を選択します。

1. ストアと FedEx システム間のすべての通信のログを保持する場合は、を設定します。 **[!UICONTROL Debug]** 対象： `Yes`.

1. を設定 **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes`  – 可用性に関係なく、顧客に対するすべての FedEx 配送方法を表示します。
   - `No`  – 注文に適用される FedEx 配送方法のみを表示します。

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の配信方法と共に表示される FedEx の表示順序を決定します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.

   ![FedEx 適用国](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce は、配送料を計算する際に、常にフルオーダー価格を FedEx に宣言します。 この動作は変更できません。

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
