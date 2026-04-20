---
title: Adobe Identity Management Service （IMS）の統合の概要
description: Adobe Commerce管理者ログインとAdobe IMSのオプション統合について説明します
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: 837da039e03db94014056fbb4e945c47fa37b7c1
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Adobe Identity Management Service （IMS）の統合の概要

{{ee-feature}}

Adobe アカウントを持つAdobe Commerce管理者ユーザーは、Adobe IDを使用してAdobe Commerceにログインできるようになりました。 Adobe Identity Management サービス（IMS）は、認証をサポートするAdobeのOAuth 2.0 ベースのID管理機能です。 Commerce管理者認証をAdobe Business製品のIMS認証ワークフローに統合すると、他のAdobe製品と連携するユーザーの認証プロセスを効率化できます。 この統合はオプションで、インスタンスごとに有効になります。 この統合が有効になっている場合は、管理者ユーザーワークフローのみが影響を受けます。 

Commerce Admin IMS統合に必要なモジュールは`adobe-ims-metapackage`にパッケージ化されており、Adobe Commerce コアリリースにバンドルされています。

この統合を実装するには、[Commerce Admin IntegrationとIMS](./adobe-ims-config.md)の設定を参照してください。

## IMSとの統合後の管理者ワークフローとインターフェイスの変更

この統合が有効になっている場合、Commerce管理者ユーザーは、管理者ユーザーの作成など、再認証を必要とする日常的なタスクを管理者で実行する際に、デフォルトのCommerce管理者ログインと認証ワークフローに変更されます。 モジュールイネーブルメントには、Adobe組織レベルでの2要素認証（2FA）の実施が必要です。 デフォルトの管理者ログインと2FAは無効になっており、デフォルトの管理者ログインのフォームは&#x200B;_[!UICONTROL Sign In with Adobe ID]_ボタンに置き換えられます。 使用権限は、引き続き管理者から管理されます。

>[!IMPORTANT]
>
>AdobeIms統合はグローバルに適用されています。 有効にすると、すべてのユーザーがAdobeImsを通じて認証する必要があります。個々のユーザーをこの設定から除外することはできません。
>
>**この統合を有効にするには、その影響を完全に理解する必要があります。**

## IMSとの管理者の統合がCommerce パスワードに与える影響

Adobe IMSと統合されたCommerceのデプロイメントには、IMS有効化プロセス中にAdobe ID アプリケーション用に設定されたAdobe IMS組織へのアクセス権を持つCommerce アカウントが必要です。  IMS統合が有効になっている場合、管理者ユーザーは、Adobeの資格情報を使用してAdobe ログインページを通じて認証を行います。 管理者ユーザーのCommerce パスワードとユーザー名は、Adobe IMS統合が有効になっている限り、認証に使用されなくなります。

IMS統合が無効になっている場合、管理者ユーザーはCommerceのユーザー名とパスワードを使用して、Adobe Commerceを通じて再度認証する必要があります。 管理者ユーザーは、この統合を有効にする前に、Commerce管理者の資格情報（ユーザー名とパスワード）と2FAの資格情報を保存する必要があります。

ユーザー認証に関連する一部のバックエンドコンポーネントでは、null以外のパスワードが引き続き必要です。 この要件を満たすために、Commerceは新しく作成された管理者ユーザーに対して、`admin_user` テーブルにランダムなパスワードを作成します。

Commerce アプリケーションのユーザーアカウントとロール権限は、引き続きCommerce管理者から管理されます。


## IMS資格情報を使用したWeb API トークンの生成

Commerce Admin APIは、Commerce インスタンスでAdobe IMSを使用した管理者認証が有効になっている場合に影響を受けます。 管理者ユーザーは、Commerce インスタンスによって発行された資格情報を使用できなくなりました。 これらは、管理者にログインし、サービスがAdmin REST APIとSOAP APIにリクエストを行うために使用できるアクセストークンを取得するために必要な資格情報です。

Adobe IMS統合が有効になったら、認証が必要なAdobe Commerce API エンドポイントに対して、管理者ユーザーは[Adobe IMS OAuth トークン ](https://developer.adobe.com/developer-console/docs/guides/authentication/)を使用する必要があります。 クライアントソリューションは、web API使用のためにトークンを動的に取得します。 この認証メカニズムは、この統合の設定の一環として、RESTおよびSOAP web API領域で有効になっています。

IMS アクセストークンを含むweb APIでのCommerce アクセストークンの使用方法の概要については、[ トークンベースの認証](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/)を参照してください。

## Commerceのセッション管理およびAdobe IMSアクセストークン

アクセストークンには、ユーザーの資格情報とログインセッション情報の両方が保持されます。 ユーザーが認証され、セッションが開始されると、次の2つの変数がユーザーのセッションに追加されます。

`token_last_check_time`。 現在の時間を識別し、`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインで使用されます。

`adobe_access_token` – 承認中に受信した`ACCESS_TOKEN`値を識別します。

`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインは、`token_last_check_time`が10分前に更新されたかどうかを確認します。 `token_last_check_time`が10分前にチェックされた場合、認証ワークフローはIMSにAPI呼び出しを行ってアクセストークンを検証し、セッションを続行します。 アクセストークンが有効な場合、`token_last_check_time`値は現在の時刻に更新されます。 トークンが無効な場合、セッションは終了します。

## 重要なファイル

`adminAdobeIms` - `AdobeImsApi` モジュールに基づく管理者ログインの実装を提供します。

`admin_adobe_ims_webapi` – 検証されたすべてのアクセストークンのレコードを保持します。 トークンが検証または無効化されると、そのステータスのレコードがこのテーブルに保存されます。

`adobeIms` - Adobe IMSとの統合に関連するすべてのビジネス ロジックを実装します（後方互換性を維持するために保持されます）。

`adobeImsApi` - Adobe IMSとの統合をサポートするインターフェイスを宣言します。

`adminadobe-ims.log` - エラーログファイル。

## 統合を有効にする

Adobe IMSメタパッケージは、Adobe Commerce 2.4.5以降でインストールされますが、使用できるように設定する必要があります。 `AdobeIms` モジュールを拡張して、認証ロジック （`AdminAdobeIms`）を有効にするモジュールをサポートします。

統合を有効にする方法について詳しくは、[Adobe IMSとのCommerce管理者統合の設定](./adobe-ims-config.md)を参照してください。
