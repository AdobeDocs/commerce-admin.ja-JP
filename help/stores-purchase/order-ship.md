---
title: 注文の発送
description: 処理オーダーの出荷情報を完了する方法と、出荷および追跡情報を表示する方法を説明します。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: abd125cc6e61850db55fb31dbcbd9dc38ac0fca5
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 注文の発送

支払済だが出荷待ちの注文のステータスは `Processing` です。 出荷レコードには、受注に関連付けられた履行プロセスの詳細な履歴が含まれます。 注文が履行されるまで、部分的な出荷を行うことができます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** を選択します。

1. _[!UICONTROL Orders]_&#x200B;の一覧で、出荷する注文を見つけ、クリックして開きます。

1. 右上隅の「**[!UICONTROL Ship]**」ボタンをクリックします。

1. 請求先または配送先住所を更新する場合は、セクションの右上隅にある **[!UICONTROL Edit]** リンクをクリックします。

   必要な変更を行い、「**[!UICONTROL Save Order Address]**」をクリックします。

1. 配送業者に配送ラベルを生成させるには、「**[!UICONTROL Create Shipping Label]**」チェックボックスを選択し、オプションを設定します。

   - 追跡番号を追加するには、[_[!UICONTROL Shipping Information]_] セクションまでスクロールし、[**[!UICONTROL Add Tracking Number]**] をクリックします。

   - 次のいずれかの操作を行います。

      - **[!UICONTROL Carrier]** を選択し、トラッキング **[!UICONTROL Number]** を入力します。

      - **[!UICONTROL Carrier]** を `Custom Value` に設定し、カスタム通信事業者の **[!UICONTROL Title]** を入力して、トラッキング **[!UICONTROL Number]** を入力します。

      - [ トラッキング情報を表示 ](#track-the-shipment).

1. 一部出荷を行うには、「出荷品目」セクションまでスクロールし、各品目の **[!UICONTROL Qty to Ship]** を入力します。

1. メールで顧客に出荷を通知するには、次の手順を実行します。

   - **[!UICONTROL Shipment Comments]** ボックスに、コメントを入力します。

   - 顧客に送信される通知メールにコメントを含めるには、「**[!UICONTROL Append Comments]**」チェックボックスを選択します。

   - 発送用メールのコピーを自分宛てに送信するには、「**[!UICONTROL Email Copy of Shipment]**」チェックボックスを選択します。

     請求書メールのステータスは、完了した請求書の請求書番号の横に、送信済みまたは未送信として表示されます。

1. 完了したら、「**[!UICONTROL Submit Shipment]**」をクリックします。

   注文のステータスが「`Processing`」から「`Complete`」に変わります。

>[!NOTE]
>
>注文が「店舗での配送」の場合、配送オプションは利用できません。 「**[!UICONTROL Notify Order is Ready for Pickup]**」をクリックして、メールを顧客にトリガーします。 すると、注文のステータスが `Complete` に変更されます。

## 出荷の詳細の表示

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Shipments]** に移動します。

1. リストで出荷を検索し、クリックしてレコードを開きます。

1. 注文にコメントを追加する場合は、「_[!UICONTROL Comments History]_」セクションまでスクロールし、ボックスにコメントを入力します。

   - コメントを顧客にメールで送信するには、「**[!UICONTROL Notify Customer by Email]**」チェックボックスをオンにします。

   - 顧客のアカウントにコメントを投稿するには、「**[!UICONTROL Visible on Frontend]**」チェックボックスをオンにします。

1. 「**[!UICONTROL Update]**」をクリックします。

## 出荷の追跡

**方法 1:** 注文情報タブから

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Orders]** に移動します。

1. グリッドで出荷順序を検索し、「**[!UICONTROL View]**」をクリックします。

1. 「_[!UICONTROL Shipping & Handling Information]_」セクションまでスクロールし、「**[!UICONTROL Track Order]**」をクリックします。

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備ができたら、「**[!UICONTROL Close Window]**」をクリックします。

**方法 2:** 「発注納入」タブ

1. _管理者_ サイドバーで、**[!UICONTROL Sales]**/**[!UICONTROL Shipments]** に移動します。

1. リストで出荷を検索し、クリックしてレコードを開きます。

1. 「**[!UICONTROL Track this Shipment]**」をクリックします。

   使用可能なトラッキング情報がポップアップウィンドウに表示されます。

1. 準備ができたら、「**[!UICONTROL Close Window]**」をクリックします。
