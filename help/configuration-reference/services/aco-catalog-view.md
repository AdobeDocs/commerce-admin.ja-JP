---
title: '[!UICONTROL Services] > ACO カタログ ビュー'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL ACO Catalog View] ページでAdobe Commerce Optimizerの設定を確認し、更新します。
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

これらの設定を使用して、[!DNL Adobe Commerce Optimizer Connector for B2B]によって発行されるアクセストークンを制御します。 ストアフロントでは、これらのトークンを使用して、管理者で設定されたカスタム共有カタログから同期されたデータを入力したCommerce Optimizer プライベートカタログビューに対して認証を行います。

{{config}}

![ACO カタログを表示するAdobe Commerce管理者は、3,600秒のTTLおよびトークン発行が有効になっているアクセストークン設定を確認します。](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | グローバル | アクセストークンが生成された後も有効な状態を維持する秒数。 この設定は、デフォルトのスコープでは読み取り専用です。 web サイトまたはストアビューのスコープで設定された値は無視されます。 デフォルトは3600秒です。 |
| [!UICONTROL Issue Access Tokens] | ストアビュー | ストアフロントがカタログビューのアクセストークンを取得できるかどうかを制御します。 `No`に設定すると、`Company.catalogViewContext`はカタログビューIDを返しますが、アクセストークンは返さないため、Adobe Commerceから同期された[!DNL Adobe Commerce Optimizer]個のプライベートカタログビューから読み取るためにストアフロントが認証できません。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO カタログ ビュー同期](./aco-catalog-view-sync.md) — カタログ ビューを[!DNL Adobe Commerce Optimizer]に同期する方法を設定します
> - [ カタログ ビュー同期ステータスの監視](../../systems/catalog-view-sync-status.md) – 同期の正常性と調整ドリフトの監視
