---
title: アクションログアーカイブ
description: 管理者アクションログアーカイブを設定および表示する方法について説明します。
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/xgyeoO5XJFZPopM9bsIn2oOtrxl4fyuEY2du5ryXeTY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# アクションログアーカイブ

{{ee-feature}}

管理者[ アクション ](action-log.md) アーカイブには、サーバーに保存されているCSV ログファイルが一覧表示されます。 設定では、ログエントリの保存期間とアーカイブ頻度を指定できます。 デフォルトでは、ファイル名には現在の日付がISO形式で含まれています：`yyyyMMddHH`

>[!NOTE]
>
>ログのアーカイブには、[cron ジョブ ](cron.md)を設定する必要があります。

## ログアーカイブの設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. **[!UICONTROL Admin Actions Log Archiving]** セクションの![拡張セレクター](../assets/icon-display-expand.png)を展開し、次のオプションを設定します。

   - **[!UICONTROL Log Entry Lifetime, Days]** — ログエントリを削除する前にデータベースに保持する日数を入力します。
   - **[!UICONTROL Log Archiving Frequency]** — `Daily`、`Weekly`または`Monthly`に設定します。

   ![詳細設定 – 管理者アクションのログのアーカイブ ](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   構成設定の詳細なリストについては、_構成リファレンス_&#x200B;の[管理者アクション ログ アーカイブ ](../configuration-reference/advanced/system.md)を参照してください。

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## アーカイブを表示

_管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**に移動します。

![ アクションログアーカイブ ](./assets/action-log-archive.png){width="600" zoomable="yes"}
