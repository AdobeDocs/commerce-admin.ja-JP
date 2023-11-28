---
title: サポートツール
description: システム内の問題を特定するために使用できる、提供されているサポートツールについて説明します。
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# サポートツール

{{ee-feature}}

サポートツールは、システムの既知の問題を特定するように設計されています。 開発および最適化プロセス中のリソースとして、また、サポートチームが問題を特定して解決するのに役立つ診断ツールとして使用できます。

## データコレクター

データコレクターで、Adobe Commerceのインストールに関する問題のトラブルシューティングに必要な、アドビのサポートチームのシステムに関する情報が収集されます。 作成されたバックアップの完了には数分かかり、コードダンプとデータベースダンプの両方が含まれます。 データは CSV または Excel XML ファイルに書き出すことができます。

![システム — データコレクター](./assets/data-collector.png){width="600" zoomable="yes"}

### データコレクターを実行する

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 右上隅で、 **[!UICONTROL New Backup]**.

   バックアップの生成には数分かかります。 処理結果は、 **[!UICONTROL Refresh Status]**. 完了すると、バックアップが _[!UICONTROL Data Collector]_グリッド。

1. バックアップの詳細を含むログを表示するには、次の手順を実行します。

   - Adobe Analytics の _[!UICONTROL Action]_列、選択&#x200B;**[!UICONTROL Show Log]**.

   - クリック **[!UICONTROL Back]** をクリックして、グリッドに戻ります。

   ![データコレクターログ](./assets/data-collector-log.png){width="600" zoomable="yes"}

### バックアップデータのエクスポート

1. 最初の列で、エクスポートするバックアップのチェックボックスを選択します。

