---
title: ギフトレジストリの設定
description: ギフトレジストリを有効にし、関連する電子メール通知を設定する方法を説明します。
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# ギフトレジストリの設定

{{ee-feature}}

顧客にギフトレジストリを提供する前に、ギフトレジストリを有効にして、関連する電子メール通知を設定する必要があります。 Adobe Commerceは、ギフトレジストリワークフローのイベントに応じて、次の電子メール通知を送信します。

- 新しいギフトレジストリが作成されると、所有者に電子メールが送信され、レジストリへのリンクが記載されて共有可能になります。
- オプションで、店舗はギフトレジストリへのリンク付きの通知をギフトレジストリ所有者の友人や家族に送信できます。
- 品目がギフトレジストリから購入されると、所有者に通知されますが、購入者は示しません。

Adobe Commerceには、ブランドに合わせてカスタマイズできるこれらの電子メールメッセージごとに、事前定義済みのテンプレートが用意されています。

## 手順 1. ギフトレジストリを有効にする

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Customers]** を選択します。 **[!UICONTROL Gift Registry]**

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General Options]** 」セクションで次の操作を実行します。

   ![お客様の設定 — ギフトレジストリ一般](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - ギフトレジストリは、デフォルトで有効になっています。 必要に応じて、 **[!UICONTROL Enable Gift Registry]** から `Yes`.

   - の場合 **[!UICONTROL Maximum Registrants]**&#x200B;の場合は、ギフトレジストリイベントへの参加を招待できる最大人数を入力します。

## 手順 2. 電子メール通知の設定

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Owner Notification]** 」セクションで次の操作を実行します。

   ![顧客の設定 — ギフトレジストリ所有者への通知](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** これは、自分の登記簿が作成された際に、贈与登録所の所有者に通知する。

   - を選択します。 [ストア連絡先](../getting-started/store-details.md#store-email-addresses) は **[!UICONTROL Email Sender]** メッセージの

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Gift Registry Sharing]** 」セクションで次の操作を実行します。

   ![顧客の設定 — ギフトレジストリの共有](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** これは、レジストリが共有されたときにギフトレジストリの受信者に通知します。

   - と表示されるストア ID を選択します。 **[!UICONTROL Email Sender]** メッセージの

   - の場合 **[!UICONTROL Maximum Sent Emails Threshold]**：一度に送信できる電子メールの最大数を入力します。

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Gift Registry Update]** 」セクションで次の操作を実行します。

   ![顧客の設定 — ギフトレジストリの更新](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - を選択します。 **[!UICONTROL Email Template]** これは、贈与登録所有者に対し、登録簿の変更を通知する。

   - と表示されるストア ID を選択します。 **[!UICONTROL Email Sender]** メッセージの

1. 完了したら、「 **[!UICONTROL Save Config]**.

1. プロンプトが表示されたら、キャッシュを更新します。

   キャッシュが更新されると、ギフトレジストリが「その他の設定」の下の「ストア」メニューに表示され、顧客アカウントで使用できるようになります。
