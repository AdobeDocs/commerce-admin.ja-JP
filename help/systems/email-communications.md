---
title: メール通信の設定
description: 返される電子メールのルーティングや特定の電子メールアドレスへの返信など、電子メールのコミュニケーションを設定する方法について説明します。
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# メール通信の設定

_メール送信設定_&#x200B;を使用すると、返されたメールまたは返信を特定のアドレスに送信できます。 ストアがSMTPまたはWindows サーバー上で実行されている場合は、ホストとポートの設定を確認できます。

>[!IMPORTANT]
>
>**セキュリティ通知**&#x200B;すべての販売者は、最近特定された潜在的なリモート コード実行の悪用から保護するために、メール送信設定を直ちに設定する必要があります。 この問題が解決されるまで、メール通信に[!DNL Sendmail]を使用することを避けることを強くお勧めします。 _[!UICONTROL Mail Sending Settings]_で、_[!UICONTROL Set Return Path]_&#x200B;が`No`に設定されていることを確認してください。

設定設定の詳細なリストについては、_設定リファレンス_&#x200B;の[_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md)を参照してください。

## メール通信の設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. **[!UICONTROL Mail Sending Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次の操作を行います。

   ![詳細設定 – メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 必要に応じて、**[!UICONTROL Disable Email Communications]**&#x200B;を`No`に設定します。

   - **[!UICONTROL Transport]**&#x200B;の場合、ストアからメール通信のトランスポートのタイプを選択します：`Sendmail`または`SMTP`

   - SMTPまたはWindows サーバーで実行している場合は、次の設定を確認します。

      - **[!UICONTROL Host]** - `localhost`またはその他

      - **[!UICONTROL Port (25)]** - `25`またはその他

   - **[!UICONTROL Set Return Path]**&#x200B;の場合、次のいずれかのオプションを選択します。

      - `No` - （推奨されるセキュリティ対策）ルートがデフォルトのストア電子メールアドレスに電子メールを返しました。
      - `Yes` - ルートがデフォルトのストア電子メールアドレスに電子メールを返しました。
      - `Specified` - ルートは、**[!UICONTROL Return Path Email]**&#x200B;で指定された電子メールアドレスに電子メールを返しました。

   - SMTP サーバーで実行している場合は、接続を設定します。

      - **[!UICONTROL Username]** - SMTP サーバーのログインユーザー名を入力します。
      - **[!UICONTROL Password]** - SMTP サーバーログインのパスワードを入力します。
      - **[!UICONTROL Auth]** - SMTP サーバー接続の認証タイプを選択：`NONE`、`PLAIN`、または`LOGIN`
      - **[!UICONTROL SSL]** - サーバーセキュリティ証明書の検証タイプを選択してください：`SSL`または`TLS`

     ![詳細設定 – メール送信設定](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 左側のパネルで、**[!UICONTROL Sales]**&#x200B;を展開し、**[!UICONTROL Sales Emails]**&#x200B;を選択します。

1. **[!UICONTROL General Settings]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Asynchronous sending]**&#x200B;を`Enable`に設定します。

   ![営業設定 – メールの一般設定](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   設定設定の詳細なリストについては、_設定リファレンス_&#x200B;の&#x200B;[_一般設定_](../configuration-reference/sales/sales-emails.md)&#x200B;を参照してください。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。
