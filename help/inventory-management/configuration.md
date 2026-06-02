---
title: ' [!DNL Inventory Management]の設定'
description: ソースの可用性、ストアフロント製品、および注文出荷を決定する [!DNL Inventory Management]  オプションの設定について説明します。
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# [!DNL Inventory Management]の設定

[!DNL Inventory Management] モジュールは、製品およびグローバルレベルでの在庫構成設定をサポートしており、ソースの可用性、ストアフロント製品、注文出荷に影響を与える追加設定も提供しています。 設定は次の場所に適用されます。

- カタログ全体：**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。 次に、左側のパネルで&#x200B;**[!UICONTROL Catalog]**&#x200B;を展開し、**[!UICONTROL Inventory]**&#x200B;を選択します。

- 特定の製品：**[!UICONTROL Catalog]** > **[!UICONTROL Products]**&#x200B;に移動します。 次に、製品を編集モードで開き、_[!UICONTROL Sources]_&#x200B;セクションの&#x200B;**[!UICONTROL Advanced Inventory]**&#x200B;をクリックします。

カタログを設定して、ストアフロントに在庫データを表示したり、アクティブなショッピングカートを管理したりできます。 各商品の在庫状況を&#x200B;_在庫中_&#x200B;または&#x200B;_在庫切れ_&#x200B;として表示し、在庫が少ない場合に利用可能な在庫を表示します。

在庫切れしきい値は、商品を再注文するタイミングを示し、在庫の販売可能数量から差し引き、バックオーダーの有効化または無効化をサポートするように設定できます。 実店舗での取り寄せ注文を許可し、すべての商品または特定の商品の最大注文数を設定します。

在庫可用性のしきい値を使用するもうひとつの方法は、需要の高い商品を管理することです。 数量の多いバイヤーに販売するのではなく、新規顧客を獲得したい場合は、1人のバイヤーが在庫全体を取り出さないように、最大数量を設定できます。

![在庫内の例、残り1個のみ](assets/storefront-stock-options-1-left.png)

## 設定オプション

[!DNL Commerce]のストアと製品は、製品、在庫、通知などを管理するための次の構成をサポートしています。 [!DNL Commerce]には、一括アクションと距離優先アルゴリズムの追加の設定設定が用意されています。

| オプション | 説明 |
|--|--|
| [!UICONTROL Manage Stock] | [!DNL Commerce]がすべての在庫を管理できるようにします。 この製品または[!DNL Commerce]のすべての製品に在庫管理を使用するかどうかを設定します。 `Yes`に設定すると、さらにオプションが表示されます。 |
| [!UICONTROL Only X left Threshold] | 特定の金額が購入可能な状態になったときに通知する数量を設定します。 この金額は在庫レベルで追跡されます。 |
| [!UICONTROL Out-of-Stock Threshold] | お客様の安全在庫、在庫切れ通知をトリガーするための数量、および在庫切れのリスクを軽減するための数量。 この値は取り寄せ注文に影響します。 オプション：<br />**[!UICONTROL No Backorders]**：商品が在庫切れの場合、取り寄せ注文は受け付けません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合は取り寄せ注文を受け付けます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合は取り寄せ注文を受け付けますが、注文を引き続き行うことができることを顧客に通知します。<br /><br />**[!UICONTROL Backorders disabled]**: 5または25など、0より大きい値を入力することをお勧めします。 <br/>**[!UICONTROL Backorders enabled]**: -5または–25など、許可されるバックオーダーの最大数量に対する負のしきい値を入力します。 値が0の場合は、無限ストックとして機能します。 正の値は無視され、0として扱われます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 1回の注文で購入できる商品の最小数量を設定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 1回の注文で購入できる商品の最大数量を設定します。 |
| [!UICONTROL Qty Uses Decimals] | 製品の数量に対して、整数ではなく10進数を許可します。 この設定は、重量、数量、長さごとに販売される製品に役立ちます。 割り当てられたソースに基づいてStock レベルで計算される、Sourceのレベルで指定されます。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 製品の一部を別々に出荷できるかどうかを判断します。 このオプションは、**[!UICONTROL Qty Uses Decimals]** = `Yes`の場合に表示されます。 |
| [!UICONTROL Backorders] | バックオーダーが許可されているかどうかを示します。 割り当てられたソースに基づいてStock レベルで計算される、Sourceのレベルで指定されます。 取り寄せ注文を許可するように有効にした場合は、在庫切れしきい値に負の値を設定することをお勧めします（[取り寄せ注文の設定](backorders.md)を参照）。 オプション：<br />**[!UICONTROL No Backorders]**：商品が在庫切れの場合、取り寄せ注文は受け付けません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合は取り寄せ注文を受け付けます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合は取り寄せ注文を受け付けますが、注文を引き続き行うことができることを顧客に通知します。 |
| [!UICONTROL Notify for Quantity Below] | 「数量を下回る」通知をトリガーする数量（在庫が少ないことを示す）を設定します。 この金額は、在庫数量からではなく、販売可能数量から差し引かれます。 |
| [!UICONTROL Enable Qty Increments] | 製品を増分販売できるかどうかを指定します。 有効な場合は、増分ステップで購入する必要がある製品の数量を入力します。 増分は、1つの製品として、また設定可能なグループ化およびバンドル製品の子として購入する必要がある製品項目の数を設定します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management]はこの値を使用しません。 返品またはクレジットメモを完了すると、製品数量は影響を受けるソース数量に自動的に返されます。 [製品オプションの設定](product-options.md)を参照してください。 |

## 設定のフォールバックと継承

設定は、継承の次のパスで上書きまたは適用されます。製品&#x200B;_[!UICONTROL Sources]_&#x200B;セクションは、製品&#x200B;_[!UICONTROL Advanced Options]_&#x200B;がグローバル _[!UICONTROL Inventory]_&#x200B;ストア設定を上書きします。

[!DNL Commerce]が適用するカスタム設定を確認する場合、次の順序に従います。

1. _[!UICONTROL Sources]_&#x200B;セクションの製品レベルでカスタム設定を確認します。 いくつかの設定を使用できます。

1. 製品&#x200B;_[!UICONTROL Advanced Inventory]_&#x200B;の設定を確認します。

1. 製品設定に「`Use Config Settings`」が選択されている場合、グローバルな&#x200B;_インベントリ_ ストア設定ページから値がチェックされます。

例えば、次のような設定を使用して、ストア全体で異なる取り寄せ注文を設定できます。

- _Globally :_ストアのバックオーダーを有効にし、在庫切れしきい値を`-50`に設定します

- _Product :_特定の製品のバックオーダーを無効にし、在庫切れしきい値を`10`に設定します
