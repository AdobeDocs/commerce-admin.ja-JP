---
title: Adobe Identity Management Service （IMS）統合の概要
description: Adobe Commerce管理者ログインとAdobe IMSのオプション統合を導入します
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="PaaS のみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Adobe Identity Management Service （IMS）統合の概要

{{ee-feature}}

Adobe Commerce アカウントを持つAdobe管理者ユーザーは、Adobe IDを使用してAdobe Commerceにログインできるようになりました。 Adobe Identity Management Service （IMS）は、認証をサポートする、Adobeの OAuth 2.0 ベースの ID 管理機能です。 Commerce Admin Authentication をAdobe Business Product の IMS 認証ワークフローに統合すると、他のAdobe製品を使用するユーザーの認証プロセスを合理化できます。 この統合はオプションで、インスタンスごとに有効になります。 この統合が有効な場合、管理ユーザーワークフローのみが影響を受けます。 

Commerce管理 IMS 統合に必要なモジュールは、Adobe Commerce コアリリースにバンドルされている `adobe-ims-metapackage` にパッケージ化されています。

この統合を実装するには、[IMS を使用したCommerce管理者の統合の設定 &#x200B;](./adobe-ims-config.md) を参照してください。

## IMS との統合後の管理ワークフローおよびインターフェイスの変更

この統合が有効になっていると、Commerce管理者ユーザーは、管理者ユーザーの作成など、再認証が必要なルーチンのタスクを管理者で実行する際に、デフォルトのCommerce Admin ログインおよび認証ワークフローに変更が生じます。 モジュールイネーブルメントには、Adobe組織レベルで二要素認証（2FA）が強化される必要があります。 デフォルトの管理者ログインと 2FA は無効になっており、デフォルトの管理者ログインフォームの代わりに「_[!UICONTROL Sign In with Adobe ID]_」ボタンが表示されます。 使用権限は引き続き管理者から管理されます。

## 管理者と IMS の統合によるCommerceのパスワードへの影響

Adobe IMSと統合されたCommerceのデプロイメントでは、IMS 有効化プロセス中にAdobe ID アプリケーション用に設定されたAdobe IMS組織にアクセスできるCommerce アカウントが必要です。  IMS 統合が有効な場合、管理者ユーザーは、Adobeのログインページを使用して、Adobe資格情報を使用して認証を行います。 Adobe IMS統合が有効になっている限り、管理者ユーザーのCommerce パスワードとユーザー名は認証に使用されなくなりました。

IMS 統合が無効な場合、管理者ユーザーは、Commerceのユーザー名とパスワードを使用して、Adobe Commerceを通じて再認証する必要があります。 管理者ユーザーは、この統合を有効にする前に、Commerce管理者資格情報（ユーザー名とパスワード）と 2FA 資格情報を保存する必要があります。

ユーザー認証に関与する特定のバックエンドコンポーネントには、引き続き null 以外のパスワードが必要です。 この要件を満たすために、Commerceは、新しく作成された管理者ユーザー用のランダムパスワードを `admin_user` テーブルに作成します。

Commerce アプリケーションのユーザーアカウントとロール権限は、引き続きCommerce管理者から管理されます。


## IMS 資格情報を使用した web API トークンの生成

Commerce インスタンスでAdobe IMSによる管理者認証が有効になっている場合、Commerce管理 API は影響を受けます。 管理者ユーザーは、Commerce インスタンスが発行した資格情報を使用できなくなります。 これらは、管理者にログインし、サービスが管理者の REST API およびSOAP API にリクエストを行うために使用できるアクセストークンを取得するために必要な資格情報です。

Adobe IMS統合が有効になると、管理者ユーザーは、認証を必要とするAdobe Commerce API エンドポイントに対して [0&rbrace;Adobe IMS OAuth トークン &rbrace; を使用する必要があります。](https://developer.adobe.com/developer-console/docs/guides/authentication/) クライアントソリューションは、web API で使用するためにトークンを動的に取得します。 この認証メカニズムは、この統合の設定の一環として、REST およびSOAP Web API 領域に対して有効になっています。

Web API でのCommerce アクセストークンの使用方法（IMS アクセストークンを含む）の概要については、[&#x200B; トークンベースの認証 &#x200B;](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) を参照してください。

## Commerce セッション管理およびAdobe IMSアクセストークン

アクセストークンには、ユーザー資格情報とログインセッション情報の両方が格納されます。 ユーザーが認証され、セッションが開始されると、次の 2 つの変数がユーザーのセッションに追加されます。

`token_last_check_time`。 現在の時刻を識別し、`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインで使用されます。

`adobe_access_token` – 認証中に受け取った `ACCESS_TOKEN` 値を識別します。

`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` プラグインは、`token_last_check_time` が 10 分前に更新されたかどうかを確認します。 10 分前に `token_last_check_time` がチェックされた場合、認証ワークフローは IMS への API 呼び出しを行い、アクセストークンを検証して、セッションを続行します。 アクセストークンが有効な場合、`token_last_check_time` 値は現在の時刻に更新されます。 トークンが無効な場合、セッションは終了します。

## 重要なファイル

`adminAdobeIms` - `AdobeImsApi` モジュールに基づく Admin ログインの実装を提供します。

`admin_adobe_ims_webapi` – 検証済みのすべてのアクセストークンの記録を保持します。 トークンが検証または無効化されると、そのステータスの記録がこの表に保持されます。

`adobeIms` - Adobe IMSとの統合に関連するすべてのビジネスロジックを実装します（後方非互換性を防ぐために保持されます）。

`adobeImsApi` - Adobe IMSとの統合をサポートするインターフェイスを宣言します。

`adminadobe-ims.log` - エラーログファイル。

## 統合の有効化

Adobe IMSメタパッケージは、Adobe Commerce 2.4.5 以降でインストールされますが、使用するように設定する必要があります。 `AdobeIms` モジュールを拡張して、認証ロジック（`AdminAdobeIms`）を有効にするモジュールをサポートします。

Adobe IMSの有効化について詳しくは、[&#x200B; 統合を使用したCommerce Admin 統合の設定 &#x200B;](./adobe-ims-config.md) を参照してください。
