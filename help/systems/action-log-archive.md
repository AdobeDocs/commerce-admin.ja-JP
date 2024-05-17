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

管理者 [アクション](action-log.md) アーカイブ：サーバーに保存されている CSV ログファイルをリストします。 設定では、ログエントリを保存する期間と、アーカイブする頻度を指定できます。 デフォルトでは、ファイル名には現在の日付が ISO 形式で含まれます。  `yyyyMMddHH`

>[!NOTE]
>
>ログのアーカイブには [cron ジョブ](cron.md) を設定します。

## ログアーカイブの設定

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します **[!UICONTROL Advanced]** を選択します **[!UICONTROL System]**.

1. を展開 ![展開セレクター](../assets/icon-display-expand.png) この **[!UICONTROL Admin Actions Log Archiving]** を選択し、次のオプションを設定します。

   - **[!UICONTROL Log Entry Lifetime, Days]** — ログ エントリを削除する前にデータベースに保存する日数を入力します。
   - **[!UICONTROL Log Archiving Frequency]**  – に設定 `Daily`, `Weekly`、または `Monthly`.

   ![詳細設定 – 管理者アクションのログのアーカイブ](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   設定の詳細なリストについては、を参照してください [管理アクションのログのアーカイブ](../configuration-reference/advanced/system.md) が含まれる _設定リファレンス_.

1. 完了したら、 **[!UICONTROL Save Config]**.

## アーカイブの表示

日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![アクションログアーカイブ](./assets/action-log-archive.png){width="600" zoomable="yes"}
