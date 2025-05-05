---
title: アクションログアーカイブ
description: 管理アクションログアーカイブを設定および表示する方法について説明します。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# アクションログアーカイブ

{{ee-feature}}

Admin [actions](action-log.md) アーカイブには、サーバーに保存されている CSV ログファイルが一覧表示されます。 設定では、ログエントリを保存する期間と、アーカイブする頻度を指定できます。 デフォルトでは、ファイル名には現在の日付が ISO 形式で含まれます。  `yyyyMMddHH`

>[!NOTE]
>
>ログのアーカイブには [cron ジョブ ](cron.md) を設定する必要があります。

## ログアーカイブの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. **[!UICONTROL Admin Actions Log Archiving]** のセクションの ![ 展開セレクター ](../assets/icon-display-expand.png) を展開し、次のオプションを設定します。

   - 「**[!UICONTROL Log Entry Lifetime, Days]**」 – ログエントリを削除する前に、ログエントリをデータベースに保持する日数を入力します。
   - **[!UICONTROL Log Archiving Frequency]** - `Daily`、`Weekly` または `Monthly` に設定します。

   ![ 詳細設定 – 管理アクションのログのアーカイブ ](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   設定の詳細なリストについては、『設定リファレンス _の [ 管理者アクションのログのアーカイブ ](../configuration-reference/advanced/system.md) を参照してください_。

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## アーカイブの表示

_管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Actions Logs]_/**[!UICONTROL Archive]**&#x200B;に移動します。

![ アクションログアーカイブ ](./assets/action-log-archive.png){width="600" zoomable="yes"}
