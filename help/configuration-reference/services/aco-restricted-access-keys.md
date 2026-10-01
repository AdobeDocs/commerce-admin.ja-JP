---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] ページで設定を確認します。
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

この設定を使用して、B2B共有カタログ ビューに対してプロビジョニングする制限付きアクセス キーに[!DNL Adobe Commerce Optimizer Connector for B2B]が適用する既定の有効期限を制御します。 これらのキーを作成、割り当て、削除するには、[制限付きアクセスキー管理](../../systems/restricted-access-keys.md)を参照してください。

{{config}}

## [!UICONTROL Provisioning]

![ プロビジョニング ](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | グローバル | 新しくプロビジョニングされた制限付きアクセスキーの有効期間。 [!DNL Adobe Commerce Optimizer]では、すべてのキーに対して少なくとも1分前の有効期限が必要です。有効期限が切れたキーはゲートウェイ読み取りから除外されるため、少なくとも1日の値が常に適用されます。 デフォルト値：`36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>自動キーのローテーションがまだ利用できないため、デフォルトの有効期限は長い有効期限に設定されます。 [ キーの選択とローテーション ](../../systems/restricted-access-keys.md#key-selection-and-rotation)を参照してください。

>[!MORELIKETHIS]
>
> - [ACO カタログビュー](./aco-catalog-view.md) — カタログビュー用のストアフロントアクセストークンの設定
> - [制限付きアクセスキー管理](../../systems/restricted-access-keys.md) – 制限付きアクセスキーの作成、割り当て、削除
> - [ カタログ ビュー同期ステータスの監視](../../systems/catalog-view-sync-status.md) – 有効期限が近づいているキーを監視します
