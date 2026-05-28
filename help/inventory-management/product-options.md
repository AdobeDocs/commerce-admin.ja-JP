---
title: ' [!DNL Inventory Management] 製品オプションの設定'
description: ' [!DNL Inventory Management] 製品設定オプションの設定方法について説明します。'
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '910'
ht-degree: 0%

---

# [!DNL Inventory Management]製品オプションの設定

これらの設定は、編集した製品にのみ適用され、グローバル web サイト レベルですべての設定を上書きします。 _[!UICONTROL Sources]_セクションと_[!UICONTROL Advanced Inventory]_ ページを使用して、製品を編集する際にこれらの設定を変更します。

- ソース別の製品オプションの設定
- 高度な在庫管理のための製品オプションの設定

## ソース別の製品オプション

製品に対して[追加されたソース ](sources-add.md)ごとの数量と追加設定を設定します。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. 商品を編集モードで開きます。

1. **[!UICONTROL Sources]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、各ソースの製品設定を構成します。

   - **[!UICONTROL Qty]** （数量）の金額を入力します。

   - **[!UICONTROL Source Item Status]**&#x200B;を`In Stock`または`Out of Stock`に設定します。

   - 「ソースごとに数量を下回る場合に通知」を変更するには、「**[!UICONTROL Notify Quantity Use Default]**」チェックボックスをオフまたは選択します。

     クリアした場合は、商品の在庫切れの通知をトリガーする在庫レベルの金額を入力します。 入力された金額は、在庫レベルでの品目の販売可能数量から減算されます。

     `Select to use Default` - [!DNL Commerce]は、製品の詳細在庫オプションで構成設定を確認します。
     `Clear to Modify` - 「数量を通知」の値を入力し、詳細在庫およびストアの設定設定を上書きします。

   製品](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}の![ ソースセクション

1. 完了したら、**[!UICONTROL Done]**、**[!UICONTROL Save]**&#x200B;の順にクリックします。

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Source Code] | グローバル | [ ソース ](sources-manage.md)の一意のコード。 |
| [!UICONTROL Name] | グローバル | ソースの一意の名前。 |
| [!UICONTROL Status] | グローバル | 製品はカタログで有効または無効になっています。 |
| [!UICONTROL Source Item Status] | グローバル | 製品の現在の可用性を決定します。 オプション：<br />`In Stock` – 製品を購入可能にします。<br />`Out of Stock` - Backordersがアクティブ化されていない限り、製品は購入可能にならず、カタログからリストが削除されます。 |
| [!UICONTROL Qty] | グローバル | 各ソースまたは各所在地の手持在庫量。 |
| [!UICONTROL Notify Quantity] | グローバル | _[!UICONTROL Notify Quantity Use Default]_が選択されていない場合は、この特定のソースの_[!UICONTROL Notify for Quantity Below]_&#x200B;の金額。 |
| [!UICONTROL Notify Quantity Use Default] | グローバル | 製品&#x200B;_[!UICONTROL Advanced Inventory]_の_[!UICONTROL Notify for Quantity Below]_&#x200B;のデフォルト設定またはストア設定のグローバル設定を使用することを示します。 |

## 高度な製品オプション

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。

1. 商品を編集モードで開きます。

1. **[!UICONTROL Sources]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、**[!UICONTROL Advanced Inventory]**&#x200B;をクリックします。

1. カタログの[在庫管理](enable.md)を有効にするには、**[!UICONTROL Manage Stock]**&#x200B;を`Yes`に設定します。

   >[!NOTE]
   >
   >子製品の[!UICONTROL Manage Stock]設定は、設定可能な製品を上書きします。

   ![製品の詳細在庫](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Out-of-Stock Threshold]**&#x200B;の金額を入力：

   | 値 | 説明 |
   | ----- | ----- |
   | 正の金額 | _[!UICONTROL Backorders]_が無効な場合は、正の値を入力します。 |
   | ゼロ | _[!UICONTROL Backorders]_が有効になっている場合、`0`と入力すると、バックオーダーを無限に設定できます。 |
   | マイナス金額 | _[!UICONTROL Backorders]_が有効になっている場合は、負の値を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、`-50`と入力して、この金額までの注文を許可します。 |

1. **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**&#x200B;を入力します。

1. **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**&#x200B;を入力します。

