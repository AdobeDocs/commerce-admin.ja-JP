---
title: メール通信を設定する
description: 返されたメールのルーティングや特定のメールアドレスへの返信など、メール通信を設定する方法を説明します。
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# メール通信を設定する

この _メール送信設定_ 返信または返信を特定のアドレスにルーティングする機能を提供する。 ストアが SMTP または Windows サーバー上で実行されている場合は、ホストとポートの設定を確認できます。

>[!IMPORTANT]
>
>**セキュリティに関する通知** すべてのマーチャントは、最近特定された潜在的なリモートコード実行の悪用から保護するために、すぐにメール送信設定を設定する必要があります。 この問題が解決されるまで、を使用しないことを強くお勧めします [!DNL Sendmail] メール通信の場合。 が含まれる _[!UICONTROL Mail Sending Settings]_必ずしてください_[!UICONTROL Set Return Path]_ はに設定されています。 `No`.

設定の詳細なリストについては、を参照してください [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) が含まれる _設定リファレンス_.

## メール通信を設定する

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Mail Sending Settings]** を選択し、次の操作を実行します。

   ![詳細設定 – メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 必要に応じて、を設定します **[!UICONTROL Disable Email Communications]** 対象： `No`.

   - の場合 **[!UICONTROL Transport]**、ストアからメール通信用のトランスポートタイプを選択します。 `Sendmail` または `SMTP`

   - SMTP または Windows サーバーで実行している場合は、次の設定を確認してください。

      - **[!UICONTROL Host]** - `localhost` またはその他

      - **[!UICONTROL Port (25)]** - `25` またはその他

   - の場合 **[!UICONTROL Set Return Path]**&#x200B;次のいずれかのオプションを選択します。

      - `No` - （推奨されるセキュリティ対策）返されたメールをデフォルトのストアメールアドレスにルーティングします。
      - `Yes` - デフォルトのストアメールアドレスに返されたメールをルートします。
      - `Specified`  – 返されるメールを次で指定されたメールアドレスにルーティングします： **[!UICONTROL Return Path Email]**.

   - SMTP サーバー上で実行している場合は、接続を設定します。

      - **[!UICONTROL Username]** - SMTP サーバーのログインユーザー名を入力します。
      - **[!UICONTROL Password]** - SMTP サーバーログインのパスワードを入力します。
      - **[!UICONTROL Auth]** - SMTP サーバー接続の認証の種類を選択してください： `NONE` , `PLAIN`、または `LOGIN`
      - **[!UICONTROL SSL]** - サーバーセキュリティ証明書の検証の種類を選択してください： `SSL` または `TLS`

     ![詳細設定 – メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 左側のパネルで、を展開します **[!UICONTROL Sales]** を選択します **[!UICONTROL Sales Emails]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL General Settings]** セクション。

1. を設定 **[!UICONTROL Asynchronous sending]** 対象： `Enable`.

   ![販売設定 – メールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   設定の詳細なリストについては、を参照してください [_一般設定_](../configuration-reference/sales/sales-emails.md) が含まれる _設定リファレンス_.

1. 完了したら、 **[!UICONTROL Save Config]**.
