---
title: ログイン情報とURL
description: 管理者およびストアフロントへのアクセス権を取得するために使用されるCommerceのURLとアカウント認証情報について説明します。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/8IGacP581jwpVtFnCFXRrG5vuIwCJaAUnbliitMHuf8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: d41d3a54-9721-475c-abd6-295bebfba9e4
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 0%

---

# ログイン情報とURL

設定と設定を進める前に、ストアの管理者とCommerce アカウントにアクセスするために必要な情報があることを確認してください。

## ストアフロント URL

[ ストアフロント ](storefront.md)のアドレスは、通常、IP アドレスに割り当てられたドメインです。 一部のストアは、ルートまたは最上位のディレクトリにインストールされます。 その他は、ルートの下のディレクトリにインストールされます。 ストアは、プライマリドメインに関連付けられたサブドメイン内に存在する場合があります。 ストアのURLは次のようになります。

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

まだドメインがない場合、ストア URLには4つの数字が含まれ、それぞれ&#x200B;_点線_&#x200B;の表記法で区切られます。

## 管理者URL

ストア [管理者](admin.md)のアドレスは、インストール中に設定されます。 デフォルトのアドレスはストアと同じですが、最後に`/admin`があります。 このガイドの例ではデフォルトのディレクトリを使用していますが、ストアに固有の場所から管理者を実行することをお勧めします。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] アカウント

お客様の[Commerce アカウント ](commerce-account-create.md)は、お客様の製品やサービス、アカウント設定、請求履歴、サポート リソースに関する情報にアクセスできます。 アカウントにアクセスするには、メインのCommerce サイトに移動し、右上隅の「**[!UICONTROL My Account]**」をクリックします。

## 顧客アカウント

ストアでの使用方法を学習する際は、必ずテスト [顧客アカウント ](../customers/account-dashboard.md)を設定して、お客様の視点からストアとチェックアウトのプロセスを体験できるようにしてください。

## サンプルデータ

[!BADGE PaaSのみ]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"}

Adobeでは、250以上の製品（そのうちの約200は設定可能な製品）、カテゴリ、プロモーション価格ルール、CMS ページ、バナーなどのサンプルストアを含むサンプルデータセットを提供しています。 サンプルデータは、ストアフロントで&#x200B;_Luma_ テーマを使用します。 [このサンプルデータのインストール ](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html)はオプションですが、コマースビジネスのカスタマイズをテストおよび開発する場合に役立ちます。
