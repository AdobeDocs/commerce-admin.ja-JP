---
title: '[!UICONTROL Services] > ACO カタログ ビュー同期'
description: Commerce管理者の[!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] ページで設定を確認します。
feature: Configuration, Security
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
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
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

これらの設定を使用して、[!DNL Adobe Commerce Optimizer Connector for B2B]がB2B共有カタログの設定（カタログ ビュー、ポリシー、価格表、キー）を[!DNL Adobe Commerce Optimizer]に同期する方法と、2つのシステム間の設定の違いを解決する方法を制御します。 これらの設定の結果を監視するには、[&#x200B; カタログ表示の同期ステータスの監視](../../systems/catalog-view-sync-status.md)を参照してください。

{{config}}

## [!UICONTROL Deletion]

![削除](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | グローバル | 共有カタログデータの保持期間。 削除された共有カタログのカタログビュー、ポリシー、メタデータがハード削除される前に保持される日数を指定します。 デフォルトの値は7日間です。 すぐにハード削除するには、`0`に設定します。 |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | グローバル | 新しく登録されたカタログビューが、カタログビュー、ポリシー、価格表、および主要設定の最初の同期を[!DNL Adobe Commerce Optimizer Connector for B2B]が完了するのを待つ日数です。ステータスは[!UICONTROL Pending]として報告されます。 同期が成功せずに猶予期間が終了すると、ステータスは[!UICONTROL Failed]に変わります。 デフォルト値：`1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| フィールド | [範囲](../../getting-started/websites-stores-views.md#scope-settings) | 説明 |
| --- | --- | --- |
| [!UICONTROL Enabled] | グローバル | スケジュールされたドリフト調整プログラムを実行して、[!DNL Adobe Commerce]から予測されるカタログ ビューと[!DNL Adobe Commerce Optimizer]のカタログ ビュー設定との違いを検出してレポートします。 `automatically repair drift`が有効になっている場合、修復可能な不一致も修正しようとします。 |
| [!UICONTROL Automatically Repair Drift] | グローバル | `Yes`に設定すると、スケジュールされたドリフト調整ツールは[!DNL Adobe Commerce Optimizer]設定を[!DNL Adobe Commerce]に一致するように更新し、設定を再同期します。 `No`に設定すると、実行ではドリフトのみが検出され、レポートが送信されます。 孤立した[!DNL Adobe Commerce Optimizer] エンティティは常に報告され、自動的に削除されることはありません。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO カタログビュー](./aco-catalog-view.md) — カタログビューのストアフロント読み取り用にアクセストークンを設定します
> - [&#x200B; カタログ ビュー同期ステータスの監視](../../systems/catalog-view-sync-status.md) – 同期の正常性を監視し、これらの設定を使用してドリフトを調整します
> - [制限付きアクセスキー管理](../../systems/restricted-access-keys.md) – 同期されたカタログ ビューに割り当てられたアクセスキーを管理します
