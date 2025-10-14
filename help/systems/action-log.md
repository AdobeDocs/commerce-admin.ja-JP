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

アクションログ機能は、ストアで作業する管理者ユーザーが行ったすべての変更を（ログとして）記録します。 これにより、ストアに加えられたすべての変更を追跡できます。 これらの変更を追跡し、ユーザーの [&#x200B; 管理者権限 &#x200B;](permissions.md) を設定することで、不要な変更からストアを保護できます。

ほとんどの管理者アクションの場合、ログに記録される情報には、アクション、ユーザーの名前、アクションの成功または失敗、アクションの影響を受けるオブジェクトの ID が含まれます。 IP アドレスと日付も記録されます。

デフォルトでは、すべての管理者アクションが有効になり、記録されます。 管理者アクションのログを設定するには、オプションを確認し、各アクションタイプのチェックボックスをオンまたはオフにします。 Adobe Commerceでは、チェックされたタイプのみがログに記録されます。

[&#x200B; アクションログレポート &#x200B;](action-log-report.md) を表示して、ログに記録された管理者アクションと詳細を確認します。

![&#x200B; 詳細設定 – 管理アクションのログ &#x200B;](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

設定の詳細なリストについては、『設定リファレンス _の [&#x200B; 管理者アクションのログのアーカイブ &#x200B;](../configuration-reference/advanced/system.md) を参照してください_。

## ログ用の管理者アクションの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL Admin]**」を選択します。

1. **[!UICONTROL Admin Actions Logging]** のセクションの ![&#x200B; 展開セレクター &#x200B;](../assets/icon-display-expand.png) を展開し、各アクションに対して次の操作を行います。

   - アクションの管理者ログを有効にするには、チェックボックスを選択します。
   - アクションの管理者ログを無効にするには、このチェックボックスをオフにします。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## 管理アクション ログのアーカイブ

管理アクションログは、任意の日数だけアーカイブできます。 アーカイブは、指定した期間の後に削除することもできます。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. **[!UICONTROL Admin Action Log Archiving]** を展開し、オプションを設定します。

   - **[!UICONTROL Logs Entry Lifetime, Days]** - アーカイブ・ログを保持する日数を設定します。
   - **[!UICONTROL Log Archiving Frequency]** - アーカイブを作成する頻度を設定します。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。
