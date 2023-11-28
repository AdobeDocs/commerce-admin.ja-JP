---
title: アクションログ
description: アクションログの概要と、ストアに対するすべての変更を追跡するのに役立つ、ログに記録されるアクションを設定する方法について説明します。
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# アクションログ

{{ee-feature}}

アクションログ機能では、ストアで作業する管理者ユーザーがおこなったすべての変更が記録（ログ）されます。 これにより、ストアに対するすべての変更を追跡できます。 これらの変更の追跡と設定 [管理者権限](permissions.md) のユーザーは、を使用して、不要な変更からストアを保護できます。

ほとんどの管理者アクションでは、ログに記録される情報には、アクション、ユーザーの名前、アクションの成功または失敗、アクションの影響を受けるオブジェクトの ID が含まれます。 IP アドレスと日付も記録されます。

デフォルトでは、すべての管理アクションが有効になり、ログに記録されます。 管理アクションログを設定するには、オプションを確認し、各アクションタイプのチェックボックスをオンまたはオフにします。 Adobe Commerceログはチェック済みのタイプのみを記録します。

次を表示： [アクションログレポート](action-log-report.md) ログに記録された管理者のアクションと詳細を確認する

![詳細設定 — 管理アクションのログ](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

設定の詳細なリストについては、 [管理アクションログのアーカイブ](../configuration-reference/advanced/system.md) （内） _設定リファレンス_.

## ログに対する管理者アクションの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL Admin]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Admin Actions Logging]** 」セクションに移動し、各アクションで次の操作を実行します。

   - アクションの管理者ログを有効にするには、チェックボックスをオンにします。
   - アクションの管理者ログを無効にするには、チェックボックスをオフにします。

1. 完了したら、「 **[!UICONTROL Save Config]**.

## 管理アクションログをアーカイブ

管理アクションログは、任意の日数にわたってアーカイブできます。 アーカイブは、指定された期間が経過した後に削除することもできます。

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 **[!UICONTROL Admin Action Log Archiving]** オプションを設定します。

   - **[!UICONTROL Logs Entry Lifetime, Days]**  — アーカイブ済みログを保持する日数を設定します。
   - **[!UICONTROL Log Archiving Frequency]**  — アーカイブ作成の頻度を設定します。

1. 完了したら、「 **[!UICONTROL Save Config]**.
