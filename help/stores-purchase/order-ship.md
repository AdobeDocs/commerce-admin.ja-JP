---
title: 注文の発送
description: 処理注文の配送先情報を完了し、出荷と追跡情報を表示する方法を説明します。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 注文の発送

支払済の注文が、出荷待ちの注文が、 `Processing` ステータス。 出荷レコードには、注文に関連付けられた履行プロセスの詳細な履歴が含まれます。 一部出荷は、注文が満たされるまで行うことができます。

1. 次の日： _管理者_ サイドバー、選択 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Adobe Analytics の _[!UICONTROL Orders]_「 」リストで、発送する注文を探し、「 」をクリックして開きます。

1. 右上隅で、 **[!UICONTROL Ship]** 」ボタンをクリックします。

1. 請求または配送先住所を更新する場合は、 **[!UICONTROL Edit]** リンクを使用して貼り付けることができます。

   必要な変更を行い、「 **[!UICONTROL Save Order Address]**.

1. 運送業者に送料ラベルを生成させるには、 **[!UICONTROL Create Shipping Label]** チェックボックスをオンにして、次のオプションを設定します。

   - トラッキング番号を追加するには、 _[!UICONTROL Shipping Information]_「 」セクションで、「**[!UICONTROL Add Tracking Number]**.

   - 次のいずれかの操作を行います。

      - を選択します。 **[!UICONTROL Carrier]** をクリックし、トラッキングを入力します。 **[!UICONTROL Number]**.

      - 設定 **[!UICONTROL Carrier]** から `Custom Value`、 **[!UICONTROL Title]** カスタム通信事業者に対して、トラッキングを入力します。 **[!UICONTROL Number]**.

      - [トラッキング情報を表示](#track-the-shipment).

1. 一部出荷を行うには、「出荷する品目」セクションまで下にスクロールし、 **[!UICONTROL Qty to Ship]** 項目ごとに

1. 顧客に出荷を電子メールで通知するには、次の手順を実行します。

   - に含めるコメントを入力します。 **[!UICONTROL Shipment Comments]** ボックス。

   - 顧客に送信する通知 E メールにコメントを含めるには、 **[!UICONTROL Append Comments]** チェックボックス。

   - 自分自身に出荷メールのコピーを送信するには、 **[!UICONTROL Email Copy of Shipment]** チェックボックス。

     請求書 E メールのステータスは、完了した請求書の請求書番号の横に、送信済みまたは未送信として表示されます。

1. 完了したら、「 **[!UICONTROL Submit Shipment]**.

   注文のステータスが次の値から変わります： `Processing` から `Complete`.

>[!NOTE]
>
>注文が「店内配送」としておこなわれている場合、配送オプションは使用できません。 クリック **[!UICONTROL Notify Order is Ready for Pickup]** を使用して、顧客に E メールをトリガーします。 オーダーのステータスが次のように変更されます。 `Complete`.

## 出荷の詳細を表示

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. リスト内の出荷を検索し、クリックしてレコードを開きます。

1. 順序にコメントを追加する場合は、 _[!UICONTROL Comments History]_」セクションでコメントを入力し、ボックスにコメントを入力します。

   - コメントを電子メールで顧客に送信するには、 **[!UICONTROL Notify Customer by Email]** チェックボックス。

   - 顧客のアカウントにコメントを投稿するには、 **[!UICONTROL Visible on Frontend]** チェックボックス。

1. クリック **[!UICONTROL Submit Comment]**.

## 出荷を追跡

**メソッド 1:** 「発注情報」タブ

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッド内の出荷オーダーを検索し、をクリックします。 **[!UICONTROL View]**.

1. 下にスクロールして、 _[!UICONTROL Shipping & Handling Information]_「 」セクションで、「 」をクリックします。**[!UICONTROL Track Order]**.

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備が整ったら、「 **[!UICONTROL Close Window]**.

**方法 2:** 発注出荷タブ

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. リスト内の出荷を検索し、クリックしてレコードを開きます。

1. クリック **[!UICONTROL Track this Shipment]**.

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備が整ったら、「 **[!UICONTROL Close Window]**.
