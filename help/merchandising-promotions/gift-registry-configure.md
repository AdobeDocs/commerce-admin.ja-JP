---
title: ギフト レジストリの構成
description: ギフトレジストリを有効にする方法と、関連するメール通知を設定する方法を説明します。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# ギフト レジストリの構成

{{ee-feature}}

顧客にギフトレジストリを提供する前に、ギフトレジストリを有効にし、関連するメール通知を設定する必要があります。 Adobe Commerceは、ギフトレジストリワークフロー内のイベントに応答して、次のメール通知を送信します。

- 新しいギフトレジストリが作成されると、共有できるレジストリへのリンクが記載されたメールが所有者に送信されます。
- 必要に応じて、ストアは、ギフト登録所有者の友人や家族にギフトレジストリへのリンクを持つ通知を送信できます。
- ギフト登録時に商品を購入した場合は、所有者に通知されますが、購入者には通知されません。

Adobe Commerceには、これらの各メールメッセージ用のテンプレートが事前定義されており、ブランドに合わせてカスタマイズできます。

## 手順 1. ギフト レジストリを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Customers]**」を展開し、「**[!UICONTROL Gift Registry]**」を選択します。

1. **[!UICONTROL General Options]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客の設定 – ギフトレジストリの一般 &#x200B;](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - ギフト レジストリは既定で有効になっています。 必要に応じて、**[!UICONTROL Enable Gift Registry]** を `Yes` に設定します。

   - **[!UICONTROL Maximum Registrants]**: ギフトレジストリイベントへの参加を招待できる最大人数を入力します。

## 手順 2. メール通知を設定する

1. **[!UICONTROL Owner Notification]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客の構成 – ギフト レジストリ所有者の通知 &#x200B;](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - ギフト レジストリの作成時に所有者に通知する **[!UICONTROL Email Template]** を選択してください。

   - メッセージの **[!UICONTROL Email Sender]** として表示される [&#x200B; ストアの連絡先 &#x200B;](../getting-started/store-details.md#store-email-addresses) を選択します。

1. **[!UICONTROL Gift Registry Sharing]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客の設定 – ギフトレジストリの共有 &#x200B;](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - レジストリが共有されたときにギフト レジストリの受信者に通知する **[!UICONTROL Email Template]** を選択してください。

   - メッセージの **[!UICONTROL Email Sender]** として表示されるストア ID を選択します。

   - **[!UICONTROL Maximum Sent Emails Threshold]**：一度に送信できるメールの最大数を入力します。

1. **[!UICONTROL Gift Registry Update]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![&#x200B; 顧客の設定 – ギフトレジストリの更新 &#x200B;](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - レジストリに対する変更をギフト レジストリ所有者に通知する **[!UICONTROL Email Template]** を選択してください。

   - メッセージの **[!UICONTROL Email Sender]** として表示されるストア ID を選択します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

1. プロンプトが表示されたら、キャッシュを更新します。

   キャッシュが更新されると、その他の設定の下のストアメニューにギフトレジストリが表示され、カスタマーアカウントで利用できるようになります。
