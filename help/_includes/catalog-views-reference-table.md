---
title: カタログビューの参照テーブル
description: カタログビューグリッドに再利用された参照テーブル
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# カタログビューの参照テーブル

グリッドには、共有カタログが[!DNL Adobe Commerce Optimizer]に同期されたときに作成された各カタログビューに1行が一覧表示されます。 グリッドは、キー割り当てアクションとは別に読み取り専用です。 コネクタがAdobe Commerceで設定された共有カタログを同期すると、カタログビューが自動的に作成および削除されます。 カタログが削除された場合、対応するカタログビューとデータが削除される前に[猶予期間](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period)があります。

制限付きアクセスキーの割り当てまたは割り当て解除については、[ カタログビューへのキーの割り当て](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view)を参照してください。

| フィールド | 説明 |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | [!DNL Adobe Commerce Optimizer]の対応するカタログ ビューの識別子。 同期の正常性を確認するには、[ カタログ表示の同期ステータスの概要](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary)を参照してください。 |
| [!UICONTROL Store View] | カタログビューが表すストアビュー。 [ ストアビュー](/help/stores-purchase/store-views.md)を参照してください。 |
| [!UICONTROL Access Keys] | 現在カタログ ビューに割り当てられている制限付きアクセス キーのタイトル。 [制限付きアクセスキー管理](/help/systems/restricted-access-keys.md)を参照してください。 |
| [!UICONTROL Actions] | カタログ ビューのキーを割り当てたり割り当て解除したりするには、**[!UICONTROL Edit Restricted Access Keys]**&#x200B;を選択します。 「[ カタログ ビューにキーを割り当て](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view)」を参照してください。 |

{style="table-layout:auto"}