1. 以下を使用します。 **[!UICONTROL Export]** メニューを使用して、エクスポートデータの形式を選択します。

   ![書き出し形式](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Web ブラウザーのダウンロード場所からファイルにアクセスし、 **[!UICONTROL Save]** その通り。

### バックアップデータをダウンロード

バックアップの生成後、コードと DB データのコピーをダウンロードできます。

1. グリッド内で必要なバックアップエンティティを探します。

1. これには、 `Complete` ステータス。

1. でエンティティ名をクリックします。 _[!UICONTROL Code Dump]_または_[!UICONTROL DB Dump]_ 列。

ダウンロードプロセスが自動的に開始します。

## バックアップデータを削除

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 削除するバックアップデータを見つけて選択します。

1. Adobe Analytics の _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## システムレポート

システムレポートツールを使用すると、システムの定期的な完全（部分的）なスナップショットを取得し、将来の参照用に保存できます。 コード開発サイクルの前後のパフォーマンス設定や、サーバー設定の変更を比較できます。 システムレポートツールを使用すると、サポートが調査を開始する際に必要な情報の準備と送信に要する時間を大幅に短縮できます。

「システムレポート」グリッドから、既存のレポートの表示とダウンロード、レポートの削除、レポートの作成を行うことができます。

### システムレポートへのアクセス

次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![管理 — システムレポート](./assets/reports.png){width="600" zoomable="yes"}

### レポートの生成

1. クリック **[!UICONTROL New Report]**.

1. Adobe Analytics の **[!UICONTROL Groups]** 」リストで、レポートに含める各情報セットを選択します。 デフォルトでは、すべてのグループが選択されています。

   ![システムレポート — グループの選択](./assets/report-create.png){width="600" zoomable="yes"}

1. 右上隅で、 **[!UICONTROL Create]**.

   選択したレポートタイプの数によっては、レポートの生成に数分かかる場合があります。 レポートの準備が整うと、グリッドの上部に、生成された日時でレポートが表示されます。

### モジュール情報の表示

インストールされているモジュールに関する有用な情報を確認できます。

**_インストールされている各モジュールのレポート情報を表示するには、次の手順に従います。_**

1. 次の日： _管理者_ サイドバー、移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. クリック **[!UICONTROL New Report]**.
1. 選択 `Modules` から **[!UICONTROL Groups]** リスト。
1. クリック **[!UICONTROL Create]**.
1. レポートが生成されたら、「 **[!UICONTROL Select]** その後 **[!UICONTROL View]** を参照して、すべてのモジュールバージョンを確認します。
1. クリック **[!UICONTROL Download]** をクリックして、レポートをダウンロードします。

### システムレポートの管理

Adobe Analytics の **[!UICONTROL Action]** グリッドの列で、次のいずれかを選択します。

- `View`  — この関数を使用して、レポートの詳細を表示します。
- `Delete`  — この関数を使用して、生成されたレポートをリストから削除します。
- `Download`  — この関数を使用して、レポートをHTML・ファイルとして保存します。

### システムレポートの詳細を表示

1. 必要なレポートに対して、 **[!UICONTROL View]** （内） _[!UICONTROL Actions]_列。

1. 左側のパネルで、を展開します。 ![拡張セレクター](../assets/icon-display-expand.png) 詳細を表示するには、レポートの各セクションを参照してください。

   ![一般的なシステムレポート情報](./assets/report-information.png){width="600" zoomable="yes"}

### 使用可能なシステムレポート

| レポートグループ | 含まれる情報 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce版<br>データ数<br>キャッシュステータス<br>インデックスのステータス |
| [!UICONTROL Environment] | 環境情報<br>MySQL ステータス |
| [!UICONTROL Data] | URL キー別の重複カテゴリ<br>URL キーで製品を重複<br>SKU 別の製品の重複<br>増分 ID 別に注文を重複<br>メール別重複ユーザー数<br>破損したカテゴリデータ |
| [!UICONTROL Modules] | カスタムモジュールリスト<br>無効なモジュールリスト<br>すべてのモジュールリスト |
| [!UICONTROL Configuration] | 設定<br>データの取得元 `app/etc/env.php`<br>発送方法<br>支払い方法<br>支払機能マトリックス |
| [!UICONTROL Logs] | ログファイル<br>上位のシステムメッセージ<br>今日の上位のシステムメッセージ<br>上位のデバッグメッセージ<br>今日のトップデバッグメッセージ<br>上位の例外メッセージ<br>今日のトップ例外メッセージ |
| [!UICONTROL Attributes] | ユーザー定義 EAV 属性<br>新しい EAV 属性<br>エンティティタイプ<br>すべての EAV 属性<br>カテゴリ EAV 属性<br>製品 EAV 属性<br>顧客 EAV 属性<br>顧客アドレスの EAV 属性<br>RMA 品目 EAV 属性 |
| [!UICONTROL Events] | カスタムグローバルイベント<br>カスタム管理イベント<br>カスタムフロントエンドイベント<br>カスタムドキュメントイベント<br>カスタム Crontab イベント<br>カスタム REST イベント<br>カスタム SOAP イベント<br>コアグローバルイベント<br>コア管理者イベント<br>コアフロントエンドイベント<br>コアドキュメントイベント<br>コア Crontab イベント<br>コア REST イベント<br>コア SOAP イベント<br>すべてのグローバルイベント<br>すべての管理イベント<br>すべてのフロントエンドイベント<br>すべての Doc イベント<br>すべての REST イベント<br>すべての SOAP イベント<br>すべての Crontab イベント |
| [!UICONTROL Cron] | ステータスコード別の Cron スケジュール<br>ジョブコード別の Cron スケジュール<br>Cron スケジュールキューでのエラー<br>Cron スケジュールリスト<br>カスタムグローバル Cron ジョブ<br>カスタム設定可能な Cron ジョブ<br>コアグローバル Cron ジョブ<br>コア設定可能な Cron ジョブ<br>すべてのグローバル Cron ジョブ<br>すべての設定可能な Cron ジョブ |
| [!UICONTROL Design] | Adminhtml テーマリスト<br>フロントエンドテーマリスト |
| [!UICONTROL Stores] | Web サイトツリー<br>Web サイトリスト<br>ストアリスト<br>ストアビュー数リスト |
| OMS コネクタ&#x200B;<br>_（OMS 統合で表示）_ | コネクタのバージョン<br>コネクタの監視<br>メッセージの処理結果 |

{style="table-layout:auto"}
