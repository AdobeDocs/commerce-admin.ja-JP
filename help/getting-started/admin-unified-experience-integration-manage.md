---
title: Experience Cloud統合の管理
description: Experience Cloud統合の管理方法と問題のトラブルシューティング方法について説明します
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Experience Cloud統合の管理

最初のイネーブルメント後に、Experience Cloud Admin Unified Experience 拡張機能を有効または無効にして、Commerce統合のステータスを管理します。

- Commerce Admin Unified Experience Extension が有効になっていて、管理者アカウントが [ 正しくプロビジョニング ](#manage-admin-user-accounts) されている場合、Commerce管理者はAdobe Experience Cloudから使用可能なCommerce プロジェクトを表示してアクセスできます。 管理者は、Commerce プロジェクト環境用の管理者 URL を使用して、個々のプロジェクトに引き続きアクセスできます。

- Commerce Admin Unified Experience 拡張機能が無効になっている場合、Experience Cloud経由でのアクセスは無効になります。 管理者は、Commerce プロジェクト環境の管理者 URL を使用して、個々のプロジェクトにログインする必要があります。

>[!WARNING]
>
>Adobe Identity Management Service （IMS）統合を無効にすると、Experience Cloud統合は自動的に無効になります。

## 管理者から統合を管理

1. Commerce管理で、左側のナビゲーションメニューから「**[!UICONTROL Stores]**」を選択して Store Configuration メニューを開き、「**[!UICONTROL Configuration]**」を選択します。

1. 設定メニューから「**[!UICONTROL Advanced > Admin]**」を選択し、**[!UICONTROL Unified Experience option]** を展開します。

   ![Experience Cloud統合用の管理ストア設定 ](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable]** の値を選択して、統合を有効または無効にします。

1. **[!UICONTROL Project Name]** 値を追加または更新して、Commerce プロジェクトワークスペースに表示されるプロジェクト名を変更します。

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

   - **Enable**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Disable**—`bin/magento config:set admin/unified_experience/enabled 0`

## 管理者ユーザーアカウントの管理

すべてのCommerce管理者ユーザーがAdobeの製品やサービスにアクセスするには、Commerce インスタンスの管理者アカウントとAdobe ユーザーアカウント（Adobe ID）の両方が必要です。 両方のアカウントが同じメールアドレスに関連付けられている必要があります。

- **Commerce管理者アカウント** - Commerce インスタンスの管理者から [Commerce管理者ユーザーを管理 ](../systems/permissions-users-all.md) します。 Commerce管理者のユーザーアカウントには、管理者ロールが割り当てられている必要があります。

  Commerce プロジェクトのシステム管理者は、[SSH を使用してリモート環境に接続し ](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=ja#connect-to-a-remote-environment)Commerce CLI `admin:user:create` および `admin:user:unlock` コマンドを使用して管理者ユーザーアカウントを追加またはロック解除できます。

- **Adobe ユーザーアカウント** - Commerce インスタンスに関連付けられているAdobe組織用の管理者がAdobe Admin Consoleにログインして、Commerce管理者ごとにAdobe IDを組織に追加する必要があります。 次に、Commerce アプリケーションにアクセスするための製品の使用権限と権限を割り当てる必要があります。 [Adobe Admin ConsoleでAdobe Commerce ユーザーを設定する ](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console) を参照してください。

Adobe Developer ConsoleからExperience Cloud統合の設定を管理する管理者には、システム管理者または開発者アクセス権を持つAdobe ユーザーアカウントが必要です。

>[!NOTE]
>
>Adobe IDは、Experience Cloudを通じて製品やサービスにアクセスするために必要な、Adobeを通じて作成されたアカウントです。 Adobe IDを持っていないCommerce管理者は、Commerce管理者へのログインに使用するのと同じメールアドレスを使用して [ 無料アカウントを作成 ](https://helpx.adobe.com/jp/manage-account/using/create-update-adobe-id.html) できます。