1. 顧客が注文数量を入力する際に整数ではなく10進数値を使用できる場合は、**[!UICONTROL Qty uses Decimals]**&#x200B;を`Yes`に設定します。

1. 商品を多くのボックスで個別に販売できる場合は、**[!UICONTROL Allow Multiple Boxes for Shipping]**&#x200B;を`Yes`に設定します。 このオプションは、**[!UICONTROL Qty Uses Decimals]**&#x200B;が`Yes`のみに設定されている場合にのみ表示されます。

1. **[!UICONTROL Backorders]**&#x200B;を次のいずれかに設定します：

   | オプション | 説明 |
   | ----- | ----- |
   | `No Backorders` | 在庫切れの際に取り寄せ注文を受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回ったときに取り寄せ注文を受け付ける。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回ったときに取り寄せ注文を受け付け、注文を引き続き行うことができることを顧客に通知します。 |

   詳しくは、[ バックオーダーの設定](backorders.md)を参照してください。

1. 製品の数量の増分をアクティブにするには、**[!UICONTROL Enable Qty Increments]**&#x200B;を`Yes`に設定し、**[!UICONTROL Qty Increments]** フィールドに、要件を満たすために購入する必要がある品目の数を入力します。

   たとえば、6単位で販売された商品は、6、12、18等単位で購入することができます。

   **[!UICONTROL Qty Increments]** フィールドは、1つの製品として、また設定可能なグループ化された製品およびバンドル製品の子として購入する必要がある製品項目の数を設定します。

1. 完了したら、**[!UICONTROL Done]**&#x200B;をクリックし、**[!UICONTROL Save]**&#x200B;をクリックします。

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Manage Stock] | グローバル | この商品をカタログで管理するために在庫管理を使用するかどうかを指定します。 すべての[!DNL Inventory Management]機能を有効または無効に設定します。 返品またはクレジットメモを完了すると、製品数量は影響を受けるソース数量に自動的に返されます。 サードパーティのERPを使用している場合は、無効にすることもできます。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 商品が在庫切れと見なされる在庫レベルを指定します。 オプション：<br />正の値 – バックオーダーが無効になっている場合は、正の金額を入力します。<br /> ゼロ （0） – バックオーダーが有効になっている場合、ゼロを入力すると、バックオーダーを無限に設定できます。<br /> マイナス値 – 取り寄せ注文を有効にすると、マイナスの金額を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、`-50`と入力して、この金額までの注文を許可します。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 1回の注文で購入できる商品の最小数を指定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | グローバル | 1回の注文で購入できる製品の最大数を指定します。 |
| [!UICONTROL Qty Uses Decimals] | グローバル | 顧客が注文数量を入力する際に、整数ではなく10進数の値を使用できるかどうかを指定します。 オプション：<br />`Yes` – 値を整数ではなく小数として入力できます。 小数点以下桁は、重量、数量、長さごとに販売される商品に適しています。<br />`No`  – 数量の値は整数で入力する必要があります。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | グローバル | 製品の一部を別々に出荷できるかどうかを判断します。 このオプションは、**[!UICONTROL Qty Uses Decimals]** = `Yes`の場合に表示されます。 |
| [!UICONTROL Backorders] | グローバル | バックオーダーの管理方法を決定します。 バックオーダーでは、オーダーの処理ステータスは変更されません。 商品が在庫があるかどうかにかかわらず、注文が行われた時点で、資金は引き続き承認されるか、すぐに獲得されます。 商品は発売後に発送されます。 有効にすると、在庫切れしきい値にマイナスの金額を入力することをお勧めします。 オプション：<br/>`No Backorders` – 商品が在庫切れの場合、取り寄せ注文を受け付けません。<br />`Allow Qty Below 0`  – 数量がゼロを下回ったときに取り寄せ注文を受け付けます。<br />`Allow Qty Below 0 and Notify Customer`  – 数量がゼロを下回ったときにバックオーダーを受け付けますが、注文を引き続き行うことができることを顧客に通知します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 製品を増分販売できるかどうかを指定します。 増分は、1つの製品として、また設定可能なグループ化およびバンドル製品の子として購入する必要がある製品項目の数を設定します。 |

>[!NOTE]
>
>シンプルな製品設定は、特定の製品の設定可能な製品設定を上書きします。
