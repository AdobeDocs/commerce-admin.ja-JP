---
title: ログイン資格情報と URL
description: 管理者とストアフロントへのアクセス権を取得するために使用されるコマース URL とアカウント資格情報について説明します。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# ログイン資格情報と URL

セットアップと設定を進める前に、ストアの管理者とコマースアカウントへのアクセスに必要な情報があることを確認してください。

## ストアフロント URL

お使いの [店頭の](storefront.md) は、通常、IP アドレスに割り当てられるドメインです。 一部のストアは、ルートまたは最上位のディレクトリにインストールされます。 その他は、ルートの下のディレクトリにインストールされます。 ストアは、プライマリドメインに関連付けられたサブドメイン内に存在する場合があります。 ストアの URL は、次のようになります。

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

ドメインがまだない場合、ストア URL には 4 つの数字のシリーズが含まれ、それぞれが _点付き四角形_ 表記法。

## 管理 URL

ストアのアドレス [管理者](admin.md) は、インストール時に設定されます。 デフォルトのアドレスはストアと同じですが、 `/admin` 最後に このガイドの例ではデフォルトのディレクトリを使用していますが、ベストプラクティスは、ストアに固有の場所から管理者を実行することです。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] アカウント

お使いの [コマースアカウント](commerce-account-create.md) では、製品やサービス、アカウント設定、請求履歴、サポートリソースに関する情報にアクセスできます。 アカウントにアクセスするには、メインのコマースサイトに移動し、 **[!UICONTROL My Account]** をクリックします。

## 顧客アカウント

ストアの操作方法を学習する際は、必ずテストを設定してください [顧客アカウント](../customers/account-dashboard.md)を使用すると、顧客の視点でストアやチェックアウトプロセスを体験できます。

## サンプルデータ

Adobeには、250 を超える製品（そのうち約 200 は設定可能な製品）、カテゴリ、プロモーション価格ルール、CMS ページ、バナーなどを含むサンプルストアを含むサンプルデータセットが用意されています。 サンプルデータは _Luma_ ストアフロントのテーマ。 [このサンプルデータのインストール](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) はオプションですが、e コマースビジネス向けのカスタマイズのテストや開発に役立ちます。
