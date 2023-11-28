---
title: '"設定" [!DNL Inventory Management]"'
description: の設定について説明します。 [!DNL Inventory Management] ソースの可用性、ストアフロント製品、および注文出荷を決定するオプション。
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# 設定 [!DNL Inventory Management]

The [!DNL Inventory Management] モジュールは、製品およびグローバルレベルで在庫構成設定をサポートし、ソースの可用性、ストアフロント製品、注文出荷に影響を与える追加の設定も提供します。 設定は次の場所に適用されます。

- カタログ全体：に移動します。 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. 次に、を展開します。**[!UICONTROL Catalog]**を選択し、**[!UICONTROL Inventory]**.

- 特定の製品：に移動します。 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. 次に、製品を編集モードで開き、 **[!UICONTROL Advanced Inventory]** （内） _[!UICONTROL Sources]_」セクションに入力します。

ストアフロントに在庫データを表示したり、アクティブな買い物かごを管理したりするようにカタログを設定できます。 各項目の可用性を次の形式で表示 _在庫あり_ または _在庫切れ_ 在庫が少ない場合に利用可能な在庫です。

在庫切れしきい値は、製品を再発注するタイミングを示し、在庫の売上数量から減算し、有効または無効のバックオーダーをサポートするように設定できます。 すべてのまたは特定の製品の最大注文数を設定して、店舗のバックオーダーを許可します。

在庫有効性しきい値を使用するもう 1 つの方法は、需要の高い製品を管理することです。 新規顧客を取り込む場合は、大量の購入者に販売するのではなく、最大数量を設定して、1 人の購入者が在庫全体を取り出さないようにすることができます。

![在庫ありの例、残り 1 件のみ](assets/storefront-stock-options-1-left.png)

## 設定オプション

[!DNL Commerce] ストアと製品は、製品、在庫、通知などの管理に関する次の設定をサポートしています。 [!DNL Commerce] には、バルクアクションと距離優先度アルゴリズムの追加設定が用意されています。

| オプション | 説明 |
|--|--|
| [!UICONTROL Manage Stock] | 有効 [!DNL Commerce] をクリックして、すべてのインベントリを管理します。 在庫管理がこの製品または [!DNL Commerce]. 次に設定すると、他のオプションが表示されます。 `Yes`. |
| [!UICONTROL Only X left Threshold] | 特定の金額が購入可能なままになった場合に通知する数量を設定します。 この金額は在庫レベルで追跡されます。 |
| [!UICONTROL Out-of-Stock Threshold] | お客様の安全在庫、在庫切れの通知をトリガーする数量、および在庫切れのリスクを軽減します。 この値はバックオーダーに影響します。 オプション：<br />**[!UICONTROL No Backorders]**：製品が在庫切れの場合は、バックオーダーを受け入れません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合にバックオーダーを受け入れます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合にバックオーダーを受け入れますが、引き続きオーダーをおこなうことができることを顧客に通知します。<br /><br />**[!UICONTROL Backorders disabled]**:0 を超える正の値（5、25 など）を入力することをお勧めします。 <br/>**[!UICONTROL Backorders enabled]**：許可されているバックオーダーの最大数量の負のしきい値（ —5 や —25 など）を入力します。 値 0 は無限在庫として機能します。 正の値は無視され、0 として扱われます。 |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 1 回の注文で購入できる製品の最小数量を設定します。 |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 1 回の注文で購入できる製品の最大数量を設定します。 |
| [!UICONTROL Qty Uses Decimals] | 製品の量に対して、整数ではなく小数の量を許可します。 この設定は、重量別、体積別、または長さ別に販売された製品に役立ちます。 ソースのレベルで指定し、割り当てられたソースに基づいて在庫レベルで計算されます。 |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 製品の部品を別々に出荷できるかどうかを指定します。 このオプションは、 **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | バックオーダーが許可されるかどうかを示します。 ソースのレベルで指定し、割り当てられたソースに基づいて在庫レベルで計算されます。 バックオーダーを許可する場合は、在庫切れしきい値に負の値を設定します ( [バックオーダーの設定](backorders.md)) を使用することをお勧めします。 オプション：<br />**[!UICONTROL No Backorders]**：製品が在庫切れの場合は、バックオーダーを受け入れません。<br />**[!UICONTROL Allow Qty Below 0]**：数量がゼロを下回った場合にバックオーダーを受け入れます。<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**：数量がゼロを下回った場合にバックオーダーを受け入れますが、引き続きオーダーをおこなうことができることを顧客に通知します。 |
| [!UICONTROL Notify for Quantity Below] | 在庫が少ない場合にトリガーする、「次の数量」通知を送信する数量を設定します。 この金額は、在庫数量からではなく、販売可能数量から控除されます。 |
| [!UICONTROL Enable Qty Increments] | 製品を数量単位で販売できるかどうかを指定します。 有効にした場合は、増分ステップで購入する必要がある製品の数量を入力します。 |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] ではこの値を使用しません。 返品またはクレジット・メモを完了すると、製品数量は影響を受けるソース数量に自動的に戻されます。 詳しくは、 [製品オプションの設定](product-options.md). |

## 設定のフォールバックと継承

継承の次のパスで設定を上書きまたは適用：製品 _[!UICONTROL Sources]_セクションが製品を上書き_[!UICONTROL Advanced Options]_ グローバルを上書き _[!UICONTROL Inventory]_ストアの設定。

条件 [!DNL Commerce] 適用するカスタム設定をチェックします。次の順序に従います。

1. 製品レベルで、 _[!UICONTROL Sources]_」セクションに入力します。 いくつかの設定を使用できます。

1. 製品をチェックします _[!UICONTROL Advanced Inventory]_設定。

1. 次の場合 `Use Config Settings` が製品設定に対して選択されている場合は、グローバル _在庫_ ストア設定ページ。

例えば、次のような設定を使用して、店舗間で異なる方法でバックオーダーを設定できます。

- _グローバル：_ ストアのバックオーダーを有効にし、在庫切れしきい値をに設定します。 `-50`

- _製品：_ 特定の製品のバックオーダーを無効にし、在庫切れしきい値をに設定します。 `10`
