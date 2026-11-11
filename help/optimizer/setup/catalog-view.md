---
title: カタログビュー
description: カタログビューの概要と、ビジネス構造、ポリシー、価格設定によって商品カタログを整理するための作成方法について説明します。
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaSのみ" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="CCDMのみでプロビジョニングされたAdobe Commerce as a Cloud Service インスタンス（Adobeで管理されるSaaS インフラストラクチャ）に適用されます。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# カタログビュー

カタログビューでは、ストアフロントが取得できる商品と価格を定義します。 コンポーザブルカタログデータモデル（CCDM）でプロビジョニングされたAdobe Commerce as a Cloud Service インスタンスでは、カタログビューは、Adobe Commerce Optimizerと同じカタログ基盤を使用します。

カタログビューは、カタログソース、ポリシー、価格表を組み合わせて、ストアフロントのカタログコンテキストを定義します。 ポリシーによって、使用可能な製品品揃えが決まります。 マーチャンダイジングルールは、その品揃えの中の商品がどのようにプロモーションおよびランク付けされるかを制御し、すべてのカタログビューに適用するか、特定のビューに合わせてカスタマイズすることができます。 [ マーチャンダイジングルールの作成](../merchandising/rules/add.md)を参照してください。

Commerce財団は、商品と価格に関する信頼できる唯一の情報源です。 商品と価格のデータAdobe Commerce as a Cloud Serviceとのネイティブな連携により、コネクタをインストールしたり、App Builderアプリを使用することなく、単一の方法でCCDMに同期できます。 web サイト、実店舗、ストアビューの設定は、カート、チェックアウト、プロモーション、顧客、注文、決済などを管理するCommerce Foundationに残っています。

>[!NOTE]
>
>CCDMでプロビジョニングされたインスタンスの場合は、[Adobe Unified Experience](../../getting-started/admin-unified-experience.md)のCommerce Adminを使用して、カタログビューとポリシーを設定し、同期済みの価格表をカタログビューに関連付けます。 ライブサーチと商品レコメンデーションでカタログサービスを使用しているインスタンスは、これらのカタログ管理画面にアクセスできません。

## カタログビューの仕組み

カタログビューは、カタログデータとストアフロントのコンテキスト用の設定を統合したものです。 事業部門、ブランド、地域、その他のストアフロント体験を表すために使用できます。

- **[カタログソース](catalog-sources.md)**&#x200B;は、カタログエクスペリエンスに商品データを提供します。
- カタログビューの商品データを&#x200B;**[ポリシー](policies.md)**&#x200B;でフィルタリングします。
- **[価格表](pricebooks.md)**&#x200B;は、カタログ ビューに関連付けられた価格データを提供します。

カタログビューは、Adobe Commerce as a Cloud Serviceのweb サイト、ストア、ストアビュー構造に置き換わるものではありません。 Commerce Foundationでは、その構造とトランザクションオペレーションを引き続き管理します。

カタログデータは、Commerce FoundationからCCDMに一元的に同期されます。 CCDMは、ストアフロントのカタログエクスペリエンスと製品の発見をサポートします。 Commerce Foundationは、カート、チェックアウト、プロモーション、お客様、注文などを引き続き処理します。

## 始める前に

カタログビューを設定する前に：

- [Adobe Commerce as a Cloud Service インスタンスがCCDM](../overview.md)を使用していることを確認します。
- ストアフロントに必要なカタログデータが入力され、[同期](data-sync.md)されていることを確認します。
- ストアフロントのコンテキストに必要な[ カタログソース ](catalog-sources.md)、[ ポリシー](policies.md)、および[価格表](pricebooks.md)を特定します。
- B2C カタログビューを手動で作成する必要があるか、ネイティブ同期によって生成されたB2B カタログビューを確認する必要があるかを判断します。

>[!NOTE]
>
>B2B実装の場合、ネイティブ同期により、Commerce FoundationのB2B設定からカタログビュー、ポリシー、価格表が生成されます。 これらの自動生成された構造の重複を手動で作成しないでください。

## B2C実装用カタログビューの作成

B2C実装でカタログビューを手動で設定する必要がある場合は、このワークフローを使用します。

