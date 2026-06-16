---
title: ギフトレジストリの設定
description: ギフトレジストリを有効にし、関連するメール通知を設定する方法について説明します。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# ギフトレジストリの設定

{{ee-feature}}

顧客にギフトレジストリを提供する前に、ギフトレジストリを有効にし、関連するメール通知を設定する必要があります。 Adobe Commerceは、ギフトレジストリワークフローのイベントに応じて、次のメール通知を送信します。

- 新しいギフトレジストリが作成されると、共有可能なレジストリへのリンクが記載されたメールが所有者に送信されます。
- オプションとして、ストアは、ギフトレジストリ所有者の友人や家族にギフトレジストリへのリンクを含む通知を送信できます。
- 所有者は、ギフトレジストリからアイテムを購入すると通知されますが、購入者は表示されません。

Adobe Commerceには、これらのメールメッセージごとに事前に定義されたテンプレートがあり、ブランドに合わせてカスタマイズできます。

## 手順1: ギフトレジストリを有効にする

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Customers]**&#x200B;を展開し、**[!UICONTROL Gift Registry]**&#x200B;を選択します

1. **[!UICONTROL General Options]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ギフトレジストリ全般](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - ギフトレジストリはデフォルトで有効になっています。 必要に応じて、**[!UICONTROL Enable Gift Registry]**&#x200B;を`Yes`に設定します。

   - **[!UICONTROL Maximum Registrants]**&#x200B;について、ギフトレジストリイベントに参加するために招待できる最大人数を入力します。

## 手順2: メール通知の設定

1. **[!UICONTROL Owner Notification]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ギフトレジストリ所有者の通知](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - レジストリの作成時にギフトレジストリの所有者に通知する&#x200B;**[!UICONTROL Email Template]**&#x200B;を選択します。

   - メッセージの&#x200B;**[!UICONTROL Email Sender]**&#x200B;として表示される[store連絡先](../getting-started/store-details.md#store-email-addresses)を選択します。

1. **[!UICONTROL Gift Registry Sharing]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ギフトレジストリの共有](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - レジストリが共有されたときにギフトレジストリの受信者に通知する&#x200B;**[!UICONTROL Email Template]**&#x200B;を選択します。

   - メッセージの&#x200B;**[!UICONTROL Email Sender]**&#x200B;として表示されるストア IDを選択します。

   - **[!UICONTROL Maximum Sent Emails Threshold]**&#x200B;の場合、一度に送信できるメールの最大数を入力します。

1. **[!UICONTROL Gift Registry Update]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![お客様の設定 – ギフトレジストリの更新](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - レジストリの変更をギフトレジストリの所有者に通知する&#x200B;**[!UICONTROL Email Template]**&#x200B;を選択します。

   - メッセージの&#x200B;**[!UICONTROL Email Sender]**&#x200B;として表示されるストア IDを選択します。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

1. プロンプトが表示されたら、キャッシュを更新します。

   キャッシュが更新されると、Gift Registryは「その他の設定」の「ストア」メニューに表示され、顧客アカウントで利用できるようになります。
