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

_メール送信設定_ を使用すると、返されたメールや返信を特定のアドレスにルーティングできます。 ストアが SMTP または Windows サーバー上で実行されている場合は、ホストとポートの設定を確認できます。

>[!IMPORTANT]
>
>**セキュリティに関する通知** すべてのマーチャントは、最近特定された潜在的なリモートコード実行の不正利用から保護するために、直ちにメール送信設定を設定する必要があります。 この問題が解決されるまで、メール通信に [!DNL Sendmail] を使用しないことを強くお勧めします。 _[!UICONTROL Mail Sending Settings]_&#x200B;で、_[!UICONTROL Set Return Path]_ が `No` に設定されていることを確認します。

設定の詳細なリストについては、_設定リファレンス_ の [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) を参照してください。

## メール通信を設定する

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. **[!UICONTROL Mail Sending Settings]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、以下を実行します。

   ![ 詳細設定 – メール送信設定 ](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 必要に応じて、**[!UICONTROL Disable Email Communications]** を `No` に設定します。

   - **[!UICONTROL Transport]**：ストアからのメール通信用のトランスポートタイプ（`Sendmail` または `SMTP`）を選択します。

   - SMTP または Windows サーバーで実行している場合は、次の設定を確認してください。

      - **[!UICONTROL Host]** - `localhost` またはその他

      - **[!UICONTROL Port (25)]** - `25` またはその他

   - **[!UICONTROL Set Return Path]** の場合、次のいずれかのオプションを選択します。

      - `No` - （推奨されるセキュリティ対策）返されたメールをデフォルトのストアメールアドレスにルーティングします。
      - `Yes` – 返されたメールをデフォルトのストアメールアドレスにルーティングします。
      - `Specified` - **[!UICONTROL Return Path Email]** で指定されたメールアドレスに返されたメールをルートします。

   - SMTP サーバー上で実行している場合は、接続を設定します。

      - **[!UICONTROL Username]** - SMTP サーバーのログインユーザー名を入力します。
      - **[!UICONTROL Password]** - SMTP サーバーログインのパスワードを入力します。
      - **[!UICONTROL Auth]** - SMTP サーバー接続の認証タイプを `NONE`、`PLAIN`、`LOGIN` から選択します
      - **[!UICONTROL SSL]** - サーバーセキュリティ証明書の検証の種類を選択します：`SSL` または `TLS`

     ![ 詳細設定 – メール送信設定 ](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 左側のパネルで「**[!UICONTROL Sales]**」を展開し、「**[!UICONTROL Sales Emails]**」を選択します。

1. 「![ 展開セレクター ](../assets/icon-display-expand.png)」を展開し、「**[!UICONTROL General Settings]**」セクションを展開します。

1. **[!UICONTROL Asynchronous sending]** を `Enable` に設定します。

   ![ 販売設定 – メールの一般設定 ](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   設定の詳細な一覧については、『設定リファレンス _の[_ 一般設定 _](../configuration-reference/sales/sales-emails.md)を参照してください_。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
