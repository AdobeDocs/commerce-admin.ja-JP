---
title: システムのバックアップ
description: ファイルシステム、データベース、メディアファイルなど、システムバックアップを作成し、スケジュールを設定する方法を説明します。
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# システムのバックアップ

Adobe CommerceとMagento Open Sourceを使用すると、ファイルシステム、データベース、メディアファイルなど、システムの様々な部分をバックアップし、自動的にロールバックできます。 各バックアップのレコードは、 _バックアップ_ ページに貼り付けます。 リストからレコードを削除すると、アーカイブされたファイルも削除されます。 データベースのバックアップファイルは GZ 形式で圧縮されます。 システムのバックアップ、データベースおよびメディアのバックアップでは、TGZ 形式が使用されます。 ベストプラクティスとして、拡張機能とアップデートをインストールする前に、バックアップツールへのアクセスを制限し、バックアップする必要があります。

- **バックアップツールへのアクセスを制限します。** バックアップとロールバック管理ツールへのアクセスは、 [ユーザーの役割](permissions-user-roles.md) バックアップおよびロールバックリソース用。 アクセスを制限するには、対応するチェックボックスを選択解除したままにします。 ロールバックリソースへのアクセス権を付与するには、バックアップリソースへのアクセス権も付与する必要があります。

- **拡張機能とアップデートをインストールする前にバックアップします。** 拡張機能をインストールまたは更新する前に、必ずバックアップを実行してください。

{{$include /help/_includes/backups-note.md}}

## バックアップの有効化とスケジュール設定

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 左側のパネルで、を展開します。 **[!UICONTROL Advanced]** を選択します。 **[!UICONTROL System]**.

1. 展開 ![拡張セレクター](../assets/icon-display-expand.png) の **[!UICONTROL Backup Settings]**.

1. 設定 **[!UICONTROL Enabled Schedule Backup]** から `Yes`.

1. 自動ベックアップをスケジュールするには、スケジュールオプションを設定します。

   - 設定 **[!UICONTROL Enabled Schedule Backup]** から `Yes`.
   - 設定 **[!UICONTROL Scheduled Backup Type]** を、スケジュールされた間隔で実行するバックアップのタイプに変更します。
   - 設定 **[!UICONTROL Start Time]** バックアップ・オペレーションを実行する時刻を指定します。
   - 設定 **[!UICONTROL Frequency]** から `Daily`, `Weekly`または `Monthly`.
   - 設定 **[!UICONTROL Maintenance Mode]** から `Yes`.

   ![高度な構成 — バックアップ](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. 完了したら、「 **[!UICONTROL Save Config]**.

## バックアップの作成

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. 右上隅で、作成するバックアップの種類をクリックします。

   - **[!UICONTROL System Backup]**  — データベースとファイル・システムの完全なバックアップを作成します。 プロセス中に、メディアフォルダをバックアップに含めるように選択できます。

   - **[!UICONTROL Database and Media Backup]**  — データベースとメディアフォルダーのバックアップを作成します。

   - **[!UICONTROL Database Backup]**  — データベースのバックアップを作成します。

   ![システムツール — バックアップ](./assets/tools-backups.png){width="600" zoomable="yes"}

1. バックアップ中にストアをメンテナンスモードにするには、チェックボックスをオンにします。

   バックアップが完了すると、メンテナンスモードは自動的にオフになります。

1. システムバックアップの場合は、 **[!UICONTROL Include Media folder to System Backup]** チェックボックスをオンにしてメディアフォルダーを含めます。

1. プロンプトが表示されたら、アクションを確定します。


