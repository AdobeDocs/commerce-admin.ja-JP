---
title: 税区分
description: 税務処理ルールに使用する税区分を構成する方法を説明します。
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 税区分

税区分は、顧客、製品および配送先に割り当てることができます。 コマースは、各顧客の買い物かごを分析し、顧客のクラス、買い物かご内の製品のクラス、地域に基づいて適切な税金を計算します。 地域は、顧客の配送先住所、請求先住所、または配送元によって決まります。 新しい税区分は、次の場合に作成できます： [課税ルール](tax-rules.md) が定義されている。

- **顧客**  — 顧客税区分を必要な数だけ作成し、割り当てることができます。 [顧客グループ](../customers/customer-groups.md). 例えば、一部の管轄区域では、卸売取引は課税されず、小売取引が課税されます。 卸売顧客グループのメンバーを卸売税区分に関連付けることができます。

- **製品**  — 製品区分は、買い物かごに正しい税率が適用されるかどうかを判断するために計算で使用されます。 製品を作成すると、特定の税区分に割り当てられます。 例えば、食品に課税されない場合や、別の料金で課税される場合があります。

- **送料**  — 店舗が送料に追加の税金を課す場合は、配送に特定の製品税区分を指定する必要があります。 次に、設定で、出荷に使用する税区分として指定します。

## 税区分の構成

配送に使用される税区分と、のデフォルトの税区分 [製品と顧客](#add-a-product-tax-class) が _[!UICONTROL Sales]_設定。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Tax Classes]** 」セクションに入力します。

   ![構成 — 税区分](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 次の各項目の税区分を選択します。

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 税区分を追加

顧客と製品の税区分を容易に追加し、個々の顧客と製品に割り当てて、税ルールで使用できます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. クリック **[!UICONTROL Add New Tax Rule]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Additional Settings]** 」セクションに入力します。

   ![新しい税区分の追加](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. の下 _顧客税区分_&#x200B;をクリックし、 **[!UICONTROL Add New Tax Class]**.

1. 次を入力します。 **[!UICONTROL Name]** 新しい税区分のテキスト・ボックス内の。

   ![新しい税区分の追加](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 使用可能な顧客税区分のリストに新しい区分を追加するには、チェックマークをクリックします。

   ![新しい税区分](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 製品税区分を追加

1. の下 _製品税区分_&#x200B;をクリックし、 **[!UICONTROL Add New Tax Class]**.

1. 次を入力します。 **[!UICONTROL Name]** 新しい税区分のテキスト・ボックス内の。

1. 使用可能な製品税区分のリストに新しい区分を追加するには、チェックマークをクリックします。

1. 完了したら、「 **[!UICONTROL Back]** ボタンバーで、 _税務処理基準_ グリッド。

## デフォルトの税金宛先

デフォルトの税金宛先設定によって、税金の計算の基礎として使用される国、都道府県、郵便番号が決まります。

**_計算のデフォルト税金宛先を設定する手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Tax]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Default Tax Destination Calculation]** 」セクションに入力します。

   ![デフォルトの税金宛先の計算](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Default Country]** 税金計算の基になる国に対して

1. 設定 **[!UICONTROL Default State]** 税の計算の基準として使用される州または都道府県に対して。

1. 設定 **[!UICONTROL Default Post Code]** 地方税の計算の基礎として使用される郵便番号。

1. 完了したら、「 **[!UICONTROL Save Config]**.
