---
title: 注文をアーカイブ
description: パフォーマンスを向上させ、組織のコマースを合理化するために注文アーカイブを設定する方法を説明します。
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 注文をアーカイブ

{{ee-feature}}

注文をアーカイブすると、パフォーマンスが定期的に向上し、ワークスペースに不要な情報がなくなるので、現在のビジネスに専念できます。 請求書、出荷、クレジット・メモは、自動または手動でアーカイブし、いつでも表示できます。

>[!NOTE]
>
>The _[!UICONTROL Archive]_オプションが [[!UICONTROL Sales] メニュー](sales-menu.md) アーカイブの場合のみ [有効](../configuration-reference/sales/sales.md).

## オーダーアーカイブの設定

ストアは、一定日数の経過後に注文、請求書、出荷、クレジットメモをアーカイブするように設定できます。 注文と関連ドキュメントをアーカイブに移動したり、前の状態に復元したりできます。 アーカイブされた注文は削除されず、管理者から引き続き使用できます。 アーカイブしたデータは CSV ファイルに書き出して、スプレッドシートで開くことができます。 有効にすると、 _アーカイブ_ アクションがワークスペースの上部に表示されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** 「 」セクションで「 」を選択します。 **[!UICONTROL Sales]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** 」セクションに入力します。

   ![オーダー、請求書、出荷、クレジット・メモ・アーカイブの構成設定](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. 設定 **[!UICONTROL Enable Archiving]** から `Yes`.

   >[!NOTE]
   >
   >後でアーカイブをオフにする場合は、アーカイブされた注文はすべて前の状態に復元されます。

1. 設定 **[!UICONTROL Archive Orders Purchased]** を、完了したオーダーがアーカイブされるまでの待機日数に設定します。

   デフォルトでは、注文は購入後 30 日間アーカイブされます。

1. Adobe Analytics の **[!UICONTROL Order Statuses to be Archived]** 「 」リストで、アーカイブする注文の識別に使用する各注文ステータスを選択します。

   複数の項目を選択するには、Ctrl キー (Windows) または Command キー (Mac) を押しながら各項目をクリックします。

1. クリック **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、無効なキャッシュを更新します。

## アーカイブ済みドキュメントの表示

1. Adobe Analytics の _[!UICONTROL Sales]_下のメニュー_[!UICONTROL Archive]_、次のいずれかを選択します。

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 詳細を表示するには、リスト内のアーカイブされたドキュメントをクリックします。

## アーカイブされたドキュメントにアクションを適用する

アクションの対象となる各ドキュメントを選択し、次のいずれかを選択します。 **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## ドキュメントを手動でアーカイブ

1. アーカイブするドキュメントの種類を次の中から選択します。

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. アーカイブする各項目のチェックボックスをオンにします。

1. 右上隅で、 **[!UICONTROL Actions]** から `Move to Archive`.

1. クリック **[!UICONTROL Submit]** 選択したドキュメントをアーカイブします。

## アーカイブしたドキュメントを復元

1. 復元するドキュメントの種類を選択します。

1. 次のいずれかのオプションを使用してドキュメントを選択します。

   - 表示されるすべてのドキュメントを選択するには、左上隅の **[!UICONTROL Select Visible]**.

   - 復元する各ドキュメントのチェックボックスを手動で選択します。

1. 右上で、 **[!UICONTROL Action]** から `Move to Orders Management`.

1. クリック **[!UICONTROL Submit]** をクリックして、ドキュメントを復元します。

## アーカイブしたドキュメントを書き出し

1. 書き出すドキュメントの種類を選択します。

1. 右上のメニューで、 **[!UICONTROL Export to:]** を次のいずれかの値に変更します。

   - `CSV`
   - `Excel`

1. クリック **[!UICONTROL Export]**.

ストアは、一定日数の経過後に注文、請求書、出荷、クレジットメモをアーカイブするように設定できます。 注文と関連ドキュメントをアーカイブに移動したり、前の状態に復元したりできます。 アーカイブされた注文は削除されず、管理者から引き続き使用できます。 アーカイブしたデータは CSV ファイルに書き出して、スプレッドシートで開くことができます。 有効にすると、 _[!UICONTROL Archive]_コマンドがワークスペースの上部に表示されます。

## オーダーを手動でアーカイブ

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. グリッド上の順序を選択するには、最初の列のチェックボックスをオンにします。

1. を設定します。 **[!UICONTROL Actions]** ～を制御する `Move to Archive` と共に、注文がアーカイブされたメッセージを探します。

   ![選択したオーダーのアーカイブへの移動 ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>アーカイブ可能なオーダーステータスのリストを指定するには、 [オーダーアーカイブの設定](#configure-the-order-archive).

## アーカイブした注文の表示

1. 次のいずれかの方法でアーカイブビューを開きます。

   - の上のボタンバーで、 _[!UICONTROL Orders]_グリッド、クリック&#x200B;**[!UICONTROL Go to Archive]**.

   - 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >注文ページと同様に、アーカイブされた注文ページのタイトルは次のようになります _[!UICONTROL Orders]_. 目に見える違いは、ボタンバーの「_[!UICONTROL Return to Orders Management]_. また、ページの URL は、自分がアーカイブの順序にあることを示します。

1. Adobe Analytics の _アクション_ 列、クリック **[!UICONTROL View]**.

   ![アーカイブした注文の表示](./assets/order-archived-view.png){width="600" zoomable="yes"}

## アーカイブされたオーダーの復元

>[!NOTE]
>
>アーカイブされた注文から復元された注文は、 [!UICONTROL Archive Orders Purchased] 設定 ( [オーダーアーカイブの設定](#configure-the-order-archive)) をクリックします。 日数は [!UICONTROL Updated At] オーダーの日付。オーダーがアーカイブから移動されたときに変更されます。

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. ボタンバーで、 **[!UICONTROL Go to Archive]**.

1. 復元するレコードを見つけ、チェックボックスをクリックして選択します。

   ![復元する順序を選択](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. を設定します。 **[!UICONTROL Actions]** ～に対する価値を制御する `Move to Order Management`.

アーカイブからアーカイブ済みの注文が削除されたことを示すメッセージを探します。

## アーカイブ済みの注文をエクスポート

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. アクションメニューで、 **[!UICONTROL Export]** をクリックし、目的の形式を選択します。
