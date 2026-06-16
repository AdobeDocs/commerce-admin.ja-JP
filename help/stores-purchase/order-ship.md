---
title: 配送
description: 処理注文の出荷情報を完了する方法、および出荷情報と追跡情報を表示する方法について説明します。
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 0%

---

# 配送

支払いが完了したが、出荷待ちの注文のステータスは`Processing`です。 出荷レコードには、注文に関連付けられたフルフィルメントプロセスの詳細な履歴が含まれます。 注文が処理されるまで、部分的な出荷を行うことができます。

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;を選択します。

1. _[!UICONTROL Orders]_&#x200B;リストで、発送する注文を検索し、クリックして開きます。

1. 右上隅の「**[!UICONTROL Ship]**」ボタンをクリックします。

1. 請求先住所または配送先住所を更新する場合は、セクションの右上隅にある&#x200B;**[!UICONTROL Edit]** リンクをクリックします。

   必要な変更を行い、**[!UICONTROL Save Order Address]**&#x200B;をクリックします。

1. 配送業者が配送ラベルを生成するには、**[!UICONTROL Create Shipping Label]** チェックボックスを選択し、オプションを設定します。

   - トラッキング番号を追加するには、_[!UICONTROL Shipping Information]_&#x200B;セクションまでスクロールダウンし、**[!UICONTROL Add Tracking Number]**&#x200B;をクリックします。

   - 次のいずれかの操作を行います。

      - **[!UICONTROL Carrier]**&#x200B;を選択し、トラッキング **[!UICONTROL Number]**&#x200B;を入力します。

      - **[!UICONTROL Carrier]**&#x200B;を`Custom Value`に設定し、カスタム キャリアの&#x200B;**[!UICONTROL Title]**&#x200B;を入力し、トラッキング **[!UICONTROL Number]**&#x200B;を入力します。

      - [&#x200B; トラッキング情報を表示](#track-the-shipment)。

1. 部分的な出荷を行うには、「出荷する品目」セクションまでスクロールし、各品目の&#x200B;**[!UICONTROL Qty to Ship]**&#x200B;を入力します。

1. 配送を電子メールでお客様に通知するには、次の操作を行います。

   - **[!UICONTROL Shipment Comments]** ボックスに含めるコメントを入力します。

   - お客様に送信される通知メールにコメントを含めるには、**[!UICONTROL Append Comments]** チェックボックスを選択します。

   - 出荷用メールのコピーを自分に送信するには、「**[!UICONTROL Email Copy of Shipment]**」チェックボックスを選択します。

     請求書の電子メールのステータスは、完了した請求書の請求書番号の横に「送信」または「未送信」と表示されます。

1. 完了したら、**[!UICONTROL Submit Shipment]**&#x200B;をクリックします。

   注文のステータスが`Processing`から`Complete`に変更されます。

>[!NOTE]
>
>注文が「実店舗配送」として行われた場合、配送オプションは利用できません。 「**[!UICONTROL Notify Order is Ready for Pickup]**」をクリックして、お客様にメールをトリガーします。 次に、注文のステータスが`Complete`に変更されます。

## 出荷詳細の表示

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**&#x200B;に移動します。

1. リスト内の出荷を検索し、クリックしてレコードを開きます。

1. 注文にコメントを追加する場合は、_[!UICONTROL Comments History]_&#x200B;セクションまで下にスクロールし、ボックスにコメントを入力します。

   - 電子メールでお客様にコメントを送信するには、**[!UICONTROL Notify Customer by Email]** チェックボックスをオンにします。

   - お客様のアカウントにコメントを投稿するには、**[!UICONTROL Visible on Frontend]** チェックボックスを選択します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## 配送の追跡

**方法1:**&#x200B;注文情報タブから

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;に移動します。

1. グリッドで出荷注文を検索し、**[!UICONTROL View]**&#x200B;をクリックします。

1. _[!UICONTROL Shipping & Handling Information]_&#x200B;セクションまでスクロールして、**[!UICONTROL Track Order]**&#x200B;をクリックします。

   使用可能なトラッキング情報はすべてポップアップウィンドウに表示されます。

1. 準備ができたら、**[!UICONTROL Close Window]**&#x200B;をクリックします。

**方法2:**&#x200B;注文出荷タブから

1. _管理者_ サイドバーで、**[!UICONTROL Sales]** > **[!UICONTROL Shipments]**&#x200B;に移動します。

1. リスト内の出荷を検索し、クリックしてレコードを開きます。

1. **[!UICONTROL Track this Shipment]**&#x200B;をクリックします。

   使用可能なトラッキング情報はすべてポップアップウィンドウに表示されます。

1. 準備ができたら、**[!UICONTROL Close Window]**&#x200B;をクリックします。
