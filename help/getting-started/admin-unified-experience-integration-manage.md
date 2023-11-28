---
title: Experience Cloud統合の管理
description: Experience Cloud統合の管理方法と問題のトラブルシューティング方法を説明します。
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Experience Cloud統合の管理

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

初回の有効化後、コマース管理の統合エクスペリエンス拡張機能を有効または無効にして、Experience Cloud統合のステータスを管理します。

- コマース管理 Unified Experience 拡張機能が有効になっていて、管理者アカウントが [適切にプロビジョニング](#manage-admin-user-accounts)コマース管理者は、使用可能な Commerce プロジェクトをAdobe Experience Cloudから表示してアクセスできます。 管理者は、コマースプロジェクト環境の管理 URL を使用して、個々のプロジェクトにアクセスできます。

- コマース管理 Unified Experience 拡張機能が無効になっている場合、Experience Cloudを介したアクセスは無効になります。 管理者は、コマースプロジェクト環境の管理 URL を使用して個々のプロジェクトにログインする必要があります。

>[!WARNING]
>
>AdobeIdentity Managementサービス (IMS) の統合が無効になっている場合、Experience Cloudの統合は自動的に無効になります。

## 管理者からの統合の管理

1. コマース管理から、 **[!UICONTROL Stores]** 左側のナビゲーションメニューから、「 **[!UICONTROL Configuration]**.

1. 設定メニューから、「 」を選択します。 **[!UICONTROL Advanced > Admin]**&#x200B;をクリックし、次にを展開します。 **[!UICONTROL Unified Experience option]**.

   ![Experience Cloud統合用の管理ストアの設定](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. 統合を有効または無効にするには、 **[!UICONTROL Enable]** の値です。

1. 「コマースプロジェクト」ワークスペースに表示されるプロジェクト名を変更するには、 **[!UICONTROL Project Name]** の値です。

1. 設定を保存します。

1. キャッシュをクリアします。

## Adobe Commerce CLI を使用した統合の管理

Commerce Cloud プロジェクトへの管理者アクセス権を持つ Commerce システム管理者は、 Adobe Commerce CLI コマンドを使用してExperience Cloud統合を管理できます。

1. ローカル開発環境から、クラウドプロジェクトにログインします。

   ```bash
   magento-cloud login
   ```

1. クラウドプロジェクト環境のルートディレクトリから、Commerce アプリケーションサーバーに接続します。

   ```bash
   ssh magento-cloud
   ```

1. 管理 Unified Experience 拡張機能のステータスを確認します。

   ```bash
   bin/magento admin:uex:status
   ```

1. 拡張機能のステータスを変更して統合を無効にします。

   - **有効にする**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **無効にする**—`bin/magento config:set admin/unified_experience/enabled 0`

## 管理者ユーザーアカウントを管理

すべての Commerce 管理者ユーザーがAdobe製品およびサービスにアクセスするには、コマースインスタンスの管理者アカウントとAdobeユーザーアカウント (Adobe ID) の両方を持っている必要があります。 両方のアカウントを同じ電子メールアドレスに関連付ける必要があります。

- **コマース管理者アカウント**—[コマース管理者ユーザーの管理](../systems/permissions-users-all.md) コマースインスタンスの管理者から。 コマース管理者のユーザーアカウントには、管理者の役割が割り当てられている必要があります。

  コマースプロジェクトのシステム管理者は、 [リモート環境に接続するための SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)、Commerce CLI を使用します。 `admin:user:create` および `admin:user:unlock` 管理者ユーザーアカウントを追加またはロック解除するコマンド

- **Adobeユーザーアカウント** — コマースインスタンスに関連付けられているAdobe組織の管理者は、Adobe Admin Consoleにログインし、各コマース管理者のAdobe IDを組織に追加する必要があります。 次に、コマースアプリケーションにアクセスするための製品の使用権限と権限を割り当てる必要があります。 詳しくは、 [Adobe Admin ConsoleでのAdobe Commerceユーザーの設定](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Adobe DeveloperコンソールからExperience Cloud統合の設定を管理する管理者は、システム管理者または開発者のアクセス権を持つAdobeユーザーアカウントを持っている必要があります。

>[!NOTE]
>
>Adobe IDは、Adobeを通じて作成されるアカウントで、製品やサービスにExperience Cloudを通じてアクセスするために必要です。 Adobe IDを持っていないコマース管理者は、 [無料アカウントを作成する](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) コマース管理者へのログインに使用するのと同じ電子メールアドレスを使用します。
