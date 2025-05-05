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

税金クラスは、顧客、製品および出荷に割り当てることができます。 Commerceは、各顧客の買い物かごを分析し、顧客のクラス、買い物かごの商品のクラスおよびリージョンに従って適切な税金を計算します。 地域は、顧客の発送先住所、請求先住所、または発送元によって決定されます。 [ 税務処理基準 ](tax-rules.md) を定義する際に、新しい税クラスを作成できます。

- **顧客** – 必要な数の顧客税金クラスを作成して、[ 顧客グループ ](../customers/customer-groups.md) に割り当てることができます。 例えば、一部の管轄区域では、卸売取引は課税されませんが、小売取引は課税されます。 Wholesale Customer グループのメンバーを Wholesale tax クラスに関連付けることができます。

- **商品** – 商品クラスは、計算で使用され、買い物かごに正しい税率が適用されるかどうかを決定します。 製品を作成すると、その製品は特定の税区分に割り当てられます。 例えば、食品に対する課税が行われない場合や、異なる税率で課税される場合があります。

- **配送料** – 店舗が配送料に追加税を請求する場合は、配送用の特定の製品税クラスを指定する必要があります。 次に、設定で、出荷に使用する税クラスとして指定します。

## 税クラスの構成

出荷に使用される税クラスと、[ 製品および顧客 ](#add-a-product-tax-class) のデフォルトの税クラスは、_[!UICONTROL Sales]_&#x200B;設定で設定されます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Tax]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Tax Classes]**」セクションを展開します。

   ![ 構成 – 税クラス ](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 次の各税金区分を選択します。

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 税クラスを追加

顧客および製品の税金クラスを簡単に追加して、個別の顧客および製品に割り当て、税務処理基準で使用できます。

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Taxes]_/**[!UICONTROL Tax Rules]**&#x200B;に移動します。

1. 「**[!UICONTROL Add New Tax Rule]**」をクリックします。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Additional Settings]**」セクションを展開します。

   ![ 新しい税クラスの追加 ](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. _顧客税区分_ の下で、「**[!UICONTROL Add New Tax Class]**」をクリックします。

1. 新しい税区分の **[!UICONTROL Name]** をテキスト・ボックスに入力します。

   ![ 新しい税クラスの追加 ](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 使用可能な顧客税区分のリストに新規区分を追加するには、チェックマークをクリックします。

   ![ 新しい税クラス ](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 製品税クラスの追加

1. _製品税区分_ で、「**[!UICONTROL Add New Tax Class]**」をクリックします。

1. 新しい税区分の **[!UICONTROL Name]** をテキスト・ボックスに入力します。

1. 使用可能な製品税区分のリストに新規区分を追加するには、チェックマークをクリックします。

1. 完了したら、ボタンバーの **[!UICONTROL Back]** をクリックして _税ルール_ グリッドに戻ります。

## 既定の税宛先

デフォルトの税金宛先設定では、税金計算の基礎として使用される国、州および郵便番号を決定します。

**_計算のデフォルト税金宛先を構成する手順は、次のとおりです。_**

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Tax]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL Default Tax Destination Calculation]**」セクションを展開します。

   ![ デフォルト税金搬送先計算 ](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 税金計算のベースとなる国の **[!UICONTROL Default Country]** を設定します。

1. 税計算の基礎として使用される都道府県に **[!UICONTROL Default State]** を設定します。

1. 地方税の計算の基礎として使用される郵便番号に **[!UICONTROL Default Post Code]** を設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
