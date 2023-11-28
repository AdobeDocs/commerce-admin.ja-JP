---
title: ストアフロントの Order Management
description: Commerce ストアフロントで、顧客が注文履歴を表示および管理する方法を説明します。
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# ストアフロントの Order Management

顧客は、自分のアカウントからすべての注文にアクセスできます。 注文は、新しい注文として表示、フィルター、追跡、再送信できます。 注文のステータスに応じて、顧客は注文、請求書、出荷、返金のレコードを印刷できます。

## 注文をフィルター

{{b2b-feature}}

初期 _[!UICONTROL My Orders]_結果には、コマースインスタンス内のすべての web サイトからの一致する下位ユーザーからの注文も含まれます。 会社のアカウントに関連付けられている顧客は、注文リストをフィルタリングして、結果内のレコードをすばやく見つけることができます。 フィルターオプションを表示するには、顧客が&#x200B;**[!UICONTROL Filter]**、およびクリック&#x200B;**[!UICONTROL Close]**をクリックして、フィルターを非表示にします。

![注文](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| フィルター | 説明 |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | SKU または製品名を入力します。 |
| [!UICONTROL Order Number] | 注文の全数または一部を指定できます。 |
| [!UICONTROL Order Status] | ドロップダウンから値を選択し、ステータスでフィルタリングします。 |
| [!UICONTROL Invoice Number] | 請求書番号の全部または一部を入力します。 |
| [!UICONTROL Order Date] | 注文日でフィルタリングする 1 つまたは両方の日付フィールドを設定します。 |
| [!UICONTROL Created by] | 注文作成者による企業注文をフィルタリングします。 |
| [!UICONTROL Order Total] | 並べ替えの合計でフィルタリングする最小値、最大値、またはその両方を設定します。 |

## 注文を表示

顧客がリスト内の注文を検索し、クリックします **[!UICONTROL View Order]**. オープンオーダーから、次のいずれかの操作を実行できます。

![注文を表示](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### 最近注文した製品を表示

The **[!UICONTROL Recent Orders]** ブロックがサイドバーおよび **[!UICONTROL My Account]** 注文後にログインした顧客のページ。 最後の購入から 5 つの製品が表示されます。

顧客は、製品を選択し、 **[!UICONTROL Add to Cart]**. また、最後の注文を表示するには、 **[!UICONTROL View all]**（にリダイレクト） _[!UICONTROL My Account]_ページと&#x200B;**[!UICONTROL Recent Orders]**ブロック。

### 印刷順序

1. 顧客がクリックする **[!UICONTROL Print Order]**.

1. [ 印刷 ] ダイアログの指示に従って、印刷を完了します。

### 請求書の印刷

1. 次の日： **[!UICONTROL Invoices]** 「 」タブで、顧客が次のいずれかをクリックします。

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![請求書](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して印刷を完了します。

### 出荷を印刷

1. 次の日： **[!UICONTROL Order Shipments]** 「 」タブで、顧客が次のいずれかをクリックします。

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![すべての出荷を印刷](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して印刷を完了します。

### 出荷を追跡する

1. 次の日： **[!UICONTROL Order Shipments]** タブ、クリック **[!UICONTROL Track this Shipment]**.

   使用可能なトラッキング情報は、ポップアップウィンドウに表示されます。

1. 準備が整ったら、顧客はクリックします **[!UICONTROL Close Window]**.

### 払い戻しの印刷

1. 次の日： **払い戻し** 「 」タブで、顧客が次のいずれかをクリックします。

   - **全払い戻しの印刷**

   - **払い戻しの印刷**

   ![払い戻し](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して印刷を完了します。

リオーダーは、 [_並べ替えを許可_](reorders-allow.md) 設定オプションが有効になっています。

顧客は、特定の注文に対して、次の 2 つのページから並べ替え機能を開始できます。

- マイ注文ページ
- 注文ビューページ

## 再注文

The _[!UICONTROL Reorder]_リンクがリストに表示され、「_[!UICONTROL View]_ リンク。

![注文ページのリンクを並べ替え](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**例 1.** 注文のすべての製品を並べ替えに使用できます

顧客が買い物かごにリダイレクトされ、すべての製品が買い物かごに追加されます。

**例 2.** 注文の一部またはすべての製品は、並べ替えに使用できません

>[!NOTE]
>
>並べ替えは可能です `Not Visible Individually` 製品。

The _[!UICONTROL Reorder]_リンクが_[!UICONTROL My Orders]_ および _[!UICONTROL View Order]_ページ。

![マイ注文ページ](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>買い物かごが空でなく、顧客がクリックした場合 **[!UICONTROL Reorder]** ( [!UICONTROL My Orders] または [!UICONTROL Order View] 」ページを参照 )、既存の製品は、追加された製品の並べ替えと共にカート内に残ります。
