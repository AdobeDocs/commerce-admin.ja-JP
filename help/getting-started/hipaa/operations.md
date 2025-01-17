---
title: 運用
description: HIPAA 対応ソリューションへの移行、およびトラブルシューティングのためのセカンダリステージング環境の使用に関するガイドライン。
source-git-commit: 999d3126ae368000fc2c58c315473739012f3934
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# 運用

Adobe Commerce向けの HIPAA 対応製品への移行と、トラブルシューティングに `staging_for_support` 環境を使用する方法については、次のガイドラインを参照してください。

## 移行

HIPAA 非対応のCommerce製品から HIPAA 対応の製品に移行する場合は、次のガイドラインに従う必要があります。

1. **既存のデータセットを削除**:Adobe Commerce SaaS レイヤーで機密データと非機密データが混在しないように、移行前に既存のデータセットをすべて削除する必要があります。 サポートチケットを作成して、データセットを削除します。
1. **新しい環境の設定**：新しい HIPAA Commerce インスタンスでの [Commerce サービスコネクタ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) の設定は、データセットが削除された後にのみ設定する必要があります。 新しい HIPAA SaaS 環境は、古いデータセットが削除された後にのみ使用する必要があります。 Commerce サービスコネクタの設定により、新しい SaaS データセットの作成が自動的にトリガーされます。
1. **移行戦略**:SaaS データセットの削除は元に戻せないプロセスであり、カタログデータと関連する設定がすべて削除されます。 古いデータや設定を引き継ぐ場合は、移行戦略を導入する必要があります。 この戦略は、商人の責任である。 既存のデータセットを削除するためのサポートチケットは、移行データのバックアップ（該当する場合）が完了した後でのみ作成してください。

>[!NOTE]
>既存のデータセットを削除するには、「HIPAA 移行：SaaS データセットを削除」というタイトルのAdobe Commerce サポートチケットを作成し、`MAGEID` を指定して、削除する必要がある SaaS プロジェクト ID を指定する必要があります。

## Adobe Commerce サポートによるトラブルシューティング

Adobe Commerce HIPAA 対応のサービスには、Adobe Commerce サポートチームがトラブルシューティング目的で使用する `staging_for_support` 環境が追加されています。

お客様は、次の環境を確認する必要 `staging_for_support` あります。

- 保護された医療情報（PHI）など、機密データは含まれませんが、これらに限定されません。
- 実稼動アクティビティには使用できません。
- 混乱を避けるために、`staging_for_support` と異なる名前を付けることはできません。
- コードと実稼動環境の設定の両方を使用して最新の状態を維持し、できるだけ実稼動環境に近い環境でトラブルシューティングが確実に実行されるようにします。

## Commerce サービス

- **HIPAA 非対応のCommerce サービス** - Adobe Commerce サービスは HIPAA に対応していないので、ライブサーチ、商品Recommendations、支払いサービス、Sales Channel、Commerce Intelligenceなどの HIPAA サービスを使用しないでください。 [HIPAA 対応サービス ](overview.md) のみを使用する必要があります。

- **データ接続** - [ データ接続 ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 拡張機能内のバックオフィスコレクターのみが HIPAA に対応しています。 HIPAA に対応していないデータ接続サービス（ストアフロントイベントやAudience Activationなど）に PHI を送信しないでください。 ストアフロントのデータ収集が無効になっていることを確認する必要があります。

- **カタログサービス** – 設計上、[ カタログサービス ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview) は PHI を処理しないので、HIPAA 対応監査およびコンプライアンスの範囲外です。 お客様は、ご自身のユースケースの評価に基づき、弁護士と相談の上、本サービスを確実に利用する責任を負います。 また、HIPAA に対応していないサービスに PHI が渡されるリスクを回避するため、連合サービスを通じてカタログサービスを使用しないでください。

- **SaaS Data Export**:[SaaS Data Export](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) サービスは、Adobe Commerceの HIPAA 対応コンポーネントのデータのみを送信するように設定する必要があります。
