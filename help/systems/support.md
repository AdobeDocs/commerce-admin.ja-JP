---
title: サポートツール
description: システムの問題を特定するために使用できる、提供されているサポートツールについて説明します。
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

データコレクターは、アドビのサポートチームがAdobe Commerceのインストールに関する問題のトラブルシューティングに必要な、お使いのシステムに関する情報を収集します。 作成されるバックアップは完了するまでに数分かかり、コードとデータベースダンプの両方が含まれます。 データは、CSV または Excel XML ファイルにエクスポートできます。

![システム – データコレクター](./assets/data-collector.png){width="600" zoomable="yes"}

### データコレクターの実行

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 右上隅のをクリックします。 **[!UICONTROL New Backup]**.

   バックアップの生成には数分かかります。 処理の結果を監視するには、次のボタンをクリックします。 **[!UICONTROL Refresh Status]**. 完了すると、バックアップがに表示されます _[!UICONTROL Data Collector]_グリッド。

1. バックアップの詳細を含むログを表示するには、次の手順を実行します。

   - が含まれる _[!UICONTROL Action]_列、選択&#x200B;**[!UICONTROL Show Log]**.

   - クリック **[!UICONTROL Back]** をクリックしてグリッドに戻ります。

   ![データ コレクタ ログ](./assets/data-collector-log.png){width="600" zoomable="yes"}

### バックアップデータの書き出し

1. 最初の列で、エクスポートするバックアップのチェックボックスを選択します。

