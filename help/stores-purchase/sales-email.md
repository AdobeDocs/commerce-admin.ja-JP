---
title: セールスメール
description: 注文に関する顧客へのコミュニケーションをサポートするようにセールスメールを設定する方法を説明します。
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# セールスメール

複数の電子メールメッセージは、1 つの注文に関連するイベントによってトリガーされ、設定は似ています。 メッセージの送信者として表示されるストアの連絡先、使用する E メールテンプレート、メッセージのコピーを受け取る他のユーザーを必ず識別してください。 セールス E メールは、イベントでトリガーされたとき、または事前に定義された間隔で送信できます。

![セールス構成 — セールスメール](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 手順 1. E メールテンプレートの更新

必ず [電子メールヘッダー](../systems/email-template-custom.md#header-template) テンプレートを使用して、ブランドや他の電子メールテンプレートを必要に応じて反映させることができます。 テンプレートの完全なリストについては、 [電子メールテンプレート](../systems/email-templates.md).

## 手順 2. 送信の種類を選択

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales Emails]**.

1. 必要に応じて、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の  **[!UICONTROL General Settings]** 」セクションに入力します。

   ![セールス構成 — セールスメールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   デフォルトでは、非同期送信はに設定されています。 `Disable`. システム設定を変更するには、 **[!UICONTROL Use system value]** チェックボックスとセット **[!UICONTROL Asynchronous sending]** を次のいずれかに変更します。

   - `Disable`  — イベントでトリガーされた場合に、セールスメールを送信します。
   - `Enable`  — 事前に定期的な間隔でセールスメールを送信します。

   Adobe Commerceサポートでは、注文の配置パフォーマンスを向上させるために、非同期送信を有効にすることをお勧めします。 詳しくは、 [注文処理の設定のベストプラクティス](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) ( Adobe Commerce Support Knowledge Base )。

## 手順 3. 各セールスメールメッセージの詳細を入力

1. 必要に応じて、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order]** 」セクションに入力します。

   ![セールス構成 — セールスメール注文](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. を確認します。 **[!UICONTROL Enabled]** が `Yes` （デフォルト）。

1. 設定 **[!UICONTROL New Order Confirmation Email]** メッセージの送信者として表示されるストア連絡先に追加します。

1. 設定 **[!UICONTROL New Order Confirmation Template]** を、登録済みの顧客に送信する e メールに使用されるテンプレートに追加します。

1. 設定 **[!UICONTROL New Order Confirmation Template for Guest]** を、ストアにアカウントを持たないゲストに送信される e メールに使用されるテンプレートに追加します。

1. の場合 **[!UICONTROL Send Order Email Copy To]**「 」に、新しい注文の E メールのコピーを受け取る人の E メールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. 設定 **[!UICONTROL Send Order Email Copy Method]** を次のいずれかに変更します。

   - `Bcc`  — を送信します。 _盲目の厚意コピー_ 顧客に送信されるのと同じ e メールのヘッダーに受信者を含めることで、 BCC 受信者は、顧客に対して表示されません。
   - `Separate Email`  — コピーを別の E メールとして送信します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Order Comments]** を参照し、これらの手順を繰り返します。

   ![セールス構成 — セールスメールの注文コメント](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 残りのセールスメールタイプの設定を完了します。

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完了したら、「 **[!UICONTROL Save Config]**.

   プロンプトが表示されたら、 [キャッシュ管理](../systems/cache-management.md) ワークスペースの上部にあるメッセージ内のリンクをクリックし、無効なキャッシュをすべてクリアします。
