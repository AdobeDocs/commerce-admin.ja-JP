---
title: 業務運営
description: HIPAA対応オファーに移行し、セカンダリステージング環境を使用してトラブルシューティングを行うためのガイドラインです。
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/w3CGUMXmuXy8006HmWG0K-q3ntjbHFAaC61O6t7S4Ao
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# 業務運営

{{ee-feature}}

Adobe CommerceのHIPAA対応ソリューションへの移行と、トラブルシューティングに`staging_for_support`環境を使用する方法については、次のガイドラインを参照してください。

## 移行

非HIPAA Commerce製品からHIPAA対応の製品に移行するお客様は、次のガイドラインに従う必要があります。

1. **既存のデータスペースを削除**：移行前に、Adobe Commerce SaaS レイヤーで機密データと非機密データが混在しないように、既存のすべてのデータスペースを削除する必要があります。 サポートチケットを作成して、データスペースを削除します。
1. **Configure new environment**：新しいHIPAA Commerce インスタンスの[Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas)設定は、データスペースが削除された後にのみ設定する必要があります。 新しいHIPAA SaaS環境は、古いデータスペースを削除した後にのみ使用する必要があります。 Commerce Services Connectorの設定により、新しいSaaS データスペースの作成が自動的にトリガーされます。
1. **移行戦略**: SaaS データスペースの削除は元に戻すことのできないプロセスであり、カタログデータと関連する設定をすべて削除します。 古いデータまたは設定のいずれかを転送する場合は、移行戦略を導入する必要があります。 この戦略は加盟店の責任です。 既存のデータスペースを削除するためのサポートチケットは、移行データのバックアップ（該当する場合）が完了した後にのみ作成する必要があります。

>[!NOTE]
>既存のデータスペースを削除するには、お客様は「HIPAA Migration: Delete SaaS dataspaces」というタイトルのAdobe Commerce サポートチケットを作成し、`MAGEID`を指定し、削除する必要があるSaaS プロジェクト IDを指定する必要があります。

## Adobe Commerce サポートによるトラブルシューティング

Adobe CommerceのHIPAA対応サービスには、Adobe Commerce サポートチームがトラブルシューティングの目的で使用する`staging_for_support`環境が追加されています。

お客様は、`staging_for_support`環境を確認する必要があります。

- 保護された健康情報（PHI）など、機密データが含まれていません。
- 実稼動アクティビティには使用しないでください。
- 混乱を避けるために、`staging_for_support`とは異なる名前を付けることはできません。
- 本番環境のコードと設定の両方を使用して最新の状態に保ち、トラブルシューティングを本番環境にできるだけ近い環境で実行できるようにします。

## Commerce services

- **非HIPAA対応のCommerce サービス**：お客様は、HIPAA対応になっていないため、ライブサーチ、商品レコメンデーション、支払いサービス、販売チャネル、Commerce IntelligenceなどのAdobe Commerce サービスを使用できません。 お客様は[HIPAA対応サービス ](overview.md)のみを使用してください。

- **データ接続** - [ データ接続](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview)拡張機能内のバックオフィスコレクターのみがHIPAA対応です。 お客様は、ストアフロントイベントやAudience Activationなど、HIPAAに対応していないデータ接続サービスにPHIを送信しないでください。 顧客は、ストアフロントデータ収集が無効になっていることを確認する必要があります。

- **カタログサービス** – 設計上、[ カタログサービス ](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview)はPHIを処理しないため、HIPAA準備監査とコンプライアンスの対象外です。 お客様は、ユースケースに関する独自の評価に基づいて、また弁護士と相談しながら、本サービスを確実に使用する責任があります。 また、PHIを非HIPAA対応サービスに渡すリスクを回避するために、フェデレーションサービスを介してカタログサービスを使用しないでください。

- **SaaS データ書き出し** - [SaaS データ書き出し](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) サービスは、Adobe CommerceのHIPAA対応コンポーネントにのみデータを送信するように設定する必要があります。
