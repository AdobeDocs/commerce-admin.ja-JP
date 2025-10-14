---
title: ログイン資格情報と URL
description: 管理者およびストアフロントへのアクセス権を取得するために使用する、Commerceの URL とアカウント資格情報について説明します。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# ログイン資格情報と URL

セットアップと設定を進める前に、ストアの管理者とCommerce アカウントにアクセスするために必要な情報があることを確認してください。

## ストアフロント URL

[&#x200B; ストアフロント &#x200B;](storefront.md) のアドレスは、通常、IP アドレスに割り当てられているドメインです。 一部のストアは、ルートまたは最上位ディレクトリにインストールされています。 その他は、ルートの下のディレクトリにインストールされます。 ストアは、プライマリドメインに関連付けられたサブドメイン内に存在する場合があります。 ストアの URL は、次のいずれかのようになります。

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx` 秒

ドメインがまだない場合、ストア URL には 4 つの数字のシリーズが含まれ、それぞれが _ドット付き四角形_ 表記でピリオドで区切られています。

## 管理者 URL

ストア [&#x200B; 管理者 &#x200B;](admin.md) のアドレスは、インストール時に設定されます。 デフォルトのアドレスはストアと同じですが、末尾には `/admin` が付きます。 このガイドの例ではデフォルトのディレクトリを使用していますが、ストアに固有の場所から管理者を実行するのがベストプラクティスです。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] アカウント

[Commerce アカウント &#x200B;](commerce-account-create.md) を使用すると、商品とサービス、アカウント設定、請求履歴、サポートリソースに関する情報にアクセスできます。 アカウントにアクセスするには、メインのCommerce サイトに移動し、右上隅の「**[!UICONTROL My Account]**」をクリックします。

## 顧客アカウント

店舗の様々な方法を学習している間は、テスト [&#x200B; 顧客アカウント &#x200B;](../customers/account-dashboard.md) を設定して、顧客の観点から店舗とチェックアウトのプロセスを体験してください。

## サンプルデータ

[!BADGE PaaS のみ &#x200B;]{type=Informative url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeが管理する PaaS インフラストラクチャ）およびオンプレミスプロジェクトにのみ適用されます。"}

Adobeは、250 個を超える商品（そのうち約 200 個は設定可能な商品）、カテゴリ、プロモーションの価格ルール、CMSページ、バナーなどを含むサンプルストアを含むサンプルデータセットを提供します。 サンプルデータでは、ストアフロントの _Luma_ テーマを使用しています。 [&#x200B; このサンプルデータのインストール &#x200B;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=ja) はオプションですが、e コマースビジネスのカスタマイズのテストと開発に役立ちます。
