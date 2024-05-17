---
title: '"設定 [!DNL Inventory Management] 製品オプション」'
description: を設定する方法を説明します [!DNL Inventory Management] 製品の設定オプション。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management] 製品オプション

これらの設定は、編集された製品にのみ適用され、グローバル web サイトレベルのすべての設定を上書きします。 製品の編集時に、次を使用してこれらの設定を変更します _[!UICONTROL Sources]_セクションと_[!UICONTROL Advanced Inventory]_ ページ。

- ソース別の製品オプションの設定
- 詳細在庫用の製品オプションの構成

## ソース別の製品オプション

次の単位で数量と追加設定を構成します [追加されたソース](sources-add.md) 商品の場合。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Sources]** セクションを開き、各ソースの製品設定を指定します。

   - を入力 **[!UICONTROL Qty]** （数量）金額。

   - を **[!UICONTROL Source Item Status]** as `In Stock` または `Out of Stock`.

   - ソースごとの以下の数量の通知を変更するには、をクリアするか、 **[!UICONTROL Notify Quantity Use Default]** チェックボックス。

     オフにした場合は、在庫切れ通知をトリガーにする在庫レベルの金額を入力します。 入力した金額は、在庫レベルで品目の販売可能数量から減算されます。

     `Select to use Default` - [!DNL Commerce] 製品の詳細在庫オプションで構成設定を確認します。
     `Clear to Modify` - 「Advanced Inventory and Store」構成設定を上書きして、「Notify Quantity」に値を入力します。

   ![製品の「ソース」セクション](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 完了したら、 **[!UICONTROL Done]**、次に **[!UICONTROL Save]**.

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Source Code] | グローバル | の一意のコード [ソース](sources-manage.md). |
| [!UICONTROL Name] | グローバル | ソースの一意の名前。 |
| [!UICONTROL Status] | グローバル | 製品がカタログで有効または無効になっている。 |
| [!UICONTROL Source Item Status] | グローバル | 商品の現在の可用性を決定します。 オプション：<br />`In Stock`  – 製品を購入できるようにします。<br />`Out of Stock` - バックオーダーが有効化されていない限り、は商品を購入できないようにし、カタログからリストを削除します。 |
| [!UICONTROL Qty] | グローバル | ソースまたは事業所ごとの手持在庫金額。 |
| [!UICONTROL Notify Quantity] | グローバル | の金額 _[!UICONTROL Notify for Quantity Below]_この特定のソースに対して_[!UICONTROL Notify Quantity Use Default]_ が選択されていません。 |
| [!UICONTROL Notify Quantity Use Default] | グローバル | デフォルト設定を使用することを示します _[!UICONTROL Notify for Quantity Below]_製品の_[!UICONTROL Advanced Inventory]_ またはストア設定のグローバル設定です。 |

## 高度な製品オプション

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 製品を編集モードで開きます。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Sources]** セクションでクリック **[!UICONTROL Advanced Inventory]**.

1. を有効にする [在庫管理](enable.md) カタログに対して、を設定します **[!UICONTROL Manage Stock]** 対象： `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] 子製品の設定は、設定可能な製品を上書きします。

   ![製品の詳細在庫](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. の金額を入力 **[!UICONTROL Out-of-Stock Threshold]**:

   | 値 | 説明 |
   | ----- | ----- |
   | 正の金額 | （を使用） _[!UICONTROL Backorders]_無効にする場合は、正の値を入力します。 |
   | ゼロ | （を使用） _[!UICONTROL Backorders]_有効、入力する `0` 無制限のバックオーダーが可能になります。 |
   | マイナスの金額 | （を使用） _[!UICONTROL Backorders]_有効にする場合は、負の値を入力することをお勧めします。 金額は販売可能数量に追加されます。 例えば、 `-50` この金額までの注文を許可します。 |

1. を入力 **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. を入力 **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. を設定 **[!UICONTROL Qty uses Decimals]** 対象： `Yes` 顧客が注文数量の入力時に整数ではなく小数値を使用できる場合。

1. を設定 **[!UICONTROL Allow Multiple Boxes for Shipping]** 対象： `Yes` 製品が別々に販売できる場合は、多くの箱に。 このオプションは、次の場合に表示されます **[!UICONTROL Qty Uses Decimals]** はに設定されています。 `Yes` のみ。

1. を設定 **[!UICONTROL Backorders]** を次のいずれかに変更します。

   | オプション | 説明 |
   | ----- | ----- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーを発注できることを通知します。 |

   詳しくは、を参照してください [バックオーダーの設定](backorders.md).

1. 製品の増分量を有効にするには、を設定します **[!UICONTROL Enable Qty Increments]** 対象： `Yes` で要件を満たすために購入する必要がある品目の数を入力します **[!UICONTROL Qty Increments]** フィールド。

   例えば、6 ずつ増分して販売される商品は、6、12、18 などの数量で購入できます。

1. 完了したら、 **[!UICONTROL Done]** その後 **[!UICONTROL Save]**.

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Manage Stock] | グローバル | カタログでこの商品を管理するために在庫管理を使用するかどうかを決定します。 すべてを有効化または無効化に設定 [!DNL Inventory Management] 機能。 返品またはクレジット・メモを完了すると、製品数量は影響を受けるソース数量に自動的に返品されます。 サードパーティの ERP システムを使用している場合は、無効にした方がよいでしょう。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 商品が在庫切れとみなされる在庫レベルを決定します。 オプション：<br />正の値 – バックオーダーを使用不可にした場合は、正の金額を入力します。<br />ゼロ（0）: 「バックオーダー」が使用可能になっている場合は、ゼロを入力すると無制限のバックオーダーが可能になります。<br />マイナス値：バックオーダーが使用可能な場合は、マイナスの金額の入力をお薦めします。 金額は販売可能数量に追加されます。 例えば、 `-50` この金額までの注文を許可します。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる商品の最小数を決定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる商品の最大数を決定します。 |
| [!UICONTROL Qty Uses Decimals] | グローバル | 顧客が注文数量を入力する際に、整数ではなく小数値を使用できるかどうかを決定します。 オプション：<br />`Yes`  – 値を整数ではなく小数として入力できます。 小数は、重量、体積、長さで販売される製品に適しています。<br />`No`  – 数量値を整数として入力する必要があります。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | グローバル | 製品の一部を個別に出荷できるかどうかを決定します。 このオプションは、次の場合に表示されます **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | グローバル | バックオーダーの管理方法を決定します。 バックオーダーによってオーダーの処理ステータスが変更されることはありません。 ファンドは、商品が在庫しているかどうかに関係なく、注文が行われるとすぐに承認または取得されます。 製品は出荷され次第、出荷されます。 有効にする場合は、在庫切れのしきい値に負の値を入力することをお勧めします。 オプション：<br/>`No Backorders`  – 商品の在庫切れ時にバックオーダーを受け付けません。<br />`Allow Qty Below 0`  – 数量がゼロを下回った場合にバックオーダーを受け入れます。<br />`Allow Qty Below 0 and Notify Customer`  – 数量がゼロを下回った場合はバックオーダーを受け入れますが、オーダーは引き続き発注可能であることを顧客に通知します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 製品を数量単位で販売できるかどうかを決定します。 |

>[!NOTE]
>
>シンプルな製品設定は、特定の製品の設定可能な製品設定を上書きします。
