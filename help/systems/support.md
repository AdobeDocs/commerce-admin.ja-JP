---
title: サポートツール
description: システムの問題を特定するために使用できるサポートツールについて説明します。
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="PaaSのみ" type="Informative" url="https://experienceleague.adobe.com/ja/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud プロジェクト（Adobeで管理されるPaaS インフラストラクチャ）とオンプレミス プロジェクトにのみ適用されます。"
source-git-commit: ea62a4a901ed3e8e91332f742ebb53fe58be706d
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# サポートツール

{{ee-feature}}

サポートツールは、システム内の既知の問題を特定するために設計されています。 開発および最適化プロセスのリソースとして、またサポートチームが問題を特定して解決するための診断ツールとして使用できます。

## システムレポート

システムレポートツールを使用すると、システムの定期的な完全または部分的なスナップショットを取得し、後で参照するために保存できます。 コード開発サイクルの前後のパフォーマンス設定、またはサーバー設定の変更を比較できます。 システムレポートツールは、調査を開始するためにサポートが必要とする情報の準備と提出にかかる時間を大幅に短縮することができます。

「システムレポート」グリッドから、既存のレポートの表示とダウンロード、レポートの削除、レポートの作成を行うことができます。

### システムレポートへのアクセス

_管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**&#x200B;に移動します。

![管理者 – システムレポート &#x200B;](./assets/reports.png){width="600" zoomable="yes"}

### レポートの生成

1. **[!UICONTROL New Report]**&#x200B;をクリックします。

1. **[!UICONTROL Groups]** リストで、レポートに含める各情報セットを選択します。 デフォルトでは、すべてのグループが選択されています。

   ![&#x200B; システムレポート – グループの選択](./assets/report-create.png){width="600" zoomable="yes"}

1. 右上隅の「**[!UICONTROL Create]**」をクリックします。

   選択したレポートタイプの数によっては、レポートが生成されるまでに数分かかる場合があります。 レポートの準備が整うと、生成された日時とともにグリッドの上部に表示されます。

### モジュール情報を表示

インストールされているモジュールに関する有用な情報を見つけることができます。

**_インストールされている各モジュールのレポート情報を表示するには:_**

1. _管理者_ サイドバーで、**[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**&#x200B;に移動します。
1. **[!UICONTROL New Report]**&#x200B;をクリックします。
1. **[!UICONTROL Groups]** リストから`Modules`を選択します。
1. **[!UICONTROL Create]**&#x200B;をクリックします。
1. レポートが生成されたら、**[!UICONTROL Select]**&#x200B;をクリックし、**[!UICONTROL View]**&#x200B;をクリックしてすべてのモジュールバージョンを表示します。
1. レポートをダウンロードするには、**[!UICONTROL Download]**&#x200B;をクリックします。

### システムレポートの管理

グリッドの&#x200B;**[!UICONTROL Action]**&#x200B;列で、次のいずれかを選択します。

- `View` – この関数を使用して、レポートの詳細を表示します。
- `Delete` – 生成されたレポートをリストから削除するには、この関数を使用します。
- `Download` – この関数を使用して、レポートをHTML ファイルとして保存します。

### システムレポートの詳細を表示

1. 必要なレポートについては、_[!UICONTROL Actions]_&#x200B;列の&#x200B;**[!UICONTROL View]**&#x200B;を選択してください。

1. 左側のパネルで、レポートの各セクションを![拡張セレクター](../assets/icon-display-expand.png)展開して、詳細を表示します。

   ![一般的なシステムレポート情報](./assets/report-information.png){width="600" zoomable="yes"}

### 利用可能なシステムレポート

| レポートグループ | 含まれる情報 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce Version<br>Data Count<br> キャッシュステータス <br>Index Status |
| [!UICONTROL Environment] | 環境情報<br>MySQL ステータス |
| [!UICONTROL Data] | URL キーでカテゴリを複製<br>URL キーで製品を複製<br>SKUで製品を複製<br> インクリメント Idで注文を複製<br> メールでユーザーを複製<br>壊れたカテゴリーデータ |
| [!UICONTROL Modules] | カスタムモジュールリスト <br>無効なモジュールリスト <br>すべてのモジュールリスト |
| [!UICONTROL Configuration] | `app/etc/env.php`<br>配送方法<br>支払い方法<br>支払い機能マトリックスからの設定<br> データ |
| [!UICONTROL Logs] | ログファイル <br>上位のシステムメッセージ <br>今日の上位のシステムメッセージ <br>上位のデバッグメッセージ <br>今日の上位のデバッグメッセージ <br>上位の例外メッセージ <br>今日の上位の例外メッセージ |
| [!UICONTROL Attributes] | ユーザー定義EAV属性<br>新しいEAV属性<br> エンティティタイプ <br>すべてのEAV属性<br> カテゴリーEAV属性<br>製品EAV属性<br>顧客EAV属性<br>顧客アドレス EAV属性<br>RMA項目EAV属性 |
| [!UICONTROL Events] | カスタムグローバルイベント <br> カスタム管理イベント <br> カスタムフロントエンドイベント <br> カスタムドキュメントイベント <br> カスタム Crontab イベント <br> カスタム REST イベント <br> カスタム SOAP イベント <br> コア管理イベント <br> コア管理イベント <br> コア管理イベント <br> コア管理イベント <br> コア REST イベント <br> コア SOAP イベント <br>すべてのグローバルイベント <br>すべての管理イベント <br>すべてのフロントエンドイベント {All REST イベント <br>すべてのSOAP}すべてのREST イベント イベント <br>すべてのCrontab イベント<br><br><br> |
| [!UICONTROL Cron] | ステータスコード別のCron スケジュール <br> ジョブコード別のCron スケジュール <br>Cron スケジュールキューのエラー<br>Cron スケジュールリスト <br> カスタムのグローバル Cron ジョブ <br> カスタム設定可能なCron ジョブ <br> コアのグローバル Cron ジョブ <br> コア設定可能なCron ジョブ <br>すべてのグローバル Cron ジョブ <br>すべての設定可能なCron ジョブ |
| [!UICONTROL Design] | Adminhtml テーマ リスト <br> フロントエンド テーマ リスト |
| [!UICONTROL Stores] | Web サイトツリー<br>Web サイトリスト <br> ストアリスト <br> ストアビューリスト |
| OMS コネクタ <br>_（OMS統合で表示）_ | コネクタバージョン <br> コネクタ監視<br> メッセージ処理結果 |

{style="table-layout:auto"}
