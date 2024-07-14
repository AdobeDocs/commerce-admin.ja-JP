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

![ 販売の構成 – 販売メール ](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 手順 1. メールテンプレートの更新

[ メールヘッダー ](../systems/email-template-custom.md#header-template) テンプレートを、ブランドや必要に応じて他のメールテンプレートが反映されるように、必ず更新してください。 テンプレートの完全なリストについては、「[ メールテンプレート ](../systems/email-templates.md)」を参照してください。

## 手順 2. 送信のタイプを選択

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Sales Emails]**」を選択します。

1. 必要に応じて、「拡張セレクター ![ の「**[!UICONTROL General Settings]**」セクション ](../assets/icon-display-expand.png) 展開します。

   ![ 販売の設定 – 販売メールの一般設定 ](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   デフォルトでは、非同期送信は `Disable` に設定されています。 システム設定を変更するには、「**[!UICONTROL Use system value]**」チェックボックスをオフにして、**[!UICONTROL Asynchronous sending]** を次のいずれかに設定します。

   - `Disable` - イベントによってトリガーされたときに販売メールを送信します。
   - `Enable` – 事前に決められた一定の間隔で販売メールを送信します。

   Adobe Commerce サポートでは、注文パフォーマンスを向上させるために、非同期送信を有効にすることをお勧めします。 Adobe Commerce サポートナレッジベースの [ 注文処理の設定のベストプラクティス ](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) を参照してください。

## 手順 3. 各販売メールメッセージの詳細を入力します

1. 必要に応じて、「拡張セレクター ![ の「**[!UICONTROL Order]**」セクション ](../assets/icon-display-expand.png) 展開します。

   ![ 販売設定 – 販売 E メールの注文 ](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]** が `Yes` （デフォルト）に設定されていることを確認します。

1. メッセージの送信者として表示されるストアの連絡先に **[!UICONTROL New Order Confirmation Email]** を設定します。

1. 登録済みの顧客に送信するメールに使用するテンプレートに **[!UICONTROL New Order Confirmation Template]** を設定します。

1. ストアのアカウントを持っていないゲストに送信するメールに使用するテンプレートに **[!UICONTROL New Order Confirmation Template for Guest]** を設定します。

1. **[!UICONTROL Send Order Email Copy To]**：新しい注文メールのコピーを受信するユーザーのメールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. **[!UICONTROL Send Order Email Copy Method]** を次のいずれかに設定します。

   - `Bcc` – 顧客に送信されるのと同じメールのヘッダーに受信者を含めることで、_ブラインドの儀礼用コピー_ を送信します。 BCC 受信者が顧客に表示されない。
   - `Separate Email` - コピーを個別のメールとして送信します。

1. **[!UICONTROL Order Comments]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下の手順を繰り返します。

   ![ 販売設定 – 販売 E メール注文コメント ](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 残りの販売 E メール・タイプの構成を入力します。

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

   プロンプトが表示されたら、ワークスペース上部のメッセージにある「[ キャッシュ管理 ](../systems/cache-management.md)」リンクをクリックし、無効なキャッシュをすべてクリアします。
