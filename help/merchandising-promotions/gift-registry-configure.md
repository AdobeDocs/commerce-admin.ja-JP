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

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Customers]** を選択します **[!UICONTROL Gift Registry]**

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General Options]** を選択し、次の操作を実行します。

   ![顧客の構成 – ギフト レジストリ全般](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - ギフト レジストリは既定で有効になっています。 必要に応じて、を設定します **[!UICONTROL Enable Gift Registry]** 対象： `Yes`.

   - の場合 **[!UICONTROL Maximum Registrants]**：ギフトレジストリイベントへの参加を招待できる最大人数を入力します。

## 手順 2. メール通知を設定する

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Owner Notification]** を選択し、次の操作を実行します。

   ![顧客の構成 – ギフト レジストリ所有者の通知](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** ギフト レジストリの所有者にレジストリの作成時に通知します。

   - を選択します。 [店舗の連絡先](../getting-started/store-details.md#store-email-addresses) として表示されます **[!UICONTROL Email Sender]** （メッセージ）。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Gift Registry Sharing]** を選択し、次の操作を実行します。

   ![顧客の設定 – ギフトレジストリの共有](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** レジストリが共有されたときに、ギフト レジストリの受信者に通知します。

   - 表示されるストア ID を選択します。 **[!UICONTROL Email Sender]** （メッセージ）。

   - の場合 **[!UICONTROL Maximum Sent Emails Threshold]**&#x200B;に設定し、一度に送信できるメールの最大数を入力します。

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Gift Registry Update]** を選択し、次の操作を実行します。

   ![顧客の構成 – ギフト レジストリの更新](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** ギフト レジストリの所有者にレジストリの変更を通知します。

   - 表示されるストア ID を選択します。 **[!UICONTROL Email Sender]** （メッセージ）。

1. 完了したら、 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、キャッシュを更新します。

   キャッシュが更新されると、その他の設定の下のストアメニューにギフトレジストリが表示され、カスタマーアカウントで利用できるようになります。
