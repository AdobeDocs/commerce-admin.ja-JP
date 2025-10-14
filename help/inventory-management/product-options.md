---
title: 設定  [!DNL Inventory Management]  製品オプション
description: 製品設定オプションを設定する方法  [!DNL Inventory Management]  説明します。
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# [!DNL Inventory Management] 製品オプションの設定

これらの設定は、編集された製品にのみ適用され、グローバル web サイトレベルのすべての設定を上書きします。 製品の編集時に、_[!UICONTROL Sources]_&#x200B;のセクションと&#x200B;_[!UICONTROL Advanced Inventory]_ のページで、これらの設定を変更します。

- ソース別の製品オプションの設定
- 詳細在庫用の製品オプションの構成

## ソース別の製品オプション

製品の [&#x200B; 追加ソース &#x200B;](sources-add.md) ごとに数量と追加設定を指定します。

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品を編集モードで開きます。

1. **[!UICONTROL Sources]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、各ソースの製品設定を指定します。

   - **[!UICONTROL Qty]** （数量）金額を入力します。

   - **[!UICONTROL Source Item Status]** を `In Stock` または `Out of Stock` に設定します。

   - ソースごとの「次の数量を通知」を変更するには、「**[!UICONTROL Notify Quantity Use Default]**」チェックボックスを選択または選択解除します。

     オフにした場合は、在庫切れ通知をトリガーにする在庫レベルの金額を入力します。 入力した金額は、在庫レベルで品目の販売可能数量から減算されます。

     `Select to use Default` - [!DNL Commerce] は、設定について製品の詳細在庫オプションを確認します。
     `Clear to Modify` - 「Advanced Inventory and Store」構成設定を上書きして、「Notify Quantity」に値を入力します。

   ![&#x200B; 製品の「ソース」セクション &#x200B;](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Done]**」をクリックし、「**[!UICONTROL Save]**」をクリックします。

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Source Code] | グローバル | [&#x200B; ソース &#x200B;](sources-manage.md) の一意のコード。 |
| [!UICONTROL Name] | グローバル | ソースの一意の名前。 |
| [!UICONTROL Status] | グローバル | 製品がカタログで有効または無効になっている。 |
| [!UICONTROL Source Item Status] | グローバル | 商品の現在の可用性を決定します。 オプション：<br />`In Stock` – 製品を購入できるようにします。<br />`Out of Stock` - バックオーダーが有効化されていない限り、は商品を購入できないようにし、カタログからリストを削除します。 |
| [!UICONTROL Qty] | グローバル | ソースまたは事業所ごとの手持在庫金額。 |
| [!UICONTROL Notify Quantity] | グローバル | _[!UICONTROL Notify Quantity Use Default]_&#x200B;が選択されていない場合のこの特定のソースの&#x200B;_[!UICONTROL Notify for Quantity Below]_ の金額。 |
| [!UICONTROL Notify Quantity Use Default] | グローバル | 製品 _[!UICONTROL Advanced Inventory]_&#x200B;定の&#x200B;_[!UICONTROL Notify for Quantity Below]_ のデフォルト設定、またはストア設定のグローバル設定を使用することを示します。 |

## 高度な製品オプション

1. _管理者_ サイドバーで、**[!UICONTROL Catalog]**/**[!UICONTROL Products]** に移動します。

1. 製品を編集モードで開きます。

1. 「![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) 「**[!UICONTROL Sources]**」セクションを展開し、「**[!UICONTROL Advanced Inventory]**」をクリックします。

1. カタログの [&#x200B; 在庫管理 &#x200B;](enable.md) を有効にするには、「**[!UICONTROL Manage Stock]**」を「`Yes`」に設定します。

   >[!NOTE]
   >
   >子製品の設定 [!UICONTROL Manage Stock]、設定可能な製品を上書きします。

   ![&#x200B; 製品の詳細在庫 &#x200B;](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Out-of-Stock Threshold]** の金額を入力してください：

   | 値 | 説明 |
   | ----- | ----- |
   | 正の金額 | _[!UICONTROL Backorders]_&#x200B;を無効にした場合は、正の値を入力します。 |
   | ゼロ | _[!UICONTROL Backorders]_&#x200B;を有効にした場合、`0` と入力すると無制限のバックオーダーが可能になります。 |
   | マイナスの金額 | _[!UICONTROL Backorders]_&#x200B;を有効にする場合は、負の値を入力することをお勧めします。 金額は販売可能数量に追加されます。 例えば、この金額までの注文を許可するには、「`-50`」と入力します。 |

1. **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** を入力します。

1. **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** を入力します。

1. 顧客が注文数量を入力する際に、整数ではなく小数値を使用できる場合は、**[!UICONTROL Qty uses Decimals]** を `Yes` に設定します。

1. 製品が多数のボックスで個別に販売できる場合は、**[!UICONTROL Allow Multiple Boxes for Shipping]** を `Yes` に設定します。 このオプションは、**[!UICONTROL Qty Uses Decimals]** が `Yes` のみに設定されている場合に表示されます。

1. **[!UICONTROL Backorders]** を次のいずれかに設定します。

   | オプション | 説明 |
   | ----- | ----- |
   | `No Backorders` | 商品が在庫切れになった場合にバックオーダーを受け付けないようにする。 |
   | `Allow Qty Below 0` | 数量がゼロを下回った場合にバックオーダーを受け入れること。 |
   | `Allow Qty Below 0 and Notify Customer` | 数量がゼロを下回った場合にバックオーダーを受け入れ、顧客に対してオーダーを発注できることを通知します。 |

   詳しくは、「バックオーダーの設定 [&#x200B; を参照してください &#x200B;](backorders.md)。

1. 製品の数量増分を有効化するには、**[!UICONTROL Enable Qty Increments]** を `Yes` に設定し、**[!UICONTROL Qty Increments]** のフィールドに要件を満たすために購入する必要がある品目の数を入力します。

   例えば、6 ずつ増分して販売される商品は、6、12、18 などの数量で購入できます。

   フィールド **[!UICONTROL Qty Increments]**、1 つの製品として、また設定可能な製品、グループ化された製品およびバンドル製品の子として購入する必要がある製品項目の数を設定します。

1. 完了したら、「**[!UICONTROL Done]**」をクリックし、次に「**[!UICONTROL Save]**」をクリックします。

### フィールドの説明

| フィールド | 範囲 | 説明 |
|--|--|--|
| [!UICONTROL Manage Stock] | グローバル | カタログでこの商品を管理するために在庫管理を使用するかどうかを決定します。 設定するとすべての [!DNL Inventory Management] 機能が有効または無効になります。 返品またはクレジット・メモを完了すると、製品数量は影響を受けるソース数量に自動的に返品されます。 サードパーティの ERP システムを使用している場合は、無効にした方がよいでしょう。 |
| [!UICONTROL Out-of-Stock Threshold] | グローバル | 商品が在庫切れとみなされる在庫レベルを決定します。 オプション：<br /> 正の値 – バックオーダーを無効にして、正の金額を入力します。<br /> ゼロ（0）：バックオーダーが使用可能な場合、ゼロを入力すると無制限のバックオーダーが可能になります。<br /> マイナス値 – バックオーダーが使用可能な場合は、マイナス金額の入力をお薦めします。 金額は販売可能数量に追加されます。 例えば、この金額までの注文を許可するには、「`-50`」と入力します。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる商品の最小数を決定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | グローバル | 1 回の注文で購入できる商品の最大数を決定します。 |
| [!UICONTROL Qty Uses Decimals] | グローバル | 顧客が注文数量を入力する際に、整数ではなく小数値を使用できるかどうかを決定します。 オプション：<br />`Yes` – 値を整数ではなく小数として入力できます。 小数は、重量、体積、長さで販売される製品に適しています。<br />`No` – 数量値を整数として入力する必要があります。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | グローバル | 製品の一部を個別に出荷できるかどうかを決定します。 このオプションは、**[!UICONTROL Qty Uses Decimals]** = `Yes` の場合に表示されます。 |
| [!UICONTROL Backorders] | グローバル | バックオーダーの管理方法を決定します。 バックオーダーによってオーダーの処理ステータスが変更されることはありません。 ファンドは、商品が在庫しているかどうかに関係なく、注文が行われるとすぐに承認または取得されます。 製品は出荷され次第、出荷されます。 有効にする場合は、在庫切れのしきい値に負の値を入力することをお勧めします。 オプション：<br/>`No Backorders` – 商品が在庫切れの場合にバックオーダーを受け付けません。<br />`Allow Qty Below 0` – 数量がゼロを下回った場合にバックオーダーを受け入れます。<br />`Allow Qty Below 0 and Notify Customer`：数量がゼロを下回った場合はバックオーダーを受け入れますが、オーダーは引き続き発注可能であることを顧客に通知します。 |
| [!UICONTROL Enable Qty Increments] | グローバル | 製品を数量単位で販売できるかどうかを決定します。 増分は、1 つの製品として、また設定可能な製品、グループ化された製品およびバンドル製品の子として購入する必要がある製品項目の数を設定します。 |

>[!NOTE]
>
>シンプルな製品設定は、特定の製品の設定可能な製品設定を上書きします。
