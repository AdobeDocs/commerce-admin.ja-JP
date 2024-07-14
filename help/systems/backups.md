---
title: システムバックアップ
description: ファイルシステム、データベース、メディアファイルを含む、システムバックアップを作成およびスケジュールする方法を説明します。
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# システムバックアップ

Adobe CommerceとMagento Open Sourceを使用すると、ファイルシステム、データベース、メディアファイルなど、システムの様々な部分をバックアップしたり、自動的にロールバックしたりできます。 各バックアップのレコードは、グリッドの [_バックアップ_] ページに表示されます。 リストからレコードを削除すると、アーカイブされたファイルも削除されます。 データベース バックアップ ファイルは、GZ 形式で圧縮されます。 システムバックアップとデータベースおよびメディアバックアップには、TGZ 形式が使用されます。 ベストプラクティスとして、拡張機能と更新をインストールする前に、バックアップツールへのアクセスを制限し、バックアップする必要があります。

- **バックアップツールへのアクセスを制限します。** バックアップおよびロールバック管理ツールへのアクセスは、バックアップおよびロールバックリソース用に [ ユーザーの役割 ](permissions-user-roles.md) を設定することで制限できます。 アクセスを制限するには、対応するチェックボックスをオフのままにします。 リソースのロールバックへのアクセス権を付与するには、バックアップ リソースへのアクセス権も付与する必要があります。

- **拡張機能とアップデートをインストールする前にバックアップしてください。** 拡張機能またはアップデートをインストールする前に、必ずバックアップを実行してください。

{{$include /help/_includes/backups-note.md}}

## バックアップの有効化とスケジュール設定

1. _管理者_ サイドバーで、**[!UICONTROL Stores]**/_[!UICONTROL Settings]_/**[!UICONTROL Configuration]**に移動します。

1. 左側のパネルで「**[!UICONTROL Advanced]**」を展開し、「**[!UICONTROL System]**」を選択します。

1. **[!UICONTROL Backup Settings]** の ![ 展開セレクター ](../assets/icon-display-expand.png) を展開します。

1. **[!UICONTROL Enabled Schedule Backup]** を `Yes` に設定します。

1. 自動バックアップをスケジュールするには、次のようにスケジュール・オプションを設定します。

   - **[!UICONTROL Enabled Schedule Backup]** を `Yes` に設定します。
   - スケジュールされた間隔で実行するバックアップのタイプに **[!UICONTROL Scheduled Backup Type]** を設定します。
   - **[!UICONTROL Start Time]** を、バックアップ操作を実行する時刻に設定します。
   - **[!UICONTROL Frequency]** を `Daily`、`Weekly` または `Monthly` に設定します。
   - **[!UICONTROL Maintenance Mode]** を `Yes` に設定します。

   ![ 詳細設定 – バックアップ ](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. 完了したら、「**[!UICONTROL Save Config]**」をクリックします。

## バックアップの作成

1. _管理者_ サイドバーで、**[!UICONTROL System]**/_[!UICONTROL Tools]_/**[!UICONTROL Backups]**に移動します。

1. 右上隅で、作成するバックアップの種類をクリックします。

   - **[!UICONTROL System Backup]** - データベースとファイル・システムの完全なバックアップを作成します。 この処理の間に、バックアップにメディア フォルダを含めることを選択できます。

   - **[!UICONTROL Database and Media Backup]** - データベースとメディア フォルダのバックアップを作成します。

   - **[!UICONTROL Database Backup]** - データベースのバックアップを作成します。

   ![ システムツール – バックアップ ](./assets/tools-backups.png){width="600" zoomable="yes"}

1. バックアップ中にストアをメンテナンスモードにするには、このチェックボックスを選択します。

   バックアップが完了すると、メンテナンスモードが自動的にオフになります。

1. システムバックアップの場合は、「**[!UICONTROL Include Media folder to System Backup]**」チェックボックスをオンにしてメディアフォルダーを含めます。

1. プロンプトが表示されたら、アクションを確認します。