1. Unified Experience](../../getting-started/admin-unified-experience.md)で[Commerce管理者にログインし、CCDMでプロビジョニングされたAdobe Commerce as a Cloud Service インスタンスを選択します。
1. 左側のナビゲーションで、**[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**&#x200B;に移動します。
1. **[!UICONTROL Create catalog view]**&#x200B;を選択します。
1. カタログビューの名前を入力します。
1. ストアフロントコンテキストの[ カタログソースまたはソース ](catalog-sources.md)を選択します。
1. 関連する[ ポリシー](policies.md)をカタログ ビューに関連付けます。
1. 関連する価格表をカタログ ビューに関連付けるには、[価格表の可用性の設定](pricebooks.md)を行います。
1. カタログビューを作成します。

## B2B カタログビュー

B2B実装の場合、ネイティブ同期により、Commerce FoundationのB2B設定からカタログビュー、ポリシー、価格表が生成されます。 CCDMで重複した構造を手作業で作成するのではなく、Commerce Foundationで基盤となるB2B カタログと企業の関係を管理できます。

セットアップ手順については、[共有カタログの作成](../../b2b/catalog-shared-create.md)および[共有カタログへの会社の割り当て](../../b2b/catalog-shared-assign-companies.md)を参照してください。

B2B関係の設定後：

1. [同期](data-sync.md)が完了したことを確認します。
2. [統合エクスペリエンスのCommerce管理者](../../getting-started/admin-unified-experience.md)の生成されたカタログ ビュー、[ ポリシー](policies.md)および[価格表](pricebooks.md)を確認してください。
3. ストアフロントに、会社の予想される製品品揃えと価格が表示されていることを確認します。
4. カートへの追加、カート、チェックアウトをテストして、製品の在庫状況とトランザクションの価格が、意図したB2B設定に一致することを確認します。

## 価格表とチェックアウト

価格表は、カタログビューを通じて利用可能な価格データを提供します。 Adobe Commerce as a Cloud Serviceでは、Commerce Foundationが価格に関する信頼できる唯一の情報源であり続けており、価格データはネイティブ統合によってCCDMに同期されます。 カタログビューを設定する場合は、CCDMで価格を個別にオーサリングするのではなく、該当する同期価格表を使用します。

カートと決済にはCommerce Foundationの価格を使用します。 表示されるストアフロントの価格が、該当するカートとチェックアウトの価格と一致することを確認します。

## カタログビューのレビューと検証

カタログビューを設定した後、ストアフロントのエクスペリエンス全体を確認します。

- 目的のカタログデータが[同期済み](data-sync.md)であることを確認します。
- カタログ ビューが、意図した[ ポリシー](policies.md)および[価格表](pricebooks.md)に関連付けられていることを確認します。
- ストアフロントが予想される商品品揃えを返すことを確認します。
- 対応するCommerce Foundationの価格に対して、表示されている価格を確認します。
- カートへの追加、カート、チェックアウトをテストします。

B2B実装の場合は、同期によって生成されたカタログ構造が、目的の会社およびカタログ設定と一致することも確認します。

## トラブルシューティング

### ストアフロントに商品が表示されない

- [ インスタンスがCCDM](../overview.md)を使用していることを確認します。
- カタログデータが[同期済み](data-sync.md)であることを確認します。
- ストアフロントが意図したカタログコンテキストを使用していることを確認します。
- カタログ ビューに関連付けられている[ ポリシー](policies.md)を確認します。

### 表示された価格は予想外です

- 対象の[価格表](pricebooks.md)がカタログビューに関連付けられていることを確認します。
- 価格データが[同期済み](data-sync.md)であり、Commerce Foundationと一致していることを確認してください。

  Web サイトと顧客グループの価格マッピングについては、[価格表](pricebooks.md)を参照してください。

- カートとチェックアウトで価格を再度検証します。

### CCDM カタログ画面はCommerce管理者には表示されません

[選択したインスタンスがCCDM](../overview.md)を使用しており、Unified Experience](../../getting-started/admin-unified-experience.md)の[Commerce Adminにアクセスしていることを確認してください。 カタログサービス v1を実行しているインスタンスには、CCDM管理画面がありません。

## 関連コンテンツ

- [Adobe Commerce as a Cloud Serviceの導入方法](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started)
- [Adobe Commerce B2B共有カタログの概要](../../b2b/catalog-shared.md)
- [Adobe Commerce as a Cloud Service リリースノート](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/release-notes)
- [カタログの同期](data-sync.md)
