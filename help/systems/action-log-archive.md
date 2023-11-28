---
title: アクションログのアーカイブ
description: 管理アクションログアーカイブを設定および表示する方法について説明します。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# アクションログのアーカイブ

{{ee-feature}}

管理者 [アクション](action-log.md) アーカイブは、サーバーに保存されている CSV ログファイルをリストします。 設定では、ログエントリの保存期間とアーカイブ頻度を指定できます。 デフォルトでは、ファイル名には現在の日付が ISO 形式で含まれます。  `yyyyMMddHH`

>[!NOTE]
>
>ログのアーカイブには [cron ジョブ](cron.md) を設定します。

## ログアーカイブの設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Admin Actions Log Archiving]** を参照し、次のオプションを設定します。

   - **[!UICONTROL Log Entry Lifetime, Days]**  — ログ・エントリを削除するまでにデータベースに保存する日数を入力します。
   - **[!UICONTROL Log Archiving Frequency]**  — に設定します。 `Daily`, `Weekly`または `Monthly`.

   ![詳細設定 — 管理アクションログのアーカイブ](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   設定の詳細なリストについては、 [管理アクションログのアーカイブ](../configuration-reference/advanced/system.md) （内） _設定リファレンス_.

1. 完了したら、「 **[!UICONTROL Save Config]**.

## アーカイブを表示

次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![アクションログのアーカイブ](./assets/action-log-archive.png){width="600" zoomable="yes"}
