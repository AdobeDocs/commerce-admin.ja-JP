---
title: 注文を更新
description: 管理者で顧客の注文を更新する方法を説明します。
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 注文を更新

注文を行ったお客様を支援する場合、注文のステータスを決定する必要があります。 に使用可能なオプション `Pending` 順序は、のオプションとは異なります `Processing` オーダー。 詳しくは、を参照してください [オーダーを処理](order-processing.md).

## 保留中の注文

顧客が注文した後、支払いを受け取る前に、注文は `Pending` ステータス。 注文を編集したり、保留にしたり、完全にキャンセルしたりできます。 保留中の注文のボタンバーには、注文に使用できるアクションのリストが表示されます。

![保留中の注文オプション](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

オーダーの大部分を変更すると、元のオーダーがキャンセルされ、新しいオーダーが生成されます。 ただし、新しい注文を生成せずに請求先または配送先住所を変更することはできます。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに [ 受注 ] ページに戻ります。 |
| **[!UICONTROL Login as Customer]** | 管理者ユーザーが、顧客の注文を支援できるようにします。 |
| **[!UICONTROL Cancel]** | 保留中の注文をキャンセルします。 |
| **[!UICONTROL Send Email]** | 保留中の注文に関するメールを顧客に送信します。 |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 保留中の注文の状態を次に変更します `On Hold`. 保留を解除するには、 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | を作成します [請求書](invoices.md#create-an-invoice) 受注を請求書に変換して「保留中受注」から、受注ステータスを「変更」に変更します。 `processing`. |
| **[!UICONTROL Ship]** | を作成 [出荷](shipments.md#create-a-shipment) 注文のレコード。 |
| **[!UICONTROL Reorder]** | 現在の保留中の注文と重複する新しい保留中の注文を作成します。 |
| **[!UICONTROL Edit]** | 保留中の注文を編集モードで開きます。 「編集」ボタンは、保留中の受注、または交渉済に基づく受注にのみ使用できます [引用符](../b2b/quotes.md). |

{style="table-layout:auto"}

## オーダーの処理

注文が入る `Processing` 状態：

* 注文の支払いが受領/キャプチャされ、支払いアクションが次のように設定されている場合に請求書が生成されます `Authorize and Capture`.
* 注文トランザクションは許可されますが、支払いアクションがに設定されている場合、支払いはまだキャプチャされません `Authorize`.

この [支払アクションの設定](../configuration-reference/sales/payment-methods.md#payment-actions) 注文の作成後に使用できる注文アクションを決定します。

を大幅に変更することはできません。 `Processing` 注文しますが、請求先と配送先住所を編集できます。

![処理順序オプション](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>支払方法の支払処理が次のように設定されている場合 `Authorize and Capture`の場合、顧客が注文すると請求書が自動的に作成されます。 この場合、を使用して資金を返金できます [クレジット メモ](credit-memo-create.md)が、できません [キャンセル](#cancel-a-pending-order) または [無効](#void-a-processing-order) オーダー。

| ボタン | 説明 |
|--- |--- |
| **[!UICONTROL Back]** | 変更を保存せずに [ 受注 ] ページに戻ります。 |
| **[!UICONTROL Send Email]** | 注文に関するメールを顧客に送信します。 |
| **[!UICONTROL Void]** | [ボイド](#void-a-processing-order) 受注取引または一部受注取引。 |
| **[!UICONTROL Credit Memo]** | を作成するプロセスを開始します。 [クレジット メモ](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 販売注文の状態を次のように変更します `On Hold`. 受注の保留を解除する手順は、次のとおりです。 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | 現在の注文に基づいて新しい保留中注文を作成します。 |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) （Adobe Commerceのみ）以下を行うプロセスを開始します [戻る](returns.md) オーダーからの 1 つ以上の品目。 |

{style="table-layout:auto"}

## 処理順序の無効化

注文がまだ注文に残っている場合 `Processing` ステータスで、支払い統合が「」に設定されている `Authorize` （ではない `Authorize and Capture`）、トランザクションの無効化または注文のキャンセルのみ可能です。 [オーダーのキャンセル](#cancel-a-pending-order) また、は認証を無効にします。

支払処理がに設定された支払方法を使用して注文が行われた場合 `Authorize and Capture` クレジット・メモを使用して資金を払い戻すことはできますが、請求され、支払いが取り込まれるため、取り消すことはできません。

お支払い方法によって、利用可能な支払いアクションが決まります。 参照： [支払いアクション](../configuration-reference/sales/payment-methods.md#payment-actions) を参照してください。

**_受注を無効にする手順は、次のとおりです。_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. が含まれる **[!UICONTROL Action]** 編集するオーダーの列で、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Void]** 注文を無効にします。

1. プロンプトに従って、 **[!UICONTROL OK]** 注文を無効にします。

必要な払い戻しを発行するには、 [クレジット メモ](credit-memo-create.md) 資金がキャプチャされた後。 以下を作成することもできます [返品承認（RMA）](returns.md) 商品の返品に対して発行されます。 詳しくは、 [オーダーの処理](order-processing.md).

## 保留中の注文を編集

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. が含まれる **[!UICONTROL Action]** 編集するオーダーの列で、 **[!UICONTROL View]**.

1. クリック **[!UICONTROL Edit]**.

   ![注文を編集](./assets/order-edit.png){width="600" zoomable="yes"}

1. プロンプトに従って、 **[!UICONTROL OK]** をクリックして編集を続行します。

1. 必要に応じて注文を更新します。

1. 変更を適用します。
   * 請求先住所または配送先住所に対する変更を保存するには、 **[!UICONTROL Save]**.
   * 明細品目に対する変更を保存し、受注を再処理するには、 **[!UICONTROL Submit Order]**.

## 注文を保留にする

お客様のご希望の支払い方法が利用できない場合、または商品が一時的に在庫切れの場合は、注文を保留にすることができます。

1. が含まれる _注文件数_ グリッド、を検索 `Pending` 保留にする注文。

1. が含まれる _アクション_ 列、クリック **[!UICONTROL View]**.

1. クリック **[!UICONTROL Hold]** 注文を保留にします。

注文の保留を解除するには、注文を再度編集し、 **[!UICONTROL Unhold]**.

## 保留中の注文をキャンセル

注文をキャンセルすると、そのステータスが次のように変更される： `Pending` 対象： `Canceled`.

1. が含まれる _[!UICONTROL Orders]_グリッドで、キャンセルする保留中の注文を検索します。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL View]**.

1. クリック **[!UICONTROL Cancel]** 注文をキャンセルします。

注文のステータスは「」になりました `Canceled`.
