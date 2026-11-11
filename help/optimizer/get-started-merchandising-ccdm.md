---
title: 役割別のカタログ マーチャンダイジングタスク
description: CCDMでプロビジョニングされたAdobe Commerce as a Cloud Service インスタンスを使用する管理者、開発者、マーチャンダイザー向けのタスクガイダンスを見つけます。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaSのみ" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="CCDMのみでプロビジョニングされたAdobe Commerce as a Cloud Service インスタンス（Adobeで管理されるSaaS インフラストラクチャ）に適用されます。"
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# 役割別のカタログ マーチャンダイジングタスク

このタスクリファレンスでは、コンポーザブルカタログデータモデル（CCDM）でプロビジョニングされたAdobe Commerce as a Cloud Service インスタンスで、カタログデータの設定、ストアフロントの統合、マーチャンダイジングの管理、パフォーマンスのレビューを行うためのガイダンスを見つけます。

責任は実装によって異なります。 次の節では、通常タスクを実行する役割ごとにタスクをグループ化します。

- 管理者は、Commerce Foundationで製品、価格、B2B設定を管理します。
- 開発者はストアフロント統合を設定し、カタログリクエストと行動データの収集を検証します。
- マーチャンダイジング担当者は、商品の発見とレコメンデーションを設定し、レポート機能を利用してマーチャンダイジングの意思決定に役立てることができます。

Adobe Commerce as a Cloud Serviceとのネイティブな連携により、商品と価格のデータをCCDMに同期。 コネクタを個別にインストールする必要はなく、App Builder アプリも必要ありません。

## カタログとストアフロントの準備

実装に適用されるタスクを完了します。 B2C カタログビューは手動で作成できます。 B2B カタログビュー、ポリシー、価格表は、Commerce FoundationのB2B設定から生成されます。

| タスク | 説明 | リソース |
| --- | --- | --- |
| **製品と価格の設定** | Commerce Foundationで商品と価格を管理します。 価格データは価格表としてCCDMに同期されます。CCDMで価格を独立して作成しないでください。 | [製品リスト ](../catalog/products-list.md)、[製品を作成](../catalog/product-create.md)、[価格範囲](../catalog/catalog-price-scope.md)、[高度な価格設定](../catalog/pricing-advanced.md) |
| **ストアビューの設定** | Commerce Foundationで、ストアフロントに必要なストアビューとローカライズされた商品データを設定します。 | [ ストアビュー](../stores-purchase/store-views.md) |
| **B2B共有カタログと会社の設定** | B2B実装の場合は、生成されたカタログ設定を確認する前に、Commerce Foundationで共有カタログと企業関係を設定します。 | [共有カタログ ](../b2b/catalog-shared.md)および[企業](../b2b/account-companies.md) |
| **B2C カタログ ビューとポリシーの設定** | カタログビューを作成し、使用可能な製品品揃えを定義するポリシーを選択します。 該当する同期価格表を各ビューに関連付けます。 | [ カタログ ビュー](./setup/catalog-view.md) |
| **B2B カタログビューのレビュー** | ネイティブ同期によって、予想されるカタログ ビュー、ポリシー、価格表が生成されたことを確認します。 重複する構造を手作業で作成するのではなく、Commerce Foundationで基盤となるB2B設定を管理できます。 | [B2B カタログ ビュー](./setup/catalog-view.md#b2b-catalog-views) |
| **ストアフロントの設定** | 目的のカタログコンテキストをリクエストするようにストアフロントを設定します。 カスタムまたはその他のストアフロントとの統合については、該当するカタログリクエストヘッダーを参照してください。 | [ ストアフロント設定](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

マーチャンダイジングを設定する前に、ストアフロントが予想される商品と価格を返すことを確認します。 カートへの追加、カート、チェックアウトをテストして、トランザクションの価格が意図したCommerce Foundation設定と一致することを確認します。

## マーチャンダイジングの設定とパフォーマンスのレビュー

| タスク | 説明 | リソース |
| --- | --- | --- |
| **製品検出の設定** | マーチャンダイジングルール、ファセット、類義語を設定する。 ルールは、あらゆるカタログビューに適用することも、特定のビューに合わせてカスタマイズすることもできます。 | [ マーチャンダイジングの概要](./merchandising/overview.md) |
| **検索設定の確認** | 実装の検索設定と使用可能なセマンティック検索オプションを確認します。 | [ マーチャンダイジング設定](./settings.md)および[ セマンティック検索](./setup/semantic-search.md) |
| **レコメンデーションの設定** | レコメンデーションユニットを作成し、ストアフロントが実装に必要な行動データを収集していることを確認します。 | [推奨事項の概要](./merchandising/recommendations/overview.md) |
| **パフォーマンスのレビュー** | 成功指標と検索パフォーマンスレポートを使用して、ストアフロントのアクティビティを評価し、マーチャンダイジングの意思決定に情報を提供します。 | [成功指標](./manage-results/success-metrics.md)および[検索パフォーマンス ](./manage-results/search-performance.md) |

## 次のステップ

マーチャンダイジングの設定とパフォーマンスの確認が完了したら、必要に応じてルール、ファセット、レコメンデーションの監視と調整を継続し、ストアフロント体験の最適化に取り組みます。
