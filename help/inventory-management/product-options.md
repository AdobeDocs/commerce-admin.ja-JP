---
title: '"設定" [!DNL Inventory Management] 製品オプション»'
description: 設定方法を学ぶ [!DNL Inventory Management] 製品設定オプション。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] 製品オプション

これらの設定は、編集された製品にのみ適用され、グローバル Web サイトレベルのすべての設定を上書きします。 製品の編集時に、 _[!UICONTROL Sources]_セクションと_[!UICONTROL Advanced Inventory]_ ページに貼り付けます。

- ソース別の製品オプションの設定
- 高度な在庫用の製品オプションの設定

## ソース別の製品オプション

数量と追加設定を次の単位で設定します。 [追加されたソース](sources-add.md) 製品の。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Sources]** 」セクションで、各ソースの製品設定を指定します。

   - を入力します。 **[!UICONTROL Qty]** （数量）金額。

   - を設定します。 **[!UICONTROL Source Item Status]** as `In Stock` または `Out of Stock`.

   - 「次の数量の通知」をソースごとに変更するには、「次の数量を通知」チェックボックスをオフにするか、 **[!UICONTROL Notify Quantity Use Default]** チェックボックス。

     オフにした場合は、品目の在庫切れ通知をトリガーする在庫レベルの金額を入力します。 入力された金額は、在庫レベルで品目の売上可能数量から差し引かれます。

     `Select to use Default` - [!DNL Commerce] 製品の [ 高度な在庫 ] オプションで設定を確認します。
     `Clear to Modify` - 「通知数量」の値を入力し、「高度な在庫」および「保管」構成設定を上書きします。

   ![製品のソースセクション](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Done]**&#x200B;を、 **[!UICONTROL Save]**.

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Source Code] | グローバル | の一意のコード [ソース](sources-manage.md). |
| [!UICONTROL Name] | グローバル | ソースの一意の名前。 |
| [!UICONTROL Status] | グローバル | カタログで製品が有効または無効になっています。 |
| [!UICONTROL Source Item Status] | グローバル | 製品の現在の可用性を決定します。 オプション：<br />`In Stock`  — 製品を購入できるようにします。<br />`Out of Stock` - Backorders が有効化されていない場合、は製品の購入を禁止し、カタログからリストを削除します。 |
| [!UICONTROL Qty] | グローバル | 各ソースまたは場所の手持在庫金額。 |
| [!UICONTROL Notify Quantity] | グローバル | の金額 _[!UICONTROL Notify for Quantity Below]_次の場合にこの特定のソースの_[!UICONTROL Notify Quantity Use Default]_ が選択されていません。 |
| [!UICONTROL Notify Quantity Use Default] | グローバル | のデフォルト設定を使用することを示します。 _[!UICONTROL Notify for Quantity Below]_製品内_[!UICONTROL Advanced Inventory]_ またはストア設定のグローバル設定。 |

## 高度な製品オプション

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Sources]** 「 」セクションで、「 」をクリックします。 **[!UICONTROL Advanced Inventory]**.

1. 有効にするには [在庫管理](enable.md) カタログに対して、 **[!UICONTROL Manage Stock]** から `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] 子製品の設定は、設定可能な製品を上書きします。

   ![製品の高度な在庫](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 次の金額を入力： **[!UICONTROL Out-of-Stock Threshold]**:

   | 値 | 説明 |
   | ----- | ----- |
   | 正の金額 | を使用 _[!UICONTROL Backorders]_無効、正の値を入力します。 |
   | ゼロ | を使用 _[!UICONTROL Backorders]_有効、入力 `0` では、無限の逆オーダーが可能です。 |
   | 負の金額 | を使用 _[!UICONTROL Backorders]_有効にする場合は、負の値を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、 `-50` ：この金額までの注文を許可します。 |

1. 次を入力します。 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. 次を入力します。 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. 設定 **[!UICONTROL Qty uses Decimals]** から `Yes` 注文された数量を入力する際に、顧客が整数ではなく小数値を使用できる場合。

1. 設定 **[!UICONTROL Allow Multiple Boxes for Shipping]** から `Yes` 製品が別々に販売できる場合は、多くの箱で。 このオプションは、 **[!UICONTROL Qty Uses Decimals]** が `Yes` のみ。

1. 設定 **[!UICONTROL Backorders]** を次のいずれかに変更します。

   | オプション | 説明 |
   | ----- | ----- |
   | `No Backorders` | 製品が在庫切れの場合にバックオーダーを受け入れないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れる。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロ未満の場合にバックオーダーを受け入れ、オーダーがまだ可能であることを顧客に通知する。 |

   詳しくは、 [バックオーダーの設定](backorders.md).

1. 製品の数量増分を有効にするには、 **[!UICONTROL Enable Qty Increments]** から `Yes` をクリックし、必要に応じて購入する必要がある品目の数を **[!UICONTROL Qty Increments]** フィールドに入力します。

   例えば、6 個の単位で販売される品目は、6 個、12 個、18 個などの数量で購入できます。

1. 完了したら、「 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Manage Stock] | グローバル | カタログでこの商品を管理するために在庫管理を使用するかどうかを決定します。 すべてを有効または無効にするには、を設定します。 [!DNL Inventory Management] 機能。 返品またはクレジット・メモを完了すると、製品数量は影響を受けるソース数量に自動的に戻されます。 サードパーティの ERP システムを使用している場合は、を無効にすることができます。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 製品が在庫切れと見なされる在庫レベルを決定します。 オプション：<br />正の値 — バックオーダーを無効にした場合は、正の値を入力します。<br />ゼロ (0) - 「バックオーダー」を有効にした場合、ゼロを入力すると無限バックオーダーが可能になります。<br />負の値 — バックオーダーを有効にした場合、負の金額を入力することをお勧めします。 金額が販売可能数量に追加されます。 例えば、 `-50` ：この金額までの注文を許可します。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる製品の最小数を決定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる製品の最大数を指定します。 |
| [!UICONTROL Qty Uses Decimals] | グローバル | 注文された数量を入力する際に、顧客が整数ではなく小数値を使用できるかどうかを指定します。 オプション：<br />`Yes`  — 値を整数ではなく小数で入力できます。 小数は、重量、体積または長さで販売される製品に適しています。<br />`No`  — 数量の値は整数で入力する必要があります。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | グローバル | 製品の部品を別々に出荷できるかどうかを指定します。 このオプションは、 **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | グローバル | バックオーダーの管理方法を決定します。 バックオーダーでは、オーダーの処理ステータスは変更されません。 商品が在庫にあるかどうかに関係なく、注文が行われると、資金は引き続き直ちに承認または取得されます。 製品は、利用可能になると出荷されます。 有効にした場合は、「在庫切れしきい値」に負の金額を入力することをお勧めします。 オプション：<br/>`No Backorders`  — 製品が在庫切れの場合は、バックオーダーを受け入れません。<br />`Allow Qty Below 0`  — 数量がゼロを下回った場合は、バックオーダーを受け入れます。<br />`Allow Qty Below 0 and Notify Customer`  — 数量がゼロを下回った場合はバックオーダーを受け入れますが、注文は依然として発注可能であることを顧客に通知します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 製品を数量単位で販売できるかどうかを指定します。 |

>[!NOTE]
>
>単純な製品設定は、特定の製品の設定可能な製品設定を上書きします。
