---
title: システムバックアップ
description: ファイルシステム、データベース、メディアファイルなどのシステムバックアップを作成およびスケジュールする方法について説明します。
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
TQID: https://experienceleague.adobe.com/kx2acbOSrWMJGv3ST6qKAXjLPgL2Lsh16wWvOxNO7FE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# システムバックアップ

Adobe CommerceとMagento Open Sourceでは、ファイルシステム、データベース、メディアファイルなど、システムのさまざまな部分をバックアップし、自動的にロールバックできます。 各バックアップのレコードが&#x200B;_バックアップ_ ページのグリッドに表示されます。 リストからレコードを削除すると、アーカイブされたファイルも削除されます。 データベースバックアップファイルは、GZ形式を使用して圧縮されます。 システム・バックアップとデータベース・バックアップおよびメディア・バックアップには、TGZ形式が使用されます。 ベストプラクティスとして、拡張機能とアップデートをインストールする前に、バックアップツールへのアクセスを制限し、バックアップする必要があります。

- **バックアップ ツールへのアクセスを制限します。** バックアップおよびロールバック管理ツールへのアクセスは、バックアップおよびロールバック リソース用に[&#x200B; ユーザーの役割](permissions-user-roles.md)を設定することで制限できます。 アクセスを制限するには、対応するチェックボックスを選択しないままにします。 リソースをロールバックするためのアクセス権を付与するには、バックアップリソースへのアクセス権も付与する必要があります。

- **拡張機能とアップデートをインストールする前にバックアップします。** 拡張機能またはアップデートをインストールする前に、必ずバックアップを実行してください。

{{$include /help/_includes/backups-note.md}}

## バックアップの有効化とスケジュール

1. _管理者_ サイドバーで、**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;に移動します。

1. 左側のパネルで、**[!UICONTROL Advanced]**&#x200B;を展開し、**[!UICONTROL System]**&#x200B;を選択します。

1. **[!UICONTROL Backup Settings]**&#x200B;の![拡張セレクター](../assets/icon-display-expand.png)を展開します。

1. **[!UICONTROL Enabled Schedule Backup]**&#x200B;を`Yes`に設定します。

1. 自動ベックアップをスケジュールするには、スケジューリングオプションを設定します。

   - **[!UICONTROL Enabled Schedule Backup]**&#x200B;を`Yes`に設定します。
   - スケジュールされた間隔で実行するバックアップのタイプに&#x200B;**[!UICONTROL Scheduled Backup Type]**&#x200B;を設定します。
   - バックアップ操作を実行する時刻に&#x200B;**[!UICONTROL Start Time]**&#x200B;を設定します。
   - **[!UICONTROL Frequency]**&#x200B;を`Daily`、`Weekly`または`Monthly`に設定します。
   - **[!UICONTROL Maintenance Mode]**&#x200B;を`Yes`に設定します。

   ![詳細設定 – バックアップ &#x200B;](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. 完了したら、**[!UICONTROL Save Config]**&#x200B;をクリックします。

## バックアップの作成

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**&#x200B;に移動します。

1. 右上隅で、作成するバックアップの種類をクリックします。

   - **[!UICONTROL System Backup]** - データベースとファイルシステムの完全バックアップを作成します。 プロセス中に、メディアフォルダーをバックアップに含めるように選択できます。

   - **[!UICONTROL Database and Media Backup]** - データベースとメディア フォルダーのバックアップを作成します。

   - **[!UICONTROL Database Backup]** - データベースのバックアップを作成します。

   ![&#x200B; システム ツール – バックアップ &#x200B;](./assets/tools-backups.png){width="600" zoomable="yes"}

1. バックアップ中にストアをメンテナンスモードにするには、チェックボックスをオンにします。

   バックアップが完了すると、メンテナンスモードが自動的にオフになります。

1. システムバックアップの場合は、**[!UICONTROL Include Media folder to System Backup]** チェックボックスを選択して、メディアフォルダーを含めます。

1. プロンプトが表示されたら、アクションを確認します。



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
