---
title: ログイン資格情報と URL
description: 管理者およびストアフロントへのアクセス権を取得するために使用する、Commerceの URL とアカウント資格情報について説明します。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# ログイン資格情報と URL

セットアップと設定を進める前に、ストアの管理者とCommerce アカウントにアクセスするために必要な情報があることを確認してください。

## ストアフロント URL

のアドレス [ストアフロント](storefront.md) は、通常、IP アドレスに割り当てられているドメインです。 一部のストアは、ルートまたは最上位ディレクトリにインストールされています。 その他は、ルートの下のディレクトリにインストールされます。 ストアは、プライマリドメインに関連付けられたサブドメイン内に存在する場合があります。 ストアの URL は、次のいずれかのようになります。

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`秒

ドメインがまだない場合、ストア URL には一連の 4 つの数値が含まれ、それぞれをピリオドで区切ります。 _点線の四角形_ 表記。

## 管理者 URL

ストアのアドレス [Admin](admin.md) はインストール時に設定されます。 デフォルトのアドレスはストアと同じですが、 `/admin` 最後です。 このガイドの例ではデフォルトのディレクトリを使用していますが、ストアに固有の場所から管理者を実行するのがベストプラクティスです。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] アカウント

あなたの [Commerce アカウント](commerce-account-create.md) では、製品とサービス、アカウント設定、請求履歴、サポートリソースに関する情報にアクセスできます。 アカウントにアクセスするには、メインのCommerce サイトに移動し、 **[!UICONTROL My Account]** 右上隅

## 顧客アカウント

お店の周りを学んでいる間、必ずテストを設定してください [顧客アカウント](../customers/account-dashboard.md)を使用すれば、ストアとチェックアウトのプロセスを顧客の観点から体験できます。

## サンプルデータ

Adobeは、250 個を超える商品（そのうち約 200 個は設定可能な商品）、カテゴリ、プロモーションの価格ルール、CMS ページ、バナーなどを含むサンプルストアを含むサンプルデータセットを提供しています。 サンプルデータでは次を使用します _Luma_ ストアフロントのテーマ。 [このサンプルデータのインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) はオプションですが、e コマースビジネスのカスタマイズのテストと開発に役立ちます。
