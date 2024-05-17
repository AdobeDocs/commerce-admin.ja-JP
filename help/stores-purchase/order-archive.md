---
title: 注文のアーカイブ
description: 注文アーカイブを設定して、パフォーマンスを向上させ、Commerceを効率化する方法を説明します。
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 注文のアーカイブ

{{ee-feature}}

注文を定期的にアーカイブすると、パフォーマンスが向上し、ワークスペースに不要な情報が含まれなくなるので、現在のビジネスに集中できます。 請求書、出荷およびクレジット・メモは、自動または手動でアーカイブでき、いつでも表示できます。

>[!NOTE]
>
>この _[!UICONTROL Archive]_オプションがに表示される [[!UICONTROL Sales] メニュー](sales-menu.md) アーカイブがの場合のみ [enabled](../configuration-reference/sales/sales.md).

## 注文アーカイブの設定

ストアは、設定した日数が経過した後に注文、請求書、出荷、およびクレジット メモをアーカイブするように構成できます。 オーダーおよび関連ドキュメントをアーカイブに移動したり、以前の状態に復元したりできます。 アーカイブ済み注文は削除されず、管理者から引き続き使用できます。 アーカイブしたデータを CSV ファイルに書き出して、スプレッドシートで開くことができます。 有効にすると、 _アーカイブ_ アクションがワークスペースの上部に表示されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** セクションで選択 **[!UICONTROL Sales]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** セクション。

   ![受注、請求書、出荷、クレジット・メモ・アーカイブの構成設定](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. を設定 **[!UICONTROL Enable Archiving]** 対象： `Yes`.

   >[!NOTE]
   >
   >後でアーカイブをオフにすることにした場合、アーカイブされたすべての注文は以前の状態に復元されます。

1. を設定 **[!UICONTROL Archive Orders Purchased]** 完了した注文がアーカイブされるまでの待機日数に設定します。

   デフォルトでは、注文は購入から 30 日後にアーカイブされます。

1. が含まれる **[!UICONTROL Order Statuses to be Archived]** リストで、アーカイブする注文を識別するために使用する各注文ステータスを選択します。

   複数の項目を選択するには、Ctrl キー（Windows）または Command キー（Mac）を押しながら各項目をクリックします。

1. クリック **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、無効なキャッシュを更新します。

## アーカイブしたドキュメントの表示

1. が含まれる _[!UICONTROL Sales]_の下のメニュー_[!UICONTROL Archive]_&#x200B;次のいずれかを選択します。

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 詳細を表示するには、リスト内のアーカイブされたドキュメントをクリックします。

## アーカイブしたドキュメントへのアクションの適用

アクションのターゲットにする各ドキュメントを選択し、次のいずれかを選択します **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## ドキュメントの手動アーカイブ

1. 以下からアーカイブするドキュメントのタイプを選択します。

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. アーカイブする各項目のチェックボックスを選択します。

1. 右上隅で、を設定します **[!UICONTROL Actions]** 対象： `Move to Archive`.

1. クリック **[!UICONTROL Submit]** 選択したドキュメントをアーカイブします。

## アーカイブされたドキュメントの復元

1. 復元するドキュメントの種類を選択します。

1. 次のいずれかのオプションを使用してドキュメントを選択します。

   - 表示されているすべてのドキュメントを選択するには、左上隅のをクリックします **[!UICONTROL Select Visible]**.

   - 復元する各ドキュメントのチェックボックスを手動で選択します。

1. 右上で、を設定 **[!UICONTROL Action]** 対象： `Move to Orders Management`.

1. クリック **[!UICONTROL Submit]** をクリックしてドキュメントを復元します。

## アーカイブしたドキュメントの書き出し

1. 書き出すドキュメントのタイプを選択します。

1. 右上のメニューで、を設定 **[!UICONTROL Export to:]** を次のいずれかの値に変更します。

   - `CSV`
   - `Excel`

1. クリック **[!UICONTROL Export]**.

ストアは、設定した日数が経過した後に注文、請求書、出荷、およびクレジット メモをアーカイブするように構成できます。 オーダーおよび関連ドキュメントをアーカイブに移動したり、以前の状態に復元したりできます。 アーカイブ済み注文は削除されず、管理者から引き続き使用できます。 アーカイブしたデータを CSV ファイルに書き出して、スプレッドシートで開くことができます。 有効にすると、 _[!UICONTROL Archive]_コマンドがワークスペースの上部に表示されます。

## 注文を手動でアーカイブ

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッド上の順序を選択するには、最初の列のチェックボックスを選択します。

1. を **[!UICONTROL Actions]** コントロール先 `Move to Archive` 注文がアーカイブされたというメッセージを探します。

   ![選択したオーダーのアーカイブへの移動 ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>アーカイブ可能な注文ステータスのリストを指定するには、以下を参照してください [注文アーカイブの設定](#configure-the-order-archive).

## アーカイブした注文の表示

1. 次のいずれかの方法を使用して、アーカイブ・ビューを開きます。

   - 上部のボタンバーで _[!UICONTROL Orders]_グリッド、クリック&#x200B;**[!UICONTROL Go to Archive]**.

   - 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >注文ページと同様に、アーカイブされた注文ページのタイトルはです _[!UICONTROL Orders]_. 顕著な違いは、ボタンバーのオプションが次の点です。_[!UICONTROL Return to Orders Management]_. ページの URL は、オーダーアーカイブにいることも示します。

1. が含まれる _アクション_ 列、クリック **[!UICONTROL View]**.

   ![アーカイブした注文の表示](./assets/order-archived-view.png){width="600" zoomable="yes"}

## アーカイブした注文の復元

>[!NOTE]
>
>アーカイブされた注文から復元された注文は、で設定された日数に従って再度アーカイブされます [!UICONTROL Archive Orders Purchased] 設定（を参照 [注文アーカイブの設定](#configure-the-order-archive)）に設定します。 日数は、に対して計算されます [!UICONTROL Updated At] オーダーの日付。オーダーがアーカイブから移動されると変更されます。

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. ボタン バーで、をクリックします **[!UICONTROL Go to Archive]**.

1. 復元するレコードを見つけ、チェックボックスをクリックして選択します。

   ![復元する注文を選択](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. を **[!UICONTROL Actions]** 制御値： `Move to Order Management`.

アーカイブした注文がアーカイブから削除されたというメッセージを探します。

## アーカイブした注文の書き出し

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. アクションメニューで、 **[!UICONTROL Export]** そして、目的の形式を選択します。
