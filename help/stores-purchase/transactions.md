---
title: 取引
description: トランザクションページについて説明し、ストアと支払いシステム間のアクティビティを追跡するために使用する方法について説明します。
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 取引

_トランザクション_ ページには、ストアと支払いシステムの間で行われたすべての支払いアクティビティが一覧表示され、より詳細な情報にアクセスできます。

## トランザクションの表示

_管理者_ サイドバーで、**[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**&#x200B;に移動します。

![&#x200B; トランザクショングリッド &#x200B;](./assets/transactions.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各トランザクションに割り当てられる一意の数値識別子。 |
| [!UICONTROL Order ID] | 顧客が注文したときに割り当てられる一意のID。 |
| [!UICONTROL Transaction ID] | 顧客が注文した後にトランザクションが発生したときに割り当てられる一意の数値識別子。 |
| [!UICONTROL Parent Transaction ID] | 親トランザクションのID番号。 |
| [!UICONTROL Payment Method] | トランザクションに関連付けられている支払い方法。 |
| [!UICONTROL Transaction Type] | トランザクションのタイプ。注文、認証、取得、無効化、返金のいずれかを選択できます。 |
| [!UICONTROL Closed] | トランザクションがクローズされたかどうかを示します。 |
| [!UICONTROL Created] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

## トランザクションの詳細を表示

表示するエントリをクリックします。

トランザクションの詳細ページで、トランザクションの詳細と子トランザクションのグリッドを表示できます。

### 取引データ

このセクションには、トランザクションに関する情報が含まれており、**注文ID**&#x200B;列の注文ページへのリンクを提供します。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Transaction ID] | トランザクション ID番号。 |
| [!UICONTROL Parent Transaction ID] | 該当する場合、親トランザクションの対応するID番号。 |
| [!UICONTROL Transaction Type] | トランザクションのタイプ。注文、認証、取得、無効化、返金のいずれかを選択できます。 |
| [!UICONTROL Is Closed] | トランザクションがクローズされたかどうかを示します。 |
| [!UICONTROL Created At] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

### 子トランザクション

[注文](orders.md)の請求書を作成した後、子トランザクションがグリッドに表示されます。 この形式を使用すると、トランザクション階層に従ってトランザクション履歴を追跡できます。

### [!UICONTROL Transaction Details]

このセクションには、特定のトランザクションに関する追加情報が含まれます。 情報は、キーと値の形式で表示されます。 使用可能なキーは次のとおりです。

- authAmount
- authCode
- VSResponse
- billTo
- cardCodeResponse
- お客様
- customerIP
- lineItems
- marketType
- 注文
- 支払い
- product
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleAmount
- solution
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>トランザクションの詳細が利用できないか、古い場合は、ボタンバーの&#x200B;**[!UICONTROL Fetch]**&#x200B;をクリックして更新します。
