---
title: ストアフロントの注文管理
description: Commerce ストアフロントで注文履歴を表示および管理する方法について説明します。
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/FGexEy3ZXcnDUoHOiGc3B24ri2AuP4vX-vX7q3tcbRA
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 753
ht-degree: 0%

---

# ストアフロントの注文管理

顧客は、自分のアカウントからすべての注文にアクセスできます。 注文は、新しい注文として表示、フィルタリング、追跡、再送信できます。 注文のステータスに応じて、顧客は注文、請求書、出荷、返品記録を印刷できます。

## フィルターの順序

{{b2b-feature}}

最初の&#x200B;_[!UICONTROL My Orders]_の結果には、コマースインスタンス内のすべてのweb サイトからの下位ユーザーからの一致する注文も含まれています。 会社アカウントに関連付けられている顧客は、注文リストをフィルタリングして、結果内のレコードをすばやく見つけることができます。 フィルターオプションを表示するには、顧客が&#x200B;**[!UICONTROL Filter]**をクリックし、**[!UICONTROL Close]**をクリックしてフィルターを非表示にします。

![自分の注文](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| フィルター | 説明 |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | SKUまたは製品名を入力します。 |
| [!UICONTROL Order Number] | フルオーダー番号または部分的オーダー番号を指定できます。 |
| [!UICONTROL Order Status] | ドロップダウンから値を選択し、ステータスでフィルタリングします。 |
| [!UICONTROL Invoice Number] | 請求書番号の全部または一部を入力します。 |
| [!UICONTROL Order Date] | 1つまたは両方の日付フィールドを設定して、注文日でフィルタリングします。 |
| [!UICONTROL Created by] | 注文の作成者による会社の注文をフィルタリングします。 |
| [!UICONTROL Order Total] | 注文の合計でフィルタリングする最小値、最大値、または両方の値を設定します。 |

## 注文の表示

顧客はリスト内の注文を見つけて、**[!UICONTROL View Order]**&#x200B;をクリックします。 オープンオーダーから、次のいずれかを行うことができます。

![注文を表示](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### 最近注文した商品の表示

**[!UICONTROL Recent Orders]** ブロックは、注文後にログインしたお客様のサイドバーと&#x200B;**[!UICONTROL My Account]** ページに表示されます。 最後に購入した5つの商品が表示されます。

お客様は、商品を選択し、**[!UICONTROL Add to Cart]**&#x200B;をクリックして、商品をカートに読み込むことができます。 また、**[!UICONTROL View all]**&#x200B;をクリックして最後の注文を表示し、_[!UICONTROL My Account]_ページと&#x200B;**[!UICONTROL Recent Orders]**ブロックにリダイレクトすることもできます。

### 印刷注文

1. お客様は&#x200B;**[!UICONTROL Print Order]**&#x200B;をクリックします。

1. 印刷ダイアログの指示に従って、印刷を完了します。

### 請求書の印刷

1. 「**[!UICONTROL Invoices]**」タブで、お客様は次のいずれかをクリックします。

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![請求書](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して、印刷を完了します。

### 印刷物の発送

1. 「**[!UICONTROL Order Shipments]**」タブで、お客様は次のいずれかをクリックします。

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![すべての出荷を印刷](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して、印刷を完了します。

### 配送の追跡

1. 「**[!UICONTROL Order Shipments]**」タブで、「**[!UICONTROL Track this Shipment]**」をクリックします。

   使用可能なトラッキング情報は、ポップアップウィンドウに表示されます。

1. 準備ができたら、お客様は&#x200B;**[!UICONTROL Close Window]**&#x200B;をクリックします。

### 返金の印刷

1. 「**返金**」タブで、お客様は次のいずれかをクリックします。

   - **すべての返金を印刷**

   - **返金を印刷**

   ![返金](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. 印刷ダイアログを使用して、印刷を完了します。

再注文は、[_再注文を許可_](reorders-allow.md)&#x200B;設定オプションが有効になっている場合に、お客様が利用できます。

お客様は、次の2つのページから特定の注文の再発注機能を開始できます。

- マイオーダーのページ
- 注文表示ページ

## 再発注

_[!UICONTROL Reorder]_リンクは、_[!UICONTROL View]_ リンクに近い注文を含むリストに表示されます。

![ マイオーダーのページ ](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}の再注文リンク

**ケース 1.** 注文のすべての商品は再発注できます

顧客はショッピングカートにリダイレクトされ、すべての商品がカートに追加されます。

**ケース 2.** 注文の一部またはすべての製品は再発注できません

>[!NOTE]
>
>`Not Visible Individually`個の商品を再注文できます。

_[!UICONTROL Reorder]_リンクが_[!UICONTROL My Orders]_&#x200B;および&#x200B;_[!UICONTROL View Order]_ページに表示されません。

![自分の注文ページ ](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>買い物かごが空ではなく、顧客が「**[!UICONTROL Reorder]**」（[!UICONTROL My Orders]または[!UICONTROL Order View] ページ）をクリックした場合、既存の商品は追加された再発注商品とともに買い物かごに残ります。

## 注文をキャンセル

「[_キャンセルを許可_](cancel-allow.md)」設定オプションが有効になっている場合、キャンセルは顧客が利用できます。

お客様は、次の3つのページから特定の注文のキャンセル機能を開始できます。

- マイオーダーのページ
- 注文表示ページ
- マイアカウントページ

_[!UICONTROL Cancel Order]_リンクが_[!UICONTROL Reorder]_ リンクの近くに表示されます。 注文をキャンセルできない場合、リンクは表示されません。

![ マイオーダーのページのキャンセルリンク ](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

キャンセルを実行するには、お客様は次の操作を行います。

1. クリック数：**[!UICONTROL Cancel Order]**

1. 解約理由を指定します

   ![ キャンセル注文理由](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   解約理由は、[_解約を許可_](cancel-allow.md) ページでカスタマイズできます。

1. クリック数：**[!UICONTROL Confirm]**

   ![ マイオーダーのページでキャンセル ](./assets/cancel-order.png){width="700" zoomable="yes"}

   解約後、_[!UICONTROL Pending]_件の状態だった注文は_[!UICONTROL Canceled]_&#x200B;件の状態に変更され、_[!UICONTROL Processing]_件の状態だった注文は_[!UICONTROL Closed]_&#x200B;件の状態に変更され、返金が処理されます。

   解約が完了すると、お客様にメールが送信されます。

   ![注文電子メールをキャンセル ](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   キャンセル情報は、お客様の注文履歴に追加されます。 注文のメモと「コメント履歴」タブに表示されます。

   ![注文メモのキャンセル ](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![ コメント履歴をキャンセル ](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   何らかの理由で注文がキャンセルできないステータスに変更され、顧客がページを更新しなかった場合、注文をキャンセルするためのリンクが引き続き表示されます。 ただし、キャンセルしようとすると、エラーメッセージが表示されます。

   ![注文キャンセルのエラーメッセージ ](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   ページを更新すると、注文が既に完了したことが表示されます。そのため、キャンセルは機能しませんでした。

   ![更新後に注文をキャンセル ](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
