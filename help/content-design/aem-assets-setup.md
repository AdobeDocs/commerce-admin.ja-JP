---
title: AEM Assets統合の設定
description: Adobe CommerceとAEM Assetsas a Cloud Serviceの間の統合を設定するための要件と手順について説明します。
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# AEM Assets統合の設定

AEM Assets環境を設定し、AEM Assets integration for Commerceをインストールして設定することで、高度なアセット管理機能を有効にします。

統合がアクティブになると、管理者は、Experience Manager Assetsのas a Cloud Serviceを、アセットの作成と管理のための唯一の情報源として、またCommerce プロジェクト用のアセットを一元的に管理、整理、配布するデジタルアセット管理ツール（DAM）として使用できるようになります。

## 要件

- Adobe Commerce 2.4.5 以降
   - PHP 8.1、8.2、8.3
   - コンポーザー：2.x
- Adobe Experience Managerは [Adobe Experience Manager Assetsのas a Cloud Service](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/overview) でプロビジョニングされています
- 統合を設定するAdobe Commerce ユーザーには、AEM Assets プロジェクトがプロビジョニングされている [IMS 組織 ](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) へのアクセス権が必要です。

## 統合の設定

>[!BEGINSHADEBOX]

**前提条件**

AEM Assets統合を設定するには、アプリケーションと環境設定をカスタマイズするための管理者アクセス権が必要です。

- AEM Assetsas a Cloud Service環境がプロビジョニングされているCloud Manager プログラムへの管理アクセス。
- Adobe Commerce環境への管理アクセスと、認証に必要な API キーを取得または生成する機能。

>[!ENDSHADEBOX]

CommerceとExperience Manager Assetsの統合を有効にするには、次の 3 つの手順を実行します。

1. [Experience Manager Assets プロジェクトを設定してCommerce アセットを管理します ](aem-assets-configure-aem.md)。

1. [Experience Manager Assets Integration 拡張機能をインストールし、Adobe Commerceを設定します ](aem-assets-configure-aem.md)。

1. [ アセットの同期を有効にする ](aem-assets-setup-synchronization.md)。
