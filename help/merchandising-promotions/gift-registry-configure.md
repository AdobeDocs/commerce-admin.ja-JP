---
title: ギフトレジストリの設定
description: ギフトレジストリを有効にし、関連するメール通知を設定する方法について説明します。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
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
