---
title: 注文の更新
description: 管理画面で顧客の注文を更新する方法を説明します。
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# 注文の更新

注文した顧客を支援する場合は、注文のステータスを判断する必要があります。 `Pending`注文で使用できるオプションは、`Processing`注文のオプションとは異なります。 詳細については、[注文の処理](order-processing.md)を参照してください。

## 保留中の注文

顧客が注文した後、支払いを受け取る前の注文のステータスは`Pending`です。 注文を編集したり、保留にしたり、完全にキャンセルしたりできます。 保留中の注文のボタンバーには、注文で使用可能なアクションが一覧表示されます。

![保留中の注文オプション ](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

注文のかなりの部分を変更すると、元の注文がキャンセルされ、新しい注文が生成されます。 ただし、新しい注文を生成することなく、請求先住所または配送先住所を変更することができます。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに注文ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | 管理者ユーザーが顧客の注文を支援できるようにします。 |
| **[!UICONTROL Cancel]** | 保留中の注文をキャンセルします。 |
| **[!UICONTROL Send Email]** | 保留中の注文に関する電子メールを顧客に送信します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 保留中の注文のステータスを`On Hold`に変更します。 保留を解除するには、_[!UICONTROL Unhold]_を選択します。 |
| **[!UICONTROL Invoice]** | 注文を請求書に変換して、保留中の注文から[請求書](invoices.md#create-an-invoice)を作成し、注文ステータスを`processing`に変更します。 |
| **[!UICONTROL Ship]** | 注文の[出荷](shipments.md#create-a-shipment) レコードを作成します。 |
| **[!UICONTROL Reorder]** | 現在の保留中の注文の複製である新しい保留中の注文を作成します。 |
| **[!UICONTROL Edit]** | 編集モードで保留中の注文を開きます。 「編集」ボタンは、保留中の注文、または交渉された[見積](../b2b/quotes.md)に基づく注文でのみ使用できます。 |

{style="table-layout:auto"}

## 注文の処理

次の場合、注文は`Processing`状態になります。

* 支払いアクションが`Authorize and Capture`に設定されている場合、注文の支払いが受け取られ、請求書が生成されます。
* 注文取引は承認されていますが、支払いアクションが`Authorize`に設定されている場合、支払いはまだキャプチャされていません。

[支払いアクション設定](../configuration-reference/sales/payment-methods.md#payment-actions)は、注文の作成後に使用できる注文アクションを決定します。

`Processing`注文を大幅に変更することはできませんが、請求先住所と配送先住所を編集できます。

![注文オプションの処理](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>支払い方法の支払いアクションが`Authorize and Capture`に設定されている場合、顧客が注文すると請求書が自動的に作成されます。 この場合、[ クレジットメモ ](credit-memo-create.md)を使用して資金を返金できますが、[ キャンセル ](#cancel-a-pending-order)または[void](#void-a-processing-order)注文をキャンセルすることはできません。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに注文ページに戻ります。 |
| **[!UICONTROL Send Email]** | 注文に関する電子メールを顧客に送信します。 |
| **[!UICONTROL Void]** | [注文トランザクション、または部分的な注文トランザクションを](#void-a-processing-order)無効にします。 |
| **[!UICONTROL Credit Memo]** | [ クレジットメモ ](credit-memo-create.md)を作成するプロセスを開始します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 販売注文のステータスを`On Hold`に変更します。 販売注文の保留を解除するには、_[!UICONTROL Unhold]_を選択します。 |
| **[!UICONTROL Reorder]** | 現在の注文に基づいて、新しい保留中の注文を作成します。 |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）注文から1つ以上のアイテムを[return](returns.md)するプロセスを開始します。 |

{style="table-layout:auto"}

## 処理指示を無効にする

注文がまだ`Processing` ステータスであり、支払い統合が`Authorize` （`Authorize and Capture`ではなく）に設定されている場合、トランザクションを無効にするか、注文をキャンセルすることしかできません。 [注文のキャンセル ](#cancel-a-pending-order)も認証を無効にします。

支払いアクションが`Authorize and Capture`に設定された支払い方法を使用して注文が行われた場合、クレジットメモを使用して資金を返金できますが、請求され、支払いが取り込まれるため、キャンセルすることはできません。

お支払い方法によって利用可能なお支払い方法が決まります。 詳しくは、[支払いアクション ](../configuration-reference/sales/payment-methods.md#payment-actions)を参照してください。

**_注文を無効にするには:_**

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**に移動します。

1. 編集する注文の&#x200B;**[!UICONTROL Action]**&#x200B;列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. **[!UICONTROL Void]**&#x200B;をクリックして注文を無効にします。

1. プロンプトで「**[!UICONTROL OK]**」をクリックして、注文を無効にします。

資金が回収された後、[ クレジットメモ ](credit-memo-create.md)を使用して、必要な払い戻しを行うことができます。 返品用に発行された[返品商品認証（RMA） ](returns.md)を作成することもできます。 詳しくは、[注文の処理](order-processing.md)を参照してください。

## 保留中の注文の編集

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**に移動します。

1. 編集する注文の&#x200B;**[!UICONTROL Action]**&#x200B;列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. **[!UICONTROL Edit]**&#x200B;をクリックします。

   ![注文を編集](./assets/order-edit.png){width="600" zoomable="yes"}

1. プロンプトで、**[!UICONTROL OK]**&#x200B;をクリックして編集を続行します。

1. 必要に応じて注文を更新します。

1. 変更を適用します。
   * 請求先住所または配送先住所に加えた変更を保存するには、**[!UICONTROL Save]**&#x200B;をクリックします。
   * 行項目に加えた変更を保存して注文を再処理するには、**[!UICONTROL Submit Order]**&#x200B;をクリックします。

## 保留中の注文

顧客が希望する支払い方法がない場合、または商品が一時的に在庫切れの場合は、注文を保留にできます。

1. _注文_ グリッドで、保留にする`Pending`注文を見つけます。

1. _アクション_&#x200B;列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. **[!UICONTROL Hold]**&#x200B;をクリックして注文を保留します。

注文の保留を削除するには、注文をもう一度編集し、**[!UICONTROL Unhold]**&#x200B;をクリックします。

## 保留中の注文のキャンセル

注文をキャンセルすると、ステータスが`Pending`から`Canceled`に変更されます。

1. _[!UICONTROL Orders]_グリッドで、キャンセルする保留中の注文を見つけます。

1. _[!UICONTROL Action]_列で、**[!UICONTROL View]**をクリックします。

1. **[!UICONTROL Cancel]**&#x200B;をクリックして注文をキャンセルします。

注文のステータスは`Canceled`になりました。
