---
title: セールスメール
description: 顧客への注文に関するコミュニケーションをサポートするようにセールスメールを設定する方法を説明します。
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
TQID: https://experienceleague.adobe.com/M9-GhmO0XeRC9sgZmQXpv759NN-5cM92Bd8ZxxM96yg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# セールスメール

複数のメールメッセージは、注文に関連するイベントによってトリガーされ、設定は類似しています。 メッセージの送信者、使用するメールテンプレート、およびメッセージのコピーを受け取る他のユーザーとして表示されるストア連絡先を特定してください。 セールスメールは、イベントによってトリガーされたときに、または事前に決められた間隔で送信することができます。

![営業設定 – セールスメール &#x200B;](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## 手順1: メールテンプレートの更新

[&#x200B; メールヘッダー](../systems/email-template-custom.md#header-template) テンプレートを更新して、ブランドと、必要に応じてその他のメールテンプレートを反映するようにしてください。 テンプレートの完全なリストについては、[&#x200B; メールテンプレート &#x200B;](../systems/email-templates.md)を参照してください。

## 手順2: 送信の種類を選択

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Sales Emails]**&#x200B;を選択します。

1. 必要に応じて、**[!UICONTROL General Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![営業設定 – 営業電子メールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   デフォルトでは、非同期送信は`Disable`に設定されています。 システム設定を変更するには、**[!UICONTROL Use system value]** チェックボックスをオフにし、**[!UICONTROL Asynchronous sending]**&#x200B;を次のいずれかに設定します。

   - `Disable` - イベントによってトリガーされたときにセールスメールを送信します。
   - `Enable` – 所定の間隔で定期的にセールスメールを送信します。

   Adobe Commerce サポートでは、非同期送信を有効にして、注文処理のパフォーマンスを向上させることをお勧めします。 Adobe Commerce サポート ナレッジベースの[注文処理に関する設定のベストプラクティス &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html)を参照してください。

## 手順3: 各セールスメールメッセージの詳細を入力します

1. 必要に応じて、**[!UICONTROL Order]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

   ![販売設定 – セールスメール注文](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]**&#x200B;が`Yes`に設定されていることを確認します（デフォルト）。

1. メッセージの送信者として表示されるストア連絡先に&#x200B;**[!UICONTROL New Order Confirmation Email]**&#x200B;を設定します。

1. 登録済みの顧客に送信される電子メールに使用されるテンプレートに&#x200B;**[!UICONTROL New Order Confirmation Template]**&#x200B;を設定します。

1. ストアのアカウントを持たないゲストに送信されるメールに使用されるテンプレートに&#x200B;**[!UICONTROL New Order Confirmation Template for Guest]**&#x200B;を設定します。

1. **[!UICONTROL Send Order Email Copy To]**&#x200B;に、新しい注文の電子メールのコピーを受け取るユーザーの電子メールアドレスを入力します。

   複数の受信者にコピーを送信する場合は、各アドレスをコンマで区切ります。

1. **[!UICONTROL Send Order Email Copy Method]**&#x200B;を次のいずれかに設定します：

   - `Bcc` – お客様に送信するのと同じメールのヘッダーに受信者を含めることで、_ブラインドの表敬文_&#x200B;を送信します。 BCC受信者は、お客様には表示されません。
   - `Separate Email` - コピーを別の電子メールとして送信します。

1. **[!UICONTROL Order Comments]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、これらの手順を繰り返します。

   ![販売設定 – セールスメール注文のコメント &#x200B;](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. 残りのセールスメールタイプの設定を完了します。

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

   プロンプトが表示されたら、ワークスペースの上部にあるメッセージの[Cache Management](../systems/cache-management.md) リンクをクリックし、無効なすべてのキャッシュをクリアします。
