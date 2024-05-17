---
title: 税クラス
description: 税務処理基準に使用する税クラスを設定する方法を説明します。
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 税クラス

税金クラスは、顧客、製品および出荷に割り当てることができます。 Commerceは、各顧客の買い物かごを分析し、顧客のクラス、買い物かごの商品のクラスおよびリージョンに従って適切な税金を計算します。 地域は、顧客の発送先住所、請求先住所、または発送元によって決定されます。 次の場合に、新しい税金クラスを作成できます [税務処理基準](tax-rules.md) が定義されています。

- **顧客**  – 必要な数の顧客税金クラスを作成して、次に割り当てることができます [顧客グループ](../customers/customer-groups.md). 例えば、一部の管轄区域では、卸売取引は課税されませんが、小売取引は課税されます。 Wholesale Customer グループのメンバーを Wholesale tax クラスに関連付けることができます。

- **製品**  – 商品クラスは、正しい税率が買い物かごに適用されることを判断するための計算で使用されます。 製品を作成すると、その製品は特定の税区分に割り当てられます。 例えば、食品に対する課税が行われない場合や、異なる税率で課税される場合があります。

- **送料**  – 店舗が配送時に追加税を請求する場合は、配送用の特定の製品税クラスを指定する必要があります。 次に、設定で、出荷に使用する税クラスとして指定します。

## 税クラスの構成

出荷に使用される税区分、およびの既定の税区分 [製品と顧客](#add-a-product-tax-class) は、 _[!UICONTROL Sales]_設定。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Tax Classes]** セクション。

   ![設定 – 税クラス](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 次の各税金区分を選択します。

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完了したら、 **[!UICONTROL Save Config]**.

## 税クラスを追加

顧客および製品の税金クラスを簡単に追加して、個別の顧客および製品に割り当て、税務処理基準で使用できます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. クリック **[!UICONTROL Add New Tax Rule]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Additional Settings]** セクション。

   ![新しい税クラスの追加](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 次の下 _顧客税金クラス_&#x200B;を選択し、 **[!UICONTROL Add New Tax Class]**.

1. を入力 **[!UICONTROL Name]** テキストボックス内の新しい税クラスの。

   ![新しい税クラスの追加](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 使用可能な顧客税区分のリストに新規区分を追加するには、チェックマークをクリックします。

   ![新しい税クラス](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 製品税クラスの追加

1. 次の下 _製品税クラス_&#x200B;を選択し、 **[!UICONTROL Add New Tax Class]**.

1. を入力 **[!UICONTROL Name]** テキストボックス内の新しい税クラスの。

1. 使用可能な製品税区分のリストに新規区分を追加するには、チェックマークをクリックします。

1. 完了したら、 **[!UICONTROL Back]** ボタン バーで、に戻ります。 _税務処理基準_ グリッド。

## 既定の税宛先

デフォルトの税金宛先設定では、税金計算の基礎として使用される国、州および郵便番号を決定します。

**_計算のデフォルト税金宛先を構成する手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Tax]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Default Tax Destination Calculation]** セクション。

   ![デフォルト税金宛先計算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Default Country]** 課税計算のベースとなる国。

1. を設定 **[!UICONTROL Default State]** 課税計算の基礎として使用される州または都道府県。

1. を設定 **[!UICONTROL Default Post Code]** 地方税の計算の基礎として使用される郵便番号。

1. 完了したら、 **[!UICONTROL Save Config]**.
