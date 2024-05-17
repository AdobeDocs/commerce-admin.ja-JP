---
title: Commerce Admin 用のExperience Cloud統合の設定
description: Commerce プロジェクトをExperience Cloudして、管理者アクセスを有効にする方法を説明します。
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# Commerce Admin とのExperience Cloud統合の設定

Commerce Admin の統合エクスペリエンスおよびCommerce Events 拡張機能を使用するようにCommerce Experience Cloudを設定して、Commerce Admin とのアプリケーション統合を開始します。


## 前提条件

- を使用するようにAdobe Commerceを設定する必要があります [Adobe IMS認証](../getting-started/adobe-ims-config.md)
- アカウントのプロビジョニングと権限：管理者は、 [Adobeのビジネスプロファイル](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) 以下のリソースにアクセスして、Experience Cloud統合を設定できます。
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html) – 組織のAdobeユーザーおよび開発者アカウントを追加および管理します
   - [Adobe Developer コンソール](https://developer.adobe.com/developer-console/docs/guides/getting-started/)- App Builder プロジェクトを作成し、Adobe I/Oイベントサービスを使用するための接続資格情報とプロジェクト設定を生成するための開発者またはシステム管理者アクセス権
   - [クラウドインフラストラクチャー上のCommerce プロジェクト](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface) – 必要なモジュールをインストールし、Adobe Commerce CLI を使用してCommerce アプリケーションサーバーを設定します
   - [Commerce管理者](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html) – ストア設定を更新し、Commerce ユーザーアカウントを管理します。

## 設定の概要

統合を有効にするには、次のタスクを実行します。

1. [Commerce環境とアプリケーション設定の確認](#check-the-commerce-environment-and-application-configuration).

1. [Commerce Admin Unified Experience 拡張機能の有効化](#enable-the-commerce-admin-unified-experience-extension).

1. [Commerce用のAdobe I/Oイベントの設定](#set-up-adobe-io-events).

1. [統合のテスト](#test-the-integration).

## Commerce環境とアプリケーション設定の確認

Experience Cloudの統合を設定する前に、プロジェクトとCommerce アプリケーションが要件を満たしていることを確認します。

1. ローカルワークステーションで、Commerce プロジェクトのプロジェクトディレクトリに移動します。

1. Experience Cloudと統合するインスタンスの環境ブランチをチェックアウトします。

1. Adobe IMSが有効になっていることを確認します。

   - の使用 [SSH アクセス URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) Commerce アプリケーションサーバーに接続します。

   - コマンドラインから、Adobe Commerce CLI を使用して、IMS モジュールのステータスを確認します。

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   モジュールが有効になっていない場合、 [ims 統合プロジェクトの組織と資格情報を使用して有効にします](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. 管理者ユーザーがAdobe IDを使用してCommerce管理者にログインできることを確認します。

   - Commerceの管理者 URL に移動します。

   - ログインしている場合は、ログアウトします。

   - 管理者ユーザーがAdobe IDを使用してログインするためにリダイレクトされていることを確認します。

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

## Commerce Admin Unified Experience を有効にする

Commerce Admin Unified Experience 拡張機能を有効にしてから、Experience Cloudを通じてログインします。

>[!NOTE]
>
>これらの手順は、Commerce Cloudプロジェクト管理者がAdobe Commerce CLI を使用して拡張機能を有効にする方法を示しています。 Commerce管理者ユーザーは、 [Commerce ストアの設定](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. ローカルワークステーションのクラウドプロジェクト環境のルートディレクトリから、を使用します [magento-cloud CLI ツール](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) Commerce アプリケーションサーバーにログインします。

   ```bash
   magento-cloud ssh
   ```

1. を有効にする `magento/module-unified-experience` Adobe Commerce CLI を使用した拡張機能：

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. キャッシュをクリアします。

   ```bash
   bin/magento cache:clean
   ```

## Commerce用のAdobe I/Oイベントの設定

Experience Cloud統合が有効な場合、Commerce プロジェクトへの管理者アクセスを管理するために、Adobe I/OイベントサービスはCommerce イベントデータをExperience Cloudに送信します。 サービスを設定するには、Commerce拡張機能のAdobe I/Oイベント （`magento/commerce-eventing`）を選択して、Admin でAdobe I/Oイベントサービスを設定します。

### Commerce イベントを有効にする

Commerce イベント拡張機能を有効にします（`magento/commerce-eventing`）を選択して、Commerce アプリケーションからAdobe I/Oイベントサービスにカスタムイベントデータを送信します。

>[!NOTE]
>
>Commerce 2.4.6 以降では、Commerce Events 拡張機能がデフォルトでインストールされます。 Commerce 2.4.5 を使用するCommerce プロジェクトの場合、まず Composer を使用して以下を行います [拡張機能のインストール](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)を選択してから、有効にします。

1. ローカルのCommerce プロジェクト開発環境から、次の設定をに追加します。 `.magento.env.yaml` ファイル。

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

1. 更新されたを追加、コミット、デプロイします。 `.magento.env.yaml file` をクラウド環境に追加します。

>[!TIP]
>
>を使用した環境変数の設定および管理について詳しくは、 `.magento.env.yaml` ファイル、を参照 [デプロイメント用の環境変数の設定](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Commerce イベント統合の設定

次のタスクを実行して、Commerce イベントの統合を設定します。 手順について詳しくは、 [CommerceのAdobe I/Oイベント](https://developer.adobe.com/commerce/extensibility/events/project-setup/) 開発者向けドキュメント。

1. [App Builder プロジェクトの作成](https://developer.adobe.com/commerce/extensibility/events/project-setup/) Commerce インスタンスからイベントデータを受け取る。

   Commerce管理者で統合を設定するには、App Builder プロジェクトの資格情報と設定データが必要です。

1. Adobe I/Oイベントを使用するようにAdobe Commerceを設定します。

   - [Adobe I/Oイベントサービスのストア設定の更新](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [Commerce イベントを送信するイベントプロバイダーの設定](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [App Builder プロジェクトを更新して、Commerce インスタンスからイベントデータを受け取ります](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Commerce インスタンスからイベントを登録または登録しないでください。 Commerce アプリケーションのイベントプロバイダーを設定すると、イベント登録が App Builder プロジェクトにプッシュされます。

   イベントプロバイダーを App Builder プロジェクトに接続したら、を購読します `observer.uex_commerce_instance_update` をイベントして、変更を保存します。

1. 接続を確立するには、イベント プロバイダーを通じて消費者にイベントを送信します。

   - ローカルクラウドプロジェクトディレクトリのコマンドラインから、 [ssh を使用してCommerce アプリケーションサーバーに接続します](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Adobe Commerce CLI を使用して、管理 Unified Experience 拡張機能のステータスを確認することで、イベントデータを送信します。

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### 統合のテスト

Commerce管理者がExperience Cloudにログインして使用可能なCommerce プロジェクトを表示し、各プロジェクトの管理者およびストアフロントにアクセスできることを確認します。

1. [Experience Cloudにサインイン](https://experiencecloud.adobe.com/library) Commerce インスタンスに関連付けられたAdobe IDと組織を使用します。

   ![Experience CloudホームページからCommerce プロジェクトへのアクセス](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. 次を選択して、使用可能なCommerce プロジェクトを表示します **[!UICONTROL Commerce]**.

   ![Experience Cloud用のCommerce プロジェクトワークスペース](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. 次を選択して、インスタンスの管理者を開きます。 **[!UICONTROL Open]**.

   ![Experience Cloud統合が有効になっているCommerce管理者ビュー](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. 管理者タスクを期待どおりに実行できることを確認します。

   Commerce管理者のワークフローも、同じプロセスに従う必要があります。 ワークフロー統合を有効にした後にExperience Cloudの変更やエラーが発生した場合は、Commerce システム管理者または [Adobeサポートチケットを送信](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

AdministratorExperience Cloudを設定したら、統合を通じてCommerce プロジェクトにアクセスできるようにExperience Cloudアカウントが正しくプロビジョニングされていることを確認します。 参照： [管理者ユーザーの管理](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
