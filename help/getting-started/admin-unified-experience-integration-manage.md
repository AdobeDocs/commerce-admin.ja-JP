---
title: Experience Cloud統合の管理
description: Experience Cloudの統合の管理方法と問題のトラブルシューティング方法について説明します
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Experience Cloud統合の管理

最初のイネーブルメント後に、Commerce Admin Unified Experience 拡張機能を有効または無効にして、Experience Cloud統合のステータスを管理します。

- Commerce Admin Unified Experience Extension が有効になっていて、管理者アカウントが [正しくプロビジョニング](#manage-admin-user-accounts)を使用すると、Commerce管理者は、Adobe Experience Cloudから使用可能なCommerce プロジェクトを表示してアクセスできます。 管理者は、Commerce プロジェクト環境用の管理者 URL を使用して、個々のプロジェクトに引き続きアクセスできます。

- Commerce Admin Unified Experience 拡張機能が無効になっている場合は、Experience Cloudからのアクセスは無効になります。 管理者は、Commerce プロジェクト環境の管理者 URL を使用して、個々のプロジェクトにログインする必要があります。

>[!WARNING]
>
>AdobeのIdentity Management サービス（IMS）統合を無効にすると、Experience Cloud統合は自動的に無効になります。

## 管理者から統合を管理

1. Commerce管理者から、次の項目を選択して、ストア設定メニューを開きます。 **[!UICONTROL Stores]** 左側のナビゲーションメニューからを選択し、 **[!UICONTROL Configuration]**.

1. 設定メニューから、を選択します。 **[!UICONTROL Advanced > Admin]**&#x200B;を選択し、 **[!UICONTROL Unified Experience option]**.

   ![Experience Cloud統合用の管理ストアの設定](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. を選択して、統合を有効または無効にします **[!UICONTROL Enable]** の値。

1. を追加または更新して、Commerce プロジェクトワークスペースに表示されるプロジェクト名を変更します。 **[!UICONTROL Project Name]** の値。

1. 設定を保存します。

1. キャッシュをクリアします。

## Adobe Commerce CLI を使用した統合の管理

Commerce クラウドプロジェクトへの管理者アクセス権を持つCommerce システム管理者は、Adobe Commerce CLI コマンドを使用してExperience Cloud統合を管理できます。

1. ローカル開発環境からクラウドプロジェクトにログインします。

   ```bash
   magento-cloud login
   ```

1. クラウドプロジェクト環境のルートディレクトリから、Commerce アプリケーションサーバーに接続します。

   ```bash
   ssh magento-cloud
   ```

1. Admin Unified Experience 拡張機能のステータスを確認します。

   ```bash
   bin/magento admin:uex:status
   ```

1. 拡張機能のステータスを変更して統合を無効にする

   - **Enable （有効）**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **無効**—`bin/magento config:set admin/unified_experience/enabled 0`

## 管理者ユーザーアカウントの管理

すべてのCommerce管理者ユーザーは、Adobeの製品やサービスにアクセスするために、Commerce インスタンスの管理者アカウントとAdobeユーザーアカウント（Adobe ID）の両方を持っている必要があります。 両方のアカウントが同じメールアドレスに関連付けられている必要があります。

- **Commerce管理者アカウント**—[Commerce管理者ユーザーの管理](../systems/permissions-users-all.md) Commerce インスタンス用に管理者から。 Commerce管理者のユーザーアカウントには、管理者ロールが割り当てられている必要があります。

  Commerce プロジェクトのシステム管理者が使用できる [リモート環境に接続するための SSH](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment)Commerce CLI を使用する `admin:user:create` および `admin:user:unlock` 管理者ユーザーアカウントを追加またはロック解除するコマンド。

- **Adobeユーザーアカウント**- Commerce インスタンスに関連付けられているAdobe組織の管理者がAdobe Admin Consoleにログインして、Commerce管理者ごとにAdobe IDを組織に追加する必要があります。 次に、Commerce アプリケーションにアクセスするための製品の使用権限と権限を割り当てる必要があります。 参照： [Adobe Admin ConsoleでのAdobe Commerce ユーザーの設定](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Adobe Developer コンソールからExperience Cloud統合の設定を管理する管理者には、システム管理者または開発者アクセス権を持つAdobeユーザーアカウントが必要です。

>[!NOTE]
>
>Adobe IDは、Experience Cloudを通じて製品やサービスにアクセスするために必要な、Adobeを通じて作成されたアカウントです。 Adobe IDを持たないCommerce管理者は、次のことができます [無料アカウントを作成](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) Commerce管理者へのログインに使用するのと同じメールアドレスを使用します。
