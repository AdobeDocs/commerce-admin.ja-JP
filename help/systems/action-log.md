---
title: アクションログ
description: アクションログと、ログに記録されたアクションを設定する方法を説明し、ストアに加えられたすべての変更を追跡できるようにします。
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# アクションログ

{{ee-feature}}

アクションログ機能は、ストアで作業する管理者ユーザーが行ったすべての変更を（ログとして）記録します。 これにより、ストアに加えられたすべての変更を追跡できます。 これらの変更の追跡とその設定 [管理者権限](permissions.md) ユーザーにとっては、は、不要な変更からストアを保護するのに役立ちます。

ほとんどの管理者アクションの場合、ログに記録される情報には、アクション、ユーザーの名前、アクションの成功または失敗、アクションの影響を受けるオブジェクトの ID が含まれます。 IP アドレスと日付も記録されます。

デフォルトでは、すべての管理者アクションが有効になり、記録されます。 管理者アクションのログを設定するには、オプションを確認し、各アクションタイプのチェックボックスをオンまたはオフにします。 Adobe Commerceでは、チェックされたタイプのみがログに記録されます。

を表示する [アクションログレポート](action-log-report.md) 記録された管理者のアクションと詳細を確認します。

![詳細設定 – 管理アクションのログ](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

設定の詳細なリストについては、を参照してください [管理アクションのログのアーカイブ](../configuration-reference/advanced/system.md) が含まれる _設定リファレンス_.

## ログ用の管理者アクションの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL Admin]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Admin Actions Logging]** を参照し、各アクションに対して次の操作を行います。

   - アクションの管理者ログを有効にするには、チェックボックスを選択します。
   - アクションの管理者ログを無効にするには、このチェックボックスをオフにします。

1. 完了したら、 **[!UICONTROL Save Config]**.

## 管理アクション ログのアーカイブ

管理アクションログは、任意の日数だけアーカイブできます。 アーカイブは、指定した期間の後に削除することもできます。

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 **[!UICONTROL Admin Action Log Archiving]** オプションを設定します。

   - **[!UICONTROL Logs Entry Lifetime, Days]** - アーカイブ ログを保持する日数を設定します。
   - **[!UICONTROL Log Archiving Frequency]** - アーカイブを作成する頻度を設定します。

1. 完了したら、 **[!UICONTROL Save Config]**.
