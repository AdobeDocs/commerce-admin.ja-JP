---
title: トランザクション
description: トランザクションページと、それを使用して店舗と支払いシステムの間のアクティビティを追跡する方法について説明します。
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# トランザクション

The _トランザクション_ ページには、お客様の店舗と支払いシステムの間で行われたすべての支払いアクティビティが一覧表示され、より詳細な情報へのアクセスが提供されます。

## トランザクションの表示

次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![トランザクショングリッド](./assets/transactions.png){width="600" zoomable="yes"}

| 列 | 説明 |
|--- |--- |
| [!UICONTROL ID] | 各トランザクションに割り当てられる一意の数値識別子。 |
| [!UICONTROL Order ID] | 顧客が注文した際に割り当てられる一意の ID。 |
| [!UICONTROL Transaction ID] | 顧客が注文した後にトランザクションが発生した場合に割り当てられる一意の数値識別子。 |
| [!UICONTROL Parent Transaction ID] | 親トランザクションの ID 番号。 |
| [!UICONTROL Payment Method] | トランザクションに関連付けられた支払い方法。 |
| [!UICONTROL Transaction Type] | 取引のタイプ（注文、承認、取得、無効、返金）。 |
| [!UICONTROL Closed] | トランザクションがクローズされているかどうか。 |
| [!UICONTROL Created] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

## トランザクションの詳細を表示

表示するエントリをクリックします。

取引の詳細ページで、取引の詳細と子取引のグリッドを確認できます。

### トランザクションデータ

このセクションには、トランザクションに関する情報が含まれ、 **注文 ID** 列。

| 列 | 説明 |
|--- |--- |
| [!UICONTROL Transaction ID] | トランザクション ID 番号。 |
| [!UICONTROL Parent Transaction ID] | 対応する親トランザクションの ID 番号（該当する場合）。 |
| [!UICONTROL Transaction Type] | 取引のタイプ（注文、承認、取得、無効、返金）。 |
| [!UICONTROL Is Closed] | トランザクションがクローズされているかどうか。 |
| [!UICONTROL Created At] | トランザクションが作成された日時。 |

{style="table-layout:auto"}

### 子トランザクション

の請求書を作成した後、子トランザクションがグリッドに表示されます。 [注文件数](orders.md). この形式では、トランザクション階層に従ってトランザクション履歴を追跡できます。

### [!UICONTROL Transaction Details]

このセクションには、特定のトランザクションに関する追加情報が含まれます。 情報は、キーと値の形式で表示されます。 使用可能なキーは次のとおりです。

- authAmount
- authCode
- aVSResponse
- billTo
- cardCodeResponse
- 顧客
- customerIP
- lineItems
- marketType
- 注文
- 支払い
- 製品
- recurringBilling
- responseCode
- responseReasonCode
- responseReasonDescription
- settleAmount
- ソリューション
- submitTimeLocal
- submitTimeUTC
- taxExempt
- transactionStatus

>[!NOTE]
>
>トランザクションの詳細が使用できない場合や古い場合は、 **[!UICONTROL Fetch]** をクリックして更新します。
