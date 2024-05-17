---
title: トランザクション
description: 取引ページと、それを使用してストアと支払いシステム間のアクティビティを追跡する方法について説明します。
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# トランザクション

この _トランザクション_ ページには、ストアと支払いシステムの間で発生したすべての支払いアクティビティが一覧表示され、より詳細な情報にアクセスできます。

## トランザクションの表示

日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![取引グリッド](./assets/transactions.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各トランザクションに割り当てられる一意の数値識別子。 |
| [!UICONTROL Order ID] | 顧客が注文を行うときに割り当てられる一意の ID。 |
| [!UICONTROL Transaction ID] | 顧客が注文した後にトランザクションが発生すると割り当てられる一意の数値識別子。 |
| [!UICONTROL Parent Transaction ID] | 親トランザクションの ID 番号。 |
| [!UICONTROL Payment Method] | トランザクションに関連付けられている支払い方法。 |
| [!UICONTROL Transaction Type] | トランザクションのタイプ。注文、承認、取得、無効、返金が可能です。 |
| [!UICONTROL Closed] | トランザクションがクローズされているかどうか。 |
| [!UICONTROL Created] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

## トランザクションの詳細の表示

表示するエントリをクリックします。

トランザクションの詳細ページには、トランザクションの詳細と子トランザクショングリッドが表示されます。

### トランザクションデータ

このセクションには、トランザクションに関する情報が含まれ、 **注文 ID** 列。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Transaction ID] | トランザクション ID 番号。 |
| [!UICONTROL Parent Transaction ID] | 該当する場合は、親トランザクションの対応する ID 番号。 |
| [!UICONTROL Transaction Type] | トランザクションのタイプ。注文、承認、取得、無効、返金が可能です。 |
| [!UICONTROL Is Closed] | トランザクションがクローズされているかどうか。 |
| [!UICONTROL Created At] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

### 子トランザクション

の請求書を作成すると、子トランザクションがグリッドに表示されます [注文件数](orders.md). この形式を使用すると、トランザクション階層に従ってトランザクション履歴を追跡できます。

### [!UICONTROL Transaction Details]

このセクションには、特定のトランザクションの追加情報が含まれます。 情報は、キーと値の形式で表示されます。 使用できるキーは次のとおりです。

- authAmount
- authCode
- VSResponse
- billTo
- cardCodeResponse
- 顧客
- customerIP
- lineItems
- marketType
- 順序
- 給付
- 製品
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleAmount
- 解決策
- submitTimeLocal
- submitTimeUTC
- taxExcempt
- transactionStatus

>[!NOTE]
>
>トランザクションの詳細が利用できない場合や古い場合は、 **[!UICONTROL Fetch]** をクリックします。
