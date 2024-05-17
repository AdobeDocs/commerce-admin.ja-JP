---
title: DHL
description: ストアの配送業者として DHL を設定する方法を説明します。
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL は、手紙、商品、情報を管理および輸送するための統合された国際サービスと、カスタマイズされた顧客志向のソリューションを提供します。

## 手順 1:DHL を有効にする

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Delivery Methods]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL DHL]** セクション。

   >[!NOTE]
   >
   >必要に応じて、まず **[!UICONTROL Use system value]** チェックボックスをオンにして、説明に従って次の設定を変更します。

1. を設定 **[!UICONTROL Enabled for Checkout]** 対象： `Yes`.

1. 通常は、デフォルトをそのまま使用できます **[!UICONTROL Gateway URL]**.

   DHL から代替 URL が提供されている場合は、このフィールドにその値を入力します。

1. DHL から提供された資格情報を使用して、次のフィールドに入力します。

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL アカウント設定](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 手順 2：パッケージの説明と手数料を入力します

1. が含まれる **[!UICONTROL Content Type]** リストから、出荷するパッケージのタイプに最も近いオプションを選択します。

   - `Documents`
   - `Non documents`

1. 要件に応じて手数料オプションを設定します。

   手数料は任意で、DHL の送料に加算される追加料金として表示されます。 手数料を含める場合は、次の操作を行います。

   - の場合 **[!UICONTROL Calculate Handling Fee]**&#x200B;で、手数料の計算に使用する方法を選択します。

      - `Fixed`
      - `Percentage`

   - の場合 **[!UICONTROL Handling Applied]**&#x200B;で、手数料の適用方法を選択します。

      - `Per Order`
      - `Per Package`

   - の場合 **[!UICONTROL Handling Fee]**&#x200B;金額の計算方法を選択して、請求金額を入力します。

     例えば、料金が固定料金に基づいている場合は、次のように金額を小数で入力します `4.90`. ただし、手数料が注文のパーセンテージに基づいている場合は、パーセンテージで金額を入力します。 例えば、注文の 6% を請求する場合は、値を `.06`.

   - 合計注文重量を分割して配送料を正確に計算できるようにするには、次のように設定します **[!UICONTROL Divide Order Weight]** 対象： `Yes`.

   - を **[!UICONTROL Weight Unit]** パッケージを次のいずれかに変更します。

      - `Pounds`
      - `Kilograms`

   - を **[!UICONTROL Size]** 一般的なパッケージを次のいずれかに変更します。

      - `Regular`
      - `Specific`

     次を選択した場合： `Specific`を入力します **[!UICONTROL Height]**, **[!UICONTROL Depth]**、および **[!UICONTROL Width]** パッケージの（センチメートル単位）。

   ![DHL パッケージ設定](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 手順 3：許可される配信方法の指定

1. の場合 **[!UICONTROL Allowed Methods]**&#x200B;を選択して、顧客が使用できるようにする各方法を選択します。

   複数の方法を選択するには、Ctrl キー（PC）または Command キー（Mac）を押したまま、各オプションをクリックします。

   正しい配信方法のリストを表示するには、まず [原産国](../configuration-reference/sales/shipping-settings.md).

1. の場合 **[!UICONTROL Ready Time]**、注文が送信されてからパッケージの出荷準備が整うまでの時間数を入力します。

1. を編集する **[!UICONTROL Displayed Error Message]** 必要に応じて。

   このメッセージは、選択したメソッドが使用できない場合に表示されます。

1. を指定する場合 [送料無料](shipping-free.md) dhl 経由のオプション、送料無料オプションを設定します。

   - の場合 **[!UICONTROL Free Method]**&#x200B;を選択します。送料無料で使用する方法を選択します。

   - を設定 **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable`  – 最小注文で送料無料を提供する場合は、を入力します **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable`  – 注文には DHL 無料配送は適用されません。

     この設定は、標準の設定と似ています _送料無料_ メソッドですが、DHL セクションに表示されるので、顧客は注文にどの方法が使用されているかを把握できます。

   - の場合 **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;を選択し、送料無料の対象となる注文の最小金額を入力します。

     ![DHL 許可メソッド](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 手順 4：適用国を指定する

1. を設定 **[!UICONTROL Ship to Applicable Countries]** を次のいずれかに変更します。

   - `All Allowed Countries`
   - `Specific Countries`

   特定の国に配送する場合は、国を **[!UICONTROL Ship to Specific Countries]** リスト。

1. を設定 **[!UICONTROL Show Method if Not Applicable]**:

   `Yes`  – 注文に適用されない場合でも、チェックアウト時の配送方法として DHL を表示します。

   `No` - DHL をチェックアウト時の配送方法として表示します（該当する場合のみ）。

1. ストアから作成された DHL 出荷の詳細を記録したログ ファイルを作成するには、次のように設定します **[!UICONTROL Debug]** 対象： `Yes`.

1. の場合 **[!UICONTROL Sort Order]**：数字を入力して、チェックアウト時に他の配信方法と共にリストされたときに DHL が表示されるシーケンスを決定します。

   `0` =最初、 `1` =秒、 `2` = 3 番目、以下同様です。

1. クリック **[!UICONTROL Save Config]**.

   ![DHL 対象国](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
