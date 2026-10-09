---
title: カタログビュー設定の管理
description: B2B共有カタログ用に作成されたAdobe Commerce Optimizer カタログビューを確認し、それらを保護する制限付きアクセスキーを割り当てる方法について説明します。
feature: B2B, Companies, Catalog Management
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e9004f3c-09ae-5d24-acd2-fa0987fdb66e
    internal-label: Companies
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# カタログビュー設定の管理

[!DNL Adobe Commerce Optimizer Connector for B2B]拡張機能がインストールされている場合、カタログビューページには、カスタム共有カタログ用に作成された[!DNL Adobe Commerce Optimizer] [ カタログビューの予測](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}が一覧表示されます。  _投影_&#x200B;は、コネクタが共有カタログデータを[!DNL Adobe Commerce Optimizer]に同期したときに作成されたカタログビューです。 コネクターは、共有カタログ内の各ストアビューに対して個別の投影を作成するので、共有カタログには複数のカタログビューを含めることができます。 ストアフロント体験では、これらのカタログビューには、関連する共有カタログに割り当てられた企業のみがアクセスできます。

例えば、Acme Industrialが、EU Web サイトに属する1つの共有カタログ、EU Businessに割り当てられているとします。 このweb サイトには、次の2つのストアビューがあります。

- `English (UK)`

- `German (Germany)`

コネクターは、共有カタログを2つの[!DNL Adobe Commerce Optimizer] カタログビューにプロジェクトします。

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

同社は英語とドイツ語のカタログビューを持っていますが、共有カタログの割り当ては1つだけです。 各ストアビューには、対応するカタログビューのデータが表示されます。

同じweb サイトと顧客グループの価格範囲を使用する場合、両方のカタログ表示で同じ価格表を共有できます。

## カタログビュー認証

コネクターは、アクセスキーが制限されたカタログビューを保護します。 Adobe Commerceでは、秘密鍵を使用して、承認済み購入者のアクセストークンに署名します。 保護されたカタログ データを返す前に、[!DNL Adobe Commerce Optimizer]は、要求されたカタログ ビューに関連付けられている対応する公開鍵に対してトークンを検証します。

トークンの有効期間を設定するか、トークンの発行を無効にするには、[ サービス/ACO カタログビュー](/help/configuration-reference/services/aco-catalog-view.md)を参照してください。

これらのカタログビューを確認し、割り当てられたキーを共有カタログの&#x200B;_[!UICONTROL Catalog Views]_タブまたは関連会社の_[!UICONTROL Catalog Views]_ セクションから管理できます。どちらも、同じカタログビューと現在のキー割り当てを一覧表示します。 各場所からの正確なナビゲーションパスについては、[制限付きアクセスキーを編集](#edit-restricted-access-keys)を参照してください。

[!DNL Adobe Commerce Optimizer]への共有カタログデータの同期を監視するには、[ カタログビュー同期ステータスの監視](/help/systems/catalog-view-sync-status.md)を参照してください。

## カタログビューリファレンス

{{$include /help/_includes/catalog-views-reference-table.md}}

## 制限付きアクセスキーの編集

{{$include /help/_includes/edit-restricted-access-keys.md}}

詳細については、[制限付きアクセスキーの管理](/help/systems/restricted-access-keys.md)を参照してください。

>[!MORELIKETHIS]
>
> - [B2B共有カタログの投影](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [ サービス > ACO カタログビュー](/help/configuration-reference/services/aco-catalog-view.md)
> - [ カタログ ビュー同期ステータスの監視](/help/systems/catalog-view-sync-status.md)
> - [共有カタログの管理](catalog-shared-manage.md)
> - [会社アカウントの管理](account-company-manage.md)
