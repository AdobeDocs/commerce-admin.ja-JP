---
title: AdobeIdentity Managementサービス (IMS) 統合の概要
description: Adobe Commerce Admin ログインとAdobe IMSのオプションの統合を紹介します
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# AdobeIdentity Managementサービス (IMS) 統合の概要

{{ee-feature}}

Adobe Commerceアカウントを持つAdobe管理者ユーザーは、Adobe IDを使用してAdobe Commerceにログインできるようになりました。 AdobeIdentity Managementサービス (IMS) は、Adobeの認証をサポートする OAuth 2.0 ベースの ID 管理機能です。 コマース管理者認証をAdobeビジネス製品の IMS 認証ワークフローに統合すると、他のAdobe製品と連携するユーザーの認証プロセスを合理化できます。 この統合はオプションで、インスタンスごとに有効になります。 この統合が有効になっている場合、管理者ユーザーワークフローのみが影響を受けます。 

コマース管理 IMS 統合に必要なモジュールは、次の場所にパッケージ化されています。  `adobe-ims-metapackage`:Adobe Commerce Core リリースにバンドルされています。

この統合の実装については、 [IMS とのコマース管理者統合の設定](./adobe-ims-config.md).

## IMS との統合後の管理ワークフローおよびインターフェイスに対する変更

この統合を有効にすると、Commerce Admin ユーザーは、管理者ユーザーの作成など、再認証が必要な管理者でのルーチンタスクを実行する際に、デフォルトの Commerce Admin ログインおよび認証ワークフローに変更されます。 モジュールのイネーブルメントには、Adobe組織レベルでの二段階認証 (2FA) の実施が必要です。 デフォルトの管理者ログインと 2FA が無効で、 _[!UICONTROL Sign In with Adobe ID]_ボタンは、デフォルトの管理者ログインフォームに代わるものです。 使用権限は引き続き管理者から管理されます。

## IMS との管理者の統合がコマースパスワードに与える影響

Adobe IMSと統合されたコマースデプロイメントには、IMS イネーブルメントプロセス中に CommerceAdobe IMS用に設定されたアプリケーション組織にアクセスできるAdobe IDアカウントが必要です。  IMS 統合が有効になっている場合、管理者ユーザーは、Adobeのログインページで、自分のAdobe資格情報を使用して認証をおこないます。 管理者ユーザーのコマースパスワードとユーザー名は、パスワードの統合が有効になっている限り、Adobe IMSに使用されなくなりました。

IMS 統合が無効になっている場合、管理者ユーザーは、コマースユーザー名とパスワードを使用して、Adobe Commerceを通じて再度認証する必要があります。 この統合を有効にする前に、管理者ユーザーは、コマース管理者の資格情報（ユーザー名とパスワード）と 2FA の資格情報を保存する必要があります。

ユーザー認証に関係するバックエンドコンポーネントには、null 以外のパスワードが引き続き必要となる場合があります。 この要件を満たすために、Commerce は、新しく作成された管理者ユーザーのランダムなパスワードを `admin_user` 表。

コマースアプリケーションのユーザーアカウントとロールの権限は、引き続きコマース管理者から管理されます。


## IMS 資格情報を使用した Web API トークンの生成

コマースインスタンスでAdobe IMSを使用した管理者認証が有効になっている場合、コマース管理 API は影響を受けます。 管理者ユーザーは、コマースインスタンスが発行した資格情報を使用できなくなりました。 これらは、管理者にログインし、管理 REST および SOAP API に対する要求をおこなう際にサービスが使用できるアクセストークンを取得するために必要な資格情報です。

Adobe IMSの統合を有効にした後、管理者ユーザーは [Adobe IMSOAuth トークン](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) ( 認証が必要なAdobe Commerce API エンドポイント用 ) クライアントソリューションは、Web API で使用するトークンを動的に取得します。 この認証メカニズムは、この統合の設定の一環として REST および SOAP Web API 領域で有効になります。

詳しくは、 [トークンベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) を参照してください。

## コマースセッション管理およびAdobe IMSアクセストークン

アクセストークンには、ユーザー資格情報とログインセッション情報の両方が保持されます。 ユーザーが認証され、セッションが開始されると、次の 2 つの変数がユーザーのセッションに追加されます。

`token_last_check_time`. 現在の時刻を識別し、 `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインです。

`adobe_access_token`  — を識別します。 `ACCESS_TOKEN` 認証中に受け取った値。

The `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインは、 `token_last_check_time` は 10 分前に更新されました。 次の場合、 `token_last_check_time` が 10 分前にチェックされた場合、認証ワークフローは IMS への API 呼び出しをおこなってアクセストークンを検証し、セッションは続行します。 アクセストークンが有効な場合、 `token_last_check_time` の値が現在の時刻に更新されます。 トークンが有効でない場合、セッションは終了します。

## 重要なファイル

`adminAdobeIms` - `AdobeImsApi` モジュール。

`admin_adobe_ims_webapi`  — 検証済みのすべてのアクセストークンのレコードを維持します。 トークンが検証または無効化されると、そのステータスのレコードがこの表に保持されます。

`adobeIms` -Adobe IMSとの統合に関連するすべてのビジネスロジックを実装します（後方互換性の低下を防ぐために保持されます）。

`adobeImsApi`  — 統合との統合をサポートするインターフェイスをAdobe IMSします。

`adminadobe-ims.log`  — エラーログファイル。

## 統合の有効化

Adobe IMSメタパッケージは、Adobe Commerce 2.4.5 以降と共にインストールされますが、使用するように設定する必要があります。 これは、 `AdobeIms` 認証ロジックを有効にするモジュールをサポートするモジュール (`AdminAdobeIms`) をクリックします。

統合の有効化について詳しくは、 [コマース管理者と統合のAdobe IMS](./adobe-ims-config.md).