1. の使用 **[!UICONTROL Export]** メニューを使用して、エクスポートデータの形式を選択します。

   ![書き出し形式](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Web ブラウザーのダウンロード場所からファイルにアクセスし、 **[!UICONTROL Save]** それ。

### バックアップデータのダウンロード

バックアップの生成後、コードと DB データのコピーをダウンロードできます。

1. グリッド内で必要なバックアップ図形を見つけます。

1. 次が含まれていることを確認します `Complete` ステータス。

1. でエンティティ名をクリックします。 _[!UICONTROL Code Dump]_または_[!UICONTROL DB Dump]_ 列。

ダウンロードプロセスが自動的に開始します。

## バックアップデータの削除

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. 削除するバックアップデータを検索して選択します。

1. が含まれる _[!UICONTROL Action]_列、クリック&#x200B;**[!UICONTROL Delete]**.

1. アクションを確定するには、 **[!UICONTROL OK]**.

## システムレポート

システムレポートツールを使用すると、システムのスナップショットを定期的に完全または部分的に作成し、後で参照するために保存できます。 コード開発サイクルの前後のパフォーマンス設定や、サーバー設定に対する変更を比較できます。 システムレポートツールを使用すると、調査を開始するためにサポートが必要とする情報の準備と送信に費やす時間を大幅に短縮できます。

システムレポートグリッドでは、既存のレポートの表示とダウンロード、レポートの削除、レポートの作成を行うことができます。

### システムレポートへのアクセス

日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![管理者 – システムレポート](./assets/reports.png){width="600" zoomable="yes"}

### レポートの生成

1. クリック **[!UICONTROL New Report]**.

1. が含まれる **[!UICONTROL Groups]** リストで、レポートに含める情報の各セットを選択します。 デフォルトでは、すべてのグループが選択されます。

   ![システムレポート – グループを選択](./assets/report-create.png){width="600" zoomable="yes"}

1. 右上隅のをクリックします。 **[!UICONTROL Create]**.

   選択したレポートタイプの数によっては、レポートの生成に数分かかることがあります。 レポートの準備が整うと、生成された日時と共にグリッドの上部に表示されます。

### モジュール情報の表示

インストールされているモジュールに関する有用な情報を確認できます。

**_インストールされている各モジュールのレポート情報を表示するには：_**

1. 日 _Admin_ サイドバー、に移動 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. クリック **[!UICONTROL New Report]**.
1. を選択 `Modules` から **[!UICONTROL Groups]** リスト。
1. クリック **[!UICONTROL Create]**.
1. レポートが生成されたら、 **[!UICONTROL Select]** その後 **[!UICONTROL View]** をクリックして、すべてのモジュールバージョンを表示します。
1. クリック **[!UICONTROL Download]** レポートをダウンロードします。

### システムレポートの管理

が含まれる **[!UICONTROL Action]** グリッドの列で、次のいずれかを選択します。

- `View`  – この関数を使用して、レポートの詳細を表示します。
- `Delete`  – この関数を使用して、生成されたレポートをリストから削除します。
- `Download`  – この関数を使用して、レポートをHTMLファイルとして保存します。

### システムレポートの詳細の表示

1. 必要なレポートで、 **[!UICONTROL View]** が含まれる _[!UICONTROL Actions]_列。

1. 左側のパネルで、を展開します ![展開セレクター](../assets/icon-display-expand.png) 詳細を表示するレポートの各セクション。

   ![一般的なシステムレポート情報](./assets/report-information.png){width="600" zoomable="yes"}

### 使用可能なシステムレポート

| レポートグループ | 含まれる情報 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerceのバージョン<br>データ数<br>キャッシュステータス<br>インデックスステータス |
| [!UICONTROL Environment] | 環境情報<br>MySQL ステータス |
| [!UICONTROL Data] | URL キー別に重複するカテゴリ<br>URL キーで製品を複製<br>SKU 別に製品を複製<br>増分 Id による重複注文<br>メールでユーザーを複製<br>カテゴリデータの破損 |
| [!UICONTROL Modules] | カスタムモジュールリスト<br>無効なモジュール リスト<br>すべてのモジュールリスト |
| [!UICONTROL Configuration] | 設定<br>からのデータ `app/etc/env.php`<br>発送方法<br>支払い方法<br>支払機能マトリックス |
| [!UICONTROL Logs] | ログファイル<br>上位のシステムメッセージ<br>今日の上位のシステムメッセージ<br>上位のデバッグメッセージ<br>今日の上位のデバッグメッセージ<br>上位の例外メッセージ<br>今日の上位の例外メッセージ |
| [!UICONTROL Attributes] | ユーザー定義の EAV 属性<br>新しい EAV 属性<br>エンティティタイプ<br>すべての EAV 属性<br>カテゴリ EAV 属性<br>製品 EAV 属性<br>顧客 EAV 属性<br>顧客の住所 EAV 属性<br>RMA 品目 EAV 属性 |
| [!UICONTROL Events] | カスタムグローバルイベント<br>カスタム管理イベント<br>カスタムフロントエンドイベント<br>カスタム ドキュメント イベント<br>カスタム Crontab イベント<br>カスタム REST イベント<br>カスタム SOAP イベント<br>主要なグローバルイベント<br>コア管理イベント<br>コアフロントエンドイベント<br>コアドキュメントイベント<br>コア Crontab イベント<br>コア REST イベント<br>コア SOAP イベント<br>すべてのグローバル イベント<br>すべての管理イベント<br>すべてのフロントエンドイベント<br>すべてのドキュメント イベント<br>すべての REST イベント<br>すべての SOAP イベント<br>すべての Crontab イベント |
| [!UICONTROL Cron] | ステータスコード別 Cron スケジュール<br>ジョブコード別の Cron スケジュール<br>Cron スケジュールキューのエラー<br>Cron スケジュールリスト<br>カスタム Global Cron ジョブ<br>カスタム設定可能な Cron ジョブ<br>コア Global Cron ジョブ<br>コア設定可能な Cron ジョブ<br>すべての Global Cron ジョブ<br>設定可能なすべての Cron ジョブ |
| [!UICONTROL Design] | Adminhtml テーマリスト<br>フロントエンドテーマリスト |
| [!UICONTROL Stores] | Web サイトツリー<br>Web サイトリスト<br>ストアリスト<br>表示リストの保存 |
| OMS コネクタ&#x200B;<br>_（OMS 統合で表示）_ | コネクタのバージョン<br>コネクタの監視<br>メッセージ処理の結果 |

{style="table-layout:auto"}
