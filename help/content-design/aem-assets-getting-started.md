---
title: Commerce用AEM Assets統合の設定
description: ストアのCommerce アセットを管理するためにExperience Manager Assets環境を設定および設定する方法について説明します。
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/loyCmoFINQvC-13BGzAUKmcF7gY6T2e6mV-lK-SnVxo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 3%

---

# Commerce用AEM Assets統合の設定

Commerce用のAdobe Experience Manager Assets統合を設定するには、アプリケーションと環境の設定をカスタマイズするための管理者権限が必要です。

- AEM Assets as a Cloud Service環境がプロビジョニングされているCloud Manager プログラムへの管理アクセス。

- Adobe Commerceへの管理アクセスと、認証に必要なAPI キーの取得または生成の機能。

## 統合の使用要件

この統合を活用するには、次の要件を満たす必要があります。

- Adobe Commerce、Adobe Experience Manager Assets、および[AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)のアクティブライセンス。

- Adobe Commerce 2.4.5以降

- Adobe Experience Managerは[Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/ja/docs/experience-manager-cloud-service/content/assets/overview)でプロビジョニングされています

- 統合を設定するAdobe Commerce ユーザーは、AEM Assets プロジェクトがプロビジョニングされている[IMS Organization](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)にアクセスできる必要があります。

## 主な特長

- **追加費用なし**：この統合は、ライセンス要件を満たす販売者に無料で提供されます。

- **Adobeの公式ソリューション** - Adobeによって開発、保守、完全サポートされ、将来のプラットフォームの機能強化に伴う安定性と整合性が確保されます。

- **Adobe Managed Support Model**:Adobeがサポートとトラブルシューティングを処理し、安心と合理的な問題解決を実現します。

## 次のステップ

Experience Manager AssetsとのCommerce統合を有効にするには、次の3つの手順を実行します。

1. [AEM Assets パッケージ ](aem-assets-configure-aem.md)をインストールします。

1. [Adobe Commerce パッケージをインストール ](aem-assets-configure-aem.md)。

1. [統合アセットを設定](aem-assets-setup-synchronization.md)。
