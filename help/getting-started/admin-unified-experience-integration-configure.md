---
title: コマース管理用のExperience Cloud統合の設定
description: 管理者がアクセスできるように Commerce プロジェクトを設定するExperience Cloudを説明します。
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '1130'
ht-degree: 0%

---

# コマース管理とのExperience Cloud統合の設定

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

コマース管理とのExperience Cloud統合を開始するには、コマース管理の統合エクスペリエンスとコマースイベントの拡張を使用するようにコマースアプリケーションを設定します。


## 前提条件

- Adobe Commerceは、 [Adobe IMS認証](../getting-started/adobe-ims-config.md)
- アカウントのプロビジョニングと権限：管理者は、 [Adobeのビジネスプロファイル](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) を使用して、次のリソースにアクセスし、Experience Cloud統合を設定します。
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html) — 組織のAdobeユーザーおよび開発者アカウントを追加および管理します
   - [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/getting-started/)— App Builder プロジェクトを作成し、接続資格情報と、接続イベントサービスを使用するプロジェクト設定を生成するための開発者またはAdobe I/O管理者アクセス
   - [クラウドインフラストラクチャプロジェクトに関するコマース](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface) — 必要なモジュールをインストールし、Adobe Commerce CLI を使用して Commerce アプリケーションサーバーを設定します
   - [コマース管理者](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html) — ストア設定を更新し、コマースユーザーアカウントを管理します

## 設定の概要

次のタスクを実行して、統合を有効にします。

