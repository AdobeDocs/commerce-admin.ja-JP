---
title: 販売メール
description: 顧客の注文に関するコミュニケーションをサポートするための販売メールを設定する方法を説明します。
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# 販売メール

1 つの注文に関連するイベントで複数のメールメッセージがトリガーされ、設定も同様です。 メッセージの送信者として表示されるストアの連絡先、使用するメールテンプレートおよびメッセージのコピーを受信する他のユーザーを必ず識別してください。 販売メールは、イベントによってトリガーされたとき、または事前に決められた間隔で送信することができます。

![販売設定 – 販売メール](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 手順 1. メールテンプレートの更新

必ずを更新してください。 [メールヘッダー](../systems/email-template-custom.md#header-template) テンプレートを使用して、ブランドや必要に応じて他のメールテンプレートを反映させる。 テンプレートの完全なリストについては、を参照してください [メールテンプレート](../systems/email-templates.md).

## 手順 2. 送信のタイプを選択

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales Emails]**.

1. 必要に応じて、を展開 ![展開セレクター](../assets/icon-display-expand.png) この  **[!UICONTROL General Settings]** セクション。

   ![販売の設定 – 販売メールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   デフォルトでは、非同期送信はに設定されています。 `Disable`. システム設定を変更するには、 **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Asynchronous sending]** を次のいずれかに変更します。

   - `Disable` - イベントによってトリガーされたときに販売メールを送信します。
   - `Enable`  – 事前に決められた一定の間隔で販売メールを送信します。

   Adobe Commerce サポートでは、注文パフォーマンスを向上させるために、非同期送信を有効にすることをお勧めします。 参照： [オーダー処理の設定のベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) （Adobe Commerce サポートナレッジベース）。

## 手順 3. 各販売メールメッセージの詳細を入力します

1. 必要に応じて、を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order]** セクション。

   ![販売設定 – 販売 E メール注文](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. を確認します。 **[!UICONTROL Enabled]** はに設定されています。 `Yes` （デフォルト）。

1. を設定 **[!UICONTROL New Order Confirmation Email]** メッセージの送信者として表示されるストアの連絡先に送信されます。

1. を設定 **[!UICONTROL New Order Confirmation Template]** 登録済みの顧客に送信するメールに使用するテンプレート。

1. を設定 **[!UICONTROL New Order Confirmation Template for Guest]** を、ストアにアカウントを持たないゲストに送信されるメールに使用されるテンプレートに設定します。

1. の場合 **[!UICONTROL Send Order Email Copy To]**&#x200B;新しい注文メールのコピーを受信するユーザーのメールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. を設定 **[!UICONTROL Send Order Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  – が _盲目の礼状コピー_ 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで答えることができます。 BCC 受信者が顧客に表示されない。
   - `Separate Email` - コピーを別のメールとして送信します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Order Comments]** を参照し、これらの手順を繰り返します。

   ![販売設定 – 販売 E メール注文コメント](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 残りの販売 E メール・タイプの構成を入力します。

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完了したら、 **[!UICONTROL Save Config]**.

   プロンプトが表示されたら、 [キャッシュ管理](../systems/cache-management.md) ワークスペースの上部にあるメッセージのリンクをクリックし、無効なキャッシュをすべてクリアします。
