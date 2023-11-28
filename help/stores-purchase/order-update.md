---
title: 注文の更新
description: 管理者で顧客の注文を更新する方法を説明します。
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 注文の更新

注文をした顧客を支援する場合は、注文のステータスを決定する必要があります。 以下に対して使用可能なオプションを示します。 `Pending` 順序は、 `Processing` 注文。 詳しくは、 [オーダーを処理](order-processing.md).

## 保留中の注文

顧客が注文した後、支払いを受け取る前に注文が `Pending` ステータス。 オーダーを編集したり、保留にしたり、完全にキャンセルしたりできます。 保留中の注文のボタンバーには、注文で使用可能なアクションが一覧表示されます。

![保留中の注文オプション](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

オーダーの実質的な部分を変更すると、元のオーダーがキャンセルされ、新しいオーダーが生成されます。 ただし、新しい注文を生成せずに請求先住所や配送先住所を変更できます。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに注文ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | 管理者ユーザーが顧客の注文を支援できるようにします。 |
| **[!UICONTROL Cancel]** | 保留中のオーダーをキャンセルします。 |
| **[!UICONTROL Send Email]** | 保留中の注文に関する E メールを顧客に送信します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 保留中の注文のステータスをに変更します `On Hold`. 保留を解除するには、 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | を作成します。 [請求書](invoices.md#create-an-invoice) 注文を請求書に変換し、注文ステータスを「 `processing`. |
| **[!UICONTROL Ship]** | を作成します。 [出荷](shipments.md#create-a-shipment) 注文のレコード。 |
| **[!UICONTROL Reorder]** | 現在の保留中のオーダーの重複となる新しい保留中のオーダーを作成します。 |
| **[!UICONTROL Edit]** | 保留中のオーダーを編集モードで開きます。 「編集」ボタンは、保留中のオーダーに対して、またはネゴシエート済みに基づくオーダーに対してのみ使用できます [引用符](../b2b/quotes.md). |

{style="table-layout:auto"}

## 処理順序

注文が `Processing` 状態：

* 注文の支払が受け取られ、取り込まれ、請求書が生成される（支払処理が次のように設定されている場合） `Authorize and Capture`.
* 注文トランザクションは許可されていますが、支払いアクションが次のように設定されている場合、支払いはまだキャプチャされていません `Authorize`.

The [支払アクション設定](../configuration-reference/sales/payment-methods.md#payment-actions) オーダーの作成後に使用可能なオーダー処理を決定します。

大幅に `Processing` 注文の場合は、請求先住所と配送先住所を編集できます。

![処理順序オプション](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>支払い方法の支払い処理が次に設定されている場合： `Authorize and Capture`」を指定すると、顧客が注文する際に請求書が自動的に作成されます。 この状況では、 [クレジットメモ](credit-memo-create.md)が、 [解約](#cancel-a-pending-order) または [ボイド](#void-a-processing-order) 注文。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに注文ページに戻ります。 |
| **[!UICONTROL Send Email]** | 注文に関する電子メールを顧客に送信します。 |
| **[!UICONTROL Void]** | [空白](#void-a-processing-order) 注文トランザクション、または注文の一部トランザクション。 |
| **[!UICONTROL Credit Memo]** | を作成するプロセスを開始します。 [クレジットメモ](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 販売注文のステータスを次に変更します `On Hold`. 受注の保留を解除するには、次を選択します。 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | 現在のオーダーに基づいて、新しい保留中のオーダーを作成します。 |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerceのみ ) [戻る](returns.md) 注文から 1 つ以上の項目。 |

{style="table-layout:auto"}

## 処理順序を無効にする

注文がまだ `Processing` のステータスと支払いの統合が `Authorize` ( ではない `Authorize and Capture`) を無効にしたり、注文をキャンセルしたりすることができます。 [オーダーのキャンセル](#cancel-a-pending-order) また、認証を無効にします。

支払方法を使用して注文が行われたとき（支払処理がに設定されている場合） `Authorize and Capture` クレジットメモを使用して払い戻しを行うことはできますが、請求済みで支払が取り込まれているため、取り消すことはできません。

お客様の支払い方法によって、使用可能な支払い処理が決まります。 詳しくは、 [支払いアクション](../configuration-reference/sales/payment-methods.md#payment-actions) を参照してください。

**_受注を無効にする手順は、次のとおりです。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Adobe Analytics の **[!UICONTROL Action]** 列をクリックし、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Void]** 命令を無効にする

1. プロンプトで、 **[!UICONTROL OK]** 命令を無効にする

必要に応じて、 [クレジットメモ](credit-memo-create.md) 資金が回収された後 また、 [返品商品承認 (RMA)](returns.md) 製品返品用に発行されました。 詳しくは、 [オーダーの処理](order-processing.md).

## 保留中のオーダーの編集

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Adobe Analytics の **[!UICONTROL Action]** 列をクリックし、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Edit]**.

   ![注文を編集](./assets/order-edit.png){width="600" zoomable="yes"}

1. プロンプトで、 **[!UICONTROL OK]** をクリックして編集を続行します。

1. 必要に応じて注文を更新します。

1. 変更を適用します。
   * 請求または配送先住所に加えた変更を保存するには、 **[!UICONTROL Save]**.
   * 行項目に加えた変更を保存し、順序を再処理するには、 **[!UICONTROL Submit Order]**.

## 注文を保留にする

顧客の希望する支払い方法が利用できない場合、または品目が一時的に在庫切れの場合、注文を保留にすることができます。

1. Adobe Analytics の _購入回数_ グリッド、 `Pending` 保留にする注文。

1. Adobe Analytics の _アクション_ 列、クリック **[!UICONTROL View]**.

1. クリック **[!UICONTROL Hold]** 注文を保留にする

注文の保留を解除するには、注文を再度編集し、 **[!UICONTROL Unhold]**.

## 保留中のオーダーをキャンセル

オーダーをキャンセルすると、ステータスが「 」から変更されます。 `Pending` から `Canceled`.

1. Adobe Analytics の _[!UICONTROL Orders]_グリッドで、キャンセルする保留中のオーダーを検索します。

1. Adobe Analytics の _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL View]**.

1. クリック **[!UICONTROL Cancel]** ：オーダーをキャンセルします。

注文のステータスが次のとおりです `Canceled`.
