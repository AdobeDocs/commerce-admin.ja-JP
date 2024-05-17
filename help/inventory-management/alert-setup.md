---
title: 製品アラート
description: 製品アラートと、そのアラートを使用して製品の在庫状態や価格の変更を顧客に通知する方法について説明します。
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# 製品アラート

顧客は、価格変更アラートと在庫内アラートの 2 種類のアラートをメールで購読できます。 アラートのタイプごとに、顧客が購読できるかどうかを判断し、使用するメールテンプレートを選択し、メールの送信者を識別できます。

![製品アラートへの新規登録](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 価格変更アラート

価格変更アラートが有効化されている場合、 _価格が下がったら知らせてくれ_ リンクは各製品ページに表示されます。 お客様は、リンクをクリックして、製品に関連するアラートを登録できます。 ゲストは、ストアでアカウントを開くように求められます。 価格が変更されたり、商品が特別になったりするたびに、アラートを購読したすべてのユーザーにメールアラートが届きます。

## 在庫中アラート

在庫内アラートは、というリンクを作成します _この製品の在庫切れを通知_ 在庫切れの製品ごとに。 お客様は、リンクをクリックしてアラートを購読できます。 商品が再入荷すると、顧客は商品が使用可能であることを知らせるメール通知を受け取ります。 アラートが発生した製品には _製品アラート_ アラートを購読している顧客をリストする製品情報パネルのタブ。

![製品および価格アラートの配信登録のリスト](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 製品アラートの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. をクリックして、 _[!UICONTROL Product Alerts]_を選択し、次の操作を実行します。

   ![製品アラート](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 顧客に価格変更アラートを提供するには、次のように設定します **[!UICONTROL Allow Alert When Product Price Changes]** 対象： `Yes`.

   - を設定 **[!UICONTROL Price Alert Email Template]** 価格アラート通知に使用するテンプレート。

   - 在庫切れの製品が再び使用可能になった場合にアラートを提供するには、次のように設定します **[!UICONTROL Allow Alert When Product Comes Back in Stock]** 対象： `Yes`.

     >[!NOTE]
     >
     >この _この製品の在庫切れを通知_ メッセージが表示されるのは、 **[!UICONTROL Display Out of Stock Products]** はに設定されています。 `Yes` （の設定 [!UICONTROL Catalog] > [!UICONTROL Inventory]）に設定します。

   - を設定 **[!UICONTROL Stock Alert Email Template]** を製品ストックアラートに使用するテンプレートに関連付けます。

   - を設定 **[!UICONTROL Alert Email Sender]** に [店舗の連絡先](../getting-started/store-details.md#store-email-addresses){target="_blank"} メールアラートの送信者として表示させる。 の詳細情報 [メールアドレスの保存](../configuration-reference/general/store-email-addresses.md){target="_blank"} （コアユーザーガイド）を参照してください。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 製品アラートのメールテンプレートを設定

次に、価格アラートのメールテンプレートを設定、追加、変更します。 追加のテンプレートを作成した後で、価格アラートの設定を編集することができます。

メールメッセージの使用について詳しくは、 [メッセージテンプレート](../systems/email-template-custom.md#message-templates) が含まれる _管理システムガイド_.

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. 次の下 _デフォルトのテンプレートを読み込む_、を選択します **[!UICONTROL Template]** をカスタマイズします。

   テーマに含まれるアラートテンプレートを選択することもできます。 または、以下から選択できます `Price Alert` または `Stock Alert` 下のテンプレート _[!UICONTROL Magento_PriceAlert]_.

1. クリック **[!UICONTROL Load Template]**.

1. を入力 **[!UICONTROL Template Name]**.

   この名前は、 _価格アラート_ 設定。

1. 既存のコンテンツを読み上げ、必要に応じて次の変更を行います。

   | フィールド | 説明 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | このテキストは、メールの件名に表示されます。 |
   | [!UICONTROL Template Content] | このテキストは、送信されたメールのコンテンツ全体に表示されます。 |

1. から生成された情報を追加するには [!DNL Commerce] データ、使用する **[!UICONTROL Insert Variable]** 使用可能な変数のリストを使用するオプション。

1. クリック **[!UICONTROL Save Template]**.

## 製品アラートの実行設定

これらの設定では、頻度を選択できます [!DNL Commerce] アラートの送信が必要な変更を確認します。 また、アラートの送信に失敗した場合に送信されるメールの受信者、送信者、テンプレートを選択することもできます。

![製品アラートの実行設定](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Catalog]** を選択します **[!UICONTROL Catalog]** その下に。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Product Alerts Run Settings]** セクション。

1. 製品アラートの送信頻度を決定するには、次のように設定します **[!UICONTROL Frequency]** を次のいずれかに変更します。

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 製品アラートが送信される時刻を決定するには、次のように設定します **[!UICONTROL Start Time]** 時、分、秒に変換します。

   >[!NOTE]
   >
   >製品アラートは、「product_alert」コンシューマーから送信されます。

1. の場合 **[!UICONTROL Error Email Recipient]**&#x200B;で、エラーが発生した場合の連絡先のメールアドレスを入力します。

1. の場合 **[!UICONTROL Error Email Sender]**&#x200B;で、エラー通知の送信者として表示されるストア id を選択します。

1. を設定 **[!UICONTROL Error Email Template]** をエラー通知に使用されるトランザクションメールテンプレートに追加します。

1. 完了したら、 **[!UICONTROL Save Config]**.
