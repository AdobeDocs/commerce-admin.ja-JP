---
title: 注文の発送
description: 処理オーダーの出荷情報を完了する方法と、出荷および追跡情報を表示する方法を説明します。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 注文の発送

支払いが完了したが、出荷を待っている注文には、 `Processing` ステータス。 出荷レコードには、受注に関連付けられた履行プロセスの詳細な履歴が含まれます。 注文が履行されるまで、部分的な出荷を行うことができます。

1. 日 _Admin_ サイドバー、選択 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. が含まれる _[!UICONTROL Orders]_リストを表示し、発送する注文を見つけてクリックして開きます。

1. 右上隅のをクリックします **[!UICONTROL Ship]** ボタン。

1. 請求先または配送先住所を更新する場合は、 **[!UICONTROL Edit]** セクションの右上隅にあるリンク。

   必要な変更を行い、 **[!UICONTROL Save Order Address]**.

1. 配送業者に配送ラベルを生成させるには、 **[!UICONTROL Create Shipping Label]** チェックボックスをオンにして、次のオプションを設定します。

   - トラッキング番号を追加するには、下にスクロールして _[!UICONTROL Shipping Information]_セクションで、をクリックします。**[!UICONTROL Add Tracking Number]**.

   - 次のいずれかの操作を行います。

      - 「」を選択します **[!UICONTROL Carrier]** およびトラッキングを入力 **[!UICONTROL Number]**.

      - を設定 **[!UICONTROL Carrier]** 対象： `Custom Value`、a と入力します **[!UICONTROL Title]** カスタムキャリアの場合、およびトラッキングを入力 **[!UICONTROL Number]**.

      - [トラッキング情報の表示](#track-the-shipment).

1. 部分出荷を行うには、「出荷品目」セクションまでスクロールし、 **[!UICONTROL Qty to Ship]** 項目ごとに調整します。

1. メールで顧客に出荷を通知するには、次の手順を実行します。

   - に含めるコメントを入力してください **[!UICONTROL Shipment Comments]** ボックス。

   - 顧客に送信される通知メールにコメントを含めるには、 **[!UICONTROL Append Comments]** チェックボックス。

   - 発送用メールのコピーを自分宛てに送信するには、 **[!UICONTROL Email Copy of Shipment]** チェックボックス。

     請求書メールのステータスは、完了した請求書の請求書番号の横に、送信済みまたは未送信として表示されます。

1. 完了したら、 **[!UICONTROL Submit Shipment]**.

   注文のステータスが次のように変更されます `Processing` 対象： `Complete`.

>[!NOTE]
>
>注文が「店舗での配送」の場合、配送オプションは利用できません。 クリック **[!UICONTROL Notify Order is Ready for Pickup]** ：顧客にメールをトリガーします。 その後、注文のステータスが「」に変更されます `Complete`.

## 出荷の詳細の表示

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. リストで出荷を検索し、クリックしてレコードを開きます。

1. 注文にコメントを追加する場合は、下にスクロールして _[!UICONTROL Comments History]_「」セクションをクリックし、ボックスにコメントを入力します。

   - コメントを顧客にメールで送信するには、 **[!UICONTROL Notify Customer by Email]** チェックボックス。

   - 顧客のアカウントにコメントを投稿するには、 **[!UICONTROL Visible on Frontend]** チェックボックス。

1. クリック **[!UICONTROL Submit Comment]**.

## 出荷の追跡

**メソッド 1:** 「注文情報」タブから

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. グリッドで出荷順序を検索し、 **[!UICONTROL View]**.

1. にスクロール ダウンします。 _[!UICONTROL Shipping & Handling Information]_セクションでクリック&#x200B;**[!UICONTROL Track Order]**.

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備ができたら、 **[!UICONTROL Close Window]**.

**メソッド 2:** 「発注納入」タブから

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. リストで出荷を検索し、クリックしてレコードを開きます。

1. クリック **[!UICONTROL Track this Shipment]**.

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備ができたら、 **[!UICONTROL Close Window]**.
