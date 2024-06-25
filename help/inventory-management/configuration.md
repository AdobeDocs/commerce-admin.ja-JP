---
title: '"設定 [!DNL Inventory Management]“'
description: 設定について説明します [!DNL Inventory Management] ソースの可用性、ストアフロント製品および注文出荷を決定するオプション。
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management]

この [!DNL Inventory Management] モジュールは、製品レベルおよびグローバルレベルで在庫設定をサポートし、ソースの可用性、ストアフロント製品および注文出荷に影響を与える追加設定も提供します。 設定は次の場合に適用されます。

- カタログ全体：に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. 次に、**[!UICONTROL Catalog]**左パネルでを選択し、**[!UICONTROL Inventory]**.

- 特定の製品：に移動 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. 次に、製品を編集モードで開き、 **[!UICONTROL Advanced Inventory]** が含まれる _[!UICONTROL Sources]_セクション。

カタログを設定して、ストアフロントに在庫データを表示したり、アクティブな買い物かごを管理したりできます。 各項目の可用性を次のように表示 _在庫あり_ または _在庫切れ_ 在庫が少ない場合に利用可能な在庫。

在庫切れのしきい値は、商品を再注文するタイミングを示し、在庫の販売可能数量から減算し、有効または無効なバックオーダーをサポートするように設定できます。 ストアのバックオーダーを許可し、すべてまたは特定の製品の最大注文数を設定します。

在庫可用性のしきい値を使用するもう 1 つの方法は、需要の高い製品を管理することです。 大量の購入者に販売するのではなく、新しい顧客を獲得したい場合は、最大数量を設定して、1 人の購入者が在庫全体を取り出さないようにすることができます。

![在庫があり、残りはたった 1 つの例](assets/storefront-stock-options-1-left.png)

## 設定オプション

[!DNL Commerce] ストアと製品は、製品、在庫、通知などを管理する次の設定をサポートしています。 [!DNL Commerce] バルクアクションと距離優先アルゴリズムの追加の設定を提供します。

| オプション | 説明 |
|--|--|
| [!UICONTROL Manage Stock] | 有効 [!DNL Commerce] すべての在庫を管理します。 在庫管理がこの製品または内のすべての製品に使用されるかどうかを設定します [!DNL Commerce]. に設定されている場合、さらにオプションを表示 `Yes`. |
| [!UICONTROL Only X left Threshold] | 特定の金額が購入できる状態になったときに通知する数量を設定します。 この金額は在庫レベルで追跡されます。 |
| [!UICONTROL Out-of-Stock Threshold] | 安全在庫、在庫切れ通知をトリガーするための数量、在庫切れのリスクを軽減するため。 この値はバックオーダーに影響します。 オプション：<br />**[!UICONTROL No Backorders]**：商品の在庫切れ時にバックオーダーを受け付けません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合にバックオーダーを受け入れます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合はバックオーダーを受け入れますが、オーダーを発注できる旨を顧客に通知します。<br /><br />**[!UICONTROL Backorders disabled]**:5 や 25 など、0 を超える正の値を入力することをお勧めします。 <br/>**[!UICONTROL Backorders enabled]**：許可されたバックオーダーの最大数量に負のしきい値（–5、-25 など）を入力します。 値 0 は無限の在庫として機能します。 正の値は無視され、0 として扱われます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 1 回の注文で購入できる商品の最小数量を設定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 1 回の注文で購入できる商品の最大数量を設定します。 |
| [!UICONTROL Qty Uses Decimals] | 製品の数量に対して、整数ではなく小数の金額を許可します。 この設定は、重量、体積、長さで販売される製品に役立ちます。 ソースのレベルで指定され、割り当てられたソースに基づいて在庫レベルで計算されます。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 製品の一部を個別に出荷できるかどうかを決定します。 このオプションは、次の場合に表示されます **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | バックオーダーが許可されているかどうかを示します。 ソースのレベルで指定され、割り当てられたソースに基づいて在庫レベルで計算されます。 バックオーダーを許可する場合は、在庫切れのしきい値に負の値を設定します（ [バックオーダーの設定](backorders.md)）をお勧めします。 オプション：<br />**[!UICONTROL No Backorders]**：商品の在庫切れ時にバックオーダーを受け付けません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合にバックオーダーを受け入れます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合はバックオーダーを受け入れますが、オーダーを発注できる旨を顧客に通知します。 |
| [!UICONTROL Notify for Quantity Below] | 低在庫を警告する「数量未満」のトリガーを示す数量を設定します。 この金額は、在庫数量からではなく、販売可能数量から差し引かれます。 |
| [!UICONTROL Enable Qty Increments] | 製品を数量単位で販売できるかどうかを決定します。 有効化されている場合は、増分手順で購入する必要がある製品の数量を入力します。 増分は、1 つの製品として、また設定可能な製品、グループ化された製品およびバンドル製品の子として購入する必要がある製品項目の数を設定します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] はこの値を使用しません。 返品またはクレジット・メモを完了すると、製品数量は影響を受けるソース数量に自動的に返品されます。 参照： [製品オプションの設定](product-options.md). |

## 設定のフォールバックと継承

設定は、次の継承パスで上書きまたは適用されます：製品 _[!UICONTROL Sources]_セクションが製品をオーバーライド_[!UICONTROL Advanced Options]_ グローバルを上書き _[!UICONTROL Inventory]_ストアの設定。

条件 [!DNL Commerce] カスタム設定が適用されるかどうかをチェックします。この順序は次のとおりです。

1. の製品レベルでカスタム設定をチェックします。 _[!UICONTROL Sources]_セクション。 いくつかの設定を使用できます。

1. 商品を確認します _[!UICONTROL Advanced Inventory]_設定。

1. 次の場合 `Use Config Settings` が製品設定に対して選択されている場合、グローバルの値をチェックします _在庫_ ストア設定ページ。

例えば、次のような設定を使用して、ストア間でバックオーダーを異なる方法で設定できます。

- _グローバル：_ 店舗のバックオーダーを有効にし、在庫切れのしきい値を次のように設定します `-50`

- _製品：_ 特定の商品のバックオーダーを無効にし、在庫切れのしきい値をに設定します `10`
