---
title: 電子メール通信の設定
description: 返信された E メールや特定の E メールアドレスへの返信のルーティングなど、E メール通信を設定する方法を説明します。
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 電子メール通信の設定

The _メール送信設定_ 返信されたメールまたは返信を特定のアドレスにルーティングする機能を提供します。 ストアが SMTP または Windows サーバー上で動作している場合は、ホストとポートの設定を確認できます。

>[!IMPORTANT]
>
>**セキュリティ通知** すべてのマーチャントは、最近特定されたリモートコード実行の悪用から保護するために、メール送信設定を直ちに設定する必要があります。 この問題が解決されるまでは、 [!DNL Sendmail] （電子メール通信用） Adobe Analytics の _[!UICONTROL Mail Sending Settings]_、次の点を確認します。_[!UICONTROL Set Return Path]_ が `No`.

設定の詳細なリストについては、 [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) （内） _設定リファレンス_.

## 電子メール通信の設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Mail Sending Settings]** 」セクションで次の操作を実行します。

   ![詳細設定 — メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 必要に応じて、 **[!UICONTROL Disable Email Communications]** から `No`.

   - の場合 **[!UICONTROL Transport]**、ストアから e メール通信用のトランスポートタイプを選択します。 `Sendmail` または `SMTP`

   - SMTP または Windows サーバーで実行している場合は、次の設定を確認します。

      - **[!UICONTROL Host]** - `localhost` またはその他

      - **[!UICONTROL Port (25)]** - `25` またはその他

   - の場合 **[!UICONTROL Set Return Path]**、次のいずれかのオプションを選択します。

      - `No` - （推奨されるセキュリティ対策）ルートがデフォルトのストア電子メールアドレスに電子メールを返しました。
      - `Yes`  — ルートがデフォルトのストア電子メールアドレスに電子メールを返しました。
      - `Specified`  — ルートは、 **[!UICONTROL Return Path Email]**.

   - SMTP サーバーで実行する場合は、接続を設定します。

      - **[!UICONTROL Username]** - SMTP サーバーのログインユーザー名を入力します。
      - **[!UICONTROL Password]** - SMTP サーバーログインのパスワードを入力します。
      - **[!UICONTROL Auth]** - SMTP サーバー接続の認証の種類を選択します。 `NONE` , `PLAIN`または `LOGIN`
      - **[!UICONTROL SSL]**  — サーバーのセキュリティ証明書の検証の種類を選択します。 `SSL` または `TLS`

     ![詳細設定 — メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 左側のパネルで、を展開します。 **[!UICONTROL Sales]** を選択します。 **[!UICONTROL Sales Emails]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL General Settings]** 」セクションに入力します。

1. 設定 **[!UICONTROL Asynchronous sending]** から `Enable`.

   ![セールス構成 — メールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   設定の詳細なリストについては、 [_一般設定_](../configuration-reference/sales/sales-emails.md) （内） _設定リファレンス_.

1. 完了したら、「 **[!UICONTROL Save Config]**.
