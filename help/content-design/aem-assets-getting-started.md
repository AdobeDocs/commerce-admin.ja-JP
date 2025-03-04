---
title: Commerce用のAEM Assets統合の設定
description: Experience Manager Assets環境を設定して、ストアのCommerce アセットを管理する方法について説明します。
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 934473c5124002b3b0b1bee2da47afff468406dc
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Commerce用のAEM Assets統合の設定

CommerceのAdobe Experience Manager Assets統合を設定するには、管理者アクセス権でアプリケーションと環境の設定をカスタマイズする必要があります。

- AEM Assets as a Cloud Service環境がプロビジョニングされているCloud Manager プログラムへの管理アクセス。

- Adobe Commerce環境への管理アクセス、および認証に必要な API キーを取得または生成する機能。

## 統合を使用するための要件

この統合を活用するには、企業が次の要件を満たす必要があります。

- Adobe Commerce、Adobe Experience Manager Assets、[AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media) のアクティブなライセンス。

- Adobe Commerce 2.4.5 以降

   - PHP 8.1、8.2、8.3
   - コンポーザー：2.x

- Adobe Experience Managerは [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/overview) でプロビジョニングされます

- 統合を設定するAdobe Commerce ユーザーには、AEM Assets プロジェクトがプロビジョニングされている [IMS 組織 ](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) へのアクセス権が必要です。

## 主なメリット

- **追加費用なし** – この統合は、ライセンス要件を満たすマーチャントに対して無料で提供されます。

- **Adobeの公式ソリューション** - Adobeで開発、維持管理、完全なサポートが行われ、安定性と将来のプラットフォーム機能強化への対応が保証されています。

- **Adobe マネージドサポートモデル** - Adobeはサポートとトラブルシューティングを扱うので、安心感があり、問題の解決が合理化されます。

## 次の手順

CommerceとExperience Manager Assetsの統合を有効にするには、次の 3 つの手順を実行します。

1. [Adobe Experience Manager Assets プロジェクトを設定してAdobe Commerce Assets を管理します ](aem-assets-configure-aem.md)。

1. [Adobe Experience Manager Assets integration for Commerce拡張機能をインストールし、Adobe Commerceを設定します ](aem-assets-configure-aem.md)。

1. [ アセットの同期を有効にする ](aem-assets-setup-synchronization.md)。