1. [コマース環境とアプリケーション設定を確認する](#check-the-commerce-environment-and-application-configuration).

1. [コマース管理 Unified Experience 拡張機能を有効にする](#enable-the-commerce-admin-unified-experience-extension).

1. [コマース用のAdobe I/Oイベントの設定](#set-up-adobe-io-events).

1. [統合のテスト](#test-the-integration).

## コマース環境とアプリケーション設定を確認する

Experience Cloud統合を設定する前に、プロジェクトとコマースアプリケーションが要件を満たしていることを確認します。

1. ローカルワークステーションで、コマースプロジェクトのプロジェクトディレクトリに移動します。

1. インスタンスと統合する環境ブランチをExperience Cloudします。

1. Adobe IMSが有効になっていることを確認します。

   - 以下を使用します。 [SSH アクセス URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) （Commerce アプリケーションサーバーに接続するための環境）

   - コマンドラインから、Adobe Commerce CLI を使用して IMS モジュールのステータスを確認します。

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   モジュールが有効でない場合、 [IMS 統合プロジェクトの組織と資格情報を使用して有効にします](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module). 資格情報をお持ちでない場合は、 [Adobeサポートチケットを送信](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

1. 管理者ユーザーが、Adobe IDを使用してコマース管理者にログインできることを確認します。

   - コマース管理 URL に移動します。

   - ログインしている場合は、ログアウトします。

   - 管理者ユーザーが、Adobe IDを使用してログインするようにリダイレクトされていることを確認します。

     ![Adobe Commerce Adobe IDを使用したログイン](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. ローカルワークステーションのクラウドプロジェクトディレクトリから、Commerce Admin Unified Experience 拡張機能がインストールされていることを確認します。

   ```bash
   composer show *unified-experience*
   ```

   拡張機能がインストールされている場合、Composer は拡張機能の名前と説明を返します。

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   拡張機能がインストールされていない場合は、Composer を使用してインストールします。 次に、変更をコミットし、クラウド環境を再デプロイします。

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## コマース管理の統合エクスペリエンスを有効にする

コマース管理 Unified Experience 拡張機能を有効にし、Experience Cloudからログインします。

>[!NOTE]
>
>以下の手順は、Commerce Cloudプロジェクト管理者がAdobe Commerce CLI を使用して拡張機能を有効にする方法を示しています。 コマース管理者ユーザーは、 [コマースストアの設定](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. ローカルワークステーションのクラウドプロジェクト環境のルートディレクトリから、 [magento-cloud CLI ツール](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) をクリックして、Commerce アプリケーションサーバーにログインします。

   ```bash
   magento-cloud ssh
   ```

1. を有効にします。 `magento/module-unified-experience` Adobe Commerce CLI を使用した拡張機能：

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. キャッシュをクリアします。

   ```bash
   bin/magento cache:clean
   ```

## コマース用のAdobe I/Oイベントの設定

Experience Cloudの統合が有効な場合、Adobe I/OイベントサービスはコマースイベントデータをExperience Cloudに送信し、コマースプロジェクトへの管理者アクセスを管理します。 サービスのセットアップでは、コマース用Adobe I/Oイベント拡張機能を有効にする必要があります (`magento/commerce-eventing`) をクリックし、管理でAdobe I/Oイベントサービスを設定します。

### コマースイベントの有効化

コマースイベント拡張機能を有効にする (`magento/commerce-eventing`) をクリックして、コマースアプリケーションからイベントイベントサービスにカスタムAdobe I/Oデータを送信します。

>[!NOTE]
>
>Commerce 2.4.6 以降の場合、 Commerce Events 拡張機能はデフォルトでインストールされます。 Commerce 2.4.5 を使用するコマースプロジェクトの場合、最初に Composer を使用して、 [拡張機能のインストール](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)をクリックし、有効にします。

1. ローカルの Commerce プロジェクト開発環境から、次の設定を `.magento.env.yaml` ファイル。

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. 更新された `.magento.env.yaml file` クラウド環境に追加します。

>[!TIP]
>
>を使用した環境変数の設定と管理の詳細 `.magento.env.yaml` ファイル： [デプロイメント用の環境変数の設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### コマースイベント統合の設定

次のタスクを実行して、コマースイベント統合を設定します。 詳しい手順については、 [コマースのAdobe I/Oイベント](https://developer.adobe.com/commerce/extensibility/events/project-setup/) 開発者向けドキュメント。

1. [App Builder プロジェクトの作成](https://developer.adobe.com/commerce/extensibility/events/project-setup/) をクリックして、Commerce インスタンスからイベントデータを受け取ります。

   コマース管理で統合を設定するには、App Builder プロジェクトの資格情報と設定データが必要です。

1. Adobe Commerceを設定してイベントイベントを使用します。Adobe I/O

   - [Store Events サービスのストア設定を更新するAdobe I/O](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [コマースイベントを送信するためのイベントプロバイダーの設定](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [コマースインスタンスからイベントデータを受け取るように App Builder プロジェクトを更新します](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   コマースインスタンスからイベントを登録または購読しないでください。 コマースアプリケーションのイベントプロバイダーを設定すると、イベント登録が App Builder プロジェクトにプッシュされます。

   イベントプロバイダーを App Builder プロジェクトに接続したら、 `observer.uex_commerce_instance_update` イベントを開き、変更を保存します。

1. 接続を確立するには、イベントプロバイダーを通じて消費者にイベントを送信します。

   - ローカルクラウドプロジェクトディレクトリのコマンドラインから、 [SSH を使用して Commerce アプリケーションサーバーに接続する](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Adobe Commerce CLI を使用して Admin Unified Experience 拡張機能のステータスを確認し、イベントデータを送信します。

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### 統合のテスト

コマース管理者がExperience Cloudにログインして、使用可能な Commerce プロジェクトを表示し、各プロジェクトの管理者とストアフロントにアクセスできることを確認します。

1. [ログインしてExperience Cloud](https://experiencecloud.adobe.com/library) コマースインスタンスに関連付けられたAdobe IDと組織を使用する。

   ![「Experience Cloud」ホームページからの Commerce プロジェクトへのアクセス](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. 選択して利用可能なコマースプロジェクトを表示 **[!UICONTROL Commerce]**.

   ![Experience Cloud用の Commerce Projects ワークスペース](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. 「 」を選択して、インスタンスの管理者を開きます。 **[!UICONTROL Open]**.

   ![コマース統合が有効なコマース管理者Experience Cloud](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. 管理者タスクが期待どおりに実行できることを確認します。

   コマース管理のワークフローも同じ手順に従う必要があります。 ワークフロー統合を有効にした後にExperience Cloudの変更やエラーが発生した場合は、コマースシステム管理者に問い合わせてください。 [Adobeサポートチケットを送信](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Experience Cloud統合を設定したら、Experience Cloudを通じて Commerce プロジェクトにアクセスするために管理者アカウントが正しくプロビジョニングされていることを確認します。 詳しくは、 [管理者ユーザーの管理](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
