---
title: 製品アラート
description: 製品アラートと、製品の在庫ステータスと価格の変更を顧客に通知する方法について説明します。
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# 製品アラート

お客様は、価格変更アラートと在庫内アラートの 2 種類のアラートを E メールで購読できます。 アラートのタイプごとに、顧客が購読できるかどうかを決定し、使用する電子メールテンプレートを選択し、電子メールの送信者を特定できます。

![新規登録して製品アラートを受け取る](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 価格変更アラート

価格変更アラートが有効な場合、 _価格が下がったら通知する_ リンクはすべての製品ページに表示されます。 お客様は、このリンクをクリックして、製品に関連するアラートを購読できます。 お客様のストアでアカウントを開くように求められます。 価格が変更されたり、製品が特別に発生した場合は常に、アラートを購読したすべてのユーザーに電子メールアラートが送信されます。

## 在庫内アラート

在庫内アラートが作成するリンクの名前は次のとおりです。 _この製品が在庫にある場合に通知する_ 在庫切れのすべての製品に対して お客様は、このリンクをクリックしてアラートを購読できます。 製品が在庫に戻ると、その製品が使用可能になったことを顧客に電子メールで通知します。 アラートを含む製品には、 _製品アラート_ 」タブをクリックします。

![製品および価格アラート購読のリスト](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 製品アラートの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. をクリックして、 _[!UICONTROL Product Alerts]_」セクションで次の操作を実行します。

   ![製品アラート](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 価格変更アラートを顧客に提供するには、 **[!UICONTROL Allow Alert When Product Price Changes]** から `Yes`.

   - 設定 **[!UICONTROL Price Alert Email Template]** を、価格アラート通知に使用するテンプレートに追加します。

   - 在庫切れの製品が再び利用可能になったときにアラートを提供するには、 **[!UICONTROL Allow Alert When Product Comes Back in Stock]** から `Yes`.

     >[!NOTE]
     >
     >The _この製品が在庫にある場合に通知する_ 次の場合にのみメッセージが表示されます： **[!UICONTROL Display Out of Stock Products]** が `Yes` ( 設定 ( ) で、 [!UICONTROL Catalog] > [!UICONTROL Inventory]) をクリックします。

   - 設定 **[!UICONTROL Stock Alert Email Template]** を、製品在庫アラートに使用するテンプレートに追加します。

   - 設定 **[!UICONTROL Alert Email Sender]** から [ストア連絡先](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} 」を参照してください。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 製品アラート電子メールテンプレートの設定

次に、価格アラートの電子メールテンプレートを設定、追加または変更します。 追加のテンプレートを作成した後で、価格アラート設定を編集することもできます。

電子メールメッセージの使用について詳しくは、 [メッセージテンプレート](../systems/email-template-custom.md#message-templates) （内） _管理システムガイド_.

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. クリック **[!UICONTROL Add New Template]**.

1. の下 _デフォルトテンプレートを読み込み_、選択 **[!UICONTROL Template]** を選択します。

   テーマに含まれるアラートテンプレートを選択することもできます。 または、 `Price Alert` または `Stock Alert` 以下のテンプレート： _[!UICONTROL Magento_PriceAlert]_.

1. クリック **[!UICONTROL Load Template]**.

1. を入力します。 **[!UICONTROL Template Name]**.

   この名前は、 _価格に関するアラート_ 設定。

1. 既存のコンテンツを読み取り、必要に応じて変更します。

   | フィールド | 説明 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | このテキストは E メールの件名行に表示されます。 |
   | [!UICONTROL Template Content] | このテキストは、送信された E メールの完全なコンテンツに表示されます。 |

1. 次の場所から生成された情報を追加するには： [!DNL Commerce] データ、 **[!UICONTROL Insert Variable]** オプションを使用して、使用可能な変数のリストを使用します。

1. クリック **[!UICONTROL Save Template]**.

## 製品アラート実行設定

これらの設定では、 [!DNL Commerce] アラートの送信が必要な変更をチェックします。 また、アラートの送信が失敗した場合に送信される E メールの受信者、送信者、テンプレートを選択することもできます。

![製品アラート実行設定](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Catalog]** を選択します。 **[!UICONTROL Catalog]** の下に

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Product Alerts Run Settings]** 」セクションに入力します。

1. 製品アラートの送信頻度を決定するには、 **[!UICONTROL Frequency]** を次のいずれかに変更します。

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 製品アラートが送信される時刻を決定するには、 **[!UICONTROL Start Time]** 時分秒

   >[!NOTE]
   >
   >製品アラートは、「product_alert」コンシューマーによって送信されます。

1. の場合 **[!UICONTROL Error Email Recipient]**「 」で、エラーが発生した場合に連絡する人の E メールアドレスを入力します。

1. の **[!UICONTROL Error Email Sender]**「 」で、エラー通知の送信者として表示されるストア ID を選択します。

1. 設定 **[!UICONTROL Error Email Template]** エラー通知に使用するトランザクション e メールテンプレートに追加します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
